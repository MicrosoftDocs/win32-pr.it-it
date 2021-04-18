---
description: Oggetto ContentInfo ASF
ms.assetid: 6b7f8b68-fe98-4aeb-9842-a80ac6235999
title: Oggetto ContentInfo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bafa14279ab35c1c6986a8e19f302c764a587a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305525"
---
# <a name="asf-contentinfo-object"></a><span data-ttu-id="7ec95-103">Oggetto ContentInfo ASF</span><span class="sxs-lookup"><span data-stu-id="7ec95-103">ASF ContentInfo Object</span></span>

<span data-ttu-id="7ec95-104">L'oggetto *CONTENTINFO* ASF archivia le informazioni dall'oggetto intestazione ASF di un file.</span><span class="sxs-lookup"><span data-stu-id="7ec95-104">The ASF *ContentInfo* object stores information from the ASF Header Object of a file.</span></span> <span data-ttu-id="7ec95-105">Un'applicazione può usare l'oggetto ContentInfo per gli scopi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ec95-105">An application can use the ContentInfo object for the following purposes:</span></span>

-   <span data-ttu-id="7ec95-106">Leggere l'oggetto intestazione per un file multimediale esistente.</span><span class="sxs-lookup"><span data-stu-id="7ec95-106">Read the Header Object for an existing media file.</span></span> <span data-ttu-id="7ec95-107">In questo caso, l'oggetto ContentInfo analizza l'oggetto Header e archivia le informazioni sul file delle caratteristiche.</span><span class="sxs-lookup"><span data-stu-id="7ec95-107">In this case, the ContentInfo object parses the Header Object and stores information about the characteristics file.</span></span> <span data-ttu-id="7ec95-108">Media Foundation espone alcune di queste proprietà tramite attributi e interfacce.</span><span class="sxs-lookup"><span data-stu-id="7ec95-108">Media Foundation exposes several of these properties through attributes and interfaces.</span></span> <span data-ttu-id="7ec95-109">Queste sono descritte in [Media Foundation attributi per gli oggetti intestazione ASF](media-foundation-attributes-for-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7ec95-109">These are described in [Media Foundation Attributes for ASF Header Objects](media-foundation-attributes-for-asf-header-objects.md).</span></span>
-   <span data-ttu-id="7ec95-110">Scrivere le informazioni di intestazione e costruire un oggetto intestazione per un nuovo file.</span><span class="sxs-lookup"><span data-stu-id="7ec95-110">Write header information and construct a Header Object for a new file.</span></span>
-   <span data-ttu-id="7ec95-111">Inizializzare altri oggetti ASF, ad esempio il [separatore ASF](asf-splitter.md), il [multiplexer](asf-multiplexer.md)ASF e l'indicizzatore ASF, durante la lettura o la scrittura di un file multimediale.</span><span class="sxs-lookup"><span data-stu-id="7ec95-111">Initialize other ASF objects such as the [ASF Splitter](asf-splitter.md), [ASF Multiplexer](asf-multiplexer.md), and the ASF Indexer, while reading or writing a media file.</span></span>

<span data-ttu-id="7ec95-112">Per informazioni sulla struttura di un file ASF, vedere la pagina relativa alla [struttura dei file ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="7ec95-112">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

## <a name="creating-the-contentinfo-object"></a><span data-ttu-id="7ec95-113">Creazione dell'oggetto ContentInfo</span><span class="sxs-lookup"><span data-stu-id="7ec95-113">Creating the ContentInfo Object</span></span>

<span data-ttu-id="7ec95-114">Per creare una nuova istanza dell'oggetto ContentInfo, chiamare la funzione [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) .</span><span class="sxs-lookup"><span data-stu-id="7ec95-114">To create a new instance of the ContentInfo object, call the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function.</span></span> <span data-ttu-id="7ec95-115">Questo metodo restituisce un puntatore a un oggetto ContentInfo vuoto che deve essere inizializzato per funzionare con un file ASF specifico.</span><span class="sxs-lookup"><span data-stu-id="7ec95-115">This method returns a pointer to an empty ContentInfo object that must be initialized to work with a specific ASF file.</span></span> <span data-ttu-id="7ec95-116">A seconda che l'applicazione legga un file esistente o scriva un nuovo file ASF, deve chiamare [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) o [**IMFASFContentInfo:: seprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) per popolare l'oggetto vuoto.</span><span class="sxs-lookup"><span data-stu-id="7ec95-116">Depending on whether the application is reading an existing file or writing a new ASF file, it must call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) or [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to populate the empty object.</span></span>

<span data-ttu-id="7ec95-117">Per ulteriori informazioni su queste chiamate al metodo, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ec95-117">For more information about these method calls, see the following topics:</span></span>

-   [<span data-ttu-id="7ec95-118">Lettura dell'oggetto intestazione ASF di un file esistente</span><span class="sxs-lookup"><span data-stu-id="7ec95-118">Reading the ASF Header Object of an Existing File</span></span>](reading-the-asf-header-object-of-an-existing-file.md)
-   [<span data-ttu-id="7ec95-119">Recupero di informazioni da oggetti Header ASF</span><span class="sxs-lookup"><span data-stu-id="7ec95-119">Getting Information from ASF Header Objects</span></span>](getting-information-from-asf-header-objects.md)
-   [<span data-ttu-id="7ec95-120">Scrittura di un oggetto intestazione ASF per un nuovo file</span><span class="sxs-lookup"><span data-stu-id="7ec95-120">Writing an ASF Header Object for a New File</span></span>](writing-an-asf-header-object-for-a-new-file.md)
-   [<span data-ttu-id="7ec95-121">Attributi di Media Foundation per oggetti intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="7ec95-121">Media Foundation Attributes for ASF Header Objects</span></span>](media-foundation-attributes-for-asf-header-objects.md)

## <a name="related-topics"></a><span data-ttu-id="7ec95-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7ec95-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ec95-123">Componenti ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="7ec95-123">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> </dl>

 

 



