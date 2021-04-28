---
description: 'Metodo IESP::D isconnect: il metodo Disconnect disconnette il NPP dalla rete.'
ms.assetid: 962e033d-a51c-47a2-83dc-cee1e7150ab8
title: Metodo IESP::D isconnect (Netmon.h)
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
ms.openlocfilehash: d0a07748781a567c889e879e2e99462d8cfb876a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110759"
---
# <a name="iespdisconnect-method"></a><span data-ttu-id="a9166-103">Metodo IESP::D isconnect</span><span class="sxs-lookup"><span data-stu-id="a9166-103">IESP::Disconnect method</span></span>

<span data-ttu-id="a9166-104">Il **metodo Disconnect** disconnette il NPP dalla rete.</span><span class="sxs-lookup"><span data-stu-id="a9166-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9166-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9166-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="a9166-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9166-106">Parameters</span></span>

<span data-ttu-id="a9166-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a9166-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9166-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9166-108">Return value</span></span>

<span data-ttu-id="a9166-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="a9166-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a9166-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="a9166-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="a9166-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a9166-111">Return code</span></span>                                                                                          | <span data-ttu-id="a9166-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9166-112">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a9166-113"><dt>**ACQUISIZIONE DI \_ NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="a9166-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="a9166-114">Il NPP acquisisce i dati.</span><span class="sxs-lookup"><span data-stu-id="a9166-114">The NPP is capturing data.</span></span> <span data-ttu-id="a9166-115">Non è possibile disconnettersi dalla rete mentre è in corso l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="a9166-115">You cannot disconnect from the network while data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="a9166-116"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="a9166-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="a9166-117">Il NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="a9166-117">The NPP is not connected to the network.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="a9166-118"><dt>**NMERR \_ NON \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="a9166-118"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="a9166-119">Il NPP è connesso alla rete, ma non con il [metodo IESP::Connect.](iesp-connect.md)</span><span class="sxs-lookup"><span data-stu-id="a9166-119">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="a9166-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9166-120">Remarks</span></span>

<span data-ttu-id="a9166-121">Questo metodo non può essere chiamato quando il NPP acquisisce dati.</span><span class="sxs-lookup"><span data-stu-id="a9166-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="a9166-122">È necessario chiamare il **metodo IESP::Stop** prima di chiamare **IESP::D isconnect.**</span><span class="sxs-lookup"><span data-stu-id="a9166-122">You must call the **IESP::Stop** method before calling **IESP::Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9166-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9166-123">Requirements</span></span>



| <span data-ttu-id="a9166-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9166-124">Requirement</span></span> | <span data-ttu-id="a9166-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a9166-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9166-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9166-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a9166-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9166-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="a9166-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9166-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a9166-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9166-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="a9166-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9166-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9166-131"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="a9166-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="a9166-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a9166-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9166-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9166-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9166-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9166-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9166-135">IESP</span><span class="sxs-lookup"><span data-stu-id="a9166-135">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="a9166-136">IESP::Connect</span><span class="sxs-lookup"><span data-stu-id="a9166-136">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="a9166-137">IESP::Stop</span><span class="sxs-lookup"><span data-stu-id="a9166-137">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




