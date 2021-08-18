---
description: Il router a più provider chiama NPGetCaps per individuare quando verranno avviati i provider di rete (nIndex è impostato su WNNC \_ START).
ms.assetid: f57bd8ff-647d-42f8-abaf-7937b24416dd
title: Override dell'intervallo di timeout MPR predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51c2c9db2fb892b7c2fc9646a9328fb9de4b7f9782ff5204ed261b16471ca4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921135"
---
# <a name="overriding-the-default-mpr-time-out-interval"></a>Override dell'intervallo di timeout MPR predefinito

Il [*router a più provider*](../secgloss/m-gly.md) chiama [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) per individuare quando verranno avviati i provider di rete (*nIndex* è impostato su WNNC \_ START). L'MPR attende quindi il periodo di timeout più lungo specificato da tutti i provider di rete prima di presentarla all'utente. Se uno dei provider di rete non sa quando verrà avviato, MPR usa un timeout predefinito di 60 secondi per tale provider.

Se necessario, l'amministratore può eseguire l'override del timeout predefinito creando il timeout del Registro di sistema **\_ REG DWORD** seguente, dove *n* è l'intervallo di timeout in millisecondi:

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ **RestoreTimeout**  =  *n*

Lo pseudocodice seguente illustra il flusso logico completo per la gestione del timeout da parte della richiesta di ripristino di microsoft.


```C++
If there is a RegistryTimeout,
Then MaxTimeout = RegistryTimeout.
Otherwise,
MaxTimeout = 0.
For each provider,
if the provider does not supply a time-out and
if there is a RegistryTimeout,
ProviderTimeout is set to RegistryTimeout.
Otherwise,
ProviderTimeout is set to DefaultTimeout.
Otherwise,
If the ProviderTimeout is longer than MaxTimeout,
MaxTimeout = ProviderTimeout.
```



 

 
