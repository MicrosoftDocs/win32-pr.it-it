---
description: Ogni effetto conforme a DXSAS deve definire come minimo un singolo parametro di effetto globale con la semantica globale.
ms.assetid: 2112db8d-6a11-451d-a9d2-ac1b3cb2da95
title: Parametro globale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647ef789e37cd7c8d6cd2fe554f1f8becbfd5e92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304098"
---
# <a name="global-parameter"></a><span data-ttu-id="037e8-103">Parametro globale</span><span class="sxs-lookup"><span data-stu-id="037e8-103">Global Parameter</span></span>

<span data-ttu-id="037e8-104">Ogni effetto conforme a DXSAS deve definire come minimo un singolo parametro di effetto globale con la semantica globale.</span><span class="sxs-lookup"><span data-stu-id="037e8-104">Each DXSAS compliant effect must define, as a minimum, a single global effect parameter with the global semantic.</span></span> <span data-ttu-id="037e8-105">Il parametro Global può inoltre utilizzare una o più annotazioni facoltative.</span><span class="sxs-lookup"><span data-stu-id="037e8-105">The global parameter can also use one or more optional annotations.</span></span> <span data-ttu-id="037e8-106">La sintassi è la seguente:</span><span class="sxs-lookup"><span data-stu-id="037e8-106">The syntax is as follows:</span></span>


```
int VariableName : SasGlobal
<
    SasVersion 
    [OptionalAnnotations]
>;
```



<span data-ttu-id="037e8-107">dove:</span><span class="sxs-lookup"><span data-stu-id="037e8-107">where:</span></span>

-   <span data-ttu-id="037e8-108">VariableName è un nome di variabile di stringa di testo ASCII specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="037e8-108">VariableName is a user-specified, ASCII text string variable name.</span></span>
-   <span data-ttu-id="037e8-109">SasGlobal è la parola chiave semantica che identifica questo parametro come parametro DXSAS globale.</span><span class="sxs-lookup"><span data-stu-id="037e8-109">SasGlobal is the semantic keyword that identifies this parameter as the global DXSAS parameter.</span></span>
-   <span data-ttu-id="037e8-110">SasVersion è l'unica annotazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="037e8-110">SasVersion is the only required annotation.</span></span>
-   <span data-ttu-id="037e8-111">OptionalAnnotations può includere gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="037e8-111">OptionalAnnotations can include the following:</span></span>
    -   [<span data-ttu-id="037e8-112">SasEffectAuthor</span><span class="sxs-lookup"><span data-stu-id="037e8-112">SasEffectAuthor</span></span>](#saseffectauthor)
    -   [<span data-ttu-id="037e8-113">SasEffectAuthoringSoftware</span><span class="sxs-lookup"><span data-stu-id="037e8-113">SasEffectAuthoringSoftware</span></span>](#saseffectauthoringsoftware)
    -   [<span data-ttu-id="037e8-114">SasEffectCategory</span><span class="sxs-lookup"><span data-stu-id="037e8-114">SasEffectCategory</span></span>](#saseffectcategory)
    -   [<span data-ttu-id="037e8-115">SasEffectCompany</span><span class="sxs-lookup"><span data-stu-id="037e8-115">SasEffectCompany</span></span>](#saseffectcompany)
    -   [<span data-ttu-id="037e8-116">SasEffectDescription</span><span class="sxs-lookup"><span data-stu-id="037e8-116">SasEffectDescription</span></span>](#saseffectdescription)
    -   [<span data-ttu-id="037e8-117">SasEffectHelp</span><span class="sxs-lookup"><span data-stu-id="037e8-117">SasEffectHelp</span></span>](#saseffecthelp)
    -   [<span data-ttu-id="037e8-118">SasEffectRevision</span><span class="sxs-lookup"><span data-stu-id="037e8-118">SasEffectRevision</span></span>](#saseffectrevision)

## <a name="sasversion"></a><span data-ttu-id="037e8-119">SasVersion</span><span class="sxs-lookup"><span data-stu-id="037e8-119">SasVersion</span></span>

<span data-ttu-id="037e8-120">L'unica annotazione richiesta è SasVersion.</span><span class="sxs-lookup"><span data-stu-id="037e8-120">The only required annotation is SasVersion.</span></span> <span data-ttu-id="037e8-121">Viene dichiarata come segue:</span><span class="sxs-lookup"><span data-stu-id="037e8-121">It is declared like this:</span></span>


```
int3 SasVersion = { major, minor, revision };
```



<span data-ttu-id="037e8-122">dove:</span><span class="sxs-lookup"><span data-stu-id="037e8-122">where:</span></span>

-   <span data-ttu-id="037e8-123">Major indica la versione principale di DXSAS.</span><span class="sxs-lookup"><span data-stu-id="037e8-123">major indicates the DXSAS major release.</span></span> <span data-ttu-id="037e8-124">Le versioni principali di DXSAS possono contenere modifiche di sweep al set di semantiche e annotazioni definite.</span><span class="sxs-lookup"><span data-stu-id="037e8-124">Major releases of DXSAS can contain sweeping changes to the set of semantics and annotations defined.</span></span> <span data-ttu-id="037e8-125">La semantica e le annotazioni possono essere aggiunte e rimosse e, in generale, la compatibilità con le versioni precedenti non è garantita.</span><span class="sxs-lookup"><span data-stu-id="037e8-125">Semantics and annotations can be added and removed and, in general, backward compatibility with previous releases is not guaranteed.</span></span>
-   <span data-ttu-id="037e8-126">minor indica la versione secondaria di SAS.</span><span class="sxs-lookup"><span data-stu-id="037e8-126">minor indicates the SAS minor release.</span></span> <span data-ttu-id="037e8-127">Le versioni secondarie di DXSAS possono includere l'aggiunta di nuove semantiche o annotazioni.</span><span class="sxs-lookup"><span data-stu-id="037e8-127">Minor releases of DXSAS can include the addition of new semantics or annotations.</span></span> <span data-ttu-id="037e8-128">Inoltre, la semantica e le annotazioni possono essere contrassegnate come deprecate nello standard DXSAS.</span><span class="sxs-lookup"><span data-stu-id="037e8-128">Additionally, semantics and annotations may be marked as deprecated in the DXSAS standard.</span></span> <span data-ttu-id="037e8-129">La semantica deprecata e le annotazioni devono essere comunque supportate dalle applicazioni host, ma possono generare un avviso di diagnostica quando viene utilizzata una semantica o un'annotazione.</span><span class="sxs-lookup"><span data-stu-id="037e8-129">Deprecated semantics and annotations must still be supported by host applications but can emit a warning diagnostic when such a semantic or annotation is used.</span></span> <span data-ttu-id="037e8-130">Le versioni secondarie sono compatibili con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="037e8-130">Minor releases are backward compatible with previous releases.</span></span>
-   <span data-ttu-id="037e8-131">Revisione indica la revisione DXSAS.</span><span class="sxs-lookup"><span data-stu-id="037e8-131">revision indicates the DXSAS revision.</span></span> <span data-ttu-id="037e8-132">Le revisioni di DXSAS esistono solo come mezzo per correggere i bug, rimuovere l'ambiguità e perfezionare lo standard.</span><span class="sxs-lookup"><span data-stu-id="037e8-132">Revisions of DXSAS exist only as a means to fix bugs, remove ambiguity, and refine the standard.</span></span> <span data-ttu-id="037e8-133">Le revisioni dello standard sono compatibili con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="037e8-133">Revisions to the standard are backward compatible with previous releases.</span></span>

<span data-ttu-id="037e8-134">La versione corrente è 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="037e8-134">The current version is 1.0.0.</span></span> <span data-ttu-id="037e8-135">Non esiste alcun valore predefinito per questa annotazione.</span><span class="sxs-lookup"><span data-stu-id="037e8-135">There is no default value for this annotation.</span></span>

## <a name="saseffectauthor"></a><span data-ttu-id="037e8-136">SasEffectAuthor</span><span class="sxs-lookup"><span data-stu-id="037e8-136">SasEffectAuthor</span></span>

<span data-ttu-id="037e8-137">Viene dichiarata la persona che ha creato l'effetto.</span><span class="sxs-lookup"><span data-stu-id="037e8-137">This declares the person who created the effect.</span></span> <span data-ttu-id="037e8-138">Viene dichiarata come segue:</span><span class="sxs-lookup"><span data-stu-id="037e8-138">It is declared like this:</span></span>


```
string SasEffectAuthor = "value";
```



<span data-ttu-id="037e8-139">dove value è una stringa che identifica l'autore dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="037e8-139">where value is a string that identifies the effect author.</span></span> <span data-ttu-id="037e8-140">Il valore predefinito è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="037e8-140">The default is an empty string.</span></span>

## <a name="saseffectauthoringsoftware"></a><span data-ttu-id="037e8-141">SasEffectAuthoringSoftware</span><span class="sxs-lookup"><span data-stu-id="037e8-141">SasEffectAuthoringSoftware</span></span>

<span data-ttu-id="037e8-142">Questo dichiara il software su cui è stato creato l'effetto.</span><span class="sxs-lookup"><span data-stu-id="037e8-142">This declares the software that the effect was authored on.</span></span> <span data-ttu-id="037e8-143">Viene dichiarata come segue:</span><span class="sxs-lookup"><span data-stu-id="037e8-143">It is declared like this:</span></span>


```
string SasEffectAuthoringSoftware = "value";
```



<span data-ttu-id="037e8-144">dove value è una stringa che identifica il software di creazione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="037e8-144">where value is a string that identifies the effect authoring software.</span></span> <span data-ttu-id="037e8-145">Il valore predefinito è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="037e8-145">The default is an empty string.</span></span>

## <a name="saseffectcategory"></a><span data-ttu-id="037e8-146">SasEffectCategory</span><span class="sxs-lookup"><span data-stu-id="037e8-146">SasEffectCategory</span></span>

<span data-ttu-id="037e8-147">Viene dichiarata la categoria Effect.</span><span class="sxs-lookup"><span data-stu-id="037e8-147">This declares the effect category.</span></span> <span data-ttu-id="037e8-148">Viene dichiarata come segue:</span><span class="sxs-lookup"><span data-stu-id="037e8-148">It is declared like this:</span></span>


```
string SasEffectCategory = "value";
```



<span data-ttu-id="037e8-149">dove value è una stringa che identifica la categoria dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="037e8-149">where value is a string that identifies the effect category.</span></span> <span data-ttu-id="037e8-150">Il valore predefinito è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="037e8-150">The default is an empty string.</span></span> <span data-ttu-id="037e8-151">La categoria viene espressa tramite un valore simile al percorso usando la barra come delimitatore.</span><span class="sxs-lookup"><span data-stu-id="037e8-151">The category is expressed via a path-like value using the forward slash as a delimiter.</span></span> <span data-ttu-id="037e8-152">Gli effetti possono appartenere solo a una categoria poiché non esiste alcuna sintassi per esprimere l'inclusione in più percorsi all'interno di un singolo valore SasEffectCategory.</span><span class="sxs-lookup"><span data-stu-id="037e8-152">Effects can only belong to one category as there is no syntax for expressing inclusion in multiple paths within a single SasEffectCategory value.</span></span> <span data-ttu-id="037e8-153">Il valore di questa annotazione non viene considerato come distinzione tra maiuscole e minuscole dall'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="037e8-153">The value of this annotation is not treated as case-sensitive by the host application.</span></span>

## <a name="saseffectcompany"></a><span data-ttu-id="037e8-154">SasEffectCompany</span><span class="sxs-lookup"><span data-stu-id="037e8-154">SasEffectCompany</span></span>

<span data-ttu-id="037e8-155">Viene dichiarata la società che ha creato l'effetto.</span><span class="sxs-lookup"><span data-stu-id="037e8-155">This declares the company that created the effect.</span></span> <span data-ttu-id="037e8-156">Viene dichiarata come segue:</span><span class="sxs-lookup"><span data-stu-id="037e8-156">It is declared like this:</span></span>


```
string SasEffectCompany = "value";
```



<span data-ttu-id="037e8-157">dove value è una stringa che identifica il nome della società che possiede l'effetto.</span><span class="sxs-lookup"><span data-stu-id="037e8-157">where value is a string that identifies the name of the company that owns the effect.</span></span> <span data-ttu-id="037e8-158">Il valore predefinito è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="037e8-158">The default is an empty string.</span></span>

## <a name="saseffectdescription"></a><span data-ttu-id="037e8-159">SasEffectDescription</span><span class="sxs-lookup"><span data-stu-id="037e8-159">SasEffectDescription</span></span>

<span data-ttu-id="037e8-160">In questo articolo viene descritto l'effetto.</span><span class="sxs-lookup"><span data-stu-id="037e8-160">This describes the effect.</span></span> <span data-ttu-id="037e8-161">Viene dichiarata come segue:</span><span class="sxs-lookup"><span data-stu-id="037e8-161">It is declared like this:</span></span>


```
string SasEffectDescription = "value";
```



<span data-ttu-id="037e8-162">dove value è una stringa che descrive l'effetto.</span><span class="sxs-lookup"><span data-stu-id="037e8-162">where value is a string that describes the effect.</span></span> <span data-ttu-id="037e8-163">Il valore predefinito è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="037e8-163">The default is an empty string.</span></span>

## <a name="saseffecthelp"></a><span data-ttu-id="037e8-164">SasEffectHelp</span><span class="sxs-lookup"><span data-stu-id="037e8-164">SasEffectHelp</span></span>

<span data-ttu-id="037e8-165">Si tratta di una stringa della guida che può essere visualizzata all'utente ogni volta che è richiesta la guida sull'effetto associato.</span><span class="sxs-lookup"><span data-stu-id="037e8-165">This is a help string that can be displayed to the user whenever help on the associated effect is requested.</span></span> <span data-ttu-id="037e8-166">Viene dichiarata come segue:</span><span class="sxs-lookup"><span data-stu-id="037e8-166">It is declared like this:</span></span>


```
string SasEffectHelp = "value";
```



<span data-ttu-id="037e8-167">dove value è una stringa che può essere visualizzata se l'utente richiede la guida.</span><span class="sxs-lookup"><span data-stu-id="037e8-167">where value is a string that can be displayed if the user requests help.</span></span> <span data-ttu-id="037e8-168">Il valore predefinito è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="037e8-168">The default is an empty string.</span></span>

## <a name="saseffectrevision"></a><span data-ttu-id="037e8-169">SasEffectRevision</span><span class="sxs-lookup"><span data-stu-id="037e8-169">SasEffectRevision</span></span>

<span data-ttu-id="037e8-170">Questa annotazione consente agli strumenti e agli utenti di registrare il numero di revisione del file degli effetti associati.</span><span class="sxs-lookup"><span data-stu-id="037e8-170">This annotation allows tools and users to record the revision number of the associated effect file.</span></span> <span data-ttu-id="037e8-171">Ad esempio, gli utenti possono inserire parole chiave appropriate nel valore di questa annotazione per richiamare la sostituzione delle parole chiave nel software di controllo delle revisioni preferito.</span><span class="sxs-lookup"><span data-stu-id="037e8-171">For example, users could insert appropriate keywords in the value of this annotation to invoke keyword substitution in their favorite revision control software.</span></span> <span data-ttu-id="037e8-172">Viene dichiarata come segue:</span><span class="sxs-lookup"><span data-stu-id="037e8-172">It is declared like this:</span></span>


```
string SasEffectRevision = "value";
```



<span data-ttu-id="037e8-173">dove value è una stringa che identifica la revisione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="037e8-173">where value is a string that identifies the effect revision.</span></span> <span data-ttu-id="037e8-174">Il valore predefinito è una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="037e8-174">The default is an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="037e8-175">Esempio</span><span class="sxs-lookup"><span data-stu-id="037e8-175">Examples</span></span>

<span data-ttu-id="037e8-176">Di seguito è riportato un esempio che usa solo la singola annotazione obbligatoria:</span><span class="sxs-lookup"><span data-stu-id="037e8-176">Here is an example that uses only the single, required annotation:</span></span>


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
>;
```



<span data-ttu-id="037e8-177">Di seguito è riportato un esempio che usa l'annotazione richiesta e diverse Annotazioni facoltative:</span><span class="sxs-lookup"><span data-stu-id="037e8-177">Here is an example that uses the required annotation and several optional annotations:</span></span>


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
  string SasEffectAuthor = "Mike's Shader";
  string SasEffectAuthoringSoftware = "fxe 2.5.4";
  string SasEffectCategory = "/surface/procedural/wood";
  string SasEffectCompany = "Microsoft Corporation";
  string SasEffectDescription = "Renders an irridescent surface.";
  string SasEffectHelp = "For more information, see https://somelocation/skin.htm";    
  string SasEffectRevision = "$Revision$";  
>;
```



## <a name="related-topics"></a><span data-ttu-id="037e8-178">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="037e8-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="037e8-179">Informazioni di riferimento sulla semantica e le annotazioni standard DirectX</span><span class="sxs-lookup"><span data-stu-id="037e8-179">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



