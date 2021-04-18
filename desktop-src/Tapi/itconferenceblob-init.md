---
description: Il metodo init Inizializza il BLOB della conferenza in base a una stringa testuale. Se pBlob è NULL, vengono usati i valori predefiniti.
ms.assetid: ba492503-90ff-45dd-a39f-6d4451e57339
title: 'Metodo ITConferenceBlob:: init (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bdd512ffeb4b380da04e59deb17315d00b7285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328232"
---
# <a name="itconferenceblobinit-method"></a><span data-ttu-id="0a410-104">Metodo ITConferenceBlob:: init</span><span class="sxs-lookup"><span data-stu-id="0a410-104">ITConferenceBlob::Init method</span></span>

<span data-ttu-id="0a410-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0a410-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0a410-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="0a410-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0a410-107">Il metodo **init** Inizializza il BLOB della conferenza in base a una stringa testuale.</span><span class="sxs-lookup"><span data-stu-id="0a410-107">The **Init** method initializes the conference blob based on a textual string.</span></span> <span data-ttu-id="0a410-108">Se *pBlob* è **null**, vengono usati i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0a410-108">If *pBlob* is **NULL**, default values are used.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a410-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a410-109">Syntax</span></span>


```C++
HRESULT Init(
  [in] BSTR               pName,
  [in] BLOB_CHARACTER_SET CharacterSet,
  [in] BSTR               pBlob
);
```



## <a name="parameters"></a><span data-ttu-id="0a410-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a410-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a410-111">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a410-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a410-112">Puntatore a una rappresentazione **BSTR** del nome della conferenza.</span><span class="sxs-lookup"><span data-stu-id="0a410-112">Pointer to a **BSTR** representation of the conference name.</span></span>

</dd> <dt>

<span data-ttu-id="0a410-113">*Carattere* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a410-113">*CharacterSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a410-114">[**BLOB \_ \_**](blob-character-set.md) Descrittore del set di caratteri del set di caratteri.</span><span class="sxs-lookup"><span data-stu-id="0a410-114">[**BLOB\_CHARACTER\_SET**](blob-character-set.md) descriptor of the character set.</span></span>

</dd> <dt>

<span data-ttu-id="0a410-115">*pBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0a410-115">*pBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a410-116">Puntatore a un **BSTR** che contiene il BLOB della conferenza.</span><span class="sxs-lookup"><span data-stu-id="0a410-116">Pointer to a **BSTR** containing the conference blob.</span></span> <span data-ttu-id="0a410-117">Se **null**, il BLOB della conferenza viene inizializzato con i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="0a410-117">If **NULL**, the conference blob is initialized with default values.</span></span> <span data-ttu-id="0a410-118">Attualmente, i valori di conferenza predefiniti sono disponibili solo se il parametro del set di *caratteri* è impostato su BCS \_ ASCII.</span><span class="sxs-lookup"><span data-stu-id="0a410-118">Currently, default conference values are available only if the *CharacterSet* parameter is set to BCS\_ASCII.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a410-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a410-119">Return value</span></span>

<span data-ttu-id="0a410-120">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="0a410-120">This method can return one of these values.</span></span>



| <span data-ttu-id="0a410-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0a410-121">Value</span></span>                                                                                         | <span data-ttu-id="0a410-122">Significato</span><span class="sxs-lookup"><span data-stu-id="0a410-122">Meaning</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a410-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0a410-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0a410-124">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="0a410-124">Method succeeded.</span></span><br/>                                               |
| <dl> <span data-ttu-id="0a410-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0a410-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="0a410-126">Il parametro *pname*, *charactert* o *pBlob* non è valido.</span><span class="sxs-lookup"><span data-stu-id="0a410-126">The *pName*, *CharacterSet*, or *pBlob* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="0a410-127"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="0a410-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0a410-128">La memoria disponibile non è sufficiente per eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="0a410-128">Insufficient memory exists to perform the operation.</span></span><br/>            |
| <dl> <span data-ttu-id="0a410-129"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="0a410-129"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="0a410-130">Errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="0a410-130">Unspecified error.</span></span><br/>                                              |
| <dl> <span data-ttu-id="0a410-131"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="0a410-131"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="0a410-132">Questo metodo non è ancora implementato.</span><span class="sxs-lookup"><span data-stu-id="0a410-132">This method is not yet implemented.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="0a410-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a410-133">Remarks</span></span>

<span data-ttu-id="0a410-134">**ITConferenceBlob:: init** restituirà un errore se il BLOB è già stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="0a410-134">**ITConferenceBlob::Init** will return a failure if the blob has already been initialized.</span></span>

<span data-ttu-id="0a410-135">L'applicazione deve usare [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per i parametri *pname* e *pBlob* .</span><span class="sxs-lookup"><span data-stu-id="0a410-135">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pName* and *pBlob* parameters.</span></span> <span data-ttu-id="0a410-136">L'applicazione deve usare [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando le variabili non sono più necessarie.</span><span class="sxs-lookup"><span data-stu-id="0a410-136">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variables are no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a410-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a410-137">Requirements</span></span>



| <span data-ttu-id="0a410-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a410-138">Requirement</span></span> | <span data-ttu-id="0a410-139">Valore</span><span class="sxs-lookup"><span data-stu-id="0a410-139">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a410-140">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="0a410-140">TAPI version</span></span><br/> | <span data-ttu-id="0a410-141">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="0a410-141">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0a410-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a410-142">Header</span></span><br/>       | <dl> <span data-ttu-id="0a410-143"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a410-143"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a410-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="0a410-144">Library</span></span><br/>      | <dl> <span data-ttu-id="0a410-145"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a410-145"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0a410-146">DLL</span><span class="sxs-lookup"><span data-stu-id="0a410-146">DLL</span></span><br/>          | <dl> <span data-ttu-id="0a410-147"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a410-147"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a410-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a410-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a410-149">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="0a410-149">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="0a410-150">**\_set di caratteri BLOB \_**</span><span class="sxs-lookup"><span data-stu-id="0a410-150">**BLOB\_CHARACTER\_SET**</span></span>](blob-character-set.md)
</dt> </dl>

 

