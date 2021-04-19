---
description: Fornisce i metodi di enumerazione standard COM per l'interfaccia IPStore.
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: Interfaccia IEnumPStoreProviders (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e01bd28722fdb4d5a0ff7e3db4f715ddc1df2315
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332098"
---
# <a name="ienumpstoreproviders-interface"></a><span data-ttu-id="0d9af-103">Interfaccia IEnumPStoreProviders</span><span class="sxs-lookup"><span data-stu-id="0d9af-103">IEnumPStoreProviders interface</span></span>

<span data-ttu-id="0d9af-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="0d9af-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="0d9af-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="0d9af-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="0d9af-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="0d9af-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="0d9af-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="0d9af-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="0d9af-108">Fornisce i metodi di enumerazione standard COM per l'interfaccia [**IPStore**](ipstore.md) .</span><span class="sxs-lookup"><span data-stu-id="0d9af-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="0d9af-109">Membri</span><span class="sxs-lookup"><span data-stu-id="0d9af-109">Members</span></span>

<span data-ttu-id="0d9af-110">L'interfaccia **IEnumPStoreProviders** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0d9af-110">The **IEnumPStoreProviders** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0d9af-111">**IEnumPStoreProviders** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0d9af-111">**IEnumPStoreProviders** also has these types of members:</span></span>

-   [<span data-ttu-id="0d9af-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="0d9af-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0d9af-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="0d9af-113">Methods</span></span>

<span data-ttu-id="0d9af-114">L'interfaccia **IEnumPStoreProviders** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="0d9af-114">The **IEnumPStoreProviders** interface has these methods.</span></span>



| <span data-ttu-id="0d9af-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="0d9af-115">Method</span></span>                                      | <span data-ttu-id="0d9af-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d9af-116">Description</span></span>                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d9af-117">**Clone**</span><span class="sxs-lookup"><span data-stu-id="0d9af-117">**Clone**</span></span>](ienumpstoreproviders-clone.md) | <span data-ttu-id="0d9af-118">Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="0d9af-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="0d9af-119">**Avanti**</span><span class="sxs-lookup"><span data-stu-id="0d9af-119">**Next**</span></span>](ienumpstoreproviders-next.md)   | <span data-ttu-id="0d9af-120">Ottiene il provider specificato successivo nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="0d9af-120">Gets the next specified provider in the enumeration sequence.</span></span><br/>                           |
| [<span data-ttu-id="0d9af-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="0d9af-121">**Reset**</span></span>](ienumpstoreproviders-reset.md) | <span data-ttu-id="0d9af-122">Reimposta l'inizio della sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="0d9af-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="0d9af-123">**Ignora**</span><span class="sxs-lookup"><span data-stu-id="0d9af-123">**Skip**</span></span>](ienumpstoreproviders-skip.md)   | <span data-ttu-id="0d9af-124">Ignora il provider specificato nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="0d9af-124">Skips the specified provider in the enumeration sequence.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="0d9af-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d9af-125">Requirements</span></span>



| <span data-ttu-id="0d9af-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d9af-126">Requirement</span></span> | <span data-ttu-id="0d9af-127">Valore</span><span class="sxs-lookup"><span data-stu-id="0d9af-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d9af-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d9af-128">Header</span></span><br/> | <dl> <span data-ttu-id="0d9af-129"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d9af-129"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="0d9af-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0d9af-130">DLL</span></span><br/>    | <dl> <span data-ttu-id="0d9af-131"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d9af-131"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
