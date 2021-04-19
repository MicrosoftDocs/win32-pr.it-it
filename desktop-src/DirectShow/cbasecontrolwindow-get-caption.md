---
description: Il \_ metodo get Caption Recupera la didascalia della finestra corrente.
ms.assetid: 51ce9cf8-0b2a-4459-b005-02dc45444fd8
title: Metodo CBaseControlWindow.get_Caption (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b8d743c746f833007d91afd4346f7f48c6218dde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326670"
---
# <a name="cbasecontrolwindowget_caption-method"></a><span data-ttu-id="994fd-103">CBaseControlWindow. Get ( \_ Metodo Caption)</span><span class="sxs-lookup"><span data-stu-id="994fd-103">CBaseControlWindow.get\_Caption method</span></span>

<span data-ttu-id="994fd-104">Il `get_Caption` metodo recupera la didascalia della finestra corrente.</span><span class="sxs-lookup"><span data-stu-id="994fd-104">The `get_Caption` method retrieves the current window caption.</span></span>

## <a name="syntax"></a><span data-ttu-id="994fd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="994fd-105">Syntax</span></span>


```C++
HRESULT get_Caption(
   BSTR *pstrCaption
);
```



## <a name="parameters"></a><span data-ttu-id="994fd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="994fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="994fd-107">*pstrCaption*</span><span class="sxs-lookup"><span data-stu-id="994fd-107">*pstrCaption*</span></span> 
</dt> <dd>

<span data-ttu-id="994fd-108">Puntatore alla didascalia della finestra corrente.</span><span class="sxs-lookup"><span data-stu-id="994fd-108">Pointer to the current window caption.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="994fd-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="994fd-109">Return value</span></span>

<span data-ttu-id="994fd-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="994fd-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="994fd-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="994fd-111">Remarks</span></span>

<span data-ttu-id="994fd-112">Per la maggior parte delle finestre di primo livello in un desktop basato su Windows è associato un titolo (didascalia).</span><span class="sxs-lookup"><span data-stu-id="994fd-112">Most top-level windows on a Windows-based desktop have a title (caption) associated with them.</span></span> <span data-ttu-id="994fd-113">Questa proprietà può essere sottoposta a query e impostata tramite l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="994fd-113">This property can be queried and set through the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span> <span data-ttu-id="994fd-114">Qualsiasi set di didascalie sarà visibile solo se nella finestra è \_ applicato lo stile di didascalia WS.</span><span class="sxs-lookup"><span data-stu-id="994fd-114">Any caption set will be visible only if the window has the WS\_CAPTION style applied.</span></span> <span data-ttu-id="994fd-115">In caso contrario, è comunque possibile impostare (e recuperare) la didascalia, anche se non sarà visibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="994fd-115">If it does not, the caption can still be set (and retrieved), although it will not be visible to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="994fd-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="994fd-116">Requirements</span></span>



| <span data-ttu-id="994fd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="994fd-117">Requirement</span></span> | <span data-ttu-id="994fd-118">Valore</span><span class="sxs-lookup"><span data-stu-id="994fd-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="994fd-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="994fd-119">Header</span></span><br/>  | <dl> <span data-ttu-id="994fd-120"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="994fd-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="994fd-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="994fd-121">Library</span></span><br/> | <dl> <span data-ttu-id="994fd-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="994fd-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="994fd-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="994fd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="994fd-124">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="994fd-124">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




