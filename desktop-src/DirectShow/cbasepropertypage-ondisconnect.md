---
description: Il metodo Disconnect viene chiamato quando la pagina delle proprietà deve rilasciare l'oggetto associato.
ms.assetid: 55bab0ca-587e-405c-9025-f391cf08a620
title: Metodo CBasePropertyPage. Disconnect (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDisconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd251d20ca82ad0374a613d9ee73f0eaee21d31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325198"
---
# <a name="cbasepropertypageondisconnect-method"></a><span data-ttu-id="821fc-103">Metodo CBasePropertyPage. Disconnect</span><span class="sxs-lookup"><span data-stu-id="821fc-103">CBasePropertyPage.OnDisconnect method</span></span>

<span data-ttu-id="821fc-104">Il `OnDisconnect` metodo viene chiamato quando la pagina delle proprietà deve rilasciare l'oggetto associato.</span><span class="sxs-lookup"><span data-stu-id="821fc-104">The `OnDisconnect` method is called when the property page should release the associated object.</span></span>

## <a name="syntax"></a><span data-ttu-id="821fc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="821fc-105">Syntax</span></span>


```C++
virtual HRESULT OnDisconnect();
```



## <a name="parameters"></a><span data-ttu-id="821fc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="821fc-106">Parameters</span></span>

<span data-ttu-id="821fc-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="821fc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="821fc-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="821fc-108">Return value</span></span>

<span data-ttu-id="821fc-109">L'implementazione della classe di base restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="821fc-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="821fc-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="821fc-110">Remarks</span></span>

<span data-ttu-id="821fc-111">Il metodo [**CBasePropertyPage:: Seobjects**](cbasepropertypage-setobjects.md) chiama il `OnDisconnect` metodo.</span><span class="sxs-lookup"><span data-stu-id="821fc-111">The [**CBasePropertyPage::SetObjects**](cbasepropertypage-setobjects.md) method calls the `OnDisconnect` method.</span></span> <span data-ttu-id="821fc-112">Eseguire l'override `OnDisconnect` per rilasciare tutti i puntatori ottenuti nel metodo [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="821fc-112">Override `OnDisconnect` to release any pointers that were obtained in the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="821fc-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="821fc-113">Examples</span></span>


```C++
HRESULT CMyProp::OnDisconnect(void)
{
    if (m_pOwningFilter)
    {
        m_pOwningFilter->Release();
        m_pOwningFilter = NULL;
    }
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="821fc-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="821fc-114">Requirements</span></span>



| <span data-ttu-id="821fc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="821fc-115">Requirement</span></span> | <span data-ttu-id="821fc-116">Valore</span><span class="sxs-lookup"><span data-stu-id="821fc-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="821fc-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="821fc-117">Header</span></span><br/>  | <dl> <span data-ttu-id="821fc-118"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="821fc-118"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="821fc-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="821fc-119">Library</span></span><br/> | <dl> <span data-ttu-id="821fc-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="821fc-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="821fc-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="821fc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="821fc-122">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="821fc-122">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




