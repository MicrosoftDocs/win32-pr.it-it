---
description: Il router multi-provider (MPR) chiama le funzioni di notifica della connessione quando si connette o disconnette una risorsa di rete. Per ricevere notifiche di questo tipo, è possibile implementare queste funzioni in una DLL.
ms.assetid: 62559eab-dd2f-43fa-9b09-5e4d82efc879
title: API di notifica della connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 352d5cb09923a666e3fe1474e9fd2ebe033f05be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131058"
---
# <a name="connection-notification-api"></a>API di notifica della connessione

Il [*router multi-provider*](/windows/desktop/SecGloss/m-gly) (MPR) chiama le funzioni di notifica della connessione quando si connette o disconnette una risorsa di rete. Per ricevere notifiche di questo tipo, è possibile implementare queste funzioni in una DLL.

Il MPR chiama la funzione [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) prima e dopo il tentativo di ogni operazione di aggiunta connessione ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)o [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)). Questa funzione non viene chiamata quando il MPR ripristina automaticamente le connessioni di rete.

Il MPR chiama la funzione [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) prima e dopo il tentativo di ogni operazione di annullamento della connessione ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) o [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).

Per ulteriori informazioni sulle funzioni WNet, vedere la pagina relativa alla [rete Windows](/windows/desktop/WNet/windows-networking-wnet-).

Per ulteriori informazioni su come creare e registrare un'applicazione che riceve notifiche di connessione di rete, vedere [ricezione di notifiche di connessione](receiving-connection-notifications.md) e [registrazione per ricevere notifiche di connessione](registering-to-receive-connection-notifications.md).

 

 
