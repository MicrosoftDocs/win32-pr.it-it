---
description: Il metodo Disconnect disconnette l'oggetto NPP dalla rete.
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: 'IDelaydC: metodo:D di connessione (Netmon. h)'
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
ms.openlocfilehash: d192aa80f543706eea4bc197bc3dc8d57dd64aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128335"
---
# <a name="idelaydcdisconnect-method"></a><span data-ttu-id="3236f-103">IDelaydC::D metodo di connessione</span><span class="sxs-lookup"><span data-stu-id="3236f-103">IDelaydC::Disconnect method</span></span>

<span data-ttu-id="3236f-104">Il metodo **Disconnect** disconnette l'oggetto NPP dalla rete.</span><span class="sxs-lookup"><span data-stu-id="3236f-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="3236f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3236f-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="3236f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3236f-106">Parameters</span></span>

<span data-ttu-id="3236f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3236f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3236f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3236f-108">Return value</span></span>

<span data-ttu-id="3236f-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3236f-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3236f-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="3236f-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="3236f-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3236f-111">Return code</span></span>                                                                                          | <span data-ttu-id="3236f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3236f-112">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3236f-113"><dt>**\_acquisizione NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="3236f-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="3236f-114">L'oggetto NPP sta acquisendo i dati.</span><span class="sxs-lookup"><span data-stu-id="3236f-114">The NPP is capturing data.</span></span> <span data-ttu-id="3236f-115">Non è possibile disconnettere l'oggetto NPP dalla rete durante un'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="3236f-115">You cannot disconnect the NPP from the network during a capture.</span></span><br/>            |
| <dl> <span data-ttu-id="3236f-116"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="3236f-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="3236f-117">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="3236f-117">The NPP is not connected to the network.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="3236f-118"><dt>**NMERR \_ non \_ ritardato**</dt></span><span class="sxs-lookup"><span data-stu-id="3236f-118"><dt>**NMERR\_NOT\_DELAYED**</dt></span></span> </dl>   | <span data-ttu-id="3236f-119">L'oggetto NPP è connesso alla rete, ma non con il metodo [IDelaydC:: Connect](idelaydc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="3236f-119">The NPP is connected to the network but not with the [IDelaydC::Connect](idelaydc-connect.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3236f-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="3236f-120">Remarks</span></span>

<span data-ttu-id="3236f-121">Questo metodo non può essere chiamato quando l'oggetto NPP sta acquisendo i dati.</span><span class="sxs-lookup"><span data-stu-id="3236f-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="3236f-122">Prima di chiamare **Disconnect**, è necessario chiamare il metodo **IDelaydC:: Stop** .</span><span class="sxs-lookup"><span data-stu-id="3236f-122">You must call the **IDelaydC::Stop** method before calling **Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3236f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3236f-123">Requirements</span></span>



| <span data-ttu-id="3236f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3236f-124">Requirement</span></span> | <span data-ttu-id="3236f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3236f-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3236f-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3236f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3236f-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3236f-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="3236f-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3236f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3236f-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3236f-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="3236f-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3236f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3236f-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3236f-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="3236f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3236f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3236f-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3236f-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3236f-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3236f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3236f-135">IDelaydC</span><span class="sxs-lookup"><span data-stu-id="3236f-135">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="3236f-136">IDelaydC:: Connect</span><span class="sxs-lookup"><span data-stu-id="3236f-136">IDelaydC::Connect</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="3236f-137">IDelaydC:: Stop</span><span class="sxs-lookup"><span data-stu-id="3236f-137">IDelaydC::Stop</span></span>](idelaydc-stop.md)
</dt> </dl>

 

 




