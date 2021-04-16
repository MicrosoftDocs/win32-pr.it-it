---
title: IAgentCharacter parla
description: IAgentCharacter parla
ms.assetid: 3c4baf83-9e69-4048-bdaf-4ead8ea8e7cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e290ab9037ee6f261445d4dfd00a206213cd26
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516768"
---
# <a name="iagentcharacterspeak"></a><span data-ttu-id="8cef4-103">IAgentCharacter:: Speak</span><span class="sxs-lookup"><span data-stu-id="8cef4-103">IAgentCharacter::Speak</span></span>

<span data-ttu-id="8cef4-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8cef4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Speak(
   BSTR bszText,    // text to speak
   BSTR bszURL,     // URL of a file to speak
   long * pdwReqID  // address of a request ID
);
```

<span data-ttu-id="8cef4-105">Pronuncia il testo o il file audio.</span><span class="sxs-lookup"><span data-stu-id="8cef4-105">Speaks the text or sound file.</span></span>

-   <span data-ttu-id="8cef4-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="8cef4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8cef4-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span><span class="sxs-lookup"><span data-stu-id="8cef4-107"><span id="bszText"></span><span id="bsztext"></span><span id="BSZTEXT"></span>*bszText*</span></span>
</dt> <dd>

<span data-ttu-id="8cef4-108">Testo da pronunciare per il carattere.</span><span class="sxs-lookup"><span data-stu-id="8cef4-108">The text the character is to speak.</span></span>

</dd> <dt>

<span data-ttu-id="8cef4-109"><span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*</span><span class="sxs-lookup"><span data-stu-id="8cef4-109"><span id="bszURL"></span><span id="bszurl"></span><span id="BSZURL"></span>*bszURL*</span></span>
</dt> <dd>

<span data-ttu-id="8cef4-110">URL (o specifica del file) di un file audio da usare per l'output parlato.</span><span class="sxs-lookup"><span data-stu-id="8cef4-110">The URL (or file specification) of a sound file to use for spoken output.</span></span> <span data-ttu-id="8cef4-111">Può trattarsi di un file audio standard (. WAV) o file audio con funzionalità avanzate linguisticamente (. LWV).</span><span class="sxs-lookup"><span data-stu-id="8cef4-111">This can be a standard sound file (.WAV) or linguistically enhanced sound file (.LWV).</span></span>

</dd> <dt>

<span data-ttu-id="8cef4-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="8cef4-112"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="8cef4-113">Indirizzo di una variabile che riceve l'ID della richiesta [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) .</span><span class="sxs-lookup"><span data-stu-id="8cef4-113">Address of a variable that receives the [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="8cef4-114">Per usare questo metodo con un carattere configurato per parlare usando un motore di sintesi vocale; è sufficiente specificare il parametro *bszText* .</span><span class="sxs-lookup"><span data-stu-id="8cef4-114">To use this method with a character configured to speak using a text-to-speech (TTS) engine; simply provide the *bszText* parameter.</span></span> <span data-ttu-id="8cef4-115">È possibile includere caratteri barra verticale ( \| ) nel parametro *bszText* per designare stringhe alternative, in modo che ogni volta che il server elabora il metodo, scelga in modo casuale una stringa diversa.</span><span class="sxs-lookup"><span data-stu-id="8cef4-115">You can include vertical bar characters (\|) in the *bszText* parameter to designate alternative strings, so that each time the server processes the method, it randomly choose a different string.</span></span> <span data-ttu-id="8cef4-116">Il supporto dell'output TTS viene definito quando il carattere viene compilato mediante l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="8cef4-116">Support of TTS output is defined when the character is compiled using the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="8cef4-117">Se si vuole usare l'output del file audio per il carattere, specificare il percorso del file nel parametro *bszURL* .</span><span class="sxs-lookup"><span data-stu-id="8cef4-117">If you want to use sound file output for the character, specify the location for the file in the *bszURL* parameter.</span></span> <span data-ttu-id="8cef4-118">Quando si utilizza il protocollo HTTP per scaricare un file audio, utilizzare il metodo [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per garantire la disponibilità del file prima di utilizzare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="8cef4-118">When using the HTTP protocol to download a sound file, use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to ensure the availability of the file before using this method.</span></span> <span data-ttu-id="8cef4-119">È possibile usare il parametro *bszText* per specificare le parole visualizzate nell'aerostato di parola del carattere.</span><span class="sxs-lookup"><span data-stu-id="8cef4-119">You can use the *bszText* parameter to specify the words that appear in the character's word balloon.</span></span> <span data-ttu-id="8cef4-120">Se si specifica un file audio con funzionalità avanzate linguisticamente (. LWV) per il parametro *bszURL* e non specificare il testo, il parametro *bszText* usa il testo archiviato nel file.</span><span class="sxs-lookup"><span data-stu-id="8cef4-120">If you specify a linguistically enhanced sound file (.LWV) for the *bszURL* parameter and do not specify text, the *bszText* parameter uses the text stored in the file.</span></span>

<span data-ttu-id="8cef4-121">Il metodo [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) usa l'ultima animazione riprodotta per determinare quale animazione di pronuncia riprodurre.</span><span class="sxs-lookup"><span data-stu-id="8cef4-121">The [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) method uses the last animation played to determine which speaking animation to play.</span></span> <span data-ttu-id="8cef4-122">Se, ad esempio, si precede il comando **Speak** con [**IAgentCharacter::P Lay**](iagentcharacter--play.md) "**GestureRight**", il server riprodurrà **GestureRight** e quindi l'animazione **GestureRight** Speaking.</span><span class="sxs-lookup"><span data-stu-id="8cef4-122">For example, if you precede the **Speak** command with an [**IAgentCharacter::Play**](iagentcharacter--play.md) "**GestureRight**", the server will play **GestureRight** and then the **GestureRight** speaking animation.</span></span> <span data-ttu-id="8cef4-123">Se l'ultima animazione riprodotta non ha un'animazione di pronuncia, Microsoft Agent esegue l'animazione assegnata allo stato di **pronuncia** del carattere.</span><span class="sxs-lookup"><span data-stu-id="8cef4-123">If the last animation played has no speaking animation, then Microsoft Agent plays the animation assigned to the character's **Speaking** state.</span></span>

<span data-ttu-id="8cef4-124">Se si chiama [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) e il canale audio è occupato, l'output audio del carattere non verrà udito, ma il testo verrà visualizzato nella parola Balloon.</span><span class="sxs-lookup"><span data-stu-id="8cef4-124">If you call [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) and the audio channel is busy, the character's audio output will not be heard, but the text will display in the word balloon.</span></span> <span data-ttu-id="8cef4-125">Anche la proprietà [Enabled](enabled-property.md) del fumetto di Word deve essere **true** per visualizzare il testo.</span><span class="sxs-lookup"><span data-stu-id="8cef4-125">The word balloon's [Enabled](enabled-property.md) property must also be **True** for the text to display.</span></span>

<span data-ttu-id="8cef4-126">Il Word Breaking automatico dell'agente Microsoft in Word Balloon interrompe le parole usando spazi vuoti (ad esempio, spazio e tabulazione).</span><span class="sxs-lookup"><span data-stu-id="8cef4-126">Microsoft Agent's automatic word breaking in the word balloon, breaks words using white-space characters (for example, space and tab).</span></span> <span data-ttu-id="8cef4-127">Tuttavia, potrebbe suddividere una parola in modo da adattarla anche al fumetto.</span><span class="sxs-lookup"><span data-stu-id="8cef4-127">However, it may break a word to fit the balloon as well.</span></span> <span data-ttu-id="8cef4-128">In lingue quali giapponese, cinese e tailandese, in cui gli spazi non vengono usati per interrompere le parole, inserire un carattere di spazio a larghezza zero Unicode (0x200B) tra i caratteri per definire interruzioni di parola logiche.</span><span class="sxs-lookup"><span data-stu-id="8cef4-128">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="8cef4-129">Impostare l'ID lingua del carattere (usando [**IAgentCharacterEx:: SetLanguageID**](iagentcharacterex--setlanguageid.md) prima di usare il metodo [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) per garantire la visualizzazione del testo appropriata all'interno del fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="8cef4-129">Set the character's language ID (using [**IAgentCharacterEx::SetLanguageID**](iagentcharacterex--setlanguageid.md) before using the [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="8cef4-130">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8cef4-130">See Also</span></span>

<span data-ttu-id="8cef4-131">[**IAgentCharacter::P Lay**](iagentcharacter--play.md), [**IAgentBalloon:: GetEnabled**](iagentballoon--getenabled.md), [**IAgentCharacter::P ripare**](iagentcharacter--prepare.md)</span><span class="sxs-lookup"><span data-stu-id="8cef4-131">[**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentBalloon::GetEnabled**](iagentballoon--getenabled.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md)</span></span>


 

 