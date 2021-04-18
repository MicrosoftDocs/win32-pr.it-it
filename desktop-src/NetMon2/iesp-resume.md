---
description: Il metodo Resume riavvia un'acquisizione sospesa.
ms.assetid: 047ea5f8-de3d-40db-ada3-fc0ef4deccef
title: 'Metodo IESP:: Resume (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 01bbb748fc91bcc5a78b281ec9ebdd2a6d479888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305873"
---
# <a name="iespresume-method"></a><span data-ttu-id="62f8e-103">Metodo IESP:: Resume</span><span class="sxs-lookup"><span data-stu-id="62f8e-103">IESP::Resume method</span></span>

<span data-ttu-id="62f8e-104">Il metodo **Resume** riavvia un'acquisizione sospesa.</span><span class="sxs-lookup"><span data-stu-id="62f8e-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="62f8e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62f8e-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="62f8e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="62f8e-106">Parameters</span></span>

<span data-ttu-id="62f8e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="62f8e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="62f8e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62f8e-108">Return value</span></span>

<span data-ttu-id="62f8e-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="62f8e-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="62f8e-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="62f8e-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="62f8e-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="62f8e-111">Return code</span></span>                                                                                                | <span data-ttu-id="62f8e-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62f8e-112">Description</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="62f8e-113"><dt>**\_acquisizione NMERR \_ non \_ sospesa**</dt></span><span class="sxs-lookup"><span data-stu-id="62f8e-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="62f8e-114">L'acquisizione non è sospesa.</span><span class="sxs-lookup"><span data-stu-id="62f8e-114">The capture is not paused.</span></span> <span data-ttu-id="62f8e-115">Chiamare [**IESP::P ause**](iesp-pause.md) per sospendere l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="62f8e-115">Call [**IESP::Pause**](iesp-pause.md) to pause the capture.</span></span><br/>                        |
| <dl> <span data-ttu-id="62f8e-116"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="62f8e-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="62f8e-117">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="62f8e-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="62f8e-118">Chiamare [**IESP:: Connect**](iesp-connect.md) per connettersi alla rete.</span><span class="sxs-lookup"><span data-stu-id="62f8e-118">Call [**IESP::Connect**](iesp-connect.md) to connect to the network.</span></span><br/> |
| <dl> <span data-ttu-id="62f8e-119"><dt>**NMERR \_ non \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="62f8e-119"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>             | <span data-ttu-id="62f8e-120">L'oggetto NPP è connesso alla rete, ma non con il metodo [**IESP:: Connect**](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="62f8e-120">The NPP is connected to the network, but not with the [**IESP::Connect**](iesp-connect.md) method.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="62f8e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="62f8e-121">Remarks</span></span>

<span data-ttu-id="62f8e-122">Mentre l'acquisizione si trova in uno stato di sospensione, i nuovi dati non vengono aggiunti al [*file di acquisizione*](c.md) corrente fino a quando non viene chiamato **IESP:: Resume** per riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="62f8e-122">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until **IESP::Resume** is called to restart the capture.</span></span> <span data-ttu-id="62f8e-123">Quando si utilizzano **pause** e **Resume** per arrestare e riavviare l'acquisizione, tutte le informazioni acquisite vengono inserite nello stesso file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="62f8e-123">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="62f8e-124">Quando si usa **Sospendi** e **Riprendi** per controllare l'acquisizione, Network Monitor continua ad aggiungere [*statistiche di conversazione*](c.md) alle statistiche esistenti per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="62f8e-124">When using **Pause** and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="62f8e-125">Per arrestare l'acquisizione, chiamare [**IESP:: Stop**](iesp-stop.md).</span><span class="sxs-lookup"><span data-stu-id="62f8e-125">To stop the capture, call [**IESP::Stop**](iesp-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62f8e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62f8e-126">Requirements</span></span>



| <span data-ttu-id="62f8e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="62f8e-127">Requirement</span></span> | <span data-ttu-id="62f8e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="62f8e-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62f8e-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62f8e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="62f8e-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="62f8e-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="62f8e-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62f8e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="62f8e-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="62f8e-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="62f8e-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62f8e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="62f8e-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="62f8e-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="62f8e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="62f8e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62f8e-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62f8e-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62f8e-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62f8e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62f8e-138">IESP</span><span class="sxs-lookup"><span data-stu-id="62f8e-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="62f8e-139">**IESP:: Connect**</span><span class="sxs-lookup"><span data-stu-id="62f8e-139">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="62f8e-140">**IESP::P ause**</span><span class="sxs-lookup"><span data-stu-id="62f8e-140">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="62f8e-141">**IESP:: Stop**</span><span class="sxs-lookup"><span data-stu-id="62f8e-141">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> </dl>

 

 




