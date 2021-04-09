---
description: Il metodo Start avvia l'acquisizione.
ms.assetid: 1f676e19-18ff-4c34-a83f-2723ff356be2
title: 'Metodo IRTC:: Start (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Start
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 3ee30112baf7813c983230fb90cd15ea7f52e2bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880709"
---
# <a name="irtcstart-method"></a><span data-ttu-id="108f9-103">Metodo IRTC:: Start</span><span class="sxs-lookup"><span data-stu-id="108f9-103">IRTC::Start method</span></span>

<span data-ttu-id="108f9-104">Il metodo **Start** avvia l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="108f9-104">The **Start** method starts the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="108f9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="108f9-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Start();
```



## <a name="parameters"></a><span data-ttu-id="108f9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="108f9-106">Parameters</span></span>

<span data-ttu-id="108f9-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="108f9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="108f9-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="108f9-108">Return value</span></span>

<span data-ttu-id="108f9-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="108f9-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="108f9-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="108f9-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="108f9-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="108f9-111">Return code</span></span>                                                                                           | <span data-ttu-id="108f9-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="108f9-112">Description</span></span>                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="108f9-113"><dt>**\_acquisizione NMERR \_ sospesa**</dt></span><span class="sxs-lookup"><span data-stu-id="108f9-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="108f9-114">L'acquisizione si trova in uno stato di sospensione e deve essere arrestata prima di poter essere riavviata.</span><span class="sxs-lookup"><span data-stu-id="108f9-114">The capture is in a paused state and must be stopped before it can be restarted.</span></span> <span data-ttu-id="108f9-115">Chiamare [IRTC:: Stop](idelaydc-stop.md) per arrestare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="108f9-115">Call [IRTC::Stop](idelaydc-stop.md) to stop the capture.</span></span><br/> |
| <dl> <span data-ttu-id="108f9-116"><dt>**\_acquisizione NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="108f9-116"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>       | <span data-ttu-id="108f9-117">Acquisizione già avviata.</span><span class="sxs-lookup"><span data-stu-id="108f9-117">The capture is already started.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="108f9-118"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="108f9-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="108f9-119">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="108f9-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="108f9-120">Chiamare [IRTC:: Connect](irtc-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="108f9-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/>                         |
| <dl> <span data-ttu-id="108f9-121"><dt>**NMERR \_ non in \_ tempo reale**</dt></span><span class="sxs-lookup"><span data-stu-id="108f9-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>   | <span data-ttu-id="108f9-122">L'oggetto NPP è connesso alla rete, ma non con il metodo [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="108f9-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="108f9-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="108f9-123">Remarks</span></span>

<span data-ttu-id="108f9-124">Quando si riavvia l'acquisizione usando i metodi IRTC:: Start e [IRTC:: Stop](irtc-stop.md) , è necessario chiamare il metodo [IRTC:: Configure](irtc-configure.md) per riconfigurare la connessione ogni volta che si chiama IRTC:: Start per riavviare l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="108f9-124">When you restart the capture by using the IRTC::Start and [IRTC::Stop](irtc-stop.md) methods, you must call the [IRTC::Configure](irtc-configure.md) method to reconfigure the connection each time you call IRTC::Start to restart the data capture.</span></span>

> [!Note]  
> <span data-ttu-id="108f9-125">È anche possibile avviare e arrestare l'acquisizione usando i metodi [IRTC::P ause](irtc-pause.md) e [IRTC:: Resume](irtc-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="108f9-125">You can also start and stop the capture by using the [IRTC::Pause](irtc-pause.md) and [IRTC::Resume](irtc-resume.md) methods.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="108f9-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="108f9-126">Requirements</span></span>



| <span data-ttu-id="108f9-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="108f9-127">Requirement</span></span> | <span data-ttu-id="108f9-128">Valore</span><span class="sxs-lookup"><span data-stu-id="108f9-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="108f9-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="108f9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="108f9-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="108f9-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="108f9-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="108f9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="108f9-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="108f9-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="108f9-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="108f9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="108f9-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="108f9-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="108f9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="108f9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="108f9-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="108f9-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="108f9-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="108f9-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="108f9-138">IRTC</span><span class="sxs-lookup"><span data-stu-id="108f9-138">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="108f9-139">IRTC:: Configure</span><span class="sxs-lookup"><span data-stu-id="108f9-139">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="108f9-140">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="108f9-140">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="108f9-141">IRTC::P ause</span><span class="sxs-lookup"><span data-stu-id="108f9-141">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="108f9-142">IRTC:: Resume</span><span class="sxs-lookup"><span data-stu-id="108f9-142">IRTC::Resume</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="108f9-143">IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="108f9-143">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




