---
description: Fornisce i metodi di enumerazione standard COM per l'interfaccia IPStore.
ms.assetid: f5290e6c-8752-4380-9210-c96a87f000ba
title: Interfaccia IEnumPStoreItems (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 11ca255cb13d998d16596bc7cc54d28d2415b227
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326289"
---
# <a name="ienumpstoreitems-interface"></a><span data-ttu-id="4719b-103">Interfaccia IEnumPStoreItems</span><span class="sxs-lookup"><span data-stu-id="4719b-103">IEnumPStoreItems interface</span></span>

<span data-ttu-id="4719b-104">\[L'archiviazione protetta (PStore) è disponibile per l'uso in Windows Server 2003 e Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4719b-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="4719b-105">È disponibile solo per le operazioni di sola lettura in Windows Server 2008 e Windows Vista, ma potrebbe non essere disponibile nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4719b-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="4719b-106">PStore usa un'implementazione precedente della protezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="4719b-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="4719b-107">Gli sviluppatori sono vivamente invitati a sfruttare i vantaggi della protezione dei dati più avanzata fornita dalle funzioni [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="4719b-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="4719b-108">Fornisce i metodi di enumerazione standard COM per l'interfaccia [**IPStore**](ipstore.md) .</span><span class="sxs-lookup"><span data-stu-id="4719b-108">Provides the COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="4719b-109">Membri</span><span class="sxs-lookup"><span data-stu-id="4719b-109">Members</span></span>

<span data-ttu-id="4719b-110">L'interfaccia **IEnumPStoreItems** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4719b-110">The **IEnumPStoreItems** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4719b-111">**IEnumPStoreItems** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4719b-111">**IEnumPStoreItems** also has these types of members:</span></span>

-   [<span data-ttu-id="4719b-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="4719b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4719b-113">Metodi</span><span class="sxs-lookup"><span data-stu-id="4719b-113">Methods</span></span>

<span data-ttu-id="4719b-114">L'interfaccia **IEnumPStoreItems** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4719b-114">The **IEnumPStoreItems** interface has these methods.</span></span>



| <span data-ttu-id="4719b-115">Metodo</span><span class="sxs-lookup"><span data-stu-id="4719b-115">Method</span></span>                                  | <span data-ttu-id="4719b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4719b-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4719b-117">**Clone**</span><span class="sxs-lookup"><span data-stu-id="4719b-117">**Clone**</span></span>](ienumpstoreitems-clone.md) | <span data-ttu-id="4719b-118">Crea un altro enumeratore che contiene lo stesso stato di enumerazione di quello corrente.</span><span class="sxs-lookup"><span data-stu-id="4719b-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="4719b-119">**Avanti**</span><span class="sxs-lookup"><span data-stu-id="4719b-119">**Next**</span></span>](ienumpstoreitems-next.md)   | <span data-ttu-id="4719b-120">Ottiene l'elemento di dati specificato successivo nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="4719b-120">Gets the next specified data item in the enumeration sequence.</span></span><br/>                          |
| [<span data-ttu-id="4719b-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="4719b-121">**Reset**</span></span>](ienumpstoreitems-reset.md) | <span data-ttu-id="4719b-122">Reimposta l'inizio della sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="4719b-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="4719b-123">**Ignora**</span><span class="sxs-lookup"><span data-stu-id="4719b-123">**Skip**</span></span>](ienumpstoreitems-skip.md)   | <span data-ttu-id="4719b-124">Ignora l'elemento dati specificato nella sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="4719b-124">Skips the specified data item in the enumeration sequence.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="4719b-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="4719b-125">Remarks</span></span>

<span data-ttu-id="4719b-126">È necessario liberare ogni elemento dopo l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="4719b-126">It is necessary to free each item after enumerating it.</span></span> <span data-ttu-id="4719b-127">È inoltre necessario rilasciare l'oggetto enumeratore quando non viene più utilizzato.</span><span class="sxs-lookup"><span data-stu-id="4719b-127">The enumerator object must also be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="4719b-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4719b-128">Requirements</span></span>



| <span data-ttu-id="4719b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4719b-129">Requirement</span></span> | <span data-ttu-id="4719b-130">Valore</span><span class="sxs-lookup"><span data-stu-id="4719b-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4719b-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4719b-131">Header</span></span><br/> | <dl> <span data-ttu-id="4719b-132"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="4719b-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="4719b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4719b-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="4719b-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4719b-134"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
