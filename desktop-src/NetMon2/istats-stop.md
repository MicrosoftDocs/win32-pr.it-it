---
description: Il metodo Stop arresta l'acquisizione corrente.
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: 'Metodo IStats:: Stop (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 7b7b58527e7bde0c3bbdec4fc162b705dd178c10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308168"
---
# <a name="istatsstop-method"></a><span data-ttu-id="3e96b-103">IStats:: Stop (metodo)</span><span class="sxs-lookup"><span data-stu-id="3e96b-103">IStats::Stop method</span></span>

<span data-ttu-id="3e96b-104">Il metodo **Stop** arresta l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="3e96b-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e96b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e96b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="3e96b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e96b-106">Parameters</span></span>

<span data-ttu-id="3e96b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3e96b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3e96b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e96b-108">Return value</span></span>

<span data-ttu-id="3e96b-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3e96b-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3e96b-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="3e96b-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="3e96b-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3e96b-111">Return code</span></span>                                                                                            | <span data-ttu-id="3e96b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e96b-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e96b-113"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="3e96b-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="3e96b-114">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="3e96b-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="3e96b-115">Chiamare il metodo [IStats:: Connect](istats-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="3e96b-115">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="3e96b-116"><dt>**NMERR \_ non \_ acquisizione**</dt></span><span class="sxs-lookup"><span data-stu-id="3e96b-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="3e96b-117">L'oggetto NPP non sta acquisendo dati.</span><span class="sxs-lookup"><span data-stu-id="3e96b-117">The NPP is not capturing data.</span></span> <span data-ttu-id="3e96b-118">Chiamare il metodo [IStats:: Start](istats-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="3e96b-118">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="3e96b-119"><dt>**NMERR \_ non \_ \_ solo statistiche**</dt></span><span class="sxs-lookup"><span data-stu-id="3e96b-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="3e96b-120">L'oggetto NPP è connesso alla rete, ma non con il metodo [IStats:: Connect](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="3e96b-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="3e96b-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e96b-121">Remarks</span></span>

<span data-ttu-id="3e96b-122">Quando si riavvia l'acquisizione dopo **IStats:: Stop** è stato chiamato, assicurarsi di chiamare il metodo [IStats:: Configure](istats-configure.md) ogni volta che si chiama [IStats:: Start](istats-start.md) per riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="3e96b-122">When restarting the capture after **IStats::Stop** has been called, make sure you call the [IStats::Configure](istats-configure.md) method each time you call [IStats::Start](istats-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e96b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e96b-123">Requirements</span></span>



| <span data-ttu-id="3e96b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e96b-124">Requirement</span></span> | <span data-ttu-id="3e96b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3e96b-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e96b-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e96b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3e96b-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3e96b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="3e96b-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e96b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3e96b-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3e96b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="3e96b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e96b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e96b-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e96b-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="3e96b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3e96b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e96b-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e96b-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e96b-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e96b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e96b-135">IStats</span><span class="sxs-lookup"><span data-stu-id="3e96b-135">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="3e96b-136">IStats:: Connect</span><span class="sxs-lookup"><span data-stu-id="3e96b-136">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="3e96b-137">IStats:: Configure</span><span class="sxs-lookup"><span data-stu-id="3e96b-137">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="3e96b-138">IStats:: Start</span><span class="sxs-lookup"><span data-stu-id="3e96b-138">IStats::Start</span></span>](istats-start.md)
</dt> </dl>

 

 




