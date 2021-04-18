---
description: Tutto il riconoscimento per i controlli abilitati all'input penna viene eseguito tramite un oggetto RecognizerContext. Le API della tecnologia Tablet PC consentono di impostare la proprietà del controllo del controllo su un oggetto RecognizerContext.
ms.assetid: 453993a7-f055-4d84-870c-256d1ec17731
title: Impostazione del contesto per i controlli Ink-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6776978834f030353a84c04f03e5ecf05ba060cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348626"
---
# <a name="setting-context-for-ink-enabled-controls"></a><span data-ttu-id="c2d70-104">Impostazione del contesto per i controlli Ink-Enabled</span><span class="sxs-lookup"><span data-stu-id="c2d70-104">Setting Context for Ink-Enabled Controls</span></span>

<span data-ttu-id="c2d70-105">Tutto il riconoscimento per i controlli abilitati all'input penna viene eseguito tramite un oggetto [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="c2d70-105">All recognition for ink-enabled controls occurs through a [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span> <span data-ttu-id="c2d70-106">Le API della tecnologia Tablet PC consentono di impostare la [**proprietà del controllo del controllo**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) su un oggetto **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="c2d70-106">The Tablet PC Technology APIs enable you to set the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property on a **RecognizerContext** object.</span></span>

<span data-ttu-id="c2d70-107">Se si sta creando un'applicazione abilitata per l'input penna, usare le proprietà del [**controllo dell'oggetto RecognizerContext e del**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) [**nome**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) per impostare i contesti.</span><span class="sxs-lookup"><span data-stu-id="c2d70-107">If you are creating an ink-enabled application, use the [**RecognizerContext**](inkrecognizercontext-class.md) object's [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) and [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) properties to set contexts.</span></span>

<span data-ttu-id="c2d70-108">È possibile passare i valori stringa dei nomi negli ambiti di input definiti nell'enumerazione [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) [**alla proprietà del controllo oggetto,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) delimitata da un'apertura (!</span><span class="sxs-lookup"><span data-stu-id="c2d70-108">You may pass in the string values of the names in the input scopes defined in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration to the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property, delimited with an opening (!</span></span> <span data-ttu-id="c2d70-109">e una chiusura.</span><span class="sxs-lookup"><span data-stu-id="c2d70-109">and a closing ).</span></span> <span data-ttu-id="c2d70-110">Per impostare, ad esempio, il contesto di un oggetto [**RecognizerContext**](inkrecognizercontext-class.md) su bias verso i caratteri utilizzati in un URL, utilizzare la sintassi illustrata negli \# esempi C seguenti:</span><span class="sxs-lookup"><span data-stu-id="c2d70-110">For example, to set the context for a [**RecognizerContext**](inkrecognizercontext-class.md) object to bias toward characters used in a URL, use the syntax shown in the following C\# examples:</span></span>


```C++
theRecoContext.Factoid = "(!IS_URL)";
```



> [!Note]  
> <span data-ttu-id="c2d70-111">Gli ambiti di input come definito nell'enumerazione [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) sostituiscono il factoids disponibile nelle versioni precedenti di Windows XP Tablet PC Edition SDK, anche se questi factoids continueranno a funzionare per garantire la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="c2d70-111">The input scopes as defined in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration supersede the factoids that were available in previous versions of the Windows XP Tablet PC Edition SDK, although these factoids will continue to work in order to provide backward compatibility.</span></span>

 

<span data-ttu-id="c2d70-112">Nell'esempio C seguente \# viene impostata [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) la proprietà del controllore per i codici postali:</span><span class="sxs-lookup"><span data-stu-id="c2d70-112">The following C\# example sets the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property for postal codes:</span></span>


```C++
theRecognizerContext.Factoid = "(!IS_ADDRESS_POSTALCODE)";
```



<span data-ttu-id="c2d70-113">È possibile combinare gli ambiti di input usando la sintassi delle espressioni regolari della grafia.</span><span class="sxs-lookup"><span data-stu-id="c2d70-113">You can combine input scopes by using the handwriting regular expression syntax.</span></span> <span data-ttu-id="c2d70-114">Per altri dettagli sull'uso della sintassi delle espressioni regolari, vedere [ambiti di input personalizzati con espressioni regolari](custom-input-scopes-with-regular-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="c2d70-114">For more details about using regular expression syntax, see [Custom Input Scopes with Regular Expressions](custom-input-scopes-with-regular-expressions.md).</span></span>

<span data-ttu-id="c2d70-115">È possibile impostare i flag di riconoscimento nell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) per influire sul comportamento del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="c2d70-115">You can set recognition flags on the [**RecognizerContext**](inkrecognizercontext-class.md) object to affect the behavior of the recognizer.</span></span> <span data-ttu-id="c2d70-116">Uno di questi flag è il flag di **coercizione** nell'enumerazione [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) dell'oggetto **RecognizerContext**.</span><span class="sxs-lookup"><span data-stu-id="c2d70-116">One such flag is the **Coerce** flag in the [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) enumeration of the **RecognizerContext**.</span></span> <span data-ttu-id="c2d70-117">Il flag di **coercizione** impone al riconoscimento di restituire un risultato che corrisponda alla definizione del controllo oggetto impostato.</span><span class="sxs-lookup"><span data-stu-id="c2d70-117">The **Coerce** flag forces the recognizer to return a result that matches the definition of the factoid that is set.</span></span> <span data-ttu-id="c2d70-118">Se, ad esempio, si dispone di un modulo che richiede all'utente di immettere una quantità numerica, può essere utile impostare il controllo del controllo dei **\_ numeri** e impostare anche la proprietà [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) su **coercizione**.</span><span class="sxs-lookup"><span data-stu-id="c2d70-118">For example, if you have a form that requires the user to enter a numerical quantity, it may be useful to set the **IS\_NUMBER** factoid and also set the [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) property to **Coerce**.</span></span> <span data-ttu-id="c2d70-119">In tale istanza, il flag di **coercizione** garantisce che il riconoscimento restituisca solo numeri.</span><span class="sxs-lookup"><span data-stu-id="c2d70-119">In that instance, the **Coerce** flag guarantees that the recognizer returns only numbers.</span></span>

<span data-ttu-id="c2d70-120">L'esempio C seguente \# imposta la proprietà [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) su **coercizione**:</span><span class="sxs-lookup"><span data-stu-id="c2d70-120">The following C\# example sets the [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) property to **Coerce**:</span></span>


```C++
theRecognizerContext.RecognitionFlags = RecognitionModes.Coerce;
```



<span data-ttu-id="c2d70-121">Tuttavia, prestare attenzione quando si decide di impostare il flag di **coercizione** .</span><span class="sxs-lookup"><span data-stu-id="c2d70-121">However, use caution when deciding to set the **Coerce** flag.</span></span> <span data-ttu-id="c2d70-122">Il flag impone al riconoscimento di trovare la corrispondenza solo con la definizione del controllo del controllo.</span><span class="sxs-lookup"><span data-stu-id="c2d70-122">The flag forces the recognizer to match only the definition of the factoid.</span></span> <span data-ttu-id="c2d70-123">Se, ad esempio, si imposta l' \_ \_ ambito di input FULLTELEPHONENUMBER telefonico e il flag di **coercizione** , il riconoscimento restituisce risultati che corrispondono esattamente alla definizione dell' \_ ambito di \_ input di FULLTELEPHONENUMBER telefonico.</span><span class="sxs-lookup"><span data-stu-id="c2d70-123">For example, if you set the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope and the **Coerce** flag, the recognizer returns results that exactly match the definition of the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope only.</span></span> <span data-ttu-id="c2d70-124">Se un utente scrive "911" con l' \_ \_ ambito di input is Phone FULLTELEPHONENUMBER e il flag di **coercizione** impostato, il riconoscimento può restituire una stringa vuota o una stringa casuale nel formato (xxx) xxx-xxxx (dove X è una cifra).</span><span class="sxs-lookup"><span data-stu-id="c2d70-124">If a user writes "911" with the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope and the **Coerce** flag set, the recognizer may return either an empty string or a random string in the format of (XXX) XXX-XXXX (where X is a digit).</span></span> <span data-ttu-id="c2d70-125">Il formato XXX non corrisponde alla definizione del controllo del \_ \_ codice FULLTELEPHONENUMBER telefonico, anche se è un numero di telefono valido.</span><span class="sxs-lookup"><span data-stu-id="c2d70-125">The format of XXX does not match the definition of the IS\_TELEPHONE\_FULLTELEPHONENUMBER factoid, even though it is a valid phone number.</span></span>

<span data-ttu-id="c2d70-126">Per gli elenchi dei formati supportati per ogni ambito di input, vedere la Guida di riferimento a [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) .</span><span class="sxs-lookup"><span data-stu-id="c2d70-126">For lists of the supported formats for each input scope, see the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) reference.</span></span>

<span data-ttu-id="c2d70-127">Per restituire un campo all'impostazione predefinita per il riconoscimento, impostare il controllo oggetto su è \_ predefinito, come nell'esempio C seguente \# :</span><span class="sxs-lookup"><span data-stu-id="c2d70-127">To return a field to the default setting for the recognizer, set the factoid to IS\_DEFAULT , as in the following C\# example:</span></span>


```C++
theRecgonizerContext.Factoid = "(!IS_DEFAULT)";
```



<span data-ttu-id="c2d70-128">Per le applicazioni che usano il controllo [InkEdit](inkedit-control-reference.md) , impostare il tipo di controllo dell'oggetto per il controllo specificando:</span><span class="sxs-lookup"><span data-stu-id="c2d70-128">For applications that use the [InkEdit](inkedit-control-reference.md) control, set the factoid type for the control by specifying:</span></span>


```C++
InkEdit1.Factoid = "(!IS_INPUTSCOPE)"
```



<span data-ttu-id="c2d70-129">Dove `IS_INPUTSCOPE` è il nome dell'ambito di input che si desidera applicare.</span><span class="sxs-lookup"><span data-stu-id="c2d70-129">Where `IS_INPUTSCOPE` is the name of the input scope you want to apply.</span></span>

<span data-ttu-id="c2d70-130">Il controllo [InkEdit](inkedit-control-reference.md) non espone un oggetto [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="c2d70-130">The [InkEdit](inkedit-control-reference.md) control does not expose a [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span> <span data-ttu-id="c2d70-131">È comunque possibile [**assegnare il contesto usando la proprietà del**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) controllo InkEdit del controllo InkEdit, ma non è possibile impostare il flag **WORDMODE** .</span><span class="sxs-lookup"><span data-stu-id="c2d70-131">You can still assign context by using the [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) property of the InkEdit control, but you cannot set the **WORDMODE** flag.</span></span>

 

 
