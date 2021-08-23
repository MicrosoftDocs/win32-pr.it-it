---
description: Il multicast IP rientra nella categoria del piano dati non sradicato e del piano di controllo non sradicato.
ms.assetid: 474a1c7f-0ece-4192-a2d9-6e2f3df2ac02
title: IP Multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b80441826f490fedc3dac3dba405ddd0d9f09d57bfd0243a66cae320c76b0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051499"
---
# <a name="ip-multicast"></a>IP Multicast

Il multicast IP rientra nella categoria del piano dati non sradicato e del piano di controllo non sradicato. Tutte le applicazioni svolgono un ruolo foglia. Attualmente, la maggior parte delle implementazioni multicast IP usa un set di opzioni socket proposte da Steve Deering alla Internet Engineering Task Force (IETF). Vengono quindi rese disponibili cinque operazioni:

-   TTL \_ MULTICAST IP: imposta l'intervallo di tempo reale \_ e controlla l'ambito di una sessione multicast.
-   IP \_ MULTICAST \_ IF: determina l'interfaccia da usare per il multicasting.
-   IP \_ ADD \_ MEMBERSHI: aggiunge una sessione multicast specificata.
-   IP \_ DROP \_ MEMBERSHIP: elimina una sessione multicast.
-   IP \_ MULTICAST \_ LOOP: controlla il loopback del traffico multicast.

L'impostazione del time-to-live per un socket IP-multicast viene mappata direttamente all'uso del codice di comando SIO \_ MULTICAST \_ SCOPE per [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl).

Il metodo per determinare l'interfaccia IP da usare per il multicasting è tramite un'opzione socket specifica TCP/IP, come descritto nell'allegato Windows Sockets 2 Protocol-Specific. Le tre operazioni rimanenti sono coperte con la semantica Windows Sockets 2 descritta qui.

L'applicazione aprirebbe socket con flag \_ foglia/d c \_ in [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa). Usa [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) per aggiungersi a un gruppo multicast nell'interfaccia predefinita designata per le operazioni multicast. Se il flag in **WSAJoinLeaf** indica che questo socket è solo un mittente, l'operazione di join è essenzialmente un'operazione no-op e non è necessario inviare messaggi IGMP. In caso contrario, viene inviato un pacchetto IGMP al router per indicare gli interessi nella ricezione dei pacchetti inviati all'indirizzo multicast specificato. Poiché l'applicazione ha creato socket foglia/d C speciali usati solo per l'esecuzione multicast, la funzione \_ \_ [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) standard verrebbe usata per uscire dalla sessione multicast. Il codice di comando SIO \_ MULTIPOINT LOOPBACK per \_ [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) fornisce un meccanismo di controllo generico per determinare se i dati inviati su un socket foglia d in uno schema multipoint non sradicato possono essere ricevuti anche nello \_ stesso socket.

> [!Note]  
> La versione Winsock dell'opzione IP MULTICAST LOOP è semanticamente diversa rispetto alla UNIX dell'opzione \_ \_ IP \_ MULTICAST \_ LOOP:

 

-   In Winsock l'opzione IP \_ MULTICAST \_ LOOP si applica solo al percorso di ricezione.
-   Nella versione UNIX, l'opzione IP \_ MULTICAST \_ LOOP si applica al percorso di invio.

Ad esempio, le applicazioni ON e OFF (che sono più facili da rilevare rispetto a X e Y) si uniscono allo stesso gruppo sulla stessa interfaccia; application ON imposta l'opzione IP \_ MULTICAST \_ LOOP attivata, l'applicazione OFF imposta l'opzione IP \_ MULTICAST \_ LOOP disattivata. Se ON e OFF sono applicazioni Winsock, OFF può essere inviato a ON, ma ON non può essere inviato a OFF. Al contrario, se ON e OFF sono UNIX applicazioni, ON può inviare a OFF, ma OFF non può inviare a ON.

 

 



