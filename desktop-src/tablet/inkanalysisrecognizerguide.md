---
description: Specifica la guida o l'area in cui viene disegnato e riconosciuto l'input penna.
ms.assetid: 5bd874ff-003b-4471-b4ef-50731007dc5a
title: Struttura InkAnalysisRecognizerGuide (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerGuide
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: eab5b1d09354f021f2c0a7e66a41b53e761d51e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306741"
---
# <a name="inkanalysisrecognizerguide-structure"></a><span data-ttu-id="06fb7-103">Struttura InkAnalysisRecognizerGuide</span><span class="sxs-lookup"><span data-stu-id="06fb7-103">InkAnalysisRecognizerGuide structure</span></span>

<span data-ttu-id="06fb7-104">Specifica la guida o l'area in cui viene disegnato e riconosciuto l'input penna.</span><span class="sxs-lookup"><span data-stu-id="06fb7-104">Specifies the guide, or area where ink is drawn and recognized.</span></span>

## <a name="syntax"></a><span data-ttu-id="06fb7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06fb7-105">Syntax</span></span>


```C++
typedef struct InkAnalysisRecognizerGuide {
  RECT rectWritingBox;
  RECT rectDrawnBox;
  long cRows;
  long cColumns;
  long midline;
} InkAnalysisRecognizerGuide;
```



## <a name="members"></a><span data-ttu-id="06fb7-106">Members</span><span class="sxs-lookup"><span data-stu-id="06fb7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="06fb7-107">**rectWritingBox**</span><span class="sxs-lookup"><span data-stu-id="06fb7-107">**rectWritingBox**</span></span>
</dt> <dd>

<span data-ttu-id="06fb7-108">Area di scrittura invisibile della Guida al riconoscimento in cui è possibile eseguire effettivamente la scrittura.</span><span class="sxs-lookup"><span data-stu-id="06fb7-108">The invisible writing area of the recognition guide in which writing can actually take place.</span></span>

</dd> <dt>

<span data-ttu-id="06fb7-109">**rectDrawnBox**</span><span class="sxs-lookup"><span data-stu-id="06fb7-109">**rectDrawnBox**</span></span>
</dt> <dd>

<span data-ttu-id="06fb7-110">Rettangolo disegnato sulla schermata del tablet e in cui viene effettuato la scrittura.</span><span class="sxs-lookup"><span data-stu-id="06fb7-110">The rectangle that is drawn on the tablet screen and in which writing takes place.</span></span>

</dd> <dt>

<span data-ttu-id="06fb7-111">**Corvi**</span><span class="sxs-lookup"><span data-stu-id="06fb7-111">**cRows**</span></span>
</dt> <dd>

<span data-ttu-id="06fb7-112">Il numero di righe nella casella della Guida per il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="06fb7-112">The number of rows in the recognition guide box.</span></span>

</dd> <dt>

<span data-ttu-id="06fb7-113">**cColumns**</span><span class="sxs-lookup"><span data-stu-id="06fb7-113">**cColumns**</span></span>
</dt> <dd>

<span data-ttu-id="06fb7-114">Il numero di colonne nella casella della Guida per il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="06fb7-114">The number of columns in the recognition guide box.</span></span>

</dd> <dt>

<span data-ttu-id="06fb7-115">**midline**</span><span class="sxs-lookup"><span data-stu-id="06fb7-115">**midline**</span></span>
</dt> <dd>

<span data-ttu-id="06fb7-116">Altezza della linea media della casella della Guida per il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="06fb7-116">The midline height of the recognition guide box.</span></span> <span data-ttu-id="06fb7-117">L'altezza del midline è la distanza tra la linea di base e la linea media, della casella disegnata.</span><span class="sxs-lookup"><span data-stu-id="06fb7-117">The midline height is the distance from the baseline to the midline, of the drawn box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06fb7-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="06fb7-118">Remarks</span></span>

<span data-ttu-id="06fb7-119">Un **InkAnalysisRecognizerGuide** definisce un'area di input prevista, ad esempio una riga o caselle, per i caratteri.</span><span class="sxs-lookup"><span data-stu-id="06fb7-119">An **InkAnalysisRecognizerGuide** defines an expected area of input, such as a line or boxes, for characters.</span></span> <span data-ttu-id="06fb7-120">Una struttura **InkAnalysisRecognizerGuide** può essere impostata solo in un nodo di contesto dell'hint di analisi (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)).</span><span class="sxs-lookup"><span data-stu-id="06fb7-120">An **InkAnalysisRecognizerGuide** structure can be set only on an analysis hint context node (see [**IContextNode::GetType**](icontextnode-gettype.md)).</span></span> <span data-ttu-id="06fb7-121">[**IInkAnalyzer**](iinkanalyzer.md) usa il percorso del nodo hint di analisi e i percorsi dei tratti di input penna per associare un tratto al nodo hint di analisi.</span><span class="sxs-lookup"><span data-stu-id="06fb7-121">The [**IInkAnalyzer**](iinkanalyzer.md) uses the location of the analysis hint node and the locations of the ink strokes to associate a stroke with the analysis hint node.</span></span> <span data-ttu-id="06fb7-122">Tutti i tratti con un'associazione al nodo hint di analisi avranno il **InkAnalysisRecognizerGuide** specificato usato quando riconosciuti da un **IInkAnalyzer**, purché **IInkAnalyzer** supporti **InkAnalysisRecognizerGuide**.</span><span class="sxs-lookup"><span data-stu-id="06fb7-122">Any strokes with an association to the analysis hint node will have the specified **InkAnalysisRecognizerGuide** used when recognized by an **IInkAnalyzer**, provided the **IInkAnalyzer** supports the **InkAnalysisRecognizerGuide**.</span></span> <span data-ttu-id="06fb7-123">I valori espressi nella classe **InkAnalysisRecognizerGuide** sono sempre relativi alla posizione del nodo hint di analisi e sono specificati nelle coordinate dello spazio di input penna.</span><span class="sxs-lookup"><span data-stu-id="06fb7-123">The values expressed in the **InkAnalysisRecognizerGuide** class are always relative to the location of the analysis hint node and are specified in ink space coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="06fb7-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06fb7-124">Requirements</span></span>



| <span data-ttu-id="06fb7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="06fb7-125">Requirement</span></span> | <span data-ttu-id="06fb7-126">Valore</span><span class="sxs-lookup"><span data-stu-id="06fb7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06fb7-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06fb7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="06fb7-128">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="06fb7-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="06fb7-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06fb7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="06fb7-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="06fb7-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="06fb7-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06fb7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="06fb7-132"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="06fb7-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06fb7-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06fb7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06fb7-134">Proprietà hint di analisi</span><span class="sxs-lookup"><span data-stu-id="06fb7-134">Analysis Hint Properties</span></span>](analysis-hint-properties.md)
</dt> <dt>

[<span data-ttu-id="06fb7-135">**Metodo IInkAnalyzer:: CreateAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="06fb7-135">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="06fb7-136">**IContextNode:: AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="06fb7-136">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="06fb7-137">**IContextNode:: GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="06fb7-137">**IContextNode::GetPropertyData**</span></span>](icontextnode-getpropertydata.md)
</dt> <dt>

[<span data-ttu-id="06fb7-138">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="06fb7-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




