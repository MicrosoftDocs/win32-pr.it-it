---
description: Il campo della crittografia è di grandi dimensioni e in continua crescita.
ms.assetid: ec50d6f1-999d-4ce9-85b4-816afb17550e
title: Tipi di provider di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e976909cec25b5194187d61d2e753eeb830c09f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750914"
---
# <a name="cryptographic-provider-types"></a>Tipi di provider di crittografia

Il campo della [*crittografia*](../secgloss/c-gly.md) è di grandi dimensioni e in continua crescita. Sono disponibili molti diversi protocolli e formati di dati standard. Questi sono in genere organizzati in gruppi o famiglie, ognuno dei quali ha un proprio set di formati di dati e un modo per eseguire operazioni. Anche se due famiglie utilizzano lo stesso algoritmo, ad esempio la [*crittografia a blocchi*](../secgloss/b-gly.md) [*RC2*](../secgloss/r-gly.md) , spesso utilizzeranno schemi di [*riempimento*](../secgloss/p-gly.md) diversi, [*lunghezze di chiave*](../secgloss/k-gly.md)diverse e modalità predefinite diverse. CryptoAPI è progettato in modo che un tipo di provider CSP rappresenti una famiglia particolare.

Quando un'applicazione si connette a un CSP di un determinato tipo, per impostazione predefinita ogni funzione CryptoAPI viene eseguita in base a quanto previsto dalla famiglia corrispondente a tale tipo di CSP. La scelta del tipo di provider di un'applicazione specifica gli elementi seguenti:



| Elemento                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*Algoritmo di scambio delle chiavi*](../secgloss/k-gly.md)                | Ogni tipo di provider specifica un solo algoritmo di scambio di chiave. Ogni CSP di un determinato tipo deve implementare questo algoritmo. Le applicazioni specificano l'algoritmo di scambio delle chiavi da usare selezionando un CSP del tipo di provider appropriato.                                                        |
| [*Algoritmo di firma digitale*](../secgloss/d-gly.md) | Ogni tipo di provider specifica un solo algoritmo di firma digitale. Ogni CSP di un determinato tipo deve implementare questo algoritmo. Le applicazioni specificano l'algoritmo di firma digitale da usare selezionando un CSP del tipo di provider appropriato.                                              |
| Formati BLOB principali                                                                                                                    | Il tipo di specifica determina il formato del [*BLOB della chiave*](../secgloss/k-gly.md) utilizzato per esportare le chiavi dal [*CSP*](../secgloss/c-gly.md) e per importare le chiavi in un CSP. |
| Formato firma digitale                                                                                                            | Il tipo di provider determina il formato della firma digitale. In questo modo si garantisce che una firma prodotta da un CSP di un determinato tipo di provider possa essere verificata da qualsiasi CSP dello stesso tipo di provider.                                                                                                              |
| Schema di derivazione della chiave della sessione                                                                                                       | Il tipo di provider determina il metodo utilizzato per derivare una [*chiave di sessione*](../secgloss/s-gly.md) da un [*hash*](../secgloss/h-gly.md).                                                                                   |
| [*Lunghezza chiave*](../secgloss/k-gly.md)                                                    | Alcuni tipi di provider specificano la lunghezza delle coppie di chiavi [*pubbliche/private*](../secgloss/p-gly.md) e delle chiavi di sessione.                                                                                                               |
| Modalità predefinite                                                                                                                       | Il tipo di provider spesso specifica le modalità predefinite per le varie opzioni, ad esempio la [*modalità*](../secgloss/c-gly.md) di crittografia a blocchi o il metodo di [*riempimento*](../secgloss/p-gly.md) della crittografia a blocchi.          |



 

Alcune applicazioni avanzate potrebbero connettersi a più CSP alla volta, ma la maggior parte delle applicazioni usa in genere solo un singolo CSP.

Attualmente sono disponibili numerosi tipi di provider predefiniti. Nelle sezioni successive vengono fornite informazioni sui tipi di provider seguenti:

-   [PROV \_ RSA \_ completo](prov-rsa-full.md)
-   [PROVA \_ \_ AES RSA](prov-rsa-aes.md)
-   [PROVA \_ RSA \_ sig](prov-rsa-sig.md)
-   [DIMOSTRAZIONE di \_ RSA \_ Schannel](prov-rsa-schannel.md)
-   [PROVA \_ DSS](prov-dss.md)
-   [PROVA \_ DSS \_ DH](prov-dss-dh.md)
-   [PROV \_ DH \_ Schannel](prov-dh-schannel.md)
-   [PROVA \_ fortezza](prov-fortezza.md)
-   [PROVA \_ MS \_ Exchange](prov-ms-exchange.md)
-   [PROVA \_ SSL](prov-ssl.md)

Anche se alcuni tipi CSP potrebbero essere parzialmente compatibili con altri, due o più applicazioni che devono [*scambiare chiavi*](../secgloss/e-gly.md) e messaggi crittografati devono usare CSP dello stesso tipo.

Un writer CSP personalizzato può definire un nuovo tipo di provider. Tuttavia, il writer CSP è quindi responsabile della distribuzione del nuovo tipo di provider agli autori di qualsiasi applicazione che lo utilizzerà. Per informazioni sulla scrittura di CSP personalizzati, vedere [provider del servizio di crittografia](cryptographic-service-providers.md).

 

 
