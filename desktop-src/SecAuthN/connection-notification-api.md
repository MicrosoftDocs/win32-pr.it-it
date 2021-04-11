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
# <a name="connection-notification-api"></a><span data-ttu-id="59491-104">API di notifica della connessione</span><span class="sxs-lookup"><span data-stu-id="59491-104">Connection Notification API</span></span>

<span data-ttu-id="59491-105">Il [*router multi-provider*](/windows/desktop/SecGloss/m-gly) (MPR) chiama le funzioni di notifica della connessione quando si connette o disconnette una risorsa di rete.</span><span class="sxs-lookup"><span data-stu-id="59491-105">The [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) calls the connection notification functions when it connects or disconnects a network resource.</span></span> <span data-ttu-id="59491-106">Per ricevere notifiche di questo tipo, è possibile implementare queste funzioni in una DLL.</span><span class="sxs-lookup"><span data-stu-id="59491-106">To receive such notifications, you can implement these functions in a DLL.</span></span>

<span data-ttu-id="59491-107">Il MPR chiama la funzione [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) prima e dopo il tentativo di ogni operazione di aggiunta connessione ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a)o [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)).</span><span class="sxs-lookup"><span data-stu-id="59491-107">The MPR calls the [**AddConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-addconnectnotify) function before and after attempting each add-connection operation ([**WNetAddConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnectiona), [**WNetAddConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection2a), or [**WNetAddConnection3**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetaddconnection3a)).</span></span> <span data-ttu-id="59491-108">Questa funzione non viene chiamata quando il MPR ripristina automaticamente le connessioni di rete.</span><span class="sxs-lookup"><span data-stu-id="59491-108">This function is not called when the MPR is automatically restoring network connections.</span></span>

<span data-ttu-id="59491-109">Il MPR chiama la funzione [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) prima e dopo il tentativo di ogni operazione di annullamento della connessione ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) o [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).</span><span class="sxs-lookup"><span data-stu-id="59491-109">The MPR calls the [**CancelConnectNotify**](/windows/desktop/api/Npapi/nf-npapi-cancelconnectnotify) function before and after attempting each cancel-connection operation ([**WNetCancelConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) or [**WNetCancelConnection2**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)).</span></span>

<span data-ttu-id="59491-110">Per ulteriori informazioni sulle funzioni WNet, vedere la pagina relativa alla [rete Windows](/windows/desktop/WNet/windows-networking-wnet-).</span><span class="sxs-lookup"><span data-stu-id="59491-110">For more information about WNet functions, see [Windows Networking](/windows/desktop/WNet/windows-networking-wnet-).</span></span>

<span data-ttu-id="59491-111">Per ulteriori informazioni su come creare e registrare un'applicazione che riceve notifiche di connessione di rete, vedere [ricezione di notifiche di connessione](receiving-connection-notifications.md) e [registrazione per ricevere notifiche di connessione](registering-to-receive-connection-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="59491-111">For more information about how to create and register an application that receives network connection notifications, see [Receiving Connection Notifications](receiving-connection-notifications.md) and [Registering to Receive Connection Notifications](registering-to-receive-connection-notifications.md).</span></span>

 

 
