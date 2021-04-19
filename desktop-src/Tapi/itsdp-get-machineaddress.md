---
description: Il \_ metodo Get MachineAddress Ottiene l'indirizzo del computer dell'host di origine.
ms.assetid: 8a67cc9f-f9fc-4ec3-86f9-ffe34d075830
title: 'Metodo ITSdp:: get_MachineAddress (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34968efa16f04cba8f99dbc0dc42b0cf4995a43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326489"
---
# <a name="itsdpget_machineaddress-method"></a><span data-ttu-id="e0108-103">Metodo ITSdp:: Get \_ MachineAddress</span><span class="sxs-lookup"><span data-stu-id="e0108-103">ITSdp::get\_MachineAddress method</span></span>

<span data-ttu-id="e0108-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e0108-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e0108-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="e0108-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e0108-106">Il metodo **get \_ MachineAddress** Ottiene l'indirizzo del computer dell'host di origine.</span><span class="sxs-lookup"><span data-stu-id="e0108-106">The **get\_MachineAddress** method gets the machine address of the originating host.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0108-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0108-107">Syntax</span></span>


```C++
HRESULT get_MachineAddress(
  [out] BSTR *ppMachineAddress
);
```



## <a name="parameters"></a><span data-ttu-id="e0108-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0108-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0108-109">*ppMachineAddress* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e0108-109">*ppMachineAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0108-110">Puntatore a un **BSTR** che contiene l'indirizzo del computer dell'host della conferenza.</span><span class="sxs-lookup"><span data-stu-id="e0108-110">Pointer to a **BSTR** containing the machine address of the conference host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0108-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0108-111">Return value</span></span>

<span data-ttu-id="e0108-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="e0108-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e0108-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e0108-113">Return code</span></span>                                                                                   | <span data-ttu-id="e0108-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0108-114">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0108-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e0108-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e0108-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="e0108-116">Method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="e0108-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="e0108-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e0108-118">Il parametro *ppMachineAddres* s non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="e0108-118">The *ppMachineAddres* s parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="e0108-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="e0108-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e0108-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e0108-120">Insufficient memory exists to perform the operation.</span></span><br/>     |
| <dl> <span data-ttu-id="e0108-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="e0108-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="e0108-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="e0108-122">Unspecified error.</span></span><br/>                                       |
| <dl> <span data-ttu-id="e0108-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="e0108-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="e0108-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="e0108-124">This method is not yet implemented.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="e0108-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0108-125">Remarks</span></span>

<span data-ttu-id="e0108-126">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppMachineAddress* .</span><span class="sxs-lookup"><span data-stu-id="e0108-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMachineAddress* parameter.</span></span>

<span data-ttu-id="e0108-127">Il parametro *ppMachineAddress* può essere restituito come nome DNS ("johnsmith.workinghard.Microsoft.com") o come indirizzo IP ("10.111.222.111").</span><span class="sxs-lookup"><span data-stu-id="e0108-127">The *ppMachineAddress* parameter can be returned as either a DNS name ("JohnSmith.workinghard.microsoft.com") or an IP address ("10.111.222.111").</span></span>

## <a name="requirements"></a><span data-ttu-id="e0108-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0108-128">Requirements</span></span>



| <span data-ttu-id="e0108-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0108-129">Requirement</span></span> | <span data-ttu-id="e0108-130">Valore</span><span class="sxs-lookup"><span data-stu-id="e0108-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0108-131">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="e0108-131">TAPI version</span></span><br/> | <span data-ttu-id="e0108-132">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e0108-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e0108-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0108-133">Header</span></span><br/>       | <dl> <span data-ttu-id="e0108-134"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0108-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0108-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="e0108-135">Library</span></span><br/>      | <dl> <span data-ttu-id="e0108-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e0108-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e0108-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e0108-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="e0108-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0108-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0108-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0108-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0108-140">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="e0108-140">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="e0108-141">**ITSdp::p UT \_ MachineAddress**</span><span class="sxs-lookup"><span data-stu-id="e0108-141">**ITSdp::put\_MachineAddress**</span></span>](itsdp-put-machineaddress.md)
</dt> </dl>

 

