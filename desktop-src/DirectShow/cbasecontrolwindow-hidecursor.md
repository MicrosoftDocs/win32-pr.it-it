---
description: Il metodo HideCursor nasconde o Visualizza il cursore.
ms.assetid: 80175d1b-9874-4295-9ebc-b0d78961a263
title: Metodo CBaseControlWindow. HideCursor (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.HideCursor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0f379c719052de77b54dba47f83b34ae235415f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329266"
---
# <a name="cbasecontrolwindowhidecursor-method"></a><span data-ttu-id="85012-103">CBaseControlWindow. HideCursor, metodo</span><span class="sxs-lookup"><span data-stu-id="85012-103">CBaseControlWindow.HideCursor method</span></span>

<span data-ttu-id="85012-104">Il `HideCursor` metodo nasconde o Visualizza il cursore.</span><span class="sxs-lookup"><span data-stu-id="85012-104">The `HideCursor` method hides or displays the cursor.</span></span>

## <a name="syntax"></a><span data-ttu-id="85012-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85012-105">Syntax</span></span>


```C++
HRESULT HideCursor(
   long HideCursor
);
```



## <a name="parameters"></a><span data-ttu-id="85012-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="85012-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85012-107">*HideCursor*</span><span class="sxs-lookup"><span data-stu-id="85012-107">*HideCursor*</span></span> 
</dt> <dd>

<span data-ttu-id="85012-108">Valore che specifica se visualizzare il cursore.</span><span class="sxs-lookup"><span data-stu-id="85012-108">Value specifying whether to show the cursor.</span></span> <span data-ttu-id="85012-109">Impostare su OATRUE per nascondere il cursore oppure OAFALSE per visualizzare il cursore.</span><span class="sxs-lookup"><span data-stu-id="85012-109">Set to OATRUE to hide the cursor, or OAFALSE to display the cursor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85012-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85012-110">Return value</span></span>

<span data-ttu-id="85012-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="85012-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="85012-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85012-112">Requirements</span></span>



| <span data-ttu-id="85012-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="85012-113">Requirement</span></span> | <span data-ttu-id="85012-114">Valore</span><span class="sxs-lookup"><span data-stu-id="85012-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85012-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85012-115">Header</span></span><br/>  | <dl> <span data-ttu-id="85012-116"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85012-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="85012-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="85012-117">Library</span></span><br/> | <dl> <span data-ttu-id="85012-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="85012-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85012-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85012-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85012-120">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="85012-120">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




