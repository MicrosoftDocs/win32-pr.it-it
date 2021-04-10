---
description: Diversi consumer, ad esempio il consumer di eventi di script attivo o il consumer di eventi della riga di comando, hanno proprietà di stringa con il qualificatore del modello.
ms.assetid: d734c226-e160-4834-a5e8-62390905dfde
ms.tgt_platform: multiple
title: Utilizzo di modelli di stringa standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc95f4b2b9b9f22e993d1de9cc8b35915918643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883510"
---
# <a name="using-standard-string-templates"></a><span data-ttu-id="054b9-103">Utilizzo di modelli di stringa standard</span><span class="sxs-lookup"><span data-stu-id="054b9-103">Using Standard String Templates</span></span>

<span data-ttu-id="054b9-104">Diversi consumer, ad esempio il consumer di eventi di script attivo o il consumer di eventi della riga di comando, hanno proprietà di stringa con il qualificatore del **modello** .</span><span class="sxs-lookup"><span data-stu-id="054b9-104">Several consumers, such as the Active Script Event Consumer or the Command Line Event Consumer, have string properties with the **Template** qualifier.</span></span> <span data-ttu-id="054b9-105">Queste proprietà utilizzano modelli di stringa standard per costruire una stringa configurata in parte dall'istanza del consumer e in parte da un evento.</span><span class="sxs-lookup"><span data-stu-id="054b9-105">These properties use standard string templates to construct a string that is configured in part by the consumer instance and in part by an event.</span></span> <span data-ttu-id="054b9-106">La struttura di un modello di stringa standard è simile alla specifica della variabile di ambiente Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="054b9-106">The structure of a standard string template is similar to the Microsoft Windows environment variable specification.</span></span>

<span data-ttu-id="054b9-107">Nell'elenco seguente vengono illustrati alcuni esempi del linguaggio del modello:</span><span class="sxs-lookup"><span data-stu-id="054b9-107">The following list shows some examples of the template language:</span></span>

-   <span data-ttu-id="054b9-108">La stringa "some text here" produce sempre la stringa "some text here".</span><span class="sxs-lookup"><span data-stu-id="054b9-108">The string "Some text here" always produces the string "Some text here".</span></span>
-   <span data-ttu-id="054b9-109">"% CPUUtilization%" produce sempre il valore della proprietà **CPUUtilization** dell'evento da recapitare.</span><span class="sxs-lookup"><span data-stu-id="054b9-109">"%CPUUtilization%" always produces the value of the **CPUUtilization** property of the event being delivered.</span></span> <span data-ttu-id="054b9-110">Se la proprietà non è una stringa, viene convertita in una stringa. ad esempio, "90" o "TRUE".</span><span class="sxs-lookup"><span data-stu-id="054b9-110">If the property is not a string, it is converted to a string; for example, "90" or "TRUE".</span></span>
-   <span data-ttu-id="054b9-111">"L'utilizzo della CPU da parte del processore è% CPUUtilization% al momento" incorpora il valore della proprietà **CPUUtilization** dell'evento nella stringa, producendo un risultato simile al seguente: "l'utilizzo della CPU del processore è 90 al momento".</span><span class="sxs-lookup"><span data-stu-id="054b9-111">"The CPU utilization of this processor is %CPUUtilization% at this time" embeds the value of the **CPUUtilization** property of the event into the string, producing something like, "The CPU utilization of this processor is 90 at this time".</span></span>
-   <span data-ttu-id="054b9-112">"% TargetInstance. CPUUtilization%" Recupera il valore della proprietà **CPUUtilization** nell'istanza incorporata della proprietà **TargetInstance** .</span><span class="sxs-lookup"><span data-stu-id="054b9-112">"%TargetInstance.CPUUtilization%" retrieves the value of the **CPUUtilization** property in the embedded instance of the **TargetInstance** property.</span></span>
-   <span data-ttu-id="054b9-113">"%%" produce un solo segno di%.</span><span class="sxs-lookup"><span data-stu-id="054b9-113">"%%" produces a single % sign.</span></span>
-   <span data-ttu-id="054b9-114">Se la proprietà da recuperare è una matrice, l'intera matrice viene prodotta nel formato seguente: "(1, 5, 10, 1024)".</span><span class="sxs-lookup"><span data-stu-id="054b9-114">If the property being retrieved is an array, the entire array is produced in the following format: "(1,5,10,1024)".</span></span> <span data-ttu-id="054b9-115">Se nella matrice è presente un solo elemento, le parentesi vengono omesse.</span><span class="sxs-lookup"><span data-stu-id="054b9-115">If there is only one element in the array, the parentheses are omitted.</span></span> <span data-ttu-id="054b9-116">Se nella matrice non sono presenti elementi, viene prodotto "()".</span><span class="sxs-lookup"><span data-stu-id="054b9-116">If there are no elements in the array, "()" is produced.</span></span>
-   <span data-ttu-id="054b9-117">Se una proprietà è un oggetto incorporato, viene prodotta la rappresentazione MOF dell'oggetto (simile al metodo [**IWbemClassObject:: GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) ).</span><span class="sxs-lookup"><span data-stu-id="054b9-117">If a property is an embedded object, the MOF representation of the object is produced (similar to the [**IWbemClassObject::GetObjectText**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getobjecttext) method).</span></span>
-   <span data-ttu-id="054b9-118">Se viene richiesta una proprietà di una matrice incorporata di oggetti, viene considerata come una proprietà con un valore di matrice.</span><span class="sxs-lookup"><span data-stu-id="054b9-118">If a property of an embedded array of objects is requested, it is treated as a property with an array value.</span></span> <span data-ttu-id="054b9-119">Ad esempio:% DriverLetter. TargetInstance .% potrebbe produrre ' ("C:", "D:")' se l'oggetto è una matrice di eventi di modifica dell'istanza incorporata.</span><span class="sxs-lookup"><span data-stu-id="054b9-119">For example: %MyEvents.TargetInstance.DriverLetter% could produce '("C:","D:")' if MyEvents is an array of embedded instance modification events.</span></span>

## <a name="string-literals"></a><span data-ttu-id="054b9-120">Valori letterali stringa</span><span class="sxs-lookup"><span data-stu-id="054b9-120">String Literals</span></span>

<span data-ttu-id="054b9-121">Qualsiasi elemento all'interno di una coppia di virgolette viene considerato un valore letterale stringa e non verrà sostituito.</span><span class="sxs-lookup"><span data-stu-id="054b9-121">Anything inside a pair of quotes is considered a string literal and will not be replaced.</span></span>

<span data-ttu-id="054b9-122">Nell'esempio seguente viene illustrata la stringa visualizzata dal compilatore per "utilizzo CPU% CPUUtilization%".</span><span class="sxs-lookup"><span data-stu-id="054b9-122">The following example shows the string that the compiler sees for "CPU utilization is %CPUUtilization%".</span></span>

``` syntax
CPU utilization is %CPUUtilization%
```

<span data-ttu-id="054b9-123">Questa stringa produce l'output seguente.</span><span class="sxs-lookup"><span data-stu-id="054b9-123">This string produces the following output.</span></span>

``` syntax
CPU utilization is 90
```

<span data-ttu-id="054b9-124">D'altra parte, la stringa "utilizzo CPU è \\ "% CPUUtilization% \\ "" viene visualizzata dal compilatore come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="054b9-124">On the other hand, the string "CPU utilization is \\"%CPUUtilization%\\"" is seen by the compiler as follows.</span></span>

``` syntax
CPU utilization is "%CPUUtilization%"
```

<span data-ttu-id="054b9-125">Questa stringa produce l'output seguente, senza alcuna sostituzione delle variabili.</span><span class="sxs-lookup"><span data-stu-id="054b9-125">This string produces the following output, with no variable substitution.</span></span>

``` syntax
CPU utilization is "%CPUUtilization%"
```

## <a name="related-topics"></a><span data-ttu-id="054b9-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="054b9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="054b9-127">Monitoraggio e risposta agli eventi con consumer standard</span><span class="sxs-lookup"><span data-stu-id="054b9-127">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



