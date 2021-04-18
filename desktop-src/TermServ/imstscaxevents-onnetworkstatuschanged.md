---
title: Metodo IMsTscAxEvents OnNetworkStatusChanged
description: Chiamato quando lo stato della rete è stato modificato. | Metodo IMsTscAxEvents OnNetworkStatusChanged
ms.assetid: 177A410E-2449-4FC7-8DE5-21F83A6DD028
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnNetworkStatusChanged
- Metodo OnNetworkStatusChanged Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnNetworkStatusChanged
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b9bdcd7774493fcc54e1390ad199a6a56a7c51
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321185"
---
# <a name="imstscaxeventsonnetworkstatuschanged-method"></a><span data-ttu-id="262d7-107">Metodo IMsTscAxEvents:: OnNetworkStatusChanged</span><span class="sxs-lookup"><span data-stu-id="262d7-107">IMsTscAxEvents::OnNetworkStatusChanged method</span></span>

<span data-ttu-id="262d7-108">Chiamato quando lo stato della rete è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="262d7-108">Called when the network status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="262d7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="262d7-109">Syntax</span></span>


```C++
void OnNetworkStatusChanged(
  [in] ULONG qualityLevel,
  [in] LONG  bandwidth,
  [in] LONG  rtt
);
```



## <a name="parameters"></a><span data-ttu-id="262d7-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="262d7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="262d7-111">*qualityLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="262d7-111">*qualityLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="262d7-112">Specifica la nuova velocità di connessione.</span><span class="sxs-lookup"><span data-stu-id="262d7-112">Specifies the new connection speed.</span></span> <span data-ttu-id="262d7-113">Si tratta di uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="262d7-113">This will be one of the following values.</span></span>

<dt>

<span data-ttu-id="262d7-114">1</span><span class="sxs-lookup"><span data-stu-id="262d7-114">1</span></span>
</dt> <dd>

<span data-ttu-id="262d7-115">Inferiore a 512 kilobyte al secondo (KBps).</span><span class="sxs-lookup"><span data-stu-id="262d7-115">Less than 512 kilobytes per second (KBps).</span></span>

</dd> <dt>

<span data-ttu-id="262d7-116">2</span><span class="sxs-lookup"><span data-stu-id="262d7-116">2</span></span>
</dt> <dd>

<span data-ttu-id="262d7-117">da 512 a 1.999 KBps.</span><span class="sxs-lookup"><span data-stu-id="262d7-117">512 to 1,999 KBps.</span></span>

</dd> <dt>

<span data-ttu-id="262d7-118">3</span><span class="sxs-lookup"><span data-stu-id="262d7-118">3</span></span>
</dt> <dd>

<span data-ttu-id="262d7-119">da 2.000 a 9.999 KBps.</span><span class="sxs-lookup"><span data-stu-id="262d7-119">2,000 to 9,999 KBps.</span></span>

</dd> <dt>

<span data-ttu-id="262d7-120">4</span><span class="sxs-lookup"><span data-stu-id="262d7-120">4</span></span>
</dt> <dd>

<span data-ttu-id="262d7-121">Maggiore o uguale a 10.000 KBps.</span><span class="sxs-lookup"><span data-stu-id="262d7-121">Greater than or equal to 10,000 KBps.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="262d7-122">*larghezza di banda* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="262d7-122">*bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="262d7-123">Specifica la larghezza di banda della connessione.</span><span class="sxs-lookup"><span data-stu-id="262d7-123">Specifies the connection bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="262d7-124">*RTT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="262d7-124">*rtt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="262d7-125">Specifica la latenza di connessione.</span><span class="sxs-lookup"><span data-stu-id="262d7-125">Specifies the connection latency.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="262d7-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="262d7-126">Return value</span></span>

<span data-ttu-id="262d7-127">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="262d7-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="262d7-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="262d7-128">Requirements</span></span>



| <span data-ttu-id="262d7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="262d7-129">Requirement</span></span> | <span data-ttu-id="262d7-130">Valore</span><span class="sxs-lookup"><span data-stu-id="262d7-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="262d7-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="262d7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="262d7-132">Windows 8</span><span class="sxs-lookup"><span data-stu-id="262d7-132">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="262d7-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="262d7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="262d7-134">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="262d7-134">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="262d7-135">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="262d7-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="262d7-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="262d7-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="262d7-137">DLL</span><span class="sxs-lookup"><span data-stu-id="262d7-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="262d7-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="262d7-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="262d7-139">IID</span><span class="sxs-lookup"><span data-stu-id="262d7-139">IID</span></span><br/>                      | <span data-ttu-id="262d7-140">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="262d7-140">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="262d7-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="262d7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="262d7-142">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="262d7-142">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





