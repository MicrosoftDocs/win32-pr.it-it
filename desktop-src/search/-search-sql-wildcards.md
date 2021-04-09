---
description: Il predicato CONTAINs supporta l'utilizzo dell'asterisco ( \* ) come carattere jolly per rappresentare parole e frasi. È possibile aggiungere l'asterisco solo alla fine della parola o della frase. La presenza dell'asterisco Abilita la modalità di corrispondenza del prefisso.
ms.assetid: 9d141c7a-a721-416e-aa61-dabdb6533462
title: Utilizzo di caratteri jolly nel predicato CONTAINs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013e49f97cf23c7a00aca7bb287edd19951520f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128526"
---
# <a name="using-wildcard-characters-in-the-contains-predicate"></a><span data-ttu-id="5695d-105">Utilizzo di caratteri jolly nel predicato CONTAINs</span><span class="sxs-lookup"><span data-stu-id="5695d-105">Using Wildcard Characters in the CONTAINS Predicate</span></span>

<span data-ttu-id="5695d-106">Il predicato CONTAINs supporta l'utilizzo dell'asterisco ( \* ) come carattere jolly per rappresentare parole e frasi.</span><span class="sxs-lookup"><span data-stu-id="5695d-106">The CONTAINS predicate supports the use of the asterisk (\*) as a wildcard character to represent words and phrases.</span></span> <span data-ttu-id="5695d-107">È possibile aggiungere l'asterisco solo alla fine della parola o della frase.</span><span class="sxs-lookup"><span data-stu-id="5695d-107">You can add the asterisk only at the end of the word or phrase.</span></span> <span data-ttu-id="5695d-108">La presenza dell'asterisco Abilita la modalità di corrispondenza del prefisso.</span><span class="sxs-lookup"><span data-stu-id="5695d-108">The presence of the asterisk enables the prefix-matching mode.</span></span> <span data-ttu-id="5695d-109">In questa modalità vengono restituite corrispondenze se la colonna contiene la parola di ricerca specificata seguita da zero o più caratteri.</span><span class="sxs-lookup"><span data-stu-id="5695d-109">In this mode, matches are returned if the column contains the specified search word followed by zero or more other characters.</span></span> <span data-ttu-id="5695d-110">Se viene specificata una frase, le corrispondenze vengono rilevate se la colonna contiene tutte le parole specificate con zero o più caratteri successivi alla parola finale.</span><span class="sxs-lookup"><span data-stu-id="5695d-110">If a phrase is provided, matches are detected if the column contains all the specified words with zero or more other characters following the final word.</span></span>

## <a name="examples"></a><span data-ttu-id="5695d-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="5695d-111">Examples</span></span>

<span data-ttu-id="5695d-112">Il primo esempio corrisponde ai documenti che contengono una parola nella colonna FileName che inizia con "serv".</span><span class="sxs-lookup"><span data-stu-id="5695d-112">The first example matches documents that have any word in the FileName column beginning with "serv".</span></span> <span data-ttu-id="5695d-113">Le parole corrispondenti di esempio includono "Server", "Server" e "Service".</span><span class="sxs-lookup"><span data-stu-id="5695d-113">Example matching words include "server", "servers", and "service".</span></span>


```
...WHERE CONTAINS(System.FileName, '"serv*"')
```



<span data-ttu-id="5695d-114">Il secondo esempio trova la corrispondenza dei documenti con qualsiasi frase nella colonna FileName che inizia con "comp" e in cui la parola successiva inizia con "serv".</span><span class="sxs-lookup"><span data-stu-id="5695d-114">The second example matches documents with any phrase in the FileName column that begins with "comp" and in which the next word begins with "serv".</span></span> <span data-ttu-id="5695d-115">Le parole corrispondenti di esempio includono "comp server", "comp Servers" e "comp Service".</span><span class="sxs-lookup"><span data-stu-id="5695d-115">Example matching words include "comp server", "comp servers", and "comp service".</span></span>


```
...WHERE CONTAINS(System.FileName, '"comp serv*"')
```



<span data-ttu-id="5695d-116">L'asterisco funziona solo per la corrispondenza dei prefissi e può essere inserito solo alla fine della parola o frase. non funziona per la corrispondenza dei suffissi.</span><span class="sxs-lookup"><span data-stu-id="5695d-116">The asterisk works only for prefix-matching and can be placed only at the end of the word or phrase; it does not work for suffix-matching.</span></span> <span data-ttu-id="5695d-117">La sintassi seguente non è valida e non corrisponde ai documenti con alcuna parola nella colonna FileName che termina con "serve".</span><span class="sxs-lookup"><span data-stu-id="5695d-117">The following syntax is not valid and does not match documents with any word in the FileName column ending with "serve".</span></span>


```
WHERE CONTAINS(System.FileName, '"*serve"')
```



## <a name="related-topics"></a><span data-ttu-id="5695d-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5695d-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5695d-119">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="5695d-119">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5695d-120">Predicato FREETEXT</span><span class="sxs-lookup"><span data-stu-id="5695d-120">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="5695d-121">Clausola WHERE</span><span class="sxs-lookup"><span data-stu-id="5695d-121">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



