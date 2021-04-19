---
description: Il metodo OnDeactivate viene chiamato quando la finestra di dialogo viene eliminata definitivamente.
ms.assetid: 47320e61-324f-4f64-abe1-38fe70e82787
title: Metodo CBasePropertyPage. OnDeactivate (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDeactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27191e4895c911d3d13a795306eee2b0ad6989ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333085"
---
# <a name="cbasepropertypageondeactivate-method"></a><span data-ttu-id="3c886-103">CBasePropertyPage. OnDeactivate, metodo</span><span class="sxs-lookup"><span data-stu-id="3c886-103">CBasePropertyPage.OnDeactivate method</span></span>

<span data-ttu-id="3c886-104">Il `OnDeactivate` metodo viene chiamato quando la finestra di dialogo viene eliminata definitivamente.</span><span class="sxs-lookup"><span data-stu-id="3c886-104">The `OnDeactivate` method is called when the dialog box window is destroyed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c886-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c886-105">Syntax</span></span>


```C++
virtual HRESULT OnDeactivate();
```



## <a name="parameters"></a><span data-ttu-id="3c886-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c886-106">Parameters</span></span>

<span data-ttu-id="3c886-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3c886-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3c886-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c886-108">Return value</span></span>

<span data-ttu-id="3c886-109">L'implementazione della classe di base restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3c886-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c886-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c886-110">Remarks</span></span>

<span data-ttu-id="3c886-111">Il metodo [**CBasePropertyPage::D ttiva**](cbasepropertypage-deactivate.md) chiama il `OnDeactivate` metodo.</span><span class="sxs-lookup"><span data-stu-id="3c886-111">The [**CBasePropertyPage::Deactivate**](cbasepropertypage-deactivate.md) method calls the `OnDeactivate` method.</span></span> <span data-ttu-id="3c886-112">Eseguire l'override `OnDeactivate` per rilasciare tutte le risorse ottenute dalla classe derivata nel metodo [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md) oppure per eseguire altre attività in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="3c886-112">Override `OnDeactivate` to release any resources that the derived class obtained in the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method, or to perform other tasks as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c886-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c886-113">Requirements</span></span>



| <span data-ttu-id="3c886-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c886-114">Requirement</span></span> | <span data-ttu-id="3c886-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3c886-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c886-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c886-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3c886-117"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c886-117"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="3c886-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="3c886-118">Library</span></span><br/> | <dl> <span data-ttu-id="3c886-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3c886-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c886-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c886-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c886-121">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="3c886-121">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




