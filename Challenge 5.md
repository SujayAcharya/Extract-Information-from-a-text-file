# Extract-Information-from-a-text-file
# Questions
1. Extract log.tar.gz
    
    ==> tar -xvf log.tar.gz
 
2. Look for unauthorized connection attempts

    ==> less auth.log

3. Extract the username an attacker tried to use

    ==> cat auth.log | grep "input_userauth_request" |awk '{print $9}'

4. Create a file containing these names (and make it organized)

    ==> cat auth.log | grep "input_userauth_request" |awk '{print $9}' | sort -u > users.txt
