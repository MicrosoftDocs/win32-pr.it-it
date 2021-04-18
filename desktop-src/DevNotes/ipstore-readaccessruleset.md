---
description: Legge le regole di accesso per un tipo specificato.
ms.assetid: fd569e7f-ca5c-4571-bbaa-c669e8780a97
title: 'Metodo IPStore:: ReadAccessRuleSet (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadAccessRuleSet
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f69c206bde67c2ddf9ed87ba0c50633ab9c15bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330429"
---
# <a name="ipstorereadaccessruleset-method"></a><span data-ttu-id="add7d-103">Metodo IPStore:: ReadAccessRuleSet</span><span class="sxs-lookup"><span data-stu-id="add7d-103">IPStore::ReadAccessRuleSet method</span></span>

<span data-ttu-id="add7d-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="add7d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="add7d-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="add7d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="add7d-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="add7d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="add7d-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="add7d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="add7d-108">\[Questo metodo non è implementato.\]</span><span class="sxs-lookup"><span data-stu-id="add7d-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="add7d-109">Legge le regole di accesso per un tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="add7d-109">Reads the access rules for a given type.</span></span>

## <a name="syntax"></a><span data-ttu-id="add7d-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="add7d-110">Syntax</span></span>


```C++
HRESULT ReadAccessRuleSet(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET **ppRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="add7d-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="add7d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="add7d-112">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="add7d-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="add7d-113">Riservato.</span><span class="sxs-lookup"><span data-stu-id="add7d-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="add7d-114">*pType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="add7d-114">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="add7d-115">Riservato.</span><span class="sxs-lookup"><span data-stu-id="add7d-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="add7d-116">*pSubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="add7d-116">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="add7d-117">Riservato.</span><span class="sxs-lookup"><span data-stu-id="add7d-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="add7d-118">*pInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="add7d-118">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="add7d-119">Riservato.</span><span class="sxs-lookup"><span data-stu-id="add7d-119">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="add7d-120">*ppRules* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="add7d-120">*ppRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="add7d-121">Riservato.</span><span class="sxs-lookup"><span data-stu-id="add7d-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="add7d-122">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="add7d-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="add7d-123">Riservato.</span><span class="sxs-lookup"><span data-stu-id="add7d-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="add7d-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="add7d-124">Return value</span></span>

<span data-ttu-id="add7d-125">Le chiamate a questo metodo avranno sempre esito negativo.</span><span class="sxs-lookup"><span data-stu-id="add7d-125">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="add7d-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="add7d-126">Requirements</span></span>



| <span data-ttu-id="add7d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="add7d-127">Requirement</span></span> | <span data-ttu-id="add7d-128">Valore</span><span class="sxs-lookup"><span data-stu-id="add7d-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="add7d-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="add7d-129">Header</span></span><br/> | <dl> <span data-ttu-id="add7d-130"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="add7d-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="add7d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="add7d-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="add7d-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="add7d-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="add7d-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="add7d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add7d-134">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="add7d-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
