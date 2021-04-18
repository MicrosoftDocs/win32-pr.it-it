---
description: Il multicast IP rientra nella categoria del piano dati non radice e del piano di controllo non radice.
ms.assetid: 474a1c7f-0ece-4192-a2d9-6e2f3df2ac02
title: Multicast IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf9469822ae974b7c616b7904f9dc7120682acb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306948"
---
# <a name="ip-multicast"></a>Multicast IP

Il multicast IP rientra nella categoria del piano dati non radice e del piano di controllo non radice. Tutte le applicazioni rivestono un ruolo foglia. Attualmente, la maggior parte delle implementazioni multicast IP usa un set di opzioni socket proposto da Steve Deering per Internet Engineering Task Force (IETF). Vengono rese disponibili cinque operazioni:

-   \_TTL multicast IP \_ : imposta la durata (TTL), controlla l'ambito di una sessione multicast.
-   \_Multicast IP \_ if: determina l'interfaccia da usare per il multicast.
-   IP \_ Add \_ MEMBERSHI-partecipa a una sessione multicast specificata.
-   \_ \_ Appartenenza al rilascio IP: Elimina una sessione multicast.
-   \_Loop multicast IP \_ : controlla il loopback del traffico multicast.

Per impostare la durata (TTL) per un socket multicast IP, è possibile eseguire il mapping diretto all'uso del \_ \_ codice del comando per l'ambito multicast Sio per [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl).

Il metodo per determinare l'interfaccia IP da utilizzare per il multicast avviene tramite un'opzione socket specifica TCP/IP, come descritto nell'allegato Windows Sockets 2 Protocol-Specific. Le restanti tre operazioni sono analizzate correttamente con la semantica di Windows Sockets 2 descritta qui.

L'applicazione aprirà i socket con i \_ flag foglia foglia/d c \_ in [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa). USA [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) per aggiungersi a un gruppo multicast sull'interfaccia predefinita designata per le operazioni multicast. Se il flag in **WSAJoinLeaf** indica che questo socket è solo un mittente, l'operazione di join è essenzialmente un no-op e non è necessario inviare messaggi IGMP. In caso contrario, viene inviato un pacchetto IGMP al router per indicare gli interessi nella ricezione dei pacchetti inviati all'indirizzo multicast specificato. Poiché l'applicazione ha creato i \_ socket foglia foglia/d speciali \_ utilizzati solo per l'esecuzione del multicast, la funzione [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) standard verrebbe utilizzata per l'eliminazione della sessione multicast. Il \_ \_ codice di comando di loopback multipoint Sio per [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) fornisce un meccanismo di controllo generico per determinare se i dati inviati in un \_ socket foglia d in uno schema MultiPoint non radice possono essere ricevuti anche sullo stesso socket.

> [!Note]  
> La versione Winsock dell' \_ \_ opzione ciclo multicast IP è semanticamente diversa dalla versione UNIX dell' \_ \_ opzione ciclo IP multicast:

 

-   In Winsock l' \_ \_ opzione ciclo IP multicast si applica solo al percorso di ricezione.
-   Nella versione UNIX, l' \_ \_ opzione ciclo multicast IP si applica al percorso di trasmissione.

Ad esempio, le applicazioni ATTIVAte e disattivate (che risultano più facili da rilevare rispetto a X e Y) si uniscono allo stesso gruppo nella stessa interfaccia; applicazione su Imposta l' \_ opzione del ciclo IP multicast \_ in, l'applicazione off imposta l' \_ opzione del ciclo multicast IP su \_ disattivato. Se ON e OFF sono applicazioni Winsock, OFF può inviare a ON, ma ON non può essere inviato a OFF. Al contrario, se ON e OFF sono applicazioni UNIX, ON può inviare a OFF, ma OFF non può inviare a ON.

 

 



