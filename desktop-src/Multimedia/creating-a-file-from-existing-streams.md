---
title: Creazione di un file da flussi esistenti
description: Creazione di un file da flussi esistenti
ms.assetid: 5149a766-7809-42b7-8e5c-b67b847b9218
keywords:
- AVISave (funzione)
- AVISaveV (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc422d2170ccd49b8a9746666db7ebbcd7dff14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955391"
---
# <a name="creating-a-file-from-existing-streams"></a><span data-ttu-id="170ac-105">Creazione di un file da flussi esistenti</span><span class="sxs-lookup"><span data-stu-id="170ac-105">Creating a File from Existing Streams</span></span>

<span data-ttu-id="170ac-106">Un modo per creare un file che contiene flussi di dati consiste nel combinare i flussi esistenti in un nuovo file.</span><span class="sxs-lookup"><span data-stu-id="170ac-106">One way to create a file that contains data streams is to combine existing streams into a new file.</span></span> <span data-ttu-id="170ac-107">I flussi che forniscono i dati per il nuovo file possono risiedere in memoria o in uno o più file.</span><span class="sxs-lookup"><span data-stu-id="170ac-107">The streams that provide data for the new file can reside in memory or in one or more files.</span></span>

<span data-ttu-id="170ac-108">È possibile compilare un file da più flussi usando la funzione [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) .</span><span class="sxs-lookup"><span data-stu-id="170ac-108">You can build a file from several streams by using the [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) function.</span></span> <span data-ttu-id="170ac-109">Questa funzione crea un file e scrive nel file i flussi di dati specificati nella sequenza chiamante.</span><span class="sxs-lookup"><span data-stu-id="170ac-109">This function creates a file and writes the data streams specified in its calling sequence to the file.</span></span> <span data-ttu-id="170ac-110">La sequenza chiamante per **AVISave** usa un numero variabile di argomenti che includono interfacce per i flussi combinati nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="170ac-110">The calling sequence for **AVISave** uses a variable number of arguments that include interfaces for the streams combined in the new file.</span></span>

<span data-ttu-id="170ac-111">È anche possibile combinare i flussi di dati in un nuovo file usando la funzione [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) .</span><span class="sxs-lookup"><span data-stu-id="170ac-111">You can also combine data streams in a new file by using the [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) function.</span></span> <span data-ttu-id="170ac-112">Questa funzione fornisce la stessa funzionalità di **AVISave**, ma quando si usa **AVISaveV**, l'applicazione specifica i flussi di dati come una matrice, non come un numero variabile di argomenti.</span><span class="sxs-lookup"><span data-stu-id="170ac-112">This function provides the same functionality as **AVISave**, but when you use **AVISaveV**, your application specifies the data streams as an array, not as a variable number of arguments.</span></span>

<span data-ttu-id="170ac-113">È possibile creare una finestra di dialogo in cui l'utente può selezionare le impostazioni di compressione per il nuovo file tramite la funzione [**AVISaveOptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions) .</span><span class="sxs-lookup"><span data-stu-id="170ac-113">You can create a dialog box in which the user can select compression settings for the new file by using the [**AVISaveOptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions) function.</span></span> <span data-ttu-id="170ac-114">Nella finestra di dialogo vengono visualizzate le impostazioni di compressione correnti e l'utente viene modificato.</span><span class="sxs-lookup"><span data-stu-id="170ac-114">The dialog box displays the current compression settings and lets the user edit them.</span></span> <span data-ttu-id="170ac-115">Le modifiche delle impostazioni di compressione vengono archiviate in una struttura [**AVICOMPRESSOPTIONS**](/windows/desktop/api/Vfw/ns-vfw-avicompressoptions) .</span><span class="sxs-lookup"><span data-stu-id="170ac-115">Compression setting changes are stored in an [**AVICOMPRESSOPTIONS**](/windows/desktop/api/Vfw/ns-vfw-avicompressoptions) structure.</span></span>

<span data-ttu-id="170ac-116">È anche possibile includere una funzione di callback con [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) e [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) che l'applicazione può usare per visualizzare lo stato di avanzamento della scrittura del file e, se necessario, consentire all'utente di annullare l'operazione di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="170ac-116">You can also include a callback function with [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) and [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) that your application can use to display the progress of writing the file and, if needed, let the user cancel the save operation.</span></span> <span data-ttu-id="170ac-117">È possibile includere l'indirizzo della funzione di callback nella sequenza chiamante di **AVISave** o **AVISaveV**.</span><span class="sxs-lookup"><span data-stu-id="170ac-117">You can include the address of the callback function in the calling sequence of **AVISave** or **AVISaveV**.</span></span>

<span data-ttu-id="170ac-118">È possibile consentire all'utente di selezionare un nome file per il nuovo file usando la funzione [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) .</span><span class="sxs-lookup"><span data-stu-id="170ac-118">You can let the user select a filename for the new file by using the [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) function.</span></span> <span data-ttu-id="170ac-119">Questa funzione Visualizza la finestra di dialogo Salva con nome in cui l'utente può visualizzare l'anteprima del primo flusso, in genere il flusso video, di un file AVI.</span><span class="sxs-lookup"><span data-stu-id="170ac-119">This function displays the Save As dialog box in which the user can preview the first stream (normally the video stream) of an AVI file.</span></span>

<span data-ttu-id="170ac-120">È possibile creare un puntatore a interfaccia file (e un file virtuale) per un gruppo di flussi usando la funzione [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) .</span><span class="sxs-lookup"><span data-stu-id="170ac-120">You can create a file interface pointer (and a virtual file) for a group of streams by using the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function.</span></span> <span data-ttu-id="170ac-121">Altre funzioni AVIFile possono usare il puntatore di interfaccia file restituito da questa funzione per accedere ai flussi nel file virtuale.</span><span class="sxs-lookup"><span data-stu-id="170ac-121">Other AVIFile functions can use the file interface pointer returned by this function to access the streams in the virtual file.</span></span> <span data-ttu-id="170ac-122">Al termine dell'utilizzo del file virtuale, eliminare il puntatore all'interfaccia di file utilizzando la funzione [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) .</span><span class="sxs-lookup"><span data-stu-id="170ac-122">After you finish using the virtual file, delete the file interface pointer by using the [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) function.</span></span>

> [!Note]  
> <span data-ttu-id="170ac-123">Per ridurre al minimo la riduzione di immagini e audio, evitare di comprimere un file AVI più di una volta.</span><span class="sxs-lookup"><span data-stu-id="170ac-123">To minimize image and audio degradation, avoid compressing an AVI file more than once.</span></span> <span data-ttu-id="170ac-124">Combinare parti del video non compresse nel sistema di modifica e quindi comprimere il prodotto finale.</span><span class="sxs-lookup"><span data-stu-id="170ac-124">Combine uncompressed pieces of video in your editing system and then compress the final product.</span></span> <span data-ttu-id="170ac-125">Per informazioni sulle opzioni di compressione, vedere [Video Compression Manager](video-compression-manager.md).</span><span class="sxs-lookup"><span data-stu-id="170ac-125">For information about compression options, see [Video Compression Manager](video-compression-manager.md).</span></span>

 

 

 




