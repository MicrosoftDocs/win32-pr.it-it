---
title: Implementazione di ILockBytes-File-Based
description: Implementato in un oggetto matrice di byte sottostante un oggetto di archiviazione di file composto COM e progettato per leggere e scrivere direttamente in un file su disco.
ms.assetid: 700b6a3c-1046-4c21-8887-16f344c23510
keywords:
- ILockBytes Strctd STG, implementazioni, basate su file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93dfe09ab0157d2d24d81b7bb2798e984d3848f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395478"
---
# <a name="ilockbytes---file-based-implementation"></a><span data-ttu-id="8a96f-104">Implementazione di ILockBytes-File-Based</span><span class="sxs-lookup"><span data-stu-id="8a96f-104">ILockBytes - File-Based Implementation</span></span>

<span data-ttu-id="8a96f-105">Implementato in un oggetto matrice di byte sottostante un oggetto di archiviazione di file composto COM e progettato per leggere e scrivere direttamente in un file su disco.</span><span class="sxs-lookup"><span data-stu-id="8a96f-105">Implemented on a byte array object underlying a COM compound file storage object, and designed to read and write directly to a disk file.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="8a96f-106">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="8a96f-106">When to Use</span></span>

<span data-ttu-id="8a96f-107">I metodi di [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) vengono chiamati dalle implementazioni di file compositi di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) nell'oggetto di archiviazione di file composto creato tramite una chiamata a [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), pertanto non è necessario chiamarli direttamente.</span><span class="sxs-lookup"><span data-stu-id="8a96f-107">Methods of [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) are called from the compound file implementations of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) and [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) on the compound file storage object created through a call to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), so you do not need to call them directly.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a96f-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="8a96f-108">Remarks</span></span>

<span data-ttu-id="8a96f-109">Di seguito sono riportati i metodi dell'implementazione di File-Based [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) .</span><span class="sxs-lookup"><span data-stu-id="8a96f-109">The following are the methods of the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) File-Based Implementation.</span></span>

<dl> <dt>

<span data-ttu-id="8a96f-110"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: ReadAt**</span><span class="sxs-lookup"><span data-stu-id="8a96f-110"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**</span></span>
</dt> <dd>

<span data-ttu-id="8a96f-111">Legge un blocco di byte da un offset specificato all'inizio della matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="8a96f-111">Reads a block of bytes from a specified offset at the beginning of the byte-array.</span></span>

</dd> <dt>

<span data-ttu-id="8a96f-112"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: WriteAt**</span><span class="sxs-lookup"><span data-stu-id="8a96f-112"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**</span></span>
</dt> <dd>

<span data-ttu-id="8a96f-113">Scrive un blocco di byte da un offset specificato all'inizio della matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="8a96f-113">Writes a block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="8a96f-114"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: Flush**</span><span class="sxs-lookup"><span data-stu-id="8a96f-114"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**</span></span>
</dt> <dd>

<span data-ttu-id="8a96f-115">Garantisce che tutti i buffer interni gestiti dall'implementazione di [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) vengano scritti nell'archiviazione fisica sottostante.</span><span class="sxs-lookup"><span data-stu-id="8a96f-115">Ensures that any internal buffers maintained by the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) implementation are written out to the underlying physical storage.</span></span>

</dd> <dt>

<span data-ttu-id="8a96f-116"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: sesize**</span><span class="sxs-lookup"><span data-stu-id="8a96f-116"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**</span></span>
</dt> <dd>

<span data-ttu-id="8a96f-117">Imposta la dimensione della matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="8a96f-117">Sets the size of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="8a96f-118"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**</span><span class="sxs-lookup"><span data-stu-id="8a96f-118"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="8a96f-119">Il parametro *dwLockTypes* è impostato su lock \_ ONLYONCE o lock \_ Exclusive, che consente o limita l'accesso alle aree bloccate.</span><span class="sxs-lookup"><span data-stu-id="8a96f-119">The *dwLockTypes* parameter is set to LOCK\_ONLYONCE or LOCK\_EXCLUSIVE, which will allow or restrict access to locked regions.</span></span>

</dd> <dt>

<span data-ttu-id="8a96f-120"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="8a96f-120"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="8a96f-121">Questo metodo sblocca l'area bloccata da [**ILockBytes:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).</span><span class="sxs-lookup"><span data-stu-id="8a96f-121">This method unlocks the region locked by [**ILockBytes::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).</span></span>

</dd> <dt>

<span data-ttu-id="8a96f-122"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: stat**</span><span class="sxs-lookup"><span data-stu-id="8a96f-122"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**</span></span>
</dt> <dd>

<span data-ttu-id="8a96f-123">L'implementazione di [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) fornita da com chiama il metodo [**ILockBytes:: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) per recuperare le informazioni sull'oggetto matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="8a96f-123">The COM-provided [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) implementation calls the [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) method to retrieve information about the byte array object.</span></span> <span data-ttu-id="8a96f-124">Se non esiste un nome ragionevole per la matrice di byte, il metodo **ILockBytes:: stat** fornito da com **restituisce null** nel membro **pwcsName** della struttura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) .</span><span class="sxs-lookup"><span data-stu-id="8a96f-124">If there is no reasonable name for the byte array, the COM-provided **ILockBytes::Stat** method returns **NULL** in the **pwcsName** member of the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="8a96f-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a96f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a96f-126">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="8a96f-126">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="8a96f-127">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="8a96f-127">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="8a96f-128">**IStream**</span><span class="sxs-lookup"><span data-stu-id="8a96f-128">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




