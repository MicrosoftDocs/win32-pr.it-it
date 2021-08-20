---
description: NLA è in grado di fornire ai client la notifica delle modifiche del percorso di rete. Il meccanismo usato per richiedere la notifica degli eventi di modifica è una combinazione delle funzioni WSALookupServiceBegin, WSANSPIoctl e WSALookupServiceNext.
ms.assetid: fed5a90d-0bc5-46e7-b3d3-edc4b303d305
title: Notifica da NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8e7309fe6845d822702ffd81448999e2472ebdd37a6949812f622110ee9d42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822666"
---
# <a name="notification-from-nla"></a>Notifica da NLA

NLA è in grado di fornire ai client la notifica delle modifiche del percorso di rete. Il meccanismo usato per richiedere la notifica degli eventi di modifica è una combinazione delle funzioni [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl)e [**WSALookupServiceNext.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)

Per ricevere la notifica delle modifiche da NLA, un client deve prima chiamare [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) per ottenere un handle di ricerca sp NLA valido. Successivamente, il client può chiamare [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) o [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) in qualsiasi ordine; per eseguire la registrazione per la notifica, chiamare la funzione **WSANSPIoctl** con il codice di controllo \_ SIO NSP \_ NOTIFY CHANGE impostato nel parametro \_ *dwControlCode.*

La [**funzione WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) restituisce WSA \_ E NO MORE come \_ \_ delimitatore di set. Quando un client si è registrato per la notifica usando la funzione [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) e **WSALookupServiceNext restituisce WSA** E NO MORE, la chiamata di \_ \_ \_ **WSALookupServiceNext** rivela di nuovo se si è verificata una modifica:

-   Se non sono state apportate modifiche rispetto al precedente WSA \_ E \_ NO \_ MORE, viene restituito WSA \_ E NO \_ \_ MORE.
-   Se si è verificata una modifica o se è stata apportata una modifica ed è stata effettuata una chiamata di polling, la chiamata alla funzione [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) restituisce le reti come strutture [**WSAQUERYSET,**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) con uno dei flag seguenti impostati nel relativo membro **dwOutputFlags:**

    <dl> RISULTATO \_ \_ AGGIUNTO  
    IL \_ RISULTATO È STATO \_ MODIFICATO  
    IL \_ RISULTATO VIENE \_ ELIMINATO  
    </dl>

La notifica delle modifiche viene fornita per tutti i campi modificati dopo che l'handle di ricerca NLA è stato ottenuto con la chiamata di funzione [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) o dall'ultima enumerazione che ha generato l'errore WSA \_ E NO \_ \_ MORE. Quando vengono fornite tutte le informazioni sul percorso di rete modificate, viene restituito WSA \_ E \_ NO \_ MORE. I client possono eseguire nuovamente una chiamata di funzione [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) sullo stesso handle di query in qualsiasi momento, uno alla volta, con il flag SIO \_ NSP \_ NOTIFY CHANGE \_ impostato. Questa funzionalità consente a un client di riciclare continuamente l'handle di query, evitando in tal modo al client di dover gestire le informazioni sullo stato di modifica in modo permanente. Quando un client non necessita più di notifiche di modifica, deve chiudere l'handle di query usando la [**funzione WSALookupServiceEnd.**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

 

 



