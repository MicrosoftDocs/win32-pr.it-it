---
description: Crea il sottotipo specificato all'interno del tipo specificato.
ms.assetid: afd5c0c6-5779-4a78-83aa-cae36f5de564
title: 'Metodo IPStore:: CreateSubtype (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e7f304b2d54bb1ae09673e77f37f95257fa6fd10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325207"
---
# <a name="ipstorecreatesubtype-method"></a><span data-ttu-id="29e0e-103">Metodo IPStore:: CreateSubtype</span><span class="sxs-lookup"><span data-stu-id="29e0e-103">IPStore::CreateSubtype method</span></span>

<span data-ttu-id="29e0e-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="29e0e-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="29e0e-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="29e0e-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="29e0e-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="29e0e-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="29e0e-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="29e0e-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="29e0e-108">Crea il sottotipo specificato all'interno del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="29e0e-108">Creates the specified subtype within the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="29e0e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29e0e-109">Syntax</span></span>


```C++
HRESULT CreateSubtype(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="29e0e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="29e0e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29e0e-111">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="29e0e-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29e0e-112">Specifica l'area di archiviazione del provider.</span><span class="sxs-lookup"><span data-stu-id="29e0e-112">Specifies the provider storage area.</span></span>



| <span data-ttu-id="29e0e-113">Valore</span><span class="sxs-lookup"><span data-stu-id="29e0e-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="29e0e-114">Significato</span><span class="sxs-lookup"><span data-stu-id="29e0e-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="29e0e-115"><dt>**Pst \_ CHIAVE \_ \_ utente corrente**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="29e0e-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="29e0e-116">L'archiviazione viene mantenuta nella sezione utente corrente del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="29e0e-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="29e0e-117"><dt>**Pst \_ CHIAVE \_ del \_ computer locale**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="29e0e-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="29e0e-118">L'archiviazione viene mantenuta nella sezione computer locale del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="29e0e-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="29e0e-119">*pType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29e0e-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29e0e-120">Puntatore a un **GUID** che identifica il tipo di dati dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="29e0e-120">A pointer to a **GUID** that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="29e0e-121">*pSubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29e0e-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29e0e-122">Puntatore a un **GUID** che identifica il sottotipo di dati dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="29e0e-122">A pointer to a **GUID** that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="29e0e-123">*pInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29e0e-123">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29e0e-124">Puntatore a una struttura [**\_ TYPEINFO PST**](pst-typeinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="29e0e-124">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="29e0e-125">*pRules* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29e0e-125">*pRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29e0e-126">Puntatore a una struttura [**\_ ACCESSRULESET PST**](pst-accessruleset.md) .</span><span class="sxs-lookup"><span data-stu-id="29e0e-126">A pointer to a [**PST\_ACCESSRULESET**](pst-accessruleset.md) structure.</span></span>

<span data-ttu-id="29e0e-127">**Windows XP:** Questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="29e0e-127">**Windows XP:** This parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="29e0e-128">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29e0e-128">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29e0e-129">Riservati deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="29e0e-129">Reserved; must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29e0e-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29e0e-130">Return value</span></span>

<span data-ttu-id="29e0e-131">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="29e0e-131">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="29e0e-132">Il valore **pst \_ E \_ OK** indica che la funzione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="29e0e-132">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="29e0e-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29e0e-133">Requirements</span></span>



| <span data-ttu-id="29e0e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="29e0e-134">Requirement</span></span> | <span data-ttu-id="29e0e-135">Valore</span><span class="sxs-lookup"><span data-stu-id="29e0e-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29e0e-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29e0e-136">Header</span></span><br/> | <dl> <span data-ttu-id="29e0e-137"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="29e0e-137"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="29e0e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="29e0e-138">DLL</span></span><br/>    | <dl> <span data-ttu-id="29e0e-139"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29e0e-139"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29e0e-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29e0e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29e0e-141">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="29e0e-141">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="29e0e-142">**\_ACCESSRULESET PST**</span><span class="sxs-lookup"><span data-stu-id="29e0e-142">**PST\_ACCESSRULESET**</span></span>](pst-accessruleset.md)
</dt> <dt>

[<span data-ttu-id="29e0e-143">**\_TYPEINFO PST**</span><span class="sxs-lookup"><span data-stu-id="29e0e-143">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
