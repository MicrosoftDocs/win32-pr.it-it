---
description: "Interfaccia IEnumPStoreProviders: fornisce metodi di enumerazione standard COM per l'interfaccia IPStore."
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: Interfaccia IEnumPStoreProviders (Pstore.h)
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
ms.openlocfilehash: cf203e0e6de08b6faff3d3b4a040018ec1122975
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089349"
---
# <a name="ienumpstoreproviders-interface"></a><span data-ttu-id="4e160-103">Interfaccia IEnumPStoreProviders</span><span class="sxs-lookup"><span data-stu-id="4e160-103">IEnumPStoreProviders interface</span></span>

<span data-ttu-id="4e160-104">\[L'archiviazione protetta (Pstore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4e160-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="4e160-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4e160-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="4e160-106">Pstore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="4e160-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="4e160-107">Gli sviluppatori sono fortemente invitati a sfruttare la protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]</span><span class="sxs-lookup"><span data-stu-id="4e160-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="4e160-108">Fornisce metodi di enumerazione standard COM per [**l'interfaccia IPStore.**](ipstore.md)</span><span class="sxs-lookup"><span data-stu-id="4e160-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="4e160-109">Membri</span><span class="sxs-lookup"><span data-stu-id="4e160-109">Members</span></span>

<span data-ttu-id="4e160-110">**L'interfaccia IEnumPStoreProviders** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown)</span><span class="sxs-lookup"><span data-stu-id="4e160-110">The **IEnumPStoreProviders** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4e160-111">**IEnumPStoreProviders** include anche questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4e160-111">**IEnumPStoreProviders** also has these types of members:</span></span>

-   [<span data-ttu-id="4e160-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="4e160-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4e160-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="4e160-113">Methods</span></span>

<span data-ttu-id="4e160-114">**L'interfaccia IEnumPStoreProviders** include questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4e160-114">The **IEnumPStoreProviders** interface has these methods.</span></span>



| <span data-ttu-id="4e160-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="4e160-115">Method</span></span>                                      | <span data-ttu-id="4e160-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e160-116">Description</span></span>                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e160-117">**Clone**</span><span class="sxs-lookup"><span data-stu-id="4e160-117">**Clone**</span></span>](ienumpstoreproviders-clone.md) | <span data-ttu-id="4e160-118">Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="4e160-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="4e160-119">**Avanti**</span><span class="sxs-lookup"><span data-stu-id="4e160-119">**Next**</span></span>](ienumpstoreproviders-next.md)   | <span data-ttu-id="4e160-120">Ottiene il provider specificato successivo nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="4e160-120">Gets the next specified provider in the enumeration sequence.</span></span><br/>                           |
| [<span data-ttu-id="4e160-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="4e160-121">**Reset**</span></span>](ienumpstoreproviders-reset.md) | <span data-ttu-id="4e160-122">Reimposta all'inizio della sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="4e160-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="4e160-123">**Ignora**</span><span class="sxs-lookup"><span data-stu-id="4e160-123">**Skip**</span></span>](ienumpstoreproviders-skip.md)   | <span data-ttu-id="4e160-124">Ignora il provider specificato nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="4e160-124">Skips the specified provider in the enumeration sequence.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="4e160-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e160-125">Requirements</span></span>



| <span data-ttu-id="4e160-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e160-126">Requirement</span></span> | <span data-ttu-id="4e160-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4e160-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e160-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e160-128">Header</span></span><br/> | <dl> <span data-ttu-id="4e160-129"><dt>Pstore.h</dt></span><span class="sxs-lookup"><span data-stu-id="4e160-129"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="4e160-130">DLL</span><span class="sxs-lookup"><span data-stu-id="4e160-130">DLL</span></span><br/>    | <dl> <span data-ttu-id="4e160-131"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e160-131"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
