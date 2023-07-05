# dockerfile_lol

#!/bin/bash

# Run component 1
ruby component1.rb &

# Run component 2
ruby component2.rb &

# Run component 3
ruby component3.rb &

# Wait for all components to finish
wait

COPY run_components.sh /app/run_components.sh
RUN chmod +x /app/run_components.sh

CMD ["/app/run_components.sh"]
