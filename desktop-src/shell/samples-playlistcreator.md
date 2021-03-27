---
description: Viene illustrato come creare un verbo che opera su un elemento o un contenitore della shell selezionato per creare una playlist.
title: Esempio di autore di playlist
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B35B7A18-2163-4860-BC50-8918056C9F4A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c5e4f6570faff459126a32ea4680d41a3b8302e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980922"
---
# <a name="playlist-creator-sample"></a><span data-ttu-id="5d34a-103">Esempio di autore di playlist</span><span class="sxs-lookup"><span data-stu-id="5d34a-103">Playlist Creator Sample</span></span>

<span data-ttu-id="5d34a-104">Viene illustrato come creare un verbo che opera su un elemento o un contenitore della shell selezionato per creare una playlist.</span><span class="sxs-lookup"><span data-stu-id="5d34a-104">Demonstrates how to create a verb that operates on a selected Shell item or container to create a playlist.</span></span>

<span data-ttu-id="5d34a-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="5d34a-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5d34a-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d34a-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="5d34a-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="5d34a-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="5d34a-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="5d34a-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="5d34a-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="5d34a-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="5d34a-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d34a-110">Requirements</span></span>



| <span data-ttu-id="5d34a-111">Prodotto</span><span class="sxs-lookup"><span data-stu-id="5d34a-111">Product</span></span>                                | <span data-ttu-id="5d34a-112">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="5d34a-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="5d34a-113">Windows</span><span class="sxs-lookup"><span data-stu-id="5d34a-113">Windows</span></span>                                | <span data-ttu-id="5d34a-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d34a-114">Windows Vista</span></span>           |
| <span data-ttu-id="5d34a-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="5d34a-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="5d34a-116">7.0</span><span class="sxs-lookup"><span data-stu-id="5d34a-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="5d34a-117">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="5d34a-117">Downloading the Sample</span></span>

| <span data-ttu-id="5d34a-118">Location</span><span class="sxs-lookup"><span data-stu-id="5d34a-118">Location</span></span>      | <span data-ttu-id="5d34a-119">URL percorso</span><span class="sxs-lookup"><span data-stu-id="5d34a-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d34a-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="5d34a-120">GitHub</span></span>  | [<span data-ttu-id="5d34a-121">Esempio PlaylistCreator</span><span class="sxs-lookup"><span data-stu-id="5d34a-121">PlaylistCreator sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlaylistCreator) |

## <a name="building-the-sample"></a><span data-ttu-id="5d34a-122">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="5d34a-122">Building the Sample</span></span>

<span data-ttu-id="5d34a-123">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="5d34a-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="5d34a-124">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **PlaylistCreator** .</span><span class="sxs-lookup"><span data-stu-id="5d34a-124">Open the command prompt window and navigate to the **PlaylistCreator** project directory.</span></span>
2.  <span data-ttu-id="5d34a-125">Immettere `msbuild PlaylistCreator.sln`.</span><span class="sxs-lookup"><span data-stu-id="5d34a-125">Enter `msbuild PlaylistCreator.sln`.</span></span>

<span data-ttu-id="5d34a-126">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="5d34a-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

> [!Note]  
> <span data-ttu-id="5d34a-127">Questo esempio può essere usato anche con il Visual C++ Express Edition se la versione completa di Visual Studio non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="5d34a-127">This sample can also be used with the Visual C++ Express Edition if the full Visual Studio is not available.</span></span>

 

1.  <span data-ttu-id="5d34a-128">Aprire Esplora risorse e passare alla directory del progetto **PlaylistCreator** .</span><span class="sxs-lookup"><span data-stu-id="5d34a-128">Open Windows Explorer and navigate to the **PlaylistCreator** project directory.</span></span>
2.  <span data-ttu-id="5d34a-129">Fare doppio clic sull'icona per il file PlaylistCreator. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5d34a-129">Double-click the icon for the PlaylistCreator.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="5d34a-130">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="5d34a-130">From the **Build** menu, select **Build Solution**.</span></span>
    > [!Note]  
    > <span data-ttu-id="5d34a-131">Se si compila 64 bit usando il Visual C++ Express Edition, è necessario usare il compilatore incrociato x64 fornito con l'Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="5d34a-131">If you are compiling 64-bit using the Visual C++ Express Edition, you must to use the x64 cross-compiler supplied with the Windows SDK.</span></span>

     

## <a name="running-the-sample"></a><span data-ttu-id="5d34a-132">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="5d34a-132">Running the Sample</span></span>

1.  <span data-ttu-id="5d34a-133">Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="5d34a-133">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="5d34a-134">Nella riga di comando, immettere `PlaylistCreator.exe` .</span><span class="sxs-lookup"><span data-stu-id="5d34a-134">At the command line, enter `PlaylistCreator.exe`.</span></span> <span data-ttu-id="5d34a-135">In alternativa, in Esplora risorse fare doppio clic sull'icona per PlaylistCreator.exe.</span><span class="sxs-lookup"><span data-stu-id="5d34a-135">Alternatively, from Windows Explorer double-click the icon for PlaylistCreator.exe.</span></span>
3.  <span data-ttu-id="5d34a-136">Fare clic con il pulsante destro del mouse su qualsiasi file o cartella musicale contenente file musicali in Esplora risorse per creare una playlist per visualizzare il menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="5d34a-136">Right-click any music file or folder containing music files in Windows Explorer to create a playlist to bring up the context menu</span></span>
4.  <span data-ttu-id="5d34a-137">È possibile creare una playlist con estensione M3U o WPL.</span><span class="sxs-lookup"><span data-stu-id="5d34a-137">You can create a .m3u or .wpl playlist.</span></span> <span data-ttu-id="5d34a-138">Le playlist vengono create nella `%userprofile%\Music\Playlists` cartella.</span><span class="sxs-lookup"><span data-stu-id="5d34a-138">Playlists are created in the `%userprofile%\Music\Playlists` folder.</span></span>
    > [!Note]  
    > <span data-ttu-id="5d34a-139">I nuovi verbi nel menu di scelta rapida sono disponibili nella cartella **Music** , nello stack di musica, negli stack della **raccolta musicale** e nelle raccolte di file musicali.</span><span class="sxs-lookup"><span data-stu-id="5d34a-139">New verbs in the context menu can be found in the **Music** folder, music stacks, stacks in the **Music Library**, and collections of music files.</span></span>

     

 

 



