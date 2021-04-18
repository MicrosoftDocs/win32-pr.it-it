---
title: Metodo BasicDevice.add_ConnectionStatusChanged
description: Registra un gestore eventi per l'evento ConnectionStatusChanged. | Metodo BasicDevice.add_ConnectionStatusChanged
ms.assetid: FFAA0981-508C-4300-9CA9-24C6AFC1183D
keywords:
- API di streaming multimediale per il metodo add_ConnectionStatusChanged
- API di streaming multimediale del metodo add_ConnectionStatusChanged, interfaccia BasicDevice
- API di streaming multimediale dell'interfaccia BasicDevice, metodo add_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.add_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61a36e46d554a953ecd061ccf2396d33b0578d8f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321258"
---
# <a name="basicdeviceadd_connectionstatuschanged-method"></a><span data-ttu-id="a80d6-107">BasicDevice. Add, \_ Metodo ConnectionStatusChanged</span><span class="sxs-lookup"><span data-stu-id="a80d6-107">BasicDevice.add\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="a80d6-108">Registra un gestore eventi per l'evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="a80d6-108">Registers an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="a80d6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a80d6-109">Syntax</span></span>


```C++
HRESULT add_ConnectionStatusChanged(
  [in]          ConnectionStatusHandler *handler,
  [out, retval] EventRegistrationToken  *token
);
```



## <a name="parameters"></a><span data-ttu-id="a80d6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a80d6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a80d6-111">*gestore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a80d6-111">*handler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a80d6-112">Funzione del gestore eventi [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a80d6-112">A [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) event handler function.</span></span>

</dd> <dt>

<span data-ttu-id="a80d6-113">*token* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="a80d6-113">*token* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a80d6-114">Riferimento a un token che può essere utilizzato per annullare la registrazione del gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="a80d6-114">Reference to a token that can be used to unregister the event handler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a80d6-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a80d6-115">Return value</span></span>

<span data-ttu-id="a80d6-116">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a80d6-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a80d6-117">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a80d6-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a80d6-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a80d6-118">Return code</span></span>                                                                          | <span data-ttu-id="a80d6-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a80d6-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a80d6-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a80d6-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a80d6-121">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="a80d6-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a80d6-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="a80d6-122">Remarks</span></span>

<span data-ttu-id="a80d6-123">Per annullare la registrazione del gestore eventi registrato da questo metodo, passare il valore del *token* al metodo [**Remove \_ ConnectionStatusChanged**](basicdevice-remove-connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="a80d6-123">To unregister the event handler that was registered by this method, pass the *token* value to the [**remove\_ConnectionStatusChanged**](basicdevice-remove-connectionstatuschanged.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="a80d6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a80d6-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="a80d6-125">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a80d6-125">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

