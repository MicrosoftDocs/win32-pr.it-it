---
description: Rappresenta la possibilità di analizzare il layout di una raccolta di tratti e di suddividerli in testo e grafica.
ms.assetid: 2c8e67fb-1032-4fcc-b419-82bae978daf8
title: Classe InkDivider (Msinkaut15. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDivider
- InkDivider.IInkDivider
api_type:
- COM
api_location:
- Inkdiv.dll
- Inkdiv.dll.dll
ms.openlocfilehash: c0658504303968803bd2abff063694701d121390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316852"
---
# <a name="inkdivider-class"></a><span data-ttu-id="07028-103">Classe InkDivider</span><span class="sxs-lookup"><span data-stu-id="07028-103">InkDivider class</span></span>

<span data-ttu-id="07028-104">Rappresenta la possibilità di analizzare il layout di una raccolta di tratti e di suddividerli in testo e grafica.</span><span class="sxs-lookup"><span data-stu-id="07028-104">Represents the ability to analyze the layout of a collection of strokes and divide them into text and graphics.</span></span>

<span data-ttu-id="07028-105">**InkDivider** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="07028-105">**InkDivider** has these types of members:</span></span>

-   [<span data-ttu-id="07028-106">Interfacce</span><span class="sxs-lookup"><span data-stu-id="07028-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="07028-107">Metodi</span><span class="sxs-lookup"><span data-stu-id="07028-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="07028-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07028-108">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="07028-109">Interfacce</span><span class="sxs-lookup"><span data-stu-id="07028-109">Interfaces</span></span>

<span data-ttu-id="07028-110">La classe **InkDivider** definisce queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="07028-110">The **InkDivider** class defines these interfaces.</span></span>



| <span data-ttu-id="07028-111">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="07028-111">Interface</span></span>       | <span data-ttu-id="07028-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07028-112">Description</span></span>                                                          |
|:----------------|:---------------------------------------------------------------------|
| <span data-ttu-id="07028-113">**IInkDivider**</span><span class="sxs-lookup"><span data-stu-id="07028-113">**IInkDivider**</span></span> | <span data-ttu-id="07028-114">Questo oggetto implementa l'interfaccia com **IInkDivider** .</span><span class="sxs-lookup"><span data-stu-id="07028-114">This object implements the **IInkDivider** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="07028-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="07028-115">Methods</span></span>

<span data-ttu-id="07028-116">La classe **InkDivider** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="07028-116">The **InkDivider** class has these methods.</span></span>



| <span data-ttu-id="07028-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="07028-117">Method</span></span>                              | <span data-ttu-id="07028-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07028-118">Description</span></span>                                                                                                                                                        |
|:------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07028-119">**Dividere**</span><span class="sxs-lookup"><span data-stu-id="07028-119">**Divide**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) | <span data-ttu-id="07028-120">Restituisce un oggetto [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) che contiene informazioni strutturali sui tratti nell'oggetto **InkDivider** .</span><span class="sxs-lookup"><span data-stu-id="07028-120">Returns an [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object that contains structural information about the strokes in the **InkDivider** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="07028-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07028-121">Properties</span></span>

<span data-ttu-id="07028-122">La classe **InkDivider** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="07028-122">The **InkDivider** class has these properties.</span></span>



| <span data-ttu-id="07028-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07028-123">Property</span></span>                                                             | <span data-ttu-id="07028-124">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="07028-124">Access type</span></span>           | <span data-ttu-id="07028-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07028-125">Description</span></span>                                                                                                                     |
|:---------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="07028-126">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="07028-126">**LineHeight**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)<br/>               | <span data-ttu-id="07028-127">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="07028-127">Read/write</span></span><br/> | <span data-ttu-id="07028-128">Ottiene o imposta l'altezza della grafia prevista in unità HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="07028-128">Gets or sets the expected handwriting height in HIMETRIC units.</span></span><br/>                                                      |
| [<span data-ttu-id="07028-129">**RecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="07028-129">**RecognizerContext**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)<br/> | <span data-ttu-id="07028-130">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="07028-130">Read/write</span></span><br/> | <span data-ttu-id="07028-131">Ottiene o imposta l'oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) utilizzato per il riconoscimento della grafia.</span><span class="sxs-lookup"><span data-stu-id="07028-131">Gets or sets the [**InkRecognizerContext**](inkrecognizercontext-class.md) object used for handwriting recognition.</span></span><br/> |
| [<span data-ttu-id="07028-132">**Tratti**</span><span class="sxs-lookup"><span data-stu-id="07028-132">**Strokes**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)<br/>                     | <span data-ttu-id="07028-133">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="07028-133">Read/write</span></span><br/> | <span data-ttu-id="07028-134">Ottiene o imposta la raccolta [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contenuta dall'oggetto **InkDivider** .</span><span class="sxs-lookup"><span data-stu-id="07028-134">Gets or sets the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection contained by the **InkDivider** object.</span></span> <br/>     |



 

## <a name="remarks"></a><span data-ttu-id="07028-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="07028-135">Remarks</span></span>

<span data-ttu-id="07028-136">È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.</span><span class="sxs-lookup"><span data-stu-id="07028-136">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="07028-137">L'oggetto **InkDivider** usa il layout dei tratti, l'ordine in cui vengono aggiunti i tratti, la direzione in cui vengono disegnati i tratti e altri fattori per eseguire l'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="07028-137">The **InkDivider** object uses the layout of the strokes, the order in which the strokes are added, the direction in which the strokes are drawn, and other factors to perform the analysis of the ink.</span></span> <span data-ttu-id="07028-138">La raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) analizzata dall'oggetto **InkDivider** è contenuta nella proprietà [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) dell'oggetto **InkDivider** .</span><span class="sxs-lookup"><span data-stu-id="07028-138">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the **InkDivider** object analyzes is contained in the [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) property of the **InkDivider** object.</span></span> <span data-ttu-id="07028-139">L'oggetto **InkDivider** analizza dinamicamente la raccolta InkStrokes quando si aggiunge o si elimina dalla raccolta, ma non esegue alcuna modifica dei tratti.</span><span class="sxs-lookup"><span data-stu-id="07028-139">The **InkDivider** object dynamically analyzes the InkStrokes collection as you add to or delete from the collection, but it performs no modification of the strokes.</span></span>

<span data-ttu-id="07028-140">I risultati dell'analisi vengono restituiti in un oggetto [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="07028-140">The analysis results are returned in an [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

<span data-ttu-id="07028-141">L'oggetto **InkDivider** usa un oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) per dividere più accuratamente i tratti e per assegnare una stringa di riconoscimento ai risultati.</span><span class="sxs-lookup"><span data-stu-id="07028-141">The **InkDivider** object uses an [**InkRecognizerContext**](inkrecognizercontext-class.md) object to more accurately divide the strokes and to assign a recognition string to the results.</span></span>

> [!Note]  
> <span data-ttu-id="07028-142">L'oggetto **InkDivider** utilizza le impostazioni predefinite delle proprietà dell'oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="07028-142">The **InkDivider** object uses the default property settings of the [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

 

<span data-ttu-id="07028-143">Se non si assegna un contesto di riconoscimento all'oggetto **InkDivider** , l'oggetto **InkDivider** analizza ancora l'input penna, ma divide i tratti in modo meno accurato e non associa il testo ai risultati della divisione.</span><span class="sxs-lookup"><span data-stu-id="07028-143">If you do not assign a recognizer context to the **InkDivider** object, the **InkDivider** object still analyzes the ink, but it divides the strokes less accurately and does not associate text with the division results.</span></span>

> [!Note]  
> <span data-ttu-id="07028-144">Prima di aggiungere tratti alla proprietà [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) , è necessario impostare la proprietà [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) .</span><span class="sxs-lookup"><span data-stu-id="07028-144">The [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property should be set before adding strokes to the [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) property.</span></span> <span data-ttu-id="07028-145">Una volta aggiunti i tratti all'oggetto **InkDivider** , non è possibile modificare la proprietà **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="07028-145">After strokes have been added to the **InkDivider** object, the **RecognizerContext** property cannot be changed.</span></span>

 

<span data-ttu-id="07028-146">Il **InkDivider** non supporta attualmente le lingue verticali.</span><span class="sxs-lookup"><span data-stu-id="07028-146">The **InkDivider** does not currently support vertical languages.</span></span> <span data-ttu-id="07028-147">Affinché l'oggetto **InkDivider** riconosca tali lingue in modo appropriato, l'oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) per la lingua deve supportare la funzionalità di input libero e i caratteri devono essere scritti da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="07028-147">For the **InkDivider** object to recognize these languages properly the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object for the language must support the free input capability and the characters must be written from left to right.</span></span>

## <a name="requirements"></a><span data-ttu-id="07028-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07028-148">Requirements</span></span>



| <span data-ttu-id="07028-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="07028-149">Requirement</span></span> | <span data-ttu-id="07028-150">Valore</span><span class="sxs-lookup"><span data-stu-id="07028-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07028-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07028-151">Minimum supported client</span></span><br/> | <span data-ttu-id="07028-152">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="07028-152">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="07028-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07028-153">Minimum supported server</span></span><br/> | <span data-ttu-id="07028-154">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="07028-154">None supported</span></span><br/>                                                                                               |
| <span data-ttu-id="07028-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07028-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="07028-156"><dt>Msinkaut15. h (richiede anche Msinkaut15 \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="07028-156"><dt>Msinkaut15.h (also requires Msinkaut15\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="07028-157">Libreria</span><span class="sxs-lookup"><span data-stu-id="07028-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="07028-158"><dt>Inkdiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07028-158"><dt>Inkdiv.dll</dt></span></span> </dl>                                   |



## <a name="see-also"></a><span data-ttu-id="07028-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07028-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07028-160">**Interfaccia IInkDivisionResult**</span><span class="sxs-lookup"><span data-stu-id="07028-160">**IInkDivisionResult Interface**</span></span>](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)
</dt> <dt>

[<span data-ttu-id="07028-161">**Classe InkRecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="07028-161">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

<span data-ttu-id="07028-162">[Raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="07028-162">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> </dl>

 

