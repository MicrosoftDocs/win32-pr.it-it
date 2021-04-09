---
description: Il metodo Resume riavvia un'acquisizione sospesa.
ms.assetid: 4fa47220-d323-407b-9dae-704969f66bdd
title: 'Metodo IDelaydC:: Resume (Netmon. h)'
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
ms.openlocfilehash: ba0deef666c2e9829cb5a71d91e73da9c1b7d780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750058"
---
# <a name="idelaydcresume-method"></a><span data-ttu-id="0adfe-103">Metodo IDelaydC:: Resume</span><span class="sxs-lookup"><span data-stu-id="0adfe-103">IDelaydC::Resume method</span></span>

<span data-ttu-id="0adfe-104">Il metodo **Resume** riavvia un'acquisizione sospesa.</span><span class="sxs-lookup"><span data-stu-id="0adfe-104">The **Resume** method restarts a paused capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0adfe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0adfe-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Resume();
```



## <a name="parameters"></a><span data-ttu-id="0adfe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0adfe-106">Parameters</span></span>

<span data-ttu-id="0adfe-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0adfe-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0adfe-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0adfe-108">Return value</span></span>

<span data-ttu-id="0adfe-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0adfe-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0adfe-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="0adfe-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="0adfe-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0adfe-111">Return code</span></span>                                                                                                | <span data-ttu-id="0adfe-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0adfe-112">Description</span></span>                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0adfe-113"><dt>**\_acquisizione NMERR \_ non \_ sospesa**</dt></span><span class="sxs-lookup"><span data-stu-id="0adfe-113"><dt>**NMERR\_CAPTURE\_NOT\_PAUSED**</dt></span></span> </dl> | <span data-ttu-id="0adfe-114">L'acquisizione non è sospesa.</span><span class="sxs-lookup"><span data-stu-id="0adfe-114">The capture is not paused.</span></span> <span data-ttu-id="0adfe-115">Chiamare [**IDelaydC::P ause**](idelaydc-pause.md) per sospendere l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="0adfe-115">Call [**IDelaydC::Pause**](idelaydc-pause.md) to pause the capture.</span></span><br/>                                |
| <dl> <span data-ttu-id="0adfe-116"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="0adfe-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>       | <span data-ttu-id="0adfe-117">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="0adfe-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="0adfe-118">Chiamare [**IDelaydC:: Connect**](idelaydc-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="0adfe-118">Call [**IDelaydC::Connect**](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="0adfe-119"><dt>**NMERR \_ non \_ ritardato**</dt></span><span class="sxs-lookup"><span data-stu-id="0adfe-119"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>         | <span data-ttu-id="0adfe-120">L'oggetto NPP è connesso alla rete, ma non con il metodo [**IDelaydC:: Connect**](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="0adfe-120">The NPP is connected to the network but not with the [**IDelaydC::Connect**](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="0adfe-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="0adfe-121">Remarks</span></span>

<span data-ttu-id="0adfe-122">Quando l'acquisizione viene sospesa, i nuovi dati non vengono aggiunti al [*file di acquisizione*](c.md) corrente fino a quando non viene chiamato il metodo **IDelaydC:: Resume** per riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="0adfe-122">While the capture is paused, new data is not added to the current [*capture file*](c.md) until the **IDelaydC::Resume** method is called to restart the capture.</span></span> <span data-ttu-id="0adfe-123">Quando si utilizzano [**pause**](idelaydc-pause.md) e **Resume** per arrestare e riavviare l'acquisizione, tutte le informazioni acquisite vengono inserite nello stesso file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="0adfe-123">When [**Pause**](idelaydc-pause.md) and **Resume** are used to stop and restart the capture, all captured information is put in the same capture file.</span></span>

<span data-ttu-id="0adfe-124">Quando si usa [**Sospendi**](idelaydc-pause.md) e **Riprendi** per controllare l'acquisizione, Network Monitor continua ad aggiungere [*statistiche di conversazione*](c.md) alle statistiche esistenti per l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="0adfe-124">When using [**Pause**](idelaydc-pause.md) and **Resume** to control the capture, Network Monitor continues to add [*conversation statistics*](c.md) to the existing statistics for the current capture.</span></span>

<span data-ttu-id="0adfe-125">Per arrestare l'acquisizione, chiamare [**IDelaydC:: Stop**](idelaydc-stop.md).</span><span class="sxs-lookup"><span data-stu-id="0adfe-125">To stop the capture, call [**IDelaydC::Stop**](idelaydc-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0adfe-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0adfe-126">Requirements</span></span>



| <span data-ttu-id="0adfe-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0adfe-127">Requirement</span></span> | <span data-ttu-id="0adfe-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0adfe-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0adfe-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0adfe-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0adfe-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0adfe-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0adfe-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0adfe-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0adfe-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0adfe-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0adfe-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0adfe-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0adfe-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0adfe-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0adfe-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0adfe-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0adfe-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0adfe-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0adfe-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0adfe-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0adfe-138">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="0adfe-138">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="0adfe-139">**IDelaydC:: Connect**</span><span class="sxs-lookup"><span data-stu-id="0adfe-139">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="0adfe-140">**IDelaydC::P ause**</span><span class="sxs-lookup"><span data-stu-id="0adfe-140">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="0adfe-141">**IDelaydC:: Stop**</span><span class="sxs-lookup"><span data-stu-id="0adfe-141">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




