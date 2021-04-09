---
description: "L'API Graphing usa i callback seguenti:"
ms.assetid: a8e083ab-b5e3-4186-99fb-cbb536e9d529
title: Callback dell'API Graphing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11f4f559307e457822cd0e7ce18ef4b44119697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050022"
---
# <a name="graphing-api-callbacks"></a><span data-ttu-id="afb37-103">Callback dell'API Graphing</span><span class="sxs-lookup"><span data-stu-id="afb37-103">Graphing API Callbacks</span></span>

<span data-ttu-id="afb37-104">L'API Graphing usa i callback seguenti:</span><span class="sxs-lookup"><span data-stu-id="afb37-104">The Graphing API uses the following callbacks:</span></span>



| <span data-ttu-id="afb37-105">Callback</span><span class="sxs-lookup"><span data-stu-id="afb37-105">Callback</span></span>                                                          | <span data-ttu-id="afb37-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afb37-106">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="afb37-107">*PFNPEER \_ \_ i dati di sicurezza gratuiti \_*</span><span class="sxs-lookup"><span data-stu-id="afb37-107">*PFNPEER\_FREE\_SECURITY\_DATA*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_free_security_data) | <span data-ttu-id="afb37-108">Specifica la funzione chiamata dall'infrastruttura peer Graphing per liberare i dati restituiti da [*PFNPEER \_ Secure \_ record*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) e [*PFNPEER \_ Validate \_ record*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) Callbacks.</span><span class="sxs-lookup"><span data-stu-id="afb37-108">Specifies the function that the Peer Graphing Infrastructure calls to free data returned by [*PFNPEER\_SECURE\_RECORD*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record) and [*PFNPEER\_VALIDATE\_RECORD*](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record) callbacks.</span></span> |
| [<span data-ttu-id="afb37-109">*\_record sicuro \_ PFNPEER*</span><span class="sxs-lookup"><span data-stu-id="afb37-109">*PFNPEER\_SECURE\_RECORD*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_secure_record)            | <span data-ttu-id="afb37-110">Specifica la funzione chiamata dall'infrastruttura del Peer Graphing per proteggere i record.</span><span class="sxs-lookup"><span data-stu-id="afb37-110">Specifies the function that the Peer Graphing Infrastructure calls to secure records.</span></span>                                                                                                                                        |
| [<span data-ttu-id="afb37-111">*\_record di convalida PFNPEER \_*</span><span class="sxs-lookup"><span data-stu-id="afb37-111">*PFNPEER\_VALIDATE\_RECORD*</span></span>](/windows/desktop/api/P2P/nc-p2p-pfnpeer_validate_record)        | <span data-ttu-id="afb37-112">Specifica la funzione chiamata dall'infrastruttura del Peer Graphing per convalidare i record.</span><span class="sxs-lookup"><span data-stu-id="afb37-112">Specifies the function that the Peer Graphing Infrastructure calls to validate records.</span></span>                                                                                                                                      |



 

 

 



