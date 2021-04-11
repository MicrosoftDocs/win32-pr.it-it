---
title: Metodo BasicDevice.remove_ConnectionStatusChanged
description: Annulla la registrazione di un gestore eventi per l'evento ConnectionStatusChanged. | Metodo BasicDevice.remove_ConnectionStatusChanged
ms.assetid: 537CA8FE-D2E1-4CC7-BB80-FBE36A2D4A1E
keywords:
- API di streaming multimediale per il metodo remove_ConnectionStatusChanged
- API di streaming multimediale del metodo remove_ConnectionStatusChanged, interfaccia BasicDevice
- API di streaming multimediale dell'interfaccia BasicDevice, metodo remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- BasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdd39309774a61c4fd115ff09e16428101439a0b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234804"
---
# <a name="basicdeviceremove_connectionstatuschanged-method"></a><span data-ttu-id="6883f-107">BasicDevice. Remove, \_ Metodo ConnectionStatusChanged</span><span class="sxs-lookup"><span data-stu-id="6883f-107">BasicDevice.remove\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="6883f-108">Annulla la registrazione di un gestore eventi per l'evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="6883f-108">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="6883f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6883f-109">Syntax</span></span>


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a><span data-ttu-id="6883f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6883f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6883f-111">*token* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6883f-111">*token* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6883f-112">Riferimento a un token ottenuto dal metodo [**Add \_ ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) quando è stato registrato il gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="6883f-112">A reference to a token obtained from the [**add\_ConnectionStatusChanged**](basicdevice-add-connectionstatuschanged.md) method when the event handler was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6883f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6883f-113">Return value</span></span>

<span data-ttu-id="6883f-114">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="6883f-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6883f-115">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="6883f-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6883f-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6883f-116">Return code</span></span>                                                                          | <span data-ttu-id="6883f-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6883f-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6883f-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6883f-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6883f-119">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="6883f-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="6883f-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6883f-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="6883f-121">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6883f-121">[**BasicDevice**](/previous-versions/windows/desktop/legacy/hh828813(v=vs.85))</span></span>
</dt> </dl>

 

