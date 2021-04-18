---
description: Il termine FORMSOF esegue corrispondenze usando altre forme linguistiche della parola.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: Termine FORMSOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20504a7a36c7f0cb9c69b9513f33446501641bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306129"
---
# <a name="formsof-term"></a><span data-ttu-id="55cb1-103">Termine FORMSOF</span><span class="sxs-lookup"><span data-stu-id="55cb1-103">FORMSOF Term</span></span>

<span data-ttu-id="55cb1-104">Il termine FORMSOF esegue corrispondenze usando altre forme linguistiche della parola.</span><span class="sxs-lookup"><span data-stu-id="55cb1-104">The FORMSOF term performs matches using other linguistic forms of the word.</span></span> <span data-ttu-id="55cb1-105">Di seguito è riportata la sintassi del termine FORMSOF:</span><span class="sxs-lookup"><span data-stu-id="55cb1-105">The following is the FORMSOF term syntax:</span></span>


```
FORMSOF (<generation_type>,<match_words>)
```



<span data-ttu-id="55cb1-106">Il tipo di generazione specifica il modo in cui Microsoft Windows Search sceglie i moduli Word alternativi.</span><span class="sxs-lookup"><span data-stu-id="55cb1-106">The generation type specifies how Microsoft Windows Search chooses the alternative word forms.</span></span> <span data-ttu-id="55cb1-107">Il valore **flessore** sceglie forme di flessione alternative per le parole di corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="55cb1-107">The **INFLECTIONAL** value chooses alternative inflection forms for the match words.</span></span> <span data-ttu-id="55cb1-108">Se la parola è un verbo, vengono usati i tempi alternativi.</span><span class="sxs-lookup"><span data-stu-id="55cb1-108">If the word is a verb, alternative tenses are used.</span></span> <span data-ttu-id="55cb1-109">Se la parola è un sostantivo, le forme singolare, plurale e possessive vengono usate per rilevare le corrispondenze.</span><span class="sxs-lookup"><span data-stu-id="55cb1-109">If the word is a noun, the singular, plural, and possessive forms are used to detect matches.</span></span>

<span data-ttu-id="55cb1-110">Il valore delle parole di ricerca corrisponde \_ a una o più parole, separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="55cb1-110">The match\_words value is one or more words, separated by commas.</span></span>

## <a name="examples"></a><span data-ttu-id="55cb1-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="55cb1-111">Examples</span></span>

<span data-ttu-id="55cb1-112">Nell'esempio seguente viene eseguita la ricerca di corrispondenze flessori per la parola "Run".</span><span class="sxs-lookup"><span data-stu-id="55cb1-112">The following example searches for inflectional matches for the word "run".</span></span> <span data-ttu-id="55cb1-113">Questo esempio corrisponde ai documenti che contengono "Run", "Running" o "Ran".</span><span class="sxs-lookup"><span data-stu-id="55cb1-113">This example matches documents containing "run", "running", or "ran".</span></span>


```
...CONTAINS('FORMSOF(INFLECTIONAL,"run")')
```



## <a name="related-topics"></a><span data-ttu-id="55cb1-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="55cb1-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="55cb1-115">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="55cb1-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="55cb1-116">Predicato FREETEXT</span><span class="sxs-lookup"><span data-stu-id="55cb1-116">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="55cb1-117">Clausola WHERE</span><span class="sxs-lookup"><span data-stu-id="55cb1-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



