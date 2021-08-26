---
description: Il router a più provider (MPR) chiama le funzioni di notifica della connessione quando si connette o disconnette una risorsa di rete. Per ricevere tali notifiche, è possibile implementare queste funzioni in una DLL.
ms.assetid: 62559eab-dd2f-43fa-9b09-5e4d82efc879
title: Connessione Notification API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0afaa2e08e6a88f101e8914d9d98a40d6024bdf942ed4bcb0fd1924bc5800213
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883311"
---
# <a name="connection-notification-api"></a>Connessione Notification API

Il [*router a più provider*](/windows/desktop/SecGloss/m-gly) (MPR) chiama le funzioni di notifica della connessione quando si connette o disconnette una risorsa di rete. Per ricevere tali notifiche, è possibile implementare queste funzioni in una DLL.

La funzione MPR chiama la [**funzione AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) prima e dopo il tentativo di ogni operazione di aggiunta connessione ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)o [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)). Questa funzione non viene chiamata quando la reimpostazione della regola MPR ripristina automaticamente le connessioni di rete.

La funzione MPR chiama la [**funzione CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) prima e dopo il tentativo di ogni operazione di annullamento della connessione ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) o [**WNetCancelConnection2).**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)

Per altre informazioni sulle funzioni WNet, vedere Windows [Networking](/windows/desktop/WNet/windows-networking-wnet-).

Per altre informazioni su come creare e registrare un'applicazione che riceve notifiche di connessione di rete, vedere [Ricezione](receiving-connection-notifications.md) di notifiche di connessione e Registrazione per la ricezione di notifiche [di connessione.](registering-to-receive-connection-notifications.md)

 

 
