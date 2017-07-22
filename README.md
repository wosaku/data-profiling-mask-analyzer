# Data Profilig Mask Analyzer


A python custom function to generate a mask analysis.


The mask analysis or string pattern is useful for fields like city, postal code, phone, etc. It shows us how the fields have been populated and we can infer some data quality issues.


Rules: 
  * lower case letter returns 'l'
  * Capital case letter returns 'L'
  * Number returns 'D'
  * Space returns 's'
  * Special character returns itself
  * Missing value returns '-null-'


Examples:
  * 'Van' returns 'Lll'
  * 'VAN' returns 'LLL'
  * 'Van BC' returns 'LllsLL'
  * '+1 123-1234-5555 returns '+DsDDD-DDDD-DDDD'
  * The standard for the Canadian Postal Code should be 'LDLsDLD'