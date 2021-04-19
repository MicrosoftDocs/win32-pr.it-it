---
description: Il \_ metodo Get BandwidthModifier ottiene il modificatore della larghezza di banda, ovvero una singola parola alfanumerica che fornisce il significato della figura della larghezza di banda. I due modificatori definiti sono CT (Total Conference) e AS (valore massimo specifico dell'applicazione).
ms.assetid: 29bf137d-e88b-437f-8bf1-824e335d47a1
title: 'Metodo ITConnection:: get_BandwidthModifier (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e278edfbdc9ae56d89547c0bcf64f90fde77baf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326512"
---
# <a name="itconnectionget_bandwidthmodifier-method"></a><span data-ttu-id="0c671-104">Metodo ITConnection:: Get \_ BandwidthModifier</span><span class="sxs-lookup"><span data-stu-id="0c671-104">ITConnection::get\_BandwidthModifier method</span></span>

<span data-ttu-id="0c671-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0c671-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0c671-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="0c671-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0c671-107">Il metodo **get \_ BandwidthModifier** ottiene il modificatore della larghezza di banda, ovvero una singola parola alfanumerica che fornisce il significato della figura della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="0c671-107">The **get\_BandwidthModifier** method gets the bandwidth modifier, which is a single, alphanumeric word giving the meaning of the bandwidth figure.</span></span> <span data-ttu-id="0c671-108">I due modificatori definiti sono CT (Total Conference) e AS (valore massimo specifico dell'applicazione).</span><span class="sxs-lookup"><span data-stu-id="0c671-108">The two modifiers defined are CT (Conference Total) and AS (Application Specific Maximum).</span></span>

## <a name="syntax"></a><span data-ttu-id="0c671-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c671-109">Syntax</span></span>


```C++
HRESULT get_BandwidthModifier(
  [out] BSTR *ppModifier
);
```



## <a name="parameters"></a><span data-ttu-id="0c671-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c671-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c671-111">*ppModifier* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0c671-111">*ppModifier* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c671-112">Puntatore a un **BSTR** che contiene il modificatore della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="0c671-112">Pointer to a **BSTR** containing the bandwidth modifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c671-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c671-113">Return value</span></span>

<span data-ttu-id="0c671-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="0c671-114">This method can return one of these values.</span></span>



| <span data-ttu-id="0c671-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0c671-115">Return code</span></span>                                                                                   | <span data-ttu-id="0c671-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c671-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0c671-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0c671-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="0c671-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0c671-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0c671-120">Il parametro *ppModifier* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="0c671-120">The *ppModifier* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="0c671-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0c671-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="0c671-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="0c671-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="0c671-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="0c671-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0c671-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="0c671-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="0c671-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="0c671-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c671-127">Remarks</span></span>

<span data-ttu-id="0c671-128">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppModifier* .</span><span class="sxs-lookup"><span data-stu-id="0c671-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppModifier* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c671-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c671-129">Requirements</span></span>



| <span data-ttu-id="0c671-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c671-130">Requirement</span></span> | <span data-ttu-id="0c671-131">Valore</span><span class="sxs-lookup"><span data-stu-id="0c671-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c671-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="0c671-132">TAPI version</span></span><br/> | <span data-ttu-id="0c671-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="0c671-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0c671-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c671-134">Header</span></span><br/>       | <dl> <span data-ttu-id="0c671-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c671-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="0c671-136">Library</span></span><br/>      | <dl> <span data-ttu-id="0c671-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0c671-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0c671-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="0c671-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c671-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c671-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c671-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c671-141">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="0c671-141">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

