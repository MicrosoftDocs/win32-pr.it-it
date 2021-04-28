---
description: "Metodo IDelaydC::P ause: il metodo Pause sospende l'acquisizione corrente."
ms.assetid: 9d5e11d1-8c45-4cf5-9fea-10c9e7a6fe86
title: Metodo IDelaydC::P ause (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Pause
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 21b4cd7b6cb921f7bd71b8670a37da12b2239b92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098499"
---
# <a name="idelaydcpause-method"></a><span data-ttu-id="85a7b-103">Metodo IDelaydC::P ause</span><span class="sxs-lookup"><span data-stu-id="85a7b-103">IDelaydC::Pause method</span></span>

<span data-ttu-id="85a7b-104">Il **metodo Pause** sospende l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="85a7b-104">The **Pause** method pauses the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="85a7b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85a7b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Pause();
```



## <a name="parameters"></a><span data-ttu-id="85a7b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="85a7b-106">Parameters</span></span>

<span data-ttu-id="85a7b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="85a7b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="85a7b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85a7b-108">Return value</span></span>

<span data-ttu-id="85a7b-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="85a7b-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="85a7b-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="85a7b-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="85a7b-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="85a7b-111">Return code</span></span>                                                                                           | <span data-ttu-id="85a7b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85a7b-112">Description</span></span>                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85a7b-113"><dt>**ACQUISIZIONE NMERR \_ \_ SOSPESA**</dt></span><span class="sxs-lookup"><span data-stu-id="85a7b-113"><dt>**NMERR\_CAPTURE\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="85a7b-114">L'acquisizione è già in stato di sospensione.</span><span class="sxs-lookup"><span data-stu-id="85a7b-114">The capture is already in a paused state.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="85a7b-115"><dt>**NMERR \_ NON \_ ACQUISISCE**</dt></span><span class="sxs-lookup"><span data-stu-id="85a7b-115"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>  | <span data-ttu-id="85a7b-116">NPP non acquisisce dati.</span><span class="sxs-lookup"><span data-stu-id="85a7b-116">The NPP is not capturing data.</span></span> <span data-ttu-id="85a7b-117">Chiamare [IDelaydC::Start](idelaydc-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="85a7b-117">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="85a7b-118"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="85a7b-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>  | <span data-ttu-id="85a7b-119">NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="85a7b-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="85a7b-120">Chiamare [IDelaydC::Connect](idelaydc-connect.md) per connettere NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="85a7b-120">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="85a7b-121"><dt>**NMERR \_ NON \_ RITARDATO**</dt></span><span class="sxs-lookup"><span data-stu-id="85a7b-121"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>    | <span data-ttu-id="85a7b-122">NPP è connesso alla rete, ma non con il [metodo IDelaydC::Connect.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="85a7b-122">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="85a7b-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="85a7b-123">Remarks</span></span>

<span data-ttu-id="85a7b-124">Mentre l'acquisizione è in stato di sospensione, i nuovi dati non vengono aggiunti al [*file*](c.md) di acquisizione corrente finché non viene chiamato il metodo **IDelaydC::Resume** per riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="85a7b-124">While the capture is in a paused state, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="85a7b-125">Quando **sospendi** **e** riprendi vengono usati per arrestare e riavviare l'acquisizione, tutte le informazioni acquisite vengono inserite nello stesso file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="85a7b-125">When **Pause** and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="85a7b-126">Quando si usa **IDelaydC::P ause** e **IDelaydC::Resume** per controllare l'acquisizione, Network Monitor continua ad aggiungere statistiche di conversazione ogni volta che l'acquisizione è in esecuzione. [](c.md)</span><span class="sxs-lookup"><span data-stu-id="85a7b-126">When using **IDelaydC::Pause** and **IDelaydC::Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) whenever the capture is running.</span></span>

<span data-ttu-id="85a7b-127">Per riavviare l'acquisizione, [chiamare IDelaydC::Resume](idelaydc-resume.md).</span><span class="sxs-lookup"><span data-stu-id="85a7b-127">To restart the capture, call [IDelaydC::Resume](idelaydc-resume.md).</span></span>

<span data-ttu-id="85a7b-128">Per arrestare l'acquisizione, [chiamare IDelaydC::Stop](idelaydc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="85a7b-128">To stop the capture, call [IDelaydC::Stop](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85a7b-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85a7b-129">Requirements</span></span>



| <span data-ttu-id="85a7b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="85a7b-130">Requirement</span></span> | <span data-ttu-id="85a7b-131">Valore</span><span class="sxs-lookup"><span data-stu-id="85a7b-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85a7b-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85a7b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="85a7b-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="85a7b-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="85a7b-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85a7b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="85a7b-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="85a7b-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="85a7b-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85a7b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="85a7b-137"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="85a7b-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="85a7b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="85a7b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85a7b-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85a7b-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85a7b-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85a7b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85a7b-141">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="85a7b-141">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="85a7b-142">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="85a7b-142">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="85a7b-143">IDelaydC::Resume</span><span class="sxs-lookup"><span data-stu-id="85a7b-143">IDelaydC::Resume</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="85a7b-144">IDelaydC::Start</span><span class="sxs-lookup"><span data-stu-id="85a7b-144">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="85a7b-145">IDelaydC::Stop</span><span class="sxs-lookup"><span data-stu-id="85a7b-145">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




