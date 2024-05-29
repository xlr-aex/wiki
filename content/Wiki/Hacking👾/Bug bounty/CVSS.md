The **Common Vulnerability Scoring System** (**CVSS**) is a free and [open](https://en.wikipedia.org/wiki/Open_standard "Open standard") [industry standard](https://en.wikipedia.org/wiki/Technical_standard "Technical standard") for assessing the severity of [computer system security](https://en.wikipedia.org/wiki/Computer_security "Computer security") [vulnerabilities](https://en.wikipedia.org/wiki/Vulnerability_(computing) "Vulnerability (computing)"). CVSS attempts to assign severity scores to vulnerabilities, allowing responders to prioritize responses and resources according to threat. Scores are calculated based on a formula that depends on several [metrics](https://en.wikipedia.org/wiki/Software_metric "Software metric"), that approximate ease and impact of an exploit. Scores range from 0 to 10, with 10 being the most severe. While many utilize only the CVSS Base score for determining severity, temporal and environmental scores also exist, to factor in availability of mitigations and how widespread vulnerable systems are within an organization, respectively.

https://www.first.org/cvss/calculator/3.0

  
Le CVSS (Common Vulnerability Scoring System) est un cadre standardisé pour évaluer la gravité des vulnérabilités de sécurité informatique. Les scores CVSS sont divisés en trois catégories : Base, Temporel, et Environnemental.

1. **CVSS de Base** : Ils évaluent la gravité intrinsèque d'une vulnérabilité, indépendamment de tout contexte extérieur. Ils se concentrent sur des facteurs tels que la complexité de l'exploitation, l'impact sur la confidentialité, l'intégrité, et la disponibilité, et si des privilèges sont nécessaires pour exploiter la vulnérabilité.
    
2. **CVSS Temporel** : Ils modifient le score de base en fonction de facteurs qui changent avec le temps, comme la disponibilité d'un exploit ou l'existence de correctifs.
    
3. **CVSS Environnemental** : Ces scores personnalisent les scores de base et temporel en tenant compte des caractéristiques uniques de l'environnement d'une organisation. Cela inclut la pertinence de la vulnérabilité pour l'environnement spécifique, les contre-mesures existantes, et l'importance des ressources affectées. Par exemple, une vulnérabilité dans un logiciel rarement utilisé dans une organisation aura un score environnemental plus bas, tandis qu'une faille dans un système critique aura un score plus élevé.
    

Dans le cadre du bug bounty, l'importance des scores CVSS environnementaux est significative. Alors que les scores de base et temporel fournissent une évaluation générale de la vulnérabilité, les scores environnementaux permettent aux chercheurs en cybersécurité et aux organisations de prioriser les vulnérabilités en fonction de leur impact spécifique sur leur propre environnement. Cela permet une allocation plus efficace des ressources pour les correctifs et les mesures de mitigation, en se concentrant sur les vulnérabilités qui posent le plus grand risque pour leur environnement particulier.

https://www.balbix.com/insights/environmental-cvss-scores/

