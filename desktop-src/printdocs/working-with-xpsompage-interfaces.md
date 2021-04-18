---
description: Questo argomento descrive come usare le interfacce a livello di pagina che consentono di accedere al contenuto di una pagina in un OM XPS.
ms.assetid: 7127ee28-eca9-4e0e-a27a-9051eb105b27
title: Utilizzo di interfacce di pagine XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8350409f2f436cc4ec2293e735c3f020b49bea68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313997"
---
# <a name="working-with-xps-om-page-interfaces"></a><span data-ttu-id="a9e8e-103">Utilizzo di interfacce di pagine XPS OM</span><span class="sxs-lookup"><span data-stu-id="a9e8e-103">Working with XPS OM Page Interfaces</span></span>

<span data-ttu-id="a9e8e-104">Questo argomento descrive come usare le interfacce a livello di pagina che consentono di accedere al contenuto di una pagina in un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="a9e8e-104">This topic describes how to use the page-level interfaces that provide access to the contents of a page in an XPS OM.</span></span>



| <span data-ttu-id="a9e8e-105">Nome interfaccia</span><span class="sxs-lookup"><span data-stu-id="a9e8e-105">Interface name</span></span>                                                                                                                                                                              | <span data-ttu-id="a9e8e-106">Interfacce figlio logiche</span><span class="sxs-lookup"><span data-stu-id="a9e8e-106">Logical child interfaces</span></span>                                                                                                                                                                                            | <span data-ttu-id="a9e8e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9e8e-107">Description</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9e8e-108">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-108">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                                                                                                                                                 | [<span data-ttu-id="a9e8e-109">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-109">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/> [<span data-ttu-id="a9e8e-110">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-110">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/> [<span data-ttu-id="a9e8e-111">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-111">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                                                                         | <span data-ttu-id="a9e8e-112">Oggetto radice del contenuto della pagina.</span><span class="sxs-lookup"><span data-stu-id="a9e8e-112">The root object of the page contents.</span></span><br/> <span data-ttu-id="a9e8e-113">Questo oggetto rappresenta una parte del documento.</span><span class="sxs-lookup"><span data-stu-id="a9e8e-113">This object represents a document part.</span></span><br/>                                                |
| [<span data-ttu-id="a9e8e-114">**IXpsOMShareable**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-114">**IXpsOMShareable**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable)<br/>                                                                                                                                       | [<span data-ttu-id="a9e8e-115">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-115">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)<br/> [<span data-ttu-id="a9e8e-116">**IXpsOMMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-116">**IXpsOMMatrixTransform**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/> [<span data-ttu-id="a9e8e-117">**IXpsOMGeometry**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-117">**IXpsOMGeometry**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/> [<span data-ttu-id="a9e8e-118">**IXpsOMBrush**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-118">**IXpsOMBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/> | <span data-ttu-id="a9e8e-119">Le interfacce che derivano dall'interfaccia [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) possono essere archiviate in un dizionario risorse e condivise.</span><span class="sxs-lookup"><span data-stu-id="a9e8e-119">Interfaces that derive from the [**IXpsOMShareable**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable) interface can be stored in a resource dictionary and shared.</span></span><br/> |
| [<span data-ttu-id="a9e8e-120">**IXpsOMRemoteDictionaryResource**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-120">**IXpsOMRemoteDictionaryResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)<br/> [<span data-ttu-id="a9e8e-121">**IXpsOMRemoteDictionaryResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-121">**IXpsOMRemoteDictionaryResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)<br/> | [<span data-ttu-id="a9e8e-122">**IXpsOMDictionary**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-122">**IXpsOMDictionary**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                                             | <span data-ttu-id="a9e8e-123">Contiene un dizionario risorse.</span><span class="sxs-lookup"><span data-stu-id="a9e8e-123">Contains a resource dictionary.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="a9e8e-124">**IXpsOMDictionary**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-124">**IXpsOMDictionary**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)<br/>                                                                                                                                     | <span data-ttu-id="a9e8e-125">nessuno</span><span class="sxs-lookup"><span data-stu-id="a9e8e-125">None</span></span><br/>                                                                                                                                                                                                     | <span data-ttu-id="a9e8e-126">Fa riferimento alle risorse condivise da altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="a9e8e-126">References the resources that are shared by other objects.</span></span><br/>                                                                              |
| [<span data-ttu-id="a9e8e-127">**IXpsOMStoryFragmentsResource**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-127">**IXpsOMStoryFragmentsResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)<br/>                                                                                                             | <span data-ttu-id="a9e8e-128">nessuno</span><span class="sxs-lookup"><span data-stu-id="a9e8e-128">None</span></span><br/>                                                                                                                                                                                                     | <span data-ttu-id="a9e8e-129">Consente di accedere al contenuto del flusso di risorse della parte StoryFragments del documento.</span><span class="sxs-lookup"><span data-stu-id="a9e8e-129">Provides access to the content of the resource stream of the StoryFragments part of the document.</span></span><br/>                                       |



 

## <a name="related-topics"></a><span data-ttu-id="a9e8e-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9e8e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9e8e-131">**Interfaccia IXpsOMDictionary**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-131">**IXpsOMDictionary Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary)
</dt> <dt>

[<span data-ttu-id="a9e8e-132">**IXpsOMDocumentStructureResource**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-132">**IXpsOMDocumentStructureResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
</dt> <dt>

[<span data-ttu-id="a9e8e-133">**Interfaccia IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-133">**IXpsOMPage Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="a9e8e-134">**Interfaccia IXpsOMRemoteDictionaryResource**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-134">**IXpsOMRemoteDictionaryResource Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresource)
</dt> <dt>

[<span data-ttu-id="a9e8e-135">**Interfaccia IXpsOMRemoteDictionaryResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-135">**IXpsOMRemoteDictionaryResourceCollection Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)
</dt> <dt>

[<span data-ttu-id="a9e8e-136">**Interfaccia IXpsOMStoryFragmentsResource**</span><span class="sxs-lookup"><span data-stu-id="a9e8e-136">**IXpsOMStoryFragmentsResource Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomstoryfragmentsresource)
</dt> </dl>

 

 




