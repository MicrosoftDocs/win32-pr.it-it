---
title: Proprietà Voice (oggetto Commands)
description: Proprietà Voice
ms.assetid: 1feb5597-7971-4778-8221-2eb3a6e5e1ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0207fb4fb6f09d460496b6886354bc17738def17
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104517271"
---
# <a name="voice-property-commands-object"></a><span data-ttu-id="9e9e6-103">Proprietà Voice (oggetto Commands)</span><span class="sxs-lookup"><span data-stu-id="9e9e6-103">Voice Property (Commands Object)</span></span>

<span data-ttu-id="9e9e6-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9e9e6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="9e9e6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="9e9e6-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="9e9e6-106">Restituisce o imposta il testo passato alla grammatica del motore vocale (per il riconoscimento).</span><span class="sxs-lookup"><span data-stu-id="9e9e6-106">Returns or sets the text that is passed to the speech engine grammar (for recognition).</span></span>

</dd> <dt>

<span data-ttu-id="9e9e6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="9e9e6-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="9e9e6-108">\*agente \***. Caratteri ("**_CharacterID_\*_"). Stringa Commands. Voice_ \*  \[  =  \]</span><span class="sxs-lookup"><span data-stu-id="9e9e6-108">*agent\***.Characters ("**_CharacterID_*_").Commands.Voice_\* \[ = *string*\]</span></span>



| <span data-ttu-id="9e9e6-109">Parte</span><span class="sxs-lookup"><span data-stu-id="9e9e6-109">Part</span></span>     | <span data-ttu-id="9e9e6-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e9e6-110">Description</span></span>                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e9e6-111">*string*</span><span class="sxs-lookup"><span data-stu-id="9e9e6-111">*string*</span></span> | <span data-ttu-id="9e9e6-112">Espressione stringa corrispondente alle parole o alla frase che deve essere utilizzata dal motore di sintesi vocale per riconoscere questo comando.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-112">A string expression corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9e9e6-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e9e6-113">Remarks</span></span>

<span data-ttu-id="9e9e6-114">Se non si specifica questo parametro, il [**VoiceCaption**](voicecaption-property.md) per l'oggetto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) non verrà visualizzato nella finestra dei comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-114">If you do not supply this parameter, the [**VoiceCaption**](voicecaption-property.md) for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object will not appear in the Voice Commands Window.</span></span>

<span data-ttu-id="9e9e6-115">L'espressione stringa fornita può includere caratteri di parentesi quadre ( \[ \] ) per indicare parole facoltative e caratteri barra verticale ( \| ) per indicare stringhe alternative.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-115">The string expression you supply can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="9e9e6-116">Le alternative devono essere racchiuse tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-116">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="9e9e6-117">Ad esempio, "(Hello \[ There \] \| HI)" indica al motore di riconoscimento vocale di accettare "Hello", "Hello there" o "Hi" per il comando.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-117">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="9e9e6-118">Ricordarsi di includere spazi appropriati tra il testo racchiuso tra parentesi quadre o le parentesi e il testo che non è racchiuso tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-118">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span> <span data-ttu-id="9e9e6-119">È possibile usare l'operatore Star ( \* ) per specificare zero o più istanze delle parole incluse nel gruppo o l'operatore più (+) per specificare una o più istanze.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-119">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="9e9e6-120">Il codice seguente, ad esempio, genera una grammatica che supporta "try this", "try this", try this ", with Unlimited iteraziones of" Please ":</span><span class="sxs-lookup"><span data-stu-id="9e9e6-120">For example, the following results in a grammar that supports "try this", "please try this", "please please try this", with unlimited iterations of "please":</span></span>


```
   "please* try this"
```



<span data-ttu-id="9e9e6-121">Il formato di grammatica seguente esclude "try this" perché l'operatore + definisce almeno un'istanza di "Please":</span><span class="sxs-lookup"><span data-stu-id="9e9e6-121">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>


```
   "please+ try this"
```



<span data-ttu-id="9e9e6-122">Gli operatori di ripetizione seguono le normali regole di precedenza e si applicano all'elemento di testo immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-122">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="9e9e6-123">Ad esempio, la grammatica seguente restituisce "New York" e "New York York", ma non "New York New York":</span><span class="sxs-lookup"><span data-stu-id="9e9e6-123">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>


```
   "New York+"
```



<span data-ttu-id="9e9e6-124">Pertanto, in genere si desidera utilizzare questi operatori con i caratteri di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-124">Therefore, you typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="9e9e6-125">Ad esempio, la grammatica seguente include sia "New York" sia "New York New York":</span><span class="sxs-lookup"><span data-stu-id="9e9e6-125">For example, the following grammar includes both "New York" and "New York New York":</span></span>


```
   "(New York)+"
```



<span data-ttu-id="9e9e6-126">Gli operatori di ripetizione sono utili quando si desidera comporre una grammatica che includa una sequenza ripetuta, ad esempio un numero di telefono o una specifica di un elenco di elementi.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-126">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items.</span></span>


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



<span data-ttu-id="9e9e6-127">Anche se gli operatori possono essere utilizzati con il carattere di raggruppamento facoltativo tra parentesi quadre, in questo modo è possibile ridurre l'efficienza dell'elaborazione della grammatica da parte dell'agente.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-127">Although the operators can also be used with the optional square-brackets grouping character, doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="9e9e6-128">È anche possibile usare i puntini di sospensione (...) per supportare l' *individuazione* di parole, ovvero indicare al motore di riconoscimento vocale di ignorare le parole pronunciate in questa posizione nella frase (talvolta denominata *Garbage* Word).</span><span class="sxs-lookup"><span data-stu-id="9e9e6-128">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="9e9e6-129">Pertanto, il motore di riconoscimento vocale riconosce solo parole specifiche nella stringa, indipendentemente dal fatto che vengano pronunciate parole o frasi adiacenti.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-129">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="9e9e6-130">Se ad esempio si imposta questa proprietà su " \[ ... \] check mail \[ ... \] ", il motore di riconoscimento vocale corrisponderà a frasi come" controllare la posta elettronica "o" selezionare la posta elettronica "per questo comando.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-130">For example, if you set this property to "\[...\] check mail \[...\]", the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="9e9e6-131">I puntini di sospensione possono essere usati in qualsiasi punto all'interno di una stringa.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-131">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="9e9e6-132">Tuttavia, prestare attenzione quando si utilizza questa tecnica perché potrebbe aumentare il rischio di corrispondenze indesiderate.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-132">However, be careful using this technique as it may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="9e9e6-133">Quando si definisce la grammatica della parola per il comando, includere almeno una parola richiesta. ovvero evitare di fornire solo parole facoltative.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-133">When defining the word grammar for your command, include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="9e9e6-134">Assicurarsi inoltre che la parola includa solo parole e lettere pronunciabili.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-134">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="9e9e6-135">Per i numeri, è preferibile scrivere la parola anziché usare una rappresentazione ambigua.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-135">For numbers, it is better to spell out the word rather than using an ambiguous representation.</span></span> <span data-ttu-id="9e9e6-136">Ad esempio, "345" non è un formato di grammatica valido.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-136">For example, "345" is not a good grammar form.</span></span> <span data-ttu-id="9e9e6-137">Analogamente, anziché "IEEE", utilizzare "I triple E".</span><span class="sxs-lookup"><span data-stu-id="9e9e6-137">Similarly, instead of "IEEE", use "I triple E".</span></span> <span data-ttu-id="9e9e6-138">Omettere anche segni di punteggiatura o simboli.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-138">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="9e9e6-139">Ad esempio, invece di "The \# $1 10 pizza!", usare "The number 1 10 Dollar pizza".</span><span class="sxs-lookup"><span data-stu-id="9e9e6-139">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="9e9e6-140">L'inclusione di caratteri o simboli non pronunciabili per un comando può causare la mancata compilazione della grammatica da parte del motore vocale per tutti i comandi.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-140">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="9e9e6-141">Infine, impostare il parametro Voice come più ragionevolmente possibile da altri comandi vocali definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-141">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="9e9e6-142">Maggiore è la somiglianza tra la grammatica vocale per i comandi, più probabile verrà creato un errore di riconoscimento da parte del motore di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-142">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="9e9e6-143">È anche possibile usare i punteggi di confidenza per distinguere meglio tra due comandi che possono avere una grammatica vocale simile o simile.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-143">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="9e9e6-144">È possibile includere nelle parole grammaticali sotto forma di "*\\ pronuncia del testo*" *, dove il testo è* il testo visualizzato e la *pronuncia* è il testo che chiarisce la pronuncia.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-144">You can include in your grammar words in the form of "*text\\pronunciation*", where *text* is the text displayed and *pronunciation* is text that clarifies the pronunciation.</span></span> <span data-ttu-id="9e9e6-145">Ad esempio, la grammatica "1st \\ First" viene riconosciuta quando l'utente dice "First", ma l'evento del [**comando**](command-event.md) restituirà il testo "1st \\ First".</span><span class="sxs-lookup"><span data-stu-id="9e9e6-145">For example, the grammar, "1st\\first", would be recognized when the user says "first", but the [**Command**](command-event.md) event will return the text, "1st\\first".</span></span> <span data-ttu-id="9e9e6-146">È anche possibile usare IPA (alfabeto fonetico internazionale) per specificare una pronuncia iniziando la pronuncia con un segno di cancelletto (" \# "), quindi includere il testo che rappresenta la pronuncia IPA.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-146">You can also use IPA (International Phonetic Alphabet) to specify a pronunciation by beginning the pronunciation with a pound sign character ("\#"), then include the text representing the IPA pronunciation.</span></span>

<span data-ttu-id="9e9e6-147">Per i motori di riconoscimento vocale giapponese è possibile definire la grammatica nel formato "*Kana \\ kanji*", riducendo le pronunce alternative e aumentando la precisione.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-147">For Japanese speech recognition engines, you can define grammar in the form "*kana\\kanji*", reducing the alternative pronunciations and increasing the accuracy.</span></span> <span data-ttu-id="9e9e6-148">L'ordine è invertito per compatibilità con le versioni precedenti. Questa operazione è particolarmente importante per la pronuncia dei nomi appropriati in kanji.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-148">(The ordering is reversed for backward compatibility.) This is particularly important for the pronunciation of proper names in Kanji.</span></span> <span data-ttu-id="9e9e6-149">Tuttavia, è possibile passare solo Kanji senza kana, nel qual caso il motore deve restare in ascolto di tutte le pronunce accettabili per il kanji.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-149">However, you can just pass in Kanji without the Kana, in which case the engine should listen for all acceptable pronunciations for the Kanji.</span></span> <span data-ttu-id="9e9e6-150">È anche possibile passare solo Kana.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-150">You can also pass in just Kana.</span></span>

<span data-ttu-id="9e9e6-151">Si noti inoltre che per lingue quali giapponese, cinese e tailandese, che non utilizzano caratteri di spazio per designare le interruzioni di parola, inserire un carattere di spazio a larghezza zero Unicode (0x200B) per indicare le interruzioni di parola logiche.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-151">Also note that for languages such as Japanese, Chinese, and Thai, that do not use space characters to designate word breaks, insert a Unicode zero-width space character (0x200B) to indicate logical word breaks.</span></span>

<span data-ttu-id="9e9e6-152">Ad eccezione degli errori che usano i caratteri di raggruppamento o di ripetizione, Agent non segnala gli errori della grammatica, a meno che il motore non segnali l'errore.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-152">Except for errors using the grouping or repetition formatting characters, Agent will not report errors in your grammar, unless the engine itself reports the error.</span></span> <span data-ttu-id="9e9e6-153">Se si passa un testo nella grammatica che non riesce a compilare il motore, ma il motore non viene gestito e restituito come errore, Agent non è in grado di segnalare l'errore.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-153">If you pass text in your grammar that the engine fails to compile, but the engine does not handle and return as an error, Agent cannot report the error.</span></span> <span data-ttu-id="9e9e6-154">Pertanto, l'applicazione client deve definire con attenzione la grammatica per la proprietà **Voice** .</span><span class="sxs-lookup"><span data-stu-id="9e9e6-154">Therefore, the client application must be carefully define grammar for the **Voice** property.</span></span>

> [!Note]  
> <span data-ttu-id="9e9e6-155">Le funzionalità di grammatica disponibili possono dipendere dal motore di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-155">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="9e9e6-156">Si consiglia di verificare con il fornitore del motore di determinare quali opzioni di grammatica sono supportate.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-156">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="9e9e6-157">Usare [**SRModeID**](srmodeid-property.md) per usare un motore specifico.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-157">Use the [**SRModeID**](srmodeid-property.md) to use a specific engine.</span></span>

 

<span data-ttu-id="9e9e6-158">Il funzionamento di questa proprietà dipende dallo stato della proprietà di riconoscimento vocale del server.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-158">The operation of this property depends on the state of the server's speech recognition property.</span></span> <span data-ttu-id="9e9e6-159">Se, ad esempio, il riconoscimento vocale è disabilitato o non è installato, questa proprietà non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="9e9e6-159">For example, if speech recognition is disabled or not installed, this property has no effect.</span></span>

 

 
