---
description: "Metodo IRTC::Stop: il metodo Stop arresta l'acquisizione corrente."
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: Metodo IRTC::Stop (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Stop
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 10bf0886032c93288435ade05fec46077d53753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113519"
---
# <a name="irtcstop-method"></a><span data-ttu-id="bf7dd-103">Metodo IRTC::Stop</span><span class="sxs-lookup"><span data-stu-id="bf7dd-103">IRTC::Stop method</span></span>

<span data-ttu-id="bf7dd-104">Il **metodo Stop** arresta l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="bf7dd-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf7dd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf7dd-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="bf7dd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf7dd-106">Parameters</span></span>

<span data-ttu-id="bf7dd-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="bf7dd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bf7dd-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf7dd-108">Return value</span></span>

<span data-ttu-id="bf7dd-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="bf7dd-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bf7dd-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="bf7dd-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="bf7dd-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bf7dd-111">Return code</span></span>                                                                                          | <span data-ttu-id="bf7dd-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf7dd-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf7dd-113"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7dd-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="bf7dd-114">Il NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="bf7dd-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="bf7dd-115">Chiamare [IRTC::Connect](irtc-connect.md) per connettere il NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="bf7dd-115">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="bf7dd-116"><dt>**NMERR \_ NON \_ ACQUISISCE**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7dd-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="bf7dd-117">Il NPP non acquisisce dati.</span><span class="sxs-lookup"><span data-stu-id="bf7dd-117">The NPP is not capturing data.</span></span> <span data-ttu-id="bf7dd-118">Chiamare [IRTC::Start](irtc-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="bf7dd-118">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="bf7dd-119"><dt>**NMERR \_ NON IN TEMPO \_ REALE**</dt></span><span class="sxs-lookup"><span data-stu-id="bf7dd-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="bf7dd-120">Il NPP è connesso alla rete, ma non con il [metodo IRTC::Connect.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="bf7dd-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="bf7dd-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="bf7dd-121">Remarks</span></span>

<span data-ttu-id="bf7dd-122">Quando si riavvia l'acquisizione dopo aver chiamato il metodo **IRTC::Stop,** assicurarsi di chiamare [IRTC::Configure](irtc-configure.md) ogni volta che si chiama [IRTC::Start](irtc-start.md) per riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="bf7dd-122">When you restart the capture after calling the **IRTC::Stop** method, make sure to call [IRTC::Configure](irtc-configure.md) each time you call [IRTC::Start](irtc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf7dd-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf7dd-123">Requirements</span></span>



| <span data-ttu-id="bf7dd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf7dd-124">Requirement</span></span> | <span data-ttu-id="bf7dd-125">Valore</span><span class="sxs-lookup"><span data-stu-id="bf7dd-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf7dd-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf7dd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bf7dd-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bf7dd-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="bf7dd-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bf7dd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bf7dd-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bf7dd-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="bf7dd-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bf7dd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf7dd-131"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="bf7dd-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="bf7dd-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bf7dd-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf7dd-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf7dd-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf7dd-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bf7dd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf7dd-135">IRTC</span><span class="sxs-lookup"><span data-stu-id="bf7dd-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="bf7dd-136">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="bf7dd-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="bf7dd-137">IRTC::Configure</span><span class="sxs-lookup"><span data-stu-id="bf7dd-137">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="bf7dd-138">IRTC::Start</span><span class="sxs-lookup"><span data-stu-id="bf7dd-138">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




