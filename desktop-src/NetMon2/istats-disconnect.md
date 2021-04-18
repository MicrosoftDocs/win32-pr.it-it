---
description: Disconnette l'oggetto NPP dalla rete.
ms.assetid: 01ff8fc2-aa27-4df8-a499-c7b00c1fa2e8
title: IStats::D metodo di connessione (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a5fa56c05036380b5dba42089979b43d776a4b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315461"
---
# <a name="istatsdisconnect-method"></a><span data-ttu-id="1a19e-103">IStats::D metodo di connessione</span><span class="sxs-lookup"><span data-stu-id="1a19e-103">IStats::Disconnect method</span></span>

<span data-ttu-id="1a19e-104">Il metodo **Disconnect** disconnette l'oggetto NPP dalla rete.</span><span class="sxs-lookup"><span data-stu-id="1a19e-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a19e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a19e-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="1a19e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a19e-106">Parameters</span></span>

<span data-ttu-id="1a19e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="1a19e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a19e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a19e-108">Return value</span></span>

<span data-ttu-id="1a19e-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1a19e-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1a19e-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="1a19e-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="1a19e-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1a19e-111">Return code</span></span>                                                                                            | <span data-ttu-id="1a19e-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a19e-112">Description</span></span>                                                                                                                 |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1a19e-113"><dt>**\_acquisizione NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="1a19e-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>        | <span data-ttu-id="1a19e-114">Il NPP sta attualmente acquisendo i dati.</span><span class="sxs-lookup"><span data-stu-id="1a19e-114">The NPP is currently capturing data.</span></span> <span data-ttu-id="1a19e-115">Non è possibile disconnettersi dalla rete mentre è in corso un'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="1a19e-115">You cannot disconnect from the network while a data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="1a19e-116"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="1a19e-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="1a19e-117">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="1a19e-117">The NPP is not connected to the network.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="1a19e-118"><dt>**NMERR \_ non \_ \_ solo statistiche**</dt></span><span class="sxs-lookup"><span data-stu-id="1a19e-118"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="1a19e-119">L'oggetto NPP è connesso alla rete, ma non con il metodo [**IStats:: Connect**](istats-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="1a19e-119">The NPP is connected to the network, but not with the [**IStats::Connect**](istats-connect.md) method.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="1a19e-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a19e-120">Remarks</span></span>

<span data-ttu-id="1a19e-121">Questo metodo non può essere chiamato quando l'oggetto NPP sta acquisendo i dati.</span><span class="sxs-lookup"><span data-stu-id="1a19e-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="1a19e-122">Chiamare il metodo **IStats::D** prima la connessione e quindi chiamare [**IStats:: Stop**](istats-stop.md).</span><span class="sxs-lookup"><span data-stu-id="1a19e-122">Call the **IStats::Disconnect** method first and then call [**IStats::Stop**](istats-stop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a19e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a19e-123">Requirements</span></span>



| <span data-ttu-id="1a19e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a19e-124">Requirement</span></span> | <span data-ttu-id="1a19e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="1a19e-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a19e-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a19e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1a19e-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1a19e-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="1a19e-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1a19e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1a19e-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1a19e-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="1a19e-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1a19e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a19e-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a19e-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="1a19e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1a19e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a19e-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a19e-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a19e-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a19e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a19e-135">**IStats**</span><span class="sxs-lookup"><span data-stu-id="1a19e-135">**IStats**</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="1a19e-136">**IStats:: Connect**</span><span class="sxs-lookup"><span data-stu-id="1a19e-136">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="1a19e-137">**IStats:: Stop**</span><span class="sxs-lookup"><span data-stu-id="1a19e-137">**IStats::Stop**</span></span>](istats-stop.md)
</dt> </dl>

 

 




