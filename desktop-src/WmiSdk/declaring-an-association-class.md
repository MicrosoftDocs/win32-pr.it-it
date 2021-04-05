---
description: Una classe di associazione è un tipo speciale di classe che definisce una relazione tra due altre classi.
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: Dichiarazione di una classe di associazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ce578ca912290fd026f225799793f89685aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058020"
---
# <a name="declaring-an-association-class"></a><span data-ttu-id="bbf97-103">Dichiarazione di una classe di associazione</span><span class="sxs-lookup"><span data-stu-id="bbf97-103">Declaring an Association Class</span></span>

<span data-ttu-id="bbf97-104">Una classe di associazione è un tipo speciale di classe che definisce una relazione tra due altre classi.</span><span class="sxs-lookup"><span data-stu-id="bbf97-104">An association class is a special type of class that defines a relationship between two other classes.</span></span>

<span data-ttu-id="bbf97-105">Nella procedura seguente viene descritto come creare una classe di associazione utilizzando il codice MOF.</span><span class="sxs-lookup"><span data-stu-id="bbf97-105">The following procedure describes how to create an association class using MOF code.</span></span>

<span data-ttu-id="bbf97-106">**Per creare una classe di associazione usando il codice MOF**</span><span class="sxs-lookup"><span data-stu-id="bbf97-106">**To create an association class using MOF code**</span></span>

1.  <span data-ttu-id="bbf97-107">Assegnare il qualificatore **Association** alla classe.</span><span class="sxs-lookup"><span data-stu-id="bbf97-107">Assign the **Association** qualifier to your class.</span></span>

    <span data-ttu-id="bbf97-108">Sebbene sia possibile creare una classe con riferimenti a oggetti o classi, l'utilizzo del qualificatore di **associazione** non solo rende chiaro che la classe è una classe di associazione, ma, come procedura consigliata, assicura che la classe funzioni completamente come una classe di associazione.</span><span class="sxs-lookup"><span data-stu-id="bbf97-108">Although it is possible to create a class with references to objects or classes, using the **Association** qualifier not only makes it clear that your class is an association class, but, as a best practice, ensures that your class fully functions as an association class.</span></span>

2.  <span data-ttu-id="bbf97-109">Creare due riferimenti all'interno della classe che descrivono le due istanze di oggetti che si desidera associare utilizzando il tipo di **riferimento** .</span><span class="sxs-lookup"><span data-stu-id="bbf97-109">Create two references within the class describing the two object instances you wish to associate together using the **ref** type.</span></span>

    <span data-ttu-id="bbf97-110">I riferimenti associano i due oggetti nell'associazione, contenenti i percorsi degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="bbf97-110">The references bind the two objects in the association by containing paths to the objects.</span></span> <span data-ttu-id="bbf97-111">Sebbene non sia obbligatorio, utilizzare anche le proprietà di riferimento come proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="bbf97-111">Although not required, use the reference properties as key properties as well.</span></span>

    <span data-ttu-id="bbf97-112">Sebbene sia possibile creare riferimenti completi o relativi agli spazi dei nomi, WMI ha solo un supporto limitato per i riferimenti tra più spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="bbf97-112">Although you can create fully qualified or namespace-relative references, WMI has only limited support for cross-namespace references.</span></span> <span data-ttu-id="bbf97-113">In particolare, solo gli oggetti definiti in modo statico possono fare riferimento tra loro tra i limiti dello spazio dei nomi. gli oggetti supportati dinamicamente non possono fare riferimento l'uno all'altro.</span><span class="sxs-lookup"><span data-stu-id="bbf97-113">Specifically, only statically defined objects can reference each other across namespace boundaries; dynamically supported objects cannot reference each other.</span></span>

    <span data-ttu-id="bbf97-114">Se necessario, usare i qualificatori **HasClassRef** e **Classref** in combinazione con il tipo di riferimento dell' **oggetto** per fare riferimento a una classe.</span><span class="sxs-lookup"><span data-stu-id="bbf97-114">If necessary, use the **HasClassRef** and **Classref** qualifiers in conjunction with the **object ref** type to reference a class.</span></span>

    <span data-ttu-id="bbf97-115">WMI supporta la presenza di un punto di riferimento **ref** a un'istanza di e l'altro riferimento all' **oggetto** punta a una classe.</span><span class="sxs-lookup"><span data-stu-id="bbf97-115">WMI supports having one **ref** reference point to an instance, and the other **object** reference point to a class.</span></span> <span data-ttu-id="bbf97-116">In questo caso, la classe Association Descriva un'associazione che associa le istanze alle classi.</span><span class="sxs-lookup"><span data-stu-id="bbf97-116">In this case, your association class would describe an association that binds instances to classes.</span></span>

    <span data-ttu-id="bbf97-117">Nell'esempio di codice seguente viene descritta la sintassi per l'utilizzo di **HasClassRef** e **Classref** con un tipo di **oggetto** .</span><span class="sxs-lookup"><span data-stu-id="bbf97-117">The following code example describes the syntax for using **HasClassRef** and **Classref** with an **object** type.</span></span>

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    <span data-ttu-id="bbf97-118">Nell'esempio precedente, il riferimento **EP1** può puntare alle definizioni di classe per la classe di **endpoint** o la classe **OtherContainer** .</span><span class="sxs-lookup"><span data-stu-id="bbf97-118">In the previous example, the **ep1** reference can point to the class definitions for either the **MyEndpoint** class or the **OtherContainer** class.</span></span> <span data-ttu-id="bbf97-119">Si noti che, sebbene sia necessario digitare debolmente la classe di riferimento, non è possibile digitare debolmente il qualificatore **Classref** ; Questa operazione ridurrebbe notevolmente l'efficienza del motore di query WMI.</span><span class="sxs-lookup"><span data-stu-id="bbf97-119">Note that while you must weakly type the reference class, you cannot weakly type the **Classref** qualifier itself; doing so would severely reduce the efficiency of the WMI query engine.</span></span> <span data-ttu-id="bbf97-120">La tipizzazione debole sta creando un riferimento che può contenere qualsiasi tipo di dati tramite la parola chiave **Object** e il tipo di dati **ref** .</span><span class="sxs-lookup"><span data-stu-id="bbf97-120">Weak typing is creating a reference that can contain any data type by using the **object** keyword and **ref** data type.</span></span> <span data-ttu-id="bbf97-121">Per usare correttamente **HasClassRef**, è necessario impostare le versioni dei qualificatori rilevanti per la propagazione a tutte le istanze e sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="bbf97-121">To successfully use **HasClassRef**, you must set the relevant qualifier flavors to propagate to all instances and subclasses.</span></span>

3.  <span data-ttu-id="bbf97-122">Creare qualsiasi altra proprietà, se necessario.</span><span class="sxs-lookup"><span data-stu-id="bbf97-122">Create any other properties as necessary.</span></span>

    <span data-ttu-id="bbf97-123">Nell'esempio di codice seguente viene illustrato che WMI non supporta attualmente le classi di associazione con meno o più di due proprietà di riferimento.</span><span class="sxs-lookup"><span data-stu-id="bbf97-123">The following code example shows that WMI does not currently support association classes having less or more than two reference properties.</span></span>

    ``` syntax
    [Association : ToInstance] 
    class MyAssocClass
    {
        ClassX ref PathToClassX ;
        ClassY ref PathToClassY ;
    };
    ```

4.  <span data-ttu-id="bbf97-124">Al termine, compilare il codice MOF con il compilatore MOF.</span><span class="sxs-lookup"><span data-stu-id="bbf97-124">When finished, compile your MOF code with the MOF compiler.</span></span>

    <span data-ttu-id="bbf97-125">Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="bbf97-125">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="bbf97-126">L'esempio di codice nel passaggio 3 definisce la classe di associazione **MyAssocClass** .</span><span class="sxs-lookup"><span data-stu-id="bbf97-126">The code example in Step 3 defines the **MyAssocClass** association class.</span></span> <span data-ttu-id="bbf97-127">La classe **MyAssocClass** definisce una relazione tra **classx** e **Classy**.</span><span class="sxs-lookup"><span data-stu-id="bbf97-127">The **MyAssocClass** class defines a relationship between **ClassX** and **ClassY**.</span></span> <span data-ttu-id="bbf97-128">Le proprietà **PathToClassX** e **PathToClassY** contengono percorsi di oggetti per le istanze delle classi da associare.</span><span class="sxs-lookup"><span data-stu-id="bbf97-128">The **PathToClassX** and **PathToClassY** properties contain object paths to the instances of the classes to be associated.</span></span> <span data-ttu-id="bbf97-129">La parola chiave **ToInstance** è uno dei diversi flag di sapore definiti da WMI per fornire informazioni sull'utilizzo di un qualificatore.</span><span class="sxs-lookup"><span data-stu-id="bbf97-129">The keyword **ToInstance** is one of several flavor flags that WMI defines to provide information about the use of a qualifier.</span></span> <span data-ttu-id="bbf97-130">La parola chiave **ToInstance** indica che WMI deve propagare il qualificatore dell' **associazione** a tutte le istanze della classe Association.</span><span class="sxs-lookup"><span data-stu-id="bbf97-130">The **ToInstance** keyword indicates that WMI should propagate the **Association** qualifier to all instances of the association class.</span></span> <span data-ttu-id="bbf97-131">Controllando questo qualificatore di istanza, il software client può determinare che un'istanza appartiene a una classe di associazione, senza dover recuperare la definizione della classe per cercare il qualificatore dell' **associazione** .</span><span class="sxs-lookup"><span data-stu-id="bbf97-131">By checking this instance qualifier, the client software can determine that an instance belongs to an association class, without having to retrieve the class definition to look for the **Association** qualifier.</span></span> <span data-ttu-id="bbf97-132">Per ulteriori informazioni, vedere [Descrizione di un qualificatore con una versione del qualificatore](describing-a-qualifier-with-a-qualifier-flavor.md) e [riferimenti](references.md).</span><span class="sxs-lookup"><span data-stu-id="bbf97-132">For more information, see [Describing a Qualifier With a Qualifier Flavor](describing-a-qualifier-with-a-qualifier-flavor.md) and [References](references.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbf97-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bbf97-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbf97-134">Progettazione di classi Managed Object Format (MOF)</span><span class="sxs-lookup"><span data-stu-id="bbf97-134">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



