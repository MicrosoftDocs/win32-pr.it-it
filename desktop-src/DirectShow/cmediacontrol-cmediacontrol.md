---
description: Metodo del costruttore.
ms.assetid: 00549dfe-5dd4-445e-bad3-eb6bcfea8f5f
title: Costruttore CMediaControl. CMediaControl (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.CMediaControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63b965ff2484d4db7f7de41d8d524bc74c31ac73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328348"
---
# <a name="cmediacontrolcmediacontrol-constructor"></a><span data-ttu-id="15fe3-103">Costruttore CMediaControl. CMediaControl</span><span class="sxs-lookup"><span data-stu-id="15fe3-103">CMediaControl.CMediaControl constructor</span></span>

<span data-ttu-id="15fe3-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="15fe3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="15fe3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15fe3-105">Syntax</span></span>


```C++
CMediaControl(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="15fe3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="15fe3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15fe3-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="15fe3-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="15fe3-108">Puntatore al nome dell'oggetto a scopo di debug.</span><span class="sxs-lookup"><span data-stu-id="15fe3-108">Pointer to the name of the object for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="15fe3-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="15fe3-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="15fe3-110">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="15fe3-110">Pointer to the owner of this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15fe3-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="15fe3-111">Remarks</span></span>

<span data-ttu-id="15fe3-112">Allocare il parametro *pname* nella memoria statica.</span><span class="sxs-lookup"><span data-stu-id="15fe3-112">Allocate the *pName* parameter in static memory.</span></span> <span data-ttu-id="15fe3-113">Questo nome viene visualizzato nel terminale di debug al momento della creazione e dell'eliminazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="15fe3-113">This name appears on the debugging terminal upon creation and deletion of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="15fe3-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15fe3-114">Requirements</span></span>



| <span data-ttu-id="15fe3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="15fe3-115">Requirement</span></span> | <span data-ttu-id="15fe3-116">Valore</span><span class="sxs-lookup"><span data-stu-id="15fe3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15fe3-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15fe3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="15fe3-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15fe3-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="15fe3-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="15fe3-119">Library</span></span><br/> | <dl> <span data-ttu-id="15fe3-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="15fe3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15fe3-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15fe3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15fe3-122">**Classe CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="15fe3-122">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




