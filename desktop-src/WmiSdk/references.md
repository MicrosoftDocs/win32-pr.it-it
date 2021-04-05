---
description: La parola chiave ref MOF descrive il percorso di un oggetto ed esegue il mapping a un \_ tipo di automazione VT BSTR.
ms.assetid: 9da25435-4ccc-4251-a4be-37239156e320
ms.tgt_platform: multiple
title: Riferimenti (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30722910de761f3d2111a3218cf364f49ccb3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883230"
---
# <a name="references-wmi"></a><span data-ttu-id="c30d1-103">Riferimenti (WMI)</span><span class="sxs-lookup"><span data-stu-id="c30d1-103">References (WMI)</span></span>

<span data-ttu-id="c30d1-104">La parola chiave **ref** MOF descrive il percorso di un oggetto ed esegue il mapping a un \_ tipo di automazione VT BSTR.</span><span class="sxs-lookup"><span data-stu-id="c30d1-104">The MOF **ref** key word describes an object path and maps to a VT\_BSTR Automation type.</span></span> <span data-ttu-id="c30d1-105">Il percorso dell'oggetto può essere un percorso completo di un server e uno spazio dei nomi oppure un percorso relativo di un altro oggetto nello stesso spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="c30d1-105">The object path can be either a full path to a server and namespace, or a relative path to another object in the same namespace.</span></span> <span data-ttu-id="c30d1-106">È possibile utilizzare una parola chiave **ref** per collegare due o più classi.</span><span class="sxs-lookup"><span data-stu-id="c30d1-106">You can use a **ref** key word to link two or more classes together.</span></span> <span data-ttu-id="c30d1-107">WMI supporta due tipi di percorsi degli oggetti, che consentono di definire percorsi generali o specifici all'interno di WMI.</span><span class="sxs-lookup"><span data-stu-id="c30d1-107">WMI supports two types of object paths, which use to define general or specific paths within WMI.</span></span>

<span data-ttu-id="c30d1-108">Lo scopo principale della parola chiave **ref** è quello di ridurre il tempo di trasporto e la codifica tra gli oggetti presenti interamente nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="c30d1-108">The main purpose of the **ref** key word is to reduce transport time and encoding between objects that exist entirely within the WMI repository.</span></span> <span data-ttu-id="c30d1-109">È anche possibile usare la parola chiave **ref** per creare un'associazione tra due classi.</span><span class="sxs-lookup"><span data-stu-id="c30d1-109">You can also use the **ref** key word to create an association between two classes.</span></span> <span data-ttu-id="c30d1-110">Per ulteriori informazioni, vedere [dichiarazione di una classe di associazione](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="c30d1-110">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span> <span data-ttu-id="c30d1-111">Se l'elemento a cui si fa riferimento si trova all'interno dello stesso file MOF, utilizzare un alias per inizializzare il valore **ref** .</span><span class="sxs-lookup"><span data-stu-id="c30d1-111">If the referenced item is located within the same MOF file, use an alias to initialize the **ref** value.</span></span> <span data-ttu-id="c30d1-112">Per ulteriori informazioni, vedere [creazione di un alias](creating-an-alias.md).</span><span class="sxs-lookup"><span data-stu-id="c30d1-112">For more information, see [Creating an Alias](creating-an-alias.md).</span></span>

> [!Note]  
> <span data-ttu-id="c30d1-113">Quando una parola chiave **ref** viene applicata a una proprietà chiave, è possibile distinguere i riferimenti agli oggetti in base al valore della stringa dell'oggetto anziché al valore dereferenziato.</span><span class="sxs-lookup"><span data-stu-id="c30d1-113">When a **ref** key word is applied to a key property, you can distinguish object references by the object string value instead of by the dereferenced value.</span></span>

 

<span data-ttu-id="c30d1-114">MOF supporta il concetto di percorso di un oggetto tipizzato in modo debole e fortemente tipizzato.</span><span class="sxs-lookup"><span data-stu-id="c30d1-114">MOF supports the concept of a weakly typed and strongly typed object path.</span></span> <span data-ttu-id="c30d1-115">Un percorso di oggetto con tipizzazione debole punta a un oggetto di una classe non specificata e usa la parola chiave **ref** con la parola chiave [Object](object.md) .</span><span class="sxs-lookup"><span data-stu-id="c30d1-115">A weakly typed object path points to an object of an unspecified class and uses the **ref** key word with the [OBJECT](object.md) keyword.</span></span> <span data-ttu-id="c30d1-116">Un oggetto fortemente tipizzato punta a un oggetto di una classe specifica e USA **ref** con il nome della classe.</span><span class="sxs-lookup"><span data-stu-id="c30d1-116">A strongly typed object points to an object of a specific class and uses **ref** with the class name.</span></span> <span data-ttu-id="c30d1-117">Nell'esempio seguente viene descritto un riferimento **RefToAnyClass** debolmente tipizzato che può puntare a qualsiasi istanza di classe o classe e un riferimento **RefToClassX** che può puntare solo a una classe o istanza di **classx** :</span><span class="sxs-lookup"><span data-stu-id="c30d1-117">The following example describes a weakly typed **RefToAnyClass** reference that can point to any class or class instance, and a **RefToClassX** reference that can point only to a **ClassX** class or instance:</span></span>

``` syntax
class MyClass
{
    object ref RefToAnyClass;       // Weakly typed
    ClassX ref RefToClassX;         // Strongly typed
};
```

<span data-ttu-id="c30d1-118">Nell'esempio seguente vengono descritte due istanze e un oggetto Association che fanno riferimento alle istanze precedenti:</span><span class="sxs-lookup"><span data-stu-id="c30d1-118">The following example describes two instances and an association object that references the previous instances:</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

Class A{
    [key] string aKey;
};

Class C{
    [key] string cKey;
};

// The following class creates an association 
// between the "A" class and the "C" class
    [Association] Class B{
    [key] A ref aRef;
    [Key, Min(1)] C ref cRef;
};

instance of a
{
    aKey = "This is the key for the A class";
};

instance of c
{
    cKey = "This is the key for the c class";
};
```

 

 



