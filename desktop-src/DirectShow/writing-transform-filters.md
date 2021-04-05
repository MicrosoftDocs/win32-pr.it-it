---
description: Scrittura di filtri di trasformazione
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: Scrittura di filtri di trasformazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d007181e437ef5691f532fec00923aa2b8012f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967689"
---
# <a name="writing-transform-filters"></a><span data-ttu-id="975df-103">Scrittura di filtri di trasformazione</span><span class="sxs-lookup"><span data-stu-id="975df-103">Writing Transform Filters</span></span>

<span data-ttu-id="975df-104">In questa sezione viene descritto come scrivere un filtro di trasformazione, definito come filtro con un pin di input e un pin di output identici.</span><span class="sxs-lookup"><span data-stu-id="975df-104">This section describes how to write a transform filter, defined as a filter that has exactly one input pin and one output pin.</span></span> <span data-ttu-id="975df-105">Per illustrare i passaggi, in questa sezione viene descritto un filtro di trasformazione ipotetico che restituisce il video codificato in fase di esecuzione (RLE).</span><span class="sxs-lookup"><span data-stu-id="975df-105">To illustrate the steps, this section describes a hypothetical transform filter that outputs run-length encoded (RLE) video.</span></span> <span data-ttu-id="975df-106">Non viene descritto l'algoritmo di codifica RLE, ma solo le attività specifiche di DirectShow.</span><span class="sxs-lookup"><span data-stu-id="975df-106">It does not describe the RLE-encoding algorithm itself, only the tasks that are specific to DirectShow.</span></span> <span data-ttu-id="975df-107">DirectShow fornisce già un codec RLE tramite il filtro del [compressore AVI](avi-compressor-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="975df-107">(DirectShow already provides an RLE codec through the [AVI Compressor](avi-compressor-filter.md) filter.)</span></span>

<span data-ttu-id="975df-108">Questa sezione presuppone che si userà la libreria di classi base DirectShow per creare filtri.</span><span class="sxs-lookup"><span data-stu-id="975df-108">This section assumes that you will use the DirectShow base class library to create filters.</span></span> <span data-ttu-id="975df-109">Sebbene sia possibile scrivere un filtro senza di esso, è consigliabile utilizzare la libreria di classi di base.</span><span class="sxs-lookup"><span data-stu-id="975df-109">Although you can write a filter without it, the base class library is strongly recommended.</span></span>

> [!Note]  
> <span data-ttu-id="975df-110">Prima di scrivere un filtro di trasformazione, valutare se un oggetto DMO (DirectX Media Object) soddisfi i requisiti.</span><span class="sxs-lookup"><span data-stu-id="975df-110">Before writing a transform filter, consider whether a DirectX Media Object (DMO) would fulfill your requirements.</span></span> <span data-ttu-id="975df-111">DMOs può eseguire molte delle stesse operazioni dei filtri e il modello di programmazione per DMOs è più semplice.</span><span class="sxs-lookup"><span data-stu-id="975df-111">DMOs can do many of the same things as filters, and the programming model for DMOs is simpler.</span></span> <span data-ttu-id="975df-112">DMOs sono ospitati in DirectShow tramite il filtro del [wrapper DMO](dmo-wrapper-filter.md) , ma possono essere usati anche all'esterno di DirectShow.</span><span class="sxs-lookup"><span data-stu-id="975df-112">DMOs are hosted in DirectShow through the [DMO Wrapper](dmo-wrapper-filter.md) filter, but can also be used outside of DirectShow.</span></span> <span data-ttu-id="975df-113">DMOs è ora la soluzione consigliata per codificatori e decodificatori.</span><span class="sxs-lookup"><span data-stu-id="975df-113">DMOs are now the recommended solution for encoders and decoders.</span></span>

 

<span data-ttu-id="975df-114">Questa sezione include gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="975df-114">This section includes the following topics:</span></span>

-   [<span data-ttu-id="975df-115">Passaggio 1. Scegliere una classe di base</span><span class="sxs-lookup"><span data-stu-id="975df-115">Step 1. Choose a Base Class</span></span>](step-1--choose-a-base-class.md)
-   [<span data-ttu-id="975df-116">Passaggio 2. Dichiarare la classe filter</span><span class="sxs-lookup"><span data-stu-id="975df-116">Step 2. Declare the Filter Class</span></span>](step-2--declare-the-filter-class.md)
-   [<span data-ttu-id="975df-117">Passaggio 3. Negoziazione del tipo di supporto multimediale</span><span class="sxs-lookup"><span data-stu-id="975df-117">Step 3. Support Media Type Negotiation</span></span>](step-3--support-media-type-negotiation.md)
-   [<span data-ttu-id="975df-118">Passaggio 4. Imposta proprietà allocatore</span><span class="sxs-lookup"><span data-stu-id="975df-118">Step 4. Set Allocator Properties</span></span>](step-4--set-allocator-properties.md)
-   [<span data-ttu-id="975df-119">Passaggio 5. Trasforma l'immagine</span><span class="sxs-lookup"><span data-stu-id="975df-119">Step 5. Transform the Image</span></span>](step-5--transform-the-image.md)
-   [<span data-ttu-id="975df-120">Passaggio 6. Aggiunta del supporto per COM</span><span class="sxs-lookup"><span data-stu-id="975df-120">Step 6. Add Support for COM</span></span>](step-6--add-support-for-com.md)

## <a name="related-topics"></a><span data-ttu-id="975df-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="975df-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="975df-122">Creazione di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="975df-122">Building DirectShow Filters</span></span>](building-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="975df-123">Classi base di DirectShow</span><span class="sxs-lookup"><span data-stu-id="975df-123">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="975df-124">Scrittura di filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="975df-124">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



