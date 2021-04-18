---
title: Metodo GetStatus di IWMDRMIndividualizationStatus (wmdrmsdk. h)
description: Il metodo GetStatus recupera informazioni dettagliate sullo stato di individualizzazione.
ms.assetid: 8985f3cc-006d-4fd5-b218-d3af3473b8e3
keywords:
- Metodo GetStatus formato Windows Media
- Metodo GetStatus formato Windows Media, interfaccia IWMDRMIndividualizationStatus
- Interfaccia IWMDRMIndividualizationStatus-formato Windows Media, metodo GetStatus
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus.GetStatus
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f144f188de46d17702dd22aa12e2245156b59a21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328534"
---
# <a name="iwmdrmindividualizationstatusgetstatus-method"></a><span data-ttu-id="b13de-106">Metodo IWMDRMIndividualizationStatus:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="b13de-106">IWMDRMIndividualizationStatus::GetStatus method</span></span>

<span data-ttu-id="b13de-107">Il metodo **GetStatus** recupera informazioni dettagliate sullo stato di individualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b13de-107">The **GetStatus** method retrieves detailed information about individualization progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="b13de-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b13de-108">Syntax</span></span>


```C++
HRESULT GetStatus(
  [out] WM_INDIVIDUALIZE_STATUS *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="b13de-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b13de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b13de-110">*pStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b13de-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b13de-111">Riceve una struttura di [**\_ \_ stato**](drmwm-individualize-status.md) del sistema di personalizzazione WM che contiene informazioni dettagliate sullo stato del tentativo di individualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b13de-111">Receives a [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure containing detailed information about the status of the individualization attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b13de-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b13de-112">Return value</span></span>

<span data-ttu-id="b13de-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b13de-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b13de-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="b13de-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b13de-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b13de-115">Return code</span></span>                                                                          | <span data-ttu-id="b13de-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b13de-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b13de-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b13de-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b13de-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="b13de-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b13de-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="b13de-119">Remarks</span></span>

<span data-ttu-id="b13de-120">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="b13de-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="b13de-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b13de-121">Requirements</span></span>



| <span data-ttu-id="b13de-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b13de-122">Requirement</span></span> | <span data-ttu-id="b13de-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b13de-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b13de-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b13de-124">Header</span></span><br/> | <dl> <span data-ttu-id="b13de-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="b13de-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b13de-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b13de-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b13de-127">**Interfaccia IWMDRMIndividualizationStatus**</span><span class="sxs-lookup"><span data-stu-id="b13de-127">**IWMDRMIndividualizationStatus Interface**</span></span>](iwmdrmindividualizationstatus.md)
</dt> </dl>

 

 





