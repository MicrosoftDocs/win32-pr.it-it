---
description: Esempio di filtri di origine push
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: Esempio di filtri di origine push
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce22c7c6d73f54152ce469b4b3bb40c20db6c29
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521330"
---
# <a name="push-source-filters-sample"></a><span data-ttu-id="11347-103">Esempio di filtri di origine push</span><span class="sxs-lookup"><span data-stu-id="11347-103">Push Source Filters Sample</span></span>

## <a name="description"></a><span data-ttu-id="11347-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11347-104">Description</span></span>

<span data-ttu-id="11347-105">Questo esempio è costituito da un set di tre filtri di origine che forniscono i dati di origine seguenti come flusso video:</span><span class="sxs-lookup"><span data-stu-id="11347-105">This sample consists of a set of three source filters that provide the following source data as a video stream:</span></span>

-   <span data-ttu-id="11347-106">CPushSourceBitmap: singola bitmap (caricata dalla directory corrente)</span><span class="sxs-lookup"><span data-stu-id="11347-106">CPushSourceBitmap: Single bitmap (loaded from current directory)</span></span>
-   <span data-ttu-id="11347-107">CPushSourceBitmapSet: set di bitmap (caricato dalla directory corrente)</span><span class="sxs-lookup"><span data-stu-id="11347-107">CPushSourceBitmapSet: Set of bitmaps (loaded from current directory)</span></span>
-   <span data-ttu-id="11347-108">CPushSourceDesktop: copia dell'immagine desktop corrente (solo GDI)</span><span class="sxs-lookup"><span data-stu-id="11347-108">CPushSourceDesktop: Copy of current desktop image (GDI only)</span></span>

## <a name="usage"></a><span data-ttu-id="11347-109">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="11347-109">Usage</span></span>

<span data-ttu-id="11347-110">Per usare un filtro, caricarlo in GraphEdit ed eseguirne il rendering del PIN di output.</span><span class="sxs-lookup"><span data-stu-id="11347-110">To use a filter, load it into GraphEdit and render its output pin.</span></span> <span data-ttu-id="11347-111">Questo consentirà di connettere un renderer video (e possibilmente un filtro del convertitore dello spazio colore) e di visualizzare l'output.</span><span class="sxs-lookup"><span data-stu-id="11347-111">This will connect a video renderer (and possibly a Color Space Converter filter) and allow you to display the output.</span></span> <span data-ttu-id="11347-112">Se si vuole eseguire il rendering dell'output in un file AVI, caricare il mux di file AVI, caricare un filtro del writer di file, specificare un nome di output per il writer di file ed eseguire il rendering del PIN di output del filtro PushSource.</span><span class="sxs-lookup"><span data-stu-id="11347-112">If you want to render the output to an AVI file, load the AVI Mux, load a File Writer Filter, provide an output name to the File Writer, and render the PushSource filter's output pin.</span></span> <span data-ttu-id="11347-113">È anche possibile caricare e connettere i commediatori video, gli effetti video e così via.</span><span class="sxs-lookup"><span data-stu-id="11347-113">You can also load and connect video compressors, video effects, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="11347-114">Il filtro di acquisizione desktop non supporta le sovrapposizioni hardware, quindi non acquisisce il rendering del video in una superficie sovrapposta o i cursori visualizzati tramite la sovrapposizione hardware.</span><span class="sxs-lookup"><span data-stu-id="11347-114">The desktop capture filter does not support hardware overlays, so it will not capture video rendered to an overlay surface or cursors displayed via hardware overlay.</span></span> <span data-ttu-id="11347-115">USA GDI per convertire l'immagine desktop corrente in una bitmap, che viene passata al pin di output come esempio multimediale.</span><span class="sxs-lookup"><span data-stu-id="11347-115">It uses GDI to convert the current desktop image into a bitmap, which is passed to the output pin as a media sample.</span></span>

 

## <a name="downloading-the-sample"></a><span data-ttu-id="11347-116">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="11347-116">Downloading the Sample</span></span>

<span data-ttu-id="11347-117">Per scaricare gli esempi di DirectShow SDK, installare la versione più recente del [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="11347-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="11347-118">Questo esempio viene installato nel percorso seguente: esempi *\[ radice \] SDK* \\ \\ \\ filtri DirectShow multimediali \\ \\ PushSource.</span><span class="sxs-lookup"><span data-stu-id="11347-118">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\PushSource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11347-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11347-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11347-120">Esempi di DirectShow</span><span class="sxs-lookup"><span data-stu-id="11347-120">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



