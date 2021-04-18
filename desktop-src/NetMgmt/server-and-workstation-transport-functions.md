---
title: Funzioni di trasporto per server e workstation
description: Il server di gestione di rete e le funzioni di trasporto workstation gestiscono l'associazione e l'annullamento dell'associazione dei protocolli di trasporto da e verso il server e il redirector.
ms.assetid: 64342e21-98f1-42d3-b541-46b826391fad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1ab4a4ce5dcc3b887eb9eb9d5759db89dfed55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298163"
---
# <a name="server-and-workstation-transport-functions"></a>Funzioni di trasporto per server e workstation

Il server di gestione di rete e le funzioni di trasporto workstation gestiscono l'associazione e l'annullamento dell'associazione dei protocolli di trasporto da e verso il server e il redirector. Le funzioni di trasporto server gestiscono i protocolli di trasporto gestiti dal server. le funzioni di trasporto workstation gestiscono i protocolli di trasporto gestiti dal redirector.

La condivisione di file tra un dispositivo di trasporto e un server dispone di due componenti:

-   Il computer server in cui risiedono i file
-   Un client SMB (Server Message Block) che accede ai file

Il computer client comunica con il computer server tramite una rete locale utilizzando un protocollo di trasporto; ad esempio TCP o XNS. Il client invia richieste al server per recuperare i dati. Il software nel computer client che genera le richieste di file è denominato *redirector* perché reindirizza le richieste di file locali al computer server. Il software nel computer che riceve e agisce sulle richieste di file viene chiamato *Server* perché serve ai client. Il formato specifico per queste richieste è denominato protocollo SMB.

Le funzioni di trasporto del server sono elencate di seguito.



| Funzione                                                     | Descrizione                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetServerComputerNameAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernameadd) | Associa un nome di server emulato a ogni protocollo di trasporto su cui è attivo un server. (Combina le funzionalità della funzione [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum) e della funzione [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex) ).                                            |
| [**NetServerComputerNameDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernamedel) | Disconnette ogni protocollo di trasporto di rete da un nome di server emulato impostato da una chiamata precedente alla funzione **NetServerComputerNameAdd** .                                                                                                                                                                               |
| [**NetServerTransportAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportadd)       | Associa il server specificato al protocollo di trasporto. Questa funzione supporta solo il livello [**informazioni \_ \_ \_ 0 del trasporto server**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0) .                                                                                                                                                |
| [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)   | Associa il server specificato al protocollo di trasporto. Questa funzione estesa supporta le informazioni sul trasporto server [**\_ \_ \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1), [**server \_ Transport \_ info \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)e [**server \_ Transport info \_ \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3) Information levels. |
| [**NetServerTransportDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportdel)       | Disconnette il protocollo di trasporto dal server.                                                                                                                                                                                                                                                                         |
| [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum)     | Enumera i protocolli di trasporto gestiti dal server.                                                                                                                                                                                                                                                                   |



 

Le funzioni di trasporto del server sono disponibili ai livelli di informazioni seguenti:

-   [**\_Informazioni sul trasporto server \_ \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0)
-   [**\_Informazioni trasporto \_ server \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1)
-   [**\_Informazioni sul trasporto server \_ \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)
-   [**Informazioni sul trasporto del SERVER \_ \_ \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3)

Le funzioni di trasporto workstation eseguono operazioni equivalenti per la workstation.

**Windows Server 2003 e Windows XP/2000:** Il redirector non supporta la funzione [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd) o [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel) . È possibile modificare manualmente le impostazioni predefinite per i protocolli di trasporto tramite la finestra di dialogo **Proprietà connessione area locale** della cartella **rete e connessioni remote** .

Le funzioni di trasporto workstation sono elencate di seguito.



| Funzione                                               | Descrizione                                                       |
|--------------------------------------------------------|-------------------------------------------------------------------|
| [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd)   | Connette il redirector al protocollo di trasporto.                |
| [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel)   | Disconnette il protocollo di trasporto dal redirector.           |
| [**NetWkstaTransportEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstatransportenum) | Elenca i protocolli di trasporto gestiti dal redirector. |



 

Le funzioni di trasporto workstation sono disponibili a un livello di informazioni:

-   [**\_Informazioni sul trasporto WKSTA \_ \_ 0**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_transport_info_0)

 

 




