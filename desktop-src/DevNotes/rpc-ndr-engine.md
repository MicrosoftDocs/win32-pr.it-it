---
description: Motore di recapito RPC
ms.assetid: FD6365A9-6EC2-407D-B397-09A91BF02379
title: Motore di recapito RPC (note per gli sviluppatori)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c39eeb38d99e01dd8ab5683cf0289b3e7e09d45f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304750"
---
# <a name="rpc-ndr-engine-developer-notes"></a><span data-ttu-id="3fb96-103">Motore di recapito RPC (note per gli sviluppatori)</span><span class="sxs-lookup"><span data-stu-id="3fb96-103">RPC NDR Engine (Developer Notes)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3fb96-104">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="3fb96-104">In this section</span></span>

-   [<span data-ttu-id="3fb96-105">**NdrComplexArrayBufferSize**</span><span class="sxs-lookup"><span data-stu-id="3fb96-105">**NdrComplexArrayBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexarraybuffersize)
-   [<span data-ttu-id="3fb96-106">**NdrComplexArrayMarshall**</span><span class="sxs-lookup"><span data-stu-id="3fb96-106">**NdrComplexArrayMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexarraymarshall)
-   [<span data-ttu-id="3fb96-107">**NdrComplexArrayUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="3fb96-107">**NdrComplexArrayUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexarrayunmarshall)
-   [<span data-ttu-id="3fb96-108">**NdrComplexStructBufferSize**</span><span class="sxs-lookup"><span data-stu-id="3fb96-108">**NdrComplexStructBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexstructbuffersize)
-   [<span data-ttu-id="3fb96-109">**NdrComplexStructMarshall**</span><span class="sxs-lookup"><span data-stu-id="3fb96-109">**NdrComplexStructMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexstructmarshall)
-   [<span data-ttu-id="3fb96-110">**NdrComplexStructUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="3fb96-110">**NdrComplexStructUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrcomplexstructunmarshall)
-   [<span data-ttu-id="3fb96-111">**NdrComformantArrayBufferSize**</span><span class="sxs-lookup"><span data-stu-id="3fb96-111">**NdrComformantArrayBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantarraybuffersize)
-   [<span data-ttu-id="3fb96-112">**NdrComformantArrayMarshall**</span><span class="sxs-lookup"><span data-stu-id="3fb96-112">**NdrComformantArrayMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrconformantarraymarshall)
-   [<span data-ttu-id="3fb96-113">**NdrSimpleStructBufferSize**</span><span class="sxs-lookup"><span data-stu-id="3fb96-113">**NdrSimpleStructBufferSize**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimplestructbuffersize)
-   [<span data-ttu-id="3fb96-114">**NdrSimpleStructMarshall**</span><span class="sxs-lookup"><span data-stu-id="3fb96-114">**NdrSimpleStructMarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimplestructmarshall)
-   [<span data-ttu-id="3fb96-115">**NdrSimpleStructUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="3fb96-115">**NdrSimpleStructUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrsimplestructunmarshall)
-   [<span data-ttu-id="3fb96-116">**NdrUserMarshalUnmarshall**</span><span class="sxs-lookup"><span data-stu-id="3fb96-116">**NdrUserMarshalUnmarshall**</span></span>](/windows/desktop/api/Rpcndr/nf-rpcndr-ndrusermarshalunmarshall)

 

 



