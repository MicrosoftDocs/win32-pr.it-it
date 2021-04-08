---
title: IAgentBalloonEx GetStyle
description: IAgentBalloonEx GetStyle
ms.assetid: 7c6a7260-073b-4535-b8e7-a8cae9aae9ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e21ab22a9aa5a85fdbe1bc541f29df75313cdce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856526"
---
# <a name="iagentballoonexgetstyle"></a><span data-ttu-id="53570-103">IAgentBalloonEx:: GetStyle</span><span class="sxs-lookup"><span data-stu-id="53570-103">IAgentBalloonEx::GetStyle</span></span>

<span data-ttu-id="53570-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53570-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetStyle(
   long * plStyle,  // address of style settings
);
```

<span data-ttu-id="53570-105">Recupera le impostazioni di stile del fumetto Word del carattere.</span><span class="sxs-lookup"><span data-stu-id="53570-105">Retrieves the character's word balloon style settings.</span></span>

-   <span data-ttu-id="53570-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="53570-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="53570-107"><span id="plStyle"></span><span id="plstyle"></span><span id="PLSTYLE"></span>*plStyle*</span><span class="sxs-lookup"><span data-stu-id="53570-107"><span id="plStyle"></span><span id="plstyle"></span><span id="PLSTYLE"></span>*plStyle*</span></span>
</dt> <dd>

<span data-ttu-id="53570-108">Impostazioni di stile per la parola Balloon, che può essere una combinazione dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="53570-108">Style settings for the word balloon, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="53570-109">Valore</span><span class="sxs-lookup"><span data-stu-id="53570-109">Value</span></span>                                                                           | <span data-ttu-id="53570-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53570-110">Description</span></span>                                                 |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="53570-111">**const unsigned short** **Balloon \_ Style \_ BALLOONON = 0x00000001;**</span><span class="sxs-lookup"><span data-stu-id="53570-111">**const unsigned short** **BALLOON\_STYLE\_BALLOONON = 0x00000001;**</span></span><br/> | <span data-ttu-id="53570-112">Il fumetto è supportato per l'output.</span><span class="sxs-lookup"><span data-stu-id="53570-112">The balloon is supported for output.</span></span>                        |
| <span data-ttu-id="53570-113">**const unsigned short** **Balloon \_ Style \_ SIZETOTEXT = 0x0000002;**</span><span class="sxs-lookup"><span data-stu-id="53570-113">**const unsigned short** **BALLOON\_STYLE \_SIZETOTEXT = 0x0000002;**</span></span>           | <span data-ttu-id="53570-114">L'altezza del fumetto è dimensionata in modo da contenere l'output di testo.</span><span class="sxs-lookup"><span data-stu-id="53570-114">The balloon height is sized to accommodate the text output.</span></span> |
| <span data-ttu-id="53570-115">Nascondi automaticamente lo stile di un **breve fumetto const senza segno** **\_ \_ = 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="53570-115">**const unsigned short** **BALLOON\_STYLE \_AUTOHIDE = 0x00000004;**</span></span>            | <span data-ttu-id="53570-116">Il fumetto viene nascosto automaticamente.</span><span class="sxs-lookup"><span data-stu-id="53570-116">The balloon is automatically hidden.</span></span>                        |
| <span data-ttu-id="53570-117">autopace **senza segno const unsigned short** **Balloon \_ \_ = 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="53570-117">**const unsigned short** **BALLOON\_STYLE \_AUTOPACE = 0x00000008;**</span></span>            | <span data-ttu-id="53570-118">L'output di testo viene gestito in base alla frequenza di output.</span><span class="sxs-lookup"><span data-stu-id="53570-118">The text output is paced based on the output rate.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="53570-119">Quando viene impostato il bit di stile **BalloonOn** , la parola Balloon viene visualizzata quando viene usato il metodo [**Speak**](speak-method.md) o [**think**](think-method.md) , a meno che l'utente non esegua l'override della relativa visualizzazione tramite la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="53570-119">When the **BalloonOn** style bit is set, the word balloon appears when the [**Speak**](speak-method.md) or [**Think**](think-method.md) method is used, unless the user overrides its display through the Microsoft Agent property sheet.</span></span> <span data-ttu-id="53570-120">Quando non è impostato, non viene visualizzato alcun fumetto.</span><span class="sxs-lookup"><span data-stu-id="53570-120">When not set, no balloon appears.</span></span>

<span data-ttu-id="53570-121">Quando è impostato il bit di stile **SizeToText** , la parola Balloon ridimensiona automaticamente l'altezza del fumetto alla dimensione corrente del testo specificato nel metodo [**Speak**](speak-method.md) o [**think**](think-method.md) .</span><span class="sxs-lookup"><span data-stu-id="53570-121">When the **SizeToText** style bit is set, the word balloon automatically sizes the height of the balloon to the current size of the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method.</span></span> <span data-ttu-id="53570-122">Quando non è impostato, l'altezza del fumetto è basata sull'impostazione della proprietà Number of Lines del fumetto.</span><span class="sxs-lookup"><span data-stu-id="53570-122">When not set, the balloon's height is based on the balloon's number of lines property setting.</span></span> <span data-ttu-id="53570-123">Questo bit di stile è impostato su 1 e un tentativo di utilizzare [**IAgentBalloonEx:: SetNumLines**](iagentballoonex--setnumlines.md) comporterà un errore.</span><span class="sxs-lookup"><span data-stu-id="53570-123">This style bit is set to 1 and an attempt to use [**IAgentBalloonEx::SetNumLines**](iagentballoonex--setnumlines.md) will result in an error.</span></span>

<span data-ttu-id="53570-124">Quando è impostato il bit di stile **Nascondi** automaticamente, la parola fumetto viene nascosta automaticamente dopo un timeout breve. Quando non è impostato, il fumetto viene visualizzato fino a quando [](think-method.md) non viene visualizzata una nuova chiamata, il carattere è [**nascosto oppure l'**](speak-method.md) utente fa clic o trascina il carattere.</span><span class="sxs-lookup"><span data-stu-id="53570-124">When the **AutoHide** style bit is set, the word balloon automatically hides after a short time-out. When not set, the balloon displays until a new [**Speak**](speak-method.md) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="53570-125">Quando è impostato il bit di stile **autopace** , la parola Balloon esegue il ritmo dell'output in base alla frequenza di output corrente, ad esempio una parola alla volta.</span><span class="sxs-lookup"><span data-stu-id="53570-125">When the **AutoPace** style bit is set, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="53570-126">Quando l'output supera le dimensioni del fumetto, viene automaticamente eseguito lo scorrimento del testo precedente.</span><span class="sxs-lookup"><span data-stu-id="53570-126">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="53570-127">Quando non è impostato, tutto il testo incluso in un'istruzione [**Speak**](speak-method.md) o [**think**](think-method.md) viene visualizzato in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="53570-127">When not set, all text included in a [**Speak**](speak-method.md) or [**Think**](think-method.md) statement displays at once.</span></span>

<span data-ttu-id="53570-128">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="53570-128">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="53570-129">Le impostazioni predefinite per questi bit di stile sono basate sulle impostazioni quando il carattere viene compilato tramite l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="53570-129">The defaults for these style bits are based on the settings when the character is compiled through the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="53570-130">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="53570-130">See Also</span></span>

[<span data-ttu-id="53570-131">**IAgentBalloonEx:: Sestyle**</span><span class="sxs-lookup"><span data-stu-id="53570-131">**IAgentBalloonEx::SetStyle**</span></span>](iagentballoonex--setstyle.md)


 

 





