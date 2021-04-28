---
description: "Metodo IStats::Stop: il metodo Stop arresta l'acquisizione corrente."
ms.assetid: 3aeeb29e-e174-46a2-82bb-44c466b8db98
title: Metodo IStats::Stop (Netmon.h)
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
ms.openlocfilehash: ef51aff870a3193963b3802332112c51f1024826
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114609"
---
# <a name="istatsstop-method"></a><span data-ttu-id="a795f-103">Metodo IStats::Stop</span><span class="sxs-lookup"><span data-stu-id="a795f-103">IStats::Stop method</span></span>

<span data-ttu-id="a795f-104">Il **metodo Stop** arresta l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="a795f-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="a795f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a795f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="a795f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a795f-106">Parameters</span></span>

<span data-ttu-id="a795f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a795f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a795f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a795f-108">Return value</span></span>

<span data-ttu-id="a795f-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="a795f-109">If the method is successful the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a795f-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="a795f-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="a795f-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a795f-111">Return code</span></span>                                                                                            | <span data-ttu-id="a795f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a795f-112">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a795f-113"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="a795f-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="a795f-114">NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="a795f-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="a795f-115">Chiamare il [metodo IStats::Connect](istats-connect.md) per connettere NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="a795f-115">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="a795f-116"><dt>**NMERR \_ NON \_ ACQUISISCE**</dt></span><span class="sxs-lookup"><span data-stu-id="a795f-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="a795f-117">NPP non acquisisce dati.</span><span class="sxs-lookup"><span data-stu-id="a795f-117">The NPP is not capturing data.</span></span> <span data-ttu-id="a795f-118">Chiamare il [metodo IStats::Start](istats-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="a795f-118">Call the [IStats::Start](istats-start.md) method to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="a795f-119"><dt>**NMERR \_ NON \_ STATS \_ ONLY**</dt></span><span class="sxs-lookup"><span data-stu-id="a795f-119"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="a795f-120">NPP è connesso alla rete, ma non con il [metodo IStats::Connect.](istats-connect.md)</span><span class="sxs-lookup"><span data-stu-id="a795f-120">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |



 

## <a name="remarks"></a><span data-ttu-id="a795f-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="a795f-121">Remarks</span></span>

<span data-ttu-id="a795f-122">Quando si riavvia l'acquisizione dopo la chiamata di **IStats::Stop,** assicurarsi di chiamare il metodo [IStats::Configure](istats-configure.md) ogni volta che si chiama [IStats::Start](istats-start.md) per riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="a795f-122">When restarting the capture after **IStats::Stop** has been called, make sure you call the [IStats::Configure](istats-configure.md) method each time you call [IStats::Start](istats-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="a795f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a795f-123">Requirements</span></span>



| <span data-ttu-id="a795f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a795f-124">Requirement</span></span> | <span data-ttu-id="a795f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a795f-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a795f-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a795f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a795f-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a795f-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="a795f-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a795f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a795f-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a795f-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="a795f-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a795f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a795f-131"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="a795f-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="a795f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a795f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a795f-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a795f-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a795f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a795f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a795f-135">IStat</span><span class="sxs-lookup"><span data-stu-id="a795f-135">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="a795f-136">IStats::Connect</span><span class="sxs-lookup"><span data-stu-id="a795f-136">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="a795f-137">IStats::Configure</span><span class="sxs-lookup"><span data-stu-id="a795f-137">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="a795f-138">IStats::Start</span><span class="sxs-lookup"><span data-stu-id="a795f-138">IStats::Start</span></span>](istats-start.md)
</dt> </dl>

 

 




