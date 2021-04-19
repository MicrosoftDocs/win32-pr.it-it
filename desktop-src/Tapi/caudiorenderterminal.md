---
description: Il terminale CAudioRenderTerminal è derivato da CSingleFilterTerminal e implementa un terminale di rendering audio statico per i dispositivi Wave usando il filtro di origine DirectShow. Per la maggior parte dei MSPs non è necessario eseguire l'override dell'implementazione di questo terminale.
ms.assetid: 58cd0765-9430-4333-ae96-4d8ca73727b5
title: CAudioRenderTerminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9915ef03a210f4ca440cb7a7b66448228b41df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314627"
---
# <a name="caudiorenderterminal"></a><span data-ttu-id="ce999-104">CAudioRenderTerminal</span><span class="sxs-lookup"><span data-stu-id="ce999-104">CAudioRenderTerminal</span></span>

<span data-ttu-id="ce999-105">Il terminale **CAudioRenderTerminal** è derivato da [CSingleFilterTerminal](csinglefilterterminal.md) e implementa un terminale di rendering audio statico per i dispositivi Wave usando il filtro di origine DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ce999-105">The **CAudioRenderTerminal** terminal is derived from [CSingleFilterTerminal](csinglefilterterminal.md) and implements a static audio render terminal for wave devices using the DirectShow waveout filter.</span></span> <span data-ttu-id="ce999-106">Per la maggior parte dei MSPs non è necessario eseguire l'override dell'implementazione di questo terminale.</span><span class="sxs-lookup"><span data-stu-id="ce999-106">Most MSPs will not need to override the implementation of this terminal.</span></span>

<span data-ttu-id="ce999-107">Definito in MSPtrmar. h.</span><span class="sxs-lookup"><span data-stu-id="ce999-107">Defined in MSPtrmar.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce999-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce999-108">Remarks</span></span>

<span data-ttu-id="ce999-109">I metodi [**put \_ Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) e [**get \_ Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) di **CAudioRenderTerminal** non sono implementati e restituiscono e \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="ce999-109">The [**put\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_balance) and [**get\_Balance**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_balance) methods of **CAudioRenderTerminal** are not implemented and will return E\_NOTIMPL.</span></span>

 

 



