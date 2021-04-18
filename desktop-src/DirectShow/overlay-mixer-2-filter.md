---
description: Filtro Overlay Mixer 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: Filtro Overlay Mixer 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22976a58b272cf04c098c102d32d154e361b8b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304173"
---
# <a name="overlay-mixer-2-filter"></a><span data-ttu-id="27794-103">Filtro Overlay Mixer 2</span><span class="sxs-lookup"><span data-stu-id="27794-103">Overlay Mixer 2 Filter</span></span>

<span data-ttu-id="27794-104">Il filtro Overlay Mixer 2 è identico al filtro per il [mixer sovrapposto](overlay-mixer-filter.md) , ad eccezione di:</span><span class="sxs-lookup"><span data-stu-id="27794-104">The Overlay Mixer 2 filter is identical to the [Overlay Mixer](overlay-mixer-filter.md) filter, except:</span></span>

-   <span data-ttu-id="27794-105">Supporta solo i tipi di supporto con formati [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="27794-105">It supports only media types with [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats.</span></span>
-   <span data-ttu-id="27794-106">Ha un merito più elevato, che consente di aggiungerlo a un grafico di filtro automaticamente.</span><span class="sxs-lookup"><span data-stu-id="27794-106">It has a higher merit, which enables it to be added to a filter graph automatically.</span></span>

<span data-ttu-id="27794-107">Il mixer sovrapposto 2 viene fornito in modo che il gestore del grafico del filtro lo aggiunga al grafico durante il rendering del video MPEG-2 non DVD.</span><span class="sxs-lookup"><span data-stu-id="27794-107">The Overlay Mixer 2 is provided so that the Filter Graph Manager will add it to the graph when it renders non-DVD MPEG-2 video.</span></span> <span data-ttu-id="27794-108">La scelta di usare il mixer di sovrimpressione o il mixer sovrapposto 2 viene gestita dal componente che compila il grafo, ovvero il gestore del grafico del filtro, il generatore di grafici di acquisizione o il generatore di grafici DVD.</span><span class="sxs-lookup"><span data-stu-id="27794-108">The choice of whether to use the Overlay Mixer or the Overlay Mixer 2 is handled by the component that builds the graph, either the Filter Graph Manager, the Capture Graph Builder, or the DVD Graph Builder.</span></span> <span data-ttu-id="27794-109">Dal punto di vista dell'applicazione, si tratta dello stesso filtro, con le stesse interfacce e funzionalità.</span><span class="sxs-lookup"><span data-stu-id="27794-109">From an application perspective, they are the same filter, with the same interfaces and functionality.</span></span>

<span data-ttu-id="27794-110">La tabella seguente contiene informazioni specifiche per il mixer sovrapposto 2.</span><span class="sxs-lookup"><span data-stu-id="27794-110">The following table contains information specific to the Overlay Mixer 2.</span></span> <span data-ttu-id="27794-111">Per tutti gli altri dati del filtro, fare riferimento alla documentazione per il mixer overlay.</span><span class="sxs-lookup"><span data-stu-id="27794-111">For all other filter data, refer to the documentation for the Overlay Mixer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="27794-112">Tipi di supporti pin di input</span><span class="sxs-lookup"><span data-stu-id="27794-112">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="27794-113">Tipo formato: Format_VIDEOINFO2</span><span class="sxs-lookup"><span data-stu-id="27794-113">Format Type: Format_VIDEOINFO2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="27794-114">CLSID filtro</span><span class="sxs-lookup"><span data-stu-id="27794-114">Filter CLSID</span></span></td>
<td><span data-ttu-id="27794-115">CLSID_OverlayMixer2</span><span class="sxs-lookup"><span data-stu-id="27794-115">CLSID_OverlayMixer2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="27794-116"><a href="merit.md">Merito</a></span><span class="sxs-lookup"><span data-stu-id="27794-116"><a href="merit.md">Merit</a></span></span></td>
<td><ul>
<li><span data-ttu-id="27794-117">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="27794-117">MERIT_UNLIKELY</span></span></li>
<li><span data-ttu-id="27794-118">Windows Vista o versioni successive: MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="27794-118">Windows Vista or later: MERIT_DO_NOT_USE</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="27794-119">In Windows Vista o versioni successive, il merito del filtro Overlay Mixer 2 è MERIT \_ non \_ \_ usare, perché i renderer video più recenti (VMR-7, VMR-9 e EVR) supportano tutti i formati **VIDEOINFOHEADER2** e pertanto non è necessario usare il mixer overlay.</span><span class="sxs-lookup"><span data-stu-id="27794-119">In Windows Vista or later, the merit of the Overlay Mixer 2 filter is MERIT\_DO\_NOT\_USE, because the newer video renderers (VMR-7, VMR-9, and EVR) all support **VIDEOINFOHEADER2** formats, and therefore it is not necessary to use the Overlay Mixer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27794-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27794-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27794-121">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="27794-121">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



