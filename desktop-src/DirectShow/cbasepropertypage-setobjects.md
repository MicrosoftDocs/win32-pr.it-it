---
description: 'Il metodo seobjects fornisce i puntatori IUnknown per gli oggetti associati alla pagina delle proprietà. Questo metodo implementa il Metodo IPropertyPage:: seobjects.'
ms.assetid: 11ca1e70-772c-414e-9647-7e4c4084c0d3
title: Metodo CBasePropertyPage. seobjects (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetObjects
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 197c5eb82de76fb5a5f606d8a161e853b0c1e8f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330411"
---
# <a name="cbasepropertypagesetobjects-method"></a><span data-ttu-id="0a4b6-104">Metodo CBasePropertyPage. seobjects</span><span class="sxs-lookup"><span data-stu-id="0a4b6-104">CBasePropertyPage.SetObjects method</span></span>

<span data-ttu-id="0a4b6-105">Il `SetObjects` metodo fornisce i puntatori **IUnknown** per gli oggetti associati alla pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="0a4b6-105">The `SetObjects` method provides **IUnknown** pointers for the objects associated with the property page.</span></span> <span data-ttu-id="0a4b6-106">Questo metodo implementa il metodo **IPropertyPage:: Seobjects** .</span><span class="sxs-lookup"><span data-stu-id="0a4b6-106">This method implements the **IPropertyPage::SetObjects** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a4b6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a4b6-107">Syntax</span></span>


```C++
HRESULT SetObjects(
   ULONG     cObjects,
   LPUNKNOWN *ppUnk
);
```



## <a name="parameters"></a><span data-ttu-id="0a4b6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a4b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a4b6-109">*cObjects*</span><span class="sxs-lookup"><span data-stu-id="0a4b6-109">*cObjects*</span></span> 
</dt> <dd>

<span data-ttu-id="0a4b6-110">Specifica il numero di puntatori **IUnknown** nella matrice specificata da *ppunk*.</span><span class="sxs-lookup"><span data-stu-id="0a4b6-110">Specifies the number of **IUnknown** pointers in the array specified by *ppUnk*.</span></span>

</dd> <dt>

<span data-ttu-id="0a4b6-111">*ppUnk*</span><span class="sxs-lookup"><span data-stu-id="0a4b6-111">*ppUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="0a4b6-112">Specifica una matrice di puntatori **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="0a4b6-112">Specifies an array of **IUnknown** pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a4b6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a4b6-113">Return value</span></span>

<span data-ttu-id="0a4b6-114">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0a4b6-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0a4b6-115">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="0a4b6-115">Possible values include the following.</span></span>



| <span data-ttu-id="0a4b6-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0a4b6-116">Return code</span></span>                                                                                  | <span data-ttu-id="0a4b6-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0a4b6-117">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="0a4b6-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0a4b6-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0a4b6-119">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0a4b6-119">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="0a4b6-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="0a4b6-120"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="0a4b6-121">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="0a4b6-121">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="0a4b6-122"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="0a4b6-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="0a4b6-123">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="0a4b6-123">Unexpected failure.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="0a4b6-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a4b6-124">Remarks</span></span>

<span data-ttu-id="0a4b6-125">Sebbene *ppunk* specifichi una matrice di puntatori **IUnknown** , la classe **CBasePropertyPage** è progettata solo per supportare un oggetto associato.</span><span class="sxs-lookup"><span data-stu-id="0a4b6-125">Although *ppUnk* specifies an array of **IUnknown** pointers, the **CBasePropertyPage** class is designed only to support one associated object.</span></span> <span data-ttu-id="0a4b6-126">Se *CObjects* è maggiore di 1, il metodo restituisce E \_ imprevisto.</span><span class="sxs-lookup"><span data-stu-id="0a4b6-126">If *cObjects* is greater than 1, the method returns E\_UNEXPECTED.</span></span>

<span data-ttu-id="0a4b6-127">Se *CObjects* è uguale a 1, questo metodo chiama il metodo [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="0a4b6-127">If *cObjects* equals 1, this method calls the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method.</span></span> <span data-ttu-id="0a4b6-128">Se *CObjects* è uguale a 0, questo metodo chiama il metodo [**CBasePropertyPage:: Disconnect**](cbasepropertypage-ondisconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="0a4b6-128">If *cObjects* equals 0, this method calls the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method.</span></span> <span data-ttu-id="0a4b6-129">La classe derivata deve eseguire l'override di entrambi i metodi; per informazioni dettagliate, vedere la sezione Osservazioni per tali metodi.</span><span class="sxs-lookup"><span data-stu-id="0a4b6-129">The derived class should override both of those methods; for details, see the remarks for those methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a4b6-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a4b6-130">Requirements</span></span>



| <span data-ttu-id="0a4b6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a4b6-131">Requirement</span></span> | <span data-ttu-id="0a4b6-132">Valore</span><span class="sxs-lookup"><span data-stu-id="0a4b6-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a4b6-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a4b6-133">Header</span></span><br/>  | <dl> <span data-ttu-id="0a4b6-134"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0a4b6-134"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="0a4b6-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="0a4b6-135">Library</span></span><br/> | <dl> <span data-ttu-id="0a4b6-136"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0a4b6-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a4b6-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a4b6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a4b6-138">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="0a4b6-138">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




