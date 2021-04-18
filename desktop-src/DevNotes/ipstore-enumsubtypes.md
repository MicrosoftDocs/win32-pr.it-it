---
description: Restituisce un'interfaccia per l'enumerazione dei sottotipi dei tipi attualmente registrati nel database protetto.
ms.assetid: 07cc43ce-2191-4b20-b23d-d96d15aa8dea
title: 'Metodo IPStore:: EnumSubtypes (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumSubtypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f0e5aafbfdadebfa96254b3bd5997ec8d07cfb64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330551"
---
# <a name="ipstoreenumsubtypes-method"></a><span data-ttu-id="a7e11-103">Metodo IPStore:: EnumSubtypes</span><span class="sxs-lookup"><span data-stu-id="a7e11-103">IPStore::EnumSubtypes method</span></span>

<span data-ttu-id="a7e11-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a7e11-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="a7e11-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a7e11-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="a7e11-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="a7e11-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="a7e11-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="a7e11-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="a7e11-108">Restituisce un'interfaccia per l'enumerazione dei sottotipi dei tipi attualmente registrati nel database protetto.</span><span class="sxs-lookup"><span data-stu-id="a7e11-108">Returns an interface for enumerating subtypes of the types currently registered in the protected database.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7e11-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7e11-109">Syntax</span></span>


```C++
HRESULT EnumSubtypes(
  [in]       PST_KEY          Key,
  [in] const GUID             *pType,
  [in]       DWORD            dwFlags,
  [in]       IEnumPStoreTypes **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="a7e11-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7e11-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7e11-111">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a7e11-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7e11-112">Specifica se il tipo è locale o associato solo all'utente che ha creato il computer.</span><span class="sxs-lookup"><span data-stu-id="a7e11-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="a7e11-113">Valore</span><span class="sxs-lookup"><span data-stu-id="a7e11-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="a7e11-114">Significato</span><span class="sxs-lookup"><span data-stu-id="a7e11-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="a7e11-115"><dt>**Pst \_ CHIAVE \_ \_ utente corrente**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="a7e11-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="a7e11-116">L'archiviazione viene mantenuta nella sezione utente corrente del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a7e11-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="a7e11-117"><dt>**Pst \_ CHIAVE \_ del \_ computer locale**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="a7e11-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="a7e11-118">L'archiviazione viene mantenuta nella sezione computer locale del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="a7e11-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a7e11-119">*pType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7e11-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7e11-120">Puntatore a un GUID che identifica il tipo di dati dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a7e11-120">A pointer to a GUID that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="a7e11-121">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7e11-121">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7e11-122">Riservato: deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="a7e11-122">Reserved: Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a7e11-123">*ppEnum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7e11-123">*ppenum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7e11-124">Puntatore a un'interfaccia [**IEnumPStoreTypes**](ienumpstoretypes.md) utilizzata per enumerare i sottotipi.</span><span class="sxs-lookup"><span data-stu-id="a7e11-124">A pointer to an [**IEnumPStoreTypes**](ienumpstoretypes.md) interface that is used to enumerate the subtypes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7e11-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7e11-125">Return value</span></span>

<span data-ttu-id="a7e11-126">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a7e11-126">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="a7e11-127">Il valore **pst \_ E \_ OK** indica che la funzione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a7e11-127">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7e11-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7e11-128">Requirements</span></span>



| <span data-ttu-id="a7e11-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7e11-129">Requirement</span></span> | <span data-ttu-id="a7e11-130">Valore</span><span class="sxs-lookup"><span data-stu-id="a7e11-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7e11-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7e11-131">Header</span></span><br/> | <dl> <span data-ttu-id="a7e11-132"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7e11-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="a7e11-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a7e11-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="a7e11-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7e11-134"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7e11-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7e11-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7e11-136">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="a7e11-136">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
