---
description: Il campo della crittografia è di grandi dimensioni e in crescita.
ms.assetid: ec50d6f1-999d-4ce9-85b4-816afb17550e
title: Tipi di provider del servizio di crittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aaeee585ff9c11e2a20a201f541f3cd147aef6e9b50c37d60156e75a1b9fd94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876211"
---
# <a name="cryptographic-provider-types"></a>Tipi di provider del servizio di crittografia

Il campo della [*crittografia è di*](../secgloss/c-gly.md) grandi dimensioni e in crescita. Esistono molti protocolli e formati di dati standard diversi. Queste sono in genere organizzate in gruppi o famiglie, ognuna delle quali ha un proprio set di formati di dati e modalità di eseguire le operazioni. Anche se due famiglie usano lo stesso algoritmo (ad esempio, la [](../secgloss/p-gly.md) crittografia a [](../secgloss/k-gly.md)blocchi [*RC2),*](../secgloss/r-gly.md) [](../secgloss/b-gly.md)spesso useranno schemi di spaziatura interna diversi, lunghezze di chiave diverse e modalità predefinite diverse. CryptoAPI è progettato in modo che un tipo di provider CSP rappresenti una famiglia specifica.

Quando un'applicazione si connette a un provider di servizi di configurazione di un determinato tipo, ognuna delle funzioni CryptoAPI funzionerà, per impostazione predefinita, in modo prescritto dalla famiglia che corrisponde a tale tipo CSP. La scelta del tipo di provider di un'applicazione specifica gli elementi seguenti:



| Elemento                                                                                                                                | Descrizione                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*Algoritmo di scambio di chiavi*](../secgloss/k-gly.md)                | Ogni tipo di provider specifica un solo algoritmo di scambio di chiavi. Ogni provider CSP di un determinato tipo deve implementare questo algoritmo. Le applicazioni specificano l'algoritmo di scambio delle chiavi da usare selezionando un provider CSP del tipo di provider appropriato.                                                        |
| [*Algoritmo di firma digitale*](../secgloss/d-gly.md) | Ogni tipo di provider specifica un solo algoritmo di firma digitale. Ogni provider CSP di un determinato tipo deve implementare questo algoritmo. Le applicazioni specificano l'algoritmo di firma digitale da usare selezionando un provider CSP del tipo di provider appropriato.                                              |
| Formati BLOB chiave                                                                                                                    | Il tipo provide determina il formato del [*BLOB di*](../secgloss/k-gly.md) chiavi usato per esportare le chiavi dal [*provider di*](../secgloss/c-gly.md) servizi di crittografia e per importare le chiavi in un provider di servizi di configurazione. |
| Formato della firma digitale                                                                                                            | Il tipo di provider determina il formato della firma digitale. Ciò garantisce che una firma prodotta da un provider CSP di un determinato tipo di provider possa essere verificata da qualsiasi provider CSP dello stesso tipo di provider.                                                                                                              |
| Schema di derivazione della chiave di sessione                                                                                                       | Il tipo di provider determina il metodo utilizzato per derivare una [*chiave di sessione*](../secgloss/s-gly.md) da un [*hash*](../secgloss/h-gly.md).                                                                                   |
| [*Lunghezza chiave*](../secgloss/k-gly.md)                                                    | Alcuni tipi di provider specificano la lunghezza delle [*coppie di chiavi pubbliche/private*](../secgloss/p-gly.md) e le chiavi di sessione.                                                                                                               |
| Modalità predefinite                                                                                                                       | Il tipo di provider spesso specifica le modalità predefinite per varie opzioni, ad esempio la modalità [*di*](../secgloss/c-gly.md) crittografia a blocchi o il metodo di riempimento della crittografia [*a*](../secgloss/p-gly.md) blocchi.          |



 

Alcune applicazioni avanzate potrebbero connettersi a più CSP alla volta, ma la maggior parte delle applicazioni in genere usa un solo provider di servizi di configurazione.

Attualmente sono disponibili diversi tipi di provider predefiniti. Le sezioni successive forniscono informazioni sui tipi di provider seguenti:

-   [PROV \_ RSA \_ FULL](prov-rsa-full.md)
-   [PROV \_ RSA \_ AES](prov-rsa-aes.md)
-   [PROV \_ RSA \_ SIG](prov-rsa-sig.md)
-   [PROV \_ RSA \_ SCHANNEL](prov-rsa-schannel.md)
-   [PROV \_ DSS](prov-dss.md)
-   [PROV \_ DSS \_ DH](prov-dss-dh.md)
-   [PROV \_ DH \_ SCHANNEL](prov-dh-schannel.md)
-   [PROV \_ FORTEZZA](prov-fortezza.md)
-   [PROV \_ MS \_ EXCHANGE](prov-ms-exchange.md)
-   [PROV \_ SSL](prov-ssl.md)

Anche se alcuni tipi CSP potrebbero essere parzialmente compatibili con altri, due o più applicazioni che devono scambiare chiavi e messaggi crittografati devono usare CSP dello stesso tipo. [](../secgloss/e-gly.md)

Un writer CSP personalizzato può definire un nuovo tipo di provider. Tuttavia, il writer CSP è quindi responsabile della distribuzione del nuovo tipo di provider agli autori di tutte le applicazioni che lo usano. Per informazioni sulla scrittura di provider di servizi di crittografia personalizzati, vedere [Provider del servizio di crittografia](cryptographic-service-providers.md).

 

 
