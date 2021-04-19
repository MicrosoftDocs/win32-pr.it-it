---
description: Il \_ metodo Put SessionVersion imposta la versione della sessione.
ms.assetid: 8984d608-0fad-4979-9c58-ac2fb7926796
title: 'ITSdp: metodo:p ut_SessionVersion (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a096117f894a2ff33f127c683b84ba50e88308e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332820"
---
# <a name="itsdpput_sessionversion-method"></a><span data-ttu-id="c4717-103">ITSdp::p UT \_ SessionVersion metodo</span><span class="sxs-lookup"><span data-stu-id="c4717-103">ITSdp::put\_SessionVersion method</span></span>

<span data-ttu-id="c4717-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c4717-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c4717-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="c4717-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c4717-106">Il metodo **put \_ SessionVersion** imposta la versione della sessione.</span><span class="sxs-lookup"><span data-stu-id="c4717-106">The **put\_SessionVersion** method sets the session version.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4717-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4717-107">Syntax</span></span>


```C++
HRESULT put_SessionVersion(
  [in] DOUBLE SessionVersion
);
```



## <a name="parameters"></a><span data-ttu-id="c4717-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4717-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4717-109">*SessionVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4717-109">*SessionVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4717-110">Valore della versione della sessione.</span><span class="sxs-lookup"><span data-stu-id="c4717-110">Session version value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4717-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4717-111">Return value</span></span>

<span data-ttu-id="c4717-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="c4717-112">This method can return one of these values.</span></span>



| <span data-ttu-id="c4717-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c4717-113">Return code</span></span>                                                                                   | <span data-ttu-id="c4717-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4717-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="c4717-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c4717-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c4717-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="c4717-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c4717-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c4717-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c4717-118">Il parametro *SessionVersion* non è valido.</span><span class="sxs-lookup"><span data-stu-id="c4717-118">The *SessionVersion* parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="c4717-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="c4717-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c4717-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="c4717-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c4717-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="c4717-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="c4717-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="c4717-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c4717-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="c4717-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="c4717-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="c4717-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="c4717-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4717-125">Remarks</span></span>

<span data-ttu-id="c4717-126">Il valore restituito di questo metodo potrebbe essere **ULONG**, ma Visual Basic non supporta il tipo **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="c4717-126">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="c4717-127">Un **Double** è il tipo più piccolo successivo che comprende l'intero intervallo di valori necessari.</span><span class="sxs-lookup"><span data-stu-id="c4717-127">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

<span data-ttu-id="c4717-128">Questa funzione può inviare dati in rete in forma non crittografata; Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="c4717-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="c4717-129">Il rischio di sicurezza di inviare i dati in testo non crittografato deve essere considerato prima di utilizzare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="c4717-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4717-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4717-130">Requirements</span></span>



| <span data-ttu-id="c4717-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4717-131">Requirement</span></span> | <span data-ttu-id="c4717-132">Valore</span><span class="sxs-lookup"><span data-stu-id="c4717-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4717-133">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="c4717-133">TAPI version</span></span><br/> | <span data-ttu-id="c4717-134">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c4717-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c4717-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4717-135">Header</span></span><br/>       | <dl> <span data-ttu-id="c4717-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4717-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4717-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4717-137">Library</span></span><br/>      | <dl> <span data-ttu-id="c4717-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4717-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c4717-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c4717-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="c4717-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4717-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4717-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4717-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4717-142">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="c4717-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="c4717-143">**ITSdp:: Get \_ SessionVersion**</span><span class="sxs-lookup"><span data-stu-id="c4717-143">**ITSdp::get\_SessionVersion**</span></span>](itsdp-get-sessionversion.md)
</dt> </dl>

 

 




