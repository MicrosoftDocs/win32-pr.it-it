---
description: Il router multi-provider (MPR) chiama NPGetCaps per scoprire quando vengono avviati i provider di rete (nIndex è impostato su WNNC \_ Start).
ms.assetid: f57bd8ff-647d-42f8-abaf-7937b24416dd
title: Sostituzione dell'intervallo di timeout predefinito di MPR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4308d94f4b16a7f67786c8a0856f23922e6f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968086"
---
# <a name="overriding-the-default-mpr-time-out-interval"></a>Sostituzione dell'intervallo di timeout predefinito di MPR

Il [*router multi-provider*](../secgloss/m-gly.md) (MPR) chiama [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) per scoprire quando vengono avviati i provider di rete (*nIndex* è impostato su WNNC \_ Start). Il MPR attende quindi il periodo di timeout più lungo specificato da tutti i provider di rete prima di presentare la rete consolidata all'utente. Se uno dei provider di rete non è a conoscenza del momento in cui viene avviato, MPR utilizza un timeout predefinito di 60 secondi per il provider.

Se necessario, l'amministratore può eseguire l'override del timeout predefinito creando il seguente timeout del registro di sistema **reg \_ DWORD** , dove *n* è l'intervallo di timeout in millisecondi:

**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ **RestoreTimeout**  =  *n*

Lo pseudocodice seguente illustra il flusso di logica completo per la gestione del timeout da parte di MPR.


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



 

 
