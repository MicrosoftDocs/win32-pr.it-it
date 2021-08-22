---
title: Funzioni dell'utilità Protezione accesso alla rete
description: Le funzioni di utilità seguenti supportano l'API protezione accesso alla rete.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9b421069804a4047b511b775c7ffafe5b4b987eb0b0ad5105f48df0ed990e22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620782"
---
# <a name="nap-utility-functions"></a>Funzioni dell'utilità Protezione accesso alla rete

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Le funzioni di utilità seguenti supportano l'API protezione accesso alla rete.

Tutte le interfacce COM supportate dal sistema nap usano le regole di gestione della memoria COM standard e l'allocatore di memoria COM (CoTaskMemAlloc e CoTaskMemFree).

-   Parametri IN: allocati e liberati dal chiamante.
-   Parametri OUT: allocati dal chiamato, liberati dal chiamante usando CoTaskMem \* ()
-   Parametri IN/OUT: allocati dal chiamante, liberati e riallocati dal chiamato, infine liberati dal chiamante, usando CoTaskMem \* ()

Nelle funzioni FreeXxx() verranno liberati anche tutti i puntatori incorporati.

-   [**AllocConnections**](allocconnections-func.md)
-   [**AllocCountedString**](alloccountedstring-func.md)
-   [**AllocFixupInfo**](allocfixupinfo-func.md)
-   [**Connessioni gratuite**](freeconnections-func.md)
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

 

 




