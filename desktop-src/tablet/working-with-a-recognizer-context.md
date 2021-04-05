---
description: L'oggetto divisore utilizza un oggetto RecognizerContext per migliorare l'analisi dei segmenti di riconoscimento e generare testo di riconoscimento per gli elementi di grafia.
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: Utilizzo di un contesto di riconoscimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdea8c59bc894a6962e8bbe7e58f316327a548e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049565"
---
# <a name="working-with-a-recognizer-context"></a><span data-ttu-id="77e47-103">Utilizzo di un contesto di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="77e47-103">Working with a Recognizer Context</span></span>

<span data-ttu-id="77e47-104">L'oggetto [**divisore**](inkdivider-class.md) utilizza un oggetto [**RecognizerContext**](inkrecognizercontext-class.md) per migliorare l'analisi dei segmenti di riconoscimento e generare testo di riconoscimento per gli elementi di grafia.</span><span class="sxs-lookup"><span data-stu-id="77e47-104">The [**Divider**](inkdivider-class.md) object uses a [**RecognizerContext**](inkrecognizercontext-class.md) to improve its analysis of recognition segments and to generate recognition text for handwriting elements.</span></span>

<span data-ttu-id="77e47-105">È possibile impostare il contesto di riconoscimento usando la proprietà [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) dell'oggetto [**divisore**](inkdivider-class.md) o specificando il contesto di riconoscimento nella chiamata al costruttore del [divisore](/previous-versions/ms839465(v=msdn.10)) (nel codice gestito).</span><span class="sxs-lookup"><span data-stu-id="77e47-105">You can set the recognizer context by using the [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property of the [**Divider**](inkdivider-class.md) object or by supplying the recognizer context in the call to the [Divider](/previous-versions/ms839465(v=msdn.10)) constructor (in managed code).</span></span> <span data-ttu-id="77e47-106">Se un contesto di riconoscimento per un riconoscimento non grafia o per un riconoscimento che non supporta la funzionalità di input libero viene assegnato alla proprietà **RecognizerContext** , viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="77e47-106">If a recognizer context for a non-handwriting recognizer or for a recognizer that does not support the free input capability is assigned to the **RecognizerContext** property, then an exception is thrown.</span></span>

<span data-ttu-id="77e47-107">Se i riconoscitori non sono installati o un contesto di riconoscimento non è assegnato all'oggetto [**divisore**](inkdivider-class.md) , l'oggetto **divisore** non utilizza un contesto di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="77e47-107">If recognizers are not installed or a recognizer context is not assigned to the [**Divider**](inkdivider-class.md) object, the **Divider** object does not use a recognizer context.</span></span> <span data-ttu-id="77e47-108">In questo caso, la funzionalità di analisi del layout esegue la divisione del segmento e nessun testo è associato all'oggetto [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="77e47-108">In this case, the layout analysis feature performs the segment division, and no text is associated with the [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

> [!Note]  
> <span data-ttu-id="77e47-109">Non è possibile modificare la proprietà [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) dopo che sono stati assegnati Strokes all'oggetto [**divisore**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="77e47-109">The [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property cannot be changed after strokes have been assigned to the [**Divider**](inkdivider-class.md) object.</span></span> <span data-ttu-id="77e47-110">L'oggetto **divisore** utilizza i valori predefiniti delle proprietà dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="77e47-110">The **Divider** object uses the default property values of the [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

 

<span data-ttu-id="77e47-111">L'oggetto [**divisore**](inkdivider-class.md) applica il contesto del riconoscimento agli elementi scritti a mano durante l'analisi del layout.</span><span class="sxs-lookup"><span data-stu-id="77e47-111">The [**Divider**](inkdivider-class.md) object applies the recognizer context to handwritten elements during layout analysis.</span></span> <span data-ttu-id="77e47-112">Tutti i tratti assegnati direttamente al contesto del riconoscimento vengono ignorati dall'oggetto **divisore** .</span><span class="sxs-lookup"><span data-stu-id="77e47-112">Any strokes you assign directly to the recognizer context are ignored by the **Divider** object.</span></span> <span data-ttu-id="77e47-113">Per ulteriori informazioni sul riconoscimento del testo, vedere [informazioni sul riconoscimento della grafia](about-handwriting-recognition.md).</span><span class="sxs-lookup"><span data-stu-id="77e47-113">For more information about text recognition, see [About Handwriting Recognition](about-handwriting-recognition.md).</span></span>

 

 
