---
description: Il metodo Disconnect disconnette l'oggetto NPP dalla rete.
ms.assetid: 47a0cce0-a50d-4bad-9787-672cc3d13d07
title: 'IRTC: metodo:D di connessione (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: df58d6ac0e61ecc370510474c3bc067726d9824b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226966"
---
# <a name="irtcdisconnect-method"></a><span data-ttu-id="dc208-103">IRTC::D metodo di connessione</span><span class="sxs-lookup"><span data-stu-id="dc208-103">IRTC::Disconnect method</span></span>

<span data-ttu-id="dc208-104">Il metodo **Disconnect** disconnette l'oggetto NPP dalla rete.</span><span class="sxs-lookup"><span data-stu-id="dc208-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc208-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc208-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="dc208-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc208-106">Parameters</span></span>

<span data-ttu-id="dc208-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="dc208-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dc208-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc208-108">Return value</span></span>

<span data-ttu-id="dc208-109">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="dc208-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="dc208-110">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="dc208-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="dc208-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="dc208-111">Return code</span></span>                                                                                          | <span data-ttu-id="dc208-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc208-112">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dc208-113"><dt>**\_acquisizione NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="dc208-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="dc208-114">L'oggetto NPP sta acquisendo i dati.</span><span class="sxs-lookup"><span data-stu-id="dc208-114">The NPP is capturing data.</span></span> <span data-ttu-id="dc208-115">Non è possibile disconnettersi dalla rete mentre è in corso l'acquisizione dei dati.</span><span class="sxs-lookup"><span data-stu-id="dc208-115">You cannot disconnect from the network while the data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="dc208-116"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="dc208-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="dc208-117">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="dc208-117">The NPP is not connected to the network.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="dc208-118"><dt>**NMERR \_ non in \_ tempo reale**</dt></span><span class="sxs-lookup"><span data-stu-id="dc208-118"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="dc208-119">L'oggetto NPP è connesso alla rete, ma non con il metodo [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="dc208-119">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="dc208-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc208-120">Remarks</span></span>

<span data-ttu-id="dc208-121">Questo metodo non può essere chiamato quando l'oggetto NPP sta acquisendo i dati.</span><span class="sxs-lookup"><span data-stu-id="dc208-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="dc208-122">È necessario chiamare il metodo [IRTC:: Stop](irtc-stop.md) prima di chiamare IRTC::D Disconnect.</span><span class="sxs-lookup"><span data-stu-id="dc208-122">You must call the [IRTC::Stop](irtc-stop.md) method before calling IRTC::Disconnect.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc208-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc208-123">Requirements</span></span>



| <span data-ttu-id="dc208-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc208-124">Requirement</span></span> | <span data-ttu-id="dc208-125">Valore</span><span class="sxs-lookup"><span data-stu-id="dc208-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc208-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc208-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dc208-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dc208-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="dc208-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc208-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dc208-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dc208-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="dc208-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc208-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc208-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc208-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="dc208-132">DLL</span><span class="sxs-lookup"><span data-stu-id="dc208-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc208-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc208-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc208-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc208-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc208-135">IRTC</span><span class="sxs-lookup"><span data-stu-id="dc208-135">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="dc208-136">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="dc208-136">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="dc208-137">IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="dc208-137">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




