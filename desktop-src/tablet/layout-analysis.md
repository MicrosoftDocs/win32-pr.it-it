---
description: L'analisi del layout opera su una raccolta Strokes e classifica i tratti in elementi di grafia e disegno. L'oggetto divisore consente di accedere alle funzionalità di analisi del layout di Tablet PC.
ms.assetid: ac30d5c2-13a1-4f9e-a519-2bf428e21c75
title: Analisi del layout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0901e7c7df96bec5ea3972f643469033fbb22ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313448"
---
# <a name="layout-analysis"></a><span data-ttu-id="6c8e3-104">Analisi del layout</span><span class="sxs-lookup"><span data-stu-id="6c8e3-104">Layout Analysis</span></span>

<span data-ttu-id="6c8e3-105">L'analisi del layout opera su una raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) e classifica i tratti in elementi di grafia e disegno.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-105">Layout analysis operates on a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection and classifies the strokes into handwriting and drawing elements.</span></span> <span data-ttu-id="6c8e3-106">L'oggetto [**divisore**](inkdivider-class.md) consente di accedere alle funzionalità di analisi del layout di Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-106">The [**Divider**](inkdivider-class.md) object provides access to the Tablet PC layout analysis features.</span></span>

<span data-ttu-id="6c8e3-107">Nella tabella seguente vengono descritti i tipi di elementi strutturali dell'enumerazione [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) in cui l'oggetto [**divisore**](inkdivider-class.md) classifica i tratti.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-107">The following table describes the structural element types of the [**InkDivisionType**](/windows/win32/api/msinkaut15/ne-msinkaut15-inkdivisiontype) enumeration into which the [**Divider**](inkdivider-class.md) object classifies strokes.</span></span>



| <span data-ttu-id="6c8e3-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c8e3-108">Type</span></span>          | <span data-ttu-id="6c8e3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c8e3-109">Description</span></span>                                                                      |
|---------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6c8e3-110">**Segmento**</span><span class="sxs-lookup"><span data-stu-id="6c8e3-110">**Segment**</span></span>   | <span data-ttu-id="6c8e3-111">Segmento di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-111">A recognition segment.</span></span><br/>                                                |
| <span data-ttu-id="6c8e3-112">**Linea**</span><span class="sxs-lookup"><span data-stu-id="6c8e3-112">**Line**</span></span>      | <span data-ttu-id="6c8e3-113">Riga di grafia che contiene uno o più segmenti di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-113">A line of handwriting that contains one or more recognition segments.</span></span><br/> |
| <span data-ttu-id="6c8e3-114">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="6c8e3-114">**Paragraph**</span></span> | <span data-ttu-id="6c8e3-115">Un blocco di tratti che contiene una o più righe di grafia.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-115">A block of strokes that contains one or more lines of handwriting.</span></span><br/>    |
| <span data-ttu-id="6c8e3-116">**Disegno**</span><span class="sxs-lookup"><span data-stu-id="6c8e3-116">**Drawing**</span></span>   | <span data-ttu-id="6c8e3-117">Input penna che non è a grafia.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-117">Ink that is not handwriting.</span></span><br/>                                          |



 

<span data-ttu-id="6c8e3-118">L' **oggetto** [**divisore**](inkdivider-class.md) dispone di una raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , che viene analizzata dinamicamente ogni volta che si aggiunge o si elimina dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-118">The [**Divider**](inkdivider-class.md) object has a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection, which the **Divider** object dynamically analyzes each time you add to or delete from the collection.</span></span> <span data-ttu-id="6c8e3-119">L'oggetto **divisore** non è serializzabile e non è possibile salvarne lo stato di analisi.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-119">The **Divider** object is not serializable, and you cannot save its analysis state.</span></span> <span data-ttu-id="6c8e3-120">Di conseguenza, l'oggetto **divisore** è progettato per le applicazioni che devono distinguere tra input grafia misto e input di disegno, ma non è necessario analizzare nuovamente grandi quantità di input penna tra le sessioni.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-120">Thus the **Divider** object is designed for applications that must differentiate between mixed handwriting and drawing input, but do not need to reanalyze large amounts of ink between sessions.</span></span>

<span data-ttu-id="6c8e3-121">È possibile ottenere uno snapshot statico del risultato dell'analisi corrente, restituito in un oggetto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="6c8e3-121">You can obtain a static snapshot of the current analysis result, which is returned in a [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span> <span data-ttu-id="6c8e3-122">È possibile ottenere oggetti [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) , ognuno dei quali rappresenta un singolo elemento strutturale di un oggetto **DivisionResult** .</span><span class="sxs-lookup"><span data-stu-id="6c8e3-122">You can obtain [**DivisionUnit**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunit) objects, each which represents a single structural element of a **DivisionResult** object.</span></span> <span data-ttu-id="6c8e3-123">Gli oggetti **DivisionResult** e **DivisionUnit** non sono serializzabili.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-123">The **DivisionResult** and **DivisionUnit** objects are not serializable.</span></span> <span data-ttu-id="6c8e3-124">Tuttavia, le informazioni sullo stato di questi oggetti sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-124">However, state information from these objects is available.</span></span>

<span data-ttu-id="6c8e3-125">L'oggetto [**divisore**](inkdivider-class.md) funziona solo con la grafia da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-125">The [**Divider**](inkdivider-class.md) object works only with left-to-right handwriting.</span></span> <span data-ttu-id="6c8e3-126">Affinché l'oggetto **divisore** analizzi correttamente le lingue verticali, ad esempio il cinese, i caratteri devono essere disegnati da sinistra a destra anziché dall'alto verso il basso.</span><span class="sxs-lookup"><span data-stu-id="6c8e3-126">For the **Divider** object to analyze vertical languages such as Chinese correctly, the characters must be drawn left-to-right instead of top-to-bottom.</span></span>

 

