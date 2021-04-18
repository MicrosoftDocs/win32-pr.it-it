---
title: Metodo add_ConnectionStatusChanged IBasicDevice
description: Registra un gestore eventi per l'evento ConnectionStatusChanged. | Metodo add_ConnectionStatusChanged IBasicDevice
ms.assetid: 1A4CCEFE-B6B6-4AFD-9296-EE923B9EF399
keywords:
- API di streaming multimediale per il metodo add_ConnectionStatusChanged
- API di streaming multimediale del metodo add_ConnectionStatusChanged, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo add_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0028e6f3dad1670974178b0f07a59f74dffdc06f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321763"
---
# <a name="ibasicdeviceadd_connectionstatuschanged-method"></a><span data-ttu-id="df6a1-107">Metodo IBasicDevice:: Add \_ ConnectionStatusChanged</span><span class="sxs-lookup"><span data-stu-id="df6a1-107">IBasicDevice::add\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="df6a1-108">Registra un gestore eventi per l'evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="df6a1-108">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="df6a1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df6a1-109">Syntax</span></span>


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a><span data-ttu-id="df6a1-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="df6a1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df6a1-111">*gestore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="df6a1-111">*handler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df6a1-112">Funzione del gestore eventi [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="df6a1-112">A [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function.</span></span>

</dd> <dt>

<span data-ttu-id="df6a1-113">*token* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="df6a1-113">*token* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="df6a1-114">Riferimento a un token che può essere utilizzato per annullare la registrazione del gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="df6a1-114">Reference to a token that can be used to unregister the event handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df6a1-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="df6a1-115">Return value</span></span>

<span data-ttu-id="df6a1-116">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="df6a1-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="df6a1-117">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="df6a1-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="df6a1-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="df6a1-118">Return code</span></span>                                                                          | <span data-ttu-id="df6a1-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df6a1-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="df6a1-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="df6a1-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="df6a1-121">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="df6a1-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="df6a1-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="df6a1-122">Remarks</span></span>

<span data-ttu-id="df6a1-123">Per annullare la registrazione del gestore eventi registrato da questo metodo, passare il valore del *token* al metodo [**Remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="df6a1-123">To unregister the event handler that was registered by this method, pass the *token* value to the [**remove\_ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="df6a1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df6a1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df6a1-125">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="df6a1-125">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

