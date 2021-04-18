---
description: Un &\# 0034; set di caratteri&\# 0034; è un mapping di caratteri ai rispettivi valori di codice di identificazione.
ms.assetid: 0a055c02-c5ed-4790-83e4-183bc3cc6b51
title: Character Sets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8e62a0afbe9e5b2b3ab596a8129db833477e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306611"
---
# <a name="character-sets"></a><span data-ttu-id="89de0-103">Character Sets</span><span class="sxs-lookup"><span data-stu-id="89de0-103">Character Sets</span></span>

<span data-ttu-id="89de0-104">Un "set di caratteri" è un mapping di caratteri ai rispettivi valori di codice di identificazione.</span><span class="sxs-lookup"><span data-stu-id="89de0-104">A "character set" is a mapping of characters to their identifying code values.</span></span> <span data-ttu-id="89de0-105">Il set di caratteri usato più di frequente nei computer attualmente è [Unicode](unicode.md), uno standard globale per la codifica dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="89de0-105">The character set most commonly used in computers today is [Unicode](unicode.md), a global standard for character encoding.</span></span> <span data-ttu-id="89de0-106">Internamente, le applicazioni Windows utilizzano l'implementazione UTF-16 di Unicode.</span><span class="sxs-lookup"><span data-stu-id="89de0-106">Internally, Windows applications use the UTF-16 implementation of Unicode.</span></span> <span data-ttu-id="89de0-107">In UTF-16 la maggior parte dei caratteri è identificata da codici a due byte.</span><span class="sxs-lookup"><span data-stu-id="89de0-107">In UTF-16, most characters are identified by two-byte codes.</span></span> <span data-ttu-id="89de0-108">I caratteri supplementari utilizzati meno di frequente sono rappresentati da una coppia di surrogati, ovvero una coppia di codici a due byte.</span><span class="sxs-lookup"><span data-stu-id="89de0-108">The less commonly used supplementary characters are each represented by a surrogate pair, which is a pair of two-byte codes.</span></span> <span data-ttu-id="89de0-109">Per ulteriori informazioni, vedere [surrogati e caratteri supplementari](surrogates-and-supplementary-characters.md).</span><span class="sxs-lookup"><span data-stu-id="89de0-109">For more information, see [Surrogates and Supplementary Characters](surrogates-and-supplementary-characters.md).</span></span>

<span data-ttu-id="89de0-110">Alcune applicazioni Windows devono funzionare con i set di caratteri meno recenti nativi di Windows Me/98/95.</span><span class="sxs-lookup"><span data-stu-id="89de0-110">Some Windows applications must work with the older character sets that are native to Windows Me/98/95.</span></span> <span data-ttu-id="89de0-111">Le [tabelle codici di Windows](code-pages.md) consentono all'applicazione di usare questi set di caratteri.</span><span class="sxs-lookup"><span data-stu-id="89de0-111">[Windows code pages](code-pages.md) allow your application to work with these character sets.</span></span> <span data-ttu-id="89de0-112">Questi set di caratteri possono essere divisi in:</span><span class="sxs-lookup"><span data-stu-id="89de0-112">These character sets can be divided into:</span></span>

-   <span data-ttu-id="89de0-113">[Set di caratteri a byte singolo](single-byte-character-sets.md) (SBCS).</span><span class="sxs-lookup"><span data-stu-id="89de0-113">[Single-byte character sets](single-byte-character-sets.md) (SBCS).</span></span> <span data-ttu-id="89de0-114">In un SBCS ogni carattere viene identificato da un valore a una larghezza di byte.</span><span class="sxs-lookup"><span data-stu-id="89de0-114">In an SBCS, each character is identified by a value one byte wide.</span></span>
-   <span data-ttu-id="89de0-115">Set di caratteri multibyte, in particolare i [set di caratteri a doppio byte](double-byte-character-sets.md) (DBCS).</span><span class="sxs-lookup"><span data-stu-id="89de0-115">Multibyte character sets, in particular the [double-byte character sets](double-byte-character-sets.md) (DBCS).</span></span> <span data-ttu-id="89de0-116">I set di caratteri multibyte forniscono un mezzo per rappresentare il numero elevato di caratteri in molte lingue asiatiche.</span><span class="sxs-lookup"><span data-stu-id="89de0-116">Multibyte character sets provide a means to represent the large number of characters in many Asian languages.</span></span>

<span data-ttu-id="89de0-117">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="89de0-117">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="89de0-118">Tabelle codici</span><span class="sxs-lookup"><span data-stu-id="89de0-118">Code Pages</span></span>](code-pages.md)
-   [<span data-ttu-id="89de0-119">Set di caratteri a byte doppio</span><span class="sxs-lookup"><span data-stu-id="89de0-119">Double-byte Character Sets</span></span>](double-byte-character-sets.md)
-   [<span data-ttu-id="89de0-120">Set di caratteri a byte singolo</span><span class="sxs-lookup"><span data-stu-id="89de0-120">Single-byte Character Sets</span></span>](single-byte-character-sets.md)
-   [<span data-ttu-id="89de0-121">Surrogati e caratteri supplementari</span><span class="sxs-lookup"><span data-stu-id="89de0-121">Surrogates and Supplementary Characters</span></span>](surrogates-and-supplementary-characters.md)
-   [<span data-ttu-id="89de0-122">Unicode</span><span class="sxs-lookup"><span data-stu-id="89de0-122">Unicode</span></span>](unicode.md)

## <a name="related-topics"></a><span data-ttu-id="89de0-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="89de0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89de0-124">Informazioni sui set di caratteri e Unicode</span><span class="sxs-lookup"><span data-stu-id="89de0-124">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



