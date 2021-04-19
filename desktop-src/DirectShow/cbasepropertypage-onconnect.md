---
description: Il metodo OnConnect fornisce un puntatore IUnknown all'oggetto associato alla pagina delle proprietà.
ms.assetid: 74cae8e1-5347-4e3d-ba5f-6a4efec2ddae
title: Metodo CBasePropertyPage. OnConnect (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38f83a7c491f1591cece8d5d85eb4525a1059d2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332648"
---
# <a name="cbasepropertypageonconnect-method"></a><span data-ttu-id="a0f22-103">Metodo CBasePropertyPage. OnConnect</span><span class="sxs-lookup"><span data-stu-id="a0f22-103">CBasePropertyPage.OnConnect method</span></span>

<span data-ttu-id="a0f22-104">Il `OnConnect` metodo fornisce un puntatore **IUnknown** all'oggetto associato alla pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="a0f22-104">The `OnConnect` method provides an **IUnknown** pointer to the object associated with the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0f22-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0f22-105">Syntax</span></span>


```C++
virtual HRESULT OnConnect(
   IUnknown *pUnknown
);
```



## <a name="parameters"></a><span data-ttu-id="a0f22-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0f22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0f22-107">*pUnknown*</span><span class="sxs-lookup"><span data-stu-id="a0f22-107">*pUnknown*</span></span> 
</dt> <dd>

<span data-ttu-id="a0f22-108">Puntatore all'interfaccia **IUnknown** dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a0f22-108">Pointer to the **IUnknown** interface of the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0f22-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0f22-109">Return value</span></span>

<span data-ttu-id="a0f22-110">L'implementazione della classe di base restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a0f22-110">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0f22-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0f22-111">Remarks</span></span>

<span data-ttu-id="a0f22-112">Il metodo [**CBasePropertyPage:: Seobjects**](cbasepropertypage-setobjects.md) chiama il `OnConnect` metodo.</span><span class="sxs-lookup"><span data-stu-id="a0f22-112">The [**CBasePropertyPage::SetObjects**](cbasepropertypage-setobjects.md) method calls the `OnConnect` method.</span></span> <span data-ttu-id="a0f22-113">Eseguire l'override di questo metodo per archiviare un puntatore all'oggetto specificato da *pUnknown*.</span><span class="sxs-lookup"><span data-stu-id="a0f22-113">Override this method to store a pointer to the object specified by *pUnknown*.</span></span> <span data-ttu-id="a0f22-114">È possibile archiviare il puntatore *pUnknown* o eseguire una query su tale puntatore per altre interfacce.</span><span class="sxs-lookup"><span data-stu-id="a0f22-114">You can either store the *pUnknown* pointer itself, or query that pointer for other interfaces.</span></span> <span data-ttu-id="a0f22-115">Se si archivia il puntatore *pUnknown* , chiamare **AddRef** prima di `OnConnect` restituire.</span><span class="sxs-lookup"><span data-stu-id="a0f22-115">If you store the *pUnknown* pointer, call **AddRef** before `OnConnect` returns.</span></span>

<span data-ttu-id="a0f22-116">Nel metodo [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md) usare il puntatore o i puntatori archiviati per recuperare i valori iniziali per le proprietà della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a0f22-116">In the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method, use the stored pointer (or pointers) to retrieve initial values for the dialog properties.</span></span> <span data-ttu-id="a0f22-117">Nel metodo [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) applicare tutte le modifiche all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a0f22-117">In the [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md) method, apply any changes back to the object.</span></span> <span data-ttu-id="a0f22-118">Rilascia tutti i puntatori nel metodo [**CBasePropertyPage:: Disconnect**](cbasepropertypage-ondisconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="a0f22-118">Release all pointers in the [**CBasePropertyPage::OnDisconnect**](cbasepropertypage-ondisconnect.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="a0f22-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="a0f22-119">Examples</span></span>


```C++
HRESULT CMyProp::OnConnect(IUnknown *pUnk)
{
    ASSERT(m_pOwningFilter == NULL);
    HRESULT hr;
    // Query pUnk for the filter's custom interface.
    hr = pUnk->QueryInterface(IID_ISomeCustomInterface,
             reinterpret_cast<void**>(&m_pOwningFilter));
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="a0f22-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0f22-120">Requirements</span></span>



| <span data-ttu-id="a0f22-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0f22-121">Requirement</span></span> | <span data-ttu-id="a0f22-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a0f22-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0f22-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0f22-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a0f22-124"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0f22-124"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="a0f22-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0f22-125">Library</span></span><br/> | <dl> <span data-ttu-id="a0f22-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a0f22-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0f22-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0f22-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0f22-128">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="a0f22-128">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




