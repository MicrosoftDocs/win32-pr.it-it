---
description: Il metodo Disconnect disconnette l'oggetto NPP dalla rete.
ms.assetid: 962e033d-a51c-47a2-83dc-cee1e7150ab8
title: 'IESP: metodo:D di connessione (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b0dac1843083d77121883b2609c32addffbae290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128327"
---
# <a name="iespdisconnect-method"></a><span data-ttu-id="5331f-103">IESP::D metodo di connessione</span><span class="sxs-lookup"><span data-stu-id="5331f-103">IESP::Disconnect method</span></span>

<span data-ttu-id="5331f-104">Il metodo **Disconnect** disconnette l'oggetto NPP dalla rete.</span><span class="sxs-lookup"><span data-stu-id="5331f-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="5331f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5331f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="5331f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5331f-106">Parameters</span></span>

<span data-ttu-id="5331f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5331f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5331f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5331f-108">Return value</span></span>

<span data-ttu-id="5331f-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5331f-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5331f-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="5331f-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="5331f-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5331f-111">Return code</span></span>                                                                                          | <span data-ttu-id="5331f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5331f-112">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5331f-113"><dt>**\_acquisizione NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="5331f-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="5331f-114">L'oggetto NPP sta acquisendo i dati.</span><span class="sxs-lookup"><span data-stu-id="5331f-114">The NPP is capturing data.</span></span> <span data-ttu-id="5331f-115">Non è possibile disconnettersi dalla rete mentre è in corso l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="5331f-115">You cannot disconnect from the network while data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="5331f-116"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="5331f-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5331f-117">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="5331f-117">The NPP is not connected to the network.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="5331f-118"><dt>**NMERR \_ non \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="5331f-118"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="5331f-119">L'oggetto NPP è connesso alla rete, ma non con il metodo [IESP:: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="5331f-119">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="5331f-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="5331f-120">Remarks</span></span>

<span data-ttu-id="5331f-121">Questo metodo non può essere chiamato quando l'oggetto NPP sta acquisendo i dati.</span><span class="sxs-lookup"><span data-stu-id="5331f-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="5331f-122">È necessario chiamare il metodo **IESP:: Stop** prima di chiamare **IESP::D Disconnect**.</span><span class="sxs-lookup"><span data-stu-id="5331f-122">You must call the **IESP::Stop** method before calling **IESP::Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5331f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5331f-123">Requirements</span></span>



| <span data-ttu-id="5331f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5331f-124">Requirement</span></span> | <span data-ttu-id="5331f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5331f-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5331f-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5331f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5331f-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5331f-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="5331f-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5331f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5331f-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5331f-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="5331f-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5331f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5331f-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5331f-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="5331f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5331f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5331f-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5331f-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5331f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5331f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5331f-135">IESP</span><span class="sxs-lookup"><span data-stu-id="5331f-135">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="5331f-136">IESP:: Connect</span><span class="sxs-lookup"><span data-stu-id="5331f-136">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="5331f-137">IESP:: Stop</span><span class="sxs-lookup"><span data-stu-id="5331f-137">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




