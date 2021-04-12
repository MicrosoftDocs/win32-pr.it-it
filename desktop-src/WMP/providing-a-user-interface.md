---
title: Fornire un'interfaccia utente
description: Fornire un'interfaccia utente
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- Plug-in di Windows Media Player, pagine delle proprietà
- plug-in, pagine delle proprietà
- plug-in di elaborazione dei segnali digitali, pagine delle proprietà
- Plug-in DSP, pagine delle proprietà
- plug-in per l'elaborazione di segnali digitali, interfaccia utente
- Plug-in DSP, interfaccia utente
- pagine delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d708d1256faf7096d15a7596a9635a33173d22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221838"
---
# <a name="providing-a-user-interface"></a><span data-ttu-id="4335b-110">Fornire un'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="4335b-110">Providing a User Interface</span></span>

<span data-ttu-id="4335b-111">I plug-in DSP possono fornire una pagina delle proprietà per creare un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="4335b-111">DSP plug-ins can provide a property page to create a user interface.</span></span> <span data-ttu-id="4335b-112">A tale scopo, il plug-in deve includere un oggetto pagina delle proprietà che fornisce un'implementazione di un'interfaccia **IPropertyPage** .</span><span class="sxs-lookup"><span data-stu-id="4335b-112">To do this, the plug-in must include a property page object that provides an implementation of an **IPropertyPage** interface.</span></span> <span data-ttu-id="4335b-113">L'oggetto plug-in DSP deve implementare **ISpecifyPropertyPages:: GetPages**, che consente a Windows Media Player di individuare e identificare la pagina delle proprietà corretta per il plug-in.</span><span class="sxs-lookup"><span data-stu-id="4335b-113">The DSP plug-in object must implement **ISpecifyPropertyPages::GetPages**, which allows Windows Media Player to locate and identify the correct property page for the plug-in.</span></span>

<span data-ttu-id="4335b-114">**Visualizzazione di un'immagine di stato**</span><span class="sxs-lookup"><span data-stu-id="4335b-114">**Displaying a Status Graphic**</span></span>

<span data-ttu-id="4335b-115">I plug-in DSP possono visualizzare un piccolo grafico o una serie di elementi grafici nell'area stato Media Player Windows per notificare all'utente che è attivo un plug-in.</span><span class="sxs-lookup"><span data-stu-id="4335b-115">DSP plug-ins can display a small graphic, or series of graphics, in the Windows Media Player status area to notify the user that a plug-in is active.</span></span> <span data-ttu-id="4335b-116">Per supportare questa funzionalità, il plug-in deve implementare l'interfaccia **IPropertyBag** .</span><span class="sxs-lookup"><span data-stu-id="4335b-116">To support this feature, the plug-in must implement the **IPropertyBag** interface.</span></span> <span data-ttu-id="4335b-117">Windows Media Player chiama **IPropertyBag:: Read**, fornendo un puntatore al nome di proprietà richiesto "IconStreams", che fa distinzione tra maiuscole e minuscole, e un puntatore a una struttura **Variant** che riceve i dati per l'elemento grafico.</span><span class="sxs-lookup"><span data-stu-id="4335b-117">Windows Media Player calls **IPropertyBag::Read**, providing a pointer to the requested property name "IconStreams", which is case-sensitive, and a pointer to a **VARIANT** structure that receives the data for the graphic.</span></span> <span data-ttu-id="4335b-118">Il plug-in crea un oggetto **IStream** (o un SAFEARRAY di oggetti **IStream** se sono presenti più elementi grafici), quindi carica i dati grafici, incluse le informazioni di intestazione, nel flusso, quindi restituisce un puntatore all'oggetto **IStream** usando il membro **punkVal** della struttura **Variant** .</span><span class="sxs-lookup"><span data-stu-id="4335b-118">The plug-in creates an **IStream** object (or a SAFEARRAY of **IStream** objects if there are multiple graphics), then loads the graphic data, including header information, into the stream, and then returns a pointer to the **IStream** object using the **punkVal** member of the **VARIANT** structure.</span></span> <span data-ttu-id="4335b-119">Se il plug-in fornisce un solo elemento grafico, specifica il membro **VT** della struttura **Variant** come VT \_ sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="4335b-119">If the plug-in supplies only one graphic, it specifies the **vt** member of the **VARIANT** structure as VT\_UNKNOWN.</span></span> <span data-ttu-id="4335b-120">Se il plug-in fornisce più oggetti di **IStream** grafici utilizzando un SAFEARRAY, specifica il membro **VT** della struttura **Variant** come matrice VT \_ .</span><span class="sxs-lookup"><span data-stu-id="4335b-120">If the plug-in supplies multiple graphic **IStream** objects using a SAFEARRAY, it specifies the **vt** member of the **VARIANT** structure as VT\_ARRAY.</span></span>

<span data-ttu-id="4335b-121">La grafica può essere archiviata in diversi formati di file, tra cui:</span><span class="sxs-lookup"><span data-stu-id="4335b-121">Graphics can be stored in a variety of file formats, including:</span></span>

<span data-ttu-id="4335b-122">**BMP**</span><span class="sxs-lookup"><span data-stu-id="4335b-122">**BMP**</span></span>

<span data-ttu-id="4335b-123">Le immagini bitmap di Microsoft Windows non sono compresse.</span><span class="sxs-lookup"><span data-stu-id="4335b-123">Microsoft Windows Bitmap images are uncompressed.</span></span>

<span data-ttu-id="4335b-124">**JPEG**</span><span class="sxs-lookup"><span data-stu-id="4335b-124">**JPEG**</span></span>

<span data-ttu-id="4335b-125">Formato di immagine compresso usato comunemente per le pagine Web.</span><span class="sxs-lookup"><span data-stu-id="4335b-125">Compressed image format commonly used for webpages.</span></span> <span data-ttu-id="4335b-126">In genere i file di formato JPEG hanno estensioni di file jpg.</span><span class="sxs-lookup"><span data-stu-id="4335b-126">JPEG format files usually have .jpg file name extensions.</span></span>

<span data-ttu-id="4335b-127">**GIF**</span><span class="sxs-lookup"><span data-stu-id="4335b-127">**GIF**</span></span>

<span data-ttu-id="4335b-128">Formato di immagine compresso usato comunemente per le pagine Web.</span><span class="sxs-lookup"><span data-stu-id="4335b-128">Compressed image format commonly used for webpages.</span></span>

<span data-ttu-id="4335b-129">**PNG**</span><span class="sxs-lookup"><span data-stu-id="4335b-129">**PNG**</span></span>

<span data-ttu-id="4335b-130">Formato di immagine compresso usato comunemente per le pagine Web.</span><span class="sxs-lookup"><span data-stu-id="4335b-130">Compressed image format commonly used for webpages.</span></span>

<span data-ttu-id="4335b-131">Le dimensioni massime per la grafica plug-in DSP sono di 38 pixel di larghezza e 14 pixel di altezza.</span><span class="sxs-lookup"><span data-stu-id="4335b-131">The maximum dimensions for DSP plug-in graphics are 38 pixels wide and 14 pixels high.</span></span>

<span data-ttu-id="4335b-132">Il flusso di byte **IStream** contenente l'elemento grafico di stato deve includere informazioni di intestazione.</span><span class="sxs-lookup"><span data-stu-id="4335b-132">The **IStream** byte stream containing the status graphic must include header information.</span></span> <span data-ttu-id="4335b-133">Senza informazioni di intestazione, Windows Media Player non è in grado di identificare correttamente il tipo di grafico e pertanto non caricherà l'immagine.</span><span class="sxs-lookup"><span data-stu-id="4335b-133">Without header information, Windows Media Player cannot properly identify the type of graphic and therefore will not load the image.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4335b-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4335b-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4335b-135">**Panoramica per gli sviluppatori di plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="4335b-135">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




