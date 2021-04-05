---
title: Gestione connessione
description: I clienti che intendono sviluppare dialer personalizzati mediante l'API del servizio di accesso remoto potrebbero voler analizzare gestione connessione Microsoft e Connection Manager Administration Kit.
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7959482542630b6dc90149971df08f7944f83fc
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104046372"
---
# <a name="connection-manager"></a><span data-ttu-id="95d0a-103">Gestione connessione</span><span class="sxs-lookup"><span data-stu-id="95d0a-103">Connection Manager</span></span>

<span data-ttu-id="95d0a-104">I clienti che intendono sviluppare dialer personalizzati mediante l'API del servizio di accesso remoto potrebbero voler analizzare gestione connessione Microsoft e Connection Manager Administration Kit.</span><span class="sxs-lookup"><span data-stu-id="95d0a-104">Customers who intend to develop custom dialers using the Remote Access Service API may want to investigate Microsoft Connection Manager and the Connection Manager Administration Kit.</span></span> <span data-ttu-id="95d0a-105">Gestione connessione è il client di accesso remoto gestito da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="95d0a-105">Connection Manager is Microsoft's managed remote access client.</span></span> <span data-ttu-id="95d0a-106">Consente a un amministratore di creare un pacchetto di configurazione di accesso remoto da distribuire agli utenti remoti dell'amministratore.</span><span class="sxs-lookup"><span data-stu-id="95d0a-106">It allows an administrator to build a remote access configuration package to be distributed to the administrator's remote users.</span></span> <span data-ttu-id="95d0a-107">Per ulteriori informazioni su gestione connessione e Connection Manager Administration Kit, vedere la Guida in linea per Microsoft Windows Server 2000 e sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="95d0a-107">For more information on Connection Manager and the Connection Manager Administration Kit, see the online help for Microsoft Windows 2000 Server and later operating systems.</span></span>

<span data-ttu-id="95d0a-108">È possibile trovare il codice sorgente per un'azione personalizzata di gestione connessione di esempio nel Software Development Kit (SDK) completo della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="95d0a-108">You can find the source code for a sample Connection Manager custom action in the complete Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="95d0a-109">Platform SDK può essere scaricato dal [sito Web Microsoft](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="95d0a-109">The Platform SDK can be downloaded at the [Microsoft Web site](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span></span> <span data-ttu-id="95d0a-110">Al termine dell'installazione, il percorso del codice di esempio è% install path% \\ Microsoft SDK \\ Samples \\ netds \\ RAS \\ ConnectionManager, dove% install path% designa la directory di installazione di base di Platform SDK, ad esempio C: \\ Program Files.</span><span class="sxs-lookup"><span data-stu-id="95d0a-110">After installation, the path to the sample code is %Install Path%\\Microsoft SDK\\Samples\\netds\\Ras\\ConnectionManager, where %Install Path% designates the base installation directory of the Platform SDK (for example, C:\\Program Files).</span></span>

<span data-ttu-id="95d0a-111">Le azioni personalizzate consentono al client di accesso remoto di eseguire azioni specifiche in diversi punti del processo di connessione.</span><span class="sxs-lookup"><span data-stu-id="95d0a-111">Custom actions make it possible for the remote access client to take specific actions at various points in the connection process.</span></span> <span data-ttu-id="95d0a-112">L'azione personalizzata illustrata nell'esempio regola automaticamente la configurazione del server proxy per una connessione in base all'indirizzo del server della connessione.</span><span class="sxs-lookup"><span data-stu-id="95d0a-112">The custom action demonstrated in the sample automatically adjusts the proxy server configuration for a connection based on the connection's server address.</span></span> <span data-ttu-id="95d0a-113">I clienti possono usare questo esempio come punto di partenza per la creazione di azioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="95d0a-113">Customers can use this sample as a starting point for creating their own custom actions.</span></span>

 

 




