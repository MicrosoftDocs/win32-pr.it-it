---
description: Il \_ metodo Put Caption Imposta il titolo o la didascalia della finestra.
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: Metodo CBaseControlWindow.put_Caption (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aca8e5e7ad04acae9fab1cfe2d44f982266805e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328352"
---
# <a name="cbasecontrolwindowput_caption-method"></a><span data-ttu-id="273b5-103">CBaseControlWindow. Put, \_ Metodo didascalia</span><span class="sxs-lookup"><span data-stu-id="273b5-103">CBaseControlWindow.put\_Caption method</span></span>

<span data-ttu-id="273b5-104">Il `put_Caption` metodo imposta il titolo o la didascalia della finestra.</span><span class="sxs-lookup"><span data-stu-id="273b5-104">The `put_Caption` method sets the window title or caption.</span></span>

## <a name="syntax"></a><span data-ttu-id="273b5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="273b5-105">Syntax</span></span>


```C++
HRESULT put_Caption(
   BSTR strCaption
);
```



## <a name="parameters"></a><span data-ttu-id="273b5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="273b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="273b5-107">*strCaption*</span><span class="sxs-lookup"><span data-stu-id="273b5-107">*strCaption*</span></span> 
</dt> <dd>

<span data-ttu-id="273b5-108">Nuova didascalia della finestra.</span><span class="sxs-lookup"><span data-stu-id="273b5-108">New window caption.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="273b5-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="273b5-109">Return value</span></span>

<span data-ttu-id="273b5-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="273b5-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="273b5-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="273b5-111">Remarks</span></span>

<span data-ttu-id="273b5-112">Per la maggior parte delle finestre di primo livello in un desktop basato su Windows è associato un titolo (didascalia).</span><span class="sxs-lookup"><span data-stu-id="273b5-112">Most top-level windows on a Windows-based desktop have a title (caption) associated with them.</span></span> <span data-ttu-id="273b5-113">Questa proprietà può essere sottoposta a query e impostata tramite l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="273b5-113">This property can be queried and set through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="273b5-114">Qualsiasi set di didascalie sarà visibile solo se nella finestra è \_ applicato lo stile di didascalia WS.</span><span class="sxs-lookup"><span data-stu-id="273b5-114">Any caption set will be visible only if the window has the WS\_CAPTION style applied.</span></span> <span data-ttu-id="273b5-115">In caso contrario, è comunque possibile impostare (e recuperare) la didascalia, anche se non sarà visibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="273b5-115">If it does not, the caption can still be set (and retrieved), although it will not be visible to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="273b5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="273b5-116">Requirements</span></span>



| <span data-ttu-id="273b5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="273b5-117">Requirement</span></span> | <span data-ttu-id="273b5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="273b5-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="273b5-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="273b5-119">Header</span></span><br/>  | <dl> <span data-ttu-id="273b5-120"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="273b5-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="273b5-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="273b5-121">Library</span></span><br/> | <dl> <span data-ttu-id="273b5-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="273b5-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="273b5-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="273b5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="273b5-124">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="273b5-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




