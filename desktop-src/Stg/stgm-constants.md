---
title: Costanti STGM (ObjBase. h)
description: Flag che indicano le condizioni per la creazione e l'eliminazione di oggetti e modalità di accesso per l'oggetto.
ms.assetid: 15a35da9-332a-46e1-9190-500c95e26f59
topic_type:
- apiref
api_name:
- STGM_READ
- STGM_WRITE
- STGM_READWRITE
- STGM_SHARE_DENY_NONE
- STGM_SHARE_DENY_READ
- STGM_SHARE_DENY_WRITE
- STGM_SHARE_EXCLUSIVE
- STGM_PRIORITY
- STGM_CREATE
- STGM_CONVERT
- STGM_FAILIFTHERE
- STGM_DIRECT
- STGM_TRANSACTED
- STGM_NOSCRATCH
- STGM_NOSNAPSHOT
- STGM_SIMPLE
- STGM_DIRECT_SWMR
- STGM_DELETEONRELEASE
api_location:
- ObjBase.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd283c2dfeddc48b6bd12f8317ec352cb62e4973
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475479"
---
# <a name="stgm-constants"></a><span data-ttu-id="1e2ca-103">Costanti STGM</span><span class="sxs-lookup"><span data-stu-id="1e2ca-103">STGM Constants</span></span>

<span data-ttu-id="1e2ca-104">Le costanti STGM sono flag che indicano le condizioni per la creazione e l'eliminazione di oggetti e modalità di accesso per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-104">The STGM constants are flags that indicate conditions for creating and deleting the object and access modes for the object.</span></span> <span data-ttu-id="1e2ca-105">Le costanti STGM sono incluse nelle interfacce [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) e nelle funzioni [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) [**, StgCreateDocfileOnILockBytes,**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes) [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)e [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) .</span><span class="sxs-lookup"><span data-stu-id="1e2ca-105">The STGM constants are included in the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), and [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interfaces and in the [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgCreateDocfileOnILockBytes**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage), and [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) functions.</span></span>

<span data-ttu-id="1e2ca-106">Questi elementi vengono spesso combinati usando un operatore **or**.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-106">These elements are often combined using an **OR** operator.</span></span> <span data-ttu-id="1e2ca-107">Sono interpretati in gruppi, come indicato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-107">They are interpreted in groups as listed in the following table.</span></span> <span data-ttu-id="1e2ca-108">Non è possibile usare più di un elemento di un singolo gruppo.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-108">It is not valid to use more than one element from a single group.</span></span>

<span data-ttu-id="1e2ca-109">Usare un flag dal gruppo di creazione quando si crea un oggetto, ad esempio con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) o [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="1e2ca-109">Use a flag from the creation group when creating an object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) or [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span>

<span data-ttu-id="1e2ca-110">Per ulteriori informazioni sulle transazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-110">For more information about transactioning, see the Remarks section.</span></span>



| <span data-ttu-id="1e2ca-111">Group</span><span class="sxs-lookup"><span data-stu-id="1e2ca-111">Group</span></span>                      | <span data-ttu-id="1e2ca-112">Flag</span><span class="sxs-lookup"><span data-stu-id="1e2ca-112">Flag</span></span>                         | <span data-ttu-id="1e2ca-113">valore</span><span class="sxs-lookup"><span data-stu-id="1e2ca-113">Value</span></span>       |
|----------------------------|------------------------------|-------------|
| <span data-ttu-id="1e2ca-114">Access</span><span class="sxs-lookup"><span data-stu-id="1e2ca-114">Access</span></span>                     | <span data-ttu-id="1e2ca-115">**STGM di \_ lettura**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-115">**STGM\_READ**</span></span>               | <span data-ttu-id="1e2ca-116">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-116">0x00000000L</span></span> |
|                            | <span data-ttu-id="1e2ca-117">**\_scrittura STGM**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-117">**STGM\_WRITE**</span></span>              | <span data-ttu-id="1e2ca-118">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-118">0x00000001L</span></span> |
|                            | <span data-ttu-id="1e2ca-119">**\_ReadWrite STGM**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-119">**STGM\_READWRITE**</span></span>          | <span data-ttu-id="1e2ca-120">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-120">0x00000002L</span></span> |
| <span data-ttu-id="1e2ca-121">Condivisione</span><span class="sxs-lookup"><span data-stu-id="1e2ca-121">Sharing</span></span>                    | <span data-ttu-id="1e2ca-122">**STGM \_ condivisione \_ Nega \_ Nessuna**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-122">**STGM\_SHARE\_DENY\_NONE**</span></span>  | <span data-ttu-id="1e2ca-123">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-123">0x00000040L</span></span> |
|                            | <span data-ttu-id="1e2ca-124">**STGM \_ condivisione \_ Nega \_ lettura**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-124">**STGM\_SHARE\_DENY\_READ**</span></span>  | <span data-ttu-id="1e2ca-125">0x00000030L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-125">0x00000030L</span></span> |
|                            | <span data-ttu-id="1e2ca-126">**STGM \_ condivisione \_ Nega \_ scrittura**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-126">**STGM\_SHARE\_DENY\_WRITE**</span></span> | <span data-ttu-id="1e2ca-127">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-127">0x00000020L</span></span> |
|                            | <span data-ttu-id="1e2ca-128">**STGM \_ condivisione \_ esclusiva**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-128">**STGM\_SHARE\_EXCLUSIVE**</span></span>   | <span data-ttu-id="1e2ca-129">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-129">0x00000010L</span></span> |
|                            | <span data-ttu-id="1e2ca-130">**\_priorità STGM**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-130">**STGM\_PRIORITY**</span></span>           | <span data-ttu-id="1e2ca-131">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-131">0x00040000L</span></span> |
| <span data-ttu-id="1e2ca-132">Creazione</span><span class="sxs-lookup"><span data-stu-id="1e2ca-132">Creation</span></span>                   | <span data-ttu-id="1e2ca-133">**creazione di STGM \_**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-133">**STGM\_CREATE**</span></span>             | <span data-ttu-id="1e2ca-134">0x00001000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-134">0x00001000L</span></span> |
|                            | <span data-ttu-id="1e2ca-135">**STGM \_ convertire**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-135">**STGM\_CONVERT**</span></span>            | <span data-ttu-id="1e2ca-136">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-136">0x00020000L</span></span> |
|                            | <span data-ttu-id="1e2ca-137">**\_FAILIFTHERE STGM**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-137">**STGM\_FAILIFTHERE**</span></span>        | <span data-ttu-id="1e2ca-138">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-138">0x00000000L</span></span> |
| <span data-ttu-id="1e2ca-139">Transazione</span><span class="sxs-lookup"><span data-stu-id="1e2ca-139">Transactioning</span></span>             | <span data-ttu-id="1e2ca-140">**STGM \_ Direct**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-140">**STGM\_DIRECT**</span></span>             | <span data-ttu-id="1e2ca-141">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-141">0x00000000L</span></span> |
|                            | <span data-ttu-id="1e2ca-142">**STGM \_ transazionale**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-142">**STGM\_TRANSACTED**</span></span>         | <span data-ttu-id="1e2ca-143">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-143">0x00010000L</span></span> |
| <span data-ttu-id="1e2ca-144">Prestazioni delle transazioni</span><span class="sxs-lookup"><span data-stu-id="1e2ca-144">Transactioning Performance</span></span> | <span data-ttu-id="1e2ca-145">**STGM \_ NOscratch**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-145">**STGM\_NOSCRATCH**</span></span>          | <span data-ttu-id="1e2ca-146">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-146">0x00100000L</span></span> |
|                            | <span data-ttu-id="1e2ca-147">**STGM \_ NOsnapshot**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-147">**STGM\_NOSNAPSHOT**</span></span>         | <span data-ttu-id="1e2ca-148">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-148">0x00200000L</span></span> |
| <span data-ttu-id="1e2ca-149">SWMR diretto e semplice</span><span class="sxs-lookup"><span data-stu-id="1e2ca-149">Direct SWMR and Simple</span></span>     | <span data-ttu-id="1e2ca-150">**STGM \_ semplice**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-150">**STGM\_SIMPLE**</span></span>             | <span data-ttu-id="1e2ca-151">0x08000000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-151">0x08000000L</span></span> |
|                            | <span data-ttu-id="1e2ca-152">**\_SWMR diretto \_ STGM**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-152">**STGM\_DIRECT\_SWMR**</span></span>       | <span data-ttu-id="1e2ca-153">0x00400000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-153">0x00400000L</span></span> |
| <span data-ttu-id="1e2ca-154">Elimina al rilascio</span><span class="sxs-lookup"><span data-stu-id="1e2ca-154">Delete On Release</span></span>          | <span data-ttu-id="1e2ca-155">**\_DELETEONRELEASE STGM**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-155">**STGM\_DELETEONRELEASE**</span></span>    | <span data-ttu-id="1e2ca-156">0x04000000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-156">0x04000000L</span></span> |



 

<dl> <dt>

<span data-ttu-id="1e2ca-157"><span id="STGM_READ"></span><span id="stgm_read"></span>**STGM di \_ lettura**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-157"><span id="STGM_READ"></span><span id="stgm_read"></span>**STGM\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-158">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-158">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-159">Indica che l'oggetto è di sola lettura, pertanto non è possibile apportare modifiche.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-159">Indicates that the object is read-only, meaning that modifications cannot be made.</span></span> <span data-ttu-id="1e2ca-160">Se, ad esempio, un oggetto flusso viene aperto con **STGM \_ Read**, il metodo [**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) può essere chiamato, ma il metodo [**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) non può essere.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-160">For example, if a stream object is opened with **STGM\_READ**, the [**ISequentialStream::Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) method may be called, but the [**ISequentialStream::Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) method may not.</span></span> <span data-ttu-id="1e2ca-161">Analogamente, se si apre un oggetto di archiviazione con **STGM \_ Read**, è possibile chiamare i metodi [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) e [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) , ma i metodi [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) e [**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) non possono essere.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-161">Similarly, if a storage object opened with **STGM\_READ**, the [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) and [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) methods may be called, but the [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) and [**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) methods may not.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-162"><span id="STGM_WRITE"></span><span id="stgm_write"></span>**\_scrittura STGM**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-162"><span id="STGM_WRITE"></span><span id="stgm_write"></span>**STGM\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-163">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-163">0x00000001L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-164">Consente di salvare le modifiche apportate all'oggetto, ma non di consentire l'accesso ai relativi dati.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-164">Enables you to save changes to the object, but does not permit access to its data.</span></span> <span data-ttu-id="1e2ca-165">Le implementazioni fornite delle interfacce [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) e [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) non supportano questa modalità di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-165">The provided implementations of the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) and [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) interfaces do not support this write-only mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-166"><span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**\_ReadWrite STGM**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-166"><span id="STGM_READWRITE"></span><span id="stgm_readwrite"></span>**STGM\_READWRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-167">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-167">0x00000002L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-168">Consente l'accesso e la modifica dei dati degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-168">Enables access and modification of object data.</span></span> <span data-ttu-id="1e2ca-169">Se, ad esempio, un oggetto flusso viene creato o aperto in questa modalità, è possibile chiamare sia [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) che **IStream:: Write**.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-169">For example, if a stream object is created or opened in this mode, it is possible to call both [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) and **IStream::Write**.</span></span> <span data-ttu-id="1e2ca-170">Tenere presente che questa costante non è una semplice operazione binaria **o** con gli elementi **\_ Read** di **STGM \_ Write** e STGM.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-170">Be aware that this constant is not a simple binary **OR** operation of the **STGM\_WRITE** and **STGM\_READ** elements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-171"><span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM \_ condivisione \_ Nega \_ Nessuna**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-171"><span id="STGM_SHARE_DENY_NONE"></span><span id="stgm_share_deny_none"></span>**STGM\_SHARE\_DENY\_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-172">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-172">0x00000040L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-173">Specifica che le aperture successive dell'oggetto non sono negate per l'accesso in lettura o in scrittura.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-173">Specifies that subsequent openings of the object are not denied read or write access.</span></span> <span data-ttu-id="1e2ca-174">Se non viene specificato alcun flag dal gruppo di condivisione, viene utilizzato questo flag.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-174">If no flag from the sharing group is specified, this flag is assumed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-175"><span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM \_ condivisione \_ Nega \_ lettura**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-175"><span id="STGM_SHARE_DENY_READ"></span><span id="stgm_share_deny_read"></span>**STGM\_SHARE\_DENY\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-176">0x00000030L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-176">0x00000030L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-177">Impedisce ad altri utenti di aprire successivamente l'oggetto in modalità di **\_ lettura STGM** .</span><span class="sxs-lookup"><span data-stu-id="1e2ca-177">Prevents others from subsequently opening the object in **STGM\_READ** mode.</span></span> <span data-ttu-id="1e2ca-178">Viene in genere usato in un oggetto di archiviazione radice.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-178">It is typically used on a root storage object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-179"><span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM \_ condivisione \_ Nega \_ scrittura**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-179"><span id="STGM_SHARE_DENY_WRITE"></span><span id="stgm_share_deny_write"></span>**STGM\_SHARE\_DENY\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-180">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-180">0x00000020L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-181">Impedisce ad altri utenti di aprire successivamente l'oggetto per l'accesso **STGM \_ Write** o **STGM \_ ReadWrite** .</span><span class="sxs-lookup"><span data-stu-id="1e2ca-181">Prevents others from subsequently opening the object for **STGM\_WRITE** or **STGM\_READWRITE** access.</span></span> <span data-ttu-id="1e2ca-182">In modalità transazionale, la condivisione della condivisione **STGM \_ \_ Deny \_ Write** o **STGM \_ share \_ Exclusive** può migliorare significativamente le prestazioni, in quanto non richiedono snapshot.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-182">In transacted mode, sharing of **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** can significantly improve performance because they do not require snapshots.</span></span> <span data-ttu-id="1e2ca-183">Per ulteriori informazioni sulle transazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-183">For more information about transactioning, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-184"><span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM \_ condivisione \_ esclusiva**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-184"><span id="STGM_SHARE_EXCLUSIVE"></span><span id="stgm_share_exclusive"></span>**STGM\_SHARE\_EXCLUSIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-185">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-185">0x00000010L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-186">Impedisce ad altri utenti di aprire successivamente l'oggetto in qualsiasi modalità.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-186">Prevents others from subsequently opening the object in any mode.</span></span> <span data-ttu-id="1e2ca-187">Tenere presente che questo valore non è una **semplice operazione or** bit per bit della **\_ condivisione STGM \_ Deny \_ Read** e **STGM \_ share \_ Deny \_ Write** values.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-187">Be aware that this value is not a simple bitwise **OR** operation of the **STGM\_SHARE\_DENY\_READ** and **STGM\_SHARE\_DENY\_WRITE** values.</span></span> <span data-ttu-id="1e2ca-188">In modalità transazionale, la condivisione della condivisione **STGM \_ \_ Deny \_ Write** o **STGM \_ share \_ Exclusive** può migliorare significativamente le prestazioni, in quanto non richiedono snapshot.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-188">In transacted mode, sharing of **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** can significantly improve performance because they do not require snapshots.</span></span> <span data-ttu-id="1e2ca-189">Per ulteriori informazioni sulle transazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-189">For more information about transactioning, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-190"><span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**\_priorità STGM**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-190"><span id="STGM_PRIORITY"></span><span id="stgm_priority"></span>**STGM\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-191">0x00040000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-191">0x00040000L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-192">Apre l'oggetto di archiviazione con accesso esclusivo alla versione di cui è stato eseguito il commit più di recente.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-192">Opens the storage object with exclusive access to the most recently committed version.</span></span> <span data-ttu-id="1e2ca-193">Di conseguenza, gli altri utenti non possono eseguire il commit delle modifiche all'oggetto mentre è aperto in modalità di priorità.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-193">Thus, other users cannot commit changes to the object while you have it open in priority mode.</span></span> <span data-ttu-id="1e2ca-194">Si ottengono vantaggi in termini di prestazioni per le operazioni di copia, ma si impedisce ad altri utenti di eseguire il commit delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-194">You gain performance benefits for copy operations, but you prevent others from committing changes.</span></span> <span data-ttu-id="1e2ca-195">Limitare il tempo in cui gli oggetti vengono aperti in modalità di priorità.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-195">Limit the time that objects are open in priority mode.</span></span> <span data-ttu-id="1e2ca-196">È necessario specificare **STGM \_ Direct** e **STGM \_ Read** con la modalità Priority e non è possibile specificare **STGM \_ DELETEONRELEASE**.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-196">You must specify **STGM\_DIRECT** and **STGM\_READ** with priority mode, and you cannot specify **STGM\_DELETEONRELEASE**.</span></span> <span data-ttu-id="1e2ca-197">**STGM \_ DELETEONRELEASE** è valido solo quando si crea un oggetto radice, ad esempio con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span><span class="sxs-lookup"><span data-stu-id="1e2ca-197">**STGM\_DELETEONRELEASE** is only valid when creating a root object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="1e2ca-198">Non è valido quando si apre un oggetto radice esistente, ad esempio con [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span><span class="sxs-lookup"><span data-stu-id="1e2ca-198">It is not valid when opening an existing root object, such as with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span></span> <span data-ttu-id="1e2ca-199">Non è inoltre valido quando si crea o si apre un sottoelemento, ad esempio con [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).</span><span class="sxs-lookup"><span data-stu-id="1e2ca-199">It is also not valid when creating or opening a subelement, such as with [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-200"><span id="STGM_CREATE"></span><span id="stgm_create"></span>**creazione di STGM \_**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-200"><span id="STGM_CREATE"></span><span id="stgm_create"></span>**STGM\_CREATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-201">0x00001000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-201">0x00001000L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-202">Indica che un oggetto o un flusso di archiviazione esistente deve essere rimosso prima che il nuovo oggetto lo sostituisca.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-202">Indicates that an existing storage object or stream should be removed before the new object replaces it.</span></span> <span data-ttu-id="1e2ca-203">Quando questo flag viene specificato solo se l'oggetto esistente è stato rimosso correttamente, viene creato un nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-203">A new object is created when this flag is specified only if the existing object has been successfully removed.</span></span>

<span data-ttu-id="1e2ca-204">Questo flag viene usato durante il tentativo di creazione:</span><span class="sxs-lookup"><span data-stu-id="1e2ca-204">This flag is used when attempting to create:</span></span>

-   <span data-ttu-id="1e2ca-205">Un oggetto di archiviazione su un disco, ma esiste un file con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-205">A storage object on a disk, but a file of that name exists.</span></span>
-   <span data-ttu-id="1e2ca-206">Oggetto all'interno di un oggetto di archiviazione, ma esiste un oggetto con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-206">An object inside a storage object, but an object with the specified name exists.</span></span>
-   <span data-ttu-id="1e2ca-207">Un oggetto matrice di byte, ma ne esiste uno con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-207">A byte array object, but one with the specified name exists.</span></span>

<span data-ttu-id="1e2ca-208">Questo flag non può essere usato con le operazioni aperte, ad esempio [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) o [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).</span><span class="sxs-lookup"><span data-stu-id="1e2ca-208">This flag cannot be used with open operations, such as [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) or [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-209"><span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM \_ convertire**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-209"><span id="STGM_CONVERT"></span><span id="stgm_convert"></span>**STGM\_CONVERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-210">0x00020000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-210">0x00020000L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-211">Crea il nuovo oggetto conservando i dati esistenti in un flusso denominato "Contents".</span><span class="sxs-lookup"><span data-stu-id="1e2ca-211">Creates the new object while preserving existing data in a stream named "Contents".</span></span> <span data-ttu-id="1e2ca-212">Nel caso di un oggetto di archiviazione o di una matrice di byte, i dati obsoleti vengono formattati in un flusso, indipendentemente dal fatto che la matrice di byte o il file esistente contenga attualmente un oggetto di archiviazione a più livelli.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-212">In the case of a storage object or a byte array, the old data is formatted into a stream regardless of whether the existing file or byte array currently contains a layered storage object.</span></span> <span data-ttu-id="1e2ca-213">Questo flag può essere utilizzato solo quando si crea un oggetto di archiviazione radice.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-213">This flag can only be used when creating a root storage object.</span></span> <span data-ttu-id="1e2ca-214">Non può essere usato in un oggetto di archiviazione. ad esempio, in [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="1e2ca-214">It cannot be used within a storage object; for example, in [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span> <span data-ttu-id="1e2ca-215">Non è inoltre valido utilizzare questo flag e il flag **STGM \_ DELETEONRELEASE** simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-215">It is also not valid to use this flag and the **STGM\_DELETEONRELEASE** flag simultaneously.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-216"><span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**\_FAILIFTHERE STGM**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-216"><span id="STGM_FAILIFTHERE"></span><span id="stgm_failifthere"></span>**STGM\_FAILIFTHERE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-217">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-217">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-218">Causa l'esito negativo dell'operazione di creazione se è presente un oggetto esistente con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-218">Causes the create operation to fail if an existing object with the specified name exists.</span></span> <span data-ttu-id="1e2ca-219">In questo caso, viene restituito **STG \_ E \_ FILEALREADYEXISTS** .</span><span class="sxs-lookup"><span data-stu-id="1e2ca-219">In this case, **STG\_E\_FILEALREADYEXISTS** is returned.</span></span> <span data-ttu-id="1e2ca-220">Questa è la modalità di creazione predefinita; ovvero, se non viene specificato nessun altro flag di creazione, **STGM \_ FAILIFTHERE** è implicito.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-220">This is the default creation mode; that is, if no other create flag is specified, **STGM\_FAILIFTHERE** is implied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-221"><span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM \_ Direct**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-221"><span id="STGM_DIRECT"></span><span id="stgm_direct"></span>**STGM\_DIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-222">0x00000000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-222">0x00000000L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-223">Indica che, in modalità diretta, ogni modifica apportata a un elemento di archiviazione o flusso viene scritta quando si verifica.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-223">Indicates that, in direct mode, each change to a storage or stream element is written as it occurs.</span></span> <span data-ttu-id="1e2ca-224">Si tratta dell'impostazione predefinita se non viene specificato né **STGM \_ Direct** né **STGM \_ transazionale** .</span><span class="sxs-lookup"><span data-stu-id="1e2ca-224">This is the default if neither **STGM\_DIRECT** nor **STGM\_TRANSACTED** is specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-225"><span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM \_ transazionale**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-225"><span id="STGM_TRANSACTED"></span><span id="stgm_transacted"></span>**STGM\_TRANSACTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-226">0x00010000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-226">0x00010000L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-227">Indica che, in modalità transazionale, le modifiche vengono memorizzate nel buffer e scritte solo se viene chiamata un'operazione di commit esplicita.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-227">Indicates that, in transacted mode, changes are buffered and written only if an explicit commit operation is called.</span></span> <span data-ttu-id="1e2ca-228">Per ignorare le modifiche, chiamare il metodo [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) nell'interfaccia [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)o [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) .</span><span class="sxs-lookup"><span data-stu-id="1e2ca-228">To ignore the changes, call the [**Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert) method in the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), or [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface.</span></span> <span data-ttu-id="1e2ca-229">L'implementazione del file composto COM di **IStorage** non supporta i flussi transazionali, il che significa che i flussi possono essere aperti solo in modalità diretta e non è possibile ripristinare le modifiche, tuttavia sono supportate le archiviazioni transazionali.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-229">The COM compound file implementation of **IStorage** does not support transacted streams, which means that streams can be opened only in direct mode, and you cannot revert changes to them, however transacted storages are supported.</span></span> <span data-ttu-id="1e2ca-230">Le implementazioni di file composto, autonome e file system NTFS di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) in modo analogo non supportano i set di proprietà semplici e sottoposti a transazione, perché questi set di proprietà sono archiviati nei flussi.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-230">The compound file, stand-alone, and NTFS file system implementations of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) similarly do not support transacted, simple property sets because these property sets are stored in streams.</span></span> <span data-ttu-id="1e2ca-231">Tuttavia, sono supportate le transazioni di set di proprietà non semplici, che possono essere creati specificando il flag **PROPSETFLAG non \_ semplice** nel parametro *grfFlags* di [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create).</span><span class="sxs-lookup"><span data-stu-id="1e2ca-231">However, transactioning of nonsimple property sets, which can be created by specifying the **PROPSETFLAG\_NONSIMPLE** flag in the *grfFlags* parameter of [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), are supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-232"><span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM \_ NOscratch**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-232"><span id="STGM_NOSCRATCH"></span><span id="stgm_noscratch"></span>**STGM\_NOSCRATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-233">0x00100000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-233">0x00100000L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-234">Indica che, in modalità transazionale, viene in genere utilizzato un file temporaneo temporaneo per salvare le modifiche fino a quando non viene chiamato il metodo **commit** .</span><span class="sxs-lookup"><span data-stu-id="1e2ca-234">Indicates that, in transacted mode, a temporary scratch file is usually used to save modifications until the **Commit** method is called.</span></span> <span data-ttu-id="1e2ca-235">La specifica di **STGM \_ noscratch** consente di usare come spazio di lavoro la parte inutilizzata del file originale anziché creare un nuovo file a tale scopo.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-235">Specifying **STGM\_NOSCRATCH** permits the unused portion of the original file to be used as work space instead of creating a new file for that purpose.</span></span> <span data-ttu-id="1e2ca-236">Questa operazione non influisce sui dati nel file originale e in alcuni casi può comportare un miglioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-236">This does not affect the data in the original file, and in certain cases can result in improved performance.</span></span> <span data-ttu-id="1e2ca-237">Non è consentito specificare questo flag senza specificare anche **STGM \_ transazionale** e questo flag può essere utilizzato solo in una radice aperta.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-237">It is not valid to specify this flag without also specifying **STGM\_TRANSACTED**, and this flag may only be used in a root open.</span></span> <span data-ttu-id="1e2ca-238">Per ulteriori informazioni sulla modalità noscratch, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-238">For more information about NoScratch mode, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-239"><span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM \_ NOsnapshot**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-239"><span id="STGM_NOSNAPSHOT"></span><span id="stgm_nosnapshot"></span>**STGM\_NOSNAPSHOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-240">0x00200000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-240">0x00200000L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-241">Questo flag viene usato per l'apertura di un oggetto di archiviazione con **STGM \_ transazionale** e senza **STGM \_ share \_ Exclusive** o **STGM \_ share \_ Deny \_ Write**.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-241">This flag is used when opening a storage object with **STGM\_TRANSACTED** and without **STGM\_SHARE\_EXCLUSIVE** or **STGM\_SHARE\_DENY\_WRITE**.</span></span> <span data-ttu-id="1e2ca-242">In questo caso, se si specifica **STGM \_ nosnapshot** si impedisce all'implementazione fornita dal sistema di creare una copia snapshot del file.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-242">In this case, specifying **STGM\_NOSNAPSHOT** prevents the system-provided implementation from creating a snapshot copy of the file.</span></span> <span data-ttu-id="1e2ca-243">Al contrario, le modifiche apportate al file vengono scritte alla fine del file.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-243">Instead, changes to the file are written to the end of the file.</span></span> <span data-ttu-id="1e2ca-244">Lo spazio inutilizzato non viene recuperato a meno che non venga eseguito il consolidamento durante il commit ed è presente un solo writer corrente sul file.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-244">Unused space is not reclaimed unless consolidation is performed during the commit, and there is only one current writer on the file.</span></span> <span data-ttu-id="1e2ca-245">Quando il file viene aperto in modalità senza snapshot, non è possibile eseguire un'altra operazione di apertura senza specificare **STGM \_ nosnapshot**.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-245">When the file is opened in no snapshot mode, another open operation cannot be performed without specifying **STGM\_NOSNAPSHOT**.</span></span> <span data-ttu-id="1e2ca-246">Questo flag può essere utilizzato solo in un'operazione di apertura radice.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-246">This flag may only be used in a root open operation.</span></span> <span data-ttu-id="1e2ca-247">Per ulteriori informazioni sulla modalità nosnapshot, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-247">For more information about NoSnapshot mode, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-248"><span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM \_ semplice**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-248"><span id="STGM_SIMPLE"></span><span id="stgm_simple"></span>**STGM\_SIMPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-249">0x08000000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-249">0x08000000L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-250">Fornisce un'implementazione più veloce di un file composto in un caso limitato, ma di uso frequente.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-250">Provides a faster implementation of a compound file in a limited, but frequently used, case.</span></span> <span data-ttu-id="1e2ca-251">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-251">For more information, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-252"><span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**\_SWMR diretto \_ STGM**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-252"><span id="STGM_DIRECT_SWMR"></span><span id="stgm_direct_swmr"></span>**STGM\_DIRECT\_SWMR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-253">0x00400000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-253">0x00400000L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-254">Supporta la modalità diretta per le operazioni su file a writer singolo e Multireader.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-254">Supports direct mode for single-writer, multireader file operations.</span></span> <span data-ttu-id="1e2ca-255">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-255">For more information, see the Remarks section.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1e2ca-256"><span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**\_DELETEONRELEASE STGM**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-256"><span id="STGM_DELETEONRELEASE"></span><span id="stgm_deleteonrelease"></span>**STGM\_DELETEONRELEASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e2ca-257">0x04000000L</span><span class="sxs-lookup"><span data-stu-id="1e2ca-257">0x04000000L</span></span>
</dt> <dt>



<span data-ttu-id="1e2ca-258">Indica che il file sottostante deve essere eliminato automaticamente quando viene rilasciato l'oggetto di archiviazione radice.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-258">Indicates that the underlying file is to be automatically destroyed when the root storage object is released.</span></span> <span data-ttu-id="1e2ca-259">Questa funzionalità è particolarmente utile per la creazione di file temporanei.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-259">This feature is most useful for creating temporary files.</span></span> <span data-ttu-id="1e2ca-260">Questo flag può essere utilizzato solo quando si crea un oggetto radice, ad esempio con [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span><span class="sxs-lookup"><span data-stu-id="1e2ca-260">This flag can only be used when creating a root object, such as with [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="1e2ca-261">Non è valido quando si apre un oggetto radice, ad esempio con [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), o quando si crea o si apre un sottoelemento, ad esempio con [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span><span class="sxs-lookup"><span data-stu-id="1e2ca-261">It is not valid when opening a root object, such as with [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex), or when creating or opening a subelement, such as with [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream).</span></span> <span data-ttu-id="1e2ca-262">Non è inoltre valido utilizzare questo flag e il \_ flag di conversione STGM simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-262">It is also not valid to use this flag and the STGM\_CONVERT flag simultaneously.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e2ca-263">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e2ca-263">Remarks</span></span>

<span data-ttu-id="1e2ca-264">È possibile combinare questi flag, ma è possibile scegliere solo un flag da ogni gruppo di flag correlati.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-264">You can combine these flags, but you can only choose one flag from each group of related flags.</span></span> <span data-ttu-id="1e2ca-265">In genere, è necessario specificare un flag da ognuno dei gruppi di accesso e condivisione per tutte le funzioni e i metodi che usano queste costanti.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-265">Typically one flag from each of the access and sharing groups must be specified for all functions and methods which use these constants.</span></span> <span data-ttu-id="1e2ca-266">I flag di altri gruppi sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-266">Flags from other groups are optional.</span></span>

### <a name="transacted-mode"></a><span data-ttu-id="1e2ca-267">Modalità transazionale</span><span class="sxs-lookup"><span data-stu-id="1e2ca-267">Transacted Mode</span></span>

<span data-ttu-id="1e2ca-268">Quando viene specificato il flag **\_ diretto STGM**, è possibile specificare solo una delle seguenti combinazioni di flag dai gruppi di accesso e condivisione.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-268">When the **STGM\_DIRECT** flag is specified, only one of the following combination of flags may be specified from the access and sharing groups.</span></span>

``` syntax
    STGM_READ      | STGM_SHARE_DENY_WRITE
```

``` syntax
    STGM_READWRITE | STGM_SHARE_EXCLUSIVE
```

``` syntax
    STGM_READ      | STGM_PRIORITY
```

<span data-ttu-id="1e2ca-269">Tenere presente che la modalità diretta è implicita in assenza di **STGM \_ transazionale**.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-269">Be aware that direct mode is implied by the absence of **STGM\_TRANSACTED**.</span></span> <span data-ttu-id="1e2ca-270">Ovvero, se non si specifica né **STGM \_ Direct** né **STGM \_ transazionale** , viene utilizzato **STGM \_ Direct** .</span><span class="sxs-lookup"><span data-stu-id="1e2ca-270">That is, if neither **STGM\_DIRECT** nor **STGM\_TRANSACTED** is specified, **STGM\_DIRECT** is assumed.</span></span>

<span data-ttu-id="1e2ca-271">Quando viene specificato il flag **\_ transazionale STGM** , gli oggetti vengono creati o aperti in modalità transazionale.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-271">When the **STGM\_TRANSACTED** flag is specified, objects are created or opened in transacted mode.</span></span> <span data-ttu-id="1e2ca-272">In questa modalità le modifiche apportate a un oggetto non vengono mantenute finché non ne viene eseguito il commit.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-272">In this mode, changes to an object do not persist until they are committed.</span></span> <span data-ttu-id="1e2ca-273">Ad esempio, le modifiche apportate a un oggetto di archiviazione transazionale non vengono rese permanente fino a quando non viene chiamato il metodo [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) .</span><span class="sxs-lookup"><span data-stu-id="1e2ca-273">For example, changes to a transacted storage object are not persisted until the [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) method is called.</span></span> <span data-ttu-id="1e2ca-274">Le modifiche apportate a tale oggetto di archiviazione andranno perse se l'oggetto di archiviazione viene rilasciato (versione finale) prima della chiamata al metodo **commit** o se viene chiamato il metodo [**IStorage:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) .</span><span class="sxs-lookup"><span data-stu-id="1e2ca-274">Changes to such a storage object will be lost if the storage object is released (final release) before the **Commit** method is called, or if the [**IStorage::Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert) method is called.</span></span>

<span data-ttu-id="1e2ca-275">Quando un oggetto viene creato o aperto in modalità transazionale, l'implementazione deve tenere i dati originali e gli aggiornamenti a questi dati, in modo che gli aggiornamenti possano essere ripristinati, se necessario.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-275">When an object is created or opened in transacted mode, the implementation must keep both the original data and updates to this data, so that updates can be reverted if necessary.</span></span> <span data-ttu-id="1e2ca-276">Questa operazione viene in genere eseguita scrivendo modifiche a un'area scratch finché non ne viene eseguito il commit oppure creando una copia, denominata snapshot, dei dati di cui è stato eseguito il commit più di recente.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-276">This is typically performed by writing changes to a scratch area until they are committed, or by creating a copy, called a snapshot, of the most recently committed data.</span></span>

<span data-ttu-id="1e2ca-277">Quando un oggetto di archiviazione radice viene aperto in modalità transazionale, è possibile controllare la posizione e il comportamento dei dati Scratch e delle copie di snapshot per ottimizzare le prestazioni con i flag **STGM \_ noscratch** e **STGM \_ nosnapshot** .</span><span class="sxs-lookup"><span data-stu-id="1e2ca-277">When a root storage object is opened in transacted mode, the location and behavior of the scratch data and the snapshot copies can be controlled to optimize performance with the **STGM\_NOSCRATCH** and **STGM\_NOSNAPSHOT** flags.</span></span> <span data-ttu-id="1e2ca-278">Viene ottenuto un oggetto di archiviazione radice, ad esempio, la funzione [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . un oggetto di archiviazione ottenuto dal metodo [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) è un oggetto di archiviazione. In genere, i dati e gli snapshot vengono archiviati in file temporanei, separati dalla risorsa di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-278">(A root storage object is obtained from, for example, the [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) function; a storage object obtained from the [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) method is a substorage object.) Typically, the scratch data and snapshots are stored in temporary files, separate from the storage.</span></span>

<span data-ttu-id="1e2ca-279">L'effetto di questi flag dipende dal numero di lettori e/o writer che accedono all'archiviazione radice.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-279">The effect of these flags depends on the number of readers and/or writers accessing the root storage.</span></span>

<span data-ttu-id="1e2ca-280">Nel caso di un singolo writer, viene aperto un oggetto di archiviazione in modalità transazionale per l'accesso in scrittura e non è possibile accedere al file.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-280">In the "single-writer" case, a transacted mode storage object is opened for write access and there can be no other access to the file.</span></span> <span data-ttu-id="1e2ca-281">Ovvero il file viene aperto con **STGM \_ transazionale**, l'accesso **STGM \_ Write** o **STGM \_ ReadWrite** e la condivisione di **STGM \_ share \_ Exclusive**.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-281">That is, the file is opened with **STGM\_TRANSACTED**, access of **STGM\_WRITE** or **STGM\_READWRITE**, and sharing of **STGM\_SHARE\_EXCLUSIVE**.</span></span> <span data-ttu-id="1e2ca-282">In questo caso, le modifiche apportate all'oggetto di archiviazione vengono scritte nell'area scratch.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-282">In this case, changes to the storage object are written to the scratch area.</span></span> <span data-ttu-id="1e2ca-283">Quando si esegue il commit di tali modifiche, queste vengono copiate nella risorsa di archiviazione originale.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-283">When those changes are committed, they are copied to the original storage.</span></span> <span data-ttu-id="1e2ca-284">Di conseguenza, se non vengono apportate modifiche all'oggetto di archiviazione, non sarà necessario alcun trasferimento di dati.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-284">Therefore, if no changes are actually made to the storage object, there will be no unnecessary data transfer.</span></span>

<span data-ttu-id="1e2ca-285">Nel caso di più writer, viene aperto un oggetto di archiviazione transazionale per l'accesso in scrittura, ma è condiviso in tali asway come per consentire altri writer.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-285">In the "multiple-writer" case, a transacted storage object is opened for write access, but is shared in such asway as to allow other writers.</span></span> <span data-ttu-id="1e2ca-286">Ovvero l'oggetto di archiviazione viene aperto con **STGM \_ transazionale**, l'accesso **STGM \_ Write** o **STGM \_ ReadWrite** e la condivisione della **condivisione \_ STGM \_ Deny \_ Read**.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-286">That is, the storage object is opened with **STGM\_TRANSACTED**, access of **STGM\_WRITE** or **STGM\_READWRITE**, and sharing of **STGM\_SHARE\_DENY\_READ**.</span></span> <span data-ttu-id="1e2ca-287">Se invece si specifica la condivisione della condivisione **STGM, \_ \_ negare \_** il valore None, il case è "multi-writer, multiple-Reader".</span><span class="sxs-lookup"><span data-stu-id="1e2ca-287">If sharing of **STGM\_SHARE\_DENY\_NONE** is specified instead, then the case is "multiple-writer, multiple-reader".</span></span> <span data-ttu-id="1e2ca-288">In questi casi, durante l'operazione di apertura verrà eseguito uno snapshot dei dati originali.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-288">In these cases, a snapshot of the original data will be made during the open operation.</span></span> <span data-ttu-id="1e2ca-289">Pertanto, anche se non viene apportata alcuna modifica all'archiviazione e/o non viene effettivamente aperto da un altro writer contemporaneamente, il trasferimento dei dati è ancora necessario durante l'apertura.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-289">Therefore, even if no changes are actually made to the storage and/or it is not actually opened by another writer simultaneously, data transfer is still necessary during the open.</span></span> <span data-ttu-id="1e2ca-290">Di conseguenza, è possibile ottenere le migliori prestazioni in fase di apertura aprendo l'oggetto di archiviazione **nella \_ condivisione STGM \_ Nega \_ scrittura** o **STGM condividono le modalità \_ \_ esclusive** .</span><span class="sxs-lookup"><span data-stu-id="1e2ca-290">As a result the best open-time performance can be obtained by opening the storage object in **STGM\_SHARE\_DENY\_WRITE** or **STGM\_SHARE\_EXCLUSIVE** modes.</span></span> <span data-ttu-id="1e2ca-291">Per altre informazioni su come viene eseguito il commit delle modifiche quando sono presenti più writer, vedere [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).</span><span class="sxs-lookup"><span data-stu-id="1e2ca-291">For more information about how changes are committed when there are multiple writers, see [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit).</span></span>

<span data-ttu-id="1e2ca-292">Nel caso di un singolo writer e di più lettori, viene aperto un oggetto di archiviazione transazionale per l'accesso in scrittura, ma condiviso con i lettori.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-292">In the "single-writer, multiple-reader" case, a transacted storage object is opened for write access, but is shared with readers.</span></span> <span data-ttu-id="1e2ca-293">Ovvero, l'oggetto di archiviazione viene aperto dal writer con **STGM \_ transazionale**, accesso a **STGM \_ ReadWrite** o **STGM \_ Write** e condivisione di **STGM \_ share \_ Deny \_ Write**.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-293">That is, the storage object is opened by the writer with **STGM\_TRANSACTED**, access of **STGM\_READWRITE** or **STGM\_WRITE**, and sharing of **STGM\_SHARE\_DENY\_WRITE**.</span></span> <span data-ttu-id="1e2ca-294">Lo spazio di archiviazione viene aperto dai lettori con **STGM \_ transazionale**, accesso di **STGM \_ Read** e condivisione di **STGM \_ share \_ Deny \_ None**.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-294">The storage is opened by readers with **STGM\_TRANSACTED**, access of **STGM\_READ**, and sharing of **STGM\_SHARE\_DENY\_NONE**.</span></span> <span data-ttu-id="1e2ca-295">In questo caso, il writer usa l'area scratch per archiviare le modifiche di cui non è stato eseguito il commit.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-295">In this case the writer uses the scratch area to store uncommitted changes.</span></span> <span data-ttu-id="1e2ca-296">Come nei casi precedenti, il lettore comporta una riduzione delle prestazioni in fase di apertura mentre viene creata una copia snapshot dei dati.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-296">As in the cases above, the reader incurs an open-time performance penalty while a snapshot copy of the data is created.</span></span>

<span data-ttu-id="1e2ca-297">In genere, l'area scratch è un file temporaneo, separato dai dati originali.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-297">Typically, the scratch area is a temporary file, separate from the original data.</span></span> <span data-ttu-id="1e2ca-298">Quando viene eseguito il commit delle modifiche nel file originale, i dati devono essere trasferiti dal file temporaneo.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-298">When changes are committed to the original file, the data must be transferred from the temporary file.</span></span> <span data-ttu-id="1e2ca-299">Per evitare questo trasferimento dei dati, è possibile specificare il flag **STGM \_ noscratch**.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-299">To avoid this data transfer, the **STGM\_NOSCRATCH** flag may be specified.</span></span> <span data-ttu-id="1e2ca-300">Quando si specifica questo flag, parti del file oggetto di archiviazione vengono utilizzate per l'area scratch, anziché un file temporaneo separato.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-300">When this flag is specified, portions of the storage object file are used for the scratch area, rather than a separate temporary file.</span></span> <span data-ttu-id="1e2ca-301">Di conseguenza, il commit delle modifiche può essere eseguito rapidamente, perché è necessario un piccolo trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-301">As a result, committing changes can be performed quickly, because little data transfer is required.</span></span> <span data-ttu-id="1e2ca-302">Lo svantaggio è che il file di archiviazione può diventare più grande di quanto sarebbe altrimenti, perché deve essere cresciuto per essere sufficientemente grande per i dati originali e per l'area scratch.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-302">The disadvantage is that the storage file can become larger than it would otherwise be, because it must be grown to be large enough for both the original data and the scratch area.</span></span> <span data-ttu-id="1e2ca-303">Per consolidare i dati e rimuovere l'area non necessaria, riaprire l'archiviazione radice in modalità transazionale, ma senza impostare il flag **STGM \_ noscratch** .</span><span class="sxs-lookup"><span data-stu-id="1e2ca-303">To consolidate the data and remove this unnecessary area, reopen the root storage in transacted mode, but without setting the **STGM\_NOSCRATCH** flag.</span></span> <span data-ttu-id="1e2ca-304">Quindi, chiamare [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) con il flag di **\_ consolidamento STGC** impostato.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-304">Then, call [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) with the **STGC\_CONSOLIDATE** flag set.</span></span>

<span data-ttu-id="1e2ca-305">Anche l'area snapshot, come l'area scratch, è in genere un file temporaneo, che può anche essere influenzato da un flag STGM.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-305">The snapshot area, like the scratch area, is also, typically, a temporary file, and this too can be affected with a STGM flag.</span></span> <span data-ttu-id="1e2ca-306">Specificando il flag **STGM \_ nosnapshot** , non viene creato un file di snapshot temporaneo separato.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-306">By specifying the **STGM\_NOSNAPSHOT** flag, a separate temporary snapshot file is not created.</span></span> <span data-ttu-id="1e2ca-307">Al contrario, i dati originali non vengono mai modificati, anche se sono presenti uno o più writer per oggetto.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-307">Instead, the original data is never modified, even if there are one or more writers per object.</span></span> <span data-ttu-id="1e2ca-308">Quando viene eseguito il commit delle modifiche, queste vengono aggiunte al file, ma i dati originali rimangono intatti.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-308">When changes are committed, they are added to the file, but the original data remains intact.</span></span> <span data-ttu-id="1e2ca-309">Questa modalità aumenta l'efficienza perché riduce il tempo di esecuzione eliminando la necessità di creare uno snapshot durante l'operazione di apertura.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-309">This mode increases efficiency because it reduces run time by eliminating the requirement of creating a snapshot during the open operation.</span></span> <span data-ttu-id="1e2ca-310">Tuttavia, l'uso di questa modalità può causare un file di archiviazione molto grande perché i dati nel file non possono mai essere sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-310">However, using this mode may result in a very large storage file because data in the file can never be overwritten.</span></span> <span data-ttu-id="1e2ca-311">Non è previsto alcun limite per le dimensioni dei file aperti in modalità nosnapshot.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-311">This is no limit to the size of files opened in NoSnapshot mode.</span></span>

### <a name="direct-single-writer-multiple-reader-mode"></a><span data-ttu-id="1e2ca-312">Single-writer diretto, modalità Multiple-Reader</span><span class="sxs-lookup"><span data-stu-id="1e2ca-312">Direct Single-Writer, Multiple-Reader Mode</span></span>

<span data-ttu-id="1e2ca-313">Come descritto, è possibile avere un solo Writer e più lettori di un oggetto di archiviazione, se tale oggetto viene aperto in modalità transazionale.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-313">As described, it is possible to have a single writer and multiple readers of a storage object, if that object is opened in transacted mode.</span></span> <span data-ttu-id="1e2ca-314">È anche possibile ottenere il case con singolo writer, Multireader in modalità diretta, specificando il flag **\_ \_ SWMR diretto STGM** .</span><span class="sxs-lookup"><span data-stu-id="1e2ca-314">It is also possible to achieve the single-writer, multireader case in direct mode, by specifying the **STGM\_DIRECT\_SWMR** flag.</span></span>

<span data-ttu-id="1e2ca-315">In **modalità \_ \_ SWMR diretta di STGM** è possibile che un chiamante apra un oggetto per l'accesso in lettura/scrittura, mentre altri chiamanti hanno contemporaneamente il file aperto per l'accesso in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-315">In **STGM\_DIRECT\_SWMR** mode, it is possible for one caller to open an object for read/write access, while other callers simultaneously have the file open for read-only access.</span></span> <span data-ttu-id="1e2ca-316">Non è consentito utilizzare questo flag in combinazione con il flag **\_ transazionale STGM** .</span><span class="sxs-lookup"><span data-stu-id="1e2ca-316">It is not valid to use this flag in combination with the **STGM\_TRANSACTED** flag.</span></span> <span data-ttu-id="1e2ca-317">In questa modalità, il writer apre l'oggetto con i flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="1e2ca-317">In this mode, the writer opens the object with the following flags:</span></span>

<span data-ttu-id="1e2ca-318">**STGM \_ Direct \_ SWMR** \| **STGM \_ ReadWrite** \| **STGM \_ share \_ DENYWRITE**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-318">**STGM\_DIRECT\_SWMR** \| **STGM\_READWRITE** \| **STGM\_SHARE\_DENYWRITE**</span></span>

<span data-ttu-id="1e2ca-319">e ognuno dei lettori apre l'oggetto con i flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="1e2ca-319">and each of the readers opens the object with these flags:</span></span>

<span data-ttu-id="1e2ca-320">**STGM \_ Direct \_ SWMR** \| **STGM \_ Read** \| **STGM \_ share \_ Deny \_ None**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-320">**STGM\_DIRECT\_SWMR** \| **STGM\_READ** \| **STGM\_SHARE\_DENY\_NONE**</span></span>

<span data-ttu-id="1e2ca-321">In questa modalità, per modificare l'oggetto di archiviazione, è necessario che il writer ottenga l'accesso esclusivo all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-321">In this mode, to modify the storage object, the writer must get exclusive access to the object.</span></span> <span data-ttu-id="1e2ca-322">Questa operazione è possibile quando tutti i lettori lo hanno chiuso.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-322">This is possible when all the readers have closed it.</span></span> <span data-ttu-id="1e2ca-323">Il writer usa l'interfaccia [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) per ottenere l'accesso esclusivo.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-323">The writer uses the [**IDirectWriterLock**](/windows/desktop/api/Objidl/nn-objidl-idirectwriterlock) interface to obtain this exclusive access.</span></span>

### <a name="simple-mode"></a><span data-ttu-id="1e2ca-324">Modalità semplice</span><span class="sxs-lookup"><span data-stu-id="1e2ca-324">Simple Mode</span></span>

<span data-ttu-id="1e2ca-325">La modalità semplice (**STGM \_ Simple**) è utile per le applicazioni che eseguono operazioni di salvataggio complete.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-325">Simple mode (**STGM\_SIMPLE**) is useful for applications that perform complete save operations.</span></span> <span data-ttu-id="1e2ca-326">È efficiente, ma presenta i vincoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="1e2ca-326">It is efficient, but has the following constraints:</span></span>

-   <span data-ttu-id="1e2ca-327">Non esiste alcun supporto per le sottoarchiviazioni.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-327">No support exists for substorages.</span></span>
-   <span data-ttu-id="1e2ca-328">Non è possibile effettuare il marshalling dell'oggetto di archiviazione e degli oggetti di flusso ottenuti da esso.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-328">The storage object, and stream objects obtained from it, cannot be marshaled.</span></span>
-   <span data-ttu-id="1e2ca-329">Ogni flusso ha una dimensione minima.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-329">Each stream has a minimum size.</span></span> <span data-ttu-id="1e2ca-330">Se un numero minore di byte minimi viene scritto in un flusso quando il flusso viene rilasciato, il flusso viene esteso alla dimensione minima.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-330">If fewer than the minimum bytes are written into a stream when the stream is released, the stream is extended to the minimum size.</span></span> <span data-ttu-id="1e2ca-331">Ad esempio, la dimensione minima per una particolare implementazione di [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) è 4 KB.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-331">For example, the minimum size for a particular [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) implementation is 4 KB.</span></span> <span data-ttu-id="1e2ca-332">Viene creato un flusso e ne viene scritto 1 KB.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-332">A stream is created and 1 KB is written to it.</span></span> <span data-ttu-id="1e2ca-333">Al rilascio finale di tale **IStream**, le dimensioni del flusso verranno estesi automaticamente a 4 KB.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-333">At the final release of that **IStream**, the stream size will be automatically extended to 4 KB.</span></span> <span data-ttu-id="1e2ca-334">Successivamente, l'apertura del flusso e la chiamata del metodo [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) mostreranno una dimensione di 4 KB.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-334">Subsequently, opening the stream and calling the [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method will show a size of 4 KB.</span></span>
-   <span data-ttu-id="1e2ca-335">Non tutti i metodi di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) o [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) saranno supportati dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-335">Not all methods of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) or [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) will be supported by the implementation.</span></span> <span data-ttu-id="1e2ca-336">Per altre informazioni, vedere [implementazione di file compositi IStorage](istorage-compound-file-implementation.md)e [implementazione di un file composto IStream](istream-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="1e2ca-336">For more information, see [IStorage - Compound File Implementation](istorage-compound-file-implementation.md), and [IStream - Compound File Implementation](istream-compound-file-implementation.md).</span></span>

<span data-ttu-id="1e2ca-337">Il [marshalling](/windows/desktop/Midl/marshaling-ole-data-types) è il processo di creazione di pacchetti, annullamento del packaging e invio di parametri del metodo di interfaccia attraverso i limiti del thread o del processo all'interno di una chiamata di procedura remota (RPC).</span><span class="sxs-lookup"><span data-stu-id="1e2ca-337">[Marshaling](/windows/desktop/Midl/marshaling-ole-data-types) is the process of packaging, unpackaging, and sending interface method parameters across thread or process boundaries within a Remote Procedure Call (RPC).</span></span> <span data-ttu-id="1e2ca-338">Per altre informazioni, vedere [Dettagli di marshalling](../com/marshaling-details.md) e [marshalling dell'interfaccia](../com/interface-marshaling.md).</span><span class="sxs-lookup"><span data-stu-id="1e2ca-338">For more information, see [Marshaling Details](../com/marshaling-details.md) and [Interface Marshaling](../com/interface-marshaling.md).</span></span>

<span data-ttu-id="1e2ca-339">Quando un oggetto di archiviazione viene ottenuto da un'operazione di creazione in modalità semplice:</span><span class="sxs-lookup"><span data-stu-id="1e2ca-339">When a storage object is obtained by a Create operation in simple mode:</span></span>

-   <span data-ttu-id="1e2ca-340">Gli elementi del flusso possono essere creati, ma non aperti.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-340">Stream elements can be created, but not opened.</span></span>
-   <span data-ttu-id="1e2ca-341">Quando viene creato un elemento Stream chiamando [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream), non è possibile creare un altro flusso fino a quando non viene rilasciato l'oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-341">When a stream element is created by calling [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream), it is not possible to create another stream until that stream object is released.</span></span>
-   <span data-ttu-id="1e2ca-342">Dopo la scrittura di tutti i flussi, chiamare [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) per scaricare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-342">After all streams are written, call [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) to flush the changes.</span></span>

<span data-ttu-id="1e2ca-343">Quando un oggetto di archiviazione viene ottenuto da un'operazione di apertura in modalità semplice:</span><span class="sxs-lookup"><span data-stu-id="1e2ca-343">When a storage object is obtained by an Open operation in simple mode:</span></span>

-   <span data-ttu-id="1e2ca-344">È possibile aprire un solo elemento di flusso alla volta.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-344">It is possible to open only one stream element at a time.</span></span>
-   <span data-ttu-id="1e2ca-345">Non è possibile modificare le dimensioni di un flusso chiamando il metodo [**IStream:: sesize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) oppure cercando o scrivendo oltre la fine del flusso.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-345">It is not possible to change the size of a stream by calling the [**IStream::SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) method or by seeking or writing beyond the end of the stream.</span></span> <span data-ttu-id="1e2ca-346">Tuttavia, poiché tutti i flussi hanno dimensioni minime, è possibile usare il flusso fino a tale dimensione, anche se in origine sono stati scritti meno dati.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-346">However, because all streams are of a minimum size, it is possible to use the stream up to that size, even if less data was originally written to it.</span></span> <span data-ttu-id="1e2ca-347">Per determinare le dimensioni di un flusso, usare il metodo [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) .</span><span class="sxs-lookup"><span data-stu-id="1e2ca-347">To determine the size of a stream, use the [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) method.</span></span>

<span data-ttu-id="1e2ca-348">Tenere presente che, se un elemento di archiviazione viene modificato da un oggetto di archiviazione che non si trova in modalità semplice, non sarà ancora possibile aprire tale elemento di archiviazione in modalità semplice.</span><span class="sxs-lookup"><span data-stu-id="1e2ca-348">Be aware that, if a storage element is modified by a storage object that is not in simple mode, it will not be possible, again, to open that storage element in simple mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e2ca-349">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e2ca-349">Requirements</span></span>



| <span data-ttu-id="1e2ca-350">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e2ca-350">Requirement</span></span> | <span data-ttu-id="1e2ca-351">Valore</span><span class="sxs-lookup"><span data-stu-id="1e2ca-351">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1e2ca-352">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e2ca-352">Minimum supported client</span></span><br/> | <span data-ttu-id="1e2ca-353">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1e2ca-353">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1e2ca-354">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e2ca-354">Minimum supported server</span></span><br/> | <span data-ttu-id="1e2ca-355">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1e2ca-355">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1e2ca-356">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e2ca-356">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e2ca-357"><dt>ObjBase. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e2ca-357"><dt>ObjBase.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e2ca-358">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e2ca-358">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e2ca-359">**ISequentialStream:: Read**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-359">**ISequentialStream::Read**</span></span>](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dt>

[<span data-ttu-id="1e2ca-360">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-360">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="1e2ca-361">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-361">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="1e2ca-362">**StgCreateDocfileOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-362">**StgCreateDocfileOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfileonilockbytes)
</dt> <dt>

[<span data-ttu-id="1e2ca-363">**StgCreateStorageEx**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-363">**StgCreateStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[<span data-ttu-id="1e2ca-364">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-364">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[<span data-ttu-id="1e2ca-365">**StgOpenStorageEx**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-365">**StgOpenStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> <dt>

[<span data-ttu-id="1e2ca-366">**StgOpenStorageOnILockBytes**</span><span class="sxs-lookup"><span data-stu-id="1e2ca-366">**StgOpenStorageOnILockBytes**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageonilockbytes)
</dt> </dl>

 

