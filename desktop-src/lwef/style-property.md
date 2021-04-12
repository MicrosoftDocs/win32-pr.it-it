---
title: Style (proprietà)
description: Style (proprietà)
ms.assetid: f01d7d51-8a16-4265-b9b7-93b64f4984e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d46dd7f7ce0e2fdc16b8b17f9074b1eef30c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330071"
---
# <a name="style-property"></a><span data-ttu-id="b0ed4-103">Style (proprietà)</span><span class="sxs-lookup"><span data-stu-id="b0ed4-103">Style Property</span></span>

<span data-ttu-id="b0ed4-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b0ed4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="b0ed4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="b0ed4-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="b0ed4-106">Restituisce o imposta lo stile di output del fumetto Word del carattere.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-106">Returns or sets the character's word balloon output style.</span></span>

</dd> <dt>

<span data-ttu-id="b0ed4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="b0ed4-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b0ed4-108">\*agente. ***Caratteri ("*** CharacterID \* \* *"). Stile Balloon. Style* \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="b0ed4-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Balloon.Style** \[ = *Style*\]</span></span>



| <span data-ttu-id="b0ed4-109">Parte</span><span class="sxs-lookup"><span data-stu-id="b0ed4-109">Part</span></span>    | <span data-ttu-id="b0ed4-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0ed4-110">Description</span></span>                                                                                                                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0ed4-111">*Style*</span><span class="sxs-lookup"><span data-stu-id="b0ed4-111">*Style*</span></span> | <span data-ttu-id="b0ed4-112">Intero che rappresenta lo stile di output del fumetto.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-112">An integer that represents the balloon's output style.</span></span> <span data-ttu-id="b0ed4-113">L'impostazione di stile è un bit con bit corrispondenti a: Balloon-on (bit 0), dimensioni-testo (bit 1), Nascondi automaticamente (bit 2), velocità automatica (bit 3), numero di caratteri per riga (bit 16-23) e numero di righe (bit 24-31).</span><span class="sxs-lookup"><span data-stu-id="b0ed4-113">The style setting is a bitfield with bits corresponding to: balloon-on (bit 0), size-to-text (bit 1), auto-hide (bit 2), auto-pace (bit 3), number of characters per lines (bits 16-23), and number of lines (bits 24-31).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0ed4-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0ed4-114">Remarks</span></span>

<span data-ttu-id="b0ed4-115">Quando il bit di stile Balloon-on è impostato su 1, la parola Balloon viene visualizzata quando viene usato un metodo [**Speak**](https://www.bing.com/search?q=**Speak**) o [**think**](think-method.md) , a meno che l'utente non esegua l'override di questa impostazione nella finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-115">When the balloon-on style bit is set to 1, the word balloon appears when a [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) method is used, unless the user overrides this setting in the Microsoft Agent property sheet.</span></span> <span data-ttu-id="b0ed4-116">Se è impostato su 0, non viene visualizzato un fumetto.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-116">When set to 0, a balloon does not appear.</span></span>

<span data-ttu-id="b0ed4-117">Quando il bit di stile da dimensione a testo è impostato su 1, la parola Balloon ridimensiona automaticamente l'altezza del fumetto alla dimensione corrente del testo per l'istruzione [**Speak**](https://www.bing.com/search?q=**Speak**) o [**think**](think-method.md) .</span><span class="sxs-lookup"><span data-stu-id="b0ed4-117">When the size-to-text style bit is set to 1, the word balloon automatically sizes the height of the balloon to the current size of the text for the [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) statement.</span></span> <span data-ttu-id="b0ed4-118">Quando è impostato su 0, l'altezza del fumetto è basata sull'impostazione della proprietà [**numberoflines**](numberoflines-property.md) .</span><span class="sxs-lookup"><span data-stu-id="b0ed4-118">When set to 0, the balloon's height is based on the [**NumberOfLines**](numberoflines-property.md) property setting.</span></span> <span data-ttu-id="b0ed4-119">Se questo bit di stile è impostato su 1 e si tenta di impostare la proprietà **numberoflines** , Agent genera un errore.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-119">If this style bit is set to 1 and you attempt to set the **NumberOfLines** property, Agent raises an error.</span></span>

<span data-ttu-id="b0ed4-120">Quando il bit di stile Nascondi automaticamente è impostato su 1, la parola fumetto viene nascosta automaticamente quando l'output parlato viene completato.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-120">When the auto-hide style bit is set to 1, the word balloon automatically hides when spoken output completes.</span></span> <span data-ttu-id="b0ed4-121">Quando è impostato su 0, il fumetto rimane visualizzato fino alla [**chiamata successiva o**](https://www.bing.com/search?q=**Speak**) di [**interazione**](think-method.md) utente, il carattere è nascosto oppure l'utente fa clic o trascina il carattere.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-121">When set to 0, the balloon remains displayed until the next [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) call, the character is hidden, or the user clicks or drags the character.</span></span>

<span data-ttu-id="b0ed4-122">Quando il bit di stile di regolazione automatica è impostato su 1, la parola Balloon esegue il ritmo dell'output in base alla frequenza di output corrente, ad esempio una parola alla volta.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-122">When the auto-pace style bit is set to 1, the word balloon paces the output based on the current output rate, for example, one word at a time.</span></span> <span data-ttu-id="b0ed4-123">Quando l'output supera le dimensioni del fumetto, viene automaticamente eseguito lo scorrimento del testo precedente.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-123">When output exceeds the size of the balloon, the former text is automatically scrolled.</span></span> <span data-ttu-id="b0ed4-124">Se impostato su 0, tutto il testo incluso in un'istruzione [**Speak**](https://www.bing.com/search?q=**Speak**) o [**think**](think-method.md) viene visualizzato in una sola volta.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-124">When set to 0, all text included in a [**Speak**](https://www.bing.com/search?q=**Speak**) or [**Think**](think-method.md) statement is displayed at once.</span></span>

<span data-ttu-id="b0ed4-125">Per recuperare solo il valore dei quattro bit inferiori **e** il valore restituito dallo **stile** con 255.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-125">To retrieve just the value of the bottom four bits, **And** the value returned by **Style** with 255.</span></span> <span data-ttu-id="b0ed4-126">Per impostare un valore di bit **oppure** il valore restituito con il valore dei bit che si desidera impostare.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-126">To set a bit value, **Or** the value returned with the value of the bits you want set.</span></span> <span data-ttu-id="b0ed4-127">Per disattivare un bit **e** il valore restituito con un complemento del bit:</span><span class="sxs-lookup"><span data-stu-id="b0ed4-127">To turn a bit off, **And** the value returned with one's complement of the bit:</span></span>


```
   Const BalloonOn = 1

   ' Turn the word balloon off
   Genie.Balloon.Style = Genie.Balloon.Style And (Not BalloonOn)
   Genie.Speak "No balloon"

   ' Turn the word balloon on
   Genie.Balloon.Style = Genie.Balloon.Style Or BalloonOn
   Genie.Speak "Balloon"
```



<span data-ttu-id="b0ed4-128">La proprietà **Style** restituisce anche il numero di caratteri per riga nel byte inferiore della parola superiore e il numero di righe nel byte massimo della parola superiore.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-128">The **Style** property also returns the number of characters per line in the lower byte of the upper word and the number of lines in the high byte of the upper word.</span></span> <span data-ttu-id="b0ed4-129">Sebbene questa operazione possa essere letta più facilmente usando le proprietà [**CharsPerLine**](charsperline-property.md) e [**numberoflines**](numberoflines-property.md), la proprietà **Style** consente anche di impostare tali valori.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-129">While this can be more easily read using the [**CharsPerLine**](charsperline-property.md) and [**NumberOfLines**](numberoflines-property.md)properties, the **Style** property also enables you to set those values.</span></span>

<span data-ttu-id="b0ed4-130">Per modificare, ad esempio, il numero di righe, deselezionare bits 24 to 31 con un'operazione **and** logica prima di impostare il nuovo valore come prodotto del nuovo valore Times 2 ^ 24, aggiunto al valore esistente della proprietà **Style** .</span><span class="sxs-lookup"><span data-stu-id="b0ed4-130">For example, to change the number of lines, clear bits 24 to 31 with a logical **AND** operation before setting the new value as the product of the new value times 2^24, added to the existing value of the **Style** property.</span></span>


```
   ' Set the number of lines to 4
   Genie.Balloon.Style = (Genie.Balloon.Style <b>AND</b> &amp;H00FFFFFF) + (4*(2^24))
```



<span data-ttu-id="b0ed4-131">Per impostare il numero di caratteri per riga, deselezionare BITS da 16 a 23 con un'operazione **and** logica prima di impostare il nuovo valore come prodotto del nuovo valore Times 2 ^ 16, aggiunto al valore esistente della proprietà Style.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-131">To set the number of characters per line, clear bits 16 to 23 with a logical **AND** operation before setting the new value as the product of the new value times 2^16, added to the existing value of the Style property.</span></span>


```
   ' Set the number of characters per line to 16
   Genie.Balloon.Style = (Genie.Balloon.Style AND &amp;HFF00FFFF) + (16*(2^16))
```



<span data-ttu-id="b0ed4-132">La proprietà **Style** può essere impostata anche se l'utente ha disabilitato la visualizzazione del fumetto usando la finestra delle proprietà di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-132">The **Style** property can be set even if the user has disabled balloon display using the Microsoft Agent property sheet.</span></span> <span data-ttu-id="b0ed4-133">Tuttavia, i valori per il numero di righe devono essere compresi tra 1 e 128 e il numero di caratteri per riga deve essere compreso tra 8 e 255.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-133">However, the values for the number of lines must be between 1 and 128 and the number characters per line must be between 8 and 255.</span></span> <span data-ttu-id="b0ed4-134">Se si fornisce un valore non valido per la proprietà **Style** , Agent genererà un errore.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-134">If you provide an invalid value for the **Style** property, Agent will raise an error.</span></span>

<span data-ttu-id="b0ed4-135">Questa proprietà si applica solo all'utilizzo del carattere da parte dell'applicazione client. l'impostazione non influisce sugli altri client del carattere o di altri caratteri dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-135">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="b0ed4-136">Le impostazioni predefinite per questi bit di stile sono basate sulle impostazioni quando il carattere viene compilato con l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="b0ed4-136">The defaults for these style bits are based on their settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

 

 




