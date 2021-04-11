---
description: Media Detector (MediaDet)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Media Detector (MediaDet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f34b1dc267480d3d6ea9efe9b9a743623a917b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132174"
---
# <a name="media-detector-mediadet"></a><span data-ttu-id="fe276-103">Media Detector (MediaDet)</span><span class="sxs-lookup"><span data-stu-id="fe276-103">Media Detector (MediaDet)</span></span>

> [!Note]  
> <span data-ttu-id="fe276-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="fe276-104">\[Deprecated.</span></span> <span data-ttu-id="fe276-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fe276-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fe276-106">L'oggetto Media Detector (MediaDet) recupera le informazioni sul formato e comunque i frame dalle origini file.</span><span class="sxs-lookup"><span data-stu-id="fe276-106">The Media Detector (MediaDet) object retrieves format information and still frames from file sources.</span></span> <span data-ttu-id="fe276-107">Il rilevatore multimediale non richiede la gestione del grafo del filtro per funzionare.</span><span class="sxs-lookup"><span data-stu-id="fe276-107">The Media Detector does not require the Filter Graph Manager to function.</span></span> <span data-ttu-id="fe276-108">Per creare questo oggetto, chiamare **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="fe276-108">To create this object, call **CoCreateInstance**.</span></span> <span data-ttu-id="fe276-109">L'identificatore di classe è CLSID \_ mediadet.</span><span class="sxs-lookup"><span data-stu-id="fe276-109">The class identifier is CLSID\_MediaDet.</span></span>

<span data-ttu-id="fe276-110">Per leggere i file di Windows Media™, l'applicazione deve fornire un certificato software, detto anche chiave.</span><span class="sxs-lookup"><span data-stu-id="fe276-110">To read Windows Media™ files, the application must provide a software certificate, also called a key.</span></span> <span data-ttu-id="fe276-111">Registrare l'applicazione come provider di chiavi tramite l'interfaccia **IObjectWithSite** del detector multimediale.</span><span class="sxs-lookup"><span data-stu-id="fe276-111">Register the application as a key provider through the Media Detector's **IObjectWithSite** interface.</span></span> <span data-ttu-id="fe276-112">Per ulteriori informazioni, vedere [sblocco di Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span><span class="sxs-lookup"><span data-stu-id="fe276-112">For more information, see [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).</span></span>

<span data-ttu-id="fe276-113">L'oggetto MediaDet espone le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="fe276-113">The MediaDet object exposes the following interfaces:</span></span>

-   [<span data-ttu-id="fe276-114">**IMediaDet**</span><span class="sxs-lookup"><span data-stu-id="fe276-114">**IMediaDet**</span></span>](imediadet.md)
-   <span data-ttu-id="fe276-115">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="fe276-115">**IObjectWithSite**</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe276-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fe276-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe276-117">Utilizzo di origini</span><span class="sxs-lookup"><span data-stu-id="fe276-117">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



