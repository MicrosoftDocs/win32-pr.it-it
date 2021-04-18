---
description: Un alias in WMI è un riferimento simbolico in una classe o in un'istanza di classe situata altrove in un file di Managed Object Format (MOF).
ms.assetid: bf4981dc-3aab-46c5-bf02-48132ccec8c2
ms.tgt_platform: multiple
title: Creazione di un alias WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdd538e113f227eac4980855ea0035e839b92fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310391"
---
# <a name="creating-a-wmi-alias"></a><span data-ttu-id="7c84a-103">Creazione di un alias WMI</span><span class="sxs-lookup"><span data-stu-id="7c84a-103">Creating a WMI Alias</span></span>

<span data-ttu-id="7c84a-104">Un [*alias*](gloss-a.md) in WMI è un riferimento simbolico in una classe o in un'istanza di classe situata altrove in un file di Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="7c84a-104">An [*alias*](gloss-a.md) in WMI is a symbolic reference in either a class or a class instance located elsewhere in a Managed Object Format (MOF) file.</span></span> <span data-ttu-id="7c84a-105">Il compilatore MOF USA alias per stabilire riferimenti tra classi e istanze.</span><span class="sxs-lookup"><span data-stu-id="7c84a-105">The MOF compiler uses aliases to establish references between classes and instances.</span></span> <span data-ttu-id="7c84a-106">Il compilatore risolve gli alias nelle classi a cui fanno riferimento, quindi i nomi di alias non sono disponibili nel codice compilato.</span><span class="sxs-lookup"><span data-stu-id="7c84a-106">The compiler resolves aliases to the classes to which they refer, so alias names are not available in compiled code.</span></span> <span data-ttu-id="7c84a-107">Di conseguenza, le applicazioni client non possono fare riferimento alle classi che usano gli alias.</span><span class="sxs-lookup"><span data-stu-id="7c84a-107">As a result, client applications cannot refer to classes using aliases.</span></span>

> [!Note]  
> <span data-ttu-id="7c84a-108">WMI supporta il riferimento in diretta ma non gli alias circolari.</span><span class="sxs-lookup"><span data-stu-id="7c84a-108">WMI supports forward referencing but not circular aliases.</span></span>

 

<span data-ttu-id="7c84a-109">Un alias ha un ambito solo nel file MOF in cui si dichiara l'alias.</span><span class="sxs-lookup"><span data-stu-id="7c84a-109">An alias has scope only within the MOF file in which you declare the alias.</span></span> <span data-ttu-id="7c84a-110">Pertanto, in genere si usa un alias come collegamento a un percorso di oggetto lungo.</span><span class="sxs-lookup"><span data-stu-id="7c84a-110">Therefore, you typically use an alias as a shortcut to a lengthy object path.</span></span>

<span data-ttu-id="7c84a-111">**Per definire un alias**</span><span class="sxs-lookup"><span data-stu-id="7c84a-111">**To define an alias**</span></span>

1.  <span data-ttu-id="7c84a-112">Aggiungere la frase "As $*aliasname*" alla dichiarazione dell'istanza o della classe.</span><span class="sxs-lookup"><span data-stu-id="7c84a-112">Add the phrase "as $*aliasname*" to the instance or class declaration.</span></span>
2.  <span data-ttu-id="7c84a-113">I nomi di alias seguono le stesse regole dei nomi di istanza e di classe, ad eccezione del fatto che i nomi di alias devono iniziare con un segno di dollaro ($).</span><span class="sxs-lookup"><span data-stu-id="7c84a-113">Alias names follow the same rules as instance and class names, except that alias names must begin with a dollar sign ($).</span></span> <span data-ttu-id="7c84a-114">I caratteri di sottolineatura possono essere visualizzati in un nome di alias che segue il carattere iniziale.</span><span class="sxs-lookup"><span data-stu-id="7c84a-114">Underscores can appear in an alias name following the initial character.</span></span>

<span data-ttu-id="7c84a-115">Nell'esempio di codice seguente viene descritto come utilizzare un alias in una definizione di classe.</span><span class="sxs-lookup"><span data-stu-id="7c84a-115">The following code example describes how to use an alias in a class definition.</span></span>

``` syntax
class MyClass as $MyClassAlias
{
};
instance of MyClass as $MyInstanceAlias
{
};
```

<span data-ttu-id="7c84a-116">Gli esempi di codice seguenti descrivono come usare un alias come riferimento simbolico a un percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="7c84a-116">The following code examples describe how to use an alias as a symbolic reference to an object path.</span></span> <span data-ttu-id="7c84a-117">Questi esempi dichiarano due classi per descrivere un disco: la classe del disco per indicare la lettera di unità e la classe DiskRef per indicare il percorso del disco.</span><span class="sxs-lookup"><span data-stu-id="7c84a-117">These examples declare two classes to describe a disk: the Disk class to indicate the drive letter and the DiskRef class to indicate the disk path.</span></span> <span data-ttu-id="7c84a-118">Per l'istanza della classe disco è definito un alias.</span><span class="sxs-lookup"><span data-stu-id="7c84a-118">An alias is defined for the Disk class instance.</span></span> <span data-ttu-id="7c84a-119">Questo alias viene usato come valore per la proprietà PathToDisk nell'istanza di DiskRef.</span><span class="sxs-lookup"><span data-stu-id="7c84a-119">This alias is used as the value for the PathToDisk property in the DiskRef instance.</span></span>

``` syntax
class Disk {
    [key]  string    DriveLetter;
};

class DiskRef 
{
    [key]  string    MyKey;
    Disk   ref       PathToDisk;
};

instance of Disk as $DiskAlias 
{
    DriveLetter = "c";
};

instance of DiskRef
{
    MyKey      =  "hello";
    PathToDisk = $DiskAlias;
};
```

## <a name="related-topics"></a><span data-ttu-id="7c84a-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7c84a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c84a-121">Creazione di una classe</span><span class="sxs-lookup"><span data-stu-id="7c84a-121">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



