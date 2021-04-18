---
title: Metodo remove_ConnectionStatusChanged IBasicDevice
description: Annulla la registrazione di un gestore eventi per l'evento ConnectionStatusChanged. | Metodo remove_ConnectionStatusChanged IBasicDevice
ms.assetid: 577D9C50-486D-441A-A9FE-AF79D1FC2B52
keywords:
- API di streaming multimediale per il metodo remove_ConnectionStatusChanged
- API di streaming multimediale del metodo remove_ConnectionStatusChanged, interfaccia IBasicDevice
- API di streaming multimediale dell'interfaccia IBasicDevice, metodo remove_ConnectionStatusChanged
topic_type:
- apiref
api_name:
- IBasicDevice.remove_ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c2bfa2886774ad637e66385a057c9d4e21efe0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321557"
---
# <a name="ibasicdeviceremove_connectionstatuschanged-method"></a><span data-ttu-id="0314a-107">Metodo IBasicDevice:: Remove \_ ConnectionStatusChanged</span><span class="sxs-lookup"><span data-stu-id="0314a-107">IBasicDevice::remove\_ConnectionStatusChanged method</span></span>

<span data-ttu-id="0314a-108">Annulla la registrazione di un gestore eventi per l'evento [**ConnectionStatusChanged**](connectionstatuschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="0314a-108">Unregisters an event handler for the [**ConnectionStatusChanged**](connectionstatuschanged.md) event.</span></span>

## <a name="syntax"></a><span data-ttu-id="0314a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0314a-109">Syntax</span></span>


```C++
HRESULT remove_ConnectionStatusChanged(
  [in] EventRegistrationToken *token
);
```



## <a name="parameters"></a><span data-ttu-id="0314a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0314a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0314a-111">*token* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0314a-111">*token* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0314a-112">Riferimento a un token ottenuto dal metodo [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) quando è stato registrato il gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="0314a-112">A reference to a token obtained from the [**add\_ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) method when the event handler was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0314a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0314a-113">Return value</span></span>

<span data-ttu-id="0314a-114">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0314a-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0314a-115">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0314a-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0314a-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0314a-116">Return code</span></span>                                                                          | <span data-ttu-id="0314a-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0314a-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0314a-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0314a-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0314a-119">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="0314a-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="0314a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0314a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0314a-121">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="0314a-121">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





