---
description: Queste costanti definiscono i valori che specificano il tipo di oggetti IContextNode.
ms.assetid: 333db79e-f503-4545-84fd-7c1a39a96728
title: Tipi di nodo di contesto (Iaguid. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNT_ANALYSISHINT
- GUID_CNT_CUSTOMRECOGNIZER
- GUID_CNT_IMAGE
- GUID_CNT_INKBULLET
- GUID_CNT_INKDRAWING
- GUID_CNT_INKWORD
- GUID_CNT_LINE
- GUID_CNT_OBJECT
- GUID_CNT_PARAGRAPH
- GUID_CNT_ROOT
- GUID_CNT_TEXTWORD
- GUID_CNT_UNCLASSIFIEDINKNODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 918b7cf818ebcedc98f45bff7c41ee66ad4d1592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127815"
---
# <a name="context-node-types"></a><span data-ttu-id="b55e2-103">Tipi di nodo di contesto</span><span class="sxs-lookup"><span data-stu-id="b55e2-103">Context Node Types</span></span>

<span data-ttu-id="b55e2-104">Queste costanti definiscono i valori che specificano il tipo di oggetti [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="b55e2-104">These constants define values that specify the type of [**IContextNode**](icontextnode.md) objects.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b55e2-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="b55e2-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b55e2-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b55e2-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl> <span data-ttu-id="b55e2-107"><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(ANALYSISHINT)</dt> </span><span class="sxs-lookup"><span data-stu-id="b55e2-107"><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(AnalysisHint)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b55e2-108">Rappresenta un nodo che contiene informazioni aggiuntive sul contesto per un'area utilizzata da <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> per migliorare l'analisi.</span><span class="sxs-lookup"><span data-stu-id="b55e2-108">Represents a node that contains additional context information for a region that the <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> uses to improve its analysis.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl> <span data-ttu-id="b55e2-109"><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(CUSTOMRECOGNIZER)</dt> </span><span class="sxs-lookup"><span data-stu-id="b55e2-109"><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(CustomRecognizer)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b55e2-110">Rappresenta un nodo utilizzato per una singola operazione di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="b55e2-110">Represents a node used for a single recognition operation.</span></span><br/> <span data-ttu-id="b55e2-111">Tutti i tratti e i nodi all'interno di un nodo di riconoscimento personalizzato sono riconosciuti da un'operazione di riconoscimento indipendente e non vengono analizzati da <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b55e2-111">All strokes and nodes that are within a custom recognizer node are recognized by an independent recognition operation and are not analyzed by the <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>.</span></span><br/> <span data-ttu-id="b55e2-112">Un nodo di riconoscimento personalizzato deve essere il figlio diretto del nodo radice dell'analizzatore di input penna.</span><span class="sxs-lookup"><span data-stu-id="b55e2-112">A custom recognizer node must be the direct child of ink analyzer's root node.</span></span><br/> <span data-ttu-id="b55e2-113">Un nodo di riconoscimento personalizzato può contenere i seguenti tipi di elementi figlio:</span><span class="sxs-lookup"><span data-stu-id="b55e2-113">A custom recognizer node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="b55e2-114">Qualsiasi numero di nodi UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="b55e2-114">Any number of UnclassifiedInk nodes.</span></span></li>
<li><span data-ttu-id="b55e2-115">Qualsiasi numero di nodi oggetto.</span><span class="sxs-lookup"><span data-stu-id="b55e2-115">Any number of Object nodes.</span></span></li>
<li><span data-ttu-id="b55e2-116">Qualsiasi numero di nodi riga.</span><span class="sxs-lookup"><span data-stu-id="b55e2-116">Any number of Line nodes.</span></span></li>
<li><span data-ttu-id="b55e2-117">Qualsiasi numero di nodi InkWord.</span><span class="sxs-lookup"><span data-stu-id="b55e2-117">Any number of InkWord nodes.</span></span></li>
<li><span data-ttu-id="b55e2-118">Qualsiasi numero di nodi con un valore Guid sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b55e2-118">Any number of nodes with an unknown Guid value.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl> <span data-ttu-id="b55e2-119"><dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(immagine)</dt> </span><span class="sxs-lookup"><span data-stu-id="b55e2-119"><dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(Image)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b55e2-120">Rappresenta un nodo per un'area bidimensionale in cui è possibile che nel documento siano presenti immagini non input penna.</span><span class="sxs-lookup"><span data-stu-id="b55e2-120">Represents a node for a two-dimensional region where any non-ink images can exist in the document.</span></span><br/> <span data-ttu-id="b55e2-121"><a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> non produce nodi Image.</span><span class="sxs-lookup"><span data-stu-id="b55e2-121">The <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> does not produce image nodes.</span></span> <span data-ttu-id="b55e2-122">Usare <a href="icontextnode-createsubnode.md"><strong>IContextNode:: CreateSubNode</strong></a> per aggiungere un nodo immagine alla struttura ad albero del nodo di contesto.</span><span class="sxs-lookup"><span data-stu-id="b55e2-122">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode</strong></a> to add an image node to the context node tree.</span></span> <span data-ttu-id="b55e2-123">Il <strong>IInkAnalyzer</strong> usa quindi le aree definite dal nodo immagine per determinare se un input penna annota l'immagine non input penna.</span><span class="sxs-lookup"><span data-stu-id="b55e2-123">The <strong>IInkAnalyzer</strong> then uses the regions defined by the image node to determine if any ink annotates the non-ink image.</span></span><br/> <span data-ttu-id="b55e2-124">Un nodo immagine non può contenere elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="b55e2-124">An image node cannot have any child elements.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl> <span data-ttu-id="b55e2-125"><dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(INKBULLET)</dt> </span><span class="sxs-lookup"><span data-stu-id="b55e2-125"><dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(InkBullet)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b55e2-126">InkBullet ContextNodeType rappresenta una raccolta di tratti che costituiscono un punto elenco in un elenco puntato.</span><span class="sxs-lookup"><span data-stu-id="b55e2-126">The InkBullet ContextNodeType represents a collection of strokes that make up a bullet in a bulleted list.</span></span><br/> <span data-ttu-id="b55e2-127">Un oggetto ContextNode di tipo InkBullet non può contenere elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="b55e2-127">A ContextNode of type InkBullet cannot have any children.</span></span> <span data-ttu-id="b55e2-128">Può essere solo un elemento figlio di un oggetto ContextNode di paragrafo.</span><span class="sxs-lookup"><span data-stu-id="b55e2-128">It can only be a child of a Paragraph ContextNode.</span></span> <span data-ttu-id="b55e2-129">In un singolo oggetto ContextNode di paragrafo può essere presente un solo InkBullet.</span><span class="sxs-lookup"><span data-stu-id="b55e2-129">Only one InkBullet can appear in a single Paragraph ContextNode.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl> <span data-ttu-id="b55e2-130"><dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(INKDRAWING)</dt> </span><span class="sxs-lookup"><span data-stu-id="b55e2-130"><dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(InkDrawing)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b55e2-131">Rappresenta un nodo per una raccolta di tratti che costituisce un disegno.</span><span class="sxs-lookup"><span data-stu-id="b55e2-131">Represents a node for a collection of strokes that constitutes a drawing.</span></span><br/> <span data-ttu-id="b55e2-132">I disegni sono tratti che vengono determinati come forme o sketch astratti.</span><span class="sxs-lookup"><span data-stu-id="b55e2-132">Drawings are strokes that are determined to be shapes or abstract sketches.</span></span> <span data-ttu-id="b55e2-133">Si tratta in genere di tratti non classificati come tratti di scrittura.</span><span class="sxs-lookup"><span data-stu-id="b55e2-133">They are generally any strokes that are not classified as writing strokes.</span></span><br/> <span data-ttu-id="b55e2-134">Un nodo di disegno input penna non può contenere elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="b55e2-134">An ink drawing node cannot have any child elements.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl> <span data-ttu-id="b55e2-135"><dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(InkWord)</dt> </span><span class="sxs-lookup"><span data-stu-id="b55e2-135"><dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(InkWord)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b55e2-136">Rappresenta un nodo per una raccolta di tratti che costituisce un raggruppamento logico per formare una parola riconoscibile.</span><span class="sxs-lookup"><span data-stu-id="b55e2-136">Represents a node for a collection of strokes that constitutes a logical grouping to form a recognizable word.</span></span><br/> <span data-ttu-id="b55e2-137">Un nodo di Word di input penna non può contenere elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="b55e2-137">An ink word node cannot contain any child elements.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl> <span data-ttu-id="b55e2-138"><dt><strong>GUID_CNT_LINE</strong></dt> <dt>(riga)</dt> </span><span class="sxs-lookup"><span data-stu-id="b55e2-138"><dt><strong>GUID_CNT_LINE</strong></dt> <dt>(Line)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b55e2-139">Rappresenta un nodo per una riga di parole.</span><span class="sxs-lookup"><span data-stu-id="b55e2-139">Represents a node for a line of words.</span></span><br/> <span data-ttu-id="b55e2-140">Un nodo linea può contenere i seguenti tipi di elementi figlio:</span><span class="sxs-lookup"><span data-stu-id="b55e2-140">A line node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="b55e2-141">Qualsiasi numero di nodi di Word di input penna.</span><span class="sxs-lookup"><span data-stu-id="b55e2-141">Any number of ink word nodes.</span></span></li>
<li><span data-ttu-id="b55e2-142">Qualsiasi numero di nodi di testo alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="b55e2-142">Any number of text word nodes.</span></span></li>
<li><span data-ttu-id="b55e2-143">Qualsiasi numero di nodi con un valore <strong>GUID</strong> sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b55e2-143">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl> <span data-ttu-id="b55e2-144"><dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(oggetto)</dt> </span><span class="sxs-lookup"><span data-stu-id="b55e2-144"><dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(Object)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b55e2-145">Rappresenta un nodo per un oggetto restituito da un &quot; riconoscimento personalizzato di un oggetto &quot; .</span><span class="sxs-lookup"><span data-stu-id="b55e2-145">Represents a node for an object that is returned from an &quot;object&quot; custom recognizer.</span></span><br/> <span data-ttu-id="b55e2-146">Un nodo oggetto non può contenere elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="b55e2-146">An object node cannot contain any child elements.</span></span><br/> <span data-ttu-id="b55e2-147">Solo i nodi di riconoscimento personalizzati possono contenere nodi oggetto.</span><span class="sxs-lookup"><span data-stu-id="b55e2-147">Only custom recognizer nodes can contain object nodes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl> <span data-ttu-id="b55e2-148"><dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(paragrafo)</dt> </span><span class="sxs-lookup"><span data-stu-id="b55e2-148"><dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(Paragraph)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b55e2-149">Rappresenta un nodo per una raccolta di nodi che costituisce un raggruppamento logico di righe.</span><span class="sxs-lookup"><span data-stu-id="b55e2-149">Represents a node for a collection of nodes that constitutes a logical grouping of lines.</span></span><br/> <span data-ttu-id="b55e2-150">La definizione esatta di un paragrafo è determinata dai motori di analisi.</span><span class="sxs-lookup"><span data-stu-id="b55e2-150">The exact definition of a paragraph is determined by the analyzing engines.</span></span> <span data-ttu-id="b55e2-151">In generale, un paragrafo contiene gruppi di righe che vengono riflussi insieme se la casella che contiene le righe è stata ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="b55e2-151">In general, a paragraph contains groups of lines that would reflow together if the box that contains the lines were resized.</span></span><br/> <span data-ttu-id="b55e2-152">Un nodo di paragrafo può contenere i seguenti tipi di elementi figlio:</span><span class="sxs-lookup"><span data-stu-id="b55e2-152">A paragraph node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="b55e2-153">Qualsiasi numero di nodi Bullet input penna.</span><span class="sxs-lookup"><span data-stu-id="b55e2-153">Any number of ink bullet nodes.</span></span></li>
<li><span data-ttu-id="b55e2-154">Qualsiasi numero di nodi riga.</span><span class="sxs-lookup"><span data-stu-id="b55e2-154">Any number of line nodes.</span></span></li>
<li><span data-ttu-id="b55e2-155">Qualsiasi numero di nodi con un valore <strong>GUID</strong> sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b55e2-155">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl> <span data-ttu-id="b55e2-156"><dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(radice)</dt> </span><span class="sxs-lookup"><span data-stu-id="b55e2-156"><dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(Root)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b55e2-157">Rappresenta un nodo per il nodo principale di una struttura ad albero di nodi che descrivono i risultati dell'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="b55e2-157">Represents a node for the top node of a tree of nodes that describe the results of ink analysis.</span></span><br/> <span data-ttu-id="b55e2-158">I nodi radice vengono in genere ottenuti dal metodo <a href="iinkanalyzer-getrootnode.md"><strong>IInkAnalyzer:: GetRootNode Method</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b55e2-158">Root nodes are generally obtained from the <a href="iinkanalyzer-getrootnode.md"><strong>IInkAnalyzer::GetRootNode Method</strong></a> method.</span></span><br/> <span data-ttu-id="b55e2-159">Un nodo radice può contenere i seguenti tipi di elementi figlio:</span><span class="sxs-lookup"><span data-stu-id="b55e2-159">A root node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="b55e2-160">Qualsiasi numero di nodi hint di analisi.</span><span class="sxs-lookup"><span data-stu-id="b55e2-160">Any number of analysis hint nodes.</span></span></li>
<li><span data-ttu-id="b55e2-161">Qualsiasi numero di nodi di riconoscimento personalizzati.</span><span class="sxs-lookup"><span data-stu-id="b55e2-161">Any number of custom recognizer nodes.</span></span></li>
<li><span data-ttu-id="b55e2-162">Qualsiasi numero di nodi Image.</span><span class="sxs-lookup"><span data-stu-id="b55e2-162">Any number of image nodes.</span></span></li>
<li><span data-ttu-id="b55e2-163">Qualsiasi numero di nodi di disegno input penna.</span><span class="sxs-lookup"><span data-stu-id="b55e2-163">Any number of ink drawing nodes.</span></span></li>
<li><span data-ttu-id="b55e2-164">Qualsiasi numero di nodi dell'area di scrittura.</span><span class="sxs-lookup"><span data-stu-id="b55e2-164">Any number of writing region nodes.</span></span></li>
<li><span data-ttu-id="b55e2-165">Qualsiasi numero di nodi Ink non classificati.</span><span class="sxs-lookup"><span data-stu-id="b55e2-165">Any number of unclassified ink nodes.</span></span></li>
<li><span data-ttu-id="b55e2-166">Qualsiasi numero di nodi con un valore <strong>GUID</strong> sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="b55e2-166">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl> <span data-ttu-id="b55e2-167"><dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(TEXTWORD)</dt> </span><span class="sxs-lookup"><span data-stu-id="b55e2-167"><dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(TextWord)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b55e2-168">Rappresenta un nodo per l'area bidimensionale in cui è possibile che nel documento esista un testo non input penna.</span><span class="sxs-lookup"><span data-stu-id="b55e2-168">Represents a node for the two-dimensional region where any non-ink text can exist in the document.</span></span><br/> <span data-ttu-id="b55e2-169"><a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> non produce nodi di Word di testo.</span><span class="sxs-lookup"><span data-stu-id="b55e2-169">The <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> does not produce text word nodes.</span></span> <span data-ttu-id="b55e2-170">Usare <a href="icontextnode-createsubnode.md"><strong>IContextNode:: CreateSubNode</strong></a> per aggiungere un nodo della parola di testo all'albero del nodo di contesto.</span><span class="sxs-lookup"><span data-stu-id="b55e2-170">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode</strong></a> to add a text word node to the context node tree.</span></span> <span data-ttu-id="b55e2-171">Il <strong>IInkAnalyzer</strong> usa quindi le aree definite dal nodo della parola di testo per determinare se un input penna annota il testo non input penna.</span><span class="sxs-lookup"><span data-stu-id="b55e2-171">The <strong>IInkAnalyzer</strong> then uses the regions defined by the text word node to determine if any ink annotates the non-ink text.</span></span><br/> <span data-ttu-id="b55e2-172">I riconoscitori futuri possono usare l'area definita da un nodo Word di testo per determinare se un input penna annota la parola non input penna.</span><span class="sxs-lookup"><span data-stu-id="b55e2-172">Future recognizers may use the region defined by a text word node to determine if any ink annotates the non-ink word.</span></span><br/> <span data-ttu-id="b55e2-173">Un nodo di testo di Word non può contenere elementi figlio</span><span class="sxs-lookup"><span data-stu-id="b55e2-173">A text word node cannot have any child elements</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl> <span data-ttu-id="b55e2-174"><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(UnclassifiedInk)</dt> </span><span class="sxs-lookup"><span data-stu-id="b55e2-174"><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(UnclassifiedInk)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b55e2-175">Rappresenta un nodo per tutti i tratti che non sono stati ancora classificati o riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="b55e2-175">Represents a node for any strokes that have not yet been classified or recognized.</span></span><br/> <span data-ttu-id="b55e2-176">Un nodo Ink non classificato non può contenere elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="b55e2-176">An unclassified ink node cannot have any child elements.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="b55e2-177">Commenti</span><span class="sxs-lookup"><span data-stu-id="b55e2-177">Remarks</span></span>

<span data-ttu-id="b55e2-178">Per altre informazioni sui diversi tipi di nodo di contesto, vedere [Cenni preliminari sull'analisi dell'input penna](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b55e2-178">For more information about the different context node types, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b55e2-179">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b55e2-179">Requirements</span></span>



| <span data-ttu-id="b55e2-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="b55e2-180">Requirement</span></span> | <span data-ttu-id="b55e2-181">Valore</span><span class="sxs-lookup"><span data-stu-id="b55e2-181">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b55e2-182">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b55e2-182">Minimum supported client</span></span><br/> | <span data-ttu-id="b55e2-183">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b55e2-183">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b55e2-184">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b55e2-184">Minimum supported server</span></span><br/> | <span data-ttu-id="b55e2-185">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b55e2-185">None supported</span></span><br/>                                                           |
| <span data-ttu-id="b55e2-186">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b55e2-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="b55e2-187"><dt>Iaguid. h</dt></span><span class="sxs-lookup"><span data-stu-id="b55e2-187"><dt>Iaguid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b55e2-188">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b55e2-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b55e2-189">**IContextNode:: CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="b55e2-189">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="b55e2-190">**IContextNode:: CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="b55e2-190">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="b55e2-191">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="b55e2-191">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
</dt> <dt>

[<span data-ttu-id="b55e2-192">**Metodo IInkAnalyzer:: CreateAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="b55e2-192">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="b55e2-193">**Metodo IInkAnalyzer:: CreateCustomRecognizer**</span><span class="sxs-lookup"><span data-stu-id="b55e2-193">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="b55e2-194">**Metodo IInkAnalyzer:: FindNodesOfType**</span><span class="sxs-lookup"><span data-stu-id="b55e2-194">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="b55e2-195">**Metodo IInkAnalyzer:: FindNodesOfTypeForStrokes**</span><span class="sxs-lookup"><span data-stu-id="b55e2-195">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="b55e2-196">**Metodo IInkAnalyzer:: FindNodesOfTypeInSubTree**</span><span class="sxs-lookup"><span data-stu-id="b55e2-196">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="b55e2-197">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="b55e2-197">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




