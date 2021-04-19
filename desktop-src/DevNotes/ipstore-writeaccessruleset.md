---
description: Scrive le regole di accesso per il tipo specificato.
ms.assetid: d5cfd782-8d87-45ae-a574-0a294a30ca71
title: 'Metodo IPStore:: WriteAccessRuleset (PStore. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteAccessRuleset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7399ff800087720d65cb45e80ccab080a7df9baf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332278"
---
# <a name="ipstorewriteaccessruleset-method"></a><span data-ttu-id="42a17-103">Metodo IPStore:: WriteAccessRuleset</span><span class="sxs-lookup"><span data-stu-id="42a17-103">IPStore::WriteAccessRuleset method</span></span>

<span data-ttu-id="42a17-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="42a17-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="42a17-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="42a17-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="42a17-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="42a17-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="42a17-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="42a17-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="42a17-108">\[Questo metodo non è implementato.\]</span><span class="sxs-lookup"><span data-stu-id="42a17-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="42a17-109">Scrive le regole di accesso per il tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="42a17-109">Writes the access rules for the given type.</span></span>

## <a name="syntax"></a><span data-ttu-id="42a17-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42a17-110">Syntax</span></span>


```C++
HRESULT WriteAccessRuleset(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="42a17-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="42a17-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42a17-112">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="42a17-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a17-113">Riservato.</span><span class="sxs-lookup"><span data-stu-id="42a17-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="42a17-114">*pType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42a17-114">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a17-115">Riservato.</span><span class="sxs-lookup"><span data-stu-id="42a17-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="42a17-116">*pSubtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42a17-116">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a17-117">Riservato.</span><span class="sxs-lookup"><span data-stu-id="42a17-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="42a17-118">*pInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42a17-118">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a17-119">Riservato.</span><span class="sxs-lookup"><span data-stu-id="42a17-119">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="42a17-120">*pRules* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42a17-120">*pRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a17-121">Riservato.</span><span class="sxs-lookup"><span data-stu-id="42a17-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="42a17-122">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="42a17-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42a17-123">Riservato.</span><span class="sxs-lookup"><span data-stu-id="42a17-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42a17-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42a17-124">Return value</span></span>

<span data-ttu-id="42a17-125">Le chiamate a questo metodo avranno sempre esito negativo.</span><span class="sxs-lookup"><span data-stu-id="42a17-125">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="42a17-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42a17-126">Requirements</span></span>



| <span data-ttu-id="42a17-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="42a17-127">Requirement</span></span> | <span data-ttu-id="42a17-128">Valore</span><span class="sxs-lookup"><span data-stu-id="42a17-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="42a17-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42a17-129">Header</span></span><br/> | <dl> <span data-ttu-id="42a17-130"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="42a17-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="42a17-131">DLL</span><span class="sxs-lookup"><span data-stu-id="42a17-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="42a17-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42a17-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42a17-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42a17-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a17-134">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="42a17-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
