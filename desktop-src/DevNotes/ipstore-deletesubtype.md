---
description: Elimina un sottotipo specificato dall'interno del tipo specificato.
ms.assetid: 1c44a609-80af-4e28-b1b5-2b4faea143bd
title: Metodo IPStore::D eleteSubtype (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 6fd89c1dd00a71cb843596e08bc168b90008b180
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331292"
---
# <a name="ipstoredeletesubtype-method"></a><span data-ttu-id="4e1b9-103">IPStore::D Metodo eleteSubtype</span><span class="sxs-lookup"><span data-stu-id="4e1b9-103">IPStore::DeleteSubtype method</span></span>

<span data-ttu-id="4e1b9-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4e1b9-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="4e1b9-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4e1b9-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="4e1b9-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="4e1b9-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="4e1b9-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="4e1b9-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="4e1b9-108">Elimina un sottotipo specificato dall'interno del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="4e1b9-108">Deletes a specified subtype from within the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e1b9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e1b9-109">Syntax</span></span>


```C++
HRESULT DeleteSubtype(
  [in]       PST_KEY Key,
  [in] const GUID    *pType,
  [in] const GUID    *pSubtype,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4e1b9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e1b9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e1b9-111">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4e1b9-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1b9-112">Specifica se il tipo è locale o associato solo all'utente che ha creato il computer.</span><span class="sxs-lookup"><span data-stu-id="4e1b9-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="4e1b9-113">Valore</span><span class="sxs-lookup"><span data-stu-id="4e1b9-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="4e1b9-114">Significato</span><span class="sxs-lookup"><span data-stu-id="4e1b9-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="4e1b9-115"><dt>**Pst \_ CHIAVE \_ \_ utente corrente**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="4e1b9-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="4e1b9-116">L'archiviazione viene mantenuta nella sezione utente corrente del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4e1b9-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="4e1b9-117"><dt>**Pst \_ CHIAVE \_ del \_ computer locale**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="4e1b9-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="4e1b9-118">L'archiviazione viene mantenuta nella sezione computer locale del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4e1b9-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4e1b9-119">*pType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e1b9-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1b9-120">Puntatore a un GUID che identifica il tipo di dati dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4e1b9-120">A pointer to a GUID that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="4e1b9-121">*pSubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e1b9-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1b9-122">Puntatore a un GUID che identifica il sottotipo di dati dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4e1b9-122">A pointer to a GUID that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="4e1b9-123">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4e1b9-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e1b9-124">Riservato: deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="4e1b9-124">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e1b9-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e1b9-125">Return value</span></span>

<span data-ttu-id="4e1b9-126">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4e1b9-126">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="4e1b9-127">Il valore **pst \_ E \_ OK** indica che la funzione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="4e1b9-127">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e1b9-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e1b9-128">Requirements</span></span>



| <span data-ttu-id="4e1b9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e1b9-129">Requirement</span></span> | <span data-ttu-id="4e1b9-130">Valore</span><span class="sxs-lookup"><span data-stu-id="4e1b9-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e1b9-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e1b9-131">Header</span></span><br/> | <dl> <span data-ttu-id="4e1b9-132"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e1b9-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="4e1b9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4e1b9-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="4e1b9-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e1b9-134"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e1b9-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e1b9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e1b9-136">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="4e1b9-136">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
