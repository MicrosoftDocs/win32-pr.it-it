---
description: Restituisce il puntatore a interfaccia di un sottotipo per l'enumerazione degli elementi nel database di archiviazione protetta.
ms.assetid: 940c321d-ec14-43fd-841b-cf581796bc87
title: 'Metodo IPStore:: EnumItems (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 9b44ee41a7daa4a75a19ca0f7045d69f5b380c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326577"
---
# <a name="ipstoreenumitems-method"></a><span data-ttu-id="0fd1c-103">Metodo IPStore:: EnumItems</span><span class="sxs-lookup"><span data-stu-id="0fd1c-103">IPStore::EnumItems method</span></span>

<span data-ttu-id="0fd1c-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0fd1c-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="0fd1c-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0fd1c-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="0fd1c-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="0fd1c-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="0fd1c-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="0fd1c-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="0fd1c-108">Restituisce il puntatore a interfaccia di un sottotipo per l'enumerazione degli elementi nel database di archiviazione protetta.</span><span class="sxs-lookup"><span data-stu-id="0fd1c-108">Returns the interface pointer of a subtype for enumerating items in the protected storage database.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd1c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0fd1c-109">Syntax</span></span>


```C++
HRESULT EnumItems(
  [in]       PST_KEY          Key,
  [in] const PSGUID           *pItemType,
  [in] const GUID             *pItemSubtype,
  [in]       DWORD            dwFlags,
  [in]       IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="0fd1c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="0fd1c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fd1c-111">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="0fd1c-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd1c-112">Specifica se il tipo è locale o associato solo all'utente che ha creato il computer.</span><span class="sxs-lookup"><span data-stu-id="0fd1c-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="0fd1c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="0fd1c-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="0fd1c-114">Significato</span><span class="sxs-lookup"><span data-stu-id="0fd1c-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="0fd1c-115"><dt>**Pst \_ CHIAVE \_ \_ utente corrente**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="0fd1c-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="0fd1c-116">L'archiviazione viene mantenuta nella sezione utente corrente del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0fd1c-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="0fd1c-117"><dt>**Pst \_ CHIAVE \_ del \_ computer locale**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="0fd1c-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="0fd1c-118">L'archiviazione viene mantenuta nella sezione computer locale del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0fd1c-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0fd1c-119">*pItemType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0fd1c-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd1c-120">Puntatore a un **GUID** che identifica il tipo di dati dell'elemento da enumerare.</span><span class="sxs-lookup"><span data-stu-id="0fd1c-120">A pointer to a **GUID** that identifies the data type of the item to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="0fd1c-121">*pItemSubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0fd1c-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd1c-122">Puntatore a un **GUID** che identifica il sottotipo di dati dell'elemento da enumerare.</span><span class="sxs-lookup"><span data-stu-id="0fd1c-122">A pointer to a **GUID** that identifies the data subtype of the item to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="0fd1c-123">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0fd1c-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd1c-124">Riservato: deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="0fd1c-124">Reserved: Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="0fd1c-125">*ppEnum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0fd1c-125">*ppenum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd1c-126">Puntatore a un puntatore a un'interfaccia [**IEnumPStoreItems**](ienumpstoreitems.md) .</span><span class="sxs-lookup"><span data-stu-id="0fd1c-126">A pointer to a pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fd1c-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0fd1c-127">Return value</span></span>

<span data-ttu-id="0fd1c-128">Il valore restituito è un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0fd1c-128">The return value is an **HRESULT**.</span></span> <span data-ttu-id="0fd1c-129">Il valore **pst \_ E \_ OK** indica che la funzione ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0fd1c-129">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fd1c-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0fd1c-130">Requirements</span></span>



| <span data-ttu-id="0fd1c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fd1c-131">Requirement</span></span> | <span data-ttu-id="0fd1c-132">Valore</span><span class="sxs-lookup"><span data-stu-id="0fd1c-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd1c-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0fd1c-133">Header</span></span><br/> | <dl> <span data-ttu-id="0fd1c-134"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fd1c-134"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="0fd1c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0fd1c-135">DLL</span></span><br/>    | <dl> <span data-ttu-id="0fd1c-136"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fd1c-136"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fd1c-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0fd1c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd1c-138">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="0fd1c-138">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
