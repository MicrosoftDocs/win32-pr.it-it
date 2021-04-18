---
title: CCLSOBJ. CPP
description: Nel componente provider di esempio, le funzioni per l'oggetto classe di schema sono contenute in cclsobj. cpp.
ms.assetid: e8cdef8e-c031-49e0-9496-871064aec8bd
ms.tgt_platform: multiple
keywords:
- CSampleDSClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23c198413819627ce1fcb5a605bd8e45faae0ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297695"
---
# <a name="cclsobjcpp"></a><span data-ttu-id="024e0-104">CCLSOBJ. CPP</span><span class="sxs-lookup"><span data-stu-id="024e0-104">CCLSOBJ.CPP</span></span>

<span data-ttu-id="024e0-105">Nel componente provider di esempio, le funzioni per l'oggetto classe di schema sono contenute in cclsobj. cpp.</span><span class="sxs-lookup"><span data-stu-id="024e0-105">In the example provider component, the functions for the schema class object are contained in cclsobj.cpp.</span></span>

<span data-ttu-id="024e0-106">La classe **CSampleDSClass** è definita in questo file.</span><span class="sxs-lookup"><span data-stu-id="024e0-106">The **CSampleDSClass** class is defined in this file.</span></span> <span data-ttu-id="024e0-107">**CSampleDSClass** viene definito con i metodi e le proprietà elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="024e0-107">**CSampleDSClass** is defined with methods and properties listed in the following table.</span></span>



| <span data-ttu-id="024e0-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="024e0-108">Method</span></span>                      | <span data-ttu-id="024e0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="024e0-109">Description</span></span>                                                                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="024e0-110">**CSampleDSClass**</span><span class="sxs-lookup"><span data-stu-id="024e0-110">**CSampleDSClass**</span></span>          | <span data-ttu-id="024e0-111">Costruttore standard.</span><span class="sxs-lookup"><span data-stu-id="024e0-111">Standard constructor.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="024e0-112">**~ CSampleDSClass**</span><span class="sxs-lookup"><span data-stu-id="024e0-112">**~CSampleDSClass**</span></span>         | <span data-ttu-id="024e0-113">Distruttore standard.</span><span class="sxs-lookup"><span data-stu-id="024e0-113">Standard destructor.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="024e0-114">**CreateClass**</span><span class="sxs-lookup"><span data-stu-id="024e0-114">**CreateClass**</span></span>             | <span data-ttu-id="024e0-115">Creare un oggetto classe di schema ADs.</span><span class="sxs-lookup"><span data-stu-id="024e0-115">Create an ADs schema class object.</span></span> <span data-ttu-id="024e0-116">Definizioni degli attributi di ricerca chiamando **SampleDSGetClassDefinition**.</span><span class="sxs-lookup"><span data-stu-id="024e0-116">Lookup attribute definitions by calling **SampleDSGetClassDefinition**.</span></span>                                                                                                 |
| <span data-ttu-id="024e0-117">**CreateClass**</span><span class="sxs-lookup"><span data-stu-id="024e0-117">**CreateClass**</span></span>             | <span data-ttu-id="024e0-118">Creare un oggetto classe di schema, in base alle definizioni degli attributi, impostando attributi noti, ad esempio quelli elencati in [**IADsClass:: MandatoryAttributes**](iadsclass-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="024e0-118">Create a schema class object, given the attribute definitions, setting known attributes, such as those listed in [**IADsClass::MandatoryAttributes**](iadsclass-property-methods.md).</span></span>                     |
| <span data-ttu-id="024e0-119">**AllocateClassObject**</span><span class="sxs-lookup"><span data-stu-id="024e0-119">**AllocateClassObject**</span></span>     | <span data-ttu-id="024e0-120">Creare un oggetto classe di schema e caricarne i dati di tipo.</span><span class="sxs-lookup"><span data-stu-id="024e0-120">Create a schema class object and load its type data.</span></span>                                                                                                                                                       |
| <span data-ttu-id="024e0-121">**QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="024e0-121">**QueryInterface**</span></span>          | <span data-ttu-id="024e0-122">Restituisce il puntatore a interfaccia richiesto, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="024e0-122">Return the requested interface pointer, if available.</span></span>                                                                                                                                                      |
| <span data-ttu-id="024e0-123">Metodi IADs standard.</span><span class="sxs-lookup"><span data-stu-id="024e0-123">Standard IADs methods.</span></span>      | <span data-ttu-id="024e0-124">Metodi di interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) standard inclusi in questo file.</span><span class="sxs-lookup"><span data-stu-id="024e0-124">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface methods included in this file.</span></span>                                                                                                                                     |
| <span data-ttu-id="024e0-125">Metodi IADsClass standard.</span><span class="sxs-lookup"><span data-stu-id="024e0-125">Standard IADsClass methods.</span></span> | <span data-ttu-id="024e0-126">Metodi di interfaccia [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) standard inclusi in questo file.</span><span class="sxs-lookup"><span data-stu-id="024e0-126">Standard [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface methods included in this file.</span></span>                                                                                                                           |
| <span data-ttu-id="024e0-127">**CreatePropertyList**</span><span class="sxs-lookup"><span data-stu-id="024e0-127">**CreatePropertyList**</span></span>      | <span data-ttu-id="024e0-128">Creare un elenco di proprietà associate a questa classe dello schema chiamando **CreatePropertyEntry**.</span><span class="sxs-lookup"><span data-stu-id="024e0-128">Create a list of properties associated with this schema class by calling **CreatePropertyEntry**.</span></span>                                                                                                          |
| <span data-ttu-id="024e0-129">**CreatePropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="024e0-129">**CreatePropertyEntry**</span></span>     | <span data-ttu-id="024e0-130">Creare un oggetto proprietà in questa classe dello schema.</span><span class="sxs-lookup"><span data-stu-id="024e0-130">Create one property object in this schema class.</span></span>                                                                                                                                                           |
| <span data-ttu-id="024e0-131">**FreePropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="024e0-131">**FreePropertyEntry**</span></span>       | <span data-ttu-id="024e0-132">Liberare la voce in **CreatePropertyEntry**.</span><span class="sxs-lookup"><span data-stu-id="024e0-132">Free the entry made in **CreatePropertyEntry**.</span></span>                                                                                                                                                            |
| <span data-ttu-id="024e0-133">**MakeVariantFromPropList**</span><span class="sxs-lookup"><span data-stu-id="024e0-133">**MakeVariantFromPropList**</span></span> | <span data-ttu-id="024e0-134">Creare una matrice di varianti dall'elenco di proprietà creato da **CreatePropertyList**.</span><span class="sxs-lookup"><span data-stu-id="024e0-134">Create an array of VARIANTS from the property list created by **CreatePropertyList**.</span></span> <span data-ttu-id="024e0-135">Può essere usato nell'implementazione di [**IADsClass:: MandatoryAttributes**](iadsclass-property-methods.md) e così via.</span><span class="sxs-lookup"><span data-stu-id="024e0-135">Can be used in the implementation of [**IADsClass::MandatoryAttributes**](iadsclass-property-methods.md) and so on.</span></span> |



 

 

 




