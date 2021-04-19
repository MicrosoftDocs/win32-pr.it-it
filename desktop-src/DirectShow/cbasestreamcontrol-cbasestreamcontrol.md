---
description: Metodo del costruttore.
ms.assetid: c0eff80f-04d3-4919-bb27-1b76c1bd1cce
title: Costruttore CBaseStreamControl. CBaseStreamControl (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d325a48476fe2a80b7424850eb71a9d667cb60e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326566"
---
# <a name="cbasestreamcontrolcbasestreamcontrol-constructor"></a><span data-ttu-id="24179-103">Costruttore CBaseStreamControl. CBaseStreamControl</span><span class="sxs-lookup"><span data-stu-id="24179-103">CBaseStreamControl.CBaseStreamControl constructor</span></span>

<span data-ttu-id="24179-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="24179-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="24179-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24179-105">Syntax</span></span>


```C++
CBaseStreamControl(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="24179-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="24179-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24179-107">*PHR*</span><span class="sxs-lookup"><span data-stu-id="24179-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="24179-108">Puntatore a un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24179-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="24179-109">Se il costruttore ha esito negativo, questo parametro riceve un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="24179-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="24179-110">In tal caso, lo stato dell'oggetto non è valido.</span><span class="sxs-lookup"><span data-stu-id="24179-110">If this occurs, the object is not in a valid state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24179-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24179-111">Requirements</span></span>



| <span data-ttu-id="24179-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="24179-112">Requirement</span></span> | <span data-ttu-id="24179-113">Valore</span><span class="sxs-lookup"><span data-stu-id="24179-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24179-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24179-114">Header</span></span><br/>  | <dl> <span data-ttu-id="24179-115"><dt>Strmctl. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24179-115"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="24179-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="24179-116">Library</span></span><br/> | <dl> <span data-ttu-id="24179-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="24179-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24179-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24179-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24179-119">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="24179-119">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




