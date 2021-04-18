---
description: ICE65 verifica che la tabella dell'ambiente non contenga valori di prefisso o di Accodamento non validi.
ms.assetid: 95d4e618-9a19-40db-910a-daab105559ae
title: ICE65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b3d2b7bcd844c970ccc7fddf376b27c2ec54f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317132"
---
# <a name="ice65"></a><span data-ttu-id="082c5-103">ICE65</span><span class="sxs-lookup"><span data-stu-id="082c5-103">ICE65</span></span>

<span data-ttu-id="082c5-104">ICE65 verifica che la [tabella dell'ambiente](environment-table.md) non contenga valori di prefisso o di Accodamento non validi.</span><span class="sxs-lookup"><span data-stu-id="082c5-104">ICE65 checks that the [Environment table](environment-table.md) does not have invalid prefix or append values.</span></span>

<span data-ttu-id="082c5-105">La mancata correzione di un avviso o di un errore segnalato da ICE65 in genere causa problemi di installazione, disinstallazione o ripristino della variabile di ambiente.</span><span class="sxs-lookup"><span data-stu-id="082c5-105">Failure to fix a warning or error reported by ICE65 generally leads to problems in install, uninstall, or repair of the environment variable.</span></span> <span data-ttu-id="082c5-106">Ad esempio, è possibile rimuovere solo alcuni valori di una determinata variabile se uno o più valori per tale variabile hanno un separatore finale.</span><span class="sxs-lookup"><span data-stu-id="082c5-106">For example, only some values of a particular variable may be removed if one or more of the values for that variable have a trailing separator.</span></span>

## <a name="result"></a><span data-ttu-id="082c5-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="082c5-107">Result</span></span>

<span data-ttu-id="082c5-108">ICE65 Invia un avviso o un errore se nella tabella dell'ambiente sono presenti valori di prefisso o di Accodamento non validi.</span><span class="sxs-lookup"><span data-stu-id="082c5-108">ICE65 posts a warning or an error if the environment table has invalid prefix or append values.</span></span>

## <a name="example"></a><span data-ttu-id="082c5-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="082c5-109">Example</span></span>

<span data-ttu-id="082c5-110">ICE65 segnala l'errore e l'avviso seguenti per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="082c5-110">ICE65 reports the following error and warning for the example shown.</span></span>

``` syntax
The environment variable 'Var3' has a separator beginning or ending its value.
```

<span data-ttu-id="082c5-111">Il valore null finale alla fine del valore ( \[ ~ \] ) contrassegna questo valore come anteposto a qualsiasi valore esistente.</span><span class="sxs-lookup"><span data-stu-id="082c5-111">The trailing null at the end of the value (\[~\]) marks this value to be prepended to any existing value.</span></span> <span data-ttu-id="082c5-112">Il carattere immediatamente prima del valore null (un punto e virgola) diventa il separatore per questo valore.</span><span class="sxs-lookup"><span data-stu-id="082c5-112">The character immediately before the null (a semicolon) becomes the separator for this value.</span></span> <span data-ttu-id="082c5-113">Questo valore dispone anche di un punto e virgola all'inizio della stringa.</span><span class="sxs-lookup"><span data-stu-id="082c5-113">This value has a semicolon at the beginning of the string as well.</span></span>

<span data-ttu-id="082c5-114">Per correggere l'errore, è sufficiente eliminare il punto e virgola principale.</span><span class="sxs-lookup"><span data-stu-id="082c5-114">To fix this error, simply delete the leading semicolon.</span></span>

``` syntax
WARNING: The environment variable 'Var2' has an alphanumeric separator
```

<span data-ttu-id="082c5-115">Il valore null principale nel valore ( \[ ~ \] ) contrassegna questo valore come accodato a qualsiasi valore esistente.</span><span class="sxs-lookup"><span data-stu-id="082c5-115">The leading null in the value (\[~\]) marks this value to be appended to any existing value.</span></span> <span data-ttu-id="082c5-116">Il carattere immediatamente successivo a null diventa il separatore per questo valore.</span><span class="sxs-lookup"><span data-stu-id="082c5-116">The character immediately after the null becomes the separator for this value.</span></span> <span data-ttu-id="082c5-117">In questo caso, tale carattere è la lettera "e", che si verifica anche al centro della stringa da accodare.</span><span class="sxs-lookup"><span data-stu-id="082c5-117">In this case, that character is the letter "e", which also occurs in the middle of the string to be appended.</span></span> <span data-ttu-id="082c5-118">Questa condizione (con un separatore che corrisponde a un carattere all'interno della stringa da accodare) può causare risultati imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="082c5-118">This condition (having a separator that is the same as a character within the string to be appended) can cause unpredictable results.</span></span>

<span data-ttu-id="082c5-119">La lettera "e", che è una lettera comune, è probabile che sia presente nel valore.</span><span class="sxs-lookup"><span data-stu-id="082c5-119">The letter "e", being a common letter, is likely to be found in the value.</span></span> <span data-ttu-id="082c5-120">Una scelta migliore è ";" o un altro carattere non alfanumerico.</span><span class="sxs-lookup"><span data-stu-id="082c5-120">A better choice would be ";" or some other non-alphanumeric character.</span></span> <span data-ttu-id="082c5-121">(Tuttavia, se il valore è un percorso, ":" e " \\ " e "." sono scelte rischiose).</span><span class="sxs-lookup"><span data-stu-id="082c5-121">(However, if the value is a path, then ":" and "\\" and "." are risky choices.)</span></span>

<span data-ttu-id="082c5-122">Per correggere il problema, usare un carattere separatore diverso.</span><span class="sxs-lookup"><span data-stu-id="082c5-122">To fix this warning, use a different separator character.</span></span>

[<span data-ttu-id="082c5-123">Tabella ambiente</span><span class="sxs-lookup"><span data-stu-id="082c5-123">Environment Table</span></span>](environment-table.md)



| <span data-ttu-id="082c5-124">Componente</span><span class="sxs-lookup"><span data-stu-id="082c5-124">Component</span></span> | <span data-ttu-id="082c5-125">Directory</span><span class="sxs-lookup"><span data-stu-id="082c5-125">Directory</span></span> | <span data-ttu-id="082c5-126">Attributi</span><span class="sxs-lookup"><span data-stu-id="082c5-126">Attributes</span></span>         | <span data-ttu-id="082c5-127">KeyPath</span><span class="sxs-lookup"><span data-stu-id="082c5-127">KeyPath</span></span>       |
|-----------|-----------|--------------------|---------------|
| <span data-ttu-id="082c5-128">Var1</span><span class="sxs-lookup"><span data-stu-id="082c5-128">Var1</span></span>      | <span data-ttu-id="082c5-129">TestVar</span><span class="sxs-lookup"><span data-stu-id="082c5-129">TestVar</span></span>   | <span data-ttu-id="082c5-130">\[~\]; AppendThis</span><span class="sxs-lookup"><span data-stu-id="082c5-130">\[~\];AppendThis</span></span>   | <span data-ttu-id="082c5-131">TestComponent</span><span class="sxs-lookup"><span data-stu-id="082c5-131">TestComponent</span></span> |
| <span data-ttu-id="082c5-132">Var2</span><span class="sxs-lookup"><span data-stu-id="082c5-132">Var2</span></span>      | <span data-ttu-id="082c5-133">TestVar</span><span class="sxs-lookup"><span data-stu-id="082c5-133">TestVar</span></span>   | <span data-ttu-id="082c5-134">\[~\]eAppendThis</span><span class="sxs-lookup"><span data-stu-id="082c5-134">\[~\]eAppendThis</span></span>   | <span data-ttu-id="082c5-135">TestComponent</span><span class="sxs-lookup"><span data-stu-id="082c5-135">TestComponent</span></span> |
| <span data-ttu-id="082c5-136">Var3</span><span class="sxs-lookup"><span data-stu-id="082c5-136">Var3</span></span>      | <span data-ttu-id="082c5-137">TestVar</span><span class="sxs-lookup"><span data-stu-id="082c5-137">TestVar</span></span>   | <span data-ttu-id="082c5-138">; PrependThis;\[~\]</span><span class="sxs-lookup"><span data-stu-id="082c5-138">;PrependThis;\[~\]</span></span> | <span data-ttu-id="082c5-139">TestComponent</span><span class="sxs-lookup"><span data-stu-id="082c5-139">TestComponent</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="082c5-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="082c5-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="082c5-141">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="082c5-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



