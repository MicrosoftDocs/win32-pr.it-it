---
description: Il metodo Deactivate Elimina la finestra di dialogo. Questo metodo implementa il Metodo IPropertyPage::D ttiva.
ms.assetid: f2d2f15f-15f6-4902-bafc-f58a684ff193
title: Metodo CBasePropertyPage. Deactivate (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Deactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63a843502fc735cc41ff3656e83ef3d6cb839a19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329420"
---
# <a name="cbasepropertypagedeactivate-method"></a><span data-ttu-id="20591-104">Metodo CBasePropertyPage. Deactivate</span><span class="sxs-lookup"><span data-stu-id="20591-104">CBasePropertyPage.Deactivate method</span></span>

<span data-ttu-id="20591-105">Il `Deactivate` metodo elimina la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="20591-105">The `Deactivate` method destroys the dialog window.</span></span> <span data-ttu-id="20591-106">Questo metodo implementa il metodo **IPropertyPage::D ttiva** .</span><span class="sxs-lookup"><span data-stu-id="20591-106">This method implements the **IPropertyPage::Deactivate** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="20591-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20591-107">Syntax</span></span>


```C++
HRESULT Deactivate();
```



## <a name="parameters"></a><span data-ttu-id="20591-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="20591-108">Parameters</span></span>

<span data-ttu-id="20591-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="20591-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="20591-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="20591-110">Return value</span></span>

<span data-ttu-id="20591-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="20591-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="20591-112">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="20591-112">Possible values include the following.</span></span>



| <span data-ttu-id="20591-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="20591-113">Return code</span></span>                                                                                  | <span data-ttu-id="20591-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20591-114">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="20591-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="20591-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="20591-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="20591-116">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="20591-117"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="20591-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="20591-118">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="20591-118">Unexpected failure.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="20591-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20591-119">Requirements</span></span>



| <span data-ttu-id="20591-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="20591-120">Requirement</span></span> | <span data-ttu-id="20591-121">Valore</span><span class="sxs-lookup"><span data-stu-id="20591-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20591-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="20591-122">Header</span></span><br/>  | <dl> <span data-ttu-id="20591-123"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20591-123"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="20591-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="20591-124">Library</span></span><br/> | <dl> <span data-ttu-id="20591-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="20591-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20591-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20591-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20591-127">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="20591-127">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> <dt>

[<span data-ttu-id="20591-128">**CBasePropertyPage:: OnDeactivate**</span><span class="sxs-lookup"><span data-stu-id="20591-128">**CBasePropertyPage::OnDeactivate**</span></span>](cbasepropertypage-ondeactivate.md)
</dt> </dl>

 

 




