---
description: Il formato del file X si riferisce ai file con estensione x.
ms.assetid: 06b3dcb3-03fc-4d99-b8c3-32f56d8bf49e
title: File X (legacy) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0e4ce85a0ff5ecbc2f680f55b8162d13bc1042
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876178"
---
# <a name="x-files-legacy-direct3d-9"></a><span data-ttu-id="23c5e-103">File X (legacy) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="23c5e-103">X Files (Legacy) (Direct3D 9)</span></span>

<span data-ttu-id="23c5e-104">Il formato del file X si riferisce ai file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="23c5e-104">The X file format refers to files with the .x file name extension.</span></span> <span data-ttu-id="23c5e-105">I file X sono stati introdotti con DirectX 2,0.</span><span class="sxs-lookup"><span data-stu-id="23c5e-105">X files were introduced with DirectX 2.0.</span></span> <span data-ttu-id="23c5e-106">Una versione binaria di questo formato è stata rilasciata successivamente con DirectX 3,0, descritta anche in questa documentazione.</span><span class="sxs-lookup"><span data-stu-id="23c5e-106">A binary version of this format was subsequently released with DirectX 3.0, which is also described in this documentation.</span></span> <span data-ttu-id="23c5e-107">DirectX 6,0 ha introdotto interfacce e metodi che consentono la lettura e la scrittura in file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="23c5e-107">DirectX 6.0 introduced interfaces and methods that enable reading from and writing to .x files.</span></span>

<span data-ttu-id="23c5e-108">I file X forniscono un formato basato su modello che consente l'archiviazione di mesh, trame, animazioni e oggetti definibili dall'utente.</span><span class="sxs-lookup"><span data-stu-id="23c5e-108">X files provide a template-driven format that enables the storage of meshes, textures, animations, and user-definable objects.</span></span> <span data-ttu-id="23c5e-109">Il supporto per i set di animazioni consente di archiviare percorsi predefiniti per la riproduzione in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="23c5e-109">Support for animation sets enables you to store predefined paths for playback in real time.</span></span> <span data-ttu-id="23c5e-110">Sono supportate anche le istanze e le gerarchie.</span><span class="sxs-lookup"><span data-stu-id="23c5e-110">Instancing and hierarchies are also supported.</span></span> <span data-ttu-id="23c5e-111">La creazione di istanze consente più riferimenti a un oggetto, ad esempio una mesh, mentre archivia i dati solo una volta per ogni file.</span><span class="sxs-lookup"><span data-stu-id="23c5e-111">Instancing enables multiple references to an object, such as a mesh, while storing its data only once per file.</span></span> <span data-ttu-id="23c5e-112">Le gerarchie vengono utilizzate per esprimere le relazioni tra i record di dati.</span><span class="sxs-lookup"><span data-stu-id="23c5e-112">Hierarchies are used to express relationships between data records.</span></span>

<span data-ttu-id="23c5e-113">Il formato di file con estensione x fornisce primitive di dati di basso livello in cui le applicazioni definiscono primitive di livello superiore tramite modelli.</span><span class="sxs-lookup"><span data-stu-id="23c5e-113">The .x file format provides low-level data primitives on which applications define higher-level primitives through templates.</span></span>

<span data-ttu-id="23c5e-114">È possibile convertire i modelli tridimensionali creati in applicazioni Maya di 3ds Max o alias del fronte di discreta in \| file con estensione x con le estensioni DirectX per Alias Maya.</span><span class="sxs-lookup"><span data-stu-id="23c5e-114">Three-dimensional models created in Discreet's 3ds max or Alias\|Wavefront's Maya applications can be converted to .x files with the DirectX Extensions for Alias Maya.</span></span>

<span data-ttu-id="23c5e-115">In questa sezione viene descritta la struttura dei file con estensione x e viene illustrato come usarli nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="23c5e-115">This section describes the structure of .x files and how to use them in your applications.</span></span> <span data-ttu-id="23c5e-116">Le informazioni sono suddivise negli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="23c5e-116">Information is divided into the following topics.</span></span>

-   [<span data-ttu-id="23c5e-117">Caricamento di un file X (legacy) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="23c5e-117">Loading an X File (Legacy) (Direct3D 9)</span></span>](loading-an-x-file--legacy-.md)
-   [<span data-ttu-id="23c5e-118">Salvataggio in un file X (legacy) (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="23c5e-118">Saving to an X File (Legacy) (Direct3D 9)</span></span>](saving-to-an-x-file--legacy-.md)
-   [<span data-ttu-id="23c5e-119">Definizione di un cubo semplice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="23c5e-119">Defining a Simple Cube (Direct3D 9)</span></span>](defining-a-simple-cube.md)
-   [<span data-ttu-id="23c5e-120">Aggiunta di trame (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="23c5e-120">Adding Textures (Direct3D 9)</span></span>](adding-textures.md)
-   [<span data-ttu-id="23c5e-121">Aggiunta di frame e animazioni (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="23c5e-121">Adding Frames and Animations (Direct3D 9)</span></span>](adding-frames-and-animations.md)

<span data-ttu-id="23c5e-122">Per ulteriori informazioni sul formato di file con estensione x, vedere la pagina relativa al [riferimento al file x](dx9-graphics-reference-d3dx-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="23c5e-122">For more information about the .x file format, see [X File Reference](dx9-graphics-reference-d3dx-x-file.md).</span></span>

<span data-ttu-id="23c5e-123">Per ulteriori informazioni sull'API file con estensione x, vedere la pagina relativa al [riferimento al file x (legacy)](dx9-graphics-reference-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="23c5e-123">For more information about the .x file API, see [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="23c5e-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23c5e-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23c5e-125">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="23c5e-125">Getting Started</span></span>](getting-started.md)
</dt> </dl>

 

 



