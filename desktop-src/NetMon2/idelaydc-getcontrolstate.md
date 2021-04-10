---
description: Il metodo GetControlState recupera lo stato dell'acquisizione, che indica se l'acquisizione viene eseguita o sospesa.
ms.assetid: 21b7faaa-591f-4e15-b4e9-453ea690ab4a
title: 'Metodo IDelaydC:: GetControlState (Netmon. h)'
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
ms.openlocfilehash: 8f5c3f084db788844f061ba2005d9c3ca38acef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966457"
---
# <a name="idelaydcgetcontrolstate-method"></a><span data-ttu-id="d02ae-103">Metodo IDelaydC:: GetControlState</span><span class="sxs-lookup"><span data-stu-id="d02ae-103">IDelaydC::GetControlState method</span></span>

<span data-ttu-id="d02ae-104">Il metodo **GetControlState** recupera lo stato dell' [*acquisizione*](c.md), che indica se l'acquisizione viene eseguita o sospesa.</span><span class="sxs-lookup"><span data-stu-id="d02ae-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="d02ae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d02ae-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="d02ae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d02ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d02ae-107">*IsRunnning* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d02ae-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d02ae-108">Indicatore dell'esecuzione dell'acquisizione corrente, incluso se l'acquisizione viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="d02ae-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="d02ae-109">Con *sospensione* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d02ae-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d02ae-110">Indicatore dell'acquisizione corrente sospesa.</span><span class="sxs-lookup"><span data-stu-id="d02ae-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d02ae-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d02ae-111">Return value</span></span>

<span data-ttu-id="d02ae-112">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d02ae-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d02ae-113">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="d02ae-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="d02ae-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d02ae-114">Return code</span></span>                                                                                          | <span data-ttu-id="d02ae-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d02ae-115">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d02ae-116"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="d02ae-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d02ae-117">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="d02ae-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="d02ae-118">Chiamare [IDelaydC:: Connect](idelaydc-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="d02ae-118">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="d02ae-119"><dt>**NMERR \_ non \_ ritardato**</dt></span><span class="sxs-lookup"><span data-stu-id="d02ae-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="d02ae-120">L'oggetto NPP è connesso alla rete, ma non con il metodo [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="d02ae-120">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="d02ae-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="d02ae-121">Remarks</span></span>

<span data-ttu-id="d02ae-122">Questo metodo può essere chiamato ogni volta che l'oggetto NPP è connesso alla rete tramite l'interfaccia [IDelaydC](idelaydc.md) .</span><span class="sxs-lookup"><span data-stu-id="d02ae-122">This method can be called any time the NPP is connected to the network by using the [IDelaydC](idelaydc.md) interface.</span></span> <span data-ttu-id="d02ae-123">È possibile utilizzare questo metodo per determinare se un'acquisizione è in esecuzione, se l'acquisizione viene sospesa o se l'acquisizione è stata arrestata, ma l'oggetto NPP non è disconnesso.</span><span class="sxs-lookup"><span data-stu-id="d02ae-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is not disconnected.</span></span>

<span data-ttu-id="d02ae-124">I metodi usati per avviare, sospendere e arrestare l'acquisizione sono elencati nell'elenco vedere anche di seguito.</span><span class="sxs-lookup"><span data-stu-id="d02ae-124">The methods used to start, pause, and, stop the capture are listed in the See Also list below.</span></span>

## <a name="requirements"></a><span data-ttu-id="d02ae-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d02ae-125">Requirements</span></span>



| <span data-ttu-id="d02ae-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d02ae-126">Requirement</span></span> | <span data-ttu-id="d02ae-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d02ae-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d02ae-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d02ae-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d02ae-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d02ae-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="d02ae-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d02ae-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d02ae-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d02ae-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="d02ae-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d02ae-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d02ae-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d02ae-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="d02ae-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d02ae-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d02ae-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d02ae-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d02ae-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d02ae-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d02ae-137">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="d02ae-137">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="d02ae-138">IDelaydC:: Connect</span><span class="sxs-lookup"><span data-stu-id="d02ae-138">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="d02ae-139">IDelaydC::P ause</span><span class="sxs-lookup"><span data-stu-id="d02ae-139">IDelaydC::Pause</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="d02ae-140">IDelaydC:: Start</span><span class="sxs-lookup"><span data-stu-id="d02ae-140">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="d02ae-141">IDelaydC:: Stop</span><span class="sxs-lookup"><span data-stu-id="d02ae-141">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




