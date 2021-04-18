---
description: "Il Metodo SetPageSite Inizializza la pagina delle proprietà e fornisce un puntatore all'interfaccia IPropertyPageSite del frame della proprietà. Questo metodo implementa il Metodo IPropertyPage:: SetPageSite."
ms.assetid: 16c4633f-2f91-4b1b-a47c-4ef945c3af00
title: Metodo CBasePropertyPage. SetPageSite (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetPageSite
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a165ff60971cef3d2373e0f07b2abee554308279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325369"
---
# <a name="cbasepropertypagesetpagesite-method"></a><span data-ttu-id="b65e7-104">CBasePropertyPage. SetPageSite, metodo</span><span class="sxs-lookup"><span data-stu-id="b65e7-104">CBasePropertyPage.SetPageSite method</span></span>

<span data-ttu-id="b65e7-105">Il `SetPageSite` metodo inizializza la pagina delle proprietà e fornisce un puntatore all'interfaccia **IPropertyPageSite** del frame della proprietà.</span><span class="sxs-lookup"><span data-stu-id="b65e7-105">The `SetPageSite` method initializes the property page and provides a pointer to the property frame's **IPropertyPageSite** interface.</span></span> <span data-ttu-id="b65e7-106">Questo metodo implementa il metodo **IPropertyPage:: SetPageSite** .</span><span class="sxs-lookup"><span data-stu-id="b65e7-106">This method implements the **IPropertyPage::SetPageSite** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b65e7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b65e7-107">Syntax</span></span>


```C++
HRESULT SetPageSite(
   IPropertyPageSite *pPageSite
);
```



## <a name="parameters"></a><span data-ttu-id="b65e7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b65e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b65e7-109">*pPageSite*</span><span class="sxs-lookup"><span data-stu-id="b65e7-109">*pPageSite*</span></span> 
</dt> <dd>

<span data-ttu-id="b65e7-110">Puntatore all'interfaccia **IPropertyPageSite** .</span><span class="sxs-lookup"><span data-stu-id="b65e7-110">Pointer to the **IPropertyPageSite** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b65e7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b65e7-111">Return value</span></span>

<span data-ttu-id="b65e7-112">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b65e7-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b65e7-113">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="b65e7-113">Possible values include the following.</span></span>



| <span data-ttu-id="b65e7-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b65e7-114">Return code</span></span>                                                                                  | <span data-ttu-id="b65e7-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b65e7-115">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="b65e7-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b65e7-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="b65e7-117">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b65e7-117">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="b65e7-118"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="b65e7-118"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="b65e7-119">Errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="b65e7-119">Unexpected failure.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b65e7-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="b65e7-120">Remarks</span></span>

<span data-ttu-id="b65e7-121">Il metodo archivia il puntatore *pPageSite* nella variabile membro [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) .</span><span class="sxs-lookup"><span data-stu-id="b65e7-121">The method stores the *pPageSite* pointer in the [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="b65e7-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b65e7-122">Requirements</span></span>



| <span data-ttu-id="b65e7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b65e7-123">Requirement</span></span> | <span data-ttu-id="b65e7-124">Valore</span><span class="sxs-lookup"><span data-stu-id="b65e7-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b65e7-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b65e7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b65e7-126"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b65e7-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="b65e7-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="b65e7-127">Library</span></span><br/> | <dl> <span data-ttu-id="b65e7-128"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b65e7-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b65e7-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b65e7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b65e7-130">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="b65e7-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




