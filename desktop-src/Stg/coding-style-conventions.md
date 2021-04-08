---
title: Convenzioni di stile di codifica
description: Le convenzioni di stile del codice vengono usate in questa serie di esempi per facilitare la chiarezza e la coerenza.
ms.assetid: d5e81a52-79f6-4561-891c-05fee125a1b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28e65e19d69f060a5f85d86976c4bd3694f7611
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734962"
---
# <a name="coding-style-conventions"></a><span data-ttu-id="442eb-103">Convenzioni di stile di codifica</span><span class="sxs-lookup"><span data-stu-id="442eb-103">Coding Style Conventions</span></span>

<span data-ttu-id="442eb-104">Le convenzioni di stile del codice vengono usate in questa serie di esempi per facilitare la chiarezza e la coerenza.</span><span class="sxs-lookup"><span data-stu-id="442eb-104">Coding style conventions are used in this sample series to aid clarity and consistency.</span></span> <span data-ttu-id="442eb-105">Vengono utilizzate le convenzioni di notazione "ungherese".</span><span class="sxs-lookup"><span data-stu-id="442eb-105">The "Hungarian" notation conventions are used.</span></span> <span data-ttu-id="442eb-106">Questi sono diventati una procedura di codifica comune nella programmazione Win32.</span><span class="sxs-lookup"><span data-stu-id="442eb-106">These have become a common coding practice in Win32 programming.</span></span> <span data-ttu-id="442eb-107">Includono la notazione del prefisso variabile che assegna ai nomi delle variabili un suggerimento del tipo della variabile.</span><span class="sxs-lookup"><span data-stu-id="442eb-107">They include variable prefix notations that give to variable names a suggestion of the type of the variable.</span></span>

<span data-ttu-id="442eb-108">Nella tabella seguente sono elencati i prefissi comuni.</span><span class="sxs-lookup"><span data-stu-id="442eb-108">The following table lists common prefixes.</span></span>



| <span data-ttu-id="442eb-109">Prefisso</span><span class="sxs-lookup"><span data-stu-id="442eb-109">Prefix</span></span> | <span data-ttu-id="442eb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="442eb-110">Description</span></span>                         |
|--------|-------------------------------------|
| <span data-ttu-id="442eb-111">a</span><span class="sxs-lookup"><span data-stu-id="442eb-111">a</span></span>      | <span data-ttu-id="442eb-112">Array</span><span class="sxs-lookup"><span data-stu-id="442eb-112">Array</span></span>                               |
| <span data-ttu-id="442eb-113">b</span><span class="sxs-lookup"><span data-stu-id="442eb-113">b</span></span>      | <span data-ttu-id="442eb-114">BOOL (int)</span><span class="sxs-lookup"><span data-stu-id="442eb-114">BOOL (int)</span></span>                          |
| <span data-ttu-id="442eb-115">c</span><span class="sxs-lookup"><span data-stu-id="442eb-115">c</span></span>      | <span data-ttu-id="442eb-116">Char</span><span class="sxs-lookup"><span data-stu-id="442eb-116">Char</span></span>                                |
| <span data-ttu-id="442eb-117">CB</span><span class="sxs-lookup"><span data-stu-id="442eb-117">cb</span></span>     | <span data-ttu-id="442eb-118">Conteggio di byte</span><span class="sxs-lookup"><span data-stu-id="442eb-118">Count of bytes</span></span>                      |
| <span data-ttu-id="442eb-119">CR</span><span class="sxs-lookup"><span data-stu-id="442eb-119">cr</span></span>     | <span data-ttu-id="442eb-120">Valore riferimento colore</span><span class="sxs-lookup"><span data-stu-id="442eb-120">Color reference value</span></span>               |
| <span data-ttu-id="442eb-121">CX</span><span class="sxs-lookup"><span data-stu-id="442eb-121">cx</span></span>     | <span data-ttu-id="442eb-122">Conteggio di x (Short)</span><span class="sxs-lookup"><span data-stu-id="442eb-122">Count of x (short)</span></span>                  |
| <span data-ttu-id="442eb-123">dw</span><span class="sxs-lookup"><span data-stu-id="442eb-123">dw</span></span>     | <span data-ttu-id="442eb-124">DWORD (unsigned long)</span><span class="sxs-lookup"><span data-stu-id="442eb-124">DWORD (unsigned long)</span></span>               |
| <span data-ttu-id="442eb-125">f</span><span class="sxs-lookup"><span data-stu-id="442eb-125">f</span></span>      | <span data-ttu-id="442eb-126">Flag (in genere più valori di bit)</span><span class="sxs-lookup"><span data-stu-id="442eb-126">Flags (usually multiple bit values)</span></span> |
| <span data-ttu-id="442eb-127">fn</span><span class="sxs-lookup"><span data-stu-id="442eb-127">fn</span></span>     | <span data-ttu-id="442eb-128">Funzione</span><span class="sxs-lookup"><span data-stu-id="442eb-128">Function</span></span>                            |
| <span data-ttu-id="442eb-129">g\_</span><span class="sxs-lookup"><span data-stu-id="442eb-129">g\_</span></span>    | <span data-ttu-id="442eb-130">Globale</span><span class="sxs-lookup"><span data-stu-id="442eb-130">Global</span></span>                              |
| <span data-ttu-id="442eb-131">h</span><span class="sxs-lookup"><span data-stu-id="442eb-131">h</span></span>      | <span data-ttu-id="442eb-132">Handle</span><span class="sxs-lookup"><span data-stu-id="442eb-132">Handle</span></span>                              |
| <span data-ttu-id="442eb-133">i</span><span class="sxs-lookup"><span data-stu-id="442eb-133">i</span></span>      | <span data-ttu-id="442eb-134">Integer</span><span class="sxs-lookup"><span data-stu-id="442eb-134">Integer</span></span>                             |
| <span data-ttu-id="442eb-135">l</span><span class="sxs-lookup"><span data-stu-id="442eb-135">l</span></span>      | <span data-ttu-id="442eb-136">long</span><span class="sxs-lookup"><span data-stu-id="442eb-136">Long</span></span>                                |
| <span data-ttu-id="442eb-137">lp</span><span class="sxs-lookup"><span data-stu-id="442eb-137">lp</span></span>     | <span data-ttu-id="442eb-138">Puntatore lungo</span><span class="sxs-lookup"><span data-stu-id="442eb-138">Long pointer</span></span>                        |
| <span data-ttu-id="442eb-139">m\_</span><span class="sxs-lookup"><span data-stu-id="442eb-139">m\_</span></span>    | <span data-ttu-id="442eb-140">Membro dati di una classe</span><span class="sxs-lookup"><span data-stu-id="442eb-140">Data member of a class</span></span>              |
| <span data-ttu-id="442eb-141">n</span><span class="sxs-lookup"><span data-stu-id="442eb-141">n</span></span>      | <span data-ttu-id="442eb-142">Int breve</span><span class="sxs-lookup"><span data-stu-id="442eb-142">Short int</span></span>                           |
| <span data-ttu-id="442eb-143">p</span><span class="sxs-lookup"><span data-stu-id="442eb-143">p</span></span>      | <span data-ttu-id="442eb-144">Puntatore</span><span class="sxs-lookup"><span data-stu-id="442eb-144">Pointer</span></span>                             |
| <span data-ttu-id="442eb-145">s</span><span class="sxs-lookup"><span data-stu-id="442eb-145">s</span></span>      | <span data-ttu-id="442eb-146">string</span><span class="sxs-lookup"><span data-stu-id="442eb-146">String</span></span>                              |
| <span data-ttu-id="442eb-147">sz</span><span class="sxs-lookup"><span data-stu-id="442eb-147">sz</span></span>     | <span data-ttu-id="442eb-148">Stringa con terminazione zero</span><span class="sxs-lookup"><span data-stu-id="442eb-148">Zero terminated String</span></span>              |
| <span data-ttu-id="442eb-149">tm</span><span class="sxs-lookup"><span data-stu-id="442eb-149">tm</span></span>     | <span data-ttu-id="442eb-150">Metrica testo</span><span class="sxs-lookup"><span data-stu-id="442eb-150">Text metric</span></span>                         |
| <span data-ttu-id="442eb-151">u</span><span class="sxs-lookup"><span data-stu-id="442eb-151">u</span></span>      | <span data-ttu-id="442eb-152">Int senza segno</span><span class="sxs-lookup"><span data-stu-id="442eb-152">Unsigned int</span></span>                        |
| <span data-ttu-id="442eb-153">ul</span><span class="sxs-lookup"><span data-stu-id="442eb-153">ul</span></span>     | <span data-ttu-id="442eb-154">Long senza segno (ULONG)</span><span class="sxs-lookup"><span data-stu-id="442eb-154">Unsigned long (ULONG)</span></span>               |
| <span data-ttu-id="442eb-155">w</span><span class="sxs-lookup"><span data-stu-id="442eb-155">w</span></span>      | <span data-ttu-id="442eb-156">WORD (unsigned short)</span><span class="sxs-lookup"><span data-stu-id="442eb-156">WORD (unsigned short)</span></span>               |
| <span data-ttu-id="442eb-157">x, y</span><span class="sxs-lookup"><span data-stu-id="442eb-157">x,y</span></span>    | <span data-ttu-id="442eb-158">coordinate x, y (Short)</span><span class="sxs-lookup"><span data-stu-id="442eb-158">x, y coordinates (short)</span></span>            |



 

<span data-ttu-id="442eb-159">Questi vengono spesso combinati, come nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="442eb-159">These are often combined, as in the following.</span></span>



| <span data-ttu-id="442eb-160">Combinazione di prefisso</span><span class="sxs-lookup"><span data-stu-id="442eb-160">Prefix combination</span></span> | <span data-ttu-id="442eb-161">Descrizione</span><span class="sxs-lookup"><span data-stu-id="442eb-161">Description</span></span>                                             |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="442eb-162">pszMyString</span><span class="sxs-lookup"><span data-stu-id="442eb-162">pszMyString</span></span>        | <span data-ttu-id="442eb-163">Puntatore a una stringa.</span><span class="sxs-lookup"><span data-stu-id="442eb-163">A pointer to a string.</span></span>                                  |
| <span data-ttu-id="442eb-164">\_pszMyString m</span><span class="sxs-lookup"><span data-stu-id="442eb-164">m\_pszMyString</span></span>     | <span data-ttu-id="442eb-165">Puntatore a una stringa che rappresenta un membro dati di una classe.</span><span class="sxs-lookup"><span data-stu-id="442eb-165">A pointer to a string that is a data member of a class.</span></span> |



 

<span data-ttu-id="442eb-166">Le altre convenzioni sono elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="442eb-166">Other conventions are listed in the following table.</span></span>



| <span data-ttu-id="442eb-167">Convenzione</span><span class="sxs-lookup"><span data-stu-id="442eb-167">Convention</span></span>       | <span data-ttu-id="442eb-168">Descrizione</span><span class="sxs-lookup"><span data-stu-id="442eb-168">Description</span></span>                                              |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="442eb-169">CMyClass</span><span class="sxs-lookup"><span data-stu-id="442eb-169">CMyClass</span></span>         | <span data-ttu-id="442eb-170">Prefisso "C" per i nomi delle classi C++.</span><span class="sxs-lookup"><span data-stu-id="442eb-170">Prefix 'C' for C++ class names.</span></span>                          |
| <span data-ttu-id="442eb-171">COMyObjectClass</span><span class="sxs-lookup"><span data-stu-id="442eb-171">COMyObjectClass</span></span>  | <span data-ttu-id="442eb-172">Prefisso "CO" per i nomi delle classi di oggetti COM.</span><span class="sxs-lookup"><span data-stu-id="442eb-172">Prefix 'CO' for COM object class names.</span></span>                  |
| <span data-ttu-id="442eb-173">CFMyClassFactory</span><span class="sxs-lookup"><span data-stu-id="442eb-173">CFMyClassFactory</span></span> | <span data-ttu-id="442eb-174">Prefisso "CF" per i nomi di class factory COM.</span><span class="sxs-lookup"><span data-stu-id="442eb-174">Prefix 'CF' for COM class factory names.</span></span>                 |
| <span data-ttu-id="442eb-175">IMyInterface</span><span class="sxs-lookup"><span data-stu-id="442eb-175">IMyInterface</span></span>     | <span data-ttu-id="442eb-176">Prefisso "I" per i nomi delle classi di interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="442eb-176">Prefix 'I' for COM interface class names.</span></span>                |
| <span data-ttu-id="442eb-177">CImpIMyInterface</span><span class="sxs-lookup"><span data-stu-id="442eb-177">CImpIMyInterface</span></span> | <span data-ttu-id="442eb-178">Prefisso ' CImpI ' per le classi di implementazione dell'interfaccia COM.</span><span class="sxs-lookup"><span data-stu-id="442eb-178">Prefix 'CImpI' for COM interface implementation classes.</span></span> |



 

<span data-ttu-id="442eb-179">Alcune convenzioni coerenti per i blocchi di intestazione dei commenti vengono usate in questa serie di esempio come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="442eb-179">Some consistent conventions for comment header blocks are used in this sample series as follows.</span></span>

## <a name="file-header"></a><span data-ttu-id="442eb-180">Intestazione del file</span><span class="sxs-lookup"><span data-stu-id="442eb-180">File Header</span></span>

``` syntax
/*+===================================================================
  File:      MYFILE.EXT

  Summary:   Brief summary of the file contents and purpose.

  Classes:   Classes declared or used (in source files).

  Functions: Functions exported (in source files).

  Origin:    Indications of where content may have come from. This
             is not a change history but rather a reference to the
             editor-inheritance behind the content or other
             indications about the origin of the source.

  Copyright and Legal notices.
  Copyright and Legal notices.
===================================================================+*/
```

## <a name="plain-comment-block"></a><span data-ttu-id="442eb-181">Blocco di commento semplice</span><span class="sxs-lookup"><span data-stu-id="442eb-181">Plain Comment Block</span></span>

``` syntax
/*--------------------------------------------------------------------
  Plain block of comment text that usually takes several lines.
  Plain block of comment text that usually takes several lines.
--------------------------------------------------------------------*/
```

## <a name="class-declaration-header"></a><span data-ttu-id="442eb-182">Intestazione della dichiarazione di classe</span><span class="sxs-lookup"><span data-stu-id="442eb-182">Class Declaration Header</span></span>

``` syntax
/*C+C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C
  Class:    CMyClass

  Summary:  Short summary of purpose and content of CMyClass.
            Short summary of purpose and content of CMyClass.

  Methods:  MyMethodOne
              Short description of MyMethodOne.
            MyMethodTwo
              Short description of MyMethodTwo.
            CMyClass
              Constructor.
            ~CMyClass
              Destructor.
C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C-C*/
```

## <a name="class-method-definition-header"></a><span data-ttu-id="442eb-183">Intestazione definizione metodo classe</span><span class="sxs-lookup"><span data-stu-id="442eb-183">Class Method Definition Header</span></span>

``` syntax
/*M+M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M
  Method:   CMyClass::MyMethodOne

  Summary:  Short summary of purpose and content of MyMethodOne.
            Short summary of purpose and content of MyMethodOne.

  Args:     MYTYPE MyArgOne
              Short description of argument MyArgOne.
            MYTYPE MyArgTwo
              Short description of argument MyArgTwo.

  Modifies: [list of member data variables modified by this method].

  Returns:  MYRETURNTYPE
              Short description of meaning of the return type values.
M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M-M*/
```

## <a name="unexported-or-local-function"></a><span data-ttu-id="442eb-184">Funzione locale o non esportata</span><span class="sxs-lookup"><span data-stu-id="442eb-184">Unexported or Local Function</span></span>

``` syntax
/*F+F+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
  Function: MyLocalFunction

  Summary:  What MyLocalFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
-----------------------------------------------------------------F-F*/
```

## <a name="exported-function-definition-header"></a><span data-ttu-id="442eb-185">Intestazione di definizione della funzione esportata</span><span class="sxs-lookup"><span data-stu-id="442eb-185">Exported Function Definition Header</span></span>

``` syntax
/*F+F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F
  Function: MyFunction

  Summary:  What MyFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F-F*/
```

## <a name="com-interface-declaration-header"></a><span data-ttu-id="442eb-186">Intestazione di dichiarazione dell'interfaccia COM</span><span class="sxs-lookup"><span data-stu-id="442eb-186">COM Interface Declaration Header</span></span>

``` syntax
/*I+I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I
  Interface: IMyInterface

  Summary:   Short summary of what features the interface can bring to
             a COM Component.

  Methods:   MYTYPE MyMethodOne
               Description.
             MYTYPE MyMethodTwo
               Description.
I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I-I*/
```

## <a name="com-object-class-declaration-header"></a><span data-ttu-id="442eb-187">Intestazione di dichiarazione della classe di oggetti COM</span><span class="sxs-lookup"><span data-stu-id="442eb-187">COM Object Class Declaration Header</span></span>

``` syntax
/*O+O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O
  ObjectClass: COMyCOMObject

  Summary:     Short summary of purpose and content of this object.

  Interfaces:  IUnknown
                 Standard interface providing COM object features.
               IMyInterfaceOne
                 Description.
               IMyInterfaceTwo
                 Description.

  Aggregation: [whether this COM Object is aggregatable or not]
O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O-O*/
```

<span data-ttu-id="442eb-188">Tutte le convenzioni di blocco di commento hanno stringhe di token iniziali e finali coerenti.</span><span class="sxs-lookup"><span data-stu-id="442eb-188">All of these comment block conventions have consistent beginning and ending token strings.</span></span> <span data-ttu-id="442eb-189">Questa coerenza supporta l'elaborazione automatica delle intestazioni in qualche modo.</span><span class="sxs-lookup"><span data-stu-id="442eb-189">This consistency supports automatic processing of the headers in some fashion.</span></span> <span data-ttu-id="442eb-190">È ad esempio possibile scrivere script AWK per filtrare le intestazioni di funzione in un file di testo separato che può quindi fungere da base per un documento di specifica.</span><span class="sxs-lookup"><span data-stu-id="442eb-190">For example, AWK scripts can be written to filter the function headers into a separate text file that can then serve as the basis for a specification document.</span></span> <span data-ttu-id="442eb-191">Analogamente, è possibile usare strumenti come l'utilità di autoduck non supportata (attualmente disponibile nel CD-ROM della libreria di sviluppo della rete per sviluppatori Microsoft) per elaborare i blocchi di commento in queste intestazioni.</span><span class="sxs-lookup"><span data-stu-id="442eb-191">Similarly, tools like the unsupported AUTODUCK utility (currently available on the Microsoft Developer Network Development Library CD-ROM) can be used to process the comment blocks in these headers.</span></span>

<span data-ttu-id="442eb-192">Nella tabella seguente sono elencate le stringhe dei token iniziali e finali utilizzate nelle esercitazioni di esempio.</span><span class="sxs-lookup"><span data-stu-id="442eb-192">The following table lists beginning and ending token strings used in sample tutorials.</span></span>



| <span data-ttu-id="442eb-193">token</span><span class="sxs-lookup"><span data-stu-id="442eb-193">Token</span></span> | <span data-ttu-id="442eb-194">Descrizione</span><span class="sxs-lookup"><span data-stu-id="442eb-194">Description</span></span>                      |
|-------|----------------------------------|
| /\*+  | <span data-ttu-id="442eb-195">Inizio intestazione file</span><span class="sxs-lookup"><span data-stu-id="442eb-195">File Header Begin</span></span>                |
| +\*/  | <span data-ttu-id="442eb-196">Fine intestazione file</span><span class="sxs-lookup"><span data-stu-id="442eb-196">File Header End</span></span>                  |
| /\*-  | <span data-ttu-id="442eb-197">Inizio intestazione blocco commento normale</span><span class="sxs-lookup"><span data-stu-id="442eb-197">Plain comment block Header Begin</span></span> |
| -\*/  | <span data-ttu-id="442eb-198">Fine intestazione blocco commento semplice</span><span class="sxs-lookup"><span data-stu-id="442eb-198">Plain comment block Header End</span></span>   |
| <span data-ttu-id="442eb-199">/\*C</span><span class="sxs-lookup"><span data-stu-id="442eb-199">/\*C</span></span>  | <span data-ttu-id="442eb-200">Inizio intestazione classe</span><span class="sxs-lookup"><span data-stu-id="442eb-200">Class Header Begin</span></span>               |
| <span data-ttu-id="442eb-201">C\*/</span><span class="sxs-lookup"><span data-stu-id="442eb-201">C\*/</span></span>  | <span data-ttu-id="442eb-202">Fine intestazione classe</span><span class="sxs-lookup"><span data-stu-id="442eb-202">Class Header End</span></span>                 |
| <span data-ttu-id="442eb-203">/\*M</span><span class="sxs-lookup"><span data-stu-id="442eb-203">/\*M</span></span>  | <span data-ttu-id="442eb-204">Inizio intestazione metodo</span><span class="sxs-lookup"><span data-stu-id="442eb-204">Method Header Begin</span></span>              |
| <span data-ttu-id="442eb-205">M\*/</span><span class="sxs-lookup"><span data-stu-id="442eb-205">M\*/</span></span>  | <span data-ttu-id="442eb-206">Fine intestazione metodo</span><span class="sxs-lookup"><span data-stu-id="442eb-206">Method Header End</span></span>                |
| <span data-ttu-id="442eb-207">/\*F</span><span class="sxs-lookup"><span data-stu-id="442eb-207">/\*F</span></span>  | <span data-ttu-id="442eb-208">Inizio intestazione funzione</span><span class="sxs-lookup"><span data-stu-id="442eb-208">Function Header Begin</span></span>            |
| <span data-ttu-id="442eb-209">F\*/</span><span class="sxs-lookup"><span data-stu-id="442eb-209">F\*/</span></span>  | <span data-ttu-id="442eb-210">Fine intestazione funzione</span><span class="sxs-lookup"><span data-stu-id="442eb-210">Function Header End</span></span>              |
| <span data-ttu-id="442eb-211">/\*I</span><span class="sxs-lookup"><span data-stu-id="442eb-211">/\*I</span></span>  | <span data-ttu-id="442eb-212">Inizio intestazione interfaccia</span><span class="sxs-lookup"><span data-stu-id="442eb-212">Interface Header Begin</span></span>           |
| <span data-ttu-id="442eb-213">I\*/</span><span class="sxs-lookup"><span data-stu-id="442eb-213">I\*/</span></span>  | <span data-ttu-id="442eb-214">Fine intestazione interfaccia</span><span class="sxs-lookup"><span data-stu-id="442eb-214">Interface Header End</span></span>             |
| <span data-ttu-id="442eb-215">/\*O</span><span class="sxs-lookup"><span data-stu-id="442eb-215">/\*O</span></span>  | <span data-ttu-id="442eb-216">Inizio intestazione classe oggetto COM</span><span class="sxs-lookup"><span data-stu-id="442eb-216">COM Object Class Header Begin</span></span>    |
| <span data-ttu-id="442eb-217">O\*/</span><span class="sxs-lookup"><span data-stu-id="442eb-217">O\*/</span></span>  | <span data-ttu-id="442eb-218">Fine intestazione classe oggetto COM</span><span class="sxs-lookup"><span data-stu-id="442eb-218">COM Object Class Header End</span></span>      |



 

<span data-ttu-id="442eb-219">Queste intestazioni possono essere utilizzate anche come segnali visivi per l'analisi rapida dei file di origine.</span><span class="sxs-lookup"><span data-stu-id="442eb-219">These headers can also be used as visual cues for rapid scanning of source files.</span></span> <span data-ttu-id="442eb-220">Consentono inoltre di accedere rapidamente ad alcune posizioni di origine se si configurano stringhe di ricerca nell'editor e quindi si ripete l'ultima ricerca per individuare rapidamente tali intestazioni.</span><span class="sxs-lookup"><span data-stu-id="442eb-220">They also provide convenience for rapidly getting to some source location if you set up search strings in your editor and then 'repeat last search' to quickly locate these headers.</span></span>

<span data-ttu-id="442eb-221">Ad esempio, la stringa di ricerca "M + M" individua l'inizio delle intestazioni del metodo e "M-M" individua l'inizio del codice effettivo di definizione/implementazione del metodo.</span><span class="sxs-lookup"><span data-stu-id="442eb-221">For example, the search string "M+M" will locate the start of method headers, and "M-M" will locate the beginning of the actual method definition/implementation code.</span></span>

 

 




