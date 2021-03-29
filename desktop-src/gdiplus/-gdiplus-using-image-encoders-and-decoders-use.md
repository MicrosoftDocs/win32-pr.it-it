---
description: Windows GDI+ fornisce la classe Image e la classe bitmap per archiviare le immagini in memoria e modificare le immagini in memoria.
ms.assetid: f9a5b4b1-4e25-42c8-a96b-a3104841e5f3
title: Uso di codificatori e decodificatori di immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c55c75e00b3d624d27ba888ae26afb3a5ee0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129051"
---
# <a name="using-image-encoders-and-decoders"></a><span data-ttu-id="2affc-103">Uso di codificatori e decodificatori di immagini</span><span class="sxs-lookup"><span data-stu-id="2affc-103">Using Image Encoders and Decoders</span></span>

<span data-ttu-id="2affc-104">Windows GDI+ fornisce la classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e la classe [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) per archiviare le immagini in memoria e modificare le immagini in memoria.</span><span class="sxs-lookup"><span data-stu-id="2affc-104">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class and the [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class for storing images in memory and manipulating images in memory.</span></span> <span data-ttu-id="2affc-105">GDI+ scrive immagini sui file su disco con l'ausilio dei codificatori di immagini e carica immagini dai file su disco con l'ausilio di decodificatori di immagini.</span><span class="sxs-lookup"><span data-stu-id="2affc-105">GDI+ writes images to disk files with the help of image encoders and loads images from disk files with the help of image decoders.</span></span> <span data-ttu-id="2affc-106">Un codificatore converte i dati in un oggetto **immagine** o **bitmap** in un formato di file su disco designato.</span><span class="sxs-lookup"><span data-stu-id="2affc-106">An encoder translates the data in an **Image** or **Bitmap** object into a designated disk file format.</span></span> <span data-ttu-id="2affc-107">Un decodificatore converte i dati in un file su disco nel formato richiesto dall' **immagine** e dagli oggetti **bitmap** .</span><span class="sxs-lookup"><span data-stu-id="2affc-107">A decoder translates the data in a disk file to the format required by the **Image** and **Bitmap** objects.</span></span> <span data-ttu-id="2affc-108">GDI+ include codificatori e decodificatori incorporati che supportano i tipi di file seguenti:</span><span class="sxs-lookup"><span data-stu-id="2affc-108">GDI+ has built-in encoders and decoders that support the following file types:</span></span>

-   <span data-ttu-id="2affc-109">BMP</span><span class="sxs-lookup"><span data-stu-id="2affc-109">BMP</span></span>
-   <span data-ttu-id="2affc-110">GIF</span><span class="sxs-lookup"><span data-stu-id="2affc-110">GIF</span></span>
-   <span data-ttu-id="2affc-111">JPEG</span><span class="sxs-lookup"><span data-stu-id="2affc-111">JPEG</span></span>
-   <span data-ttu-id="2affc-112">PNG</span><span class="sxs-lookup"><span data-stu-id="2affc-112">PNG</span></span>
-   <span data-ttu-id="2affc-113">TIFF</span><span class="sxs-lookup"><span data-stu-id="2affc-113">TIFF</span></span>

<span data-ttu-id="2affc-114">GDI+ dispone inoltre di decodificatori incorporati che supportano i tipi di file seguenti:</span><span class="sxs-lookup"><span data-stu-id="2affc-114">GDI+ also has built-in decoders that support the following file types:</span></span>

-   <span data-ttu-id="2affc-115">WMF</span><span class="sxs-lookup"><span data-stu-id="2affc-115">WMF</span></span>
-   <span data-ttu-id="2affc-116">EMF</span><span class="sxs-lookup"><span data-stu-id="2affc-116">EMF</span></span>
-   <span data-ttu-id="2affc-117">ICONA</span><span class="sxs-lookup"><span data-stu-id="2affc-117">ICON</span></span>

<span data-ttu-id="2affc-118">Negli argomenti seguenti vengono illustrati in modo più dettagliato i codificatori e i decodificatori:</span><span class="sxs-lookup"><span data-stu-id="2affc-118">The following topics discuss encoders and decoders in more detail:</span></span>

-   [<span data-ttu-id="2affc-119">Elenco di codificatori installati</span><span class="sxs-lookup"><span data-stu-id="2affc-119">Listing Installed Encoders</span></span>](-gdiplus-listing-installed-encoders-use.md)
-   [<span data-ttu-id="2affc-120">Elenco di decodificatori installati</span><span class="sxs-lookup"><span data-stu-id="2affc-120">Listing Installed Decoders</span></span>](-gdiplus-listing-installed-decoders-use.md)
-   [<span data-ttu-id="2affc-121">Recupero dell'identificatore di classe per un codificatore</span><span class="sxs-lookup"><span data-stu-id="2affc-121">Retrieving the Class Identifier for an Encoder</span></span>](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [<span data-ttu-id="2affc-122">Determinazione dei parametri supportati da un codificatore</span><span class="sxs-lookup"><span data-stu-id="2affc-122">Determining the Parameters Supported by an Encoder</span></span>](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [<span data-ttu-id="2affc-123">Conversione di un'immagine BMP in un'immagine PNG</span><span class="sxs-lookup"><span data-stu-id="2affc-123">Converting a BMP Image to a PNG Image</span></span>](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [<span data-ttu-id="2affc-124">Impostazione del livello di compressione JPEG</span><span class="sxs-lookup"><span data-stu-id="2affc-124">Setting JPEG Compression Level</span></span>](-gdiplus-setting-jpeg-compression-level-use.md)
-   [<span data-ttu-id="2affc-125">Trasformazione di un'immagine JPEG senza perdita di informazioni</span><span class="sxs-lookup"><span data-stu-id="2affc-125">Transforming a JPEG Image Without Loss of Information</span></span>](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [<span data-ttu-id="2affc-126">Creazione e salvataggio di un'immagine a più frame</span><span class="sxs-lookup"><span data-stu-id="2affc-126">Creating and Saving a Multiple-Frame Image</span></span>](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [<span data-ttu-id="2affc-127">Copia di singoli frame da un'immagine Multiple-Frame</span><span class="sxs-lookup"><span data-stu-id="2affc-127">Copying Individual Frames from a Multiple-Frame Image</span></span>](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 



