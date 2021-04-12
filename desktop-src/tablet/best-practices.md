---
description: Panoramica delle procedure consigliate per l'uso dell'oggetto pannello input penna.
ms.assetid: 5b127743-0c88-4c4c-bcb6-5a91690cd2a1
title: Procedure consigliate (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd492dfeda94ce9dce056b286ef1989f3389658c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234084"
---
# <a name="best-practices-tablet-pc"></a><span data-ttu-id="d7ef1-103">Procedure consigliate (Tablet PC)</span><span class="sxs-lookup"><span data-stu-id="d7ef1-103">Best Practices (Tablet PC)</span></span>

<span data-ttu-id="d7ef1-104">Esistono alcune linee guida da tenere presenti quando si usa l'oggetto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="d7ef1-104">There are a few guidelines to keep in mind when using the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

-   [<span data-ttu-id="d7ef1-105">Preferisci controllo InkEdit</span><span class="sxs-lookup"><span data-stu-id="d7ef1-105">Prefer InkEdit Control</span></span>](#prefer-inkedit-control)
-   [<span data-ttu-id="d7ef1-106">Disabilitare la modalità input penna nei controlli InkEdit</span><span class="sxs-lookup"><span data-stu-id="d7ef1-106">Disable Ink Mode on InkEdit Controls</span></span>](#disable-ink-mode-on-inkedit-controls)
-   [<span data-ttu-id="d7ef1-107">Uso di controlli senza finestra</span><span class="sxs-lookup"><span data-stu-id="d7ef1-107">Using Windowless Controls</span></span>](#using-windowless-controls)
-   [<span data-ttu-id="d7ef1-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7ef1-108">Related topics</span></span>](#related-topics)

## <a name="prefer-inkedit-control"></a><span data-ttu-id="d7ef1-109">Preferisci controllo InkEdit</span><span class="sxs-lookup"><span data-stu-id="d7ef1-109">Prefer InkEdit Control</span></span>

<span data-ttu-id="d7ef1-110">[InkEdit](inkedit-control-reference.md) è il controllo preferito a cui alleghi l'oggetto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="d7ef1-110">[InkEdit](inkedit-control-reference.md) is the preferred control to which to attach the [**PenInputPanel**](peninputpanel-class.md) object.</span></span> <span data-ttu-id="d7ef1-111">Il controllo InkEdit fornisce il supporto per il [Framework dei servizi di testo (TSF)](text-services-framework.md).</span><span class="sxs-lookup"><span data-stu-id="d7ef1-111">The InkEdit control provides support for the [Text Services Framework (TSF)](text-services-framework.md).</span></span>

## <a name="disable-ink-mode-on-inkedit-controls"></a><span data-ttu-id="d7ef1-112">Disabilitare la modalità input penna nei controlli InkEdit</span><span class="sxs-lookup"><span data-stu-id="d7ef1-112">Disable Ink Mode on InkEdit Controls</span></span>

<span data-ttu-id="d7ef1-113">Quando viene collegato a un controllo [InkEdit](inkedit-control-reference.md) , impostare la proprietà [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) del controllo InkEdit sul valore [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) .</span><span class="sxs-lookup"><span data-stu-id="d7ef1-113">When attached to an [InkEdit](inkedit-control-reference.md) control, set the [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property of the InkEdit control to the [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) value.</span></span> <span data-ttu-id="d7ef1-114">Se la proprietà **InkMode** non è impostata sul valore **InkMode** , il controllo InkEdit interpreta il primo tap come tratto, lo passa al riconoscimento e inserisce il testo nel controllo InkEdit.</span><span class="sxs-lookup"><span data-stu-id="d7ef1-114">If the **InkMode** property is not set to the **InkMode** value, the InkEdit control interprets the first tap as a stroke, passes it to the recognizer, and inserts the text in the InkEdit control.</span></span> <span data-ttu-id="d7ef1-115">Poiché si dispone già di un oggetto [**PenInputPanel**](peninputpanel-class.md) collegato per accettare input penna, non è necessario che il controllo InkEdit sia abilitato anche per l'input penna.</span><span class="sxs-lookup"><span data-stu-id="d7ef1-115">Since you already have a [**PenInputPanel**](peninputpanel-class.md) object attached to accept ink input, there is no need to have the InkEdit control also enabled for ink input.</span></span>

## <a name="using-windowless-controls"></a><span data-ttu-id="d7ef1-116">Uso di controlli senza finestra</span><span class="sxs-lookup"><span data-stu-id="d7ef1-116">Using Windowless Controls</span></span>

<span data-ttu-id="d7ef1-117">Quando un oggetto [**PenInputPanel**](peninputpanel-class.md) è associato a una finestra padre che contiene più di un controllo senza finestra, l'oggetto **PenInputPanel** non sa come tenere traccia del punto di inserimento quando lo stato attivo viene spostato tra gli elementi figlio senza finestra.</span><span class="sxs-lookup"><span data-stu-id="d7ef1-117">When a [**PenInputPanel**](peninputpanel-class.md) object is attached to a parent window that contains more than one windowless control, the **PenInputPanel** object does not know how to track the caret as focus moves among windowless children.</span></span> <span data-ttu-id="d7ef1-118">L'input della grafia può essere inviato al figlio errato quando lo stato attivo viene spostato da un controllo senza finestra a un altro mentre l'input è in sospeso.</span><span class="sxs-lookup"><span data-stu-id="d7ef1-118">Handwriting input can be sent to the wrong child when focus moves from one windowless control to another while input is pending.</span></span>

<span data-ttu-id="d7ef1-119">Per usare l'oggetto [**PenInputPanel**](peninputpanel-class.md) in un ambiente privo di finestra, è possibile usare la tecnica seguente:</span><span class="sxs-lookup"><span data-stu-id="d7ef1-119">To use the [**PenInputPanel**](peninputpanel-class.md) object in a windowless environment, the following technique can be used:</span></span>

1.  <span data-ttu-id="d7ef1-120">Crea un'istanza di un controllo [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) e la posiziona sul controllo senza finestra.</span><span class="sxs-lookup"><span data-stu-id="d7ef1-120">Instantiate a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) control and position it over the windowless control.</span></span>
2.  <span data-ttu-id="d7ef1-121">Alleghi l'oggetto [**PenInputPanel**](peninputpanel-class.md) al nuovo controllo casella di testo.</span><span class="sxs-lookup"><span data-stu-id="d7ef1-121">Attach the [**PenInputPanel**](peninputpanel-class.md) object to the new text box control.</span></span>
3.  <span data-ttu-id="d7ef1-122">Consentire al controllo casella di testo di raccogliere il testo riconosciuto dall'oggetto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="d7ef1-122">Let the text box control collect the recognized text from the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>
4.  <span data-ttu-id="d7ef1-123">Quando lo stato attivo si sposta dal controllo casella di testo, chiamare il metodo [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) dell'oggetto [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="d7ef1-123">When focus changes away from the text box control, call the [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) method of the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>
5.  <span data-ttu-id="d7ef1-124">Copiare il testo riconosciuto dal controllo casella di testo nell'elemento figlio privo di finestra.</span><span class="sxs-lookup"><span data-stu-id="d7ef1-124">Copy the recognized text from the text box control to the windowless child.</span></span>
6.  <span data-ttu-id="d7ef1-125">Scollegare l'oggetto [**PenInputPanel**](peninputpanel-class.md) impostando la proprietà [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (solo codice gestito) o la proprietà [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) su null.</span><span class="sxs-lookup"><span data-stu-id="d7ef1-125">Detach the [**PenInputPanel**](peninputpanel-class.md) object by setting its [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (managed code only) property or [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) property to null.</span></span>
7.  <span data-ttu-id="d7ef1-126">Elimina il controllo casella di testo.</span><span class="sxs-lookup"><span data-stu-id="d7ef1-126">Destroy the text box control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d7ef1-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7ef1-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7ef1-128">**Classe PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="d7ef1-128">**PenInputPanel Class**</span></span>](peninputpanel-class.md)
</dt> <dt>

<span data-ttu-id="d7ef1-129">[Microsoft. Ink. PenInputPanel](/previous-versions/ms583923(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="d7ef1-129">[Microsoft.Ink.PenInputPanel](/previous-versions/ms583923(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="d7ef1-130">Text Services Framework</span><span class="sxs-lookup"><span data-stu-id="d7ef1-130">Text Services Framework</span></span>](../tsf/text-services-framework.md)
</dt> </dl>

 

 
