---
description: "Metodo IRTC::GetControlState: il metodo GetControlState recupera lo stato dell'acquisizione, che indica se l'acquisizione è in esecuzione o sospesa."
ms.assetid: ae0cf869-bf5b-4c23-a924-014554053c92
title: Metodo IRTC::GetControlState (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d2e41ad3e4119fffbada26fe3ebebdfe3bf82043
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110709"
---
# <a name="irtcgetcontrolstate-method"></a><span data-ttu-id="d51ca-103">Metodo IRTC::GetControlState</span><span class="sxs-lookup"><span data-stu-id="d51ca-103">IRTC::GetControlState method</span></span>

<span data-ttu-id="d51ca-104">Il **metodo GetControlState** recupera lo stato dell'acquisizione , che indica se l'acquisizione è in esecuzione o sospesa. [](c.md)</span><span class="sxs-lookup"><span data-stu-id="d51ca-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="d51ca-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d51ca-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="d51ca-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d51ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d51ca-107">*IsRunnning* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="d51ca-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d51ca-108">Indicatore che l'acquisizione corrente è in esecuzione, anche se l'acquisizione è sospesa.</span><span class="sxs-lookup"><span data-stu-id="d51ca-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="d51ca-109">*IsPaused* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="d51ca-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d51ca-110">Indicatore che l'acquisizione corrente è sospesa.</span><span class="sxs-lookup"><span data-stu-id="d51ca-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d51ca-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d51ca-111">Return value</span></span>

<span data-ttu-id="d51ca-112">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="d51ca-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d51ca-113">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="d51ca-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="d51ca-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d51ca-114">Return code</span></span>                                                                                          | <span data-ttu-id="d51ca-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d51ca-115">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d51ca-116"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="d51ca-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d51ca-117">NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="d51ca-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="d51ca-118">Chiamare [IRTC::Connect](irtc-connect.md) per connettere NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="d51ca-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="d51ca-119"><dt>**NMERR \_ NON IN TEMPO \_ REALE**</dt></span><span class="sxs-lookup"><span data-stu-id="d51ca-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="d51ca-120">NPP è connesso alla rete, ma non con il [metodo IRTC::Connect.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="d51ca-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="d51ca-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="d51ca-121">Remarks</span></span>

<span data-ttu-id="d51ca-122">Questo metodo può essere chiamato ogni volta che il NPP è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="d51ca-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="d51ca-123">È possibile usare questo metodo per determinare se un'acquisizione è in esecuzione, se l'acquisizione è sospesa o se l'acquisizione è stata arrestata ma NPP è ancora connesso.</span><span class="sxs-lookup"><span data-stu-id="d51ca-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="d51ca-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d51ca-124">Requirements</span></span>



| <span data-ttu-id="d51ca-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d51ca-125">Requirement</span></span> | <span data-ttu-id="d51ca-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d51ca-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d51ca-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d51ca-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d51ca-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d51ca-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="d51ca-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d51ca-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d51ca-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d51ca-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="d51ca-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d51ca-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d51ca-132"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="d51ca-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="d51ca-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d51ca-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d51ca-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d51ca-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d51ca-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d51ca-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d51ca-136">IRTC</span><span class="sxs-lookup"><span data-stu-id="d51ca-136">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="d51ca-137">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="d51ca-137">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="d51ca-138">IRTC::P ause</span><span class="sxs-lookup"><span data-stu-id="d51ca-138">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="d51ca-139">IRTC::Start</span><span class="sxs-lookup"><span data-stu-id="d51ca-139">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="d51ca-140">IRTC::Stop</span><span class="sxs-lookup"><span data-stu-id="d51ca-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




