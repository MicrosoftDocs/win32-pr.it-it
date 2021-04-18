---
title: Direct2D non supporta il rendering in metafile avanzati in Internet Explorer 9
description: Direct2D non supporta il rendering in metafile avanzati in Internet Explorer 9
ms.assetid: D106FBD6-F05E-41A6-B8F8-569EB9810E2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed5ab00b12a85f62a7ff65bbc6034227ac7a5129
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "106300573"
---
# <a name="direct2d-does-not-support-rendering-to-rich-metafiles-in-internet-explorer-9"></a><span data-ttu-id="085eb-103">Direct2D non supporta il rendering in metafile avanzati in Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="085eb-103">Direct2D does not support rendering to rich metafiles in Internet Explorer 9</span></span>

## <a name="platforms"></a><span data-ttu-id="085eb-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="085eb-104">Platforms</span></span>

<span data-ttu-id="085eb-105">**Client** – Windows Vista Windows \| 7 Windows \| 8</span><span class="sxs-lookup"><span data-stu-id="085eb-105">**Clients** – Windows Vista \| Windows 7 \| Windows 8</span></span>  
<span data-ttu-id="085eb-106">**Server** : windows Server 2008 \| Windows Server 2008 R2 \| Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="085eb-106">**Servers** – Windows Server 2008 \| Windows Server 2008 R2 \| Windows Server 2012</span></span>  




## <a name="description"></a><span data-ttu-id="085eb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="085eb-107">Description</span></span>

<span data-ttu-id="085eb-108">A causa delle modifiche di rendering interne in Internet Explorer 9, le API [IHTMLElementRender::D rawtodc](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) e [IViewObject::D RAW](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) creeranno ora un metafile contenente un'unica bitmap che rappresenta il contenuto Web invece di un metafile completo contenente informazioni sul testo e sul vettore.</span><span class="sxs-lookup"><span data-stu-id="085eb-108">Due to internal rendering changes in Internet Explorer 9, the [IHTMLElementRender::DrawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85)) and [IViewObject::Draw](/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw) APIs will now create a metafile containing a single bitmap that represents the web content instead of a rich metafile containing text and vector info.</span></span> <span data-ttu-id="085eb-109">Questa modifica era dovuta al passaggio dal rendering GDI al rendering Direct2D con accelerazione hardware (D2D).</span><span class="sxs-lookup"><span data-stu-id="085eb-109">This change was due to the move from GDI rendering to hardware-accelerated Direct2D (D2D) rendering.</span></span>

<span data-ttu-id="085eb-110">Questa modifica influiscono sulle app che usano queste API e si basa su informazioni sul testo o sul vettore nel metafile.</span><span class="sxs-lookup"><span data-stu-id="085eb-110">This change affects apps that use these APIs and rely on text or vector info in the metafile.</span></span>

## <a name="manifestation"></a><span data-ttu-id="085eb-111">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="085eb-111">Manifestation</span></span>

<span data-ttu-id="085eb-112">A seconda dell'app interessata da questa modifica, gli utenti potrebbero vedere un comportamento danneggiato o errato nelle app.</span><span class="sxs-lookup"><span data-stu-id="085eb-112">Depending on the app that is affected by this change, users might see broken or incorrect behavior in their apps.</span></span>

## <a name="mitigation"></a><span data-ttu-id="085eb-113">Strategia di riduzione del rischio</span><span class="sxs-lookup"><span data-stu-id="085eb-113">Mitigation</span></span>

<span data-ttu-id="085eb-114">Le app che devono solo estrarre informazioni di testo da un documento Web (senza informazioni di posizionamento) possono usare la proprietà [InnerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) per estrarre il testo.</span><span class="sxs-lookup"><span data-stu-id="085eb-114">Apps that only need to extract text info from a web document (without positioning info) can use the [innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85)) property to extract text.</span></span>

<span data-ttu-id="085eb-115">Le app che usano IViewObject::D RAW possono usare la [funzionalità \_ IVIEWOBJECTDRAW \_ DMLT9 \_ con \_ ](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) la chiave di controllo della funzionalità GDI per ripristinare il rendering GDI se la modalità documento è la seguente:</span><span class="sxs-lookup"><span data-stu-id="085eb-115">Apps that use IViewObject::Draw can use the [FEATURE\_IVIEWOBJECTDRAW\_DMLT9\_WITH\_GDI](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85)) feature control key to revert to GDI rendering if the document mode:</span></span>

-   <span data-ttu-id="085eb-116">È minore o uguale a 8</span><span class="sxs-lookup"><span data-stu-id="085eb-116">Is less or equal to 8</span></span>
-   <span data-ttu-id="085eb-117">Il FCK autorizza l'host a usare GDI</span><span class="sxs-lookup"><span data-stu-id="085eb-117">The FCK authorizes that host to use GDI</span></span>
-   <span data-ttu-id="085eb-118">E un controller di dominio metafile viene passato all'API</span><span class="sxs-lookup"><span data-stu-id="085eb-118">And a metafile DC is passed to the API</span></span>

## <a name="resources"></a><span data-ttu-id="085eb-119">Risorse</span><span class="sxs-lookup"><span data-stu-id="085eb-119">Resources</span></span>

-   <span data-ttu-id="085eb-120">[IHTMLElementRender::D rawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="085eb-120">[IHTMLElementRender::DrawToDC](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752273(v=vs.85))</span></span>
-   [<span data-ttu-id="085eb-121">IViewObject::D RAW</span><span class="sxs-lookup"><span data-stu-id="085eb-121">IViewObject::Draw</span></span>](/windows/win32/api/oleidl/nf-oleidl-iviewobject-draw)
-   <span data-ttu-id="085eb-122">[Proprietà IHTMLElement:: innerText](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="085eb-122">[IHTMLElement::innerText Property](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752299(v=vs.85))</span></span>
-   <span data-ttu-id="085eb-123">[Controlli delle funzionalità Internet (I.. L](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="085eb-123">[Internet Feature Controls (I..L)](/previous-versions/windows/internet-explorer/ie-developer/general-info/ee330732(v=vs.85))</span></span>

 

 