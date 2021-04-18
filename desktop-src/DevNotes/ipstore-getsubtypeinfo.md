---
description: Recupera le informazioni associate a un sottotipo.
ms.assetid: 3daf5f37-9e7f-4ce1-bd35-d7e3c2ef5c28
title: 'Metodo IPStore:: GetSubtypeInfo (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetSubtypeInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: db7cb02d1c21b8bb1717514a6347339065e4f112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330868"
---
# <a name="ipstoregetsubtypeinfo-method"></a><span data-ttu-id="9bc6f-103">Metodo IPStore:: GetSubtypeInfo</span><span class="sxs-lookup"><span data-stu-id="9bc6f-103">IPStore::GetSubtypeInfo method</span></span>

<span data-ttu-id="9bc6f-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9bc6f-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="9bc6f-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="9bc6f-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="9bc6f-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="9bc6f-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="9bc6f-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="9bc6f-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="9bc6f-108">Recupera le informazioni associate a un sottotipo.</span><span class="sxs-lookup"><span data-stu-id="9bc6f-108">Retrieves information associated with a subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bc6f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9bc6f-109">Syntax</span></span>


```C++
HRESULT GetSubtypeInfo(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in] const GUID          *pSubtype,
  [in]       PPST_TYPEINFO **ppInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="9bc6f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="9bc6f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bc6f-111">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="9bc6f-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bc6f-112">Area di archiviazione del provider.</span><span class="sxs-lookup"><span data-stu-id="9bc6f-112">The provider storage area.</span></span>



| <span data-ttu-id="9bc6f-113">Valore</span><span class="sxs-lookup"><span data-stu-id="9bc6f-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="9bc6f-114">Significato</span><span class="sxs-lookup"><span data-stu-id="9bc6f-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="9bc6f-115"><dt>**Pst \_ CHIAVE \_ \_ utente corrente**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="9bc6f-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="9bc6f-116">L'archiviazione viene mantenuta nella sezione utente corrente del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9bc6f-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="9bc6f-117"><dt>**Pst \_ CHIAVE \_ del \_ computer locale**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="9bc6f-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="9bc6f-118">L'archiviazione viene mantenuta nella sezione computer locale del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="9bc6f-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9bc6f-119">*pType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9bc6f-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bc6f-120">Puntatore a un GUID che identifica il tipo di dati dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9bc6f-120">A pointer to a GUID that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="9bc6f-121">*pSubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9bc6f-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bc6f-122">Puntatore a un GUID che identifica il sottotipo di dati dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9bc6f-122">A pointer to a GUID that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="9bc6f-123">*ppInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9bc6f-123">*ppInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bc6f-124">Puntatore a una struttura [**\_ TYPEINFO PST**](pst-typeinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="9bc6f-124">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9bc6f-125">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9bc6f-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bc6f-126">Riservato: deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="9bc6f-126">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bc6f-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9bc6f-127">Return value</span></span>

<span data-ttu-id="9bc6f-128">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9bc6f-128">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="9bc6f-129">Il valore PST \_ E \_ OK indica che la funzione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="9bc6f-129">A value of PST\_E\_OK indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bc6f-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bc6f-130">Requirements</span></span>



| <span data-ttu-id="9bc6f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bc6f-131">Requirement</span></span> | <span data-ttu-id="9bc6f-132">Valore</span><span class="sxs-lookup"><span data-stu-id="9bc6f-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc6f-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9bc6f-133">Header</span></span><br/> | <dl> <span data-ttu-id="9bc6f-134"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bc6f-134"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="9bc6f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9bc6f-135">DLL</span></span><br/>    | <dl> <span data-ttu-id="9bc6f-136"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bc6f-136"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bc6f-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9bc6f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bc6f-138">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="9bc6f-138">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="9bc6f-139">**\_TYPEINFO PST**</span><span class="sxs-lookup"><span data-stu-id="9bc6f-139">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
