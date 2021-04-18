---
description: Il \_ metodo Put originator imposta l'origine della conferenza.
ms.assetid: b70fc584-3536-4296-bc38-e20ff6630abc
title: 'ITSdp: metodo:p ut_Originator (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506554668e697e9281dc5dc15784fa36f7429d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323938"
---
# <a name="itsdpput_originator-method"></a><span data-ttu-id="db5ab-103">ITSdp: metodo di \_ origine ut:p</span><span class="sxs-lookup"><span data-stu-id="db5ab-103">ITSdp::put\_Originator method</span></span>

<span data-ttu-id="db5ab-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="db5ab-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="db5ab-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="db5ab-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="db5ab-106">Il metodo **put \_ originator** imposta l'origine della conferenza.</span><span class="sxs-lookup"><span data-stu-id="db5ab-106">The **put\_Originator** method sets the conference originator.</span></span>

## <a name="syntax"></a><span data-ttu-id="db5ab-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db5ab-107">Syntax</span></span>


```C++
HRESULT put_Originator(
  [in] BSTR pOriginator
);
```



## <a name="parameters"></a><span data-ttu-id="db5ab-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="db5ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db5ab-109">*pOriginator* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db5ab-109">*pOriginator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db5ab-110">Puntatore a una rappresentazione **BSTR** del creatore della conferenza.</span><span class="sxs-lookup"><span data-stu-id="db5ab-110">Pointer to a **BSTR** representation of the conference originator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db5ab-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db5ab-111">Return value</span></span>

<span data-ttu-id="db5ab-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="db5ab-112">This method can return one of these values.</span></span>



| <span data-ttu-id="db5ab-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="db5ab-113">Return code</span></span>                                                                                   | <span data-ttu-id="db5ab-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db5ab-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="db5ab-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="db5ab-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="db5ab-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="db5ab-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="db5ab-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="db5ab-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="db5ab-118">Il parametro *pOriginator* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="db5ab-118">The *pOriginator* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="db5ab-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="db5ab-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="db5ab-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="db5ab-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="db5ab-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="db5ab-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="db5ab-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="db5ab-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="db5ab-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="db5ab-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="db5ab-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="db5ab-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="db5ab-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="db5ab-125">Remarks</span></span>

<span data-ttu-id="db5ab-126">L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *POriginator* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="db5ab-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pOriginator* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="db5ab-127">Questa funzione può inviare dati in rete in forma non crittografata; Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="db5ab-127">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="db5ab-128">Il rischio di sicurezza di inviare i dati in testo non crittografato deve essere considerato prima di utilizzare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="db5ab-128">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="db5ab-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db5ab-129">Requirements</span></span>



| <span data-ttu-id="db5ab-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="db5ab-130">Requirement</span></span> | <span data-ttu-id="db5ab-131">Valore</span><span class="sxs-lookup"><span data-stu-id="db5ab-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db5ab-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="db5ab-132">TAPI version</span></span><br/> | <span data-ttu-id="db5ab-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="db5ab-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="db5ab-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db5ab-134">Header</span></span><br/>       | <dl> <span data-ttu-id="db5ab-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="db5ab-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="db5ab-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="db5ab-136">Library</span></span><br/>      | <dl> <span data-ttu-id="db5ab-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="db5ab-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="db5ab-138">DLL</span><span class="sxs-lookup"><span data-stu-id="db5ab-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="db5ab-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db5ab-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db5ab-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db5ab-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db5ab-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="db5ab-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="db5ab-142">**ITSdp:: Get \_ originator**</span><span class="sxs-lookup"><span data-stu-id="db5ab-142">**ITSdp::get\_Originator**</span></span>](itsdp-get-originator.md)
</dt> </dl>

 

