---
title: Evitare di nascondere le informazioni
description: In alcuni casi, i programmi nascondono intenzionalmente o inavvertitamente le informazioni dal motore di marshalling RPC.
ms.assetid: 016b9221-092d-4c25-a396-4f41dcdfb3cf
keywords:
- compatibilità con le versioni precedenti della programmazione Windows a 64 bit
- problemi di compatibilità programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e68ab20ccf267fed187488e4ec2a4d740492338fa1758703827101bd9b98bd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132864"
---
# <a name="avoiding-information-hiding"></a>Evitare di nascondere le informazioni

In alcuni casi, i programmi nascondono intenzionalmente o inavvertitamente le informazioni dal motore di marshalling RPC. Di seguito sono riportati alcuni esempi:

-   Invio di una struttura di dati come blocco di byte non indifferenziato
-   Sfruttare le prestazioni usando un effetto collaterale di un metodo per incanalare dati aggiuntivi in rete
-   Tentativo di eliminare un handle passandolo come **DWORD** o **ULONG**

Queste tecniche introducono quasi sempre problemi di compatibilità anche prima di convertire l'applicazione in un Windows a 64 bit.

Anziché inviare un contesto del server come **DWORD** in una chiamata di procedura remota standard, usare un handle di contesto per fornire un handle opaco a un contesto del server mantenuto per conto di un client. I contesti sono identificati da GUID definiti dal run-time RPC quando un server crea un handle di contesto per un client. Non viene usato alcun puntatore sulla rete e l'operazione è completamente trasparente attraverso i limiti a 32 o 64 bit. Per altre informazioni sull'uso degli handle di contesto, vedere [Handle di contesto.](/windows/desktop/Rpc/context-handles)

Le interfacce DCOM non possono usare handle di contesto perché COM fornisce la propria gestione del contesto. Anziché creare un handle di contesto, è possibile passare un puntatore a interfaccia all'oggetto COM. È quindi possibile chiamare i metodi direttamente tramite il puntatore di interfaccia o posizionare il puntatore all'interno di altre chiamate. Per rilasciare l'oggetto server, il client chiama il metodo **Release** dell'interfaccia tramite il puntatore a interfaccia .

Anche in questo caso, è possibile che non sia possibile modificare la progettazione originale del codice che si sta traslando. Se non è possibile evitare l'invio di un puntatore in transito come **DWORD,** sarà necessario implementare una qualche forma di mapping lato server tra i valori **DWORD** e i puntatori. Un modo per eseguire questa operazione è modificare i puntatori nell'applicazione lato client in tipi di precisione del puntatore, ad esempio **ULONG \_ PTR** o **DWORD \_ PTR.** Usare quindi la chiamata MIDL \[ [**\_ come**](/windows/desktop/Midl/call-as) \] attributo per inserire i puntatori in transito come valori **DWORD.** Il wrapper sul lato client deve passare solo gli argomenti. Il wrapper sul lato server gestisce il mapping tra entrambi i tipi. In modo analogo, è possibile usare l'attributo transmit as o rappresentare come attributo per convertire i dati in un formato compatibile con le versioni precedenti per la rappresentazione \[ [**\_**](/windows/desktop/Midl/transmit-as) \] in \[ [**\_**](/windows/desktop/Midl/represent-as) \] transito.

Se la compatibilità con le versioni precedenti non è un problema o se l'handle non viene usato per le chiamate remote e si è certi che le chiamate remote tra processi a 32 e 64 bit non si verificano mai, è possibile ridefinire un argomento come **ULONG64.** Se necessario, è possibile modificare l'applicazione a 32 bit per passare un **valore DWORD** all'utente. In alternativa, è possibile compilare stub separati da file IDL separati per ogni piattaforma usando **un valore DWORD** in un Windows a 32 bit e **un ULONG64** in un Windows a 64 bit.

 

 