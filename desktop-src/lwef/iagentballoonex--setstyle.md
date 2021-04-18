---
title: IAgentBalloonEx-stile
description: IAgentBalloonEx-stile
ms.assetid: 5be569b7-8a2d-437b-b5db-401af343bc78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d942cc8adaf454a7c5f1cd299581f917560c00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298981"
---
# <a name="iagentballoonexsetstyle"></a><span data-ttu-id="251c6-103">IAgentBalloonEx:: Sestyle</span><span class="sxs-lookup"><span data-stu-id="251c6-103">IAgentBalloonEx::SetStyle</span></span>

<span data-ttu-id="251c6-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="251c6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetStyle(
   long lStyle,  // style settings
);
```

<span data-ttu-id="251c6-105">Recupera le impostazioni di stile del fumetto Word del carattere.</span><span class="sxs-lookup"><span data-stu-id="251c6-105">Retrieves the character's word balloon style settings.</span></span>

-   <span data-ttu-id="251c6-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="251c6-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="251c6-107"><span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lStyle*</span><span class="sxs-lookup"><span data-stu-id="251c6-107"><span id="lStyle"></span><span id="lstyle"></span><span id="LSTYLE"></span>*lStyle*</span></span>
</dt> <dd>

<span data-ttu-id="251c6-108">Impostazioni di stile per la parola Balloon, che può essere una combinazione dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="251c6-108">Style settings for the word balloon, which can be a combination of any of the following values:</span></span>



| <span data-ttu-id="251c6-109">Valore</span><span class="sxs-lookup"><span data-stu-id="251c6-109">Value</span></span>                                                                            | <span data-ttu-id="251c6-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="251c6-110">Description</span></span>                                                 |
|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="251c6-111">**const unsigned short** **Balloon \_ Style \_ BALLOONON = 0x00000001;**</span><span class="sxs-lookup"><span data-stu-id="251c6-111">**const unsigned short** **BALLOON\_STYLE\_BALLOONON = 0x00000001;**</span></span><br/>  | <span data-ttu-id="251c6-112">Il fumetto è supportato per l'output.</span><span class="sxs-lookup"><span data-stu-id="251c6-112">The balloon is supported for output.</span></span>                        |
| <span data-ttu-id="251c6-113">**const unsigned short** **Balloon \_ Style \_ SIZETOTEXT = 0x0000002;**</span><span class="sxs-lookup"><span data-stu-id="251c6-113">**const unsigned short** **BALLOON\_STYLE \_SIZETOTEXT = 0x0000002;**</span></span><br/> | <span data-ttu-id="251c6-114">L'altezza del fumetto è dimensionata in modo da contenere l'output di testo.</span><span class="sxs-lookup"><span data-stu-id="251c6-114">The balloon height is sized to accommodate the text output.</span></span> |
| <span data-ttu-id="251c6-115">Nascondi automaticamente lo stile di un **breve fumetto const senza segno** **\_ \_ = 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="251c6-115">**const unsigned short** **BALLOON\_STYLE \_AUTOHIDE = 0x00000004;**</span></span><br/>  | <span data-ttu-id="251c6-116">Il fumetto viene nascosto automaticamente.</span><span class="sxs-lookup"><span data-stu-id="251c6-116">The balloon is automatically hidden.</span></span>                        |
| <span data-ttu-id="251c6-117">autopace **senza segno const unsigned short** **Balloon \_ \_ = 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="251c6-117">**const unsigned short** **BALLOON\_STYLE \_AUTOPACE = 0x00000008;**</span></span><br/>  | <span data-ttu-id="251c6-118">L'output di testo viene gestito in base alla frequenza di output.</span><span class="sxs-lookup"><span data-stu-id="251c6-118">The text output is paced based on the output rate.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="251c6-119">Quando viene impostato il bit di stile **BalloonOn** , la parola Balloon viene visualizzata quando viene usato il metodo [**Speak**](speak-method.md) o [**think**](think-method.md) , a meno che l'utente non esegua l'override della relativa visualizzazione nella finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="251c6-119">When the **BalloonOn** style bit is set, the word balloon appears when the [**Speak**](speak-method.md) or [**Think**](think-method.md) method is used, unless the user overrides its display in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="251c6-120">Quando non è impostato, non viene visualizzato alcun fumetto.</span><span class="sxs-lookup"><span data-stu-id="251c6-120">When not set, no balloon appears.</span></span>

<span data-ttu-id="251c6-121">Quando è impostato il bit di stile **SizeToText** , la parola Balloon ridimensiona automaticamente l'altezza del fumetto alla dimensione corrente del testo specificato nel metodo [**Speak**](speak-method.md) o [**think**](think-method.md) .</span><span class="sxs-lookup"><span data-stu-id="251c6-121">When the **SizeToText** style bit is set, the word balloon automatically sizes the height of the balloon to the current size of the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method.</span></span> <span data-ttu-id="251c6-122">Quando non è impostato, l'altezza del fumetto è basata sull'impostazione della proprietà Number of Lines del fumetto.</span><span class="sxs-lookup"><span data-stu-id="251c6-122">When not set, the balloon's height is based on the balloon's number of lines property setting.</span></span> <span data-ttu-id="251c6-123">Questo bit di stile è impostato su 1 e un tentativo di utilizzare [**IAgentBalloonEx:: SetNumLines**](iagentballoonex--setnumlines.md) comporterà un errore.</span><span class="sxs-lookup"><span data-stu-id="251c6-123">This style bit is set to 1 and an attempt to use [**IAgentBalloonEx::SetNumLines**](iagentballoonex--setnumlines.md) will result in an error.</span></span>

<span data-ttu-id="251c6-124">Quando viene impostato il bit di stile **Nascondi** automaticamente, la parola fumetto viene nascosta automaticamente dopo un breve timeout.</span><span class="sxs-lookup"><span data-stu-id="251c6-124">When the **AutoHide** style bit is set, the word balloon automatically hides after a short timeout.</span></span> <span data-ttu-id="251c6-125">Quando non è impostato, il fumetto viene visualizzato fino a quando [](think-method.md) non viene visualizzata una nuova chiamata, il carattere è [**nascosto oppure l'**](speak-method.md) utente fa clic o trascina il carattere.</span><span class="sxs-lookup"><span data-stu-id="251c6-125">When not set, the balloon displays until a new [**Speak**](speak-method.md) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="251c6-126">Quando è impostato il bit di stile **autopace** , la parola Balloon esegue il ritmo dell'output in base alla frequenza di output corrente, ad esempio una parola alla volta.</span><span class="sxs-lookup"><span data-stu-id="251c6-126">When the **AutoPace** style bit is set, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="251c6-127">Quando l'output supera le dimensioni del fumetto, viene automaticamente eseguito lo scorrimento del testo precedente.</span><span class="sxs-lookup"><span data-stu-id="251c6-127">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="251c6-128">Quando non è impostato, tutto il testo incluso in un'istruzione [**Speak**](speak-method.md) o [**think**](think-method.md) viene visualizzato in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="251c6-128">When not set, all text included in a [**Speak**](speak-method.md) or [**Think**](think-method.md) statement displays at once.</span></span>

<span data-ttu-id="251c6-129">La proprietà Style del fumetto può essere impostata anche se l'utente ha disabilitato la visualizzazione del fumetto usando la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="251c6-129">The Balloon's style property can be set even if the user has disabled display of the Balloon using the Microsoft Agent property sheet.</span></span>

<span data-ttu-id="251c6-130">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="251c6-130">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="251c6-131">Le impostazioni predefinite per questi bit di stile sono basate sulle impostazioni quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="251c6-131">The defaults for these style bits are based on their settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="251c6-132">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="251c6-132">See Also</span></span>

[<span data-ttu-id="251c6-133">**IAgentBalloonEx:: GetStyle**</span><span class="sxs-lookup"><span data-stu-id="251c6-133">**IAgentBalloonEx::GetStyle**</span></span>](iagentballoonex--getstyle.md)


 

 





