---
title: Archiviazione e flussi
description: Un oggetto di archiviazione è analogo a una directory file system.
ms.assetid: 57b2a66d-e912-4879-b778-75f8461d211f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebc44a22779b4ae63ee7c39b55888d2ea23579f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708353"
---
# <a name="storages-and-streams"></a><span data-ttu-id="1940a-103">Archiviazione e flussi</span><span class="sxs-lookup"><span data-stu-id="1940a-103">Storages and Streams</span></span>

<span data-ttu-id="1940a-104">Un oggetto di archiviazione è analogo a una directory file system.</span><span class="sxs-lookup"><span data-stu-id="1940a-104">A storage object is analogous to a file system directory.</span></span> <span data-ttu-id="1940a-105">Così come una directory può contenere altre directory e file, un oggetto di archiviazione può contenere altri oggetti di archiviazione e oggetti Stream.</span><span class="sxs-lookup"><span data-stu-id="1940a-105">Just as a directory can contain other directories and files, a storage object can contain other storage objects and stream objects.</span></span> <span data-ttu-id="1940a-106">Analogamente a una directory, un oggetto di archiviazione tiene traccia delle posizioni e delle dimensioni degli oggetti di archiviazione e degli oggetti flusso annidati sotto di esso.</span><span class="sxs-lookup"><span data-stu-id="1940a-106">Also like a directory, a storage object tracks the locations and sizes of the storage objects and stream objects nested beneath it.</span></span>

<span data-ttu-id="1940a-107">Un oggetto flusso è analogo alla nozione tradizionale di un file.</span><span class="sxs-lookup"><span data-stu-id="1940a-107">A stream object is analogous to the traditional notion of a file.</span></span> <span data-ttu-id="1940a-108">Analogamente a un file, un flusso contiene dati archiviati come sequenza consecutiva di byte.</span><span class="sxs-lookup"><span data-stu-id="1940a-108">Like a file, a stream contains data stored as a consecutive sequence of bytes.</span></span>

<span data-ttu-id="1940a-109">Un file composto COM è costituito da un oggetto di archiviazione radice che contiene almeno un oggetto flusso che rappresenta i dati nativi insieme a uno o più oggetti di archiviazione corrispondenti agli oggetti collegati e incorporati.</span><span class="sxs-lookup"><span data-stu-id="1940a-109">A COM compound file consists of a root storage object containing at least one stream object representing its native data along with one or more storage objects corresponding to its linked and embedded objects.</span></span> <span data-ttu-id="1940a-110">L'oggetto di archiviazione radice viene mappato a un nome di file in qualsiasi file system risieda.</span><span class="sxs-lookup"><span data-stu-id="1940a-110">The root storage object maps to a file name in whatever file system it happens to reside.</span></span> <span data-ttu-id="1940a-111">Tutti gli oggetti all'interno del documento sono rappresentati anche da un oggetto di archiviazione contenente uno o più oggetti flusso e probabilmente che contengono anche uno o più oggetti di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1940a-111">Each of the objects inside the document also is represented by a storage object containing one or more stream objects, and perhaps also containing one or more storage objects.</span></span> <span data-ttu-id="1940a-112">In questo modo, un documento può essere costituito da un numero illimitato di oggetti annidati.</span><span class="sxs-lookup"><span data-stu-id="1940a-112">In this way, a document can consist of an unlimited number of nested objects.</span></span> <span data-ttu-id="1940a-113">Per ulteriori informazioni, vedere [file composti](compound-files.md).</span><span class="sxs-lookup"><span data-stu-id="1940a-113">For more information, see [Compound Files](compound-files.md).</span></span>

 

 




