
Color logs

add the following in your ~/.bashrc

``
alias fixcolor="awk '/35=R/ {print \"\033[32m\" \$0 \"\033[39m\"; next} /35=S/ {print \"\033[31m\" \$1 \"\033[39m\"; next} 1'"
``

Load the changes

``
source ~/.bashrc
``

use it as following 

``
tailf FIXT.1.1-SGBTLZ-SGCIB.messages.log | fixcolor
``
