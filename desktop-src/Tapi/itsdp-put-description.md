---
description: Il \_ metodo Put Description imposta la descrizione della sessione.
ms.assetid: 535957e7-effe-4b1b-8cba-38a7a3fe9a9a
title: 'ITSdp: metodo:p ut_Description (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea8799ce9b2b8f3f44147b8ca60a92d2c37d5e87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332821"
---
# <a name="itsdpput_description-method"></a><span data-ttu-id="67c68-103">ITSdp::p \_ metodo di descrizione ut</span><span class="sxs-lookup"><span data-stu-id="67c68-103">ITSdp::put\_Description method</span></span>

<span data-ttu-id="67c68-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="67c68-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="67c68-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="67c68-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="67c68-106">Il metodo **put \_ Description** imposta la descrizione della sessione.</span><span class="sxs-lookup"><span data-stu-id="67c68-106">The **put\_Description** method sets the session description.</span></span>

## <a name="syntax"></a><span data-ttu-id="67c68-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67c68-107">Syntax</span></span>


```C++
HRESULT put_Description(
  [in] BSTR pDescription
);
```



## <a name="parameters"></a><span data-ttu-id="67c68-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="67c68-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67c68-109">*pDescription* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67c68-109">*pDescription* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67c68-110">Puntatore a un **BSTR** che contiene la descrizione della sessione.</span><span class="sxs-lookup"><span data-stu-id="67c68-110">Pointer to a **BSTR** containing the session description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67c68-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67c68-111">Return value</span></span>

<span data-ttu-id="67c68-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="67c68-112">This method can return one of these values.</span></span>



| <span data-ttu-id="67c68-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="67c68-113">Return code</span></span>                                                                                   | <span data-ttu-id="67c68-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67c68-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="67c68-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="67c68-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="67c68-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="67c68-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="67c68-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="67c68-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="67c68-118">Il parametro *pDescription* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="67c68-118">The *pDescription* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="67c68-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="67c68-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="67c68-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="67c68-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="67c68-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="67c68-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="67c68-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="67c68-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="67c68-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="67c68-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="67c68-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="67c68-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="67c68-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="67c68-125">Remarks</span></span>

<span data-ttu-id="67c68-126">L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PDescription* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="67c68-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pDescription* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="67c68-127">Questa funzione può inviare dati in rete in forma non crittografata; Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="67c68-127">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="67c68-128">Il rischio di sicurezza di inviare i dati in testo non crittografato deve essere considerato prima di utilizzare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="67c68-128">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="67c68-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67c68-129">Requirements</span></span>



| <span data-ttu-id="67c68-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="67c68-130">Requirement</span></span> | <span data-ttu-id="67c68-131">Valore</span><span class="sxs-lookup"><span data-stu-id="67c68-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="67c68-132">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="67c68-132">TAPI version</span></span><br/> | <span data-ttu-id="67c68-133">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="67c68-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="67c68-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67c68-134">Header</span></span><br/>       | <dl> <span data-ttu-id="67c68-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="67c68-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="67c68-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="67c68-136">Library</span></span><br/>      | <dl> <span data-ttu-id="67c68-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67c68-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="67c68-138">DLL</span><span class="sxs-lookup"><span data-stu-id="67c68-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="67c68-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67c68-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67c68-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67c68-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c68-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="67c68-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="67c68-142">**Descrizione di ITSdp:: Get \_**</span><span class="sxs-lookup"><span data-stu-id="67c68-142">**ITSdp::get\_Description**</span></span>](itsdp-get-description.md)
</dt> </dl>

 

