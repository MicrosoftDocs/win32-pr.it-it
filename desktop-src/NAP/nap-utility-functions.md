---
title: Funzioni di utilità NAP
description: Le funzioni di utilità seguenti supportano l'API NAP.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c423909011c81f52ea89ce8d3137b35c55167
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709799"
---
# <a name="nap-utility-functions"></a>Funzioni di utilità NAP

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Le funzioni di utilità seguenti supportano l'API NAP.

Tutte le interfacce COM supportate dal sistema NAP utilizzano le regole di gestione della memoria COM standard e l'allocatore di memoria COM (CoTaskMemAlloc e CoTaskMemFree).

-   IN Parameters-allocato e liberato dal chiamante.
-   Parametri OUT, allocati dal chiamato, liberati dal chiamante tramite CoTaskMem \* ()
-   Parametri IN/OUT, allocati dal chiamante, liberati e riallocati dal chiamato, infine liberati dal chiamante, utilizzando CoTaskMem \* ()

Nelle funzioni FreeXxx () verranno liberati anche tutti i puntatori incorporati.

-   [**AllocConnections**](allocconnections-func.md)
-   [**AllocCountedString**](alloccountedstring-func.md)
-   [**AllocFixupInfo**](allocfixupinfo-func.md)
-   [**FreeConnections**](freeconnections-func.md)
-   [**FreeCountedString**](freecountedstring-func.md)
-   [**FreeFixupInfo**](freefixupinfo-func.md)
-   [**FreeIsolationInfo**](freeisolationinfo-func.md)
-   [**FreeIsolationInfoEx**](freeisolationinfoex.md)
-   [**FreeNapComponentRegistrationInfoArray**](freenapcomponentregistrationinfoarray-func.md)
-   [**FreeNetworkSoH**](freenetworksoh-func.md)
-   [**FreePrivateData**](freeprivatedata-func.md)
-   [**FreeSoH**](freesoh-func.md)
-   [**FreeSoHAttributeValue**](freesohattributevalue-func.md)
-   [**FreeSystemHealthAgentState**](freesystemhealthagentstate-func.md)
-   [**InitializeNapAgentNotifier**](initializenapagentnotifier.md)
-   [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md)

 

 




