---
description: Legge l'elemento dati specificato dall'archivio protetto.
ms.assetid: e565a0ea-5d8e-4706-a176-2305a95f0d67
title: 'Metodo IPStore:: ReadItem (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 0464ef06bc7c2842d0c8f9ff76e8174f05338919
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331665"
---
# <a name="ipstorereaditem-method"></a><span data-ttu-id="d0acb-103">Metodo IPStore:: ReadItem</span><span class="sxs-lookup"><span data-stu-id="d0acb-103">IPStore::ReadItem method</span></span>

<span data-ttu-id="d0acb-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d0acb-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="d0acb-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="d0acb-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="d0acb-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="d0acb-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="d0acb-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="d0acb-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="d0acb-108">Legge l'elemento dati specificato dall'archivio protetto.</span><span class="sxs-lookup"><span data-stu-id="d0acb-108">Reads the specified data item from protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0acb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0acb-109">Syntax</span></span>


```C++
HRESULT ReadItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       DWORD          cbData,
  [in]       BYTE_RPC_FAR   *pbData,
  [in]       PPST_PROMPTIFO pPromptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d0acb-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0acb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0acb-111">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d0acb-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0acb-112">Area di archiviazione del provider.</span><span class="sxs-lookup"><span data-stu-id="d0acb-112">The provider storage area.</span></span>



| <span data-ttu-id="d0acb-113">Valore</span><span class="sxs-lookup"><span data-stu-id="d0acb-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="d0acb-114">Significato</span><span class="sxs-lookup"><span data-stu-id="d0acb-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="d0acb-115"><dt>**Pst \_ CHIAVE \_ \_ utente corrente**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="d0acb-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="d0acb-116">L'archiviazione viene mantenuta nella sezione utente corrente del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d0acb-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="d0acb-117"><dt>**Pst \_ CHIAVE \_ del \_ computer locale**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="d0acb-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="d0acb-118">L'archiviazione viene mantenuta nella sezione computer locale del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d0acb-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d0acb-119">*pItemType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0acb-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0acb-120">Puntatore a un GUID che identifica il tipo di dati dell'elemento da leggere.</span><span class="sxs-lookup"><span data-stu-id="d0acb-120">A pointer to a GUID that identifies the data type of the item to read.</span></span>

</dd> <dt>

<span data-ttu-id="d0acb-121">*pItemSubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0acb-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0acb-122">Puntatore a un GUID che identifica il sottotipo di dati dell'elemento da leggere.</span><span class="sxs-lookup"><span data-stu-id="d0acb-122">A pointer to a GUID that identifies the data subtype of the item to read.</span></span>

</dd> <dt>

<span data-ttu-id="d0acb-123">*szItemName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0acb-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0acb-124">Puntatore a una stringa che contiene il nome assegnato all'elemento di dati archiviato.</span><span class="sxs-lookup"><span data-stu-id="d0acb-124">A pointer to a string that contains the name assigned to the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="d0acb-125">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0acb-125">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0acb-126">**Valore DWORD** che indica le dimensioni del buffer che contiene l'elemento dati archiviato.</span><span class="sxs-lookup"><span data-stu-id="d0acb-126">A **DWORD** that indicates the size of the buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="d0acb-127">*pbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0acb-127">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0acb-128">Puntatore a un buffer che contiene l'elemento di dati archiviato.</span><span class="sxs-lookup"><span data-stu-id="d0acb-128">A pointer to a buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="d0acb-129">*pPromptInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0acb-129">*pPromptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0acb-130">Puntatore a una struttura [**\_ PROMPTINFO PST**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="d0acb-130">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d0acb-131">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0acb-131">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0acb-132">Specifica l'interfaccia utente e i comportamenti di sicurezza per l'operazione di lettura.</span><span class="sxs-lookup"><span data-stu-id="d0acb-132">Specifies user interface and security behaviors for the read operation.</span></span>

<span data-ttu-id="d0acb-133">I valori dei flag possono essere combinati con un OR logico.</span><span class="sxs-lookup"><span data-stu-id="d0acb-133">The flag values can be combined with a logical OR.</span></span>



| <span data-ttu-id="d0acb-134">Valore</span><span class="sxs-lookup"><span data-stu-id="d0acb-134">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="d0acb-135">Significato</span><span class="sxs-lookup"><span data-stu-id="d0acb-135">Meaning</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <span data-ttu-id="d0acb-136"><dt>**Pst \_ 0x00000004 \_ ItemData senza restrizioni**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d0acb-136"><dt>**PST\_UNRESTRICTED\_ITEMDATA**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="d0acb-137">Specifica che il flusso di dati non è sicuro.</span><span class="sxs-lookup"><span data-stu-id="d0acb-137">Specifies that the data stream is nonsecure.</span></span> <span data-ttu-id="d0acb-138">Per impostazione predefinita, le chiamate agli elementi sono sicure.</span><span class="sxs-lookup"><span data-stu-id="d0acb-138">By default, item calls are secure.</span></span><br/>                                                                                                                                             |
| <span id="PST_PROMPT_QUERY"></span><span id="pst_prompt_query"></span><dl> <span data-ttu-id="d0acb-139"><dt>**Pst \_ Richiedi \_ query**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="d0acb-139"><dt>**PST\_PROMPT\_QUERY**</dt> <dt>0x00000008</dt></span></span> </dl>                            | <span data-ttu-id="d0acb-140">Specifica che la conferma viene restituita al completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="d0acb-140">Specifies that the confirmation be returned upon success.</span></span> <span data-ttu-id="d0acb-141">Se l'interfaccia utente è abilitata, viene restituito un esito positivo di **pst \_ E \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="d0acb-141">If the user interface is enabled, a success of **PST\_E\_OK** is returned.</span></span> <span data-ttu-id="d0acb-142">Se l'interfaccia utente non è abilitata, viene restituito un valore di **pst \_ E \_ Item \_** .</span><span class="sxs-lookup"><span data-stu-id="d0acb-142">If the user interface is not enabled, a value of **PST\_E\_ITEM\_EXISTS** is returned.</span></span><br/> |
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <span data-ttu-id="d0acb-143"><dt>**Pst \_ Nessuna \_ \_ migrazione dell'interfaccia utente**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="d0acb-143"><dt>**PST\_NO\_UI\_MIGRATION**</dt> <dt>0x00000010</dt></span></span> </dl>                  | <span data-ttu-id="d0acb-144">Non visualizzare l'interfaccia utente a meno che non sia necessaria una password personalizzata.</span><span class="sxs-lookup"><span data-stu-id="d0acb-144">Do not show user interface unless a custom password is required.</span></span><br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0acb-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0acb-145">Return value</span></span>

<span data-ttu-id="d0acb-146">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d0acb-146">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="d0acb-147">Il valore **pst \_ E \_ OK** indica che la funzione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="d0acb-147">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0acb-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0acb-148">Remarks</span></span>

<span data-ttu-id="d0acb-149">Se **ReadItem** viene completato correttamente, l'applicazione deve liberare il buffer di dati restituito tramite la funzione [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) .</span><span class="sxs-lookup"><span data-stu-id="d0acb-149">If **ReadItem** completes successfully, the application is responsible for freeing the returned data buffer using the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0acb-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0acb-150">Requirements</span></span>



| <span data-ttu-id="d0acb-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0acb-151">Requirement</span></span> | <span data-ttu-id="d0acb-152">Valore</span><span class="sxs-lookup"><span data-stu-id="d0acb-152">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0acb-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0acb-153">Header</span></span><br/> | <dl> <span data-ttu-id="d0acb-154"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0acb-154"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="d0acb-155">DLL</span><span class="sxs-lookup"><span data-stu-id="d0acb-155">DLL</span></span><br/>    | <dl> <span data-ttu-id="d0acb-156"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0acb-156"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0acb-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0acb-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0acb-158">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="d0acb-158">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="d0acb-159">**\_PROMPTINFO PST**</span><span class="sxs-lookup"><span data-stu-id="d0acb-159">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
