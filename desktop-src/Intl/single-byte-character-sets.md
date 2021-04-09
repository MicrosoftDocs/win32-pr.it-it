---
description: Un set di caratteri a byte singolo (SBCS) è un mapping di 256 singoli caratteri ai rispettivi valori di codice di identificazione, implementati come tabella codici.
ms.assetid: 53f74132-91aa-4257-846a-f6e1f2f9ae0b
title: Set di caratteri a byte singolo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5618b191b83e33333dce2a290d8c9a7181233df4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968593"
---
# <a name="single-byte-character-sets"></a><span data-ttu-id="af0b0-103">Set di caratteri a byte singolo</span><span class="sxs-lookup"><span data-stu-id="af0b0-103">Single-byte Character Sets</span></span>

<span data-ttu-id="af0b0-104">Un set di caratteri a byte singolo (SBCS) è un mapping di 256 singoli caratteri ai rispettivi valori di codice di identificazione, implementati come tabella codici.</span><span class="sxs-lookup"><span data-stu-id="af0b0-104">A single-byte character set (SBCS) is a mapping of 256 individual characters to their identifying code values, implemented as a code page.</span></span> <span data-ttu-id="af0b0-105">Un SBCS può corrispondere a una tabella codici di Windows o a una tabella codici OEM.</span><span class="sxs-lookup"><span data-stu-id="af0b0-105">An SBCS can correspond either to a Windows code page or an OEM code page.</span></span> <span data-ttu-id="af0b0-106">Una tabella codici SBCS può includere anche una tabella codici non nativa, ad esempio una tabella codici EBCDIC.</span><span class="sxs-lookup"><span data-stu-id="af0b0-106">An SBCS code page can also include a non-native code page, for example, an EBCDIC code page.</span></span> <span data-ttu-id="af0b0-107">Per le definizioni di queste tabelle codici, vedere [tabelle codici](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="af0b0-107">For definitions of these code pages, see [Code Pages](code-pages.md).</span></span>

> [!Note]  
> <span data-ttu-id="af0b0-108">Le nuove applicazioni Windows devono utilizzare [Unicode](unicode.md) per evitare le incoerenze di diverse tabelle codici e per semplificare la localizzazione.</span><span class="sxs-lookup"><span data-stu-id="af0b0-108">New Windows applications should use [Unicode](unicode.md) to avoid the inconsistencies of varied code pages and for ease of localization.</span></span> <span data-ttu-id="af0b0-109">Tuttavia, alcuni protocolli legacy richiedono l'uso di un SBCS.</span><span class="sxs-lookup"><span data-stu-id="af0b0-109">However, some legacy protocols require the use of an SBCS.</span></span> <span data-ttu-id="af0b0-110">Ogni tabella codici SBCS supporta caratteri diversi, ma nessuna pagina supporta l'intera gamma di caratteri forniti da Unicode.</span><span class="sxs-lookup"><span data-stu-id="af0b0-110">Each SBCS code page supports different characters, but no page supports the full breadth of characters provided by Unicode.</span></span> <span data-ttu-id="af0b0-111">Ogni tabella codici SBCS supporta un subset diverso, codificato in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="af0b0-111">Each SBCS code page supports a different subset, differently encoded.</span></span> <span data-ttu-id="af0b0-112">I dati convertiti da una tabella codici SBCS a un'altra sono soggetti a danneggiamento, perché lo stesso valore di dati in tabelle codici diverse può codificare un carattere diverso.</span><span class="sxs-lookup"><span data-stu-id="af0b0-112">Data converted from one SBCS code page to another is subject to corruption, because the same data value on different code pages can encode a different character.</span></span> <span data-ttu-id="af0b0-113">I dati convertiti da Unicode a SBCS sono soggetti alla perdita di dati perché una determinata tabella codici potrebbe non essere in grado di rappresentare ogni carattere utilizzato in tali dati Unicode particolari.</span><span class="sxs-lookup"><span data-stu-id="af0b0-113">Data converted from Unicode to SBCS is subject to data loss because a given code page might not be able to represent every character used in that particular Unicode data.</span></span>

 

<span data-ttu-id="af0b0-114">Le applicazioni usano le tabelle codici di Windows SBCS con le versioni "A" delle funzioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="af0b0-114">Your applications use SBCS Windows code pages with the "A" versions of Windows functions.</span></span> <span data-ttu-id="af0b0-115">Vedere [convenzioni per prototipi di funzione](conventions-for-function-prototypes.md) e [tabelle codici](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="af0b0-115">See [Conventions for Function Prototypes](conventions-for-function-prototypes.md) and [Code Pages](code-pages.md).</span></span> <span data-ttu-id="af0b0-116">Per semplificare l'identificazione di una tabella codici SBCS, un'applicazione può utilizzare la funzione [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) o [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) .</span><span class="sxs-lookup"><span data-stu-id="af0b0-116">To help identify an SBCS code page, an application can use the [**GetCPInfo**](/windows/desktop/api/Winnls/nf-winnls-getcpinfo) or [**GetCPInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcpinfoexa) function.</span></span> <span data-ttu-id="af0b0-117">Inoltre, un'applicazione può utilizzare le funzioni [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) per eseguire il mapping tra le stringhe Unicode e SBCS.</span><span class="sxs-lookup"><span data-stu-id="af0b0-117">In addition, an application can use the [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) and [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) functions to map between Unicode and SBCS strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af0b0-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="af0b0-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af0b0-119">Character Sets</span><span class="sxs-lookup"><span data-stu-id="af0b0-119">Character Sets</span></span>](character-sets.md)
</dt> <dt>

[<span data-ttu-id="af0b0-120">Set di caratteri a byte doppio</span><span class="sxs-lookup"><span data-stu-id="af0b0-120">Double-byte Character Sets</span></span>](double-byte-character-sets.md)
</dt> </dl>

 

 



