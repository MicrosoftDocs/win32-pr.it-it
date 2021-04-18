---
title: Combinazioni di testo
description: Combinazioni di testo
ms.assetid: 0220b77e-5f1e-4569-a8fe-5085e0c16338
keywords:
- Interfacce di Windows Media Player Mobile, Marquees
- interfacce, Marquee
- riferimento per Skin, Marquees
- Marquees in Skin, combinazioni di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5668a9e18555b871c82bae7ed1826766ec9429e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515841"
---
# <a name="text-combinations"></a><span data-ttu-id="dab0e-107">Combinazioni di testo</span><span class="sxs-lookup"><span data-stu-id="dab0e-107">Text Combinations</span></span>

<span data-ttu-id="dab0e-108">Questo valore è un elenco di combinazioni di caselle di testo, separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="dab0e-108">This value is a list of text display box combinations, separated by commas.</span></span> <span data-ttu-id="dab0e-109">Le caselle di visualizzazione del testo possono essere unite in join da un carattere più per creare un nuovo valore di visualizzazione Marquee e qualsiasi tipo di testo definito nella sezione tipo testo può essere usato nel Marquee.</span><span class="sxs-lookup"><span data-stu-id="dab0e-109">Text display boxes can be joined together by a plus character to create a new marquee display value and any text type defined in the Text Type section can be used in your marquee.</span></span>

<span data-ttu-id="dab0e-110">Quando si determinano gli elementi da visualizzare, Windows Media Player mobile valuta ogni elemento dell'elenco per verificare se sono disponibili tutte le parti.</span><span class="sxs-lookup"><span data-stu-id="dab0e-110">When determining what to display, Windows Media Player Mobile evaluates each item in the list to see if all parts are available.</span></span> <span data-ttu-id="dab0e-111">In caso contrario, l'elemento successivo viene valutato e così via fino a quando non vengono trovate tutte le parti disponibili.</span><span class="sxs-lookup"><span data-stu-id="dab0e-111">If not, the next item is evaluated, and so on, until all the available parts have been found.</span></span> <span data-ttu-id="dab0e-112">Se, ad esempio, si desidera visualizzare autore e titolo, ma non si è certi che entrambi siano disponibili, utilizzare il valore seguente:</span><span class="sxs-lookup"><span data-stu-id="dab0e-112">For example, if you want to display Author and Title, but you're not sure whether both are available, use the following value:</span></span>


```C++
Title+Author, Title, Author

```



<span data-ttu-id="dab0e-113">Nell'esempio precedente, il titolo + autore verrà visualizzato se il titolo e l'autore sono stati definiti per l'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="dab0e-113">In the preceding example, the Title+Author will be displayed if the title and author have been defined for the media item.</span></span> <span data-ttu-id="dab0e-114">Se non sono definiti entrambi, il titolo viene valutato e visualizzato se definito.</span><span class="sxs-lookup"><span data-stu-id="dab0e-114">If both are not defined, the Title is evaluated and displayed if defined.</span></span> <span data-ttu-id="dab0e-115">Se il titolo non è definito, l'autore viene visualizzato se definito.</span><span class="sxs-lookup"><span data-stu-id="dab0e-115">If the Title is not defined, the Author is displayed if defined.</span></span> <span data-ttu-id="dab0e-116">Se non viene definito alcun elemento, non viene visualizzato nulla.</span><span class="sxs-lookup"><span data-stu-id="dab0e-116">If neither is defined, then nothing is displayed.</span></span>

<span data-ttu-id="dab0e-117">Quando si usa il segno più per la concatenazione, assicurarsi di non avere spazi su entrambi i lati del segno più.</span><span class="sxs-lookup"><span data-stu-id="dab0e-117">When using the plus sign for concatenation, be sure you have no spaces on either side of the plus sign.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dab0e-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dab0e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dab0e-119">**Testo scorrevole**</span><span class="sxs-lookup"><span data-stu-id="dab0e-119">**Marquee**</span></span>](marquee.md)
</dt> <dt>

[<span data-ttu-id="dab0e-120">**Tipo di testo**</span><span class="sxs-lookup"><span data-stu-id="dab0e-120">**Text Type**</span></span>](text-type.md)
</dt> </dl>

 

 




