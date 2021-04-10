---
description: Un qualificatore è un flag che descrive ulteriori informazioni su un qualificatore.
ms.assetid: a7d9d1c0-9386-4c90-9788-993b35ed12db
ms.tgt_platform: multiple
title: Descrizione di un qualificatore con una versione di qualificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cfc2c590ec8916e2e9538b3e8224e97b3b5dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226949"
---
# <a name="describing-a-qualifier-with-a-qualifier-flavor"></a><span data-ttu-id="aad43-103">Descrizione di un qualificatore con una versione di qualificatore</span><span class="sxs-lookup"><span data-stu-id="aad43-103">Describing a Qualifier with a Qualifier Flavor</span></span>

<span data-ttu-id="aad43-104">Un [*qualificatore*](gloss-q.md) è un flag che descrive ulteriori informazioni su un qualificatore.</span><span class="sxs-lookup"><span data-stu-id="aad43-104">A [*qualifier flavor*](gloss-q.md) is a flag that describes more information about a qualifier.</span></span> <span data-ttu-id="aad43-105">Ad esempio, la versione del qualificatore con restrizioni indica che WMI non deve propagare il qualificatore associato a tutte le classi o istanze derivate.</span><span class="sxs-lookup"><span data-stu-id="aad43-105">For example, the Restricted qualifier flavor states that WMI should not propagate the associated qualifier to any derived classes or instances.</span></span> <span data-ttu-id="aad43-106">È possibile impostare le versioni utilizzando il codice MOF o a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="aad43-106">You can set flavors using either MOF code or programmatically.</span></span> <span data-ttu-id="aad43-107">Sebbene sia possibile descrivere diversi effetti con le varianti, lo scopo principale dei flag di sapore è quello di definire la modalità di propagazione dei qualificatori tramite l'ereditarietà da parte di WMI.</span><span class="sxs-lookup"><span data-stu-id="aad43-107">While you can describe a variety of effects with flavors, the main purposes of flavor flags is to define how WMI propagates qualifiers through inheritance.</span></span>

<span data-ttu-id="aad43-108">WMI definisce diverse versioni del qualificatore che è possibile alleghi a qualsiasi qualificatore, indipendentemente dall'origine del qualificatore.</span><span class="sxs-lookup"><span data-stu-id="aad43-108">WMI defines several qualifier flavors that you can attach to any qualifier, regardless of the origin of the qualifier.</span></span> <span data-ttu-id="aad43-109">Tuttavia, alcune versioni non sono appropriate per tutti i tipi di qualificatore.</span><span class="sxs-lookup"><span data-stu-id="aad43-109">However, some flavors are not appropriate for all qualifier types.</span></span> <span data-ttu-id="aad43-110">La caratteristica **ToClass** , ad esempio, è appropriata solo per i qualificatori definiti per una classe.</span><span class="sxs-lookup"><span data-stu-id="aad43-110">The **ToSubClass** flavor, for example, is appropriate only for qualifiers defined for a class.</span></span> <span data-ttu-id="aad43-111">Non è possibile aggiungere **ToClass** a un qualificatore usato per descrivere un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="aad43-111">You cannot attach **ToSubClass** to a qualifier used to describe an instance.</span></span>

<span data-ttu-id="aad43-112">È possibile utilizzare le varianti per descrivere diversi effetti per i qualificatori.</span><span class="sxs-lookup"><span data-stu-id="aad43-112">You can use flavors to describe a variety of different effects for qualifiers.</span></span> <span data-ttu-id="aad43-113">Il flavor può, ad esempio, indicare se un qualificatore può essere localizzato.</span><span class="sxs-lookup"><span data-stu-id="aad43-113">For example, flavor can indicate if a qualifier can be localized.</span></span> <span data-ttu-id="aad43-114">Uno degli scopi principali di una versione del qualificatore consiste tuttavia nel descrivere se una classe padre può passare i qualificatori a una sottoclasse o a un'istanza della classe.</span><span class="sxs-lookup"><span data-stu-id="aad43-114">However, one of the main purposes of a qualifier flavor is to describe whether a parent class can pass qualifiers to a subclass or class instance.</span></span> <span data-ttu-id="aad43-115">È anche possibile usare i tipi per determinare se una proprietà della classe passa un qualificatore a una proprietà dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="aad43-115">You can also use flavors to determine if a class property passes a qualifier on to an instance property.</span></span> <span data-ttu-id="aad43-116">Usare infine le versioni per indicare se una sottoclasse può eseguire l'override del valore originale di un qualificatore ereditato.</span><span class="sxs-lookup"><span data-stu-id="aad43-116">Finally, use flavors to state whether a subclass can override the original value of an inherited qualifier.</span></span> <span data-ttu-id="aad43-117">Tuttavia, i qualificatori dichiarati per una classe o un'istanza non vengono propagati alle proprietà di tale classe o istanza.</span><span class="sxs-lookup"><span data-stu-id="aad43-117">However, qualifiers that you declare for a class or instance do not propagate to the properties of that class or instance.</span></span> <span data-ttu-id="aad43-118">Inoltre **, le versioni** che stabiliscono le autorizzazioni di sostituzione sono valide solo se si impostano anche le versioni **ToClass o ToClass** .</span><span class="sxs-lookup"><span data-stu-id="aad43-118">Further, flavors that establish override permissions are valid only if you also set the **ToInstance** or **ToSubClass** flavors.</span></span>

<span data-ttu-id="aad43-119">Una versione può essere assegnata a livello globale a un qualificatore per un intero file MOF usando la sintassi seguente, in cui lo spazio vuoto funge da delimitatore quando vengono specificate più versioni.</span><span class="sxs-lookup"><span data-stu-id="aad43-119">A flavor can be globally assigned to a qualifier for an entire MOF file using the following syntax in which white space acts as the delimiter when multiple flavors are specified.</span></span>

``` syntax
Qualifier QualifierName : flavor1 <flavor2...>;
```

<span data-ttu-id="aad43-120">Le versioni globali si applicano a tutti gli utilizzi successivi del qualificatore nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="aad43-120">Global flavors apply to all subsequent uses of the qualifier in the MOF file.</span></span> <span data-ttu-id="aad43-121">Le istruzioni di sapore globale possono essere presenti in qualsiasi punto del file all'esterno di un blocco di dichiarazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="aad43-121">Global flavor statements may occur anywhere in the file outside of an object declaration block.</span></span> <span data-ttu-id="aad43-122">Le versioni ridefinite a livello di classe, istanza o proprietà sostituiscono le dichiarazioni di sapore globale per l'ambito di tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="aad43-122">Flavors redefined at the class, instance, or property level override the global flavor declarations for the scope of that object.</span></span>

<span data-ttu-id="aad43-123">Non è possibile definire una nuova versione.</span><span class="sxs-lookup"><span data-stu-id="aad43-123">You cannot define a new flavor.</span></span> <span data-ttu-id="aad43-124">Sebbene sia possibile creare un nuovo qualificatore, utilizzare solo le [versioni dei qualificatori](qualifier-flavors.md) esistenti per descrivere il nuovo qualificatore.</span><span class="sxs-lookup"><span data-stu-id="aad43-124">Although you can create a new qualifier, use only existing [Qualifier Flavors](qualifier-flavors.md) to describe your new qualifier.</span></span>

<span data-ttu-id="aad43-125">**Per definire le versioni del qualificatore in MOF**</span><span class="sxs-lookup"><span data-stu-id="aad43-125">**To define qualifier flavors in MOF**</span></span>

-   <span data-ttu-id="aad43-126">Dichiarare le versioni che descrivono un qualificatore specificato dopo il nome del qualificatore tra le parentesi quadre del qualificatore.</span><span class="sxs-lookup"><span data-stu-id="aad43-126">Declare the flavors that describe a given qualifier after the qualifier name, between the qualifier brackets.</span></span> <span data-ttu-id="aad43-127">Usare uno spazio vuoto come delimitatore tra più varianti.</span><span class="sxs-lookup"><span data-stu-id="aad43-127">Use white space as the delimiter between multiple flavors.</span></span>

    <span data-ttu-id="aad43-128">Nell'esempio seguente viene illustrato il modello per il fissaggio dei qualificatori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="aad43-128">The following example shows the pattern for attaching predefined qualifiers.</span></span>

    ``` syntax
    [qualifier1 : flavor1 flavor2 flavor3, qualifier2 : flavor1]
    ```

<span data-ttu-id="aad43-129">È possibile aggiungere le versioni del qualificatore a livello di codice solo in C++.</span><span class="sxs-lookup"><span data-stu-id="aad43-129">You can add qualifier flavors programmatically only in C++.</span></span> <span data-ttu-id="aad43-130">Questa operazione non è disponibile nell' [API di scripting per WMI](scripting-api-for-wmi.md), sebbene sia possibile aggiungere un nuovo qualificatore chiamando [**dell'SWbemQualifierSet. Add**](swbemqualifierset-add.md).</span><span class="sxs-lookup"><span data-stu-id="aad43-130">This operation is not available in the [Scripting API for WMI](scripting-api-for-wmi.md), although you can add a new qualifier by calling [**SWbemQualifierSet.Add**](swbemqualifierset-add.md).</span></span>

<span data-ttu-id="aad43-131">**Per assegnare una versione con C++**</span><span class="sxs-lookup"><span data-stu-id="aad43-131">**To assign a flavor using C++**</span></span>

-   <span data-ttu-id="aad43-132">Chiamare il metodo [**IWbemQualifierSet::P UT**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) con il parametro *lFlavor* impostato su una delle costanti definite per il metodo.</span><span class="sxs-lookup"><span data-stu-id="aad43-132">Call the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method with the *lFlavor* parameter set to one of the constants defined for the method.</span></span>

 

 



