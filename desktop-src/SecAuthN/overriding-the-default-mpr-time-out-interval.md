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
# <a name="overriding-the-default-mpr-time-out-interval"></a><span data-ttu-id="ddd7a-103">Sostituzione dell'intervallo di timeout predefinito di MPR</span><span class="sxs-lookup"><span data-stu-id="ddd7a-103">Overriding the Default MPR Time-out Interval</span></span>

<span data-ttu-id="ddd7a-104">Il [*router multi-provider*](../secgloss/m-gly.md) (MPR) chiama [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) per scoprire quando vengono avviati i provider di rete (*nIndex* è impostato su WNNC \_ Start).</span><span class="sxs-lookup"><span data-stu-id="ddd7a-104">The [*Multiple Provider Router*](../secgloss/m-gly.md) (MPR) calls [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) to find out when the network providers will start (*nIndex* is set to WNNC\_START).</span></span> <span data-ttu-id="ddd7a-105">Il MPR attende quindi il periodo di timeout più lungo specificato da tutti i provider di rete prima di presentare la rete consolidata all'utente.</span><span class="sxs-lookup"><span data-stu-id="ddd7a-105">The MPR then waits for the longest time-out period specified by all network providers before it presents the consolidated network to the user.</span></span> <span data-ttu-id="ddd7a-106">Se uno dei provider di rete non è a conoscenza del momento in cui viene avviato, MPR utilizza un timeout predefinito di 60 secondi per il provider.</span><span class="sxs-lookup"><span data-stu-id="ddd7a-106">If one of the network providers does not know when it will start, MPR uses a default time-out of 60 seconds for that provider.</span></span>

<span data-ttu-id="ddd7a-107">Se necessario, l'amministratore può eseguire l'override del timeout predefinito creando il seguente timeout del registro di sistema **reg \_ DWORD** , dove *n* è l'intervallo di timeout in millisecondi:</span><span class="sxs-lookup"><span data-stu-id="ddd7a-107">If necessary, the administrator can override the default time-out by creating the following **REG\_DWORD** registry time-out, where *n* is the time-out interval in milliseconds:</span></span>

<span data-ttu-id="ddd7a-108">**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ **RestoreTimeout**  =  *n*</span><span class="sxs-lookup"><span data-stu-id="ddd7a-108">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**RestoreTimeout** = *n*</span></span>

<span data-ttu-id="ddd7a-109">Lo pseudocodice seguente illustra il flusso di logica completo per la gestione del timeout da parte di MPR.</span><span class="sxs-lookup"><span data-stu-id="ddd7a-109">The following pseudocode shows the complete logic flow for time-out handling by the MPR.</span></span>


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



 

 
