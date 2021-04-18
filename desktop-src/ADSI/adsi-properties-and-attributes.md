---
title: Proprietà e attributi ADSI
description: Gli attributi vengono talvolta indicati come proprietà. Questo può causare confusione. In questa documentazione vengono utilizzate le seguenti definizioni per proprietà e attributi.
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- Proprietà ADSI e attributi ADSI
- ADSI ADSI, uso, accesso e manipolazione di dati, proprietà e attributi
- Proprietà ADSI
- attributi ADSI
- Proprietà ADSI, defined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c7b1dca9882f53b7fa746121ed431ace7f9af7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297701"
---
# <a name="adsi-properties-and-attributes"></a><span data-ttu-id="6bb40-110">Proprietà e attributi ADSI</span><span class="sxs-lookup"><span data-stu-id="6bb40-110">ADSI Properties and Attributes</span></span>

<span data-ttu-id="6bb40-111">Gli attributi vengono talvolta indicati come proprietà.</span><span class="sxs-lookup"><span data-stu-id="6bb40-111">Attributes are sometimes referred to as properties.</span></span> <span data-ttu-id="6bb40-112">Questo può causare confusione.</span><span class="sxs-lookup"><span data-stu-id="6bb40-112">This can cause confusion.</span></span> <span data-ttu-id="6bb40-113">In questa documentazione vengono utilizzate le seguenti definizioni per proprietà e attributi.</span><span class="sxs-lookup"><span data-stu-id="6bb40-113">This documentation uses the following definitions for properties and attributes.</span></span>

<span data-ttu-id="6bb40-114">Le proprietà sono valori denominati associati a un oggetto di programmazione.</span><span class="sxs-lookup"><span data-stu-id="6bb40-114">Properties are named values associated with a programming object.</span></span> <span data-ttu-id="6bb40-115">Ad esempio, l'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) espone proprietà quali la [**classe**](iads-property-methods.md) e il **nome**.</span><span class="sxs-lookup"><span data-stu-id="6bb40-115">For example, the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface exposes properties such as [**Class**](iads-property-methods.md) and **Name**.</span></span>

<span data-ttu-id="6bb40-116">Gli attributi sono i dati associati agli oggetti in un servizio directory.</span><span class="sxs-lookup"><span data-stu-id="6bb40-116">Attributes are the data associated with objects in a directory service.</span></span> <span data-ttu-id="6bb40-117">Ad esempio, un oggetto utente avrà un attributo denominato **CN** che contiene una stringa che rappresenta il nome distinto comune o relativo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6bb40-117">For example, a user object will have an attribute called **cn** which contains a string that is the common or relative distinguished name of the object.</span></span> <span data-ttu-id="6bb40-118">Gli attributi sono accessibili tramite metodi di interfaccia ADSI, ad esempio [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put).</span><span class="sxs-lookup"><span data-stu-id="6bb40-118">Attributes are accessible through ADSI interface methods such as [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put).</span></span>

<span data-ttu-id="6bb40-119">Per ulteriori informazioni sulle proprietà e sugli attributi ADSI, vedere:</span><span class="sxs-lookup"><span data-stu-id="6bb40-119">For more information about ADSI properties and attributes, see:</span></span>

-   [<span data-ttu-id="6bb40-120">Cache degli attributi ADSI</span><span class="sxs-lookup"><span data-stu-id="6bb40-120">The ADSI Attribute Cache</span></span>](the-adsi-attribute-cache.md)
-   [<span data-ttu-id="6bb40-121">Attributi singolo e più valori</span><span class="sxs-lookup"><span data-stu-id="6bb40-121">Single vs. Multiple Value Attributes</span></span>](single-vs--multiple-value-attributes.md)
-   [<span data-ttu-id="6bb40-122">Active Directory gli attributi operativi</span><span class="sxs-lookup"><span data-stu-id="6bb40-122">Active Directory Operational Attributes</span></span>](active-directory-operational-attributes.md)

 

 




