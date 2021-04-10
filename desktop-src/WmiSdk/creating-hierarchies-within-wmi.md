---
description: Lo spazio dei nomi WMI è un oggetto di programmazione che definisce l'ambito per un set di classi e istanze. Le classi del provider WMI devono essere definite all'interno di uno spazio dei nomi.
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: Creazione di gerarchie all'interno di WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5743c8da8c40fc0419a96a8ec9c65e7e112573a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226954"
---
# <a name="creating-hierarchies-within-wmi"></a><span data-ttu-id="f1fad-104">Creazione di gerarchie all'interno di WMI</span><span class="sxs-lookup"><span data-stu-id="f1fad-104">Creating Hierarchies Within WMI</span></span>

<span data-ttu-id="f1fad-105">[*Lo spazio dei nomi WMI*](gloss-n.md) è un oggetto di programmazione che definisce l'ambito per un set di classi e istanze.</span><span class="sxs-lookup"><span data-stu-id="f1fad-105">[*WMI namespace*](gloss-n.md) is a programming object that defines the scope for a set of classes and instances.</span></span> <span data-ttu-id="f1fad-106">Le classi del provider WMI devono essere definite all'interno di uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f1fad-106">WMI provider classes must be defined inside a namespace.</span></span>

<span data-ttu-id="f1fad-107">Gli spazi dei nomi descrivono diversi ambienti gestiti, ad esempio l'ambiente SMS.</span><span class="sxs-lookup"><span data-stu-id="f1fad-107">Namespaces describe different managed environments, such as the SMS environment.</span></span> <span data-ttu-id="f1fad-108">Poiché le classi e le istanze di uno schema definiscono i componenti di un ambiente gestito, per ogni nuovo schema è necessario un nuovo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f1fad-108">Because the classes and instances of a schema define the components of a managed environment, each new schema requires a new namespace.</span></span> <span data-ttu-id="f1fad-109">Lo spazio dei nomi radice cimv2, ad esempio, \\ contiene le classi e le istanze definite nello schema Win32, nonché le classi del Common Information Model padre (CIM) da cui lo schema Win32 eredita.</span><span class="sxs-lookup"><span data-stu-id="f1fad-109">For example, the root\\cimv2 namespace contains the classes and instances defined in the Win32 schema as well as the parent Common Information Model (CIM) classes from which the Win32 schema inherits.</span></span> <span data-ttu-id="f1fad-110">Le classi CIM sono definite da Distributed Management Task Force ([DMTF](https://www.dmtf.org/home)).</span><span class="sxs-lookup"><span data-stu-id="f1fad-110">CIM classes are defined by the Distributed Management Task Force ([DMTF](https://www.dmtf.org/home)).</span></span>

> [!Note]  
> <span data-ttu-id="f1fad-111">Per assicurarsi che tutte le definizioni delle classi WMI per gli oggetti gestiti vengano ripristinate nel [*repository WMI*](gloss-w.md) se WMI presenta un errore e viene riavviato, usare l'istruzione del preprocessore [**\# pragma autocover**](pragma-autorecover.md) nel file [*Managed Object Format (MOF)*](gloss-m.md) .</span><span class="sxs-lookup"><span data-stu-id="f1fad-111">To ensure that all of your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor instruction in your [*Managed Object Format (MOF)*](gloss-m.md) file.</span></span>

 

<span data-ttu-id="f1fad-112">WMI definisce uno spazio dei nomi come istanza della classe di sistema [**\_ \_ dello spazio dei nomi**](--namespace.md) o qualsiasi classe che deriva dallo **\_ \_ spazio dei nomi**.</span><span class="sxs-lookup"><span data-stu-id="f1fad-112">WMI defines a namespace as an instance of the [**\_\_Namespace**](--namespace.md) system class or any class that derives from **\_\_Namespace**.</span></span> <span data-ttu-id="f1fad-113">La classe di sistema **\_ \_ dello spazio dei nomi** ha una singola proprietà denominata **Name**, che deve essere univoca all'interno dell'ambito dello spazio dei nomi padre.</span><span class="sxs-lookup"><span data-stu-id="f1fad-113">The **\_\_Namespace** system class has a single property called **Name**, which must be unique within the scope of the parent namespace.</span></span> <span data-ttu-id="f1fad-114">La proprietà **Name** deve contenere anche una stringa che inizia con una lettera.</span><span class="sxs-lookup"><span data-stu-id="f1fad-114">The **Name** property must also contain a string that begins with a letter.</span></span> <span data-ttu-id="f1fad-115">Tutti gli altri caratteri nella stringa possono essere lettere, cifre o caratteri di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="f1fad-115">All other characters in the string can be letters, digits, or underscores.</span></span> <span data-ttu-id="f1fad-116">Tutti i caratteri non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f1fad-116">All characters are case-insensitive.</span></span>

<span data-ttu-id="f1fad-117">Oltre a determinare il nome univoco per uno spazio dei nomi figlio, lo spazio dei nomi WMI padre può proteggere le istanze statiche delle classi da modifiche accidentali da parte di altri provider.</span><span class="sxs-lookup"><span data-stu-id="f1fad-117">In addition to determining the unique name for a child namespace, the parent WMI namespace can protect the static instances of your classes from accidental modification by other providers.</span></span> <span data-ttu-id="f1fad-118">Ad esempio, potrebbe risultare utile annidare un nuovo spazio dei nomi in uno spazio dei nomi esistente per un altro provider.</span><span class="sxs-lookup"><span data-stu-id="f1fad-118">For example, you may find it convenient to nest a new namespace under an existing namespace for another provider.</span></span> <span data-ttu-id="f1fad-119">Tuttavia, il provider originale può tentare di aggiornare tutte le istanze della classe in modo che corrispondano a un nuovo schema.</span><span class="sxs-lookup"><span data-stu-id="f1fad-119">However, the original provider may try to update all class instances to match up with a new schema.</span></span> <span data-ttu-id="f1fad-120">In questo modo, il provider originale può eliminare tutti i sottoelementi figlio in uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f1fad-120">In doing so, the original provider may delete all sub-children in a namespace.</span></span> <span data-ttu-id="f1fad-121">Sebbene sia un'azione appropriata per lo spazio dei nomi di destinazione, può influire sulle istanze di classe non correlate in uno spazio dei nomi figlio (ovvero, le classi del provider personalizzate).</span><span class="sxs-lookup"><span data-stu-id="f1fad-121">While this may be an appropriate action for the target namespace, it may affect unrelated class instances in a child namespace (i.e., your own provider classes).</span></span>

<span data-ttu-id="f1fad-122">Pertanto, in genere è consigliabile creare e registrare lo spazio dei nomi come separato dagli spazi dei nomi che non si controllano direttamente.</span><span class="sxs-lookup"><span data-stu-id="f1fad-122">Therefore, it is generally recommended that you create and register your namespace as separate from namespaces that you do not directly control.</span></span> <span data-ttu-id="f1fad-123">Ciò è particolarmente vero se le classi derivano solo da classi CIM generali o da altre classi della società.</span><span class="sxs-lookup"><span data-stu-id="f1fad-123">This is especially true if your classes derive only from general CIM classes or other classes from your company.</span></span> <span data-ttu-id="f1fad-124">Lo spazio dei nomi può trovarsi nello spazio dei nomi **radice** , ad esempio quanto segue:</span><span class="sxs-lookup"><span data-stu-id="f1fad-124">Your namespace can be under the **Root** namespace, such as the following:</span></span>

<span data-ttu-id="f1fad-125">**Radice/MyCompany/prodotto**</span><span class="sxs-lookup"><span data-stu-id="f1fad-125">**Root/myCompany/myProduct**</span></span>

<span data-ttu-id="f1fad-126">Se invece la nuova classe deriva dalla classe di un altro provider, potrebbe essere necessario archiviare la classe in uno spazio dei nomi secondario del provider.</span><span class="sxs-lookup"><span data-stu-id="f1fad-126">In contrast, if your new class derives from the class of another provider, you may need to store your class in a sub-namespace of that provider.</span></span> <span data-ttu-id="f1fad-127">Si noti che questo espone la nuova classe all'eliminazione accidentale da parte del provider originale.</span><span class="sxs-lookup"><span data-stu-id="f1fad-127">Note that this exposes your new class to accidental deletion by the original provider.</span></span>

<span data-ttu-id="f1fad-128">In WMI sono disponibili diversi modi per creare uno spazio dei nomi:</span><span class="sxs-lookup"><span data-stu-id="f1fad-128">WMI provides several different ways to create a namespace:</span></span>

-   [<span data-ttu-id="f1fad-129">Creazione di uno spazio dei nomi figlio con codice MOF</span><span class="sxs-lookup"><span data-stu-id="f1fad-129">Creating a Child Namespace with MOF Code</span></span>](creating-a-child-namespace-with-mof-code.md)
-   [<span data-ttu-id="f1fad-130">Creazione di uno spazio dei nomi di pari livello con codice MOF</span><span class="sxs-lookup"><span data-stu-id="f1fad-130">Creating a Sibling Namespace with MOF Code</span></span>](creating-a-sibling-namespace-with-mof-code.md)
-   [<span data-ttu-id="f1fad-131">Creazione di uno spazio dei nomi con l'API WMI</span><span class="sxs-lookup"><span data-stu-id="f1fad-131">Creating a Namespace with the WMI API</span></span>](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a><span data-ttu-id="f1fad-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1fad-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1fad-133">Progettazione di classi Managed Object Format (MOF)</span><span class="sxs-lookup"><span data-stu-id="f1fad-133">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



