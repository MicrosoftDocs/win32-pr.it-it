---
description: Sequenza temporale
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Sequenza temporale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d1f802f12df6ca3469b8283bd4fe8b27e22412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319540"
---
# <a name="timeline"></a><span data-ttu-id="60272-103">Sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="60272-103">Timeline</span></span>

> [!Note]  
> <span data-ttu-id="60272-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="60272-104">\[Deprecated.</span></span> <span data-ttu-id="60272-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="60272-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="60272-106">L'oggetto sequenza temporale gestisce tutti gli oggetti in un progetto di modifica video.</span><span class="sxs-lookup"><span data-stu-id="60272-106">The timeline object manages all of the objects in a video editing project.</span></span> <span data-ttu-id="60272-107">Per creare questo oggetto, chiamare **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="60272-107">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="60272-108">L'identificatore di classe è CLSID \_ AMTimeline.</span><span class="sxs-lookup"><span data-stu-id="60272-108">The class identifier is CLSID\_AMTimeline.</span></span>

<span data-ttu-id="60272-109">Per leggere i file di Windows Media™, l'applicazione deve fornire un certificato software, detto anche chiave.</span><span class="sxs-lookup"><span data-stu-id="60272-109">To read Windows Media™ files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="60272-110">Registrare l'applicazione come provider di chiavi tramite l'interfaccia **IObjectWithSite** della sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="60272-110">Register the application as a key provider through the timeline's **IObjectWithSite** interface.</span></span> <span data-ttu-id="60272-111">Per ulteriori informazioni, vedere [sblocco di Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span><span class="sxs-lookup"><span data-stu-id="60272-111">For more information, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="60272-112">L'oggetto sequenza temporale espone le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="60272-112">The timeline object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="60272-113">**IAMSetErrorLog**</span><span class="sxs-lookup"><span data-stu-id="60272-113">**IAMSetErrorLog**</span></span>](iamseterrorlog.md)
-   [<span data-ttu-id="60272-114">**IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="60272-114">**IAMTimeline**</span></span>](iamtimeline.md)
-   <span data-ttu-id="60272-115">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="60272-115">**IObjectWithSite**</span></span>
-   <span data-ttu-id="60272-116">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="60272-116">**IPersistStream**</span></span>

## <a name="related-topics"></a><span data-ttu-id="60272-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60272-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60272-118">Modello di sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="60272-118">The Timeline Model</span></span>](the-timeline-model.md)
</dt> <dt>

[<span data-ttu-id="60272-119">Creazione di una sequenza temporale</span><span class="sxs-lookup"><span data-stu-id="60272-119">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 



