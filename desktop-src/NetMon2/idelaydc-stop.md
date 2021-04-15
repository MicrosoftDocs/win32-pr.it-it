---
description: Il metodo Stop arresta l'acquisizione corrente.
ms.assetid: 1b627137-e72d-4425-98d9-e296fb07e509
title: 'Metodo IDelaydC:: Stop (Netmon. h)'
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
ms.openlocfilehash: 42c9cc1c4b6da7b5f934dd96f26aa9348c43ac0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484308"
---
# <a name="idelaydcstop-method"></a><span data-ttu-id="0e4d0-103">Metodo IDelaydC:: Stop</span><span class="sxs-lookup"><span data-stu-id="0e4d0-103">IDelaydC::Stop method</span></span>

<span data-ttu-id="0e4d0-104">Il metodo **Stop** arresta l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="0e4d0-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e4d0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e4d0-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="0e4d0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e4d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e4d0-107">*lpStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0e4d0-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e4d0-108">Puntatore a una struttura di [statistiche](statistics.md) che contiene le statistiche di rete, ad esempio i frame totali e i byte totali acquisiti.</span><span class="sxs-lookup"><span data-stu-id="0e4d0-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e4d0-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e4d0-109">Return value</span></span>

<span data-ttu-id="0e4d0-110">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0e4d0-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="0e4d0-111">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="0e4d0-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="0e4d0-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0e4d0-112">Return code</span></span>                                                                                          | <span data-ttu-id="0e4d0-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e4d0-113">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e4d0-114"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="0e4d0-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="0e4d0-115">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="0e4d0-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="0e4d0-116">Chiamare [IDelaydC:: Connect](idelaydc-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="0e4d0-116">Call [IDelaydC::Connect](idelaydc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="0e4d0-117"><dt>**NMERR \_ non \_ acquisizione**</dt></span><span class="sxs-lookup"><span data-stu-id="0e4d0-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="0e4d0-118">L'oggetto NPP non sta acquisendo dati.</span><span class="sxs-lookup"><span data-stu-id="0e4d0-118">The NPP is not capturing data.</span></span> <span data-ttu-id="0e4d0-119">Chiamare [IDelaydC:: Start](idelaydc-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="0e4d0-119">Call [IDelaydC::Start](idelaydc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="0e4d0-120"><dt>**NMERR \_ non \_ ritardato**</dt></span><span class="sxs-lookup"><span data-stu-id="0e4d0-120"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="0e4d0-121">L'oggetto NPP è connesso alla rete, ma non con il metodo [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="0e4d0-121">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="0e4d0-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e4d0-122">Remarks</span></span>

<span data-ttu-id="0e4d0-123">Quando viene chiamato **IDelaydC:: Stop** , Network Monitor interrompe l'acquisizione dei dati e chiude il [*file di acquisizione*](c.md).</span><span class="sxs-lookup"><span data-stu-id="0e4d0-123">When **IDelaydC::Stop** is called, Network Monitor stops capturing data and closes the [*capture file*](c.md).</span></span> <span data-ttu-id="0e4d0-124">(Il nome del file di acquisizione è stato restituito quando è stato chiamato [IDelaydC:: Start](idelaydc-start.md) ).</span><span class="sxs-lookup"><span data-stu-id="0e4d0-124">(The name of the capture file was returned when [IDelaydC::Start](idelaydc-start.md) was called).</span></span> <span data-ttu-id="0e4d0-125">È ora possibile esaminare il contenuto del file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="0e4d0-125">You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="0e4d0-126">Quando si arresta e si avvia l'acquisizione, assicurarsi di chiamare il metodo [IDelaydC:: Configure](idelaydc-configure.md) ogni volta che si chiama [IDelaydC:: Start](idelaydc-start.md) per riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="0e4d0-126">When you stop and start the capture, make sure you call the [IDelaydC::Configure](idelaydc-configure.md) method each time you call [IDelaydC::Start](idelaydc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e4d0-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e4d0-127">Requirements</span></span>



| <span data-ttu-id="0e4d0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e4d0-128">Requirement</span></span> | <span data-ttu-id="0e4d0-129">Valore</span><span class="sxs-lookup"><span data-stu-id="0e4d0-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e4d0-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e4d0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0e4d0-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0e4d0-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="0e4d0-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e4d0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0e4d0-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0e4d0-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="0e4d0-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e4d0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e4d0-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e4d0-135"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="0e4d0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0e4d0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e4d0-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e4d0-137"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e4d0-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e4d0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e4d0-139">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="0e4d0-139">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="0e4d0-140">IDelaydC:: Connect</span><span class="sxs-lookup"><span data-stu-id="0e4d0-140">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="0e4d0-141">IDelaydC:: Configure</span><span class="sxs-lookup"><span data-stu-id="0e4d0-141">IDelaydC::Configure</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="0e4d0-142">IDelaydC:: Start</span><span class="sxs-lookup"><span data-stu-id="0e4d0-142">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="0e4d0-143">Statistiche</span><span class="sxs-lookup"><span data-stu-id="0e4d0-143">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




