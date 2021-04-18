---
description: Elimina l'elemento specificato dall'archivio protetto.
ms.assetid: 1d071245-a563-4fba-9300-c47ca9a9d625
title: Metodo IPStore::D eleteItem (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3a882b9178160e8e82222943501c3317f8f11536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331293"
---
# <a name="ipstoredeleteitem-method"></a><span data-ttu-id="4b415-103">IPStore::D Metodo eleteItem</span><span class="sxs-lookup"><span data-stu-id="4b415-103">IPStore::DeleteItem method</span></span>

<span data-ttu-id="4b415-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4b415-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="4b415-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4b415-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="4b415-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="4b415-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="4b415-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="4b415-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="4b415-108">Elimina l'elemento specificato dall'archivio protetto.</span><span class="sxs-lookup"><span data-stu-id="4b415-108">Deletes the specified item from the protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b415-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b415-109">Syntax</span></span>


```C++
HRESULT DeleteItem(
  [in]       PST_KEY         Key,
  [in] const GUID            *pItemType,
  [in] const GUID            *pItemSubType,
  [in]       LPCWSTR         szItemName,
  [in]       PPST_PROMPTINFO pPromptInfo,
  [in]       DWORD           dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4b415-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4b415-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b415-111">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4b415-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b415-112">Area di archiviazione del provider.</span><span class="sxs-lookup"><span data-stu-id="4b415-112">The provider storage area.</span></span>



| <span data-ttu-id="4b415-113">Valore</span><span class="sxs-lookup"><span data-stu-id="4b415-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="4b415-114">Significato</span><span class="sxs-lookup"><span data-stu-id="4b415-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="4b415-115"><dt>**Pst \_ CHIAVE \_ \_ utente corrente**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="4b415-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="4b415-116">L'archiviazione viene mantenuta nella sezione utente corrente del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4b415-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="4b415-117"><dt>**Pst \_ CHIAVE \_ del \_ computer locale**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="4b415-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="4b415-118">L'archiviazione viene mantenuta nella sezione computer locale del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4b415-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4b415-119">*pItemType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b415-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b415-120">Puntatore a un **GUID** che identifica il tipo di dati dell'elemento da eliminare.</span><span class="sxs-lookup"><span data-stu-id="4b415-120">A pointer to a **GUID** that identifies the data type of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="4b415-121">*pItemSubType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b415-121">*pItemSubType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b415-122">**GUID** che indica il sottotipo di elemento da eliminare.</span><span class="sxs-lookup"><span data-stu-id="4b415-122">A **GUID** that indicates the item subtype to delete.</span></span>

</dd> <dt>

<span data-ttu-id="4b415-123">*szItemName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b415-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b415-124">Stringa che contiene il nome dell'elemento da eliminare.</span><span class="sxs-lookup"><span data-stu-id="4b415-124">A string that contains the name of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="4b415-125">*pPromptInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b415-125">*pPromptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b415-126">Puntatore a una struttura [**\_ PROMPTINFO PST**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="4b415-126">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4b415-127">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4b415-127">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b415-128">Specifica l'interfaccia utente e i comportamenti di sicurezza per l'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="4b415-128">Specifies user interface and security behaviors for the delete operation.</span></span>



| <span data-ttu-id="4b415-129">Valore</span><span class="sxs-lookup"><span data-stu-id="4b415-129">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="4b415-130">Significato</span><span class="sxs-lookup"><span data-stu-id="4b415-130">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <span data-ttu-id="4b415-131"><dt>**Pst \_ Nessuna \_ \_ migrazione dell'interfaccia utente**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="4b415-131"><dt>**PST\_NO\_UI\_MIGRATION**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="4b415-132">Non visualizzare l'interfaccia utente a meno che non sia necessaria una password personalizzata.</span><span class="sxs-lookup"><span data-stu-id="4b415-132">Do not show user interface unless a custom password is required.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b415-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4b415-133">Return value</span></span>

<span data-ttu-id="4b415-134">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4b415-134">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="4b415-135">Il valore **pst \_ E \_ OK** indica che la funzione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4b415-135">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b415-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b415-136">Requirements</span></span>



| <span data-ttu-id="4b415-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b415-137">Requirement</span></span> | <span data-ttu-id="4b415-138">Valore</span><span class="sxs-lookup"><span data-stu-id="4b415-138">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b415-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b415-139">Header</span></span><br/> | <dl> <span data-ttu-id="4b415-140"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b415-140"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="4b415-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4b415-141">DLL</span></span><br/>    | <dl> <span data-ttu-id="4b415-142"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b415-142"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b415-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b415-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b415-144">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="4b415-144">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="4b415-145">**\_PROMPTINFO PST**</span><span class="sxs-lookup"><span data-stu-id="4b415-145">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
