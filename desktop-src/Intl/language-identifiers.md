---
description: Un identificatore di lingua è un'abbreviazione numerica internazionale standard per la lingua in un paese o in un'area geografica.
ms.assetid: 076e2a43-256a-4646-a5c8-1d48ab08ce1a
title: Identificatori di lingua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e3e8f88a64d49d04402c0e72a3946bcddc41e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307854"
---
# <a name="language-identifiers"></a><span data-ttu-id="5d222-103">Identificatori di lingua</span><span class="sxs-lookup"><span data-stu-id="5d222-103">Language Identifiers</span></span>

<span data-ttu-id="5d222-104">Un identificatore di lingua è un'abbreviazione numerica internazionale standard per la [lingua](locales-and-languages.md) in un paese o in un'area geografica.</span><span class="sxs-lookup"><span data-stu-id="5d222-104">A language identifier is a standard international numeric abbreviation for the [language](locales-and-languages.md) in a country or geographical region.</span></span> <span data-ttu-id="5d222-105">Ogni lingua dispone di un identificatore di lingua univoco (tipo di dati LANGID), un valore a 16 bit costituito da un identificatore di lingua principale e un identificatore di lingua.</span><span class="sxs-lookup"><span data-stu-id="5d222-105">Each language has a unique language identifier (data type LANGID), a 16-bit value that consists of a primary language identifier and a sublanguage identifier.</span></span> <span data-ttu-id="5d222-106">Per informazioni dettagliate sugli identificatori di lingua, vedere [costanti e stringhe degli identificatori di lingua](language-identifier-constants-and-strings.md).</span><span class="sxs-lookup"><span data-stu-id="5d222-106">For details of language identifiers, see [Language Identifier Constants and Strings](language-identifier-constants-and-strings.md).</span></span>

<span data-ttu-id="5d222-107">Un identificatore di lingua viene costruito usando la macro [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) .</span><span class="sxs-lookup"><span data-stu-id="5d222-107">A language identifier is constructed using the [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) macro.</span></span> <span data-ttu-id="5d222-108">Nella figura seguente viene illustrato il formato dei bit in un identificatore di lingua.</span><span class="sxs-lookup"><span data-stu-id="5d222-108">The following illustration shows the format of the bits in a language identifier.</span></span>

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

<span data-ttu-id="5d222-109">Gli identificatori di lingua predefiniti sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5d222-109">The following are predefined language identifiers:</span></span>

-   <span data-ttu-id="5d222-110">\_impostazione predefinita del sistema lang \_ .</span><span class="sxs-lookup"><span data-stu-id="5d222-110">LANG\_SYSTEM\_DEFAULT.</span></span> <span data-ttu-id="5d222-111">Lingua predefinita del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5d222-111">The operating system default language.</span></span>
-   <span data-ttu-id="5d222-112">\_impostazione predefinita dell'utente lang \_ .</span><span class="sxs-lookup"><span data-stu-id="5d222-112">LANG\_USER\_DEFAULT.</span></span> <span data-ttu-id="5d222-113">Lingua dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="5d222-113">The language of the current user.</span></span>

<span data-ttu-id="5d222-114">L'applicazione può recuperare gli identificatori di lingua correnti utilizzando le funzioni dell' [interfaccia utente multilingue](multilingual-user-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="5d222-114">Your application can retrieve the current language identifiers by using the [Multilingual User Interface](multilingual-user-interface.md) functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d222-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5d222-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d222-116">Impostazioni locali e lingue</span><span class="sxs-lookup"><span data-stu-id="5d222-116">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="5d222-117">Costanti e stringhe degli identificatori di lingua</span><span class="sxs-lookup"><span data-stu-id="5d222-117">Language Identifier Constants and Strings</span></span>](language-identifier-constants-and-strings.md)
</dt> <dt>

[<span data-ttu-id="5d222-118">Interfaccia utente multilingue</span><span class="sxs-lookup"><span data-stu-id="5d222-118">Multilingual User Interface</span></span>](multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="5d222-119">**MAKELANGID**</span><span class="sxs-lookup"><span data-stu-id="5d222-119">**MAKELANGID**</span></span>](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 



