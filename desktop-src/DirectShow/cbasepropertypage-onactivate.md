---
description: Il metodo OnActivate viene chiamato quando la pagina delle proprietà viene attivata.
ms.assetid: aff843d4-cfb2-4255-a59c-0579f1cd24bd
title: Metodo CBasePropertyPage. OnActivate (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnActivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5093cb2ac71e8010bc689e4517b3d8bb758c8436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329411"
---
# <a name="cbasepropertypageonactivate-method"></a><span data-ttu-id="59319-103">Metodo CBasePropertyPage. OnActivate</span><span class="sxs-lookup"><span data-stu-id="59319-103">CBasePropertyPage.OnActivate method</span></span>

<span data-ttu-id="59319-104">Il `OnActivate` metodo viene chiamato quando la pagina delle proprietà viene attivata.</span><span class="sxs-lookup"><span data-stu-id="59319-104">The `OnActivate` method is called when the property page is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="59319-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59319-105">Syntax</span></span>


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a><span data-ttu-id="59319-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="59319-106">Parameters</span></span>

<span data-ttu-id="59319-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="59319-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59319-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59319-108">Return value</span></span>

<span data-ttu-id="59319-109">L'implementazione della classe di base restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="59319-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="59319-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="59319-110">Remarks</span></span>

<span data-ttu-id="59319-111">Il metodo [**CBasePropertyPage:: Activate**](cbasepropertypage-activate.md) chiama il `OnActivate` metodo.</span><span class="sxs-lookup"><span data-stu-id="59319-111">The [**CBasePropertyPage::Activate**](cbasepropertypage-activate.md) method calls the `OnActivate` method.</span></span> <span data-ttu-id="59319-112">Nella classe derivata eseguire l'override `OnActivate` di per inizializzare la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="59319-112">In your derived class, override `OnActivate` to initialize the dialog box.</span></span>

## <a name="examples"></a><span data-ttu-id="59319-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="59319-113">Examples</span></span>

<span data-ttu-id="59319-114">Nell'esempio seguente viene inizializzato un controllo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="59319-114">The following example initializes a trackbar control.</span></span> <span data-ttu-id="59319-115">Questo esempio si basa sul presupposto che **m \_ pOwningFilter** sia un puntatore a un'interfaccia personalizzata nel filtro associato alla pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="59319-115">This example assumes that **m\_pOwningFilter** is a pointer to a custom interface on the filter associated with the property page.</span></span> <span data-ttu-id="59319-116">Usare il metodo [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) per inizializzare tali puntatori.</span><span class="sxs-lookup"><span data-stu-id="59319-116">(Use the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to initialize such pointers.)</span></span>


```C++
HRESULT CMyProp::OnActivate(void)
{
    ASSERT(m_pOwningFilter != NULL);
    m_pOwningFilter->GetSomeProperty(&m_lOldVal);
    
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0, MAKELONG(0, 100));
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 10, 0);
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lOldVal);
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="59319-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59319-117">Requirements</span></span>



| <span data-ttu-id="59319-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="59319-118">Requirement</span></span> | <span data-ttu-id="59319-119">Valore</span><span class="sxs-lookup"><span data-stu-id="59319-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59319-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59319-120">Header</span></span><br/>  | <dl> <span data-ttu-id="59319-121"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59319-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="59319-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="59319-122">Library</span></span><br/> | <dl> <span data-ttu-id="59319-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="59319-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59319-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59319-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59319-125">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="59319-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




