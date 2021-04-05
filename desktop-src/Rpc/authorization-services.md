---
title: Servizi di autorizzazione
description: Un servizio di autorizzazione è il metodo utilizzato dal provider di servizi condivisi per autorizzare l'accesso a una procedura remota. Gli SSP possono fornire più di un servizio di autorizzazione. Tuttavia, in genere ne selezionano uno come valore predefinito.
ms.assetid: 5ea3cde9-96e9-4208-bb61-d0f98f23b90c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f834c69726425a52a033e0dbb08bf6f1f3a38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045024"
---
# <a name="authorization-services"></a><span data-ttu-id="ebc16-105">Servizi di autorizzazione</span><span class="sxs-lookup"><span data-stu-id="ebc16-105">Authorization Services</span></span>

<span data-ttu-id="ebc16-106">Un servizio di autorizzazione è il metodo utilizzato dal provider di servizi condivisi per autorizzare l'accesso a una procedura remota.</span><span class="sxs-lookup"><span data-stu-id="ebc16-106">An authorization service is the method that the SSP uses to authorize access to a remote procedure.</span></span> <span data-ttu-id="ebc16-107">Gli SSP possono fornire più di un servizio di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="ebc16-107">SSPs can provide more than one authorization service.</span></span> <span data-ttu-id="ebc16-108">Tuttavia, in genere ne selezionano uno come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="ebc16-108">However, they usually select one as a default.</span></span>

<span data-ttu-id="ebc16-109">L'applicazione può usare il metodo di autorizzazione predefinito per il provider di servizi condivisi corrente oppure può specificarne uno.</span><span class="sxs-lookup"><span data-stu-id="ebc16-109">Your application can use the default authorization method for the current SSP, or it can specify one.</span></span> <span data-ttu-id="ebc16-110">Attualmente, Microsoft RPC supporta due metodi di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="ebc16-110">At present, Microsoft RPC supports two methods of authorization.</span></span> <span data-ttu-id="ebc16-111">Uno riguarda il server per fornire l'autorizzazione in base al nome del programma client.</span><span class="sxs-lookup"><span data-stu-id="ebc16-111">One is for the server to provide authorization based on the name of the client program.</span></span> <span data-ttu-id="ebc16-112">L'altro è che il server confronti le credenziali di autenticazione del client con l'elenco di controllo di accesso (ACL) del server.</span><span class="sxs-lookup"><span data-stu-id="ebc16-112">The other is for the server to compare the client's authentication credentials against the server's access control list (ACL).</span></span>

<span data-ttu-id="ebc16-113">Per un elenco di servizi di autorizzazione, vedere [costanti del servizio di autorizzazione](authorization-service-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ebc16-113">For a list of authorization services, see [Authorization-Service Constants](authorization-service-constants.md).</span></span>

> [!Note]  
> <span data-ttu-id="ebc16-114">Si consiglia agli sviluppatori di usare RPC \_ C \_ AUTHZ \_ None.</span><span class="sxs-lookup"><span data-stu-id="ebc16-114">It is recommended that developers use RPC\_C\_AUTHZ\_NONE.</span></span>

 

 

 




