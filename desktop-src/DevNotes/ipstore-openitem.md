---
description: Apre un elemento per più accessi.
ms.assetid: b0602abd-dbda-40d0-befa-348c1179fa4f
title: 'Metodo IPStore:: OpenItem (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.OpenItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 065b98c1f302596ce5a4a428ef2486e7cdcc2320
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324279"
---
# <a name="ipstoreopenitem-method"></a><span data-ttu-id="ae946-103">Metodo IPStore:: OpenItem</span><span class="sxs-lookup"><span data-stu-id="ae946-103">IPStore::OpenItem method</span></span>

<span data-ttu-id="ae946-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ae946-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="ae946-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ae946-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="ae946-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="ae946-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="ae946-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="ae946-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="ae946-108">Apre un elemento per più accessi.</span><span class="sxs-lookup"><span data-stu-id="ae946-108">Opens an item for multiple accesses.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae946-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae946-109">Syntax</span></span>


```C++
HRESULT OpenItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       PST_ACCESSMODE ModeFlags,
  [in]       PPST_PROMPTIFO pProomptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ae946-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae946-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae946-111">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ae946-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae946-112">Specifica se il tipo è locale o associato solo all'utente che ha creato il computer.</span><span class="sxs-lookup"><span data-stu-id="ae946-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="ae946-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ae946-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="ae946-114">Significato</span><span class="sxs-lookup"><span data-stu-id="ae946-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="ae946-115"><dt>**Pst \_ CHIAVE \_ \_ utente corrente**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="ae946-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="ae946-116">L'archiviazione viene mantenuta nella sezione utente corrente del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ae946-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="ae946-117"><dt>**Pst \_ CHIAVE \_ del \_ computer locale**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ae946-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="ae946-118">L'archiviazione viene mantenuta nella sezione computer locale del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ae946-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ae946-119">*pItemType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae946-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae946-120">Puntatore a un GUID che identifica il tipo di dati dell'elemento da aprire.</span><span class="sxs-lookup"><span data-stu-id="ae946-120">A pointer to a GUID that identifies the data type of the item to open.</span></span>

</dd> <dt>

<span data-ttu-id="ae946-121">*pItemSubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae946-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae946-122">Puntatore a un GUID che indica il sottotipo di elemento da aprire.</span><span class="sxs-lookup"><span data-stu-id="ae946-122">A pointer to a GUID that indicates the item subtype to open.</span></span>

</dd> <dt>

<span data-ttu-id="ae946-123">*szItemName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae946-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae946-124">Stringa che contiene il nome dell'elemento da aprire.</span><span class="sxs-lookup"><span data-stu-id="ae946-124">A string that contains the name of the item to open.</span></span>

</dd> <dt>

<span data-ttu-id="ae946-125">*ModeFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae946-125">*ModeFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae946-126">Descrive le modalità di accesso a cui si riferisce un set specificato di clausole di accesso.</span><span class="sxs-lookup"><span data-stu-id="ae946-126">Describes the access modes to which a specified set of access clauses pertains.</span></span> <span data-ttu-id="ae946-127">Per altre informazioni, vedere [**tipi di PStore**](pstore-types.md).</span><span class="sxs-lookup"><span data-stu-id="ae946-127">For more information, see [**PStore Types**](pstore-types.md).</span></span>



| <span data-ttu-id="ae946-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ae946-128">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="ae946-129">Significato</span><span class="sxs-lookup"><span data-stu-id="ae946-129">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <span data-ttu-id="ae946-130"><dt>**Pst \_ Leggi**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="ae946-130"><dt>**PST\_READ**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="ae946-131">Modalità di accesso in lettura.</span><span class="sxs-lookup"><span data-stu-id="ae946-131">Read access mode.</span></span><br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <span data-ttu-id="ae946-132"><dt>**Pst \_ Scrivi**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="ae946-132"><dt>**PST\_WRITE**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="ae946-133">Modalità di accesso in scrittura.</span><span class="sxs-lookup"><span data-stu-id="ae946-133">Write access mode.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ae946-134">*pProomptInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae946-134">*pProomptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae946-135">Puntatore a una struttura [**\_ PROMPTINFO PST**](pst-promptinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="ae946-135">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="ae946-136">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ae946-136">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae946-137">Riservato: deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="ae946-137">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae946-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae946-138">Return value</span></span>

<span data-ttu-id="ae946-139">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ae946-139">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="ae946-140">Il valore **pst \_ E \_ OK** indica che la funzione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ae946-140">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae946-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae946-141">Remarks</span></span>

<span data-ttu-id="ae946-142">Per aprire un elemento nel database di archiviazione protetta, l'uso di **OpenItem** richiede la chiusura finale con [**IPStore:: CloseItem**](ipstore-closeitem.md) per impedire una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="ae946-142">Using **OpenItem** to open an item in the protected storage database requires that it eventually be closed using [**IPStore::CloseItem**](ipstore-closeitem.md) to prevent a memory leak.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae946-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae946-143">Requirements</span></span>



| <span data-ttu-id="ae946-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae946-144">Requirement</span></span> | <span data-ttu-id="ae946-145">Valore</span><span class="sxs-lookup"><span data-stu-id="ae946-145">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae946-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae946-146">Header</span></span><br/> | <dl> <span data-ttu-id="ae946-147"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae946-147"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="ae946-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ae946-148">DLL</span></span><br/>    | <dl> <span data-ttu-id="ae946-149"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae946-149"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae946-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae946-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae946-151">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="ae946-151">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="ae946-152">**\_PROMPTINFO PST**</span><span class="sxs-lookup"><span data-stu-id="ae946-152">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
