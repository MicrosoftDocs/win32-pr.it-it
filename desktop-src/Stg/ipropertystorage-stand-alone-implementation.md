---
title: IPropertyStorage-implementazione autonoma
description: L'implementazione autonoma fornita dal sistema di IPropertySetStorage include un'implementazione di IPropertyStorage, l'interfaccia che legge e scrive le proprietà in una risorsa di archiviazione del set di proprietà.
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- IPropertyStorage-implementazione autonoma
- IPropertyStorage Strctd STG, implementazioni, autonome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35965831b0105557044461236030e3543c13217
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399194"
---
# <a name="ipropertystorage-stand-alone-implementation"></a><span data-ttu-id="d379d-105">IPropertyStorage-implementazione autonoma</span><span class="sxs-lookup"><span data-stu-id="d379d-105">IPropertyStorage-Stand-alone Implementation</span></span>

<span data-ttu-id="d379d-106">L'implementazione autonoma fornita dal sistema di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) include un'implementazione di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), l'interfaccia che legge e scrive le proprietà in una risorsa di archiviazione del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d379d-106">The system-provided, stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) includes an implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), the interface that reads and writes properties in a property set storage.</span></span> <span data-ttu-id="d379d-107">L'interfaccia **IPropertySetStorage** crea e apre i set di proprietà in una risorsa di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d379d-107">The **IPropertySetStorage** interface creates and opens property sets in a storage.</span></span> <span data-ttu-id="d379d-108">Le interfacce [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) e [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) sono inoltre disponibili nell'implementazione autonoma.</span><span class="sxs-lookup"><span data-stu-id="d379d-108">The [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) and [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) interfaces are also provided in the stand-alone implementation.</span></span>

<span data-ttu-id="d379d-109">Per ottenere un puntatore all'implementazione autonoma di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), chiamare la funzione [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) per creare un nuovo set di proprietà o [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) per ottenere il puntatore di interfaccia in un set di proprietà esistente (o chiamare i metodi [**create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) o [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) dell'implementazione autonoma [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ).</span><span class="sxs-lookup"><span data-stu-id="d379d-109">To get a pointer to the stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), call the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) function to create a new property set or [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) to obtain the interface pointer on an existing property set (or call the [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) or [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) methods of the [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) stand-alone implementation).</span></span>

<span data-ttu-id="d379d-110">L'implementazione autonoma di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) Crea set di proprietà per qualsiasi oggetto di archiviazione o flusso, non solo per i flussi e le archiviazioni di file composte.</span><span class="sxs-lookup"><span data-stu-id="d379d-110">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) creates property sets on any storage or stream object, not just on compound file storages and streams.</span></span> <span data-ttu-id="d379d-111">L'implementazione autonoma non dipende dai file composti e può essere usata con qualsiasi implementazione di archivi strutturati.</span><span class="sxs-lookup"><span data-stu-id="d379d-111">The stand-alone implementation does not depend on compound files and can be used with any implementation of structured storages.</span></span> <span data-ttu-id="d379d-112">Per ulteriori informazioni sull'implementazione del file composito di questa interfaccia, vedere [IPropertyStorage-compound file implementation](ipropertystorage-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="d379d-112">For more information about the compound file implementation of this interface, see [IPropertyStorage-Compound File Implementation](ipropertystorage-compound-file-implementation.md).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="d379d-113">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="d379d-113">When to Use</span></span>

<span data-ttu-id="d379d-114">Utilizzare [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) per gestire le proprietà all'interno di un singolo set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d379d-114">Use [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) to manage properties within a single property set.</span></span> <span data-ttu-id="d379d-115">I metodi supportano la lettura, la scrittura e l'eliminazione di entrambe le proprietà e i nomi di stringa facoltativi che possono essere associati a ID di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d379d-115">Its methods support reading, writing, and deleting both properties and the optional string names that can be associated with property IDs.</span></span> <span data-ttu-id="d379d-116">Altri metodi supportano le operazioni di commit e ripristino standard.</span><span class="sxs-lookup"><span data-stu-id="d379d-116">Other methods support the standard commit and revert storage operations.</span></span> <span data-ttu-id="d379d-117">Esiste anche un metodo che imposta i tempi associati all'archiviazione delle proprietà e un altro che consente l'assegnazione di un CLSID da usare per associare altro codice, ad esempio il codice dell'interfaccia utente, con il set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d379d-117">There is also a method that sets times associated with the property storage, and another that permits the assignment of a CLSID to be used to associate other code, such as user interface code, with the property set.</span></span> <span data-ttu-id="d379d-118">Il metodo [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) fornisce un puntatore all'implementazione autonoma di [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), che enumera le proprietà nel set.</span><span class="sxs-lookup"><span data-stu-id="d379d-118">The [**Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) method supplies a pointer to the stand-alone implementation of [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), which enumerates the properties in the set.</span></span>

## <a name="version-0-and-version-1-property-set-formats"></a><span data-ttu-id="d379d-119">Formati di set di proprietà versione 0 e versione 1</span><span class="sxs-lookup"><span data-stu-id="d379d-119">Version 0 and Version 1 Property Set Formats</span></span>

<span data-ttu-id="d379d-120">L'implementazione autonoma di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supporta sia la versione 0 che i formati di serializzazione del set di proprietà versione 1.</span><span class="sxs-lookup"><span data-stu-id="d379d-120">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supports both the version 0 and the version 1 property set serialization formats.</span></span> <span data-ttu-id="d379d-121">Per ulteriori informazioni, vedere [serializzazione del set di proprietà](version-0-vs--version-1-property-set-serialization.md).</span><span class="sxs-lookup"><span data-stu-id="d379d-121">For more information, see [Property Set Serialization](version-0-vs--version-1-property-set-serialization.md).</span></span> <span data-ttu-id="d379d-122">I set di proprietà vengono creati nel formato versione 0 e rimangono in tale formato a meno che non vengano richieste nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="d379d-122">Property sets are created in version 0 format and remain in that format unless new features are requested.</span></span> <span data-ttu-id="d379d-123">In quel momento, il formato viene aggiornato alla versione 1.</span><span class="sxs-lookup"><span data-stu-id="d379d-123">At that time, the format is updated to version 1.</span></span>

<span data-ttu-id="d379d-124">Se, ad esempio, viene creato un set di proprietà con il \_ flag predefinito PROPSETFLAG, il formato è la versione 0.</span><span class="sxs-lookup"><span data-stu-id="d379d-124">For example, if a property set is created with the PROPSETFLAG\_DEFAULT flag, its format is version 0.</span></span> <span data-ttu-id="d379d-125">Fino a quando i tipi di proprietà conformi al formato versione 0 vengono scritti e letti dal set di proprietà, il set di proprietà rimane nel formato versione 0.</span><span class="sxs-lookup"><span data-stu-id="d379d-125">As long as property types that conform to the version 0 format are written to and read from that property set, the property set remains in version 0 format.</span></span> <span data-ttu-id="d379d-126">Se un tipo di proprietà della versione 1 viene scritto nel set di proprietà, il set di proprietà viene aggiornato automaticamente alla versione 1.</span><span class="sxs-lookup"><span data-stu-id="d379d-126">If a version 1 property type is written to the property set, the property set is automatically updated to version 1.</span></span> <span data-ttu-id="d379d-127">Successivamente, il set di proprietà non può più essere letto dalle implementazioni che comprendono solo la versione 0.</span><span class="sxs-lookup"><span data-stu-id="d379d-127">Subsequently, that property set can no longer be read by implementations that only understand version 0.</span></span>

## <a name="ipropertystorage-and-variant-types"></a><span data-ttu-id="d379d-128">Tipi IPropertyStorage e Variant</span><span class="sxs-lookup"><span data-stu-id="d379d-128">IPropertyStorage and Variant Types</span></span>

<span data-ttu-id="d379d-129">L'implementazione autonoma di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) non supporta i tipi Variant VT \_ Unknown o VT \_ Dispatch nel membro **VT** della struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="d379d-129">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) does not support the variant types VT\_UNKNOWN or VT\_DISPATCH in the **vt** member of the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

<span data-ttu-id="d379d-130">I tipi Variant seguenti sono supportati all'interno di SafeArray; ovvero, questi valori possono essere combinati con \_ una matrice VT nel membro **VT** della struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="d379d-130">The following variant types are supported within a SafeArray; that is, these values can be combined with VT\_ARRAY in the **vt** member of the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>



<span data-ttu-id="d379d-131">Tipi Variant supportati all'interno di SafeArray mediante l'implementazione del file composto di [ **IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)</span><span class="sxs-lookup"><span data-stu-id="d379d-131">Variant types supported within SafeArray by compound file implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)</span></span>

<span data-ttu-id="d379d-132">VT \_ I1</span><span class="sxs-lookup"><span data-stu-id="d379d-132">VT\_I1</span></span>

<span data-ttu-id="d379d-133">\_Ui1 VT</span><span class="sxs-lookup"><span data-stu-id="d379d-133">VT\_UI1</span></span>

<span data-ttu-id="d379d-134">\_I2 VT</span><span class="sxs-lookup"><span data-stu-id="d379d-134">VT\_I2</span></span>

<span data-ttu-id="d379d-135">\_UI2 VT</span><span class="sxs-lookup"><span data-stu-id="d379d-135">VT\_UI2</span></span>

<span data-ttu-id="d379d-136">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="d379d-136">VT\_I4</span></span>

<span data-ttu-id="d379d-137">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="d379d-137">VT\_UI4</span></span>

<span data-ttu-id="d379d-138">\_int VT</span><span class="sxs-lookup"><span data-stu-id="d379d-138">VT\_INT</span></span>

<span data-ttu-id="d379d-139">\_uint VT</span><span class="sxs-lookup"><span data-stu-id="d379d-139">VT\_UINT</span></span>

<span data-ttu-id="d379d-140">\_R4 VT</span><span class="sxs-lookup"><span data-stu-id="d379d-140">VT\_R4</span></span>

<span data-ttu-id="d379d-141">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="d379d-141">VT\_R8</span></span>

<span data-ttu-id="d379d-142">\_CY VT</span><span class="sxs-lookup"><span data-stu-id="d379d-142">VT\_CY</span></span>

<span data-ttu-id="d379d-143">\_Data VT</span><span class="sxs-lookup"><span data-stu-id="d379d-143">VT\_DATE</span></span>

<span data-ttu-id="d379d-144">\_BSTR VT</span><span class="sxs-lookup"><span data-stu-id="d379d-144">VT\_BSTR</span></span>

<span data-ttu-id="d379d-145">\_bool VT</span><span class="sxs-lookup"><span data-stu-id="d379d-145">VT\_BOOL</span></span>

<span data-ttu-id="d379d-146">\_decimale VT</span><span class="sxs-lookup"><span data-stu-id="d379d-146">VT\_DECIMAL</span></span>

<span data-ttu-id="d379d-147">\_errore VT</span><span class="sxs-lookup"><span data-stu-id="d379d-147">VT\_ERROR</span></span>

<span data-ttu-id="d379d-148">\_variante VT</span><span class="sxs-lookup"><span data-stu-id="d379d-148">VT\_VARIANT</span></span>

 



 

<span data-ttu-id="d379d-149">Quando \_ la variante VT viene combinata con \_ la matrice VT, il SAFEARRAY stesso include le strutture [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="d379d-149">When VT\_VARIANT is combined with VT\_ARRAY, the SafeArray itself holds [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structures.</span></span> <span data-ttu-id="d379d-150">Tuttavia, i tipi di questi elementi devono essere ricavati dall'elenco precedente, non possono essere \_ varianti VT e non possono includere gli \_ indicatori del vettore VT, dell'array VT o del \_ \_ ByRef VT.</span><span class="sxs-lookup"><span data-stu-id="d379d-150">However, the types of these elements must be taken from the preceding list, cannot be VT\_VARIANT, and cannot include the VT\_VECTOR, VT\_ARRAY, or VT\_BYREF indicators.</span></span>

## <a name="ipropertystorage-methods"></a><span data-ttu-id="d379d-151">Metodi IPropertyStorage</span><span class="sxs-lookup"><span data-stu-id="d379d-151">IPropertyStorage Methods</span></span>

<span data-ttu-id="d379d-152">L'implementazione autonoma di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supporta i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d379d-152">The stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) supports the following methods:</span></span>

<dl> <dt>

<span data-ttu-id="d379d-153"><span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)</span><span class="sxs-lookup"><span data-stu-id="d379d-153"><span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)</span></span>
</dt> <dd>

<span data-ttu-id="d379d-154">Legge le proprietà specificate nella matrice *rgpspec* e fornisce i valori di tutte le proprietà valide nella matrice *rgvar* degli elementi [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .</span><span class="sxs-lookup"><span data-stu-id="d379d-154">Reads the properties specified in the *rgpspec* array and supplies the values of all valid properties in the *rgvar* array of [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) elements.</span></span>

<span data-ttu-id="d379d-155">Nell'implementazione autonoma fornita dal sistema, gli identificatori di proprietà duplicati che fanno riferimento a flussi o tipi di archiviazione generano più chiamate a [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) o [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) e l'esito positivo o negativo di [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) dipende dalla capacità dell'implementazione di archiviazione sottostante di condividere le archiviazioni aperte.</span><span class="sxs-lookup"><span data-stu-id="d379d-155">In the system-provided, stand-alone implementation, duplicate property identifiers that refer to stream- or storage-types result in multiple calls to [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) or [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) and the success or failure of [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) depends on the underlying storage implementation's ability to share open storages.</span></span>

<span data-ttu-id="d379d-156">Inoltre, per garantire un'operazione thread-safe se la stessa proprietà con valori di flusso o di archiviazione viene richiesta più volte tramite lo stesso puntatore [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , l'apertura avrà esito positivo o negativo a seconda che la proprietà sia già aperta e che la file system sottostante gestisca più aperture di un flusso o di un'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d379d-156">In addition, to ensure thread-safe operation if the same stream- or storage-valued property is requested multiple times through the same [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) pointer, the open will succeed or fail depending on whether or not the property is already open and on whether the underlying file system handles multiple opens of a stream or storage.</span></span> <span data-ttu-id="d379d-157">Di conseguenza, l'operazione [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) su una proprietà con valori di flusso o di archiviazione restituisce sempre una chiamata a [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)o [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), passando l'accesso ( \_ ad esempio, STGM ReadWrite) e i valori di condivisione (ad esempio, STGM \_ share \_ Exclusive) specificati quando il set di proprietà è stato originariamente aperto o creato.</span><span class="sxs-lookup"><span data-stu-id="d379d-157">Thus, the [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) operation on a stream- or storage-valued property always results in a call to [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream), or [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), passing the access (STGM\_READWRITE, for example) and share values (STGM\_SHARE\_EXCLUSIVE, for example) specified when the property set was originally opened or created.</span></span>

<span data-ttu-id="d379d-158">Se il metodo ha esito negativo, i valori scritti in *rgvar* non \[ \] sono definiti.</span><span class="sxs-lookup"><span data-stu-id="d379d-158">If the method fails, the values written to *rgvar*\[\] are undefined.</span></span> <span data-ttu-id="d379d-159">Se alcune proprietà con valori di archiviazione o flusso vengono aperte correttamente, ma si verifica un errore prima del completamento dell'esecuzione, queste proprietà devono essere rilasciate prima che il metodo venga restituito.</span><span class="sxs-lookup"><span data-stu-id="d379d-159">If some stream- or storage-valued properties are opened successfully but an error occurs before execution is complete, these properties should be released before the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="d379d-160"><span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage:: WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)</span><span class="sxs-lookup"><span data-stu-id="d379d-160"><span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)</span></span>
</dt> <dd>

<span data-ttu-id="d379d-161">Scrive le proprietà specificate nella matrice *rgpspec* \[ \] , assegnando loro i tag e i valori [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) specificati in *rgvar* \[ \] .</span><span class="sxs-lookup"><span data-stu-id="d379d-161">Writes the properties specified in the *rgpspec*\[\] array, assigning them the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) tags and values specified in *rgvar*\[\].</span></span> <span data-ttu-id="d379d-162">Alle proprietà già esistenti vengono assegnati i valori **PROPVARIANT** specificati e vengono create le proprietà attualmente non esistenti.</span><span class="sxs-lookup"><span data-stu-id="d379d-162">Properties that already exist are assigned the specified **PROPVARIANT** values, and properties that do not currently exist are created.</span></span>

</dd> <dt>

<span data-ttu-id="d379d-163"><span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::D eleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)</span><span class="sxs-lookup"><span data-stu-id="d379d-163"><span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage::DeleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)</span></span>
</dt> <dd>

<span data-ttu-id="d379d-164">Elimina le proprietà specificate in *rgpspec* \[ \] .</span><span class="sxs-lookup"><span data-stu-id="d379d-164">Deletes the properties specified in the *rgpspec*\[\].</span></span>

</dd> <dt>

<span data-ttu-id="d379d-165"><span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage:: ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)</span><span class="sxs-lookup"><span data-stu-id="d379d-165"><span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="d379d-166">Legge i nomi di stringa esistenti associati agli ID di proprietà specificati nella matrice *rgpropid* \[ \] .</span><span class="sxs-lookup"><span data-stu-id="d379d-166">Reads existing string names associated with the property IDs specified in the *rgpropid*\[\] array.</span></span>

</dd> <dt>

<span data-ttu-id="d379d-167"><span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage:: WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)</span><span class="sxs-lookup"><span data-stu-id="d379d-167"><span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="d379d-168">Assegna i nomi di stringa specificati nella matrice *rglpwstrName* agli ID di proprietà specificati nella matrice *rgpropid* .</span><span class="sxs-lookup"><span data-stu-id="d379d-168">Assigns string names specified in the *rglpwstrName* array to property IDs specified in the *rgpropid* array.</span></span>

</dd> <dt>

<span data-ttu-id="d379d-169"><span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::D eletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)</span><span class="sxs-lookup"><span data-stu-id="d379d-169"><span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage::DeletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)</span></span>
</dt> <dd>

<span data-ttu-id="d379d-170">Elimina i nomi di stringa degli ID di proprietà specificati nella matrice *rgpropid* scrivendo **null** nel nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="d379d-170">Deletes the string names of the property IDs specified in the *rgpropid* array by writing **NULL** to the property name.</span></span>

</dd> <dt>

<span data-ttu-id="d379d-171"><span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage:: seclasse**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)</span><span class="sxs-lookup"><span data-stu-id="d379d-171"><span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)</span></span>
</dt> <dd>

<span data-ttu-id="d379d-172">Imposta il **CLSID** del flusso del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d379d-172">Sets the **CLSID** of the property set stream.</span></span> <span data-ttu-id="d379d-173">Nell'implementazione autonoma, l'impostazione del CLSID su un set di proprietà non semplice, che può contenere proprietà con valori di archiviazione o flusso, come descritto in [**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create), imposta anche il CLSID sulla sottoarchiviazione sottostante in modo che sia possibile ottenerlo tramite una chiamata a [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).</span><span class="sxs-lookup"><span data-stu-id="d379d-173">In the stand-alone implementation, setting the CLSID on a nonsimple property set (one that can contain storage- or stream-valued properties, as described in [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) also sets the CLSID on the underlying substorage so that it can be obtained through a call to [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).</span></span>

</dd> <dt>

<span data-ttu-id="d379d-174"><span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage:: commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)</span><span class="sxs-lookup"><span data-stu-id="d379d-174"><span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage::Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)</span></span>
</dt> <dd>

<span data-ttu-id="d379d-175">Per i set di proprietà semplici e non semplici, Scarica l'immagine di memoria sul sottosistema del disco.</span><span class="sxs-lookup"><span data-stu-id="d379d-175">For both simple and nonsimple property sets, flushes the memory image to the disk subsystem.</span></span> <span data-ttu-id="d379d-176">Inoltre, per i set di proprietà in modalità transazionale non semplici, questo metodo chiama [**IStorage:: commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) sul set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="d379d-176">In addition, for nonsimple transacted-mode property sets, this method calls [**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) on the property set.</span></span>

</dd> <dt>

<span data-ttu-id="d379d-177"><span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage:: Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)</span><span class="sxs-lookup"><span data-stu-id="d379d-177"><span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage::Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)</span></span>
</dt> <dd>

<span data-ttu-id="d379d-178">Solo per set di proprietà non semplici, chiama il metodo [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) dell'archiviazione sottostante e riapre il flusso "Contents".</span><span class="sxs-lookup"><span data-stu-id="d379d-178">For nonsimple property sets only, calls the [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) method of the underlying storage and reopens the 'contents' stream.</span></span> <span data-ttu-id="d379d-179">Per i set di proprietà semplici, restituisce solo E \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d379d-179">For simple property sets, only returns E\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="d379d-180"><span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)</span><span class="sxs-lookup"><span data-stu-id="d379d-180"><span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)</span></span>
</dt> <dd>

<span data-ttu-id="d379d-181">Crea un oggetto enumeratore che implementa [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), i metodi di cui è possibile chiamare per enumerare le strutture [**Campo STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) che forniscono informazioni su ognuna delle proprietà nel set.</span><span class="sxs-lookup"><span data-stu-id="d379d-181">Creates an enumerator object that implements [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), the methods of which can be called to enumerate the [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) structures that provide information about each of the properties in the set.</span></span>

<span data-ttu-id="d379d-182">Questa implementazione crea una matrice in cui viene letto l'intero set di proprietà e che può essere condiviso quando viene chiamato [**IEnumSTATPROPSTG:: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) .</span><span class="sxs-lookup"><span data-stu-id="d379d-182">This implementation creates an array into which the entire property set is read and which can be shared when [**IEnumSTATPROPSTG::Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) is called.</span></span>

</dd> <dt>

<span data-ttu-id="d379d-183"><span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage:: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)</span><span class="sxs-lookup"><span data-stu-id="d379d-183"><span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage::Stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)</span></span>
</dt> <dd>

<span data-ttu-id="d379d-184">Compila i membri di una struttura [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , che contiene informazioni sul set di proprietà nel suo complesso.</span><span class="sxs-lookup"><span data-stu-id="d379d-184">Fills in the members of a [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structure, which contains information about the property set as a whole.</span></span> <span data-ttu-id="d379d-185">Al ritorno, fornisce un puntatore alla struttura.</span><span class="sxs-lookup"><span data-stu-id="d379d-185">On return, supplies a pointer to the structure.</span></span>

<span data-ttu-id="d379d-186">Per i set di archiviazione non semplici, questa implementazione chiama [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (o [**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) per ottenere le informazioni dal flusso o dall'archivio sottostante.</span><span class="sxs-lookup"><span data-stu-id="d379d-186">For nonsimple storage sets, this implementation calls [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (or [**IStream::Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) to get the information from the underlying storage or stream.</span></span>

</dd> <dt>

<span data-ttu-id="d379d-187"><span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage:: setimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)</span><span class="sxs-lookup"><span data-stu-id="d379d-187"><span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)</span></span>
</dt> <dd>

<span data-ttu-id="d379d-188">Solo per set di proprietà non semplici, imposta le ore supportate dall'archiviazione sottostante.</span><span class="sxs-lookup"><span data-stu-id="d379d-188">For nonsimple property sets only, sets the times supported by the underlying storage.</span></span> <span data-ttu-id="d379d-189">Questa implementazione di [**Timers**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) chiama il metodo [**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) dell'archiviazione sottostante per modificare gli orari.</span><span class="sxs-lookup"><span data-stu-id="d379d-189">This implementation of [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) calls the [**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) method of the underlying storage to modify the times.</span></span> <span data-ttu-id="d379d-190">Supporta le ore supportate dal metodo sottostante, che può essere l'ora di modifica, l'ora di accesso o l'ora di creazione.</span><span class="sxs-lookup"><span data-stu-id="d379d-190">It supports the times supported by the underlying method which can be modification time, access time, or creation time.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="d379d-191">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d379d-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d379d-192">IPropertySetStorage-implementazione autonoma</span><span class="sxs-lookup"><span data-stu-id="d379d-192">IPropertySetStorage-Stand-alone Implementation</span></span>](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[<span data-ttu-id="d379d-193">**IPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="d379d-193">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[<span data-ttu-id="d379d-194">**IStorage:: SetElementTimes**</span><span class="sxs-lookup"><span data-stu-id="d379d-194">**IStorage::SetElementTimes**</span></span>](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[<span data-ttu-id="d379d-195">**StgOpenPropStg**</span><span class="sxs-lookup"><span data-stu-id="d379d-195">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[<span data-ttu-id="d379d-196">**StgCreatePropStg**</span><span class="sxs-lookup"><span data-stu-id="d379d-196">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[<span data-ttu-id="d379d-197">**StgCreatePropSetStg**</span><span class="sxs-lookup"><span data-stu-id="d379d-197">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 