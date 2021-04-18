---
description: 'Le funzioni API Windows che modificano i caratteri vengono in genere implementate in uno dei tre formati seguenti:'
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Unicode nell'API Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5686a7f65edefb11458374b7f72262448becd6d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314801"
---
# <a name="unicode-in-the-windows-api"></a><span data-ttu-id="f8dc4-103">Unicode nell'API Windows</span><span class="sxs-lookup"><span data-stu-id="f8dc4-103">Unicode in the Windows API</span></span>

<span data-ttu-id="f8dc4-104">Le funzioni API Windows che modificano i caratteri vengono in genere implementate in uno dei tre formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="f8dc4-104">Windows API functions that manipulate characters are generally implemented in one of three formats:</span></span>

-   <span data-ttu-id="f8dc4-105">Versione generica che può essere compilata per le tabelle codici di Windows o Unicode</span><span class="sxs-lookup"><span data-stu-id="f8dc4-105">A generic version that can be compiled for either Windows code pages or Unicode</span></span>
-   <span data-ttu-id="f8dc4-106">Una versione della [tabella codici di Windows](code-pages.md) con la lettera "a" usata per indicare "ANSI"</span><span class="sxs-lookup"><span data-stu-id="f8dc4-106">A [Windows code page](code-pages.md) version with the letter "A" used to indicate "ANSI"</span></span>
-   <span data-ttu-id="f8dc4-107">Una versione [Unicode](unicode.md) con la lettera "W" utilizzata per indicare "wide"</span><span class="sxs-lookup"><span data-stu-id="f8dc4-107">A [Unicode](unicode.md) version with the letter "W" used to indicate "wide"</span></span>

<span data-ttu-id="f8dc4-108">Alcune funzioni più recenti supportano solo versioni Unicode.</span><span class="sxs-lookup"><span data-stu-id="f8dc4-108">Some newer functions support only Unicode versions.</span></span> <span data-ttu-id="f8dc4-109">Per altre informazioni, vedere [convenzioni per i prototipi di funzione](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="f8dc4-109">For more information, see [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span>

<span data-ttu-id="f8dc4-110">Negli argomenti seguenti vengono illustrati i tipi di dati Unicode e il modo in cui vengono utilizzati in funzioni e messaggi. l'uso di risorse, nomi file e argomenti della riga di comando; metodi e per la conversione tra tipi diversi di stringhe.</span><span class="sxs-lookup"><span data-stu-id="f8dc4-110">The following topics discuss Unicode data types and how they are used in functions and messages; the use of resources, file names, and command line arguments; and methods of translating between different types of strings.</span></span>

-   [<span data-ttu-id="f8dc4-111">Traduzione automatica di messaggi</span><span class="sxs-lookup"><span data-stu-id="f8dc4-111">Automatic Message Translation</span></span>](automatic-message-translation.md)
-   [<span data-ttu-id="f8dc4-112">Set di caratteri utilizzati nei nomi file</span><span class="sxs-lookup"><span data-stu-id="f8dc4-112">Character Sets Used in File Names</span></span>](character-sets-used-in-file-names.md)
-   [<span data-ttu-id="f8dc4-113">Argomenti della riga di comando</span><span class="sxs-lookup"><span data-stu-id="f8dc4-113">Command Line Arguments</span></span>](command-line-arguments.md)
-   [<span data-ttu-id="f8dc4-114">Convenzioni per prototipi di funzione</span><span class="sxs-lookup"><span data-stu-id="f8dc4-114">Conventions for Function Prototypes</span></span>](conventions-for-function-prototypes.md)
-   [<span data-ttu-id="f8dc4-115">Funzioni C standard</span><span class="sxs-lookup"><span data-stu-id="f8dc4-115">Standard C Functions</span></span>](standard-c-functions.md)
-   [<span data-ttu-id="f8dc4-116">Differenze tra le funzioni di stringa</span><span class="sxs-lookup"><span data-stu-id="f8dc4-116">String Function Differences</span></span>](string-function-differences.md)
-   [<span data-ttu-id="f8dc4-117">Conversione tra tipi di stringa</span><span class="sxs-lookup"><span data-stu-id="f8dc4-117">Translation Between String Types</span></span>](translation-between-string-types.md)
-   [<span data-ttu-id="f8dc4-118">Tipi di dati di Windows per le stringhe</span><span class="sxs-lookup"><span data-stu-id="f8dc4-118">Windows Data Types for Strings</span></span>](windows-data-types-for-strings.md)

## <a name="related-topics"></a><span data-ttu-id="f8dc4-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8dc4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8dc4-120">Informazioni sui set di caratteri e Unicode</span><span class="sxs-lookup"><span data-stu-id="f8dc4-120">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



