---
title: API Servizi Desktop remoto
description: L'API Servizi Desktop remoto è particolarmente utile per le applicazioni client/server e le applicazioni per Servizi Desktop remoto l'amministrazione.
ms.assetid: 4bd10a15-78d6-4754-9e17-f2576ee8b9d0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5aa187378625242463ea91151a6961b08d2a77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855901"
---
# <a name="remote-desktop-services-api"></a><span data-ttu-id="49a06-103">API Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="49a06-103">Remote Desktop Services API</span></span>

<span data-ttu-id="49a06-104">La maggior parte delle applicazioni viene eseguita senza modifiche in un ambiente di Servizi Desktop remoto (noto in precedenza come servizi Terminal) e non è necessario usare l'API Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="49a06-104">Most applications run without modification in a Remote Desktop Services (formerly known as Terminal Services) environment and do not need to use the Remote Desktop Services API.</span></span> <span data-ttu-id="49a06-105">L'API Servizi Desktop remoto è particolarmente utile per le applicazioni client/server e le applicazioni per Servizi Desktop remoto l'amministrazione.</span><span class="sxs-lookup"><span data-stu-id="49a06-105">The Remote Desktop Services API is primarily useful to client/server applications and applications for Remote Desktop Services administration.</span></span>

<span data-ttu-id="49a06-106">L'API Servizi Desktop remoto è un set di chiamate di funzione in Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="49a06-106">The Remote Desktop Services API is a set of function calls into Wtsapi32.dll.</span></span> <span data-ttu-id="49a06-107">Per progettare l'applicazione per l'esecuzione in ambienti Servizi Desktop remoto e non Servizi Desktop remoto, utilizzare il collegamento dinamico in fase di esecuzione per verificare la presenza di Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="49a06-107">To design your application to run in both Remote Desktop Services and non-Remote Desktop Services environments, use run-time dynamic linking to check for the presence of Wtsapi32.dll.</span></span> <span data-ttu-id="49a06-108">Per ulteriori informazioni, vedere il [collegamento di run-time a Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span><span class="sxs-lookup"><span data-stu-id="49a06-108">For more information, see [Run-Time Linking to Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).</span></span>

<span data-ttu-id="49a06-109">L'API Servizi Desktop remoto consente alle applicazioni di eseguire le attività seguenti in un ambiente Servizi Desktop remoto:</span><span class="sxs-lookup"><span data-stu-id="49a06-109">The Remote Desktop Services API enables applications to perform the following tasks in a Remote Desktop Services environment:</span></span>

-   <span data-ttu-id="49a06-110">[Servizi Desktop remoto amministrazione](terminal-services-administration.md), ad esempio l'enumerazione e la gestione di server di host sessione Desktop remoto (host sessione Desktop remoto) (noti in precedenza come Terminal Server) in un dominio o l'enumerazione e la gestione di sessioni e processi in un server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="49a06-110">[Remote Desktop Services Administration](terminal-services-administration.md), such as enumerating and managing Remote Desktop Session Host (RD Session Host) servers (formerly known as terminal servers) in a domain or enumerating and managing sessions and processes on an RD Session Host server.</span></span>
-   <span data-ttu-id="49a06-111">Miglioramento delle applicazioni client/server in un ambiente Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="49a06-111">Enhancing client/server applications in a Remote Desktop Services environment.</span></span>
-   <span data-ttu-id="49a06-112">Uso di [Servizi Desktop remoto canali virtuali](terminal-services-virtual-channels.md) per la comunicazione tra i moduli client e server di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="49a06-112">Using [Remote Desktop Services Virtual Channels](terminal-services-virtual-channels.md) to communicate between client and server modules of an application.</span></span>
-   <span data-ttu-id="49a06-113">[Impostazione e recupero di Servizi Desktop remoto informazioni di configurazione utente specifiche](terminal-services-user-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="49a06-113">[Setting and retrieving Remote Desktop Services specific user configuration information](terminal-services-user-configuration.md).</span></span>

 

 




