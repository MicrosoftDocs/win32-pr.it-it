---
description: Il metodo SetControlWindowPin imposta il pin con cui eseguire la sincronizzazione.
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: Metodo CBaseControlWindow. SetControlWindowPin (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetControlWindowPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1aa3d4960799c2286e17709258ea90b76332bc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333363"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a><span data-ttu-id="7f5ec-103">CBaseControlWindow. SetControlWindowPin, metodo</span><span class="sxs-lookup"><span data-stu-id="7f5ec-103">CBaseControlWindow.SetControlWindowPin method</span></span>

<span data-ttu-id="7f5ec-104">Il `SetControlWindowPin` metodo imposta il pin con cui eseguire la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="7f5ec-104">The `SetControlWindowPin` method sets the pin with which to synchronize.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f5ec-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f5ec-105">Syntax</span></span>


```C++
void SetControlWindowPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="7f5ec-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f5ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f5ec-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="7f5ec-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="7f5ec-108">Puntatore al pin con il quale viene sincronizzata l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7f5ec-108">Pointer to the pin with which the interface is synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f5ec-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f5ec-109">Return value</span></span>

<span data-ttu-id="7f5ec-110">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="7f5ec-110">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f5ec-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f5ec-111">Remarks</span></span>

<span data-ttu-id="7f5ec-112">Questa funzione membro imposta la \_ variabile membro pPin m uguale al parametro pPin.</span><span class="sxs-lookup"><span data-stu-id="7f5ec-112">This member function sets the m\_pPin member variable equal to the pPin parameter.</span></span> <span data-ttu-id="7f5ec-113">Come descritto nel costruttore, l'interfaccia può essere chiamata solo quando il filtro è stato connesso correttamente.</span><span class="sxs-lookup"><span data-stu-id="7f5ec-113">As described in the constructor, the interface can be called only when the filter has been connected successfully.</span></span> <span data-ttu-id="7f5ec-114">L'oggetto viene passato tramite questa funzione membro al pin con il quale deve essere sincronizzato; nella maggior parte dei casi, determina se il PIN è connesso ogni volta che è presente un metodo di interfaccia denominato e restituisce VFW \_ e \_ non \_ connesso in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="7f5ec-114">The object is passed in through this member function to the pin with which it should synchronize; in most cases, it will determine if the pin is connected whenever it has an interface method called and will return VFW\_E\_NOT\_CONNECTED if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f5ec-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f5ec-115">Requirements</span></span>



| <span data-ttu-id="7f5ec-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f5ec-116">Requirement</span></span> | <span data-ttu-id="7f5ec-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7f5ec-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f5ec-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f5ec-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7f5ec-119"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f5ec-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7f5ec-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="7f5ec-120">Library</span></span><br/> | <dl> <span data-ttu-id="7f5ec-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7f5ec-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f5ec-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f5ec-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f5ec-123">**Classe CBaseControlWindow**</span><span class="sxs-lookup"><span data-stu-id="7f5ec-123">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




