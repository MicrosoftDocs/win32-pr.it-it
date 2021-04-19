---
description: Il \_ metodo Put MEDIANAME imposta il nome del supporto. I supporti definiti sono audio, video, lavagna, testo e dati.
ms.assetid: 0dd18add-6c7e-40a8-8b39-10c65bdfb2e0
title: 'ITMedia: metodo:p ut_MediaName (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66dcbd4e29f59694d610fb4e6af9fd49aa53323d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326626"
---
# <a name="itmediaput_medianame-method"></a><span data-ttu-id="0e429-104">ITMedia::p UT \_ MEDIANAME Method</span><span class="sxs-lookup"><span data-stu-id="0e429-104">ITMedia::put\_MediaName method</span></span>

<span data-ttu-id="0e429-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0e429-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0e429-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="0e429-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0e429-107">Il metodo **put \_ MEDIANAME** imposta il nome del supporto.</span><span class="sxs-lookup"><span data-stu-id="0e429-107">The **put\_MediaName** method sets the media name.</span></span> <span data-ttu-id="0e429-108">I supporti definiti sono audio, video, lavagna, testo e dati.</span><span class="sxs-lookup"><span data-stu-id="0e429-108">Defined media are audio, video, whiteboard, text, and data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e429-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e429-109">Syntax</span></span>


```C++
HRESULT put_MediaName(
  [in] BSTR pMediaName
);
```



## <a name="parameters"></a><span data-ttu-id="0e429-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e429-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e429-111">*pMediaName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0e429-111">*pMediaName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e429-112">Puntatore a un **BSTR** che contiene il nome del supporto da impostare.</span><span class="sxs-lookup"><span data-stu-id="0e429-112">Pointer to a **BSTR** containing the media name to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e429-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e429-113">Return value</span></span>

<span data-ttu-id="0e429-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="0e429-114">This method can return one of these values.</span></span>



| <span data-ttu-id="0e429-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0e429-115">Return code</span></span>                                                                                   | <span data-ttu-id="0e429-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e429-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0e429-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0e429-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0e429-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="0e429-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0e429-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="0e429-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0e429-120">Il parametro *pMediaName* non è un puntatore valido.</span><span class="sxs-lookup"><span data-stu-id="0e429-120">The *pMediaName* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="0e429-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="0e429-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0e429-122">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="0e429-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="0e429-123"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="0e429-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="0e429-124">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="0e429-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0e429-125"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="0e429-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="0e429-126">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="0e429-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="0e429-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e429-127">Remarks</span></span>

<span data-ttu-id="0e429-128">L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PMediaName* e usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="0e429-128">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMediaName* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="0e429-129">Questa funzione può inviare dati in rete in forma non crittografata; Pertanto, un utente che intercetta la rete potrebbe essere in grado di leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="0e429-129">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="0e429-130">Il rischio di sicurezza di inviare i dati in testo non crittografato deve essere considerato prima di utilizzare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="0e429-130">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e429-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e429-131">Requirements</span></span>



| <span data-ttu-id="0e429-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e429-132">Requirement</span></span> | <span data-ttu-id="0e429-133">Valore</span><span class="sxs-lookup"><span data-stu-id="0e429-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e429-134">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="0e429-134">TAPI version</span></span><br/> | <span data-ttu-id="0e429-135">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="0e429-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0e429-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e429-136">Header</span></span><br/>       | <dl> <span data-ttu-id="0e429-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e429-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0e429-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="0e429-138">Library</span></span><br/>      | <dl> <span data-ttu-id="0e429-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0e429-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0e429-140">DLL</span><span class="sxs-lookup"><span data-stu-id="0e429-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="0e429-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e429-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e429-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e429-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e429-143">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="0e429-143">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="0e429-144">**ITMedia:: Get \_ MEDIANAME**</span><span class="sxs-lookup"><span data-stu-id="0e429-144">**ITMedia::get\_MediaName**</span></span>](itmedia-get-medianame.md)
</dt> </dl>

 

