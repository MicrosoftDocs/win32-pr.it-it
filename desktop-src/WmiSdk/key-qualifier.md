---
description: Il qualificatore chiave indica se la proprietà fa parte dell'handle dello spazio dei nomi.
ms.assetid: 838d295f-e812-4e46-99a4-d2714a0ae8dc
ms.tgt_platform: multiple
title: Qualificatore chiave
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Key
api_type:
- NA
api_location: ''
ms.openlocfilehash: affc9f4be594723700a65c9c92f8ae37ffead265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758324"
---
# <a name="key-qualifier"></a><span data-ttu-id="351eb-103">Qualificatore chiave</span><span class="sxs-lookup"><span data-stu-id="351eb-103">Key Qualifier</span></span>

<span data-ttu-id="351eb-104">Il qualificatore **chiave** indica se la proprietà fa parte dell'handle dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="351eb-104">The **Key** qualifier indicates whether the property is part of the namespace handle.</span></span> <span data-ttu-id="351eb-105">Se più di una proprietà dispone del qualificatore **chiave** , tutte queste proprietà costituiscono collettivamente la chiave (una chiave composta).</span><span class="sxs-lookup"><span data-stu-id="351eb-105">If more than one property has the **Key** qualifier, then all such properties collectively form the key (a compound key).</span></span> <span data-ttu-id="351eb-106">Quando vengono rilevate insieme, le proprietà chiave devono fornire un riferimento univoco per ogni istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="351eb-106">When taken together, the key properties must supply a unique reference for each class instance.</span></span> <span data-ttu-id="351eb-107">Se questo qualificatore viene inserito in una proprietà, è consentito solo il valore **true** .</span><span class="sxs-lookup"><span data-stu-id="351eb-107">If this qualifier is placed on a property, only the value **TRUE** is allowed.</span></span>

<span data-ttu-id="351eb-108">È possibile utilizzare qualsiasi tipo di proprietà, ad eccezione di quanto segue:</span><span class="sxs-lookup"><span data-stu-id="351eb-108">You can use any property type except for the following:</span></span>

-   <span data-ttu-id="351eb-109">Matrici</span><span class="sxs-lookup"><span data-stu-id="351eb-109">Arrays</span></span>
-   <span data-ttu-id="351eb-110">Numeri reali e a virgola mobile</span><span class="sxs-lookup"><span data-stu-id="351eb-110">Real and floating-point numbers</span></span>
-   <span data-ttu-id="351eb-111">Oggetti incorporati</span><span class="sxs-lookup"><span data-stu-id="351eb-111">Embedded objects</span></span>
-   <span data-ttu-id="351eb-112">Caratteri inferiori a ASCII 32 (ovvero spazi vuoti)</span><span class="sxs-lookup"><span data-stu-id="351eb-112">Characters lower than ASCII 32 (that is, white space characters)</span></span>
-   <span data-ttu-id="351eb-113">Le stringhe di caratteri di tipo **Char16** o stringhe di caratteri definite come chiavi devono contenere valori maggiori di U + 0020.</span><span class="sxs-lookup"><span data-stu-id="351eb-113">Character strings of type **char16** or character strings that are defined as keys must contain values greater than U+0020.</span></span> <span data-ttu-id="351eb-114">Questo perché WMI usa i valori di chiave nei percorsi degli oggetti e non è possibile usare caratteri non stampabili in un percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="351eb-114">This is because WMI uses key values in object paths, and you cannot use nonprinting characters in an object path.</span></span>

<span data-ttu-id="351eb-115">Quando una classe padre specifica una chiave, tutte le classi derivate dalla classe padre ereditano tale chiave.</span><span class="sxs-lookup"><span data-stu-id="351eb-115">When a parent class specifies a key, all classes derived from the parent class inherit that key.</span></span> <span data-ttu-id="351eb-116">Le classi derivate non possono modificare la chiave ereditata o definire una nuova proprietà della chiave.</span><span class="sxs-lookup"><span data-stu-id="351eb-116">The derived classes cannot alter the inherited key or define any new key property.</span></span> <span data-ttu-id="351eb-117">Tuttavia, quando si deriva una sottoclasse da una classe astratta senza una chiave, è possibile introdurre una chiave nella sottoclasse.</span><span class="sxs-lookup"><span data-stu-id="351eb-117">However, when you derive a subclass from an abstract class without a key, you can introduce a key in the subclass.</span></span>

<span data-ttu-id="351eb-118">Tutte le classi che definiscono più istanze devono specificare una chiave.</span><span class="sxs-lookup"><span data-stu-id="351eb-118">All classes that define more than one instance must specify a key.</span></span> <span data-ttu-id="351eb-119">Poiché le classi astratte non definiscono alcuna istanza, non è necessario specificare chiavi.</span><span class="sxs-lookup"><span data-stu-id="351eb-119">Because abstract classes do not define any instances, they do not need to specify keys.</span></span> <span data-ttu-id="351eb-120">Poiché le classi singleton definiscono solo un'istanza, non possono specificare chiavi.</span><span class="sxs-lookup"><span data-stu-id="351eb-120">Because singleton classes define only one instance, they cannot specify keys.</span></span>

<span data-ttu-id="351eb-121">Le chiavi vengono scritte una volta alla creazione dell'istanza dell'oggetto e non devono essere modificate in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="351eb-121">Keys are written one time at object instantiation and must not be modified later.</span></span> <span data-ttu-id="351eb-122">Non ha senso applicare un valore predefinito a una proprietà con chiave qualificata.</span><span class="sxs-lookup"><span data-stu-id="351eb-122">It does not make sense to apply a default value to a key-qualified property.</span></span>

## <a name="requirements"></a><span data-ttu-id="351eb-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="351eb-123">Requirements</span></span>



| <span data-ttu-id="351eb-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="351eb-124">Requirement</span></span> | <span data-ttu-id="351eb-125">Valore</span><span class="sxs-lookup"><span data-stu-id="351eb-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="351eb-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="351eb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="351eb-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="351eb-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="351eb-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="351eb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="351eb-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="351eb-129">Windows Server 2008</span></span><br/> |



 

 




