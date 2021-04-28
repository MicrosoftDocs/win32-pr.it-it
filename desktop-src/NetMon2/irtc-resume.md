---
description: "Metodo IRTC::Resume: il metodo Resume riavvia un'acquisizione sospesa."
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: Metodo IRTC::Resume (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 55e5cb66eecbee96df9573e9347d1f32e3508d2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110564"
---
# <a name="irtcresume-method"></a><span data-ttu-id="7dd14-103">Metodo IRTC::Resume</span><span class="sxs-lookup"><span data-stu-id="7dd14-103">IRTC::Resume method</span></span>

<span data-ttu-id="7dd14-104">Il **metodo Resume** riavvia un'acquisizione sospesa.</span><span class="sxs-lookup"><span data-stu-id="7dd14-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dd14-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7dd14-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="7dd14-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7dd14-106">Parameters</span></span>

<span data-ttu-id="7dd14-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7dd14-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7dd14-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7dd14-108">Return value</span></span>

<span data-ttu-id="7dd14-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="7dd14-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="7dd14-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="7dd14-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="7dd14-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7dd14-111">Return code</span></span>                                                                                                | <span data-ttu-id="7dd14-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7dd14-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7dd14-113"><dt>**ACQUISIZIONE NMERR \_ \_ NON \_ SOSPESA**</dt></span><span class="sxs-lookup"><span data-stu-id="7dd14-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="7dd14-114">L'acquisizione non viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="7dd14-114">The capture is not paused.</span></span> <span data-ttu-id="7dd14-115">Chiamare [IRTC::P ause](irtc-pause.md) per sospendere l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="7dd14-115">Call [IRTC::Pause](irtc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="7dd14-116"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="7dd14-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="7dd14-117">NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="7dd14-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="7dd14-118">Chiamare [IRTC::Connect](irtc-connect.md) per connettere NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="7dd14-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="7dd14-119"><dt>**NMERR \_ NON IN TEMPO \_ REALE**</dt></span><span class="sxs-lookup"><span data-stu-id="7dd14-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>        | <span data-ttu-id="7dd14-120">NPP è connesso alla rete, ma non con il [metodo IRTC::Connect.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="7dd14-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="7dd14-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="7dd14-121">Remarks</span></span>

<span data-ttu-id="7dd14-122">Mentre l'acquisizione è in stato di sospensione, i nuovi dati non vengono acquisiti fino a quando una chiamata al metodo [IRTC::Resume](idelaydc-resume.md) non riavvia l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="7dd14-122">While the capture is in a paused state, new data is not captured until a call to the [IRTC::Resume](idelaydc-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="7dd14-123">Quando si usano **i metodi Pause** e **Resume** per controllare [](c.md) l'acquisizione, Network Monitor continua ad aggiungere statistiche di conversazione alle statistiche esistenti per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="7dd14-123">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="7dd14-124">Per arrestare l'acquisizione, chiamare il [metodo IRTC::Stop.](irtc-stop.md)</span><span class="sxs-lookup"><span data-stu-id="7dd14-124">To stop the capture, call the [IRTC::Stop](irtc-stop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dd14-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7dd14-125">Requirements</span></span>



| <span data-ttu-id="7dd14-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dd14-126">Requirement</span></span> | <span data-ttu-id="7dd14-127">Valore</span><span class="sxs-lookup"><span data-stu-id="7dd14-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd14-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dd14-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7dd14-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7dd14-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="7dd14-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dd14-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7dd14-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7dd14-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="7dd14-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7dd14-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dd14-133"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="7dd14-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="7dd14-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7dd14-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7dd14-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dd14-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dd14-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7dd14-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dd14-137">IRTC</span><span class="sxs-lookup"><span data-stu-id="7dd14-137">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="7dd14-138">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="7dd14-138">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="7dd14-139">IRTC::P ause</span><span class="sxs-lookup"><span data-stu-id="7dd14-139">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="7dd14-140">IRTC::Stop</span><span class="sxs-lookup"><span data-stu-id="7dd14-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




