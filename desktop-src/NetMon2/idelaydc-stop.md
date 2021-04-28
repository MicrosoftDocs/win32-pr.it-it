---
description: "Metodo IDelaydC::Stop: il metodo Stop arresta l'acquisizione corrente."
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: Metodo IDelaydC::Stop (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 38be5b6ba4c3f6edcd716f4d0235150e96dd692a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110779"
---
# <a name="idelaydcstop-method"></a><span data-ttu-id="c5914-103">Metodo IDelaydC::Stop</span><span class="sxs-lookup"><span data-stu-id="c5914-103">IDelaydC::Stop method</span></span>

<span data-ttu-id="c5914-104">Il **metodo Stop** arresta l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="c5914-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5914-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5914-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="c5914-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5914-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5914-107">*lpStats* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="c5914-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5914-108">Puntatore a una [struttura STATISTICS](statistics.md) che contiene statistiche di rete, ad esempio i frame totali e i byte totali acquisiti.</span><span class="sxs-lookup"><span data-stu-id="c5914-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5914-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5914-109">Return value</span></span>

<span data-ttu-id="c5914-110">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="c5914-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c5914-111">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5914-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="c5914-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c5914-112">Return code</span></span>                                                                                          | <span data-ttu-id="c5914-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5914-113">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c5914-114"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="c5914-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="c5914-115">Il NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="c5914-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="c5914-116">Chiamare [IDelaydC::Connect](idelaydc-connect.md) per connettere il NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="c5914-116">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="c5914-117"><dt>**NMERR \_ NON \_ ACQUISISCE**</dt></span><span class="sxs-lookup"><span data-stu-id="c5914-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="c5914-118">Il NPP non acquisisce dati.</span><span class="sxs-lookup"><span data-stu-id="c5914-118">The NPP is not capturing data.</span></span> <span data-ttu-id="c5914-119">Chiamare [IDelaydC::Start](idelaydc-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c5914-119">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="c5914-120"><dt>**NMERR \_ NON \_ RITARDATO**</dt></span><span class="sxs-lookup"><span data-stu-id="c5914-120"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="c5914-121">Il NPP è connesso alla rete, ma non con il [metodo IDelaydC::Connect.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="c5914-121">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="c5914-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5914-122">Remarks</span></span>

<span data-ttu-id="c5914-123">Quando **viene chiamato IDelaydC::Stop,** Network Monitor l'acquisizione dei dati e chiude il [*file di acquisizione*](c.md).</span><span class="sxs-lookup"><span data-stu-id="c5914-123">When **IDelaydC::Stop** is called, Network Monitor stops capturing data and closes the [*capture file*](c.md).</span></span> <span data-ttu-id="c5914-124">Il nome del file di acquisizione è stato restituito quando è stato chiamato [IDelaydC::Start.](idelaydc-start.md)</span><span class="sxs-lookup"><span data-stu-id="c5914-124">(The name of the capture file was returned when [IDelaydC::Start](idelaydc-start.md) was called).</span></span> <span data-ttu-id="c5914-125">È ora possibile esaminare il contenuto del file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c5914-125">You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="c5914-126">Quando si arresta e si avvia l'acquisizione, assicurarsi di chiamare il metodo [IDelaydC::Configure](idelaydc-configure.md) ogni volta che si chiama [IDelaydC::Start](idelaydc-start.md) per riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c5914-126">When you stop and start the capture, make sure you call the [IDelaydC::Configure](idelaydc-configure.md) method each time you call [IDelaydC::Start](idelaydc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5914-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5914-127">Requirements</span></span>



| <span data-ttu-id="c5914-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5914-128">Requirement</span></span> | <span data-ttu-id="c5914-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c5914-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5914-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5914-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c5914-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c5914-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c5914-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5914-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c5914-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c5914-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c5914-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5914-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5914-135"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="c5914-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c5914-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c5914-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5914-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5914-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5914-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5914-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5914-139">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="c5914-139">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="c5914-140">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="c5914-140">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="c5914-141">IDelaydC::Configure</span><span class="sxs-lookup"><span data-stu-id="c5914-141">IDelaydC::Configure</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="c5914-142">IDelaydC::Start</span><span class="sxs-lookup"><span data-stu-id="c5914-142">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="c5914-143">Statistiche</span><span class="sxs-lookup"><span data-stu-id="c5914-143">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




