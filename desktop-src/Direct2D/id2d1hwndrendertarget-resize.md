---
title: Metodi di ridimensionamento ID2D1HwndRenderTarget (D2d1. h)
description: Consente di modificare le dimensioni della destinazione di rendering nella dimensione in pixel specificata.
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
keywords:
- Ridimensiona metodi Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3f15af87c59c943bd7d5dc8ece708d3603bddce6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330071"
---
# <a name="id2d1hwndrendertargetresize-methods"></a><span data-ttu-id="59e2b-104">Metodi ID2D1HwndRenderTarget:: Resize</span><span class="sxs-lookup"><span data-stu-id="59e2b-104">ID2D1HwndRenderTarget::Resize methods</span></span>

<span data-ttu-id="59e2b-105">Consente di modificare le dimensioni della destinazione di rendering nella dimensione in pixel specificata.</span><span class="sxs-lookup"><span data-stu-id="59e2b-105">Changes the size of the render target to the specified pixel size.</span></span>

### <a name="overload-list"></a><span data-ttu-id="59e2b-106">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="59e2b-106">Overload list</span></span>



| <span data-ttu-id="59e2b-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="59e2b-107">Method</span></span>                                                                         | <span data-ttu-id="59e2b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59e2b-108">Description</span></span>                                                                    |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="59e2b-109">[**Ridimensiona (D2D1 \_ dimensioni \_ U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))</span><span class="sxs-lookup"><span data-stu-id="59e2b-109">[**Resize(D2D1\_SIZE\_U&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u_))</span></span>  | <span data-ttu-id="59e2b-110">Consente di modificare le dimensioni della destinazione di rendering nella dimensione in pixel specificata.</span><span class="sxs-lookup"><span data-stu-id="59e2b-110">Changes the size of the render target to the specified pixel size.</span></span> <br/> |
| <span data-ttu-id="59e2b-111">[**Ridimensiona (D2D1 \_ dimensioni \_ U \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u))</span><span class="sxs-lookup"><span data-stu-id="59e2b-111">[**Resize(D2D1\_SIZE\_U\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u))</span></span> | <span data-ttu-id="59e2b-112">Consente di modificare le dimensioni della destinazione di rendering nella dimensione in pixel specificata.</span><span class="sxs-lookup"><span data-stu-id="59e2b-112">Changes the size of the render target to the specified pixel size.</span></span><br/>  |



## <a name="remarks"></a><span data-ttu-id="59e2b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="59e2b-113">Remarks</span></span>

<span data-ttu-id="59e2b-114">Dopo la chiamata a questo metodo, il contenuto del back-buffer della destinazione di rendering non è definito, anche se è stata specificata l'opzione [**\_ \_ \_ Mantieni \_ contenuto d2d1 opzioni presenti**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) durante la creazione della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="59e2b-114">After this method is called, the contents of the render target's back-buffer are not defined, even if the [**D2D1\_PRESENT\_OPTIONS\_RETAIN\_CONTENTS**](/windows/win32/api/d2d1/ne-d2d1-d2d1_present_options) option was specified when the render target was created.</span></span>

## <a name="requirements"></a><span data-ttu-id="59e2b-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59e2b-115">Requirements</span></span>



| <span data-ttu-id="59e2b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="59e2b-116">Requirement</span></span> | <span data-ttu-id="59e2b-117">Valore</span><span class="sxs-lookup"><span data-stu-id="59e2b-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="59e2b-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59e2b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="59e2b-119"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="59e2b-119"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="59e2b-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="59e2b-120">Library</span></span><br/> | <dl> <span data-ttu-id="59e2b-121"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59e2b-121"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="59e2b-122">DLL</span><span class="sxs-lookup"><span data-stu-id="59e2b-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="59e2b-123"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59e2b-123"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59e2b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59e2b-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="59e2b-125">[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="59e2b-125">[**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span></span>
</dt> </dl>

<span data-ttu-id="59e2b-126">�</span><span class="sxs-lookup"><span data-stu-id="59e2b-126">�</span></span>

<span data-ttu-id="59e2b-127">�</span><span class="sxs-lookup"><span data-stu-id="59e2b-127">�</span></span>
