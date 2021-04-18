---
description: "Quando si crea un'istanza di con oggetti incorporati, eseguire le attività seguenti:"
ms.assetid: 2abf6197-8b95-4c04-b154-508aa85fe12f
ms.tgt_platform: multiple
title: Creazione di oggetti incorporati
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a76a70fa0e01068622a4f4cdbbbfb6c992b67f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316568"
---
# <a name="creating-embedded-objects"></a><span data-ttu-id="cf143-103">Creazione di oggetti incorporati</span><span class="sxs-lookup"><span data-stu-id="cf143-103">Creating Embedded Objects</span></span>

<span data-ttu-id="cf143-104">Quando si crea un'istanza di con oggetti incorporati, eseguire le attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="cf143-104">When creating an instance with embedded objects, perform the following tasks:</span></span>

-   <span data-ttu-id="cf143-105">È necessario dichiarare un oggetto incorporato come fortemente tipizzato o debolmente tipizzato.</span><span class="sxs-lookup"><span data-stu-id="cf143-105">You must declare an embedded object as strongly typed or weakly typed.</span></span>

    <span data-ttu-id="cf143-106">Un oggetto fortemente tipizzato punta a un oggetto di una classe specifica e usa il nome della classe.</span><span class="sxs-lookup"><span data-stu-id="cf143-106">A strongly typed object points to an object of a specific class and uses the class name.</span></span> <span data-ttu-id="cf143-107">Un oggetto con tipizzazione debole punta a un oggetto di una classe non specificata e utilizza la parola chiave **Object** .</span><span class="sxs-lookup"><span data-stu-id="cf143-107">A weakly typed object points to an object of an unspecified class and uses the **object** keyword.</span></span> <span data-ttu-id="cf143-108">Entrambi gli oggetti sono mappati al tipo **\_ sconosciuto VT** .</span><span class="sxs-lookup"><span data-stu-id="cf143-108">Both objects map to the **VT\_UNKNOWN** type.</span></span>

-   <span data-ttu-id="cf143-109">È possibile utilizzare **null** come valore predefinito di oggetti e percorsi incorporati nelle inizializzazioni e nelle dichiarazioni.</span><span class="sxs-lookup"><span data-stu-id="cf143-109">You can use **NULL** for the default value of embedded objects and paths in initializations and declarations.</span></span>
-   <span data-ttu-id="cf143-110">Quando si incorpora un percorso di oggetto, non inserire spazi vuoti tra gli elementi del percorso incorporato.</span><span class="sxs-lookup"><span data-stu-id="cf143-110">When embedding an object path, do not place white space between the elements of the embedded path.</span></span> <span data-ttu-id="cf143-111">Il percorso dell'oggetto "Class1Index = 3;", ad esempio, non contiene alcuno spazio tra il nome della proprietà "Class1index" e il valore assegnato, ovvero "3".</span><span class="sxs-lookup"><span data-stu-id="cf143-111">For example, the object path "Class1Index=3;" contains no space between the property name "Class1index" and the value being assigned, which is "3".</span></span>

<span data-ttu-id="cf143-112">Nella dichiarazione di classe seguente viene illustrato come dichiarare oggetti incorporati fortemente tipizzati e con tipizzazione debole.</span><span class="sxs-lookup"><span data-stu-id="cf143-112">The following class declaration shows you how to declare strongly typed and weakly typed embedded objects.</span></span>

``` syntax
Class MyClass
{
    EmbedClass    Object1;          // Strongly typed
    object        Object2;          // Weakly typed
};
```

<span data-ttu-id="cf143-113">Negli esempi seguenti viene descritto come dichiarare oggetti incorporati all'interno di una dichiarazione di classe.</span><span class="sxs-lookup"><span data-stu-id="cf143-113">The following examples describe how to declare embedded objects within a class declaration.</span></span>

``` syntax
Class Class1 
{ 
     [key] sint32 Class1Index;
};

Class Class2 
{
    [key] sint32 Class2Index;
    Class1 EmbedObject1 = instance of Class1{Class1Index=3;};
};

Class Class3
{
    [key] sint32 Class3Index;
    Class2 EmbedObject2 = instance of Class2 {Class2Index=4;};
};
```

<span data-ttu-id="cf143-114">Nell'esempio seguente viene descritta l'inizializzazione di una proprietà che è un oggetto fortemente tipizzato e un'altra proprietà che è una matrice di oggetti con tipizzazione debole.</span><span class="sxs-lookup"><span data-stu-id="cf143-114">The following example describes the initialization of one property that is a strongly typed object and another property that is an array of weakly typed objects.</span></span>

``` syntax
Class EmbedClass1
{
    [key] sint32 intval;
};

Class EmbedClass2
{
    [key] string sval;
};

Class ContainerClass
{
    [key] sint32 intval;
    EmbedClass1 SingleObject;
    Object ArrayObject[];
};

Instance of ContainerClass
{
    intval = 33;
    SingleObject = instance of EmbedClass1 {intval=99;};
    ArrayObject = {instance of EmbedClass2 {sval="something";},
                   instance of EmbedClass1 {intval=100;}};
};
```

 

 



