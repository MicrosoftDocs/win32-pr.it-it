---
title: Informazioni sugli URL SAMI
description: Informazioni sugli URL SAMI
ms.assetid: 6898a0d5-cfd0-4ba5-8cd1-907cf110667c
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
- SAMI (Synchronized Accessible Media Interchange), URL
- SAMI (interscambio multimediale accessibile sincronizzato), URL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7a41e70d0239b9bdac7d12f9a2dd2f75be15b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221246"
---
# <a name="about-sami-urls"></a><span data-ttu-id="3a56c-114">Informazioni sugli URL SAMI</span><span class="sxs-lookup"><span data-stu-id="3a56c-114">About SAMI URLs</span></span>

<span data-ttu-id="3a56c-115">I file SAMI possono essere associati a file multimediali digitali usando un singolo URL.</span><span class="sxs-lookup"><span data-stu-id="3a56c-115">SAMI files can be associated with digital media files by using a single URL.</span></span> <span data-ttu-id="3a56c-116">Questa operazione viene eseguita tramite *il parametro dell'URL Sami* .</span><span class="sxs-lookup"><span data-stu-id="3a56c-116">This is accomplished by using *the sami* URL parameter.</span></span> <span data-ttu-id="3a56c-117">Il parametro URL è preceduto dall'URL di base e da un?</span><span class="sxs-lookup"><span data-stu-id="3a56c-117">The URL parameter is preceded by the base URL and a ?</span></span> <span data-ttu-id="3a56c-118">.</span><span class="sxs-lookup"><span data-stu-id="3a56c-118">character.</span></span> <span data-ttu-id="3a56c-119">Un URL con un parametro *Sami* segue questa sintassi:</span><span class="sxs-lookup"><span data-stu-id="3a56c-119">A URL with a *sami* parameter follows this syntax:</span></span>

<span data-ttu-id="3a56c-120">*URL*? *Sami* = *captionsURL*.</span><span class="sxs-lookup"><span data-stu-id="3a56c-120">*URL*?*sami*=*captionsURL*.</span></span>

<span data-ttu-id="3a56c-121">Il valore del parametro URL segue il nome del parametro e un segno di uguale, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="3a56c-121">The value of the URL parameter follows the parameter name and an equals sign, as in the following example:</span></span>


```C++
https://proseware.com/samitest.wma?sami=https://acc.proseware.com/test.smi

```



<span data-ttu-id="3a56c-122">Questa sintassi dell'URL viene comunemente utilizzata in un collegamento ipertestuale o in un metafile di Windows Media per collegarsi direttamente ai percorsi del file multimediale digitale e del file SAMI.</span><span class="sxs-lookup"><span data-stu-id="3a56c-122">This URL syntax is commonly used in a hyperlink or a Windows Media metafile to link directly to the locations of both the digital media file and the SAMI file.</span></span> <span data-ttu-id="3a56c-123">Quando l'utente fa clic sul collegamento ipertestuale, Windows Media Player viene avviato in modalità completa e riproduce il contenuto multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="3a56c-123">When the user clicks on the hyperlink, Windows Media Player launches in full mode and plays the digital media content.</span></span>

<span data-ttu-id="3a56c-124">Se il parametro dell'URL *Sami* non è specificato, Windows Media Player cerca un file Sami che si trova nella stessa posizione del file multimediale digitale e che ha lo stesso nome di file, ad eccezione dell'estensione del nome file, che deve essere. SMI.</span><span class="sxs-lookup"><span data-stu-id="3a56c-124">If the *sami* URL parameter is not specified, Windows Media Player will look for a SAMI file that is in the same location as the digital media file and that has the same file name except for the file name extension, which must be .smi.</span></span> <span data-ttu-id="3a56c-125">Se è presente un file di questo tipo, questo verrà aperto automaticamente se nel lettore è stata abilitata la visualizzazione della didascalia.</span><span class="sxs-lookup"><span data-stu-id="3a56c-125">If such a file is present, it will be opened automatically if caption display has been enabled in the Player.</span></span>

<span data-ttu-id="3a56c-126">Le didascalie chiuse sono abilitate in Windows Media Player facendo clic sul menu **Riproduci** , quindi facendo clic su **didascalie e sottotitoli** e quindi **su on**.</span><span class="sxs-lookup"><span data-stu-id="3a56c-126">Closed captions are enabled in Windows Media Player by clicking the **Play** menu, then clicking **Captions and Subtitles**, and then clicking **On**.</span></span> <span data-ttu-id="3a56c-127">Se le didascalie chiuse sono abilitate, le didascalie contenute nel file SAMI verranno visualizzate durante la riproduzione dell'elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="3a56c-127">If closed captions are enabled, the captions contained in the SAMI file will display while the media item plays.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a56c-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a56c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a56c-129">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="3a56c-129">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




