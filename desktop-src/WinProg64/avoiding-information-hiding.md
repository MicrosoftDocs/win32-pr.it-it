---
title: Evitare le informazioni nascoste
description: Occasionalmente, i programmi nascondono intenzionalmente o inavvertitamente le informazioni dal motore di marshalling RPC.
ms.assetid: 016b9221-092d-4c25-a396-4f41dcdfb3cf
keywords:
- Programmazione Windows con compatibilità con le versioni precedenti a 64 bit
- problemi di compatibilità programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4b9e4ba7ed5165378beb93005243af03f9e469
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399287"
---
# <a name="avoiding-information-hiding"></a>Evitare le informazioni nascoste

Occasionalmente, i programmi nascondono intenzionalmente o inavvertitamente le informazioni dal motore di marshalling RPC. Di seguito sono riportati alcuni esempi:

-   Invio di una struttura di dati come blocco di byte non differenziato
-   Sfruttando le prestazioni usando un effetto collaterale di un metodo per il canale di dati aggiuntivi attraverso la rete
-   Tentativo di mascherare un handle passandolo come **valore DWORD** o **ULONG**

Queste tecniche sono quasi garantite per introdurre problemi di compatibilità anche prima di trasferire l'applicazione in Windows a 64 bit.

Anziché inviare un contesto server come **DWORD** in una chiamata di procedura remota standard, utilizzare un handle di contesto per fornire un handle opaco a un contesto server che viene mantenuto per conto di un client. I contesti vengono identificati dai GUID definiti dalla fase di esecuzione RPC quando un server crea un handle di contesto per un client. Nessun puntatore viene utilizzato in transito e l'operazione è completamente trasparente nei limiti 32 o 64 bit. Per altre informazioni sull'uso degli handle di contesto, vedere [handle di contesto](/windows/desktop/Rpc/context-handles).

Le interfacce DCOM non possono utilizzare handle di contesto poiché COM fornisce la propria gestione del contesto. Anziché creare un handle di contesto, è possibile passare un puntatore di interfaccia all'oggetto COM. È quindi possibile chiamare i metodi direttamente tramite il puntatore di interfaccia o posizionare il puntatore all'interno di altre chiamate. Per rilasciare l'oggetto server, il client chiama il metodo di **rilascio** dell'interfaccia tramite il puntatore di interfaccia.

Anche in questo caso, è possibile che non sia possibile modificare la progettazione originale del codice che si sta trasportando. Se non esiste alcun modo per evitare di inviare un puntatore attraverso la rete come **DWORD**, sarà necessario implementare una forma di mapping lato server tra i valori **DWORD** e i puntatori. Un modo per eseguire questa operazione consiste nel modificare i puntatori nell'applicazione lato client in tipi di precisione puntatore, ad esempio **ULONG \_ ptr** o **DWORD \_ ptr**. Usare quindi la \[ [**chiamata MIDL \_ come**](/windows/desktop/Midl/call-as) \] attributo per inserire i puntatori in transito come valori **DWORD** . Il wrapper lato client deve passare solo gli argomenti insieme a. Il wrapper lato server gestisce il mapping tra entrambi i tipi. In modo analogo, è possibile usare l'attributo \[ [**trasmissione \_ As**](/windows/desktop/Midl/transmit-as) \] o l'attributo \[ [**rappresenta \_ come**](/windows/desktop/Midl/represent-as) \] per convertire i dati in un formato compatibile con le versioni precedenti per la rappresentazione in transito.

Se la compatibilità con i fili precedenti non è un problema o se l'handle non viene usato per le chiamate remote e si è certi che le chiamate remote tra i processi 32 e 64 bit non verranno mai eseguite, è possibile ridefinire un argomento come **ULONG64**. Se necessario, è possibile modificare l'applicazione a 32 bit per passare un **valore DWORD** all'utente. In alternativa, è possibile compilare Stub distinti da file IDL distinti per ogni piattaforma usando un **valore DWORD** in windows a 32 bit e un **ULONG64** su Windows a 64 bit.

 

 