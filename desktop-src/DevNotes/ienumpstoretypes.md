---
description: "Interfaccia IEnumPStoreTypes: fornisce metodi di enumerazione standard COM per l'interfaccia IPStore."
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: Interfaccia IEnumPStoreTypes (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7ca2e250864889a5fda465e146287bf59a2b6346
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089359"
---
# <a name="ienumpstoretypes-interface"></a><span data-ttu-id="e7a6b-103">Interfaccia IEnumPStoreTypes</span><span class="sxs-lookup"><span data-stu-id="e7a6b-103">IEnumPStoreTypes interface</span></span>

<span data-ttu-id="e7a6b-104">\[L'archiviazione protetta (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="e7a6b-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="e7a6b-106">Pstore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="e7a6b-107">Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]</span><span class="sxs-lookup"><span data-stu-id="e7a6b-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="e7a6b-108">Fornisce metodi di enumerazione standard COM per [**l'interfaccia IPStore.**](ipstore.md)</span><span class="sxs-lookup"><span data-stu-id="e7a6b-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="e7a6b-109">Membri</span><span class="sxs-lookup"><span data-stu-id="e7a6b-109">Members</span></span>

<span data-ttu-id="e7a6b-110">**L'interfaccia IEnumPStoreTypes** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="e7a6b-110">The **IEnumPStoreTypes** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e7a6b-111">**IEnumPStoreTypes** include anche questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e7a6b-111">**IEnumPStoreTypes** also has these types of members:</span></span>

-   [<span data-ttu-id="e7a6b-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="e7a6b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e7a6b-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="e7a6b-113">Methods</span></span>

<span data-ttu-id="e7a6b-114">**L'interfaccia IEnumPStoreTypes** include questi metodi.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-114">The **IEnumPStoreTypes** interface has these methods.</span></span>



| <span data-ttu-id="e7a6b-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="e7a6b-115">Method</span></span>                                  | <span data-ttu-id="e7a6b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7a6b-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7a6b-117">**Clone**</span><span class="sxs-lookup"><span data-stu-id="e7a6b-117">**Clone**</span></span>](ienumpstoretypes-clone.md) | <span data-ttu-id="e7a6b-118">Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="e7a6b-119">**Avanti**</span><span class="sxs-lookup"><span data-stu-id="e7a6b-119">**Next**</span></span>](ienumpstoretypes-next.md)   | <span data-ttu-id="e7a6b-120">Ottiene il tipo di provider specificato successivo nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-120">Gets the next specified provider type in the enumeration sequence.</span></span><br/>                      |
| [<span data-ttu-id="e7a6b-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="e7a6b-121">**Reset**</span></span>](ienumpstoretypes-reset.md) | <span data-ttu-id="e7a6b-122">Reimposta all'inizio della sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="e7a6b-123">**Ignora**</span><span class="sxs-lookup"><span data-stu-id="e7a6b-123">**Skip**</span></span>](ienumpstoretypes-skip.md)   | <span data-ttu-id="e7a6b-124">Ignora il tipo di provider specificato nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-124">Skips the specified provider type in the enumeration sequence.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="e7a6b-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7a6b-125">Remarks</span></span>

<span data-ttu-id="e7a6b-126">L'oggetto enumeratore deve essere rilasciato quando non viene più utilizzato.</span><span class="sxs-lookup"><span data-stu-id="e7a6b-126">The enumerator object must be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7a6b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7a6b-127">Requirements</span></span>



| <span data-ttu-id="e7a6b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7a6b-128">Requirement</span></span> | <span data-ttu-id="e7a6b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="e7a6b-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a6b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7a6b-130">Header</span></span><br/> | <dl> <span data-ttu-id="e7a6b-131"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="e7a6b-131"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="e7a6b-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e7a6b-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="e7a6b-133"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7a6b-133"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
