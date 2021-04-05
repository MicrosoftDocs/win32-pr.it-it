---
title: CENUMSCH. CPP
description: Nel componente provider di esempio, l'enumerazione di un oggetto dello schema utilizza i metodi, da cenumsch. cpp, elencati nella tabella seguente.
ms.assetid: edad1ad1-16b9-40f3-b841-a70aa7fff5d9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcc6d053bb698817ff73db876b00640ed00c8ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855345"
---
# <a name="cenumschcpp"></a><span data-ttu-id="c797e-103">CENUMSCH. CPP</span><span class="sxs-lookup"><span data-stu-id="c797e-103">CENUMSCH.CPP</span></span>

<span data-ttu-id="c797e-104">Nel componente provider di esempio, l'enumerazione di un oggetto dello schema utilizza i metodi, da cenumsch. cpp, elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c797e-104">In the example provider component, the enumeration of a schema object uses the methods, from cenumsch.cpp, listed in the following table.</span></span>



| <span data-ttu-id="c797e-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="c797e-105">Method</span></span>                                        | <span data-ttu-id="c797e-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c797e-106">Description</span></span>                                                                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c797e-107">**CSampleDSSchemaEnum:: create**</span><span class="sxs-lookup"><span data-stu-id="c797e-107">**CSampleDSSchemaEnum::Create**</span></span>               | <span data-ttu-id="c797e-108">Creare un oggetto per consentire l'enumerazione di un oggetto classe di schema ADSI.</span><span class="sxs-lookup"><span data-stu-id="c797e-108">Create an object to allow enumeration of an ADSI schema class object.</span></span>                                                |
| <span data-ttu-id="c797e-109">**CSampleDSSchemaEnum::CSampleDSSchemaEnum**</span><span class="sxs-lookup"><span data-stu-id="c797e-109">**CSampleDSSchemaEnum::CSampleDSSchemaEnum**</span></span>  | <span data-ttu-id="c797e-110">Costruttore standard.</span><span class="sxs-lookup"><span data-stu-id="c797e-110">Standard constructor.</span></span>                                                                                                |
| <span data-ttu-id="c797e-111">**CSampleDSSchemaEnum:: ~ CSampleDSSchemaEnum**</span><span class="sxs-lookup"><span data-stu-id="c797e-111">**CSampleDSSchemaEnum::~CSampleDSSchemaEnum**</span></span> | <span data-ttu-id="c797e-112">Distruttore standard.</span><span class="sxs-lookup"><span data-stu-id="c797e-112">Standard destructor.</span></span>                                                                                                 |
| <span data-ttu-id="c797e-113">**CSampleDSSchemaEnum:: Next**</span><span class="sxs-lookup"><span data-stu-id="c797e-113">**CSampleDSSchemaEnum::Next**</span></span>                 | <span data-ttu-id="c797e-114">Recupera il numero specificato di elementi dall'oggetto dello schema indicato.</span><span class="sxs-lookup"><span data-stu-id="c797e-114">Retrieve the specified number of elements from the schema object indicated.</span></span>                                          |
| <span data-ttu-id="c797e-115">**CSampleDSSchemaEnum:: EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="c797e-115">**CSampleDSSchemaEnum::EnumObjects**</span></span>          | <span data-ttu-id="c797e-116">Gestire il recupero dei puntatori di interfaccia agli oggetti del tipo di oggetto indicato.</span><span class="sxs-lookup"><span data-stu-id="c797e-116">Manage retrieving the interfaces pointers to the objects of the object type indicated.</span></span>                               |
| <span data-ttu-id="c797e-117">**CSampleDSSchemaEnum:: EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="c797e-117">**CSampleDSSchemaEnum::EnumObjects**</span></span>          | <span data-ttu-id="c797e-118">Gestire il recupero dei puntatori di interfaccia agli oggetti del tipo di oggetto predefinito.</span><span class="sxs-lookup"><span data-stu-id="c797e-118">Manage retrieving the interface pointers to the objects of the default object type.</span></span>                                  |
| <span data-ttu-id="c797e-119">**CSampleDSSchemaEnum::EnumClasses**</span><span class="sxs-lookup"><span data-stu-id="c797e-119">**CSampleDSSchemaEnum::EnumClasses**</span></span>          | <span data-ttu-id="c797e-120">Gestire il recupero dei puntatori di interfaccia solo agli oggetti della classe di schema contenuti in questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="c797e-120">Manage retrieving the interface pointers to only the schema class objects contained in this object.</span></span>                  |
| <span data-ttu-id="c797e-121">**CSampleDSSchemaEnum:: GetClassObject**</span><span class="sxs-lookup"><span data-stu-id="c797e-121">**CSampleDSSchemaEnum::GetClassObject**</span></span>       | <span data-ttu-id="c797e-122">Recuperare la definizione della classe dello schema successiva; Se trovato, creare un oggetto classe di schema e restituire il puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c797e-122">Retrieve the next schema class definition; if found, create a schema class object, and return the interface pointer.</span></span> |
| <span data-ttu-id="c797e-123">**CSampleDSSchemaEnum:: EnumProperties**</span><span class="sxs-lookup"><span data-stu-id="c797e-123">**CSampleDSSchemaEnum::EnumProperties**</span></span>       | <span data-ttu-id="c797e-124">Gestire il recupero dei puntatori di interfaccia agli oggetti proprietà contenuti solo in questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="c797e-124">Manage retrieving the interface pointers to the property objects only contained in this object.</span></span>                      |
| <span data-ttu-id="c797e-125">**CSampleDSSchemaEnum:: GetPropertyObject**</span><span class="sxs-lookup"><span data-stu-id="c797e-125">**CSampleDSSchemaEnum::GetPropertyObject**</span></span>    | <span data-ttu-id="c797e-126">Recuperare la definizione di proprietà successiva. Se trovato, creare un oggetto classe di schema e restituire il puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c797e-126">Retrieve the next property definition; if found, create a schema class object, and return the interface pointer.</span></span>     |
| <span data-ttu-id="c797e-127">**CSampleDSSchemaEnum::EnumSyntaxes**</span><span class="sxs-lookup"><span data-stu-id="c797e-127">**CSampleDSSchemaEnum::EnumSyntaxes**</span></span>         | <span data-ttu-id="c797e-128">Gestire il recupero dei puntatori di interfaccia agli oggetti della sintassi contenuti solo in questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="c797e-128">Manage retrieving the interface pointers to the syntax objects only contained in this object.</span></span>                        |
| <span data-ttu-id="c797e-129">**CSampleDSSchemaEnum::GetSyntaxObject**</span><span class="sxs-lookup"><span data-stu-id="c797e-129">**CSampleDSSchemaEnum::GetSyntaxObject**</span></span>      | <span data-ttu-id="c797e-130">Recuperare la definizione della sintassi successiva; Se trovato, creare un oggetto classe di schema e restituire il puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c797e-130">Retrieve the next syntax definition; if found, create a schema class object, and return the interface pointer.</span></span>       |



 

 

 




