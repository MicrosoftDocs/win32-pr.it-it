---
title: Informazioni sui plug-in di conversione
description: Informazioni sui plug-in di conversione
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Windows Media Player, plug-in di conversione
- Plug-in di Windows Media Player, conversione
- plug-in, conversione
- plug-in di conversione, informazioni
- Advanced Systems Format (ASF)
- ASF (formato avanzato dei sistemi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6e2a8fa41b657a593dc03082f871503b53eba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708053"
---
# <a name="about-conversion-plug-ins"></a><span data-ttu-id="8a8e5-109">Informazioni sui plug-in di conversione</span><span class="sxs-lookup"><span data-stu-id="8a8e5-109">About Conversion Plug-ins</span></span>

<span data-ttu-id="8a8e5-110">È possibile creare un plug-in di Windows Media Player per convertire i file multimediali digitali creati usando le tecnologie non fornite da Microsoft, nel formato ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="8a8e5-110">You can create a Windows Media Player plug-in to convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).</span></span>

<span data-ttu-id="8a8e5-111">I plug-in di conversione sono oggetti Component Object Model (COM) che vengono inseriti in un pacchetto e distribuiti come file eseguibili (exe).</span><span class="sxs-lookup"><span data-stu-id="8a8e5-111">Conversion plug-ins are Component Object Model (COM) objects that are packaged and distributed as executable (.exe) files.</span></span> <span data-ttu-id="8a8e5-112">Windows Media Player crea un'istanza dei plug-in di conversione per convertire i formati multimediali digitali di terze parti negli scenari seguenti:</span><span class="sxs-lookup"><span data-stu-id="8a8e5-112">Windows Media Player instantiates conversion plug-ins to convert third-party digital media formats in the following scenarios:</span></span>

-   <span data-ttu-id="8a8e5-113">Il contenuto multimediale digitale viene copiato nel computer da un dispositivo portatile.</span><span class="sxs-lookup"><span data-stu-id="8a8e5-113">Digital media content is copied to the computer from a portable device.</span></span>
-   <span data-ttu-id="8a8e5-114">Il contenuto multimediale digitale viene aggiunto alla libreria usando **IWMPMediaCollection:: Add**.</span><span class="sxs-lookup"><span data-stu-id="8a8e5-114">Digital media content is added to the library by using **IWMPMediaCollection::add**.</span></span>
-   <span data-ttu-id="8a8e5-115">Il contenuto multimediale digitale viene aggiunto alla libreria usando la funzionalità di ricerca di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8a8e5-115">Digital media content is added to the library by using the search feature of Windows Media Player.</span></span>
-   <span data-ttu-id="8a8e5-116">Il contenuto multimediale digitale viene aggiunto alla libreria dalla funzionalità di monitoraggio delle cartelle di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8a8e5-116">Digital media content is added to the library by the folder monitoring feature of Windows Media Player.</span></span>
-   <span data-ttu-id="8a8e5-117">Il contenuto multimediale digitale viene aggiunto all'elenco di sincronizzazione quando l'utente trascina un file e lo rilascia.</span><span class="sxs-lookup"><span data-stu-id="8a8e5-117">Digital media content is added to the sync list when the user drags and drops a file.</span></span>

<span data-ttu-id="8a8e5-118">Dopo che Windows Media Player crea un'istanza di un plug-in di conversione, il plug-in deve convertire il file fornito in ASF o WMA e aggiungere i relativi metadati.</span><span class="sxs-lookup"><span data-stu-id="8a8e5-118">After Windows Media Player creates an instance of a conversion plug-in, the plug-in must convert the supplied file to ASF or WMA and add relevant metadata.</span></span> <span data-ttu-id="8a8e5-119">Non usare il plug-in di conversione per la transcodifica del file. Il plug-in deve quindi copiare il file convertito nella cartella specificata e restituire il percorso del nuovo file a Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8a8e5-119">(Do not use the conversion plug-in to transcode the file.) The plug-in must then copy the converted file to the specified folder and return the path to the new file to Windows Media Player.</span></span>

<span data-ttu-id="8a8e5-120">I plug-in di conversione devono implementare l'interfaccia **IWMPConvert** .</span><span class="sxs-lookup"><span data-stu-id="8a8e5-120">Conversion plug-ins must implement the **IWMPConvert** interface.</span></span> <span data-ttu-id="8a8e5-121">Vedere informazioni [di riferimento sulla programmazione di plug-in di conversione](conversion-plug-ins-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="8a8e5-121">See [Conversion Plug-ins Programming Reference](conversion-plug-ins-programming-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a8e5-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a8e5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a8e5-123">**Informazioni sul processo di conversione**</span><span class="sxs-lookup"><span data-stu-id="8a8e5-123">**About the Conversion Process**</span></span>](about-the-conversion-process.md)
</dt> <dt>

[<span data-ttu-id="8a8e5-124">**Aggiunta di metadati ai file convertiti**</span><span class="sxs-lookup"><span data-stu-id="8a8e5-124">**Adding Metadata to Converted Files**</span></span>](adding-metadata-to-converted-files.md)
</dt> <dt>

[<span data-ttu-id="8a8e5-125">**Plug-in di conversione di Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="8a8e5-125">**Windows Media Player Conversion Plug-ins**</span></span>](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




