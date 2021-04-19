---
description: Il metodo SetWindowForeground sposta la finestra video in primo piano e, facoltativamente, lo rende attivo.
ms.assetid: 41c26bff-0023-41ad-bca8-8f0c43c94814
title: Metodo CBaseControlWindow. SetWindowForeground (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowForeground
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52c9a37f23b555e140bfd541cf0b5e8e782f8d51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333362"
---
# <a name="cbasecontrolwindowsetwindowforeground-method"></a><span data-ttu-id="090d9-103">CBaseControlWindow. SetWindowForeground, metodo</span><span class="sxs-lookup"><span data-stu-id="090d9-103">CBaseControlWindow.SetWindowForeground method</span></span>

<span data-ttu-id="090d9-104">Il `SetWindowForeground` metodo sposta la finestra del video in primo piano e, facoltativamente, lo rende attivo.</span><span class="sxs-lookup"><span data-stu-id="090d9-104">The `SetWindowForeground` method moves the video window to the foreground and optionally gives it focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="090d9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="090d9-105">Syntax</span></span>


```C++
HRESULT SetWindowForeground(
   long Focus
);
```



## <a name="parameters"></a><span data-ttu-id="090d9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="090d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="090d9-107">*Lo stato attivo*</span><span class="sxs-lookup"><span data-stu-id="090d9-107">*Focus*</span></span> 
</dt> <dd>

<span data-ttu-id="090d9-108">Valore che specifica se la finestra video otterrà lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="090d9-108">Value that specifies whether the video window will get focus.</span></span> <span data-ttu-id="090d9-109">Il valore 1 indica lo stato attivo della finestra e 0 non lo è.</span><span class="sxs-lookup"><span data-stu-id="090d9-109">A value of  1 gives the window focus and 0 does not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="090d9-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="090d9-110">Return value</span></span>

<span data-ttu-id="090d9-111">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="090d9-111">Returns one of the following values.</span></span>



| <span data-ttu-id="090d9-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="090d9-112">Return code</span></span>                                                                                           | <span data-ttu-id="090d9-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="090d9-113">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="090d9-114"><dt>**NOERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="090d9-114"><dt>**NOERROR**</dt></span></span> </dl>                | <span data-ttu-id="090d9-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="090d9-115">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="090d9-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="090d9-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl>          | <span data-ttu-id="090d9-117">Lo stato attivo non è uguale a 1 o 0.</span><span class="sxs-lookup"><span data-stu-id="090d9-117">Focus doesn't equal  1 or 0.</span></span><br/>                                   |
| <dl> <span data-ttu-id="090d9-118"><dt>**VFW \_ E \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="090d9-118"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="090d9-119">Il filtro corrente non è connesso a un grafico di filtro completo.</span><span class="sxs-lookup"><span data-stu-id="090d9-119">The current filter isn't connected to a complete filter graph.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="090d9-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="090d9-120">Requirements</span></span>



| <span data-ttu-id="090d9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="090d9-121">Requirement</span></span> | <span data-ttu-id="090d9-122">Valore</span><span class="sxs-lookup"><span data-stu-id="090d9-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="090d9-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="090d9-123">Header</span></span><br/>  | <dl> <span data-ttu-id="090d9-124"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="090d9-124"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="090d9-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="090d9-125">Library</span></span><br/> | <dl> <span data-ttu-id="090d9-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="090d9-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="090d9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="090d9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="090d9-128">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="090d9-128">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




