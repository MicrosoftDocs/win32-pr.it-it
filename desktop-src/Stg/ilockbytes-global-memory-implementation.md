---
title: ILockBytes-implementazione della memoria globale
description: L'implementazione della memoria globale ILockBytes viene implementata in un oggetto matrice di byte sottostante un oggetto di archiviazione di file composto COM e progettato per la lettura e la scrittura direttamente nella memoria globale.
ms.assetid: 6ab019b0-34d7-4b6e-ba77-6b6881fabd29
keywords:
- ILockBytes Strctd STG, implementazioni, memoria globale
- ILockBytes Strctd STG, implementazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d7cae82c1503fcb53d2cfd8fee39095eb60801
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328863"
---
# <a name="ilockbytes---global-memory-implementation"></a><span data-ttu-id="1a413-105">ILockBytes-implementazione della memoria globale</span><span class="sxs-lookup"><span data-stu-id="1a413-105">ILockBytes - Global Memory Implementation</span></span>

<span data-ttu-id="1a413-106">L'implementazione della memoria globale ILockBytes viene implementata in un oggetto matrice di byte sottostante un oggetto di archiviazione di file composto COM e progettato per la lettura e la scrittura direttamente nella memoria globale.</span><span class="sxs-lookup"><span data-stu-id="1a413-106">The ILockBytes global memory implementation is implemented on a byte array object underlying a COM compound file storage object, and designed to read and write directly to global memory.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="1a413-107">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="1a413-107">When to Use</span></span>

<span data-ttu-id="1a413-108">I metodi di [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) vengono chiamati dalle implementazioni di file compositi di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) nell'oggetto di archiviazione di file composti creato tramite una chiamata a [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).</span><span class="sxs-lookup"><span data-stu-id="1a413-108">Methods of [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) are called from the compound file implementations of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) and [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) on the compound file storage object created through a call to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).</span></span>

## <a name="remarks"></a><span data-ttu-id="1a413-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a413-109">Remarks</span></span>

<span data-ttu-id="1a413-110">Di seguito sono riportati i metodi dell'implementazione della memoria globale [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .</span><span class="sxs-lookup"><span data-stu-id="1a413-110">The following are the methods of the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) Global Memory Implementation.</span></span>

<dl> <dt>

<span data-ttu-id="1a413-111"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: ReadAt**</span><span class="sxs-lookup"><span data-stu-id="1a413-111"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**</span></span>
</dt> <dd>

<span data-ttu-id="1a413-112">Legge un blocco di byte da un offset specificato all'inizio della matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="1a413-112">Reads a block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="1a413-113"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: WriteAt**</span><span class="sxs-lookup"><span data-stu-id="1a413-113"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**</span></span>
</dt> <dd>

<span data-ttu-id="1a413-114">Scrive il blocco di byte da un offset specificato all'inizio della matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="1a413-114">Writes the block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="1a413-115"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: Flush**</span><span class="sxs-lookup"><span data-stu-id="1a413-115"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**</span></span>
</dt> <dd>

<span data-ttu-id="1a413-116">A differenza dell'implementazione basata su file, la chiamata a questo metodo nell'implementazione della memoria globale non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="1a413-116">Unlike file-based implementation, calling this method in global memory implementation has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="1a413-117"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: sesize**</span><span class="sxs-lookup"><span data-stu-id="1a413-117"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**</span></span>
</dt> <dd>

<span data-ttu-id="1a413-118">Imposta la dimensione della matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="1a413-118">Sets the size of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="1a413-119"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**</span><span class="sxs-lookup"><span data-stu-id="1a413-119"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="1a413-120">Questa implementazione non supporta il blocco, quindi *dwLocksType* è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="1a413-120">This implementation does not support locking, so *dwLocksType* is set to zero.</span></span> <span data-ttu-id="1a413-121">Il chiamante deve garantire che gli accessi siano validi e si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="1a413-121">The caller must ensure accesses are valid and mutually exclusive.</span></span>

</dd> <dt>

<span data-ttu-id="1a413-122"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="1a413-122"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="1a413-123">Questa implementazione non supporta il blocco.</span><span class="sxs-lookup"><span data-stu-id="1a413-123">This implementation does not support locking.</span></span>

</dd> <dt>

<span data-ttu-id="1a413-124"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: stat**</span><span class="sxs-lookup"><span data-stu-id="1a413-124"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**</span></span>
</dt> <dd>

<span data-ttu-id="1a413-125">L'implementazione di [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) fornita da com chiama il metodo [**ILockBytes:: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) per recuperare i dati sull'oggetto matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="1a413-125">The COM-provided [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) implementation calls the [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) method to retrieve data about the byte array object.</span></span> <span data-ttu-id="1a413-126">Se non esiste un nome ragionevole per la matrice di byte, il metodo **ILockBytes:: stat** fornito da com **restituisce null** nel membro **pwcsName** della struttura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) .</span><span class="sxs-lookup"><span data-stu-id="1a413-126">If there is no reasonable name for the byte array, the COM-provided **ILockBytes::Stat** method returns **NULL** in the **pwcsName** member of the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="1a413-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1a413-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a413-128">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="1a413-128">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="1a413-129">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="1a413-129">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="1a413-130">**IStream**</span><span class="sxs-lookup"><span data-stu-id="1a413-130">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




