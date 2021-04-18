---
description: Il formato del tipo di carattere OpenType basato su Unicode estende il formato del file del tipo di carattere TrueType.
ms.assetid: 0d67481a-79ff-448c-b77c-a55bf935a22a
title: Formato dei tipi di carattere OpenType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a907f0a0480c92a35b299540e3bed240ebc3b6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319053"
---
# <a name="opentype-font-format"></a><span data-ttu-id="48b65-103">Formato dei tipi di carattere OpenType</span><span class="sxs-lookup"><span data-stu-id="48b65-103">OpenType Font Format</span></span>

<span data-ttu-id="48b65-104">Il formato del tipo di carattere OpenType basato su Unicode estende il formato del file del tipo di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="48b65-104">The Unicode-based OpenType font format extends the TrueType font file format.</span></span> <span data-ttu-id="48b65-105">I tipi di carattere OpenType consentono il mapping tra caratteri e [glifi](uniscribe-glossary.md), abilitando il supporto per legature, moduli posizionali, alternative e altre sostituzioni.</span><span class="sxs-lookup"><span data-stu-id="48b65-105">OpenType fonts allow mapping between characters and [glyphs](uniscribe-glossary.md), enabling support for ligatures, positional forms, alternates, and other substitutions.</span></span> <span data-ttu-id="48b65-106">I tipi di carattere OpenType possono includere anche informazioni che supportano il posizionamento del glifo bidimensionale e l'allegato del glifo e possono contenere strutture TrueType o PostScript.</span><span class="sxs-lookup"><span data-stu-id="48b65-106">OpenType fonts can also include information that supports two-dimensional glyph positioning and glyph attachment, and can contain either TrueType or PostScript outlines.</span></span>

<span data-ttu-id="48b65-107">Le funzionalità di layout nei tipi di carattere OpenType sono organizzate in base a script e linguaggi, consentendo a un singolo tipo di carattere di supportare più sistemi di scrittura, anche nello stesso script.</span><span class="sxs-lookup"><span data-stu-id="48b65-107">Layout features within OpenType fonts are organized by scripts and languages, allowing a single font to support multiple writing systems, even within the same script.</span></span> <span data-ttu-id="48b65-108">Per garantire la coerenza nelle operazioni di layout del testo ed evitare un sovraccarico superfluo nei file o nelle applicazioni dei tipi di carattere, molti degli algoritmi di layout del testo e semantica del linguaggio sono inclusi in Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="48b65-108">To ensure consistency in text layout operations and to avoid unnecessary overhead in font files or applications, many of the text layout and language semantic algorithms are included in Uniscribe.</span></span> <span data-ttu-id="48b65-109">Ciò consente allo sviluppatore di tipi di carattere di definire regole di script generalizzate all'interno di un tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="48b65-109">This relieves the font developer from having to define generalized script rules within a font.</span></span>

<span data-ttu-id="48b65-110">Le applicazioni possono introdurre conoscenze specifiche o preferenze relative al layout di script.</span><span class="sxs-lookup"><span data-stu-id="48b65-110">Applications can introduce specific knowledge or preferences regarding script layout.</span></span> <span data-ttu-id="48b65-111">I tipi di carattere del layout OpenType potrebbero contenere anche regole di layout che duplicano o sostituiscono quelle applicate dai servizi del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="48b65-111">OpenType layout fonts might even contain layout rules that duplicate or supersede those applied by operating system services.</span></span> <span data-ttu-id="48b65-112">La struttura a più livelli dei servizi del sistema operativo che supportano il layout del testo consente a un'applicazione di scegliere le informazioni sul layout da usare e di selezionare la modalità di applicazione.</span><span class="sxs-lookup"><span data-stu-id="48b65-112">The layered structure of operating system services supporting text layout allows an application to choose the layout information to use, and select how to apply it.</span></span> <span data-ttu-id="48b65-113">Per ulteriori informazioni, vedere [Cenni preliminari sulle specifiche di Microsoft Typography](https://www.microsoft.com/typography/SpecificationsOverview.mspx) o la [specifica OpenType](https://www.microsoft.com/typography/otspec/).</span><span class="sxs-lookup"><span data-stu-id="48b65-113">For additional information, see the [Microsoft Typography Specifications overview](https://www.microsoft.com/typography/SpecificationsOverview.mspx) or the [OpenType Specification](https://www.microsoft.com/typography/otspec/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="48b65-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="48b65-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="48b65-115">Informazioni su Uniscribe</span><span class="sxs-lookup"><span data-stu-id="48b65-115">About Uniscribe</span></span>](about-uniscribe.md)
</dt> </dl>

 

 



