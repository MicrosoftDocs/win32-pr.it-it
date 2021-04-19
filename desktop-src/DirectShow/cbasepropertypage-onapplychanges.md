---
description: Il metodo OnApplyChanges viene chiamato quando l'utente applica le modifiche alla pagina delle proprietà.
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: Metodo CBasePropertyPage. OnApplyChanges (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnApplyChanges
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbcea308a8daaa8b9fdf15be765dc5d3a0df182c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332649"
---
# <a name="cbasepropertypageonapplychanges-method"></a><span data-ttu-id="c2e7c-103">CBasePropertyPage. OnApplyChanges, metodo</span><span class="sxs-lookup"><span data-stu-id="c2e7c-103">CBasePropertyPage.OnApplyChanges method</span></span>

<span data-ttu-id="c2e7c-104">Il `OnApplyChanges` metodo viene chiamato quando l'utente applica le modifiche alla pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="c2e7c-104">The `OnApplyChanges` method is called when the user applies changes to the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e7c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2e7c-105">Syntax</span></span>


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a><span data-ttu-id="c2e7c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2e7c-106">Parameters</span></span>

<span data-ttu-id="c2e7c-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c2e7c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c2e7c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2e7c-108">Return value</span></span>

<span data-ttu-id="c2e7c-109">L'implementazione della classe di base restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c2e7c-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2e7c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2e7c-110">Remarks</span></span>

<span data-ttu-id="c2e7c-111">Il metodo [**CBasePropertyPage:: Apply**](cbasepropertypage-apply.md) chiama `OnApplyChanges` se il flag [**CBasePropertyPage:: m \_ bDirty**](cbasepropertypage-m-bdirty.md) è **true**.</span><span class="sxs-lookup"><span data-stu-id="c2e7c-111">The [**CBasePropertyPage::Apply**](cbasepropertypage-apply.md) method calls `OnApplyChanges` if the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag is **TRUE**.</span></span> <span data-ttu-id="c2e7c-112">Eseguire l'override `OnApplyChanges` di per elaborare le modifiche e reimpostare **m \_ bDirty** su **false**.</span><span class="sxs-lookup"><span data-stu-id="c2e7c-112">Override `OnApplyChanges` to process the changes and reset **m\_bDirty** to **FALSE**.</span></span>

## <a name="examples"></a><span data-ttu-id="c2e7c-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="c2e7c-113">Examples</span></span>


```C++
HRESULT CMyProp::OnApplyChanges(void)
{
    ASSERT(m_pOwningFilter != NULL);
    return m_pOwningFilter->SetSomeProperty(&m_lNewVal);
}
```



## <a name="requirements"></a><span data-ttu-id="c2e7c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2e7c-114">Requirements</span></span>



| <span data-ttu-id="c2e7c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2e7c-115">Requirement</span></span> | <span data-ttu-id="c2e7c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c2e7c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e7c-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2e7c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c2e7c-118"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c2e7c-118"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="c2e7c-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="c2e7c-119">Library</span></span><br/> | <dl> <span data-ttu-id="c2e7c-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c2e7c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2e7c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2e7c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e7c-122">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="c2e7c-122">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




