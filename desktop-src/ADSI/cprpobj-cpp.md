---
title: CPRPOBJ. CPP
description: Nel componente provider di esempio, i metodi dell'oggetto Property, in cprpobj. cpp, sono elencati nella tabella seguente.
ms.assetid: 88628b9b-12e6-4d64-9a21-b30f7392a5f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948409cc135daaffa249f8aa0b3729b34799957c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220919"
---
# <a name="cprpobjcpp"></a><span data-ttu-id="a79ce-103">CPRPOBJ. CPP</span><span class="sxs-lookup"><span data-stu-id="a79ce-103">CPRPOBJ.CPP</span></span>

<span data-ttu-id="a79ce-104">Nel componente provider di esempio, i metodi dell'oggetto Property, in cprpobj. cpp, sono elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a79ce-104">In the example provider component, property object methods, in cprpobj.cpp, are listed in the following table.</span></span>



| <span data-ttu-id="a79ce-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="a79ce-105">Method</span></span>                                                 | <span data-ttu-id="a79ce-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a79ce-106">Description</span></span>                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a79ce-107">**CSampleDSProperty::CSampleDSProperty**</span><span class="sxs-lookup"><span data-stu-id="a79ce-107">**CSampleDSProperty::CSampleDSProperty**</span></span>               | <span data-ttu-id="a79ce-108">Costruttore standard.</span><span class="sxs-lookup"><span data-stu-id="a79ce-108">Standard constructor.</span></span>                                                                                                                          |
| <span data-ttu-id="a79ce-109">**CSampleDSProperty:: ~ CSampleDSProperty**</span><span class="sxs-lookup"><span data-stu-id="a79ce-109">**CSampleDSProperty::~CSampleDSProperty**</span></span>              | <span data-ttu-id="a79ce-110">Distruttore standard.</span><span class="sxs-lookup"><span data-stu-id="a79ce-110">Standard destructor.</span></span>                                                                                                                           |
| <span data-ttu-id="a79ce-111">**CSampleDSProperty:: CreateProperty**</span><span class="sxs-lookup"><span data-stu-id="a79ce-111">**CSampleDSProperty::CreateProperty**</span></span>                  | <span data-ttu-id="a79ce-112">Creare un oggetto proprietà ADS, cercando le definizioni degli attributi chiamando **SampleDSGetPropertyDefinition**.</span><span class="sxs-lookup"><span data-stu-id="a79ce-112">Create an ADS Property object, looking up the attribute definitions by calling **SampleDSGetPropertyDefinition**.</span></span>                              |
| <span data-ttu-id="a79ce-113">**CSampleDSProperty:: CreateProperty**</span><span class="sxs-lookup"><span data-stu-id="a79ce-113">**CSampleDSProperty::CreateProperty**</span></span>                  | <span data-ttu-id="a79ce-114">Data la definizione dell'attributo, creare un oggetto Property, impostando la corrispondenza tra le sintassi degli annunci supportati e le sintassi del provider.</span><span class="sxs-lookup"><span data-stu-id="a79ce-114">Given the attribute definition, create a property object, setting the correspondence between supported ADS syntaxes and the provider syntaxes.</span></span> |
| <span data-ttu-id="a79ce-115">**CSampleDSProperty::AllocatePropertyObject**</span><span class="sxs-lookup"><span data-stu-id="a79ce-115">**CSampleDSProperty::AllocatePropertyObject**</span></span>          | <span data-ttu-id="a79ce-116">Creare un oggetto proprietà e caricarne i dati di tipo.</span><span class="sxs-lookup"><span data-stu-id="a79ce-116">Create a property object and load its type data.</span></span>                                                                                               |
| <span data-ttu-id="a79ce-117">**CSampleDSProperty:: QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="a79ce-117">**CSampleDSProperty::QueryInterface**</span></span>                  | <span data-ttu-id="a79ce-118">Restituisce il puntatore a interfaccia richiesto, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="a79ce-118">Return the requested interface pointer, if available.</span></span>                                                                                          |
| <span data-ttu-id="a79ce-119">Metodi [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) standard.</span><span class="sxs-lookup"><span data-stu-id="a79ce-119">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) methods.</span></span>                 |                                                                                                                                                |
| <span data-ttu-id="a79ce-120">Metodi [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) standard.</span><span class="sxs-lookup"><span data-stu-id="a79ce-120">Standard [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) methods.</span></span> |                                                                                                                                                |
| <span data-ttu-id="a79ce-121">**MapSyntaxIdtoADsSyntax**</span><span class="sxs-lookup"><span data-stu-id="a79ce-121">**MapSyntaxIdtoADsSyntax**</span></span>                             | <span data-ttu-id="a79ce-122">Impostare la corrispondenza tra l'ID sintassi e la sintassi ADS.</span><span class="sxs-lookup"><span data-stu-id="a79ce-122">Set the correspondence between the syntax ID and the ADS syntax.</span></span>                                                                               |
| <span data-ttu-id="a79ce-123">**MapSyntaxIdtoSampleDSSyntax**</span><span class="sxs-lookup"><span data-stu-id="a79ce-123">**MapSyntaxIdtoSampleDSSyntax**</span></span>                        | <span data-ttu-id="a79ce-124">Impostare la corrispondenza tra l'ID sintassi e la sintassi del provider.</span><span class="sxs-lookup"><span data-stu-id="a79ce-124">Set the correspondence between the syntax ID and the provider syntax.</span></span>                                                                          |



 

 

 




