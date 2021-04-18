---
description: Il metodo Resume riavvia un'acquisizione sospesa.
ms.assetid: 685dfdee-3bd0-44b3-ac4f-c9960cf77c5c
title: 'Metodo IRTC:: Resume (Netmon. h)'
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
ms.openlocfilehash: 991f70944b44ce13641318219788d9d6122b15c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310499"
---
# <a name="irtcresume-method"></a><span data-ttu-id="07746-103">Metodo IRTC:: Resume</span><span class="sxs-lookup"><span data-stu-id="07746-103">IRTC::Resume method</span></span>

<span data-ttu-id="07746-104">Il metodo **Resume** riavvia un'acquisizione sospesa.</span><span class="sxs-lookup"><span data-stu-id="07746-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="07746-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07746-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="07746-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="07746-106">Parameters</span></span>

<span data-ttu-id="07746-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="07746-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="07746-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07746-108">Return value</span></span>

<span data-ttu-id="07746-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="07746-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="07746-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="07746-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="07746-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="07746-111">Return code</span></span>                                                                                                | <span data-ttu-id="07746-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07746-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="07746-113"><dt>**\_acquisizione NMERR \_ non \_ sospesa**</dt></span><span class="sxs-lookup"><span data-stu-id="07746-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="07746-114">L'acquisizione non è sospesa.</span><span class="sxs-lookup"><span data-stu-id="07746-114">The capture is not paused.</span></span> <span data-ttu-id="07746-115">Chiamare [IRTC::P ause](irtc-pause.md) per sospendere l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="07746-115">Call [IRTC::Pause](irtc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="07746-116"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="07746-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="07746-117">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="07746-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="07746-118">Chiamare [IRTC:: Connect](irtc-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="07746-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="07746-119"><dt>**NMERR \_ non in \_ tempo reale**</dt></span><span class="sxs-lookup"><span data-stu-id="07746-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>        | <span data-ttu-id="07746-120">L'oggetto NPP è connesso alla rete, ma non con il metodo [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="07746-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="07746-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="07746-121">Remarks</span></span>

<span data-ttu-id="07746-122">Mentre l'acquisizione si trova in uno stato di sospensione, i nuovi dati non vengono acquisiti fino a quando una chiamata al metodo [IRTC:: Resume](idelaydc-resume.md) riavvia l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="07746-122">While the capture is in a paused state, new data is not captured until a call to the [IRTC::Resume](idelaydc-resume.md) method restarts the capture.</span></span>

<span data-ttu-id="07746-123">Quando si utilizzano i metodi di **sospensione** e **ripresa** per controllare l'acquisizione, Network Monitor continua ad aggiungere [*statistiche di conversazione*](c.md) alle statistiche esistenti per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="07746-123">When using the **Pause** and **Resume** methods to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="07746-124">Per arrestare l'acquisizione, chiamare il metodo [IRTC:: Stop](irtc-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="07746-124">To stop the capture, call the [IRTC::Stop](irtc-stop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="07746-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07746-125">Requirements</span></span>



| <span data-ttu-id="07746-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="07746-126">Requirement</span></span> | <span data-ttu-id="07746-127">Valore</span><span class="sxs-lookup"><span data-stu-id="07746-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07746-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07746-128">Minimum supported client</span></span><br/> | <span data-ttu-id="07746-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="07746-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="07746-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07746-130">Minimum supported server</span></span><br/> | <span data-ttu-id="07746-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="07746-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="07746-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07746-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="07746-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="07746-133"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="07746-134">DLL</span><span class="sxs-lookup"><span data-stu-id="07746-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07746-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07746-135"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07746-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07746-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07746-137">IRTC</span><span class="sxs-lookup"><span data-stu-id="07746-137">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="07746-138">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="07746-138">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="07746-139">IRTC::P ause</span><span class="sxs-lookup"><span data-stu-id="07746-139">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="07746-140">IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="07746-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




