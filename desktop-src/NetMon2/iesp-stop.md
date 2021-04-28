---
description: "Metodo IESP::Stop: il metodo Stop arresta l'acquisizione corrente."
ms.assetid: d2d4e51a-c6a4-4aec-a805-929af621ffb3
title: Metodo IESP::Stop (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ac262d8da5ab218db7300ea38da59d5c738421c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103769"
---
# <a name="iespstop-method"></a><span data-ttu-id="609bc-103">Metodo IESP::Stop</span><span class="sxs-lookup"><span data-stu-id="609bc-103">IESP::Stop method</span></span>

<span data-ttu-id="609bc-104">Il **metodo Stop** arresta l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="609bc-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="609bc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="609bc-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop(
  [out] LPSTATISTICS lpStats
);
```



## <a name="parameters"></a><span data-ttu-id="609bc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="609bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="609bc-107">*lpStats* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="609bc-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="609bc-108">Puntatore a una [struttura STATISTICS](statistics.md) che contiene statistiche di rete, ad esempio frame totali e byte totali acquisiti.</span><span class="sxs-lookup"><span data-stu-id="609bc-108">Pointer to a [STATISTICS](statistics.md) structure that contains network statistics such as total frames and total bytes captured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="609bc-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="609bc-109">Return value</span></span>

<span data-ttu-id="609bc-110">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="609bc-110">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="609bc-111">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="609bc-111">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="609bc-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="609bc-112">Return code</span></span>                                                                                          | <span data-ttu-id="609bc-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="609bc-113">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="609bc-114"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="609bc-114"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="609bc-115">NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="609bc-115">The NPP is not connected to the network.</span></span> <span data-ttu-id="609bc-116">Chiamare [IESP::Connect](iesp-connect.md) per connettere NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="609bc-116">Call [IESP::Connect](iesp-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="609bc-117"><dt>**NMERR \_ NON \_ ACQUISISCE**</dt></span><span class="sxs-lookup"><span data-stu-id="609bc-117"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="609bc-118">NPP non acquisisce dati.</span><span class="sxs-lookup"><span data-stu-id="609bc-118">The NPP is not capturing data.</span></span> <span data-ttu-id="609bc-119">Chiamare [IESP::Start](iesp-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="609bc-119">Call [IESP::Start](iesp-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="609bc-120"><dt>**NMERR \_ NON \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="609bc-120"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="609bc-121">NPP è connesso alla rete, ma non con il [metodo IESP::Connect.](iesp-connect.md)</span><span class="sxs-lookup"><span data-stu-id="609bc-121">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="609bc-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="609bc-122">Remarks</span></span>

<span data-ttu-id="609bc-123">Quando viene **chiamato il metodo IESP::Stop,** Network Monitor l'acquisizione dei dati e chiude il [*file di acquisizione.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="609bc-123">When the **IESP::Stop** method is called, Network Monitor stops capturing data and closes the [*capture file.*](c.md)</span></span> <span data-ttu-id="609bc-124">Il nome del file di acquisizione è stato restituito quando è stato chiamato [IESP::Start.](iesp-start.md) È ora possibile esaminare il contenuto del file di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="609bc-124">(The name of the capture file was returned when [IESP::Start](iesp-start.md) was called.) You can now look at the contents of the capture file.</span></span>

<span data-ttu-id="609bc-125">Quando si arresta e si riavvia l'acquisizione, assicurarsi di chiamare il metodo [IESP::Configure](iesp-configure.md) ogni volta che si chiama [IESP::Start](iesp-start.md) per riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="609bc-125">When you stop and restart the capture, make sure to call the [IESP::Configure](iesp-configure.md) method each time you call [IESP::Start](iesp-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="609bc-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="609bc-126">Requirements</span></span>



| <span data-ttu-id="609bc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="609bc-127">Requirement</span></span> | <span data-ttu-id="609bc-128">Valore</span><span class="sxs-lookup"><span data-stu-id="609bc-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="609bc-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="609bc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="609bc-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="609bc-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="609bc-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="609bc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="609bc-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="609bc-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="609bc-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="609bc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="609bc-134"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="609bc-134"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="609bc-135">DLL</span><span class="sxs-lookup"><span data-stu-id="609bc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="609bc-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="609bc-136"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="609bc-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="609bc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="609bc-138">IESP</span><span class="sxs-lookup"><span data-stu-id="609bc-138">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="609bc-139">IESP::Connect</span><span class="sxs-lookup"><span data-stu-id="609bc-139">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="609bc-140">IESP::Start</span><span class="sxs-lookup"><span data-stu-id="609bc-140">IESP::Start</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="609bc-141">Statistiche</span><span class="sxs-lookup"><span data-stu-id="609bc-141">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




