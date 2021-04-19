---
description: Il \_ metodo Put MachineAddress imposta l'indirizzo del computer dell'host di origine.
ms.assetid: f4af55b1-e20b-4fe8-a15e-a1a68d22f1b9
title: 'ITSdp: metodo:p ut_MachineAddress (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec09d41cb7735383f08ce8c8983331165c54fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332726"
---
# <a name="itsdpput_machineaddress-method"></a><span data-ttu-id="eecab-103">ITSdp::p UT \_ MachineAddress metodo</span><span class="sxs-lookup"><span data-stu-id="eecab-103">ITSdp::put\_MachineAddress method</span></span>

<span data-ttu-id="eecab-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eecab-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="eecab-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="eecab-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="eecab-106">Il metodo **put \_ MachineAddress** imposta l'indirizzo del computer dell'host di origine.</span><span class="sxs-lookup"><span data-stu-id="eecab-106">The **put\_MachineAddress** method sets the machine address of the originating host.</span></span>

## <a name="syntax"></a><span data-ttu-id="eecab-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eecab-107">Syntax</span></span>


```C++
HRESULT put_MachineAddress(
  [in] BSTR pMachineAddress
);
```



## <a name="parameters"></a><span data-ttu-id="eecab-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="eecab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eecab-109">*pMachineAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eecab-109">*pMachineAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eecab-110">Puntatore a un **BSTR** che contiene l'indirizzo del computer dell'host della conferenza.</span><span class="sxs-lookup"><span data-stu-id="eecab-110">Pointer to a **BSTR** containing the machine address of the conference host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eecab-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eecab-111">Return value</span></span>

<span data-ttu-id="eecab-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="eecab-112">This method can return one of these values.</span></span>



| <span data-ttu-id="eecab-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="eecab-113">Return code</span></span>                                                                                   | <span data-ttu-id="eecab-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eecab-114">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="eecab-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="eecab-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="eecab-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="eecab-116">Method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="eecab-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="eecab-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="eecab-118">Il parametro *pMachineAddress* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="eecab-118">The *pMachineAddress* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="eecab-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="eecab-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="eecab-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="eecab-120">Insufficient memory exists to perform the operation.</span></span><br/>    |
| <dl> <span data-ttu-id="eecab-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="eecab-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="eecab-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="eecab-122">Unspecified error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="eecab-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="eecab-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="eecab-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="eecab-124">This method is not yet implemented.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="eecab-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="eecab-125">Remarks</span></span>

<span data-ttu-id="eecab-126">L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PMachineAddress* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="eecab-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMachineAddress* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="eecab-127">Il parametro *pMachineAddress* può essere un nome DNS ("johnsmith.workinghard.Microsoft.com") o un indirizzo IP ("10.111.222.111").</span><span class="sxs-lookup"><span data-stu-id="eecab-127">The *pMachineAddress* parameter can be either a DNS name ("JohnSmith.workinghard.microsoft.com") or an IP address ("10.111.222.111").</span></span>

<span data-ttu-id="eecab-128">Questa funzione può inviare dati in rete in forma non crittografata; Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="eecab-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="eecab-129">Il rischio di sicurezza di inviare i dati in testo non crittografato deve essere considerato prima di utilizzare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="eecab-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eecab-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eecab-130">Requirements</span></span>



| <span data-ttu-id="eecab-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="eecab-131">Requirement</span></span> | <span data-ttu-id="eecab-132">Valore</span><span class="sxs-lookup"><span data-stu-id="eecab-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eecab-133">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="eecab-133">TAPI version</span></span><br/> | <span data-ttu-id="eecab-134">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="eecab-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="eecab-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eecab-135">Header</span></span><br/>       | <dl> <span data-ttu-id="eecab-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="eecab-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="eecab-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="eecab-137">Library</span></span><br/>      | <dl> <span data-ttu-id="eecab-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eecab-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="eecab-139">DLL</span><span class="sxs-lookup"><span data-stu-id="eecab-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="eecab-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eecab-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eecab-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eecab-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eecab-142">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="eecab-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="eecab-143">**ITSdp:: Get \_ MachineAddress**</span><span class="sxs-lookup"><span data-stu-id="eecab-143">**ITSdp::get\_MachineAddress**</span></span>](itsdp-get-machineaddress.md)
</dt> </dl>

 

