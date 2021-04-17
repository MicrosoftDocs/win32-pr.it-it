---
description: Rappresenta l'area utilizzata dal riconoscitore in cui è possibile disegnare l'input penna. L'area è nota come guida al riconoscimento.
ms.assetid: c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7
title: Classe InkRecognizerGuide (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerGuide
- InkRecognizerGuide.IInkRecognizerGuide
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 55729513f748afc87f184b73eaba976184307bc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234082"
---
# <a name="inkrecognizerguide-class"></a><span data-ttu-id="4e883-104">Classe InkRecognizerGuide</span><span class="sxs-lookup"><span data-stu-id="4e883-104">InkRecognizerGuide class</span></span>

<span data-ttu-id="4e883-105">Rappresenta l'area utilizzata dal riconoscitore in cui è possibile disegnare l'input penna.</span><span class="sxs-lookup"><span data-stu-id="4e883-105">Represents the area that the recognizer uses in which ink can be drawn.</span></span> <span data-ttu-id="4e883-106">L'area è nota come guida al riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="4e883-106">The area is known as the recognition guide.</span></span>

<span data-ttu-id="4e883-107">**InkRecognizerGuide** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4e883-107">**InkRecognizerGuide** has these types of members:</span></span>

-   [<span data-ttu-id="4e883-108">Interfacce</span><span class="sxs-lookup"><span data-stu-id="4e883-108">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="4e883-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4e883-109">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="4e883-110">Interfacce</span><span class="sxs-lookup"><span data-stu-id="4e883-110">Interfaces</span></span>

<span data-ttu-id="4e883-111">La classe **InkRecognizerGuide** definisce queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="4e883-111">The **InkRecognizerGuide** class defines these interfaces.</span></span>



| <span data-ttu-id="4e883-112">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="4e883-112">Interface</span></span>               | <span data-ttu-id="4e883-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e883-113">Description</span></span>                                                                  |
|:------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="4e883-114">**IInkRecognizerGuide**</span><span class="sxs-lookup"><span data-stu-id="4e883-114">**IInkRecognizerGuide**</span></span> | <span data-ttu-id="4e883-115">Questo oggetto implementa l'interfaccia com **IInkRecognizerGuide** .</span><span class="sxs-lookup"><span data-stu-id="4e883-115">This object implements the **IInkRecognizerGuide** COM interface.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4e883-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4e883-116">Properties</span></span>

<span data-ttu-id="4e883-117">La classe **InkRecognizerGuide** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4e883-117">The **InkRecognizerGuide** class has these properties.</span></span>



| <span data-ttu-id="4e883-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4e883-118">Property</span></span>                                                       | <span data-ttu-id="4e883-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="4e883-119">Access type</span></span>           | <span data-ttu-id="4e883-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e883-120">Description</span></span>                                                                                                                    |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e883-121">**Colonne**</span><span class="sxs-lookup"><span data-stu-id="4e883-121">**Columns**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns)<br/>       | <span data-ttu-id="4e883-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4e883-122">Read/write</span></span><br/> | <span data-ttu-id="4e883-123">Ottiene o imposta il numero di colonne nella casella della guida.</span><span class="sxs-lookup"><span data-stu-id="4e883-123">Gets or sets the number of columns in the guide box.</span></span><br/>                                                                |
| [<span data-ttu-id="4e883-124">**DrawnBox**</span><span class="sxs-lookup"><span data-stu-id="4e883-124">**DrawnBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)<br/>     | <span data-ttu-id="4e883-125">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4e883-125">Read/write</span></span><br/> | <span data-ttu-id="4e883-126">Ottiene o imposta la casella che viene fisicamente disegnata nella schermata del tablet e in cui avviene la scrittura.</span><span class="sxs-lookup"><span data-stu-id="4e883-126">Gets or sets the box that is physically drawn on the tablet's screen and in which writing takes place.</span></span><br/>              |
| [<span data-ttu-id="4e883-127">**GuideData**</span><span class="sxs-lookup"><span data-stu-id="4e883-127">**GuideData**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_guidedata)<br/>   | <span data-ttu-id="4e883-128">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4e883-128">Read/write</span></span><br/> | <span data-ttu-id="4e883-129">Ottiene o imposta i dati della Guida per gli sviluppatori C++.</span><span class="sxs-lookup"><span data-stu-id="4e883-129">Gets or sets guide data for C++ developers.</span></span><br/>                                                                         |
| [<span data-ttu-id="4e883-130">**Midline**</span><span class="sxs-lookup"><span data-stu-id="4e883-130">**Midline**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_midline)<br/>       | <span data-ttu-id="4e883-131">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4e883-131">Read/write</span></span><br/> | <span data-ttu-id="4e883-132">Ottiene o imposta l'altezza del midline.</span><span class="sxs-lookup"><span data-stu-id="4e883-132">Gets or sets the midline height.</span></span> <span data-ttu-id="4e883-133">L'altezza del midline è la distanza tra la linea di base e la linea media, della casella disegnata.</span><span class="sxs-lookup"><span data-stu-id="4e883-133">The midline height is distance from the baseline to the midline, of the drawn box.</span></span><br/> |
| [<span data-ttu-id="4e883-134">**Righe**</span><span class="sxs-lookup"><span data-stu-id="4e883-134">**Rows**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows)<br/>             | <span data-ttu-id="4e883-135">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4e883-135">Read/write</span></span><br/> | <span data-ttu-id="4e883-136">Ottiene o imposta il numero di righe nella casella della guida.</span><span class="sxs-lookup"><span data-stu-id="4e883-136">Gets or sets the number of rows in the guide box.</span></span><br/>                                                                   |
| [<span data-ttu-id="4e883-137">**WritingBox**</span><span class="sxs-lookup"><span data-stu-id="4e883-137">**WritingBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)<br/> | <span data-ttu-id="4e883-138">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="4e883-138">Read/write</span></span><br/> | <span data-ttu-id="4e883-139">Ottiene o imposta l'area di scrittura invisibile della casella della Guida in cui può effettivamente essere eseguita la scrittura.</span><span class="sxs-lookup"><span data-stu-id="4e883-139">Gets or sets the invisible writing area of the guide box in which writing can actually take place.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="4e883-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e883-140">Remarks</span></span>

<span data-ttu-id="4e883-141">È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="4e883-141">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method.</span></span>

<span data-ttu-id="4e883-142">Per impostazione predefinita, non è disponibile alcuna guida per il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="4e883-142">By default, there is no recognizer guide.</span></span> <span data-ttu-id="4e883-143">Una guida predefinita ha tutti i valori delle proprietà impostati su 0.</span><span class="sxs-lookup"><span data-stu-id="4e883-143">A default guide has all property values set to 0.</span></span> <span data-ttu-id="4e883-144">Per impostare la guida, è necessario utilizzare le proprietà di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="4e883-144">You must use the properties of this object to set the guide.</span></span>

<span data-ttu-id="4e883-145">Se l'applicazione ha disegnato linee guida sullo schermo in cui si prevede che l'utente scriva, l'applicazione deve impostare i valori delle proprietà della Guida di riconoscimento per informare il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="4e883-145">If the application has drawn guidelines on the screen on which the user is expected to write, the application should set the values of the properties of the recognizer guide to inform the recognizer.</span></span> <span data-ttu-id="4e883-146">Queste proprietà sono destinate solo all'uso del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="4e883-146">These properties are for the recognizer's use only.</span></span> <span data-ttu-id="4e883-147">L'impostazione non consente di creare gli indizi visivi sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="4e883-147">Setting them does not, by itself, draw visual clues on the display.</span></span> <span data-ttu-id="4e883-148">L'applicazione o il controllo disegna gli indizi visivi.</span><span class="sxs-lookup"><span data-stu-id="4e883-148">The application or the control draws the visual clues.</span></span>

<span data-ttu-id="4e883-149">La guida per il riconoscimento può essere costituita da righe e colonne e fornisce al riconoscimento un contesto migliore in cui eseguire il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="4e883-149">The recognizer guide can consist of rows and columns, and these give the recognizer a better context in which to perform recognition.</span></span> <span data-ttu-id="4e883-150">Le lettere quali "t" e "I" sono più facilmente riconosciute quando viene usata una guida per fornire contesto all'input penna.</span><span class="sxs-lookup"><span data-stu-id="4e883-150">Letters such as "t" and "I" are more easily recognized when a guide is used to give context to the ink.</span></span> <span data-ttu-id="4e883-151">Ad esempio, è possibile creare linee orizzontali in una schermata, che mostrano dove deve essere eseguita la scrittura (questo tipo di guida è costituito solo da righe e senza colonne).</span><span class="sxs-lookup"><span data-stu-id="4e883-151">For example, you can draw horizontal lines on a screen, that show where writing should occur (this type of guide would consist only of rows, and no columns).</span></span> <span data-ttu-id="4e883-152">Scrivendo sulle righe, invece di uno spazio arbitrario, l'accuratezza del riconoscimento migliora.</span><span class="sxs-lookup"><span data-stu-id="4e883-152">By writing on the lines, instead of some arbitrary space, recognition accuracy improves.</span></span>

<span data-ttu-id="4e883-153">La guida specifica i limiti dell'input penna nelle coordinate dello spazio di input penna.</span><span class="sxs-lookup"><span data-stu-id="4e883-153">The guide specifies the boundaries of the ink in ink space coordinates.</span></span>

<span data-ttu-id="4e883-154">La proprietà [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) può definire una casella di dimensioni uguali o inferiori alla casella definita dalla proprietà [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) .</span><span class="sxs-lookup"><span data-stu-id="4e883-154">The [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) property can define a box which is the same size as or smaller than the box defined by the [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) property.</span></span>

<span data-ttu-id="4e883-155">Nella figura seguente vengono illustrati gli elementi di una guida di riconoscimento con due righe e nessuna colonna.</span><span class="sxs-lookup"><span data-stu-id="4e883-155">The following figure shows the elements of a recognizer guide with two rows and no columns.</span></span>

![illustrazione che Mostra gli elementi della guida del riconoscitore](images/927cc2f3-549f-4279-aab9-bd5ade070eaf.jpg)

<span data-ttu-id="4e883-157">Oltre a disegnare linee sullo schermo che mostrano gli utenti in cui scrivere, è possibile disegnare le celle sullo schermo in cui vengono scritti i caratteri o le parole.</span><span class="sxs-lookup"><span data-stu-id="4e883-157">In addition to drawing lines on the screen that show users where to write, you can draw cells on the screen in which characters or words are written.</span></span> <span data-ttu-id="4e883-158">Questo metodo è denominato input boxed ed è utile con alcune lingue asiatiche.</span><span class="sxs-lookup"><span data-stu-id="4e883-158">This is called boxed input and is useful with some Asian languages.</span></span> <span data-ttu-id="4e883-159">Per determinare se il riconoscimento è in grado di eseguire l'input boxed, chiamare la proprietà [**capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) dell'oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) .</span><span class="sxs-lookup"><span data-stu-id="4e883-159">To determine if the recognizer is capable of boxed input, call the [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) property of the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object.</span></span>

<span data-ttu-id="4e883-160">Nella figura seguente viene illustrata una guida di riconoscimento con quattro colonne.</span><span class="sxs-lookup"><span data-stu-id="4e883-160">The following figure shows a recognizer guide with four columns.</span></span>

![illustrazione che mostra la guida al riconoscitore con quattro colonne](images/de44c07e-4b55-42d0-8e8b-997e2da79e52.jpg)

## <a name="requirements"></a><span data-ttu-id="4e883-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e883-162">Requirements</span></span>



| <span data-ttu-id="4e883-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e883-163">Requirement</span></span> | <span data-ttu-id="4e883-164">Valore</span><span class="sxs-lookup"><span data-stu-id="4e883-164">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e883-165">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e883-165">Minimum supported client</span></span><br/> | <span data-ttu-id="4e883-166">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4e883-166">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4e883-167">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e883-167">Minimum supported server</span></span><br/> | <span data-ttu-id="4e883-168">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4e883-168">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4e883-169">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e883-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e883-170"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4e883-170"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4e883-171">Libreria</span><span class="sxs-lookup"><span data-stu-id="4e883-171">Library</span></span><br/>                  | <dl> <span data-ttu-id="4e883-172"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e883-172"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4e883-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e883-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e883-174">**Interfaccia IInkRecognizer**</span><span class="sxs-lookup"><span data-stu-id="4e883-174">**IInkRecognizer Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[<span data-ttu-id="4e883-175">**Classe InkRecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="4e883-175">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> </dl>

 

