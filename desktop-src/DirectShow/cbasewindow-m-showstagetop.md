---
description: Messaggio privato che imposta lo stile della finestra su WS ex in primo piano \_ \_ .
ms.assetid: 4934400e-4ca5-4ace-b9b9-3889f4cf610e
title: 'Membro CBaseWindow:: m_ShowStageTop (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ShowStageTop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8ed0069c5c65f2bb1a113c899e2d90de0cabcd10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325776"
---
# <a name="cbasewindowm_showstagetop-member"></a><span data-ttu-id="99558-103">Membro ShowStageTop di CBaseWindow:: m \_</span><span class="sxs-lookup"><span data-stu-id="99558-103">CBaseWindow::m\_ShowStageTop member</span></span>

<span data-ttu-id="99558-104">Messaggio privato che imposta lo stile della finestra su WS ex in primo piano \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="99558-104">Private message that sets the window style to WS\_EX\_TOPMOST.</span></span>

## <a name="syntax"></a><span data-ttu-id="99558-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99558-105">Syntax</span></span>


```C++
UINT m_ShowStageTop;
```



## <a name="remarks"></a><span data-ttu-id="99558-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="99558-106">Remarks</span></span>

<span data-ttu-id="99558-107">I renderer video devono inviare questo messaggio alla finestra se passano alla modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="99558-107">Video renderers should send this message to the window if they switch to full-screen mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="99558-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99558-108">Requirements</span></span>



| <span data-ttu-id="99558-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="99558-109">Requirement</span></span> | <span data-ttu-id="99558-110">Valore</span><span class="sxs-lookup"><span data-stu-id="99558-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99558-111">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99558-111">Header</span></span><br/>  | <dl> <span data-ttu-id="99558-112"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99558-112"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="99558-113">Libreria</span><span class="sxs-lookup"><span data-stu-id="99558-113">Library</span></span><br/> | <dl> <span data-ttu-id="99558-114"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="99558-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99558-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99558-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99558-116">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="99558-116">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




