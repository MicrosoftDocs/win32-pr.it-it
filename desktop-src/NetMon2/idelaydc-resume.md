---
description: "Metodo IDelaydC::Resume: il metodo Resume riavvia un'acquisizione sospesa."
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: Metodo IDelaydC::Resume (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Resume
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 9c8c3b505e0e9fb306a444111cce22c8c580d015
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109189"
---
# <a name="idelaydcresume-method"></a><span data-ttu-id="691cd-103">Metodo IDelaydC::Resume</span><span class="sxs-lookup"><span data-stu-id="691cd-103">IDelaydC::Resume method</span></span>

<span data-ttu-id="691cd-104">Il **metodo Resume** riavvia un'acquisizione sospesa.</span><span class="sxs-lookup"><span data-stu-id="691cd-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="691cd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="691cd-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="691cd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="691cd-106">Parameters</span></span>

<span data-ttu-id="691cd-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="691cd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="691cd-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="691cd-108">Return value</span></span>

<span data-ttu-id="691cd-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="691cd-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="691cd-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="691cd-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="691cd-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="691cd-111">Return code</span></span>                                                                                                | <span data-ttu-id="691cd-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="691cd-112">Description</span></span>                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="691cd-113"><dt>**ACQUISIZIONE NMERR \_ \_ NON \_ SOSPESA**</dt></span><span class="sxs-lookup"><span data-stu-id="691cd-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="691cd-114">L'acquisizione non viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="691cd-114">The capture is not paused.</span></span> <span data-ttu-id="691cd-115">Chiamare [**IDelaydC::P ause**](idelaydc-pause.md) per sospendere l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="691cd-115">Call [**IDelaydC::Pause**](idelaydc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="691cd-116"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="691cd-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="691cd-117">NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="691cd-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="691cd-118">Chiamare [**IDelaydC::Connect**](idelaydc-connect.md) per connettere NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="691cd-118">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="691cd-119"><dt>**NMERR \_ NON \_ RITARDATO**</dt></span><span class="sxs-lookup"><span data-stu-id="691cd-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>         | <span data-ttu-id="691cd-120">NPP è connesso alla rete, ma non con il [**metodo IDelaydC::Connect.**](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="691cd-120">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="691cd-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="691cd-121">Remarks</span></span>

<span data-ttu-id="691cd-122">Durante la sospensione dell'acquisizione, i nuovi dati non vengono aggiunti al [*file*](c.md) di acquisizione corrente finché non viene chiamato il metodo **IDelaydC::Resume** per riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="691cd-122">While the capture is paused, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="691cd-123">Quando [**sospendi**](idelaydc-pause.md) **e** riprendi vengono usati per arrestare e riavviare l'acquisizione, tutte le informazioni acquisite vengono inserite nello stesso file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="691cd-123">When [**Pause**](idelaydc-pause.md) and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="691cd-124">Quando si [**usano Pause**](idelaydc-pause.md) e **Resume** per controllare l'acquisizione, Network Monitor continua ad aggiungere statistiche di conversazione alle statistiche esistenti per l'acquisizione corrente. [](c.md)</span><span class="sxs-lookup"><span data-stu-id="691cd-124">When using [**Pause**](idelaydc-pause.md) and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="691cd-125">Per arrestare l'acquisizione, [**chiamare IDelaydC::Stop**](idelaydc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="691cd-125">To stop the capture, call [**IDelaydC::Stop**](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="691cd-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="691cd-126">Requirements</span></span>



| <span data-ttu-id="691cd-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="691cd-127">Requirement</span></span> | <span data-ttu-id="691cd-128">Valore</span><span class="sxs-lookup"><span data-stu-id="691cd-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="691cd-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="691cd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="691cd-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="691cd-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="691cd-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="691cd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="691cd-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="691cd-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="691cd-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="691cd-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="691cd-134"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="691cd-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="691cd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="691cd-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="691cd-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="691cd-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="691cd-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="691cd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="691cd-138">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="691cd-138">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="691cd-139">**IDelaydC::Connect**</span><span class="sxs-lookup"><span data-stu-id="691cd-139">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="691cd-140">**IDelaydC::P ause**</span><span class="sxs-lookup"><span data-stu-id="691cd-140">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="691cd-141">**IDelaydC::Stop**</span><span class="sxs-lookup"><span data-stu-id="691cd-141">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




