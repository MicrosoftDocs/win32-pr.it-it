---
description: "Metodo IDelaydC::GetControlState: il metodo GetControlState recupera lo stato dell'acquisizione, che indica se l'acquisizione è in esecuzione o sospesa."
ms.assetid: 21b7faaa-591f-4e15-b4e9-453ea690ab4a
title: Metodo IDelaydC::GetControlState (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 825112ec9a33ef176d5a69765837214249e33102
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110769"
---
# <a name="idelaydcgetcontrolstate-method"></a><span data-ttu-id="3fc6e-103">Metodo IDelaydC::GetControlState</span><span class="sxs-lookup"><span data-stu-id="3fc6e-103">IDelaydC::GetControlState method</span></span>

<span data-ttu-id="3fc6e-104">Il **metodo GetControlState** recupera lo stato dell'acquisizione , che indica se l'acquisizione è in esecuzione o sospesa. [](c.md)</span><span class="sxs-lookup"><span data-stu-id="3fc6e-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fc6e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3fc6e-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="3fc6e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3fc6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fc6e-107">*IsRunnning* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="3fc6e-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fc6e-108">Indicatore che l'acquisizione corrente è in esecuzione, incluso se l'acquisizione è sospesa.</span><span class="sxs-lookup"><span data-stu-id="3fc6e-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="3fc6e-109">*IsPaused* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="3fc6e-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3fc6e-110">Indicatore che l'acquisizione corrente è sospesa.</span><span class="sxs-lookup"><span data-stu-id="3fc6e-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fc6e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3fc6e-111">Return value</span></span>

<span data-ttu-id="3fc6e-112">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="3fc6e-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3fc6e-113">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="3fc6e-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="3fc6e-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3fc6e-114">Return code</span></span>                                                                                          | <span data-ttu-id="3fc6e-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fc6e-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3fc6e-116"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="3fc6e-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="3fc6e-117">Il NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="3fc6e-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="3fc6e-118">Chiamare [IDelaydC::Connect](idelaydc-connect.md) per connettere il NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="3fc6e-118">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="3fc6e-119"><dt>**NMERR \_ NON \_ RITARDATO**</dt></span><span class="sxs-lookup"><span data-stu-id="3fc6e-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="3fc6e-120">Il NPP è connesso alla rete, ma non con il [metodo IDelaydC::Connect.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="3fc6e-120">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="3fc6e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fc6e-121">Remarks</span></span>

<span data-ttu-id="3fc6e-122">Questo metodo può essere chiamato ogni volta che il NPP è connesso alla rete usando [l'interfaccia IDelaydC.](idelaydc.md)</span><span class="sxs-lookup"><span data-stu-id="3fc6e-122">This method can be called any time the NPP is connected to the network by using the [IDelaydC](idelaydc.md) interface.</span></span> <span data-ttu-id="3fc6e-123">È possibile usare questo metodo per scoprire se un'acquisizione è in esecuzione, se l'acquisizione è sospesa o se l'acquisizione è stata arrestata ma il NPP non è disconnesso.</span><span class="sxs-lookup"><span data-stu-id="3fc6e-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

<span data-ttu-id="3fc6e-124">I metodi usati per avviare, sospendere e arrestare l'acquisizione sono elencati nell'elenco Vedere anche riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="3fc6e-124">The methods used to start, pause, and, stop the capture are listed in the See Also list below.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fc6e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fc6e-125">Requirements</span></span>



| <span data-ttu-id="3fc6e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fc6e-126">Requirement</span></span> | <span data-ttu-id="3fc6e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3fc6e-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fc6e-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fc6e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3fc6e-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3fc6e-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="3fc6e-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fc6e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3fc6e-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3fc6e-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="3fc6e-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fc6e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fc6e-133"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="3fc6e-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="3fc6e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="3fc6e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fc6e-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fc6e-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fc6e-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fc6e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fc6e-137">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="3fc6e-137">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="3fc6e-138">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="3fc6e-138">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="3fc6e-139">IDelaydC::P ause</span><span class="sxs-lookup"><span data-stu-id="3fc6e-139">IDelaydC::Pause</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="3fc6e-140">IDelaydC::Start</span><span class="sxs-lookup"><span data-stu-id="3fc6e-140">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="3fc6e-141">IDelaydC::Stop</span><span class="sxs-lookup"><span data-stu-id="3fc6e-141">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




