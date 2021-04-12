---
description: Una matrice è un elenco indicizzato di valori di dati con lo stesso tipo di dati a cui è possibile fare riferimento. Oltre alle matrici stringa e numeriche, MOF supporta matrici di oggetti incorporati e riferimenti.
ms.assetid: f63c222f-499d-4776-8901-65cb8b142d2b
ms.tgt_platform: multiple
title: Matrici MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0443f2ef3b3fe8fca398e281de71b0927a4f06f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226476"
---
# <a name="mof-arrays"></a><span data-ttu-id="9cd1b-104">Matrici MOF</span><span class="sxs-lookup"><span data-stu-id="9cd1b-104">MOF Arrays</span></span>

<span data-ttu-id="9cd1b-105">Una matrice è un elenco indicizzato di valori di dati con lo stesso tipo di dati a cui è possibile fare riferimento.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-105">An array is an indexed list of data values that are of the same data type, which you can reference.</span></span> <span data-ttu-id="9cd1b-106">Oltre alle matrici stringa e numeriche, MOF supporta matrici di oggetti incorporati e riferimenti.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-106">In addition to string and numeric arrays, MOF supports arrays of embedded objects and references.</span></span>

<span data-ttu-id="9cd1b-107">Le regole seguenti definiscono una matrice MOF:</span><span class="sxs-lookup"><span data-stu-id="9cd1b-107">The following rules define a MOF array:</span></span>

-   <span data-ttu-id="9cd1b-108">Le parentesi quadre usate dopo l'identificatore della proprietà specificano una matrice in una definizione di classe.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-108">Brackets used after the property identifier specify an array in a class definition.</span></span>

    ``` syntax
    Class ArrayDataSample1
    {
        string strArray1[];
    };
    ```

-   <span data-ttu-id="9cd1b-109">Tutte le matrici devono essere unidimensionali.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-109">All arrays must be one-dimensional.</span></span>
-   <span data-ttu-id="9cd1b-110">Le matrici possono essere senza limiti o avere dimensioni esplicite.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-110">Arrays can be unbounded or have an explicit size.</span></span>

    ``` syntax
    Class MyClass
    {
        sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskArray1[]);
        sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskArray2[32]);
    };
    ```

    <span data-ttu-id="9cd1b-111">WMI implementa matrici delimitate e non vincolate come strutture **SAFEARRAY** , che consentono a WMI di variare le dimensioni della matrice in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-111">WMI implements bounded and unbounded arrays as **SAFEARRAY** structures, which allows WMI to vary array dimensions at run time.</span></span> <span data-ttu-id="9cd1b-112">Quando si dichiara una matrice con una dimensione esplicita, WMI archivia le dimensioni come qualificatore e considera le dimensioni massime suggerite.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-112">When you declare an array with an explicit size, WMI stores the size as a qualifier, and treats the size as the suggested maximum size.</span></span> <span data-ttu-id="9cd1b-113">Tuttavia, WMI può espandere le dimensioni, se necessario.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-113">However, WMI can expand the size if necessary.</span></span> <span data-ttu-id="9cd1b-114">La modifica delle dimensioni esplicite non ha alcun effetto sui dati effettivi.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-114">Changing the explicit size has no effect on the actual data.</span></span>

-   <span data-ttu-id="9cd1b-115">Le matrici vengono inizializzate specificando i valori del tipo appropriato in un elenco delimitato da virgole.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-115">Arrays are initialized by specifying values of the appropriate type in a comma-separated list.</span></span>

    ``` syntax
    Class ArrayDataSample2
    {
        [key] string s;
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
    };
    ```

-   <span data-ttu-id="9cd1b-116">Una matrice di riferimenti viene dichiarata come una matrice di stringhe di percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-116">An array of references is declared as an array of object path strings.</span></span>

    <span data-ttu-id="9cd1b-117">Quando si dichiara una stringa del percorso di un oggetto, non inserire spazi vuoti tra gli elementi del percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-117">When declaring an object path string, do not place white space between the elements of the object path.</span></span> <span data-ttu-id="9cd1b-118">Nell'esempio seguente viene descritto come dichiarare un riferimento al percorso di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-118">The following example describes how to declare an object path reference.</span></span>

    ``` syntax
    Class ClassWithRefArray
        { 
        [key] string s; 
        object ref refArray[]; 
        };

    instance of ClassWithRefArray
        {
        s = 23;
        refArray = {"Disk.Name=\"C:\"", "Disk.Name=\"E:\""};
        };
    ```

-   <span data-ttu-id="9cd1b-119">È possibile usare una matrice come parametro per un metodo, ma non come valore restituito per un parametro di input o di input-output.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-119">You can use an array as a parameter for a method, but not as a return value for an input or input-output parameter.</span></span>
-   <span data-ttu-id="9cd1b-120">Tutti gli elementi di una matrice vengono creati come valori dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-120">All elements in an array are created as values of the same type.</span></span>

    <span data-ttu-id="9cd1b-121">Se gli elementi di una matrice sono del tipo di **oggetto** , è possibile inserire qualsiasi tipo di oggetto nella matrice.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-121">If the elements of an array are of the **object** type, then you can place any kind of object in the array.</span></span> <span data-ttu-id="9cd1b-122">D'altra parte, se si dichiara un tipo specifico di oggetto, WMI consente solo gli oggetti della classe o della sottoclasse nella matrice.</span><span class="sxs-lookup"><span data-stu-id="9cd1b-122">On the other hand, if you declare a specific type of object, then WMI allows only objects of that class or subclass in the array.</span></span> <span data-ttu-id="9cd1b-123">Negli esempi seguenti vengono illustrate le dichiarazioni di matrice che includono l'utilizzo del tipo di **oggetto** .</span><span class="sxs-lookup"><span data-stu-id="9cd1b-123">The following examples show array declarations that includes using the **object** type.</span></span>

    ``` syntax
    Class EmbedClass
    {
        [key] sint32 PropOfClass;
    };

    Class ArrayDataClass
    {
        [key] string s;
        string strArray1[];
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
        EmbedClass objArray[];
    };

    instance of ArrayDataClass
    { 
        s = "keyStuff";
        strArray1 = { "1.2.3.4", "1.2.3.5", "1.2.3.7"};
        strArray2 = 
            {
                "SELECT * FROM RegistryKeyChangeEvent",
                "SELECT * FROM RegistryValueChangeEvent",
                "SELECT * FROM RegistryTreeChangeEvent"
            };
        dwArray  = { 1,2,3,5,6 };
        objArray = {
                       instance of EmbedClass{PropOfClass=3;},
                       instance of EmbedClass{PropOfClass=4;}
                   };
    };
    ```

 

 



