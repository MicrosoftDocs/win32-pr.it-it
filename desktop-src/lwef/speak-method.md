---
title: Speak (metodo)
description: Speak (metodo)
ms.assetid: 6267e04c-feb5-4f48-8a88-4e6ca3388bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88792a53fac80c68154f938e91fb9bfe63b2b8e3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472923"
---
# <a name="speak-method"></a><span data-ttu-id="c38b5-103">Speak (metodo)</span><span class="sxs-lookup"><span data-stu-id="c38b5-103">Speak Method</span></span>

<span data-ttu-id="c38b5-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c38b5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c38b5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="c38b5-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c38b5-106">Pronuncia il testo o il file audio specificato per il carattere specificato.</span><span class="sxs-lookup"><span data-stu-id="c38b5-106">Speaks the specified text or sound file for the specified character.</span></span>

</dd> <dt>

<span data-ttu-id="c38b5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="c38b5-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c38b5-108">\*agente ***. Caratteri ("*** CharacterID \* \* *"). Pronuncia* \*  \[ *testo* \] , \[ *URL*\]</span><span class="sxs-lookup"><span data-stu-id="c38b5-108">*agent ***.Characters ("*** CharacterID\*\*\*").Speak*\* \[*Text*\], \[*Url*\]</span></span>



| <span data-ttu-id="c38b5-109">Parte</span><span class="sxs-lookup"><span data-stu-id="c38b5-109">Part</span></span>   | <span data-ttu-id="c38b5-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c38b5-110">Description</span></span>                                                                                                                                                                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c38b5-111">*Text*</span><span class="sxs-lookup"><span data-stu-id="c38b5-111">*Text*</span></span> | <span data-ttu-id="c38b5-112">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c38b5-112">Optional.</span></span> <span data-ttu-id="c38b5-113">Stringa che specifica l'elemento indicato dal carattere.</span><span class="sxs-lookup"><span data-stu-id="c38b5-113">A string that specifies what the character says.</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="c38b5-114">*Url*</span><span class="sxs-lookup"><span data-stu-id="c38b5-114">*Url*</span></span>  | <span data-ttu-id="c38b5-115">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c38b5-115">Optional.</span></span> <span data-ttu-id="c38b5-116">Espressione stringa che specifica il percorso di un file audio (. WAV o. Formato LWV).</span><span class="sxs-lookup"><span data-stu-id="c38b5-116">A string expression specifying the location of an audio file (.WAV or .LWV format).</span></span> <span data-ttu-id="c38b5-117">Il percorso può essere specificato come file (inclusa una specifica del percorso UNC) o un URL (quando vengono recuperati anche i dati di animazione dei caratteri tramite il protocollo HTTP).</span><span class="sxs-lookup"><span data-stu-id="c38b5-117">The location can be specified as a file (including a UNC path specification) or URL (when character animation data is also being retrieved via HTTP protocol).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c38b5-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="c38b5-118">Remarks</span></span>

<span data-ttu-id="c38b5-119">Sebbene i parametri *Text* e *URL* siano facoltativi, è necessario specificare uno di essi.</span><span class="sxs-lookup"><span data-stu-id="c38b5-119">Although the *Text* and *Url* parameters are optional, one of them must be supplied.</span></span> <span data-ttu-id="c38b5-120">Per usare questo metodo con un carattere configurato per parlare solo nella relativa bolla di parola o usando un motore di sintesi vocale, è sufficiente fornire il parametro di *testo* .</span><span class="sxs-lookup"><span data-stu-id="c38b5-120">To use this method with a character configured to speak only in its word balloon or using a text-to-speech (TTS) engine, simply provide the *Text* parameter.</span></span> <span data-ttu-id="c38b5-121">Includere uno spazio tra le parole per definire le interruzioni di parola appropriate nel fumetto di parole, anche per le lingue in cui non sono tradizionalmente inclusi gli spazi.</span><span class="sxs-lookup"><span data-stu-id="c38b5-121">Include a space between words to define appropriate word breaks in the word balloon, even for languages that do not traditionally include spaces.</span></span>

<span data-ttu-id="c38b5-122">È anche possibile includere caratteri barra verticale ( \| ) nel parametro di *testo* per designare stringhe alternative, in modo che il server scelga in modo casuale una stringa diversa ogni volta che elabora il metodo.</span><span class="sxs-lookup"><span data-stu-id="c38b5-122">You can also include vertical bar characters (\|) in the *Text* parameter to designate alternative strings, so that the server randomly chooses a different string each time it processes the method.</span></span>

<span data-ttu-id="c38b5-123">Il supporto dei caratteri dell'output TTS viene definito quando il carattere viene compilato tramite l'editor dei caratteri di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="c38b5-123">Character support of TTS output is defined when the character is compiled using the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="c38b5-124">Per generare l'output TTS, è necessario che sia già installato un motore TTS compatibile prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="c38b5-124">To generate TTS output, a compatible TTS engine must already be installed before calling this method.</span></span> <span data-ttu-id="c38b5-125">Per ulteriori informazioni, vedere [accesso ai servizi di riconoscimento vocale](accessing-speech-services.md).</span><span class="sxs-lookup"><span data-stu-id="c38b5-125">For further information, see [Accessing Speech Services](accessing-speech-services.md).</span></span>

<span data-ttu-id="c38b5-126">Se si usa il file audio registrato (. WAV o. Output del formato LWV) per il carattere, specificare il percorso del file nel parametro *URL* .</span><span class="sxs-lookup"><span data-stu-id="c38b5-126">If you use recorded sound-file (.WAV or .LWV format only) output for the character, specify the file's location in the *Url* parameter.</span></span> <span data-ttu-id="c38b5-127">Questa specifica di file può includere un percorso locale (assoluto o relativo) o UNC (Universal Naming Convention).</span><span class="sxs-lookup"><span data-stu-id="c38b5-127">This file specification can include a local (absolute or relative) or universal naming convention (UNC) path.</span></span> <span data-ttu-id="c38b5-128">Il nome file non può includere caratteri non inclusi nella tabella codici degli Stati Uniti 1252.</span><span class="sxs-lookup"><span data-stu-id="c38b5-128">The filename cannot include any characters not included in the US code page 1252.</span></span> <span data-ttu-id="c38b5-129">Tuttavia, se si utilizza il protocollo HTTP per accedere ai dati di animazione dei caratteri, utilizzare il metodo [**Get**](get-method.md) per caricare l'animazione prima di chiamare il metodo **Speak** .</span><span class="sxs-lookup"><span data-stu-id="c38b5-129">However, if you are using the HTTP protocol to access the character animation data, use the [**Get**](get-method.md) method to load the animation before calling the **Speak** method.</span></span> <span data-ttu-id="c38b5-130">Per informazioni su Creative, vedere [uso dello strumento di modifica audio per informazioni linguistiche di Microsoft](using-the-microsoft-linguistic-information-sound-editing-tool.md) . File LWV.</span><span class="sxs-lookup"><span data-stu-id="c38b5-130">See [Using the Microsoft Linguistic Information Sound Editing Tool](using-the-microsoft-linguistic-information-sound-editing-tool.md) for information about creative .LWV files.</span></span>

<span data-ttu-id="c38b5-131">Quando si usa l'output del file audio registrato, è comunque possibile usare il parametro *Text* per specificare le parole visualizzate nell'aerostato di parole del carattere.</span><span class="sxs-lookup"><span data-stu-id="c38b5-131">When using recorded sound-file output, you can still use the *Text* parameter to specify the words that appear in the character's word balloon.</span></span> <span data-ttu-id="c38b5-132">Tuttavia, se si specifica un file audio con funzionalità avanzate linguisticamente (. LWV) per il parametro *URL* e non specificare il testo per la parola Balloon, il parametro *Text* usa il testo archiviato nel file.</span><span class="sxs-lookup"><span data-stu-id="c38b5-132">However, if you specify a linguistically enhanced sound file (.LWV) for the *Url* parameter and do not specify text for the word balloon, the *Text* parameter uses the text stored in the file.</span></span>

<span data-ttu-id="c38b5-133">È anche possibile variare i parametri dell'output vocale con tag speciali inclusi nel parametro di *testo* .</span><span class="sxs-lookup"><span data-stu-id="c38b5-133">You can also vary parameters of the speech output with special tags that you include in the *Text* parameter.</span></span> <span data-ttu-id="c38b5-134">Per ulteriori informazioni, vedere [tag di output di sintesi vocale di Microsoft Agent](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="c38b5-134">For more information, see [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

<span data-ttu-id="c38b5-135">Se si dichiara un riferimento a un oggetto e lo si imposta su questo metodo, viene restituito un oggetto [**Request**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="c38b5-135">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="c38b5-136">È possibile usarlo per sincronizzare altre parti del codice con l'output parlato del carattere, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="c38b5-136">You can use this to synchronize other parts of your code with the character's spoken output, as in the following example:</span></span>


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here it is.")
...
   Sub Agent1_RequestComplete (ByVal Request as Object)
   ' Make certain the request exists
   If SpeakRequest Not Nothing Then
      ' See if it was this request
      If Request = SpeakRequest Then
         ' Display the message box 
         Msgbox "Ta da!"
      End If
   End If
   End Sub
```



<span data-ttu-id="c38b5-137">È anche possibile usare un oggetto [**Request**](/windows/desktop/lwef/the-request-object) per verificare la presenza di determinate condizioni di errore.</span><span class="sxs-lookup"><span data-stu-id="c38b5-137">You can also use a [**Request**](/windows/desktop/lwef/the-request-object) object to check for certain error conditions.</span></span> <span data-ttu-id="c38b5-138">Se, ad esempio, si usa il metodo **Speak** per parlare e non è installato un motore TTS compatibile, il server imposta la proprietà [**status**](status-property.md) dell'oggetto **Request** su "failed" con la relativa proprietà [**Description**](description-property.md) su "classe non registrata" o "errore sconosciuto o restituito oggetto".</span><span class="sxs-lookup"><span data-stu-id="c38b5-138">For example, if you use the **Speak** method to speak and do not have a compatible TTS engine installed, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with its [**Description**](description-property.md) property to "Class not registered" or "Unknown or object returned error".</span></span> <span data-ttu-id="c38b5-139">Per determinare se è installato un motore TTS, utilizzare la proprietà [**TTSModeID**](ttsmodeid-property.md) .</span><span class="sxs-lookup"><span data-stu-id="c38b5-139">To determine if you have a TTS engine installed, use the [**TTSModeID**](ttsmodeid-property.md) property.</span></span>

<span data-ttu-id="c38b5-140">Analogamente, se il carattere tenta di pronunciare un file audio e se il file non è stato caricato o se si verifica un problema con il dispositivo audio, il server imposta anche la proprietà [**status**](status-property.md) dell'oggetto [**Request**](/windows/desktop/lwef/the-request-object) su "failed" con un numero di codice di errore appropriato.</span><span class="sxs-lookup"><span data-stu-id="c38b5-140">Similarly, if you have the character attempt to speak a sound file, and if the file has not been loaded or there is a problem with the audio device, the server also sets the [**Request**](/windows/desktop/lwef/the-request-object) object's [**Status**](status-property.md) property to "failed" with an appropriate error code number.</span></span>

<span data-ttu-id="c38b5-141">Per sincronizzare il codice, è anche possibile includere tag di riconoscimento vocale nel testo Speak:</span><span class="sxs-lookup"><span data-stu-id="c38b5-141">You can also include bookmark speech tags in your Speak text to synchronize your code:</span></span>


```
   Dim SpeakRequest as Object
...
   Set SpeakRequest = Genie.Speak ("And here \mrk=100\it is.")
...
   Sub Agent1_Bookmark (ByVal BookmarkID As Long)
   If BookmarkID = 100 Then
      ' Display the message box 
         Msgbox "Tada!"
      End If
   End Sub
```



<span data-ttu-id="c38b5-142">Per altre informazioni sul tag vocale del segnalibro, vedere [tag di output vocale](mrk-tag.md).</span><span class="sxs-lookup"><span data-stu-id="c38b5-142">For more information on the bookmark speech tag, see [Speech Output Tags](mrk-tag.md).</span></span>

<span data-ttu-id="c38b5-143">Il metodo **Speak** usa l'ultima azione riprodotta per determinare quale animazione di pronuncia riprodurre.</span><span class="sxs-lookup"><span data-stu-id="c38b5-143">The **Speak** method uses the last action played to determine which speaking animation to play.</span></span> <span data-ttu-id="c38b5-144">Se, ad esempio, il comando **Speak** è stato preceduto da [**Play**](play-method.md) "**GestureRight**", il server eseguirà **GestureRight** e quindi l'animazione **GestureRight** Speaking.</span><span class="sxs-lookup"><span data-stu-id="c38b5-144">For example, if you preceded the **Speak** command with a [**Play**](play-method.md) "**GestureRight**", the server will play **GestureRight** and then the **GestureRight** speaking animation.</span></span> <span data-ttu-id="c38b5-145">Se l'ultima animazione riprodotta non ha un'animazione di pronuncia, Agent riproduce l'animazione assegnata allo stato di **pronuncia** del carattere.</span><span class="sxs-lookup"><span data-stu-id="c38b5-145">If the last animation played has no speaking animation, Agent plays the animation assigned to the character's **Speaking** state.</span></span>

<span data-ttu-id="c38b5-146">Se si chiama **Speak** e il canale audio è occupato, l'output audio del carattere non verrà udito, ma il testo verrà visualizzato nella parola Balloon.</span><span class="sxs-lookup"><span data-stu-id="c38b5-146">If you call **Speak** and the audio channel is busy, the character's audio output will not be heard, but the text will display in the word balloon.</span></span>

<span data-ttu-id="c38b5-147">Il Word Breaking automatico dell'agente in Word Balloon interrompe le parole usando spazi vuoti (ad esempio, spazio o tabulazione).</span><span class="sxs-lookup"><span data-stu-id="c38b5-147">Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, Space or Tab).</span></span> <span data-ttu-id="c38b5-148">Tuttavia, se non è possibile, potrebbe interrompere una parola per adattarla al fumetto.</span><span class="sxs-lookup"><span data-stu-id="c38b5-148">However, if it cannot, it may break a word to fit the balloon.</span></span> <span data-ttu-id="c38b5-149">In lingue quali giapponese, cinese e tailandese, in cui gli spazi non vengono usati per interrompere le parole, inserire un carattere di spazio a larghezza zero Unicode (0x200B) tra i caratteri per definire interruzioni di parola logiche.</span><span class="sxs-lookup"><span data-stu-id="c38b5-149">In languages like Japanese, Chinese, and Thai, where spaces are not used to break words, insert a Unicode zero-width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="c38b5-150">Anche la proprietà [**Enabled**](enabled-property.md) del fumetto di Word deve essere **true** per visualizzare il testo.</span><span class="sxs-lookup"><span data-stu-id="c38b5-150">The word balloon's [**Enabled**](enabled-property.md) property must also be **True** for text to display.</span></span>

 

> [!Note]  
> <span data-ttu-id="c38b5-151">Impostare l'ID lingua del carattere (impostando il **LanguageID** del carattere prima di usare il metodo **Speak** per garantire la visualizzazione del testo appropriata all'interno del fumetto di Word.</span><span class="sxs-lookup"><span data-stu-id="c38b5-151">Set the character's language ID (by setting the character's **LanguageID** before using the **Speak** method to ensure appropriate text display within the word balloon.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="c38b5-152">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c38b5-152">See Also</span></span>

<span data-ttu-id="c38b5-153">[**Evento segnalibro**](bookmark-event.md), [**evento RequestStart**](requeststart-event.md), [**evento RequestComplete**](requestcomplete-event.md)</span><span class="sxs-lookup"><span data-stu-id="c38b5-153">[**Bookmark event**](bookmark-event.md), [**RequestStart event**](requeststart-event.md), [**RequestComplete event**](requestcomplete-event.md)</span></span>


 

 