---
title: Amministrazione del server RAS
description: Windows NT Server 4,0 fornisce un set di funzioni per l'amministrazione delle autorizzazioni e delle porte utente nei server RAS Windows NT/Windows 2000.
ms.assetid: 0b517c4d-dcae-477b-b274-c3773bd172ef
keywords:
- Amministrazione del server, RAS
- Amministrazione, server RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e096610e1cfe986c504a017f4d2b0d1033a6e6d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221880"
---
# <a name="ras-server-administration"></a><span data-ttu-id="3336e-105">Amministrazione del server RAS</span><span class="sxs-lookup"><span data-stu-id="3336e-105">RAS Server Administration</span></span>

<span data-ttu-id="3336e-106">Windows NT Server 4,0 fornisce un set di funzioni per l'amministrazione delle autorizzazioni e delle porte utente nei server RAS Windows NT/Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3336e-106">Windows NT Server 4.0 provides a set of functions for administering user permissions and ports on Windows NT/Windows 2000 RAS servers.</span></span> <span data-ttu-id="3336e-107">Windows 95 non supporta queste funzioni.</span><span class="sxs-lookup"><span data-stu-id="3336e-107">Windows 95 does not support these functions.</span></span> <span data-ttu-id="3336e-108">Utilizzando queste funzioni, è possibile sviluppare un'applicazione di amministrazione del server RAS per eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="3336e-108">Using these functions, you can develop a RAS server administration application to perform the following tasks:</span></span>

-   <span data-ttu-id="3336e-109">Enumerare gli utenti che dispongono di un set specificato di autorizzazioni RAS</span><span class="sxs-lookup"><span data-stu-id="3336e-109">Enumerate those users who have a specified set of RAS permissions</span></span>
-   <span data-ttu-id="3336e-110">Assegnare o revocare le autorizzazioni RAS per un utente specificato</span><span class="sxs-lookup"><span data-stu-id="3336e-110">Assign or revoke RAS permissions for a specified user</span></span>
-   <span data-ttu-id="3336e-111">Enumerare le porte configurate in un server RAS</span><span class="sxs-lookup"><span data-stu-id="3336e-111">Enumerate the configured ports on a RAS server</span></span>
-   <span data-ttu-id="3336e-112">Ottenere informazioni e statistiche su una porta specificata in un server RAS</span><span class="sxs-lookup"><span data-stu-id="3336e-112">Get information and statistics about a specified port on a RAS server</span></span>
-   <span data-ttu-id="3336e-113">Reimposta i contatori delle statistiche per una porta specificata</span><span class="sxs-lookup"><span data-stu-id="3336e-113">Reset the statistics counters for a specified port</span></span>
-   <span data-ttu-id="3336e-114">Disconnettere una porta specificata</span><span class="sxs-lookup"><span data-stu-id="3336e-114">Disconnect a specified port</span></span>

<span data-ttu-id="3336e-115">È inoltre possibile installare una DLL di amministrazione del server RAS per il controllo delle connessioni utente e l'assegnazione di indirizzi IP agli utenti con connessione remota.</span><span class="sxs-lookup"><span data-stu-id="3336e-115">You can also install a RAS server administration DLL for auditing user connections and assigning IP addresses to dial-in users.</span></span> <span data-ttu-id="3336e-116">La DLL esporta un set di funzioni che il server RAS chiama ogni volta che un utente tenta di connettersi o disconnettersi.</span><span class="sxs-lookup"><span data-stu-id="3336e-116">The DLL exports a set of functions that the RAS server calls whenever a user tries to connect or disconnect.</span></span>

 

 




