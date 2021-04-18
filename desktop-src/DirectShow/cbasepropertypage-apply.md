---
description: "Il metodo Apply applica i valori correnti della pagina delle proprietà all'oggetto associato alla pagina delle proprietà. Questo metodo implementa il Metodo IPropertyPage:: Apply."
ms.assetid: 9fe759d1-2b46-4489-b7b8-b5a35330091d
title: Metodo CBasePropertyPage. Apply (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Apply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21d1208979cca167b059cb720c492ac51c362c39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329421"
---
# <a name="cbasepropertypageapply-method"></a><span data-ttu-id="02972-104">Metodo CBasePropertyPage. Apply</span><span class="sxs-lookup"><span data-stu-id="02972-104">CBasePropertyPage.Apply method</span></span>

<span data-ttu-id="02972-105">Il `Apply` metodo applica i valori correnti della pagina delle proprietà all'oggetto associato alla pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="02972-105">The `Apply` method applies the current property page values to the object associated with the property page.</span></span> <span data-ttu-id="02972-106">Questo metodo implementa il metodo **IPropertyPage:: Apply** .</span><span class="sxs-lookup"><span data-stu-id="02972-106">This method implements the **IPropertyPage::Apply** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="02972-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02972-107">Syntax</span></span>


```C++
HRESULT Apply();
```



## <a name="parameters"></a><span data-ttu-id="02972-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="02972-108">Parameters</span></span>

<span data-ttu-id="02972-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="02972-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="02972-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02972-110">Return value</span></span>

<span data-ttu-id="02972-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="02972-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="02972-112">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="02972-112">Possible values include the following.</span></span>



| <span data-ttu-id="02972-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="02972-113">Return code</span></span>                                                                                  | <span data-ttu-id="02972-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02972-114">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="02972-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="02972-115"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="02972-116">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="02972-116">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="02972-117"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="02972-117"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="02972-118">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="02972-118">Unexpected failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="02972-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="02972-119">Remarks</span></span>

<span data-ttu-id="02972-120">Se il flag [**CBasePropertyPage:: m \_ BDirty**](cbasepropertypage-m-bdirty.md) è **true**, questo metodo chiama il metodo [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) .</span><span class="sxs-lookup"><span data-stu-id="02972-120">If the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag is **TRUE**, this method calls the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method.</span></span> <span data-ttu-id="02972-121">Eseguire l'override di **OnApplyChanges** per applicare le modifiche all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="02972-121">Override **OnApplyChanges** to apply the changes to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="02972-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02972-122">Requirements</span></span>



| <span data-ttu-id="02972-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="02972-123">Requirement</span></span> | <span data-ttu-id="02972-124">Valore</span><span class="sxs-lookup"><span data-stu-id="02972-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02972-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02972-125">Header</span></span><br/>  | <dl> <span data-ttu-id="02972-126"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02972-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="02972-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="02972-127">Library</span></span><br/> | <dl> <span data-ttu-id="02972-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="02972-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02972-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02972-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02972-130">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="02972-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




