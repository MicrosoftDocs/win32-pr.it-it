---
title: CPROPS. CPP
description: Nel componente provider di esempio, è possibile trovare un esempio di implementazione della cache delle proprietà in cProps. cpp. I metodi supportati sono elencati nella tabella seguente.
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b9f4fddfea6900fd8d7a06bee9979744eefd30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855333"
---
# <a name="cpropscpp"></a><span data-ttu-id="467b6-104">CPROPS. CPP</span><span class="sxs-lookup"><span data-stu-id="467b6-104">CPROPS.CPP</span></span>

<span data-ttu-id="467b6-105">Nel componente provider di esempio, è possibile trovare un esempio di implementazione della cache delle proprietà in cProps. cpp.</span><span class="sxs-lookup"><span data-stu-id="467b6-105">In the example provider component, an example of a property cache implementation can be found in cprops.cpp.</span></span> <span data-ttu-id="467b6-106">I metodi supportati sono elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="467b6-106">Supported methods are listed in the following table.</span></span>



| <span data-ttu-id="467b6-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="467b6-107">Method</span></span>                                           | <span data-ttu-id="467b6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="467b6-108">Description</span></span>                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="467b6-109">**CPropertyCache:: AddProperty**</span><span class="sxs-lookup"><span data-stu-id="467b6-109">**CPropertyCache::addproperty**</span></span>                  | <span data-ttu-id="467b6-110">Estendere la cache delle proprietà aggiungendone una nuova.</span><span class="sxs-lookup"><span data-stu-id="467b6-110">Extend the property cache by adding a new one.</span></span>                                                                      |
| <span data-ttu-id="467b6-111">**CPropertyCache:: UpdateProperty**</span><span class="sxs-lookup"><span data-stu-id="467b6-111">**CPropertyCache::updateproperty**</span></span>               | <span data-ttu-id="467b6-112">Cercare la proprietà, liberarne il contenuto e usare invece i nuovi valori; contrassegnare quindi la cache modificata per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="467b6-112">Look up the property, free its contents, and use new values instead; then mark the cache changed for this property.</span></span> |
| <span data-ttu-id="467b6-113">**CPropertyCache:: FindProperty**</span><span class="sxs-lookup"><span data-stu-id="467b6-113">**CPropertyCache::findproperty**</span></span>                 | <span data-ttu-id="467b6-114">Cercare questa proprietà in base al nome; salvare il relativo indice.</span><span class="sxs-lookup"><span data-stu-id="467b6-114">Look up this property by name; save its index.</span></span>                                                                      |
| <span data-ttu-id="467b6-115">**CPropertyCache:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="467b6-115">**CPropertyCache::getproperty**</span></span>                  | <span data-ttu-id="467b6-116">Trovare la proprietà nella cache, se disponibile, in caso contrario chiamare **GetInfo**.</span><span class="sxs-lookup"><span data-stu-id="467b6-116">Find the property in the cache if available, otherwise call **GetInfo**.</span></span> <span data-ttu-id="467b6-117">Impostare l'indice e copiare i nuovi valori.</span><span class="sxs-lookup"><span data-stu-id="467b6-117">Set the index and copy in the new values.</span></span>  |
| <span data-ttu-id="467b6-118">**CPropertyCache::p utproperty**</span><span class="sxs-lookup"><span data-stu-id="467b6-118">**CPropertyCache::putproperty**</span></span>                  | <span data-ttu-id="467b6-119">Trovare la proprietà.</span><span class="sxs-lookup"><span data-stu-id="467b6-119">Find the property.</span></span> <span data-ttu-id="467b6-120">Liberare le informazioni disponibili e inserire i nuovi valori.</span><span class="sxs-lookup"><span data-stu-id="467b6-120">Free what was there and put in new values.</span></span>                                                       |
| <span data-ttu-id="467b6-121">**CPropertyCache:: CPropertyCache**</span><span class="sxs-lookup"><span data-stu-id="467b6-121">**CPropertyCache::CPropertyCache**</span></span>               | <span data-ttu-id="467b6-122">Costruttore standard.</span><span class="sxs-lookup"><span data-stu-id="467b6-122">Standard constructor.</span></span>                                                                                               |
| <span data-ttu-id="467b6-123">**CPropertyCache:: ~ CPropertyCache**</span><span class="sxs-lookup"><span data-stu-id="467b6-123">**CPropertyCache::~CPropertyCache**</span></span>              | <span data-ttu-id="467b6-124">Distruttore standard.</span><span class="sxs-lookup"><span data-stu-id="467b6-124">Standard destructor.</span></span>                                                                                                |
| <span data-ttu-id="467b6-125">**CPropertyCache:: createpropertycache**</span><span class="sxs-lookup"><span data-stu-id="467b6-125">**CPropertyCache::createpropertycache**</span></span>          | <span data-ttu-id="467b6-126">Creare la cache.</span><span class="sxs-lookup"><span data-stu-id="467b6-126">Create the cache.</span></span>                                                                                                   |
| <span data-ttu-id="467b6-127">**CPropertyCache:: unboundgetproperty**</span><span class="sxs-lookup"><span data-stu-id="467b6-127">**CPropertyCache::unboundgetproperty**</span></span>           | <span data-ttu-id="467b6-128">Trovare la proprietà nella cache e impostarla su questi valori.</span><span class="sxs-lookup"><span data-stu-id="467b6-128">Find the property in the cache and set it to these values.</span></span>                                                          |
| <span data-ttu-id="467b6-129">**CPropertyCache:: SampleDSMarshallProperties**</span><span class="sxs-lookup"><span data-stu-id="467b6-129">**CPropertyCache::SampleDSMarshallProperties**</span></span>   | <span data-ttu-id="467b6-130">Eseguire il marshalling dei dati e dei valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="467b6-130">Marshal property data and values.</span></span>                                                                                   |
| <span data-ttu-id="467b6-131">**CPropertyCache:: marshallproperty**</span><span class="sxs-lookup"><span data-stu-id="467b6-131">**CPropertyCache::marshallproperty**</span></span>             | <span data-ttu-id="467b6-132">Eseguire il marshalling di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="467b6-132">Marshal a property.</span></span>                                                                                                 |
| <span data-ttu-id="467b6-133">**CPropertyCache:: SampleDSUnMarshallProperties**</span><span class="sxs-lookup"><span data-stu-id="467b6-133">**CPropertyCache::SampleDSUnMarshallProperties**</span></span> | <span data-ttu-id="467b6-134">Annullare il marshalling dei dati e dei valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="467b6-134">Unmarshal property data and values.</span></span>                                                                                 |
| <span data-ttu-id="467b6-135">**CPropertyCache:: unmarshallproperty**</span><span class="sxs-lookup"><span data-stu-id="467b6-135">**CPropertyCache::unmarshallproperty**</span></span>           | <span data-ttu-id="467b6-136">Annullare il marshalling di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="467b6-136">Unmarshal a property.</span></span>                                                                                               |



 

 

 




