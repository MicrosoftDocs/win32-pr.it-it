---
description: Il metodo GetControlState recupera lo stato dell'acquisizione, che indica se l'acquisizione viene eseguita o sospesa.
ms.assetid: ae0cf869-bf5b-4c23-a924-014554053c92
title: 'Metodo IRTC:: GetControlState (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d437d9463ed3225cd3a474e78220acf1f07af4bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880717"
---
# <a name="irtcgetcontrolstate-method"></a><span data-ttu-id="58e1e-103">Metodo IRTC:: GetControlState</span><span class="sxs-lookup"><span data-stu-id="58e1e-103">IRTC::GetControlState method</span></span>

<span data-ttu-id="58e1e-104">Il metodo **GetControlState** recupera lo stato dell' [*acquisizione*](c.md), che indica se l'acquisizione viene eseguita o sospesa.</span><span class="sxs-lookup"><span data-stu-id="58e1e-104">The **GetControlState** method retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="58e1e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58e1e-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a><span data-ttu-id="58e1e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="58e1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58e1e-107">*IsRunnning* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="58e1e-107">*IsRunnning* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58e1e-108">Indicatore dell'esecuzione dell'acquisizione corrente, incluso se l'acquisizione viene sospesa.</span><span class="sxs-lookup"><span data-stu-id="58e1e-108">Indicator that the current capture is running, including if the capture is paused.</span></span>

</dd> <dt>

<span data-ttu-id="58e1e-109">Con *sospensione* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="58e1e-109">*IsPaused* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58e1e-110">Indicatore dell'acquisizione corrente sospesa.</span><span class="sxs-lookup"><span data-stu-id="58e1e-110">Indicator that the current capture is paused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58e1e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58e1e-111">Return value</span></span>

<span data-ttu-id="58e1e-112">Se il metodo ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="58e1e-112">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="58e1e-113">Se il metodo ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="58e1e-113">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="58e1e-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="58e1e-114">Return code</span></span>                                                                                          | <span data-ttu-id="58e1e-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58e1e-115">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="58e1e-116"><dt>**NMERR \_ non \_ connesso**</dt></span><span class="sxs-lookup"><span data-stu-id="58e1e-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="58e1e-117">L'oggetto NPP non è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="58e1e-117">The NPP is not connected to the network.</span></span> <span data-ttu-id="58e1e-118">Chiamare [IRTC:: Connect](irtc-connect.md) per connettere l'oggetto NPP alla rete.</span><span class="sxs-lookup"><span data-stu-id="58e1e-118">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="58e1e-119"><dt>**NMERR \_ non in \_ tempo reale**</dt></span><span class="sxs-lookup"><span data-stu-id="58e1e-119"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="58e1e-120">L'oggetto NPP è connesso alla rete, ma non con il metodo [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="58e1e-120">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="58e1e-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="58e1e-121">Remarks</span></span>

<span data-ttu-id="58e1e-122">Questo metodo può essere chiamato ogni volta che l'oggetto NPP è connesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="58e1e-122">This method can be called any time the NPP is connected to the network.</span></span> <span data-ttu-id="58e1e-123">È possibile utilizzare questo metodo per determinare se un'acquisizione è in esecuzione, se l'acquisizione viene sospesa o se l'acquisizione è stata arrestata, ma l'oggetto NPP è ancora connesso.</span><span class="sxs-lookup"><span data-stu-id="58e1e-123">You can use this method to find out if a capture is running, if the capture is paused, or if the capture has been stopped but the NPP is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="58e1e-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58e1e-124">Requirements</span></span>



| <span data-ttu-id="58e1e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="58e1e-125">Requirement</span></span> | <span data-ttu-id="58e1e-126">Valore</span><span class="sxs-lookup"><span data-stu-id="58e1e-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58e1e-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58e1e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="58e1e-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="58e1e-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="58e1e-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58e1e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="58e1e-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="58e1e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="58e1e-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58e1e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="58e1e-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="58e1e-132"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="58e1e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="58e1e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58e1e-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58e1e-134"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58e1e-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58e1e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e1e-136">IRTC</span><span class="sxs-lookup"><span data-stu-id="58e1e-136">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="58e1e-137">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="58e1e-137">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="58e1e-138">IRTC::P ause</span><span class="sxs-lookup"><span data-stu-id="58e1e-138">IRTC::Pause</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="58e1e-139">IRTC:: Start</span><span class="sxs-lookup"><span data-stu-id="58e1e-139">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="58e1e-140">IRTC:: Stop</span><span class="sxs-lookup"><span data-stu-id="58e1e-140">IRTC::Stop</span></span>](irtc-stop.md)
</dt> </dl>

 

 




