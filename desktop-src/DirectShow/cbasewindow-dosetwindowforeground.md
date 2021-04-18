---
description: Il metodo DoSetWindowForeground porta la finestra in primo piano.
ms.assetid: 5aace88b-14c0-41ce-95a3-0e255ca56ae6
title: Metodo CBaseWindow. DoSetWindowForeground (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoSetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 16a4c8bf41c042c99624289fa26fe252dee62747
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325328"
---
# <a name="cbasewindowdosetwindowforeground-method"></a><span data-ttu-id="8d830-103">CBaseWindow. DoSetWindowForeground, metodo</span><span class="sxs-lookup"><span data-stu-id="8d830-103">CBaseWindow.DoSetWindowForeground method</span></span>

<span data-ttu-id="8d830-104">Il `DoSetWindowForeground` metodo porta la finestra in primo piano.</span><span class="sxs-lookup"><span data-stu-id="8d830-104">The `DoSetWindowForeground` method brings the window to the foreground.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d830-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d830-105">Syntax</span></span>


```C++
void DoSetWindowForeground(
   BOOL bFocus
);
```



## <a name="parameters"></a><span data-ttu-id="8d830-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d830-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d830-107">*bFocus*</span><span class="sxs-lookup"><span data-stu-id="8d830-107">*bFocus*</span></span> 
</dt> <dd>

<span data-ttu-id="8d830-108">Valore booleano che specifica se assegnare lo stato attivo della finestra.</span><span class="sxs-lookup"><span data-stu-id="8d830-108">Boolean value that specifies whether to give the window focus.</span></span> <span data-ttu-id="8d830-109">Se il valore è **true**, la finestra ottiene lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="8d830-109">If the value is **TRUE**, the window gains focus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d830-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d830-110">Return value</span></span>

<span data-ttu-id="8d830-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8d830-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d830-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d830-112">Requirements</span></span>



| <span data-ttu-id="8d830-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d830-113">Requirement</span></span> | <span data-ttu-id="8d830-114">Valore</span><span class="sxs-lookup"><span data-stu-id="8d830-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d830-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d830-115">Header</span></span><br/>  | <dl> <span data-ttu-id="8d830-116"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d830-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8d830-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="8d830-117">Library</span></span><br/> | <dl> <span data-ttu-id="8d830-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8d830-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d830-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d830-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d830-120">**Classe CBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="8d830-120">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




