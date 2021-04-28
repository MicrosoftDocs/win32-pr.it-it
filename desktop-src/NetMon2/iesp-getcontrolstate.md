---
description: "Metodo IESP::GetControlState: il metodo GetControlState recupera lo stato dell'acquisizione, che indica se l'acquisizione è in esecuzione o sospesa."
ms.assetid: 19cc3095-3aa3-4482-95f5-959b19f76cea
title: Metodo IESP::GetControlState (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b007eb6824ee3e65cdf8195914bbff3a50c39b2c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114679"
---
# <a name="iespgetcontrolstate-method"></a><span data-ttu-id="0546b-103">Metodo IESP::GetControlState</span><span class="sxs-lookup"><span data-stu-id="0546b-103">IESP::GetControlState method</span></span>

<span data-ttu-id="0546b-104">Il **metodo GetControlState** recupera lo stato dell'acquisizione , che indica se l'acquisizione è in esecuzione o sospesa. [](c.md)</span><span class="sxs-lookup"><span data-stu-id="0546b-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="0546b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0546b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="0546b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0546b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0546b-107">*IsRunnning* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="0546b-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0546b-108">Indicatore che l'acquisizione corrente è in esecuzione, anche se l'acquisizione è sospesa.</span><span class="sxs-lookup"><span data-stu-id="0546b-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="0546b-109">*IsPaused* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="0546b-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0546b-110">Indicatore che l'acquisizione corrente è sospesa.</span><span class="sxs-lookup"><span data-stu-id="0546b-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0546b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0546b-111">Return value</span></span>

<span data-ttu-id="0546b-112">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="0546b-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0546b-113">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="0546b-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="0546b-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0546b-114">Return code</span></span>                                                                                          | <span data-ttu-id="0546b-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0546b-115">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0546b-116"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="0546b-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="0546b-117">NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="0546b-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="0546b-118">Chiamare [IESP::Connect](iesp-connect.md) per connettere NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="0546b-118">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="0546b-119"><dt>**NMERR \_ NON \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="0546b-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="0546b-120">NPP è connesso alla rete, ma non con il [metodo IESP::Connect.](iesp-connect.md)</span><span class="sxs-lookup"><span data-stu-id="0546b-120">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="0546b-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="0546b-121">Remarks</span></span>

<span data-ttu-id="0546b-122">Questo metodo può essere chiamato ogni volta che il NPP è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="0546b-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="0546b-123">È possibile usare questo metodo per determinare se un'acquisizione è in esecuzione, se l'acquisizione è sospesa o se l'acquisizione è stata arrestata ma il servizio NPP è ancora connesso.</span><span class="sxs-lookup"><span data-stu-id="0546b-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="0546b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0546b-124">Requirements</span></span>



| <span data-ttu-id="0546b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0546b-125">Requirement</span></span> | <span data-ttu-id="0546b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0546b-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0546b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0546b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0546b-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0546b-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0546b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0546b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0546b-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0546b-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0546b-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0546b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0546b-132"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="0546b-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0546b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0546b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0546b-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0546b-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0546b-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0546b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0546b-136">IESP</span><span class="sxs-lookup"><span data-stu-id="0546b-136">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="0546b-137">IESP::Connect</span><span class="sxs-lookup"><span data-stu-id="0546b-137">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="0546b-138">IESP::P ause</span><span class="sxs-lookup"><span data-stu-id="0546b-138">IESP::Pause</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="0546b-139">IESP::Start</span><span class="sxs-lookup"><span data-stu-id="0546b-139">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="0546b-140">IESP::Stop</span><span class="sxs-lookup"><span data-stu-id="0546b-140">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




