---
description: Componente Windows Imaging
ms.assetid: b872baf9-9fcb-4604-a518-26e109eda792
title: Componente Windows Imaging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00bb18e2e432abbe3cfb3b72d28ceb4182e63ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232470"
---
# <a name="windows-imaging-component"></a><span data-ttu-id="dbbe4-103">Componente Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="dbbe4-103">Windows Imaging Component</span></span>

## <a name="purpose"></a><span data-ttu-id="dbbe4-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="dbbe4-104">Purpose</span></span>

<span data-ttu-id="dbbe4-105">Windows Imaging Component (WIC) è una piattaforma estendibile che fornisce un'API di basso livello per le immagini digitali.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-105">The Windows Imaging Component (WIC) is an extensible platform that provides low-level API for digital images.</span></span>  <span data-ttu-id="dbbe4-106">WIC supporta i formati di immagine Web standard, le immagini con intervallo dinamico elevato e i dati delle fotocamere non elaborate.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-106">WIC supports the standard web image formats, high dynamic range images, and raw camera data.</span></span>  <span data-ttu-id="dbbe4-107">WIC supporta inoltre funzionalità aggiuntive, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="dbbe4-107">WIC also supports additional features such as:</span></span>

-   <span data-ttu-id="dbbe4-108">Supporto incorporato per i formati di metadati standard</span><span class="sxs-lookup"><span data-stu-id="dbbe4-108">Built-in support for standard metadata formats</span></span>
-   <span data-ttu-id="dbbe4-109">Framework estensibile per codec di immagini, formati pixel e formati di metadati.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-109">Extensible framework for image codecs, pixel formats, and metadata formats.</span></span>
-   <span data-ttu-id="dbbe4-110">Ampia gamma di supporto per il formato pixel.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-110">Wide range of pixel format support.</span></span>
-   <span data-ttu-id="dbbe4-111">Supporto per colori elevati; inclusi i formati di intervallo esteso a 30 bit, a 32 bit e di precisione elevata e a 48 bit e i formati pixel a gamma ampia.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-111">High-color support; including 30-bit extended range, 30-bit high precision, and 48-bit high precision and wide gamut pixel formats.</span></span>
-   <span data-ttu-id="dbbe4-112">Decodifica di immagini progressive.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-112">Progressive image decoding.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="dbbe4-113">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="dbbe4-113">Developer Audience</span></span>

<span data-ttu-id="dbbe4-114">WIC è progettato per soddisfare le esigenze delle classi di sviluppatori seguenti:</span><span class="sxs-lookup"><span data-stu-id="dbbe4-114">WIC is designed to meet the needs of the following classes of developers:</span></span>

-   <span data-ttu-id="dbbe4-115">Sviluppatori che leggono e scrivono i dati delle immagini in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-115">Developers who read and write image data in an application.</span></span>
-   <span data-ttu-id="dbbe4-116">Sviluppatori che leggono e scrivono i metadati delle immagini in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-116">Developers who read and write image metadata in an application.</span></span>
-   <span data-ttu-id="dbbe4-117">Sviluppatori che desiderano l'individuazione di codec di run-time per codec di immagini appena progettati o implementati.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-117">Developers who want run-time codec discovery for newly designed or implemented image codecs.</span></span>
-   <span data-ttu-id="dbbe4-118">Sviluppatori che progettano o implementano nuovi codec di immagini e formati di metadati.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-118">Developers designing or implementing new image codecs and metadata formats.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="dbbe4-119">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="dbbe4-119">In this section</span></span>



| <span data-ttu-id="dbbe4-120">Argomento</span><span class="sxs-lookup"><span data-stu-id="dbbe4-120">Topic</span></span>                                                                 | <span data-ttu-id="dbbe4-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbbe4-121">Description</span></span>                                         |
|-----------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="dbbe4-122">Novità in WIC</span><span class="sxs-lookup"><span data-stu-id="dbbe4-122">What's New in WIC</span></span>](what-s-new-in-wic-for-windows-8-1.md)<br/> |                                                     |
| [<span data-ttu-id="dbbe4-123">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="dbbe4-123">Programming Guide</span></span>](-wic-programming-guide.md)<br/>            | <span data-ttu-id="dbbe4-124">Viene descritto come utilizzare le API WIC.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-124">Describes how to use the WIC APIs.</span></span><br/>       |
| [<span data-ttu-id="dbbe4-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="dbbe4-125">Reference</span></span>](-wic-codec-reference.md)<br/>                      | <span data-ttu-id="dbbe4-126">Contiene il riferimento per le API WIC.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-126">Contains the reference for the WIC APIs.</span></span><br/> |
| [<span data-ttu-id="dbbe4-127">Esempi WIC</span><span class="sxs-lookup"><span data-stu-id="dbbe4-127">WIC Samples</span></span>](-wic-samples.md)<br/>                            | <span data-ttu-id="dbbe4-128">Fornisce esempi per WIC.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-128">Provides samples for WIC.</span></span><br/>                |
| [<span data-ttu-id="dbbe4-129">Glossario</span><span class="sxs-lookup"><span data-stu-id="dbbe4-129">Glossary</span></span>](-wic-glossary.md)<br/>                              | <span data-ttu-id="dbbe4-130">Definisce i termini utilizzati in WIC.</span><span class="sxs-lookup"><span data-stu-id="dbbe4-130">Defines terms that are used in WIC.</span></span><br/>      |



 

 

 




