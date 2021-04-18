---
description: Fornisce i metodi di enumerazione standard COM per l'interfaccia IPStore.
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: Interfaccia IEnumPStoreTypes (PStore. h)
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
ms.openlocfilehash: 748f6e21701fdd27c2a88d1959b0b29cf56929f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332091"
---
# <a name="ienumpstoretypes-interface"></a><span data-ttu-id="7204e-103">Interfaccia IEnumPStoreTypes</span><span class="sxs-lookup"><span data-stu-id="7204e-103">IEnumPStoreTypes interface</span></span>

<span data-ttu-id="7204e-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7204e-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="7204e-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="7204e-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="7204e-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="7204e-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="7204e-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="7204e-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="7204e-108">Fornisce i metodi di enumerazione standard COM per l'interfaccia [**IPStore**](ipstore.md) .</span><span class="sxs-lookup"><span data-stu-id="7204e-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="7204e-109">Membri</span><span class="sxs-lookup"><span data-stu-id="7204e-109">Members</span></span>

<span data-ttu-id="7204e-110">L'interfaccia **IEnumPStoreTypes** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7204e-110">The **IEnumPStoreTypes** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7204e-111">**IEnumPStoreTypes** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7204e-111">**IEnumPStoreTypes** also has these types of members:</span></span>

-   [<span data-ttu-id="7204e-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="7204e-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7204e-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="7204e-113">Methods</span></span>

<span data-ttu-id="7204e-114">L'interfaccia **IEnumPStoreTypes** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7204e-114">The **IEnumPStoreTypes** interface has these methods.</span></span>



| <span data-ttu-id="7204e-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="7204e-115">Method</span></span>                                  | <span data-ttu-id="7204e-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7204e-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7204e-117">**Clone**</span><span class="sxs-lookup"><span data-stu-id="7204e-117">**Clone**</span></span>](ienumpstoretypes-clone.md) | <span data-ttu-id="7204e-118">Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="7204e-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="7204e-119">**Avanti**</span><span class="sxs-lookup"><span data-stu-id="7204e-119">**Next**</span></span>](ienumpstoretypes-next.md)   | <span data-ttu-id="7204e-120">Ottiene il tipo di provider successivo specificato nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="7204e-120">Gets the next specified provider type in the enumeration sequence.</span></span><br/>                      |
| [<span data-ttu-id="7204e-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="7204e-121">**Reset**</span></span>](ienumpstoretypes-reset.md) | <span data-ttu-id="7204e-122">Reimposta l'inizio della sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="7204e-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="7204e-123">**Ignora**</span><span class="sxs-lookup"><span data-stu-id="7204e-123">**Skip**</span></span>](ienumpstoretypes-skip.md)   | <span data-ttu-id="7204e-124">Ignora il tipo di provider specificato nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="7204e-124">Skips the specified provider type in the enumeration sequence.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="7204e-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="7204e-125">Remarks</span></span>

<span data-ttu-id="7204e-126">È necessario rilasciare l'oggetto enumeratore quando non è più usato.</span><span class="sxs-lookup"><span data-stu-id="7204e-126">The enumerator object must be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="7204e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7204e-127">Requirements</span></span>



| <span data-ttu-id="7204e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7204e-128">Requirement</span></span> | <span data-ttu-id="7204e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="7204e-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7204e-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7204e-130">Header</span></span><br/> | <dl> <span data-ttu-id="7204e-131"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="7204e-131"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="7204e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7204e-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="7204e-133"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7204e-133"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
