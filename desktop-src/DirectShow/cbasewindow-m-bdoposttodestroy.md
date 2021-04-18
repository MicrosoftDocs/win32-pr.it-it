---
description: Flag che specifica se la finestra Invia o invia il messaggio di distruzione.
ms.assetid: 553a372e-1abe-4661-bfa5-b8a63be63c72
title: 'Membro CBaseWindow:: m_bDoPostToDestroy (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bDoPostToDestroy
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 804d0910760ddac5ea4d74979293f43e5b189225
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330518"
---
# <a name="cbasewindowm_bdoposttodestroy-member"></a><span data-ttu-id="2dd00-103">Membro bDoPostToDestroy di CBaseWindow:: m \_</span><span class="sxs-lookup"><span data-stu-id="2dd00-103">CBaseWindow::m\_bDoPostToDestroy member</span></span>

<span data-ttu-id="2dd00-104">Flag che specifica se la finestra Invia o invia il messaggio di distruzione.</span><span class="sxs-lookup"><span data-stu-id="2dd00-104">Flag that specifies whether the window posts or sends its destruction message.</span></span> <span data-ttu-id="2dd00-105">Se **true**, il metodo [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) usa la funzione **PostMessage** per inviare a se stesso un messaggio di distruzione privata.</span><span class="sxs-lookup"><span data-stu-id="2dd00-105">If **TRUE**, the [**CBaseWindow::DoneWithWindow**](cbasewindow-donewithwindow.md) method uses the **PostMessage** function to send itself a private destruction message.</span></span> <span data-ttu-id="2dd00-106">Se **false**, **DoneWithWindow** utilizza la funzione **SendMessage** per inviare il messaggio.</span><span class="sxs-lookup"><span data-stu-id="2dd00-106">If **FALSE**, **DoneWithWindow** uses the **SendMessage** function to send the message.</span></span> <span data-ttu-id="2dd00-107">Per impostazione predefinita, il valore è **false**.</span><span class="sxs-lookup"><span data-stu-id="2dd00-107">By default, the value is **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd00-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2dd00-108">Syntax</span></span>


```C++
BOOL m_bDoPostToDestroy;
```



## <a name="requirements"></a><span data-ttu-id="2dd00-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2dd00-109">Requirements</span></span>



| <span data-ttu-id="2dd00-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dd00-110">Requirement</span></span> | <span data-ttu-id="2dd00-111">Valore</span><span class="sxs-lookup"><span data-stu-id="2dd00-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dd00-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2dd00-112">Header</span></span><br/>  | <dl> <span data-ttu-id="2dd00-113"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2dd00-113"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2dd00-114">Libreria</span><span class="sxs-lookup"><span data-stu-id="2dd00-114">Library</span></span><br/> | <dl> <span data-ttu-id="2dd00-115"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2dd00-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dd00-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2dd00-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dd00-117">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="2dd00-117">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




