---
title: Chiamata delle funzioni
description: Chiamata delle funzioni
ms.assetid: c5a675f2-86fc-4f53-8d09-604ab4752d7b
keywords:
- Interfacce di Media Player Windows, chiamata di funzioni in JScript
- interfacce, chiamata di funzioni in JScript
- chiamata di funzioni in JScript
- File JScript per interfacce, chiamate di funzioni
- Windows Media Player Skin, attributo scriptFile in JScript
- interfacce, attributo scriptFile in JScript
- attributi, scriptFile in JScript
- attributo scriptFile in JScript
- File JScript per interfacce, attributo scriptFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9450c8ca09b75f66f6206c850a656192bb1bb9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516078"
---
# <a name="calling-functions"></a><span data-ttu-id="9170e-112">Chiamata delle funzioni</span><span class="sxs-lookup"><span data-stu-id="9170e-112">Calling Functions</span></span>

<span data-ttu-id="9170e-113">Se è necessario chiamare più righe di codice, è possibile caricare un file di script usando l'attributo **scriptFile** dell'elemento **View** e chiamare le funzioni nello script.</span><span class="sxs-lookup"><span data-stu-id="9170e-113">If you need to call more than a few lines of code, you can load a script file using the **scriptFile** attribute of the **VIEW** element, and call the functions in the script.</span></span> <span data-ttu-id="9170e-114">È possibile caricare più di un file per visualizzazione:</span><span class="sxs-lookup"><span data-stu-id="9170e-114">You can load more than one file per view:</span></span>


```C++
scriptFile = "myfile1.js;myfile2.js;myfile3.js"

```



<span data-ttu-id="9170e-115">Una volta caricati i file di script, è possibile chiamare le funzioni all'interno della sezione di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="9170e-115">After the script files are loaded, you can call functions in them from inside your View section.</span></span> <span data-ttu-id="9170e-116">Ad esempio, per chiamare una *funzione denominata Function* quando si fa clic su un elemento, digitare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="9170e-116">For example, to call a function called *myfunction* when something is clicked, type the following:</span></span>


```C++
onclick = "JScript: myfunction()"

```



> [!Note]  
> <span data-ttu-id="9170e-117">Se si dispone di più di una vista, solo le funzioni nei file caricati nella visualizzazione corrente sono disponibili per il codice XML e JScript in esecuzione con la visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="9170e-117">If you have more than one view, only the functions in files loaded into the current view are available to the XML and JScript code running with the current view.</span></span> <span data-ttu-id="9170e-118">I file caricati in altre viste non si trovano nell'ambito della visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="9170e-118">Files loaded in other views are not in scope with the current view.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9170e-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9170e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9170e-120">**Utilizzo di JScript**</span><span class="sxs-lookup"><span data-stu-id="9170e-120">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




