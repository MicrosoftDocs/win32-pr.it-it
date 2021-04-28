---
description: 'Metodo IDelaydC::D isconnect: il metodo Disconnect disconnette il NPP dalla rete.'
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: Metodo IDelaydC::D isconnect (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 967bd9674cb28363804b8c8af12c541bcb8675ff
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110809"
---
# <a name="idelaydcdisconnect-method"></a><span data-ttu-id="5a94b-103">Metodo IDelaydC::D isconnect</span><span class="sxs-lookup"><span data-stu-id="5a94b-103">IDelaydC::Disconnect method</span></span>

<span data-ttu-id="5a94b-104">Il **metodo Disconnect** disconnette il NPP dalla rete.</span><span class="sxs-lookup"><span data-stu-id="5a94b-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a94b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a94b-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="5a94b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a94b-106">Parameters</span></span>

<span data-ttu-id="5a94b-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5a94b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5a94b-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a94b-108">Return value</span></span>

<span data-ttu-id="5a94b-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="5a94b-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5a94b-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="5a94b-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="5a94b-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5a94b-111">Return code</span></span>                                                                                          | <span data-ttu-id="5a94b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a94b-112">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a94b-113"><dt>**ACQUISIZIONE DI \_ NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="5a94b-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="5a94b-114">Il NPP acquisisce i dati.</span><span class="sxs-lookup"><span data-stu-id="5a94b-114">The NPP is capturing data.</span></span> <span data-ttu-id="5a94b-115">Non è possibile disconnettere il NPP dalla rete durante un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="5a94b-115">You cannot disconnect the NPP from the network during a capture.</span></span><br/>            |
| <dl> <span data-ttu-id="5a94b-116"><dt>**NMERR \_ NON \_ CONNESSO**</dt></span><span class="sxs-lookup"><span data-stu-id="5a94b-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5a94b-117">Il NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="5a94b-117">The NPP is not connected to the network.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="5a94b-118"><dt>**NMERR \_ NON \_ RITARDATO**</dt></span><span class="sxs-lookup"><span data-stu-id="5a94b-118"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="5a94b-119">Il NPP è connesso alla rete, ma non con il [metodo IDelaydC::Connect.](idelaydc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="5a94b-119">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5a94b-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a94b-120">Remarks</span></span>

<span data-ttu-id="5a94b-121">Questo metodo non può essere chiamato quando il NPP acquisisce dati.</span><span class="sxs-lookup"><span data-stu-id="5a94b-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="5a94b-122">È necessario chiamare il **metodo IDelaydC::Stop** prima di chiamare **Disconnect.**</span><span class="sxs-lookup"><span data-stu-id="5a94b-122">You must call the **IDelaydC::Stop** method before calling **Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a94b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a94b-123">Requirements</span></span>



| <span data-ttu-id="5a94b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a94b-124">Requirement</span></span> | <span data-ttu-id="5a94b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5a94b-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a94b-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a94b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5a94b-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5a94b-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="5a94b-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a94b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5a94b-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5a94b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="5a94b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a94b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a94b-131"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="5a94b-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="5a94b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5a94b-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a94b-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a94b-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a94b-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a94b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a94b-135">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="5a94b-135">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="5a94b-136">IDelaydC::Connect</span><span class="sxs-lookup"><span data-stu-id="5a94b-136">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="5a94b-137">IDelaydC::Stop</span><span class="sxs-lookup"><span data-stu-id="5a94b-137">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




