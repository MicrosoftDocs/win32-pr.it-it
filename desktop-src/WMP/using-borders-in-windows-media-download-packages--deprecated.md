---
title: Uso dei bordi nei pacchetti di download di Windows Media (deprecato)
description: Uso dei bordi nei pacchetti di download di Windows Media (deprecato)
ms.assetid: d3961c5f-8cce-439d-9a13-41be2f45d92c
keywords:
- Metafile di Windows Media, pacchetti di download di Windows Media
- Windows Media Player, pacchetti di download di Windows Media
- Metafile, pacchetti di download di Windows Media
- Windows Media, pacchetti di download di Windows Media
- bordi, informazioni
- Pacchetti di download di Windows Media, bordi
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 87f7d0fec341bb79bfe9b8dd739b63a9ba3a66ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396162"
---
# <a name="using-borders-in-windows-media-download-packages-deprecated"></a><span data-ttu-id="9c3cf-109">Uso dei bordi nei pacchetti di download di Windows Media (deprecato)</span><span class="sxs-lookup"><span data-stu-id="9c3cf-109">Using Borders in Windows Media Download Packages (deprecated)</span></span>

<span data-ttu-id="9c3cf-110">Questa pagina documenta una funzionalità che potrebbe non essere disponibile nelle versioni future di Windows Media Player e Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="9c3cf-111">I bordi consentono di creare un'interfaccia utente grafica personalizzata per il contenuto in pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-111">Borders enable you to create a customized graphical user interface for your packaged content.</span></span> <span data-ttu-id="9c3cf-112">Il bordo può includere elementi quali immagini, controlli interattivi e collegamenti a siti Web.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-112">The border can include elements such as images, interactive controls, and links to websites.</span></span> <span data-ttu-id="9c3cf-113">È possibile usare i bordi nei casi in cui si vuole aggiungere altro valore al contenuto incluso nel pacchetto, ad esempio per la personalizzazione o la pubblicità.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-113">You can use borders in cases where you want to add additional value to your packaged content, such as for branding or advertising.</span></span> <span data-ttu-id="9c3cf-114">Dopo che gli utenti hanno scaricato e aperto il pacchetto di download di Windows Media, Windows Media Player visualizza automaticamente il bordo personalizzato quando riproduce il contenuto in pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-114">After users download and open your Windows Media Download package, Windows Media Player automatically displays your custom border when it plays the packaged content.</span></span>

<span data-ttu-id="9c3cf-115">Diversamente da un'interfaccia personalizzata, che consente agli utenti di sostituire completamente l'interfaccia utente di Windows Media Player, viene visualizzato un bordo solo nel riquadro **ora di riproduzione** del lettore in modalità piena.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-115">Unlike a skin, which enables users to completely replace the Windows Media Player user interface, a border is displayed only in the **Now Playing** pane of the full mode Player.</span></span> <span data-ttu-id="9c3cf-116">Tuttavia, per creare i bordi vengono usati anche gli stessi strumenti e tecnologie usati per creare le interfacce.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-116">However, the same tools and technologies that you use to create skins are also used to create borders.</span></span> <span data-ttu-id="9c3cf-117">Nella figura seguente viene illustrato un bordo.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-117">The following illustration shows a border.</span></span>

![bordo visualizzato in Windows Media Player 10](images/border-v10.png)

<span data-ttu-id="9c3cf-119">È importante comprendere le tecniche di base per la creazione di un'interfaccia prima di provare a creare un bordo.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-119">It is important to understand the basic techniques for creating a skin before attempting to create a border.</span></span> <span data-ttu-id="9c3cf-120">La programmazione di bordi viene eseguita utilizzando due linguaggi di programmazione: Extensible Markup Language (XML) e Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-120">Border programming is accomplished using two programming languages: Extensible Markup Language (XML) and Microsoft JScript.</span></span> <span data-ttu-id="9c3cf-121">XML viene utilizzato per definire elementi di interfaccia quali pulsanti, dispositivi di scorrimento e caselle di testo.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-121">XML is used to define interface elements such as buttons, sliders, and text boxes.</span></span> <span data-ttu-id="9c3cf-122">Non è necessario comprendere tutti i dettagli di XML poiché non è necessario scrivere nuovi elementi di codice XML. è possibile utilizzare semplicemente quelli forniti da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-122">You don't need to understand all the details of XML since you don't have to write new XML code elements; you can simply use the ones provided by Windows Media Player.</span></span> <span data-ttu-id="9c3cf-123">Sebbene non sia necessario per la creazione di bordi, JScript può essere utilizzato per fornire funzionalità aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-123">Although JScript is not required for creating borders, it can be used to provide additional functionality.</span></span>

<span data-ttu-id="9c3cf-124">Un file di bordo compresso con estensione WMZ include un file di definizione del bordo con estensione del nome di file WMS e tutti i file di immagine utilizzati all'interno del bordo.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-124">A compressed border file with a .wmz file name extension includes a border definition file with a .wms file name extension and all the image files used within the border.</span></span>

<span data-ttu-id="9c3cf-125">Per includere un bordo in un pacchetto di download di Windows Media, è sufficiente creare un bordo e fare riferimento a tale bordo in una playlist Windows Media Metafile.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-125">To include a border in a Windows Media Download package, simply create a border and reference that border in a Windows Media metafile playlist.</span></span> <span data-ttu-id="9c3cf-126">Il file di bordo viene caricato in Windows Media Player dopo che il lettore analizza il metafile e interpreta l'elemento **Skin** che fa riferimento al bordo.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-126">The border file is loaded into Windows Media Player after the Player parses the metafile and interprets the **SKIN** element that references the border.</span></span> <span data-ttu-id="9c3cf-127">L'elemento **Skin** viene usato solo per i bordi e l'attributo href dell'elemento **Skin** può fare riferimento a una sola interfaccia per ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="9c3cf-127">The **SKIN** element is used only for borders, and the HREF attribute of the **SKIN** element can reference only one skin for each package.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c3cf-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9c3cf-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c3cf-129">**Bordi per Windows Media Player (deprecato)**</span><span class="sxs-lookup"><span data-stu-id="9c3cf-129">**Borders for Windows Media Player (deprecated)**</span></span>](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[<span data-ttu-id="9c3cf-130">**Pacchetti di download di Windows Media (deprecato)**</span><span class="sxs-lookup"><span data-stu-id="9c3cf-130">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> <dt>

[<span data-ttu-id="9c3cf-131">**Interfacce di Media Player Windows**</span><span class="sxs-lookup"><span data-stu-id="9c3cf-131">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




