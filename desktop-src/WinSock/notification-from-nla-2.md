---
description: NLA è in grado di fornire ai propri client la notifica delle modifiche del percorso di rete. Il meccanismo usato per richiedere la notifica degli eventi di modifica è una combinazione delle funzioni WSALookupServiceBegin, WSANSPIoctl e WSALookupServiceNext.
ms.assetid: fed5a90d-0bc5-46e7-b3d3-edc4b303d305
title: Notifica da NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ee0ad0530725db27c8f5df39b6fc573f7e97c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526125"
---
# <a name="notification-from-nla"></a>Notifica da NLA

NLA è in grado di fornire ai propri client la notifica delle modifiche del percorso di rete. Il meccanismo usato per richiedere la notifica degli eventi di modifica è una combinazione delle funzioni [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl)e [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) .

Per ricevere una notifica di modifica da NLA, un client deve prima chiamare il [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) per ottenere un handle di ricerca NLA SP valido. Il client può quindi chiamare [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) o [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) in qualsiasi ordine. per eseguire la registrazione per la notifica, chiamare la funzione **WSANSPIoctl** con il \_ codice di controllo delle modifiche di NSP \_ Notify di sio \_ impostato nel parametro *dwControlCode* .

La funzione [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) restituisce WSA \_ E \_ non \_ più come delimitatore di set. Quando un client si è registrato per la notifica tramite la funzione [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) e **WSALookupServiceNext** restituisce WSA \_ e \_ non \_ più, la chiamata di **WSALookupServiceNext** indica di nuovo se si è verificata una modifica:

-   Se non sono state apportate modifiche rispetto alla precedente WSA \_ e \_ , non viene più \_ \_ restituito WSA e \_ \_ .
-   Se si è verificata una modifica o se si è verificata una modifica e viene effettuata una chiamata di polling, la chiamata della funzione [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) restituisce le reti come strutture [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , con uno dei flag seguenti impostati nel membro **dwOutputFlags** :

    <dl> RISULTATO \_ \_ aggiunto  
    RISULTATO \_ \_ modificato  
    RISULTATO \_ \_ eliminato  
    </dl>

Viene fornita una notifica di modifica per tutti i campi modificati dall'handle di ricerca NLA ottenuti con la chiamata di funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) o dall'ultima enumerazione che ha generato l' \_ errore WSA \_ \_ . Quando vengono specificate tutte le informazioni sul percorso di rete modificate, WSA \_ E \_ non \_ viene più restituito. I client possono riemettere una chiamata di funzione [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) sullo stesso handle di query in qualsiasi momento, uno alla volta, con il \_ flag sio NSP \_ Notify \_ Change set. Questa funzionalità consente a un client di riciclare l'handle di query su base continuativa, evitando in tal modo al client di dover mantenere le informazioni sullo stato di modifica autonomamente. Quando un client non necessita più delle notifiche di modifica, deve chiudere l'handle di query usando la funzione [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) .

 

 



