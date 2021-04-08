---
title: IPropertySetStorage-implementazione autonoma
description: L'implementazione autonoma fornita dal sistema di IPropertySetStorage include un'implementazione di IPropertyStorage e IPropertySetStorage.
ms.assetid: 0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2
keywords:
- IPropertySetStorage Strctd STG, implementazioni
- IPropertySetStorage Strctd STG, implementazioni, autonome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9fd0afe31775b06b3a5f61f4c79939be976e98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046851"
---
# <a name="ipropertysetstorage-stand-alone-implementation"></a><span data-ttu-id="fe084-105">IPropertySetStorage-implementazione autonoma</span><span class="sxs-lookup"><span data-stu-id="fe084-105">IPropertySetStorage-Stand-alone Implementation</span></span>

<span data-ttu-id="fe084-106">L'implementazione autonoma fornita dal sistema di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) include un'implementazione di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) e **IPropertySetStorage**. [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) è l'interfaccia che legge e scrive le proprietà in una risorsa di archiviazione del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="fe084-106">The system-provided, stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) includes an implementation of both [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) and **IPropertySetStorage**.[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) is the interface that reads and writes properties in a property set storage.</span></span> <span data-ttu-id="fe084-107">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) è l'interfaccia che crea e apre i set di proprietà in una risorsa di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fe084-107">[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) is the interface that creates and opens property sets in a storage.</span></span> <span data-ttu-id="fe084-108">Le interfacce [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) e [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) sono inoltre disponibili nell'implementazione autonoma.</span><span class="sxs-lookup"><span data-stu-id="fe084-108">The [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) and [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) interfaces are also provided in the stand-alone implementation.</span></span>

<span data-ttu-id="fe084-109">Per usare l'implementazione autonoma di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), ottenere prima un puntatore all'implementazione autonoma fornita dal sistema e associare l'implementazione fornita dal sistema all'oggetto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fe084-109">To use the stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), first obtain a pointer to the system-provided, stand-alone implementation and associate the system-provided implementation with your storage object.</span></span> <span data-ttu-id="fe084-110">Per ottenere un puntatore all'implementazione autonoma di **IPropertySetStorage**, chiamare la funzione [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) e specificare il parametro *pStorage* che specifica l'oggetto di archiviazione che conterrà il set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="fe084-110">To get a pointer to the stand-alone implementation of **IPropertySetStorage**, call the [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) function and provide the *pStorage* parameter specifying the storage object that will contain the property set.</span></span> <span data-ttu-id="fe084-111">Questa funzione fornisce un puntatore alla nuova interfaccia **IPropertySetStorage** per l'oggetto di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="fe084-111">This function provides a pointer to the new **IPropertySetStorage** interface for the specified storage object.</span></span>

<span data-ttu-id="fe084-112">L'implementazione autonoma di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) Crea set di proprietà per qualsiasi oggetto di archiviazione, non solo per le archiviazioni di file composte.</span><span class="sxs-lookup"><span data-stu-id="fe084-112">The stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) creates property sets on any storage object, not just on compound file storages.</span></span> <span data-ttu-id="fe084-113">L'implementazione autonoma non dipende dai file composti e può essere usata con qualsiasi implementazione di archivi strutturati.</span><span class="sxs-lookup"><span data-stu-id="fe084-113">The stand-alone implementation does not depend on compound files and can be used with any implementation of structured storages.</span></span> <span data-ttu-id="fe084-114">Tutte le restrizioni relative alle archiviazioni strutturate fornite dal chiamante si applicano a questa implementazione dei set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="fe084-114">Any restrictions on the caller-provided structured storages apply to this implementation of property sets.</span></span> <span data-ttu-id="fe084-115">Se ad esempio si fornisce un'archiviazione in modalità semplice per [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), il valore di **IPropertySetStorage** risultante sarà limitato dal [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)fornito.</span><span class="sxs-lookup"><span data-stu-id="fe084-115">For example, if you provide a simple-mode storage to [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), the resulting **IPropertySetStorage** will be restricted by the supplied [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage).</span></span>

<span data-ttu-id="fe084-116">Per ulteriori informazioni sull'implementazione del file composto di questa interfaccia, vedere la sezione [implementazione di file compositi IPropertySetStorage](ipropertysetstorage-compound-file-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="fe084-116">For more information about the compound file implementation of this interface, see the section [IPropertySetStorage-Compound File Implementation](ipropertysetstorage-compound-file-implementation.md).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="fe084-117">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="fe084-117">When to Use</span></span>

<span data-ttu-id="fe084-118">Chiamare i metodi di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) per creare, aprire ed eliminare set di proprietà in qualsiasi archivio strutturato.</span><span class="sxs-lookup"><span data-stu-id="fe084-118">Call the methods of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) to create, open, and delete property sets in any structured storage.</span></span> <span data-ttu-id="fe084-119">Esiste anche un metodo che fornisce un puntatore all'enumeratore [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) che può essere usato per enumerare i set di proprietà nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="fe084-119">There is also a method that supplies a pointer to the [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) enumerator that can be used to enumerate the property sets in the storage.</span></span>

<span data-ttu-id="fe084-120">L'implementazione autonoma fornisce anche le funzioni di supporto [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) e [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) , oltre ai metodi [**create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) e [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , per creare e aprire i set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="fe084-120">The stand-alone implementation also provides the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) and [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) helper functions, in addition to the [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) methods, to create and open property sets.</span></span> <span data-ttu-id="fe084-121">Queste due funzioni aggiungono il supporto per il \_ valore non memorizzato nel buffer PROPSETFLAG, in modo che sia possibile scrivere le modifiche direttamente nel set di proprietà anziché memorizzarle nel buffer in una cache.</span><span class="sxs-lookup"><span data-stu-id="fe084-121">These two functions add support for the PROPSETFLAG\_UNBUFFERED value so you can write changes directly to the property set instead of buffering them in a cache.</span></span> <span data-ttu-id="fe084-122">Per altre informazioni, vedere [**costanti PROPSETFLAG**](propsetflag-constants.md).</span><span class="sxs-lookup"><span data-stu-id="fe084-122">For more information, see [**PROPSETFLAG Constants**](propsetflag-constants.md).</span></span>

## <a name="methods"></a><span data-ttu-id="fe084-123">Metodi</span><span class="sxs-lookup"><span data-stu-id="fe084-123">Methods</span></span>

<span data-ttu-id="fe084-124">L'implementazione autonoma di [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="fe084-124">The stand-alone implementation of [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) supports the following methods.</span></span>

<dl> <dt>

<span data-ttu-id="fe084-125"><span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage:: create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)</span><span class="sxs-lookup"><span data-stu-id="fe084-125"><span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)</span></span>
</dt> <dd>

<span data-ttu-id="fe084-126">Crea un nuovo set di proprietà nell'archivio e restituisce un puntatore all'interfaccia [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) nel set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="fe084-126">Creates a new property set in the storage and returns a pointer to the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

<span data-ttu-id="fe084-127">Se si prevede di usare il valore PROPSETFLAG non \_ memorizzato nel buffer, usare invece la funzione [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) per creare e aprire il nuovo set di proprietà e ottenere un puntatore all'implementazione autonoma per l'interfaccia [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) nel set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="fe084-127">If you plan to use the PROPSETFLAG\_UNBUFFERED value, use the [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) function instead to create and open the new property set and to obtain a pointer to the stand-alone implementation for the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

</dd> <dt>

<span data-ttu-id="fe084-128"><span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)</span><span class="sxs-lookup"><span data-stu-id="fe084-128"><span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage::Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)</span></span>
</dt> <dd>

<span data-ttu-id="fe084-129">Apre un set di proprietà esistente nell'archiviazione e restituisce un puntatore all'interfaccia [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) nel set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="fe084-129">Opens an existing property set in the storage and returns a pointer to the [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) interface on the property set.</span></span>

<span data-ttu-id="fe084-130">Se si prevede di usare il valore PROPSETFLAG non \_ memorizzato nel buffer, usare invece la funzione [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) per ottenere un puntatore all'implementazione autonoma di [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) nel set di proprietà specificato.</span><span class="sxs-lookup"><span data-stu-id="fe084-130">If you plan to use the PROPSETFLAG\_UNBUFFERED value, use the [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) function instead to obtain a pointer to the stand-alone implementation of [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) on the specified property set.</span></span>

</dd> <dt>

<span data-ttu-id="fe084-131"><span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::D Elimina**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)</span><span class="sxs-lookup"><span data-stu-id="fe084-131"><span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage::Delete**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)</span></span>
</dt> <dd>

<span data-ttu-id="fe084-132">Elimina un set di proprietà in questa risorsa di archiviazione del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="fe084-132">Deletes a property set in this property set storage.</span></span>

</dd> <dt>

<span data-ttu-id="fe084-133"><span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage:: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)</span><span class="sxs-lookup"><span data-stu-id="fe084-133"><span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage::Enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)</span></span>
</dt> <dd>

<span data-ttu-id="fe084-134">Crea un oggetto che può essere utilizzato per enumerare le strutture [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) .</span><span class="sxs-lookup"><span data-stu-id="fe084-134">Creates an object that can be used to enumerate [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) structures.</span></span> <span data-ttu-id="fe084-135">Ogni struttura **STATPROPSETSTG** fornisce dati su un singolo set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="fe084-135">Each **STATPROPSETSTG** structure provides data about a single property set.</span></span>

> [!Note]  
> <span data-ttu-id="fe084-136">Il set di proprietà DocumentSummaryInformation e UserDefined è univoco in quanto può includere due sezioni del set di proprietà in un singolo flusso sottostante.</span><span class="sxs-lookup"><span data-stu-id="fe084-136">The DocumentSummaryInformation and UserDefined property set is unique in that it may have two property set sections in a single underlying stream.</span></span> <span data-ttu-id="fe084-137">Per ulteriori informazioni, vedere [i set di proprietà DocumentSummaryInformation e UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md) .</span><span class="sxs-lookup"><span data-stu-id="fe084-137">For more information, see [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md) .</span></span>

 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="fe084-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fe084-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe084-139">IPropertyStorage-implementazione autonoma</span><span class="sxs-lookup"><span data-stu-id="fe084-139">IPropertyStorage-Stand-alone Implementation</span></span>](ipropertystorage-stand-alone-implementation.md)
</dt> <dt>

[<span data-ttu-id="fe084-140">**IPropertySetStorage**</span><span class="sxs-lookup"><span data-stu-id="fe084-140">**IPropertySetStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[<span data-ttu-id="fe084-141">**IPropertyStorage**</span><span class="sxs-lookup"><span data-stu-id="fe084-141">**IPropertyStorage**</span></span>](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[<span data-ttu-id="fe084-142">**IStorage:: EnumElements**</span><span class="sxs-lookup"><span data-stu-id="fe084-142">**IStorage::EnumElements**</span></span>](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[<span data-ttu-id="fe084-143">**Costanti PROPSETFLAG**</span><span class="sxs-lookup"><span data-stu-id="fe084-143">**PROPSETFLAG Constants**</span></span>](propsetflag-constants.md)
</dt> <dt>

[<span data-ttu-id="fe084-144">**STATPROPSETSTG**</span><span class="sxs-lookup"><span data-stu-id="fe084-144">**STATPROPSETSTG**</span></span>](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> <dt>

[<span data-ttu-id="fe084-145">**StgCreatePropSetStg**</span><span class="sxs-lookup"><span data-stu-id="fe084-145">**StgCreatePropSetStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> <dt>

[<span data-ttu-id="fe084-146">**StgCreatePropStg**</span><span class="sxs-lookup"><span data-stu-id="fe084-146">**StgCreatePropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[<span data-ttu-id="fe084-147">**StgOpenPropStg**</span><span class="sxs-lookup"><span data-stu-id="fe084-147">**StgOpenPropStg**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[<span data-ttu-id="fe084-148">**Costanti STGM**</span><span class="sxs-lookup"><span data-stu-id="fe084-148">**STGM Constants**</span></span>](stgm-constants.md)
</dt> </dl>

 

 