---
title: Metodo IRemoteDesktopClientEvents OnNetworkStatusChanged
description: Chiamato quando lo stato della rete è stato modificato. | Metodo IRemoteDesktopClientEvents OnNetworkStatusChanged
ms.assetid: B68D1AA0-6403-40CA-95C5-BBBF39CEFFD8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnNetworkStatusChanged
- Metodo OnNetworkStatusChanged Servizi Desktop remoto, interfaccia IRemoteDesktopClientEvents
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto, metodo OnNetworkStatusChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnNetworkStatusChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de64d8b16ea9acf9defc976d4baa91afd64f8fa7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104530661"
---
# <a name="iremotedesktopclienteventsonnetworkstatuschanged-method"></a><span data-ttu-id="0e35d-107">Metodo IRemoteDesktopClientEvents:: OnNetworkStatusChanged</span><span class="sxs-lookup"><span data-stu-id="0e35d-107">IRemoteDesktopClientEvents::OnNetworkStatusChanged method</span></span>

<span data-ttu-id="0e35d-108">Chiamato quando lo stato della rete è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="0e35d-108">Called when the network status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e35d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e35d-109">Syntax</span></span>


```C++
void OnNetworkStatusChanged(
  [in] unsigned long qualityLevel,
  [in] long          bandwidth,
  [in] long          rtt
);
```



## <a name="parameters"></a><span data-ttu-id="0e35d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e35d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e35d-111">*qualityLevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e35d-111">*qualityLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e35d-112">Nuovo livello di qualità della connessione.</span><span class="sxs-lookup"><span data-stu-id="0e35d-112">The new quality level of the connection.</span></span> <span data-ttu-id="0e35d-113">Il livello di qualità è determinato dai valori della larghezza di banda e del tempo di round trip (RTT).</span><span class="sxs-lookup"><span data-stu-id="0e35d-113">The quality level is determined from the bandwidth and round-trip time (rtt) values.</span></span>

<span data-ttu-id="0e35d-114">Uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0e35d-114">One of the following values.</span></span>



| <span data-ttu-id="0e35d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0e35d-115">Value</span></span>                                                                        | <span data-ttu-id="0e35d-116">Significato</span><span class="sxs-lookup"><span data-stu-id="0e35d-116">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="0e35d-117"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0e35d-117"><dt>0</dt></span></span> </dl> | <span data-ttu-id="0e35d-118">Non è stato possibile determinare il livello di qualità.</span><span class="sxs-lookup"><span data-stu-id="0e35d-118">The quality level could not be determined.</span></span><br/>       |
| <dl> <span data-ttu-id="0e35d-119"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0e35d-119"><dt>1</dt></span></span> </dl> | <span data-ttu-id="0e35d-120">La qualità della connessione è scadente (una barra).</span><span class="sxs-lookup"><span data-stu-id="0e35d-120">The connection quality is poor (one bar).</span></span><br/>        |
| <dl> <span data-ttu-id="0e35d-121"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0e35d-121"><dt>2</dt></span></span> </dl> | <span data-ttu-id="0e35d-122">La qualità della connessione è equa (due barre).</span><span class="sxs-lookup"><span data-stu-id="0e35d-122">The connection quality is fair (two bars).</span></span><br/>       |
| <dl> <span data-ttu-id="0e35d-123"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0e35d-123"><dt>3</dt></span></span> </dl> | <span data-ttu-id="0e35d-124">La qualità della connessione è corretta (tre barre).</span><span class="sxs-lookup"><span data-stu-id="0e35d-124">The connection quality is good (three bars).</span></span><br/>     |
| <dl> <span data-ttu-id="0e35d-125"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0e35d-125"><dt>4</dt></span></span> </dl> | <span data-ttu-id="0e35d-126">La qualità della connessione è eccellente (quattro barre).</span><span class="sxs-lookup"><span data-stu-id="0e35d-126">The connection quality is excellent (four bars).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0e35d-127">*larghezza di banda* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e35d-127">*bandwidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e35d-128">Specifica la nuova larghezza di banda della connessione, in kilobit al secondo (Kbps).</span><span class="sxs-lookup"><span data-stu-id="0e35d-128">Specifies the new connection bandwidth, in kilobits per second (Kbps).</span></span>

</dd> <dt>

<span data-ttu-id="0e35d-129">*RTT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e35d-129">*rtt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e35d-130">Specifica il nuovo tempo di round trip della connessione (latenza), in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="0e35d-130">Specifies the new connection roundtrip time (latency), in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e35d-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e35d-131">Return value</span></span>

<span data-ttu-id="0e35d-132">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0e35d-132">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e35d-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e35d-133">Requirements</span></span>



| <span data-ttu-id="0e35d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e35d-134">Requirement</span></span> | <span data-ttu-id="0e35d-135">Valore</span><span class="sxs-lookup"><span data-stu-id="0e35d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e35d-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e35d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0e35d-137">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0e35d-137">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="0e35d-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e35d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0e35d-139">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0e35d-139">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="0e35d-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="0e35d-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="0e35d-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e35d-141"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="0e35d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0e35d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e35d-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e35d-143"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="0e35d-144">IID</span><span class="sxs-lookup"><span data-stu-id="0e35d-144">IID</span></span><br/>                      | <span data-ttu-id="0e35d-145">DIID \_ IRemoteDesktopClientEvents è definito come 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="0e35d-145">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0e35d-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e35d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e35d-147">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="0e35d-147">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





