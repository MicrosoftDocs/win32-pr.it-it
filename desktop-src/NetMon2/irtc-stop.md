---
description: Il metodo Stop arresta l'acquisizione corrente.
ms.assetid: 64a80ff1-5a48-4be8-835d-a3d304ebb324
title: 'Metodo IRTC:: Stop (Netmon. h)'
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
ms.openlocfilehash: f25bf9d56a6f41acefad9a552dd2f591158bc74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310500"
---
# <a name="irtcstop-method"></a><span data-ttu-id="aca0f-103">Metodo IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="aca0f-103">IRTC::Stop method</span></span>

<span data-ttu-id="aca0f-104">Il metodo **Stop** arresta l'acquisizione corrente.</span><span class="sxs-lookup"><span data-stu-id="aca0f-104">The **Stop** method stops the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="aca0f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aca0f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Stop();
```



## <a name="parameters"></a><span data-ttu-id="aca0f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aca0f-106">Parameters</span></span>

<span data-ttu-id="aca0f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="aca0f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aca0f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aca0f-108">Return value</span></span>

<span data-ttu-id="aca0f-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="aca0f-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="aca0f-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="aca0f-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="aca0f-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="aca0f-111">Return code</span></span>                                                                                          | <span data-ttu-id="aca0f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aca0f-112">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aca0f-113"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="aca0f-113"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="aca0f-114">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="aca0f-114">The NPP is not connected to the network.</span></span> <span data-ttu-id="aca0f-115">Chiamare [IRTC:: Connect](irtc-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="aca0f-115">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="aca0f-116"><dt>**NMERR \_ non \_ acquisizione**</dt></span><span class="sxs-lookup"><span data-stu-id="aca0f-116"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="aca0f-117">L'oggetto NPP non sta acquisendo dati.</span><span class="sxs-lookup"><span data-stu-id="aca0f-117">The NPP is not capturing data.</span></span> <span data-ttu-id="aca0f-118">Chiamare [IRTC:: Start](irtc-start.md) per avviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="aca0f-118">Call [IRTC::Start](irtc-start.md) to start the capture.</span></span><br/>                            |
| <dl> <span data-ttu-id="aca0f-119"><dt>**NMERR \_ non in \_ tempo reale**</dt></span><span class="sxs-lookup"><span data-stu-id="aca0f-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="aca0f-120">L'oggetto NPP è connesso alla rete, ma non con il metodo [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="aca0f-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="aca0f-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="aca0f-121">Remarks</span></span>

<span data-ttu-id="aca0f-122">Quando si riavvia l'acquisizione dopo aver chiamato il metodo **IRTC:: Stop** , assicurarsi di chiamare [IRTC:: Configure](irtc-configure.md) ogni volta che si chiama [IRTC:: Start](irtc-start.md) per riavviare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="aca0f-122">When you restart the capture after calling the **IRTC::Stop** method, make sure to call [IRTC::Configure](irtc-configure.md) each time you call [IRTC::Start](irtc-start.md) to restart the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="aca0f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aca0f-123">Requirements</span></span>



| <span data-ttu-id="aca0f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="aca0f-124">Requirement</span></span> | <span data-ttu-id="aca0f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="aca0f-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aca0f-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aca0f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="aca0f-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aca0f-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="aca0f-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aca0f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="aca0f-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aca0f-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="aca0f-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aca0f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="aca0f-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="aca0f-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="aca0f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="aca0f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aca0f-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aca0f-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aca0f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aca0f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aca0f-135">IRTC</span><span class="sxs-lookup"><span data-stu-id="aca0f-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="aca0f-136">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="aca0f-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="aca0f-137">IRTC:: Configure</span><span class="sxs-lookup"><span data-stu-id="aca0f-137">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="aca0f-138">IRTC:: Start</span><span class="sxs-lookup"><span data-stu-id="aca0f-138">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




