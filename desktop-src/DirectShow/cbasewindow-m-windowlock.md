---
description: Sezione critica, per serializzare l'accesso all'oggetto.
ms.assetid: 24a5b1b2-209e-4262-aa48-fd4534b2da57
title: 'Membro CBaseWindow:: m_WindowLock (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_WindowLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38227e505f2e05e024c8cecf12ab3cb8c336bfe1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325773"
---
# <a name="cbasewindowm_windowlock-member"></a><span data-ttu-id="a0bd5-103">Membro WindowLock di CBaseWindow:: m \_</span><span class="sxs-lookup"><span data-stu-id="a0bd5-103">CBaseWindow::m\_WindowLock member</span></span>

<span data-ttu-id="a0bd5-104">Sezione critica, per serializzare l'accesso all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a0bd5-104">Critical section, to serialize access to the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0bd5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0bd5-105">Syntax</span></span>


```C++
CCritSec m_WindowLock;
```



## <a name="requirements"></a><span data-ttu-id="a0bd5-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0bd5-106">Requirements</span></span>



| <span data-ttu-id="a0bd5-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0bd5-107">Requirement</span></span> | <span data-ttu-id="a0bd5-108">Valore</span><span class="sxs-lookup"><span data-stu-id="a0bd5-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0bd5-109">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0bd5-109">Header</span></span><br/>  | <dl> <span data-ttu-id="a0bd5-110"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0bd5-110"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a0bd5-111">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0bd5-111">Library</span></span><br/> | <dl> <span data-ttu-id="a0bd5-112"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a0bd5-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0bd5-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0bd5-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0bd5-114">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="a0bd5-114">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




