# voting_assignment

Putty not working, got new instance running on my master's device(Ankit Kumar Pathak)

Observations:
1. While applying the yaml files, got error in creation of vote and result pod that the ports were busy. So, made changes in the vote.yaml and result.yaml file, by changing the ports
Voting page: http://3.1.204.85:31005/
Result Page: http://3.1.204.85:31006/
3. On deleting Vote pod, a new vote pod is created and application runs normally.
4. On deleting worker pod, new worker pod gets created and application runs normally
5. On deleting DB pod, application stops recording the response and we get an error of socket missing.
6. To solve this problem, we need to restart the result pod which inturns creates a new db pod and our application return backs to normal.
