---
title: Informazioni sui file SAMI
description: Informazioni sui file SAMI
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- Modello a oggetti di Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- modello a oggetti, interscambio multimediale accessibile sincronizzato (SAMI)
- Windows Media Player Mobile, Media Interchange accessibile sincronizzato (SAMI)
- Controllo ActiveX Windows Media Player, Media Interchange accessibile sincronizzato (SAMI)
- Windows Media Player Mobile ActiveX Control, Synchronized Accessible Media Interchange (SAMI)
- Controllo ActiveX, interscambio multimediale accessibile sincronizzato (SAMI)
- SAMI (Synchronized Accessible Media Interchange), file
- SAMI (interscambio multimediale accessibile sincronizzato), file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d310ab3eb3016937f148ebb26e810dd9e6e6b6b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856266"
---
# <a name="about-sami-files"></a><span data-ttu-id="b047a-112">Informazioni sui file SAMI</span><span class="sxs-lookup"><span data-stu-id="b047a-112">About SAMI Files</span></span>

<span data-ttu-id="b047a-113">I file SAMI sono file di testo con estensione SMI o Sami.</span><span class="sxs-lookup"><span data-stu-id="b047a-113">SAMI files are text files that have an .smi or .sami file name extension.</span></span> <span data-ttu-id="b047a-114">Contengono le stringhe di testo usate per le didascalie chiuse, i sottotitoli e le descrizioni audio sincronizzati.</span><span class="sxs-lookup"><span data-stu-id="b047a-114">They contain the text strings used for synchronized closed captions, subtitles, and audio descriptions.</span></span> <span data-ttu-id="b047a-115">Specificano anche i parametri di intervallo usati dal controllo Media Player Windows per sincronizzare il testo della didascalia chiusa con contenuto audio o video.</span><span class="sxs-lookup"><span data-stu-id="b047a-115">They also specify the timing parameters used by the Windows Media Player control to synchronize closed caption text with audio or video content.</span></span> <span data-ttu-id="b047a-116">Quando un file multimediale digitale raggiunge un'ora designata nel file SAMI, il testo viene modificato di conseguenza nell'area di visualizzazione didascalia chiusa della pagina Web.</span><span class="sxs-lookup"><span data-stu-id="b047a-116">When a digital media file reaches a time designated in the SAMI file, the text changes accordingly in the closed caption display area of the webpage.</span></span>

<span data-ttu-id="b047a-117">Oltre a un semplice editor di testo, ad esempio Microsoft Notepad, non è necessario un software speciale per creare un file SAMI.</span><span class="sxs-lookup"><span data-stu-id="b047a-117">Other than a simple text editor (such as Microsoft Notepad), special software is not required to create a SAMI file.</span></span> <span data-ttu-id="b047a-118">SAMI e HTML condividono elementi comuni, ad esempio i <HEAD> <BODY> tag e.</span><span class="sxs-lookup"><span data-stu-id="b047a-118">SAMI and HTML share common elements, such as the <HEAD> and <BODY> tags.</span></span> <span data-ttu-id="b047a-119">Come in HTML, i tag usati nei file SAMI devono essere sempre usati in coppie.</span><span class="sxs-lookup"><span data-stu-id="b047a-119">As in HTML, tags used in SAMI files must always be used in pairs.</span></span> <span data-ttu-id="b047a-120">Ad esempio, un elemento BODY inizia con un <BODY> tag e deve terminare sempre con un </BODY> tag.</span><span class="sxs-lookup"><span data-stu-id="b047a-120">For example, a BODY element begins with a <BODY> tag and must always end with a </BODY> tag.</span></span>

<span data-ttu-id="b047a-121">Un file SAMI di base richiede tre tag fondamentali: <SAMI> , <HEAD> e <BODY> .</span><span class="sxs-lookup"><span data-stu-id="b047a-121">A basic SAMI file requires three fundamental tags: <SAMI>, <HEAD>, and <BODY>.</span></span>

<span data-ttu-id="b047a-122">Il <SAMI> tag identifica il documento come documento Sami, in modo che le altre applicazioni possano riconoscere il formato del file.</span><span class="sxs-lookup"><span data-stu-id="b047a-122">The <SAMI> tag identifies the document as a SAMI document so other applications can recognize its file format.</span></span>

<span data-ttu-id="b047a-123">Tra i tag <HEAD> e </HEAD> si definiscono le linee guida di base e altre informazioni sul formato per il documento Sami, ad esempio il titolo del documento, le informazioni generali e le proprietà di stile per i sottotitoli codificati.</span><span class="sxs-lookup"><span data-stu-id="b047a-123">Between the <HEAD> and </HEAD> tags, you define basic guidelines and other format information for the SAMI document, such as the document title, general information, and style properties for closed captions.</span></span> <span data-ttu-id="b047a-124">Analogamente al codice HTML, il contenuto dichiarato all'interno dell'elemento HEAD non viene visualizzato come output.</span><span class="sxs-lookup"><span data-stu-id="b047a-124">Like HTML, content declared within the HEAD element does not display as output.</span></span>

<span data-ttu-id="b047a-125">Gli elementi e gli attributi definiti tra i tag <BODY> e </BODY> visualizzano il contenuto visualizzato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="b047a-125">Elements and attributes defined between the <BODY> and </BODY> tags display content seen by the user.</span></span> <span data-ttu-id="b047a-126">In SAMI l'elemento BODY contiene i parametri per la sincronizzazione e le stringhe di testo utilizzate per le didascalie chiuse.</span><span class="sxs-lookup"><span data-stu-id="b047a-126">In SAMI, the BODY element contains the parameters for synchronization and the text strings used for closed captions.</span></span>

<span data-ttu-id="b047a-127">Definito all'interno dell'elemento HEAD, l'elemento STYLE fornisce la funzionalità aggiuntiva in SAMI.</span><span class="sxs-lookup"><span data-stu-id="b047a-127">Defined within the HEAD element, the STYLE element provides for added functionality in SAMI.</span></span> <span data-ttu-id="b047a-128">Tra i tag <STYLE> e </STYLE> è possibile definire diversi selettori CSS (CSS) per lo stile e il layout.</span><span class="sxs-lookup"><span data-stu-id="b047a-128">Between the <STYLE> and </STYLE> tags, you can define several Cascading Style Sheet (CSS) selectors for style and layout.</span></span> <span data-ttu-id="b047a-129">È possibile personalizzare le proprietà di stile, ad esempio tipi di carattere, dimensioni e allineamento, per offrire un'esperienza utente avanzata e promuovere anche l'accessibilità.</span><span class="sxs-lookup"><span data-stu-id="b047a-129">Style properties such as fonts, sizes, and alignments can be customized to provide a rich user experience while also promoting accessibility.</span></span> <span data-ttu-id="b047a-130">Ad esempio, la definizione di una classe di stile del tipo di carattere testo di grandi dimensioni può migliorare la leggibilità per gli utenti che hanno difficoltà a leggere testo di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="b047a-130">For example, defining a large text font style class can improve the readability for users who have difficulty reading small text.</span></span> <span data-ttu-id="b047a-131">Inoltre, definendo diverse classi di linguaggio, è possibile aiutare gli utenti internazionali a comprendere meglio il contenuto multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="b047a-131">In addition, by defining several different language classes, you can help international users better understand the digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b047a-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b047a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b047a-133">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="b047a-133">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




