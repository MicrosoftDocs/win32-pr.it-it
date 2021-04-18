---
description: Restituisce un'interfaccia per l'enumerazione dei tipi attualmente registrati nel database protetto.
ms.assetid: 0c0c2ad7-90b0-4fc0-8972-82eb159653be
title: 'Metodo IPStore:: EnumTypes (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 73166a9fc1d76ae9f67528636eda567b9fa190a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324281"
---
# <a name="ipstoreenumtypes-method"></a><span data-ttu-id="db5c8-103">Metodo IPStore:: EnumTypes</span><span class="sxs-lookup"><span data-stu-id="db5c8-103">IPStore::EnumTypes method</span></span>

<span data-ttu-id="db5c8-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="db5c8-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="db5c8-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="db5c8-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="db5c8-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="db5c8-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="db5c8-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="db5c8-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="db5c8-108">Restituisce un'interfaccia per l'enumerazione dei tipi attualmente registrati nel database protetto.</span><span class="sxs-lookup"><span data-stu-id="db5c8-108">Returns an interface for enumerating types that are currently registered in the protected database.</span></span>

## <a name="syntax"></a><span data-ttu-id="db5c8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="db5c8-109">Syntax</span></span>


```C++
HRESULT EnumTypes(
  [in] PST_KEY          Key,
  [in] DWORD            dwFlags,
  [in] IEnumPStoreTypes **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="db5c8-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="db5c8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db5c8-111">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="db5c8-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db5c8-112">Specifica se il tipo è locale o associato solo all'utente che ha creato il computer.</span><span class="sxs-lookup"><span data-stu-id="db5c8-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="db5c8-113">Valore</span><span class="sxs-lookup"><span data-stu-id="db5c8-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="db5c8-114">Significato</span><span class="sxs-lookup"><span data-stu-id="db5c8-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="db5c8-115"><dt>**Pst \_ CHIAVE \_ \_ utente corrente**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="db5c8-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="db5c8-116">L'archiviazione viene mantenuta nella sezione utente corrente del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="db5c8-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="db5c8-117"><dt>**Pst \_ CHIAVE \_ del \_ computer locale**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="db5c8-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="db5c8-118">L'archiviazione viene mantenuta nella sezione computer locale del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="db5c8-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="db5c8-119">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db5c8-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db5c8-120">Riservato: deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="db5c8-120">Reserved: Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="db5c8-121">*ppEnum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db5c8-121">*ppenum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db5c8-122">Puntatore a un'interfaccia [**IEnumPStoreTypes**](ienumpstoretypes.md) utilizzata per eseguire le attività di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="db5c8-122">A pointer to an [**IEnumPStoreTypes**](ienumpstoretypes.md) interface that is used to perform the enumeration tasks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db5c8-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="db5c8-123">Return value</span></span>

<span data-ttu-id="db5c8-124">Il valore restituito è un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="db5c8-124">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="db5c8-125">Il valore **pst \_ E \_ OK** indica che la funzione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="db5c8-125">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="db5c8-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="db5c8-126">Requirements</span></span>



| <span data-ttu-id="db5c8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="db5c8-127">Requirement</span></span> | <span data-ttu-id="db5c8-128">Valore</span><span class="sxs-lookup"><span data-stu-id="db5c8-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db5c8-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="db5c8-129">Header</span></span><br/> | <dl> <span data-ttu-id="db5c8-130"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="db5c8-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="db5c8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="db5c8-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="db5c8-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db5c8-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db5c8-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="db5c8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db5c8-134">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="db5c8-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
