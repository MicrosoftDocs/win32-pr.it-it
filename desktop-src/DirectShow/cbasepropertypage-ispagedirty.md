---
description: "Il metodo IsPageDirty indica se la pagina delle proprietà è stata modificata dopo l'attivazione o dopo la chiamata più recente a IPropertyPage:: Apply. Questo metodo implementa il Metodo IPropertyPage:: IsPageDirty."
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: Metodo CBasePropertyPage. IsPageDirty (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.IsPageDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c69c2e7d480f63542e146c73e56b9e692693f665
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330687"
---
# <a name="cbasepropertypageispagedirty-method"></a><span data-ttu-id="558e7-104">CBasePropertyPage. IsPageDirty, metodo</span><span class="sxs-lookup"><span data-stu-id="558e7-104">CBasePropertyPage.IsPageDirty method</span></span>

<span data-ttu-id="558e7-105">Il `IsPageDirty` metodo indica se la pagina delle proprietà è stata modificata dopo l'attivazione o dopo la chiamata più recente a **IPropertyPage:: Apply**.</span><span class="sxs-lookup"><span data-stu-id="558e7-105">The `IsPageDirty` method indicates whether the property page has changed since it was activated or since the most recent call to **IPropertyPage::Apply**.</span></span> <span data-ttu-id="558e7-106">Questo metodo implementa il metodo **IPropertyPage:: IsPageDirty** .</span><span class="sxs-lookup"><span data-stu-id="558e7-106">This method implements the **IPropertyPage::IsPageDirty** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="558e7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="558e7-107">Syntax</span></span>


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a><span data-ttu-id="558e7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="558e7-108">Parameters</span></span>

<span data-ttu-id="558e7-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="558e7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="558e7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="558e7-110">Return value</span></span>

<span data-ttu-id="558e7-111">Restituisce \_ OK se [**CBasePropertyPage:: m \_ bDirty**](cbasepropertypage-m-bdirty.md) è **true** oppure S \_ false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="558e7-111">Returns S\_OK if [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) is **TRUE**, or S\_FALSE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="558e7-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="558e7-112">Requirements</span></span>



| <span data-ttu-id="558e7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="558e7-113">Requirement</span></span> | <span data-ttu-id="558e7-114">Valore</span><span class="sxs-lookup"><span data-stu-id="558e7-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="558e7-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="558e7-115">Header</span></span><br/>  | <dl> <span data-ttu-id="558e7-116"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="558e7-116"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="558e7-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="558e7-117">Library</span></span><br/> | <dl> <span data-ttu-id="558e7-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="558e7-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="558e7-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="558e7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="558e7-120">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="558e7-120">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




