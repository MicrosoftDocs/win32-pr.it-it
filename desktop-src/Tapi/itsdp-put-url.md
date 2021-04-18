---
description: Il \_ metodo Put URL imposta l'URL.
ms.assetid: 538bb1dd-c7ad-446d-9df7-23363b466263
title: 'ITSdp: metodo:p ut_Url (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b791d18b97851e6b0b27a4ba26d1dfdbce7dbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329327"
---
# <a name="itsdpput_url-method"></a><span data-ttu-id="70c50-103">ITSdp: \_ metodo URL ut:p</span><span class="sxs-lookup"><span data-stu-id="70c50-103">ITSdp::put\_Url method</span></span>

<span data-ttu-id="70c50-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="70c50-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="70c50-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="70c50-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="70c50-106">Il metodo **put \_ URL** imposta l'URL.</span><span class="sxs-lookup"><span data-stu-id="70c50-106">The **put\_Url** method sets the URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="70c50-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70c50-107">Syntax</span></span>


```C++
HRESULT put_Url(
  [in] BSTR pUrl
);
```



## <a name="parameters"></a><span data-ttu-id="70c50-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="70c50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70c50-109">*rovescio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="70c50-109">*pUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70c50-110">Puntatore a una rappresentazione **BSTR** dell'URL.</span><span class="sxs-lookup"><span data-stu-id="70c50-110">Pointer to a **BSTR** representation of the URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70c50-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="70c50-111">Return value</span></span>

<span data-ttu-id="70c50-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="70c50-112">This method can return one of these values.</span></span>



| <span data-ttu-id="70c50-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="70c50-113">Return code</span></span>                                                                                   | <span data-ttu-id="70c50-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70c50-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="70c50-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="70c50-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="70c50-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="70c50-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="70c50-117"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="70c50-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="70c50-118">Il parametro *rovescio* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="70c50-118">The *pUrl* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="70c50-119"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="70c50-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="70c50-120">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="70c50-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="70c50-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="70c50-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="70c50-122">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="70c50-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="70c50-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="70c50-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="70c50-124">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="70c50-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="70c50-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="70c50-125">Remarks</span></span>

<span data-ttu-id="70c50-126">L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *rovescio* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="70c50-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pUrl* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="70c50-127">Un URL viene in genere usato per fare riferimento a una pagina Web contenente risorse aggiuntive o informazioni complementari su una conferenza.</span><span class="sxs-lookup"><span data-stu-id="70c50-127">An URL is typically used to reference a Web page containing additional resources or background information about a conference.</span></span>

<span data-ttu-id="70c50-128">Questa funzione può inviare dati in rete in forma non crittografata; Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="70c50-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="70c50-129">Il rischio di sicurezza di inviare i dati in testo non crittografato deve essere considerato prima di utilizzare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="70c50-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="70c50-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70c50-130">Requirements</span></span>



| <span data-ttu-id="70c50-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="70c50-131">Requirement</span></span> | <span data-ttu-id="70c50-132">Valore</span><span class="sxs-lookup"><span data-stu-id="70c50-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70c50-133">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="70c50-133">TAPI version</span></span><br/> | <span data-ttu-id="70c50-134">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="70c50-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="70c50-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70c50-135">Header</span></span><br/>       | <dl> <span data-ttu-id="70c50-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="70c50-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="70c50-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="70c50-137">Library</span></span><br/>      | <dl> <span data-ttu-id="70c50-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70c50-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="70c50-139">DLL</span><span class="sxs-lookup"><span data-stu-id="70c50-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="70c50-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70c50-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70c50-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="70c50-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70c50-142">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="70c50-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="70c50-143">**URL di ITSdp:: Get \_**</span><span class="sxs-lookup"><span data-stu-id="70c50-143">**ITSdp::get\_Url**</span></span>](itsdp-get-url.md)
</dt> </dl>

 

