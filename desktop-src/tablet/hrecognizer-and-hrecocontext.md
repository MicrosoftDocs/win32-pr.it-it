---
description: Si fa riferimento a un riconoscitore Ink con un handle HRECOGNIZER e un contesto di riconoscimento come handle HRECOCONTEXT. Una libreria di collegamento dinamico (DLL) di riconoscimento può implementare i riconoscitori per più di un linguaggio.
ms.assetid: 23002d02-cf8f-489b-a50f-4a18ac091825
title: HRECOGNIZER e HRECOCONTEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12af1bb5569a22a612f0a3ed667a55aac81da2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307481"
---
# <a name="hrecognizer-and-hrecocontext"></a><span data-ttu-id="cb6cb-103">HRECOGNIZER e HRECOCONTEXT</span><span class="sxs-lookup"><span data-stu-id="cb6cb-103">HRECOGNIZER and HRECOCONTEXT</span></span>

<span data-ttu-id="cb6cb-104">Si fa riferimento a un riconoscitore Ink con un handle [HRECOGNIZER](hrecognizer-handle.md) e un contesto di riconoscimento come handle [HRECOCONTEXT](hrecocontext-handle.md) .</span><span class="sxs-lookup"><span data-stu-id="cb6cb-104">You reference an ink recognizer with an [HRECOGNIZER](hrecognizer-handle.md) handle and a recognizer context as an [HRECOCONTEXT](hrecocontext-handle.md) handle.</span></span>

<span data-ttu-id="cb6cb-105">Una libreria di collegamento dinamico (DLL) di riconoscimento può implementare i riconoscitori per più di un linguaggio.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-105">A recognizer dynamic-link library (DLL) can implement recognizers for more than one language.</span></span> <span data-ttu-id="cb6cb-106">In tal caso, ogni lingua viene selezionata da un CLSID passato durante la creazione dell'oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-106">If so, each language is selected by a CLSID that is passed in when creating the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object in the application.</span></span> <span data-ttu-id="cb6cb-107">Inoltre, una DLL del riconoscitore può creare più handle di riconoscimento quando viene caricato, uno o più per ogni lingua riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-107">In addition, a recognizer DLL can create multiple recognizer handles when it is loaded, one or more for each language recognized.</span></span>

<span data-ttu-id="cb6cb-108">Viene creato un contesto di riconoscimento per rappresentare l'evento di riconoscimento di uno specifico input penna.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-108">A recognizer context is created to represent the event of recognizing a specific piece of ink.</span></span> <span data-ttu-id="cb6cb-109">Quando viene creato il contesto, l'handle degli oggetti riconoscimento associato viene passato alla funzione [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) .</span><span class="sxs-lookup"><span data-stu-id="cb6cb-109">When the context is created, the associated recognizer objects handle is passed to the [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) function.</span></span> <span data-ttu-id="cb6cb-110">In questo caso il linguaggio viene associato al contesto del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-110">This associates the language with the recognizer context.</span></span>

<span data-ttu-id="cb6cb-111">Un contesto di riconoscimento può rappresentare il riconoscimento di tutto l'input penna nel corpo di un messaggio di posta elettronica, l'input penna di un singolo campo all'interno di un'applicazione o una singola riga di testo scritta nel pannello di input di Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-111">A recognizer context may represent the recognition of all the ink in the body of an email, the ink of a single field within an application, or a single line of text written in the Tablet PC Input Panel.</span></span> <span data-ttu-id="cb6cb-112">Il volume di input penna in un singolo contesto di riconoscimento può variare da un singolo tratto a una pagina intera o più.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-112">The volume of ink in a single recognizer context may vary from a single stroke to a whole page or more.</span></span>

<span data-ttu-id="cb6cb-113">Il contesto del riconoscimento è definito dalle impostazioni di:</span><span class="sxs-lookup"><span data-stu-id="cb6cb-113">The recognizer context is defined by the settings of:</span></span>

-   <span data-ttu-id="cb6cb-114">Guida al riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-114">The recognition guide.</span></span>
-   <span data-ttu-id="cb6cb-115">Qualsiasi factoids.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-115">Any factoids.</span></span>
-   <span data-ttu-id="cb6cb-116">Qualsiasi flag.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-116">Any flags.</span></span>
-   <span data-ttu-id="cb6cb-117">Contesto del testo.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-117">The text context.</span></span>
-   <span data-ttu-id="cb6cb-118">Qualsiasi elenco di parole.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-118">Any word list.</span></span>
-   <span data-ttu-id="cb6cb-119">Modalità di completamento automatico dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-119">The character Autocomplete mode.</span></span>

<span data-ttu-id="cb6cb-120">L'handle per il contesto di riconoscimento viene passato a tutte le funzioni che utilizzano queste impostazioni.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-120">The handle for the recognizer context is passed to all functions that use these settings.</span></span> <span data-ttu-id="cb6cb-121">Se si modifica un'impostazione, il contesto di riconoscimento viene modificato.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-121">Changing a setting changes the recognizer context.</span></span>

<span data-ttu-id="cb6cb-122">L'applicazione può usare diversi contesti per riconoscere l'input penna da diverse parti dello schermo.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-122">The application may use several contexts to recognize ink from different parts of the screen.</span></span> <span data-ttu-id="cb6cb-123">Un singolo contesto può riconoscere più righe di testo.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-123">An individual context can recognize multiple lines of text.</span></span> <span data-ttu-id="cb6cb-124">Tuttavia, un singolo contesto non può elaborare due paragrafi scritti side-by-Side, ad esempio più colonne in un articolo di giornale.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-124">However, an individual context cannot process two paragraphs written side by side, such as multiple columns in a newspaper article.</span></span>

<span data-ttu-id="cb6cb-125">Per riconoscere il nuovo input penna, creare un nuovo contesto.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-125">To recognize new ink, create a new context.</span></span> <span data-ttu-id="cb6cb-126">In alternativa, usare la funzione [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) per creare una copia di un contesto che non ha l'input penna e i risultati oppure la funzione [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) per cancellare un contesto dell'input penna e dei risultati.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-126">As an alternative, use the [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) function to make a copy of a context that does not have the ink and results, or the [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) function to clear a context of its ink and results.</span></span> <span data-ttu-id="cb6cb-127">Con questi approcci, un'applicazione Ink può riutilizzare un contesto.</span><span class="sxs-lookup"><span data-stu-id="cb6cb-127">With these approaches, an ink application can reuse a context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb6cb-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cb6cb-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb6cb-129">**Funzione seguide**</span><span class="sxs-lookup"><span data-stu-id="cb6cb-129">**SetGuide Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setguide)
</dt> <dt>

[<span data-ttu-id="cb6cb-130">**Getguide (funzione)**</span><span class="sxs-lookup"><span data-stu-id="cb6cb-130">**GetGuide Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getguide)
</dt> <dt>

[<span data-ttu-id="cb6cb-131">**SetFactoid (funzione)**</span><span class="sxs-lookup"><span data-stu-id="cb6cb-131">**SetFactoid Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setfactoid)
</dt> <dt>

[<span data-ttu-id="cb6cb-132">**Funzione seflags**</span><span class="sxs-lookup"><span data-stu-id="cb6cb-132">**SetFlags Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setflags)
</dt> <dt>

[<span data-ttu-id="cb6cb-133">**SetEnabledUnicodeRanges (funzione)**</span><span class="sxs-lookup"><span data-stu-id="cb6cb-133">**SetEnabledUnicodeRanges Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)
</dt> <dt>

[<span data-ttu-id="cb6cb-134">**GetEnabledUnicodeRanges (funzione)**</span><span class="sxs-lookup"><span data-stu-id="cb6cb-134">**GetEnabledUnicodeRanges Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)
</dt> <dt>

[<span data-ttu-id="cb6cb-135">**SetCACMode (funzione)**</span><span class="sxs-lookup"><span data-stu-id="cb6cb-135">**SetCACMode Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setcacmode)
</dt> <dt>

[<span data-ttu-id="cb6cb-136">**SetTextContext (funzione)**</span><span class="sxs-lookup"><span data-stu-id="cb6cb-136">**SetTextContext Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-settextcontext)
</dt> <dt>

[<span data-ttu-id="cb6cb-137">**Funzione WordList**</span><span class="sxs-lookup"><span data-stu-id="cb6cb-137">**SetWordList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 



