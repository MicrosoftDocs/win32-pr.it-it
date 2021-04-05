---
title: Utilizzo dell'applicazione desktop di esempio
description: Utilizzo dell'applicazione desktop di esempio
ms.assetid: 5e3e5283-9e27-4f6a-93a9-84d84f2e875a
keywords:
- Windows Media Gestione dispositivi, esempi
- Gestione dispositivi, esempi
- applicazioni desktop, esempi
- Windows Media Gestione dispositivi, esempio di applicazione desktop
- Esempio di Gestione dispositivi, applicazione desktop
- esempi, applicazioni desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd511ea5241f458d2cd926dc8fb2f3681757ff8b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708746"
---
# <a name="using-the-sample-desktop-application"></a><span data-ttu-id="e8115-109">Utilizzo dell'applicazione desktop di esempio</span><span class="sxs-lookup"><span data-stu-id="e8115-109">Using the Sample Desktop Application</span></span>

<span data-ttu-id="e8115-110">L'applicazione desktop di esempio è una finestra di base a due riquadri, come Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="e8115-110">The sample desktop application is a basic two-paned window somewhat like Windows Explorer.</span></span> <span data-ttu-id="e8115-111">Consente di esplorare il contenuto di un dispositivo, usando una visualizzazione albero delle cartelle nel riquadro sinistro e i file nel riquadro di destra.</span><span class="sxs-lookup"><span data-stu-id="e8115-111">It allows you to browse the contents of a device, using a tree view display of folders in the left pane, and files in the right pane.</span></span> <span data-ttu-id="e8115-112">La radice di ogni albero di cartelle viene considerata logicamente un dispositivo diverso, anche se alcuni dispositivi potrebbero rappresentarsi come diversi oggetti (uno per ogni archiviazione radice).</span><span class="sxs-lookup"><span data-stu-id="e8115-112">The root of each folder tree is logically considered a different device, although some devices might represent themselves as several objects (one for each root storage).</span></span> <span data-ttu-id="e8115-113">Per leggere le proprietà di base di una cartella o di un file, fare clic con il pulsante destro del mouse sull'oggetto e scegliere **Proprietà**.</span><span class="sxs-lookup"><span data-stu-id="e8115-113">To read the basic properties of either a folder or a file, right-click the object and select **Properties**.</span></span>

<span data-ttu-id="e8115-114">È possibile eliminare i file nel dispositivo selezionando un file nel riquadro destro e selezionando **Elimina** dal menu **file** .</span><span class="sxs-lookup"><span data-stu-id="e8115-114">You can delete files on the device by selecting a file in the right pane and selecting **Delete** on the **File** menu.</span></span> <span data-ttu-id="e8115-115">Per aggiungere file multimediali al dispositivo, è possibile trascinare i file dal desktop nel riquadro destro del programma.</span><span class="sxs-lookup"><span data-stu-id="e8115-115">To add media files to the device, you can drag files from the desktop onto the right pane of the program.</span></span> <span data-ttu-id="e8115-116">Si noti che i file devono essere di un formato multimediale supportato dal dispositivo. i file di formati non accettabili (file non multimediali, ad esempio file con estensione txt o formati multimediali non supportati dal dispositivo) non verranno inviati al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8115-116">Note that files must be of a media format supported by the device; files of unacceptable formats (non-media files such as .txt files, or media formats not supported by the device) will not be sent to the device.</span></span> <span data-ttu-id="e8115-117">(Si noti che questa restrizione è il programma; Windows Media Gestione dispositivi consente di inviare qualsiasi file a un dispositivo se viene accettato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8115-117">(Note that this restriction is the program's; Windows Media Device Manager enables you to send any file to a device if the device will accept it.)</span></span>

<span data-ttu-id="e8115-118">Per acquisire gli eventi di callback inviati all'interfaccia [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) , è necessario selezionare l'opzione "utilizza interfaccia operativa" nel menu **Opzioni** .</span><span class="sxs-lookup"><span data-stu-id="e8115-118">To capture callback events sent to the [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) interface, you must check the "Use Operation Interface" option in the **Options** menu.</span></span>

<span data-ttu-id="e8115-119">Il menu **Opzioni** consente inoltre di scegliere se utilizzare più interfacce avanzate con le funzionalità supportate dai dispositivi avanzati.</span><span class="sxs-lookup"><span data-stu-id="e8115-119">The **Options** menu also enables you to choose whether to use several more advanced interfaces with features supported by advanced devices.</span></span>

<span data-ttu-id="e8115-120">Nel menu **contenitori** sono disponibili opzioni che consentono di creare una playlist o un album.</span><span class="sxs-lookup"><span data-stu-id="e8115-120">The **Containers** menu has options to allow you to create a playlist or an album.</span></span> <span data-ttu-id="e8115-121">Per creare una playlist, selezionare uno o più brani sul dispositivo e fare clic su **Crea playlist** nel menu **contenitori** .</span><span class="sxs-lookup"><span data-stu-id="e8115-121">To create a playlist, select one or more songs on the device and click **Create Playlist** on the **Containers** menu.</span></span> <span data-ttu-id="e8115-122">Questa funzionalità funziona solo nei dispositivi MTP, perché il codice supporta solo la creazione di un file di playlist "virtuale".</span><span class="sxs-lookup"><span data-stu-id="e8115-122">This feature only works on MTP devices, because the code only supports the creation of an "virtual" playlist file.</span></span> <span data-ttu-id="e8115-123">Una playlist virtuale è una playlist specificata solo dai valori dei metadati, anziché da un file fisico, ad esempio un file WPL. Per usare questa funzionalità, il dispositivo deve supportare playlist vuote.</span><span class="sxs-lookup"><span data-stu-id="e8115-123">(A virtual playlist is a playlist that is specified only by metadata values, rather than by a physical file, for example a WPL file.) The device must support empty playlists to use this feature.</span></span>

<span data-ttu-id="e8115-124">Per creare un album (una playlist con un'immagine associata), selezionare uno o più brani sul dispositivo e fare clic su **Crea album** nel menu **contenitori** .</span><span class="sxs-lookup"><span data-stu-id="e8115-124">To create an album (a playlist with an associated image), select one or more songs on the device and click **Create Album** on the **Containers** menu.</span></span> <span data-ttu-id="e8115-125">Una finestra di dialogo consente di selezionare un file di immagine nel computer da associare all'album.</span><span class="sxs-lookup"><span data-stu-id="e8115-125">A dialog box allows you to browse to a picture file on your computer to associate with the album.</span></span> <span data-ttu-id="e8115-126">Analogamente al modo in cui vengono create le playlist, l'applicazione crea un file di album "vuoto"; Se il dispositivo non supporta gli album vuoti, la funzionalità non funzionerà.</span><span class="sxs-lookup"><span data-stu-id="e8115-126">Similarly to the way it creates playlists, the application creates an "empty" album file; if the device does not support empty albums, this feature will not work.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8115-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e8115-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8115-128">**Applicazione desktop di esempio**</span><span class="sxs-lookup"><span data-stu-id="e8115-128">**Sample Desktop Application**</span></span>](sample-desktop-application.md)
</dt> </dl>

 

 




