---
description: Non tutte le applicazioni richiedono l'uso del riconoscimento, ma poiché la maggior parte delle applicazioni è stata progettata con testo come tipo di dati primario, la possibilità di convertire input penna in testo è molto utile.
ms.assetid: 70d25839-6ddd-40db-8891-92da074d17b0
title: Riconoscimento input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca4ec6f897c797d86df96c5d9c2cfd5d80f16c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553595"
---
# <a name="ink-recognition"></a><span data-ttu-id="a16c8-103">Riconoscimento input penna</span><span class="sxs-lookup"><span data-stu-id="a16c8-103">Ink Recognition</span></span>

<span data-ttu-id="a16c8-104">Non tutte le applicazioni richiedono l'uso del riconoscimento, ma poiché la maggior parte delle applicazioni è stata progettata con testo come tipo di dati primario, la possibilità di convertire input penna in testo è molto utile.</span><span class="sxs-lookup"><span data-stu-id="a16c8-104">Not all applications require the use of recognition, but because most applications were designed with text as their primary data type, the ability to convert ink into text is very valuable.</span></span> <span data-ttu-id="a16c8-105">È possibile utilizzare le funzionalità di riconoscimento dell'API della piattaforma Tablet PC per eseguire una query per ottenere informazioni sui motori di riconoscimento disponibili, ad esempio le lingue riconosciute.</span><span class="sxs-lookup"><span data-stu-id="a16c8-105">You can use the recognition features of the Tablet PC platform API to query for information about the recognition engines that are available, such as what languages they recognize.</span></span> <span data-ttu-id="a16c8-106">È quindi possibile inviare una raccolta [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) da un oggetto [**Ink**](inkdisp-class.md) a un motore di riconoscimento e fare in modo che restituisca un oggetto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) .</span><span class="sxs-lookup"><span data-stu-id="a16c8-106">You can then send a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection from an [**Ink**](inkdisp-class.md) object to a recognition engine and have it return a [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object.</span></span>

## <a name="recognizercontext-object"></a><span data-ttu-id="a16c8-107">RecognizerContext (oggetto)</span><span class="sxs-lookup"><span data-stu-id="a16c8-107">RecognizerContext Object</span></span>

<span data-ttu-id="a16c8-108">Un oggetto [**RecognizerContext**](inkrecognizercontext-class.md) è la creazione di un'istanza di un determinato riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="a16c8-108">A [**RecognizerContext**](inkrecognizercontext-class.md) object is the instantiation of a given recognizer.</span></span> <span data-ttu-id="a16c8-109">L'oggetto **RecognizerContext** consente di riconoscere un determinato insieme di tratti in modo sincrono o asincrono.</span><span class="sxs-lookup"><span data-stu-id="a16c8-109">The **RecognizerContext** object enables you to recognize a given collection of strokes synchronously or asynchronously.</span></span> <span data-ttu-id="a16c8-110">Quando si riconosce in modo asincrono, l'oggetto **RecognizerContext** restituisce l'oggetto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) in un callback di evento all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a16c8-110">When recognizing asynchronously, the **RecognizerContext** object returns the [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object in an event callback to the application.</span></span>

## <a name="recognizers-and-recognizer-objects"></a><span data-ttu-id="a16c8-111">Riconoscitori e oggetti di riconoscimento</span><span class="sxs-lookup"><span data-stu-id="a16c8-111">Recognizers and Recognizer Objects</span></span>

<span data-ttu-id="a16c8-112">Un singolo Tablet PC può avere uno o più sistemi di riconoscimento disponibili.</span><span class="sxs-lookup"><span data-stu-id="a16c8-112">A single Tablet PC may have one or more recognizers available.</span></span> <span data-ttu-id="a16c8-113">È possibile eseguire una query sulla raccolta del riconoscitore per determinare il riconoscimento da usare.</span><span class="sxs-lookup"><span data-stu-id="a16c8-113">You can query the recognizer's collection to determine which recognizer to use.</span></span> <span data-ttu-id="a16c8-114">Un riconoscitore fornisce informazioni specifiche sulle funzionalità, ad esempio il linguaggio che può riconoscere e il produttore.</span><span class="sxs-lookup"><span data-stu-id="a16c8-114">A recognizer provides specific information about its capabilities such as the language it can recognize and the manufacturer.</span></span>

<span data-ttu-id="a16c8-115">Per determinare se è installato almeno un riconoscimento, creare un'istanza di un oggetto [**InkRecognizerContext**](inkrecognizercontext-class.md) come illustrato negli esempi di codice C++ e C seguenti \# .</span><span class="sxs-lookup"><span data-stu-id="a16c8-115">To determine whether at least one recognizer is installed, instantiate an [**InkRecognizerContext**](inkrecognizercontext-class.md) object as shown in the following C++ and C\# code examples.</span></span> <span data-ttu-id="a16c8-116">Se non è presente un riconoscitore, la chiamata a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="a16c8-116">If a recognizer is not present, this call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fails.</span></span>


```C++
CComPtr<IInkRecognizerContext> g_pIInkRecoContext;
hr = CoCreateInstance(CLSID_InkRecognizerContext, 
      NULL, CLSCTX_INPROC_SERVER,
      IID_IInkRecognizerContext, 
(void **) &g_pIInkRecoContext);
if (FAILED(hr)) 
{
      ::MessageBox(NULL, TEXT("No recognizers installed.\nExiting."), 
      gc_szAppName, MB_ICONERROR);
      return -1;
}
```




```CSharp
try
{
  Recognizers recos = new Recognizers();//Check for recognizer.
  Recognizer defReco = recos.GetDefaultRecognizer();
  recoContext = defReco.CreateRecognizerContext();
}
catch
{
  MessageBox.Show("No recognizers installed.");
}
```



## <a name="recognitionresult-and-recognitionalternate-objects"></a><span data-ttu-id="a16c8-117">Oggetti RecognitionResult e RecognitionAlternate</span><span class="sxs-lookup"><span data-stu-id="a16c8-117">RecognitionResult and RecognitionAlternate Objects</span></span>

<span data-ttu-id="a16c8-118">I risultati del riconoscimento vengono restituiti in un oggetto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) .</span><span class="sxs-lookup"><span data-stu-id="a16c8-118">The results of the recognition are returned in a [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object.</span></span> <span data-ttu-id="a16c8-119">I risultati contengono una stringa di risultato migliore nella proprietà di [tostringa](/previous-versions/ms829602(v=msdn.10)) , oltre a una raccolta di risultati alternativi in una raccolta [**RecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) .</span><span class="sxs-lookup"><span data-stu-id="a16c8-119">The results contain a best result string in the [TopString](/previous-versions/ms829602(v=msdn.10)) property, as well as a collection of alternative results in a [**RecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) collection.</span></span> <span data-ttu-id="a16c8-120">L'oggetto **RecognitionResult** può essere reso permanente con la raccolta di [**tratti**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) originale dalla quale è stato generato.</span><span class="sxs-lookup"><span data-stu-id="a16c8-120">The **RecognitionResult** object can be persisted with the original [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection from which it was generated.</span></span>

## <a name="recognizerguide-structure"></a><span data-ttu-id="a16c8-121">Struttura RecognizerGuide</span><span class="sxs-lookup"><span data-stu-id="a16c8-121">RecognizerGuide Structure</span></span>

<span data-ttu-id="a16c8-122">La guida per il riconoscimento può essere costituita da righe e colonne e fornisce al riconoscimento un contesto migliore in cui eseguire il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="a16c8-122">The recognizer guide can consist of rows and columns, and gives the recognizer a better context in which to perform recognition.</span></span> <span data-ttu-id="a16c8-123">Ad esempio, è possibile creare linee orizzontali sullo schermo di un utente, quasi come una parte di carta regolata, che mostra dove deve essere eseguita la grafia (questo tipo di guida è costituito solo da righe e senza colonne).</span><span class="sxs-lookup"><span data-stu-id="a16c8-123">For example, you can draw horizontal lines on a user's screen, almost like a ruled piece of paper, that show where handwriting should occur (this type of guide would consist only of rows, and no columns).</span></span> <span data-ttu-id="a16c8-124">Se un utente scrive sulle righe, anziché uno spazio arbitrario, l'accuratezza del riconoscimento migliora.</span><span class="sxs-lookup"><span data-stu-id="a16c8-124">If a user writes on the lines, instead of some arbitrary space, recognition accuracy improves.</span></span>

<span data-ttu-id="a16c8-125">Nella figura seguente viene illustrata una struttura [**RecognizerGuide**](inkrecognizerguide-class.md) con due righe per l'input.</span><span class="sxs-lookup"><span data-stu-id="a16c8-125">The following illustration shows a [**RecognizerGuide**](inkrecognizerguide-class.md) structure with two lines for input.</span></span>

![illustrazione che mostra la guida per il riconoscimento a due righe](images/9791100b-8279-4dd0-823f-0a38a0308a74.jpg)

<span data-ttu-id="a16c8-127">Nella figura seguente viene illustrata una struttura [**RecognizerGuide**](inkrecognizerguide-class.md) con quattro colonne e tre righe.</span><span class="sxs-lookup"><span data-stu-id="a16c8-127">The following illustration shows a [**RecognizerGuide**](inkrecognizerguide-class.md) structure with four columns and three rows.</span></span>

![illustrazione che mostra la guida per i riconoscitori tre per quattro](images/d1bbf2d3-9653-49d7-bf48-c1b26645074c.jpg)

<span data-ttu-id="a16c8-129">Per ulteriori informazioni sull'utilizzo della struttura [**RecognizerGuide**](inkrecognizerguide-class.md) , vedere l'argomento di riferimento **RecognizerGuide** .</span><span class="sxs-lookup"><span data-stu-id="a16c8-129">For more information about using the [**RecognizerGuide**](inkrecognizerguide-class.md) structure, see the **RecognizerGuide** reference topic.</span></span>

 

 
