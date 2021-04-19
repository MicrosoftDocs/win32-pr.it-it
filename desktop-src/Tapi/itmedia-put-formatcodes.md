---
description: Il \_ metodo Put codiciformato imposta l'elenco dei codici di formato del payload multimediale. La variante contiene un SAFEARRAY di BSTR. Ogni BSTR all'interno di tale matrice è una stringa di codice del formato.
ms.assetid: b76a7fee-0fae-41fb-a8cd-6803458d9182
title: 'ITMedia: metodo:p ut_FormatCodes (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9131f946635c2bb066e704f1d6245c1c30d1372
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323939"
---
# <a name="itmediaput_formatcodes-method"></a><span data-ttu-id="47f72-105">ITMedia::p UT \_ codiciformato metodo</span><span class="sxs-lookup"><span data-stu-id="47f72-105">ITMedia::put\_FormatCodes method</span></span>

<span data-ttu-id="47f72-106">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="47f72-106">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="47f72-107">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="47f72-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="47f72-108">Il metodo **put \_ codiciformato** imposta l'elenco dei codici di formato del payload multimediale.</span><span class="sxs-lookup"><span data-stu-id="47f72-108">The **put\_FormatCodes** method sets the list of media payload format codes.</span></span> <span data-ttu-id="47f72-109">La variante contiene un elemento SAFEARRAY di **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="47f72-109">The variant contains a SAFEARRAY of **BSTR** s.</span></span> <span data-ttu-id="47f72-110">Ogni **BSTR** all'interno di tale matrice è una stringa di codice del formato.</span><span class="sxs-lookup"><span data-stu-id="47f72-110">Each **BSTR** within that array is a format code string.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f72-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47f72-111">Syntax</span></span>


```C++
HRESULT put_FormatCodes(
  [in] VARIANT NewVal
);
```



## <a name="parameters"></a><span data-ttu-id="47f72-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="47f72-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47f72-113">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47f72-113">*NewVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f72-114">Elenco dei codici di formato del payload multimediale.</span><span class="sxs-lookup"><span data-stu-id="47f72-114">List of media payload format codes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47f72-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47f72-115">Return value</span></span>

<span data-ttu-id="47f72-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="47f72-116">This method can return one of these values.</span></span>



| <span data-ttu-id="47f72-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="47f72-117">Return code</span></span>                                                                                   | <span data-ttu-id="47f72-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47f72-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="47f72-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="47f72-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="47f72-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="47f72-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="47f72-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="47f72-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="47f72-122">Il parametro *NewVal* non è valido.</span><span class="sxs-lookup"><span data-stu-id="47f72-122">The *NewVal* parameter is not valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="47f72-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="47f72-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="47f72-124">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="47f72-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="47f72-125"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="47f72-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="47f72-126">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="47f72-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="47f72-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="47f72-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="47f72-128">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="47f72-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="47f72-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="47f72-129">Remarks</span></span>

<span data-ttu-id="47f72-130">Quando viene fornito un elenco di formati di payload, questo implica che tutti questi formati possono essere utilizzati nella sessione, ma il primo di questi formati è il formato predefinito per la sessione.</span><span class="sxs-lookup"><span data-stu-id="47f72-130">When a list of payload formats is given, this implies that all of these formats may be used in the session, but the first of these formats is the default format for the session.</span></span> <span data-ttu-id="47f72-131">Quando il protocollo di trasporto è RTP, i codici di formato sono tipi di payload RTP.</span><span class="sxs-lookup"><span data-stu-id="47f72-131">When the transport protocol is RTP, the format codes are RTP payload types.</span></span>

## <a name="requirements"></a><span data-ttu-id="47f72-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47f72-132">Requirements</span></span>



| <span data-ttu-id="47f72-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="47f72-133">Requirement</span></span> | <span data-ttu-id="47f72-134">Valore</span><span class="sxs-lookup"><span data-stu-id="47f72-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47f72-135">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="47f72-135">TAPI version</span></span><br/> | <span data-ttu-id="47f72-136">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="47f72-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="47f72-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="47f72-137">Header</span></span><br/>       | <dl> <span data-ttu-id="47f72-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="47f72-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="47f72-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="47f72-139">Library</span></span><br/>      | <dl> <span data-ttu-id="47f72-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47f72-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="47f72-141">DLL</span><span class="sxs-lookup"><span data-stu-id="47f72-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="47f72-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47f72-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47f72-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47f72-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47f72-144">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="47f72-144">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="47f72-145">**ITMedia:: Get \_ codiciformato**</span><span class="sxs-lookup"><span data-stu-id="47f72-145">**ITMedia::get\_FormatCodes**</span></span>](itmedia-get-formatcodes.md)
</dt> </dl>

 

 




