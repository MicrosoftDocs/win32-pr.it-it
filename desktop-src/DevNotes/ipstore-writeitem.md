---
description: Scrive un elemento di dati in un archivio protetto.
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: 'Metodo IPStore:: WriteItem (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: b11436ca5a884b7d45c853433c3203b219e0527c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331467"
---
# <a name="ipstorewriteitem-method"></a><span data-ttu-id="b2fb3-103">Metodo IPStore:: WriteItem</span><span class="sxs-lookup"><span data-stu-id="b2fb3-103">IPStore::WriteItem method</span></span>

<span data-ttu-id="b2fb3-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="b2fb3-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="b2fb3-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="b2fb3-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="b2fb3-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="b2fb3-108">Scrive un elemento di dati in un archivio protetto.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-108">Writes a data item to protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2fb3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b2fb3-109">Syntax</span></span>


```C++
HRESULT WriteItem(
  [in]        PST_KEY        Key,
  [in]  const GUID           *pItemType,
  [in]  const GUID           *pItemSubtype,
  [in]        LPCWSTR        *szItemName,
  [out]       DWORD          *cbData,
  [out]       BYTE           ppbData,
  [in]        PPST_PROMPTIFO pProomptInfo,
  [in]        DWORD          dwDefaultConfirmationStyle,
  [in]        DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b2fb3-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2fb3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2fb3-111">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b2fb3-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2fb3-112">Area di archiviazione del provider.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-112">The provider storage area.</span></span>



| <span data-ttu-id="b2fb3-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b2fb3-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="b2fb3-114">Significato</span><span class="sxs-lookup"><span data-stu-id="b2fb3-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="b2fb3-115"><dt>**Pst \_ CHIAVE \_ \_ utente corrente**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="b2fb3-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="b2fb3-116">L'archiviazione viene mantenuta nella sezione utente corrente del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="b2fb3-117"><dt>**Pst \_ CHIAVE \_ del \_ computer locale**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="b2fb3-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="b2fb3-118">L'archiviazione viene mantenuta nella sezione computer locale del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="b2fb3-119">*pItemType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2fb3-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2fb3-120">Puntatore a un **GUID** che identifica il tipo di dati dell'elemento di dati in fase di scrittura.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-120">A pointer to a **GUID** that identifies the data type of the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="b2fb3-121">*pItemSubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2fb3-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2fb3-122">Puntatore a un **GUID** che identifica il sottotipo di dati dell'elemento di dati da scrivere.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-122">A pointer to a **GUID** that identifies the data subtype of the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="b2fb3-123">*szItemName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2fb3-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2fb3-124">Puntatore a una stringa che contiene il nome assegnato all'elemento di dati archiviato.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-124">A pointer to a string that contains the name assigned to the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="b2fb3-125">*cbData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b2fb3-125">*cbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2fb3-126">Puntatore a un **valore DWORD** che indica le dimensioni del buffer che contiene l'elemento dati archiviato.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-126">A pointer to a **DWORD** that indicates the size of the buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="b2fb3-127">*ppbData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b2fb3-127">*ppbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2fb3-128">Puntatore a un buffer contenente l'elemento di dati in fase di scrittura.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-128">A pointer to a buffer that contains the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="b2fb3-129">*pProomptInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2fb3-129">*pProomptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2fb3-130">Puntatore a una [**struttura \_ PROMPTINFO PST**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="b2fb3-130">Pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="b2fb3-131">*dwDefaultConfirmationStyle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2fb3-131">*dwDefaultConfirmationStyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2fb3-132">Stile di conferma predefinito.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-132">The default confirmation style.</span></span>



| <span data-ttu-id="b2fb3-133">Valore</span><span class="sxs-lookup"><span data-stu-id="b2fb3-133">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="b2fb3-134">Significato</span><span class="sxs-lookup"><span data-stu-id="b2fb3-134">Meaning</span></span>                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <span data-ttu-id="b2fb3-135"><dt>**Pst \_ 0x00000000 \_ predefinito CF**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b2fb3-135"><dt>**PST\_CF\_DEFAULT**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="b2fb3-136">Consente all'utente di scegliere lo stile di conferma.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-136">Allows the user to choose the confirmation style.</span></span> <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <span data-ttu-id="b2fb3-137"><dt>**Pst \_ CF \_ None**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="b2fb3-137"><dt>**PST\_CF\_NONE**</dt> <dt>0x00000001</dt></span></span> </dl>          | <span data-ttu-id="b2fb3-138">Forza la creazione di elementi invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-138">Forces silent item creation.</span></span> <br/>                      |



 

</dd> <dt>

<span data-ttu-id="b2fb3-139">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b2fb3-139">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2fb3-140">L'interfaccia utente e i comportamenti di sicurezza per l'operazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-140">The user interface and security behaviors for the write operation.</span></span>



| <span data-ttu-id="b2fb3-141">Valore</span><span class="sxs-lookup"><span data-stu-id="b2fb3-141">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="b2fb3-142">Significato</span><span class="sxs-lookup"><span data-stu-id="b2fb3-142">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <span data-ttu-id="b2fb3-143"><dt>**Pst \_ Nessuna \_ sovrascrittura**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="b2fb3-143"><dt>**PST\_NO\_OVERWRITE**</dt> <dt>0x00000002</dt></span></span> </dl>                            | <span data-ttu-id="b2fb3-144">Specifica che l'elemento deve essere creato nell'archivio protetto.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-144">Specifies that the item be created in protected storage.</span></span> <span data-ttu-id="b2fb3-145">La sovrascrittura di un elemento esistente non è consentita.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-145">Overwriting of an existing item is disallowed.</span></span><br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <span data-ttu-id="b2fb3-146"><dt>**Pst \_ 0x00000004 \_ ItemData senza restrizioni**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b2fb3-146"><dt>**PST\_UNRESTRICTED\_ITEMDATA**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="b2fb3-147">Specifica che il flusso di dati non è sicuro.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-147">Specifies that the data stream is nonsecure.</span></span> <span data-ttu-id="b2fb3-148">Per impostazione predefinita, le chiamate agli elementi sono sicure.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-148">By default, item calls are secure.</span></span><br/>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2fb3-149">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2fb3-149">Return value</span></span>

<span data-ttu-id="b2fb3-150">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b2fb3-150">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="b2fb3-151">Il valore **pst \_ E \_ OK** indica che la funzione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b2fb3-151">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2fb3-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2fb3-152">Requirements</span></span>



| <span data-ttu-id="b2fb3-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2fb3-153">Requirement</span></span> | <span data-ttu-id="b2fb3-154">Valore</span><span class="sxs-lookup"><span data-stu-id="b2fb3-154">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2fb3-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2fb3-155">Header</span></span><br/> | <dl> <span data-ttu-id="b2fb3-156"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2fb3-156"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="b2fb3-157">DLL</span><span class="sxs-lookup"><span data-stu-id="b2fb3-157">DLL</span></span><br/>    | <dl> <span data-ttu-id="b2fb3-158"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2fb3-158"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2fb3-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b2fb3-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2fb3-160">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="b2fb3-160">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="b2fb3-161">**\_PROMPTINFO PST**</span><span class="sxs-lookup"><span data-stu-id="b2fb3-161">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
