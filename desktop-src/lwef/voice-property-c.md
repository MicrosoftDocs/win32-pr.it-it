---
title: Proprietà Voice (oggetto Command)
description: Informazioni sulla proprietà Voice dell'oggetto Command, che restituisce o imposta il testo per la grammatica del motore di riconoscimento vocale per la corrispondenza di questo comando per il carattere.
ms.assetid: e393aa89-6fa7-4080-9faf-66faca83d561
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee7981de076fb3c7d8f796a8cc7d1177f96495c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396146"
---
# <a name="voice-property-command-object"></a><span data-ttu-id="f330a-103">Proprietà Voice (oggetto Command)</span><span class="sxs-lookup"><span data-stu-id="f330a-103">Voice Property (Command Object)</span></span>

<span data-ttu-id="f330a-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f330a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="f330a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="f330a-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="f330a-106">Restituisce o imposta il testo passato alla grammatica del motore di riconoscimento vocale (per il riconoscimento) per la corrispondenza di [**questo comando**](/windows/desktop/lwef/the-command-object) per il carattere.</span><span class="sxs-lookup"><span data-stu-id="f330a-106">Returns or sets the text that is passed to the speech engine grammar (for recognition) for matching this [**Command**](/windows/desktop/lwef/the-command-object) for the character.</span></span>

</dd> <dt>

<span data-ttu-id="f330a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**</span><span class="sxs-lookup"><span data-stu-id="f330a-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="f330a-108">*agent\***. Caratteri ("**_CharacterID_*_"). Comandi ("_*_name_*_"). Stringa_ \*  \[  =  *vocale*\]</span><span class="sxs-lookup"><span data-stu-id="f330a-108">*agent\***.Characters ("**_CharacterID_*_").Commands ("_*_name_*_").Voice_\* \[ = *string*\]</span></span>



| <span data-ttu-id="f330a-109">Parte</span><span class="sxs-lookup"><span data-stu-id="f330a-109">Part</span></span>     | <span data-ttu-id="f330a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f330a-110">Description</span></span>                                                                                                                                       |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f330a-111">*string*</span><span class="sxs-lookup"><span data-stu-id="f330a-111">*string*</span></span> | <span data-ttu-id="f330a-112">Espressione stringa corrispondente alle parole o alle frasi che devono essere usate dal motore di riconoscimento vocale per il riconoscimento di [**questo comando.**](/windows/desktop/lwef/the-command-object)</span><span class="sxs-lookup"><span data-stu-id="f330a-112">A string expression corresponding to the words or phrase to be used by the speech engine for recognizing this [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f330a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f330a-113">Remarks</span></span>

<span data-ttu-id="f330a-114">Se non si specifica questo parametro, [**l'oggetto VoiceCaption**](voicecaption-property.md) per [**l'oggetto Commands**](/windows/desktop/lwef/the-commands-collection-object) non verrà visualizzato nella finestra Comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="f330a-114">If you do not supply this parameter, the [**VoiceCaption**](voicecaption-property.md) for your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object will not appear in the Voice Commands Window.</span></span> <span data-ttu-id="f330a-115">Se si specifica un parametro [**Voice**](voice-property.md) ma non **voiceCaption** (o [**Caption),**](https://www.bing.com/search?q=**Caption**)il comando non verrà visualizzato nella finestra Comandi vocali, ma sarà accessibile dalla voce quando l'applicazione client diventa attiva per l'input.</span><span class="sxs-lookup"><span data-stu-id="f330a-115">If you specify a [**Voice**](voice-property.md) parameter but not a **VoiceCaption** (or [**Caption**](https://www.bing.com/search?q=**Caption**)), the command will not appear in the Voice Commands Window, but it will be voice-accessible when the client application becomes input-active.</span></span>

<span data-ttu-id="f330a-116">L'espressione stringa può includere parentesi quadre ( ) per indicare parole facoltative e caratteri barra \[ \] verticale ( ) per indicare \| stringhe alternative.</span><span class="sxs-lookup"><span data-stu-id="f330a-116">Your string expression can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="f330a-117">Le alternative devono essere racchiuse tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="f330a-117">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="f330a-118">Ad esempio, "(hello there hi)" indica al motore di riconoscimento vocale di accettare \[ \] \| "hello", "hello there" o "hi" per il comando.</span><span class="sxs-lookup"><span data-stu-id="f330a-118">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="f330a-119">Ricordarsi di includere gli spazi appropriati tra il testo tra parentesi quadre o tra parentesi e il testo che non è tra parentesi o parentesi.</span><span class="sxs-lookup"><span data-stu-id="f330a-119">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span>

<span data-ttu-id="f330a-120">È possibile usare l'operatore star ( ) per specificare zero o più istanze delle parole incluse nel gruppo o l'operatore più (+) per specificare una \* o più istanze.</span><span class="sxs-lookup"><span data-stu-id="f330a-120">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="f330a-121">Ad esempio, i risultati seguenti in una grammatica che supporta "prova questo", "prova questo", "prova questo", "prova questo", con iterazioni illimitate di "please":</span><span class="sxs-lookup"><span data-stu-id="f330a-121">For example, the following results in a grammar that supports "try this", "please try this", "please please try this", with unlimited iterations of "please":</span></span>


```
   "please* try this"
```



<span data-ttu-id="f330a-122">Il formato grammaticale seguente esclude "try this" perché l'operatore + definisce almeno un'istanza di "please":</span><span class="sxs-lookup"><span data-stu-id="f330a-122">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>


```
   "please+ try this"
```



<span data-ttu-id="f330a-123">Gli operatori di ripetizione seguono le normali regole di precedenza e si applicano all'elemento di testo immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="f330a-123">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="f330a-124">Ad esempio, la grammatica seguente determina "New York" e "New York York", ma non "New York New York":</span><span class="sxs-lookup"><span data-stu-id="f330a-124">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>


```
   "New York+"
```



<span data-ttu-id="f330a-125">Pertanto, in genere si vogliono usare questi operatori con i caratteri di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="f330a-125">Therefore, you typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="f330a-126">Ad esempio, la grammatica seguente include sia "New York" che "New York New York":</span><span class="sxs-lookup"><span data-stu-id="f330a-126">For example, the following grammar includes both "New York" and "New York New York":</span></span>


```
   "(New York)+"
```



<span data-ttu-id="f330a-127">Gli operatori di ripetizione sono utili quando si vuole comporre una grammatica che include una sequenza ripetuta, ad esempio un numero di telefono o una specifica di un elenco di elementi.</span><span class="sxs-lookup"><span data-stu-id="f330a-127">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items.</span></span>


```
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```



<span data-ttu-id="f330a-128">Anche se gli operatori possono essere usati anche con il carattere di raggruppamento facoltativo tra parentesi quadre, questa operazione può ridurre l'efficienza dell'elaborazione della grammatica da parte di Agent.</span><span class="sxs-lookup"><span data-stu-id="f330a-128">Although the operators can also be used with the optional square-brackets grouping character, doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="f330a-129">È anche possibile usare i puntini di sospensione (...) per supportare l'avvistamento di parole, ovvero  per fare in modo che il motore di riconoscimento vocale ignori le parole pronunciate in questa posizione nella frase (talvolta dette parole non usate).</span><span class="sxs-lookup"><span data-stu-id="f330a-129">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="f330a-130">Di conseguenza, il motore di riconoscimento vocale riconosce solo parole specifiche nella stringa, indipendentemente da quando vengono pronunciate con parole o frasi adiacenti.</span><span class="sxs-lookup"><span data-stu-id="f330a-130">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="f330a-131">Ad esempio, se si imposta questa proprietà su " \[ ... \] check mail ... ", il motore di riconoscimento vocale corrisponderà a frasi come \[ \] "controlla posta" o "controlla posta per favore" a questo comando.</span><span class="sxs-lookup"><span data-stu-id="f330a-131">For example, if you set this property to "\[...\] check mail \[...\]", the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="f330a-132">I puntini di sospensione possono essere usati ovunque all'interno di una stringa.</span><span class="sxs-lookup"><span data-stu-id="f330a-132">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="f330a-133">Tuttavia, prestare attenzione a usare questa tecnica perché può aumentare il potenziale di corrispondenze indesiderate.</span><span class="sxs-lookup"><span data-stu-id="f330a-133">However, be careful using this technique as it may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="f330a-134">Quando si definisce la grammatica delle parole per il comando, includere almeno una parola necessaria. in altre parole, evitare di specificare solo parole facoltative.</span><span class="sxs-lookup"><span data-stu-id="f330a-134">When defining the word grammar for your command, include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="f330a-135">Assicurarsi inoltre che la parola includa solo parole e lettere pronunciabili.</span><span class="sxs-lookup"><span data-stu-id="f330a-135">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="f330a-136">Per i numeri, è meglio scrivere la parola anziché usare una rappresentazione ambigua.</span><span class="sxs-lookup"><span data-stu-id="f330a-136">For numbers, it is better to spell out the word rather than using an ambiguous representation.</span></span> <span data-ttu-id="f330a-137">Ad esempio, "345" non è un buon formato grammaticale.</span><span class="sxs-lookup"><span data-stu-id="f330a-137">For example, "345" is not a good grammar form.</span></span> <span data-ttu-id="f330a-138">Analogamente, invece di "IEEE", usare "I triple E".</span><span class="sxs-lookup"><span data-stu-id="f330a-138">Similarly, instead of "IEEE", use "I triple E".</span></span> <span data-ttu-id="f330a-139">Omettere anche eventuali segni di punteggiatura o simboli.</span><span class="sxs-lookup"><span data-stu-id="f330a-139">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="f330a-140">Ad esempio, anziché "la \# pizza da 1$10!", usare "la pizza numero 10 dollari".</span><span class="sxs-lookup"><span data-stu-id="f330a-140">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="f330a-141">Se si includono caratteri o simboli non pronunciabili per un comando, il motore di riconoscimento vocale potrebbe non compilare la grammatica per tutti i comandi.</span><span class="sxs-lookup"><span data-stu-id="f330a-141">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="f330a-142">Infine, rendere il parametro voce il più possibile distinto dagli altri comandi vocali definiti.</span><span class="sxs-lookup"><span data-stu-id="f330a-142">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="f330a-143">Maggiore è la somiglianza tra la grammatica vocale per i comandi, maggiore è la probabilità che il motore di riconoscimento vocale restituirà un errore di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="f330a-143">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="f330a-144">È anche possibile usare i punteggi di attendibilità per distinguere meglio tra due comandi che possono avere grammatica vocale simile o simile.</span><span class="sxs-lookup"><span data-stu-id="f330a-144">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="f330a-145">È possibile includere nelle parole grammaticali sotto forma di  "*\\ pronuncia* del testo ", dove testo è il testo visualizzato e *pronuncia* è testo che chiarisce la pronuncia.</span><span class="sxs-lookup"><span data-stu-id="f330a-145">You can include in your grammar words in the form of "*text\\pronunciation*", where *text* is the text displayed and *pronunciation* is text that clarifies the pronunciation.</span></span> <span data-ttu-id="f330a-146">Ad esempio, la grammatica "1st first", verrebbe riconosciuta quando l'utente dice "first", ma l'evento Command restituirà il testo \\ "1st [](/windows/desktop/lwef/the-command-object) \\ first".</span><span class="sxs-lookup"><span data-stu-id="f330a-146">For example, the grammar, "1st\\first", would be recognized when the user says "first", but the [**Command**](/windows/desktop/lwef/the-command-object) event will return the text, "1st\\first".</span></span> <span data-ttu-id="f330a-147">È anche possibile usare IPA (Alfabeto fonetico internazionale) per specificare una pronuncia iniziando la pronuncia con un carattere cancelletto (" "), quindi includere il testo che rappresenta la \# pronuncia IPA.</span><span class="sxs-lookup"><span data-stu-id="f330a-147">You can also use IPA (International Phonetic Alphabet) to specify a pronunciation by beginning the pronunciation with a pound sign character ("\#"), then include the text representing the IPA pronunciation.</span></span>

<span data-ttu-id="f330a-148">Per i motori di riconoscimento vocale giapponese, è possibile definire la grammatica nel formato "*kana \\ kanji*", riducendo le pronunce alternative e aumentando l'accuratezza.</span><span class="sxs-lookup"><span data-stu-id="f330a-148">For Japanese speech recognition engines, you can define grammar in the form "*kana\\kanji*", reducing the alternative pronunciations and increasing the accuracy.</span></span> <span data-ttu-id="f330a-149">L'ordinamento viene invertito per garantire la compatibilità con le versioni precedenti. Ciò è particolarmente importante per la pronuncia dei nomi propri in Kanji.</span><span class="sxs-lookup"><span data-stu-id="f330a-149">(The ordering is reversed for backward compatibility.) This is particularly important for the pronunciation of proper names in Kanji.</span></span> <span data-ttu-id="f330a-150">Tuttavia, è possibile passare kanji senza Kana, nel qual caso il motore deve restare in ascolto di tutte le pronunce accettabili per kanji.</span><span class="sxs-lookup"><span data-stu-id="f330a-150">However, you can just pass in Kanji without the Kana, in which case the engine should listen for all acceptable pronunciations for the Kanji.</span></span> <span data-ttu-id="f330a-151">È anche possibile passare solo Kana.</span><span class="sxs-lookup"><span data-stu-id="f330a-151">You can also pass in just Kana.</span></span>

<span data-ttu-id="f330a-152">Si noti anche che per lingue come il giapponese, il cinese e il tailandese, che non usano spazi per designare interruzioni di parola, inserire uno spazio unicode a larghezza zero (0x200B) per indicare interruzioni di parola logiche.</span><span class="sxs-lookup"><span data-stu-id="f330a-152">Also note that for languages such as Japanese, Chinese, and Thai, that do not use space characters to designate word breaks, insert a Unicode zero-width space character (0x200B) to indicate logical word breaks.</span></span>

<span data-ttu-id="f330a-153">Fatta eccezione per gli errori che usano i caratteri di formattazione di raggruppamento o ripetizione, Agent non segnala gli errori nella grammatica, a meno che il motore non ne restituirà l'errore.</span><span class="sxs-lookup"><span data-stu-id="f330a-153">Except for errors using the grouping or repetition formatting characters, Agent will not report errors in your grammar, unless the engine itself reports the error.</span></span> <span data-ttu-id="f330a-154">Se si passa testo nella grammatica che il motore non riesce a compilare, ma il motore non gestisce e restituisce come errore, Agent non può segnalare l'errore.</span><span class="sxs-lookup"><span data-stu-id="f330a-154">If you pass text in your grammar that the engine fails to compile, but the engine does not handle and return as an error, Agent cannot report the error.</span></span> <span data-ttu-id="f330a-155">Pertanto, l'applicazione client deve definire con attenzione la grammatica per la [**proprietà**](voice-property.md) Voice.</span><span class="sxs-lookup"><span data-stu-id="f330a-155">Therefore, the client application must be carefully define grammar for the [**Voice**](voice-property.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="f330a-156">Le funzionalità grammaticali disponibili possono dipendere dal motore di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="f330a-156">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="f330a-157">È possibile rivolgersi al fornitore del motore per determinare le opzioni grammaticali supportate.</span><span class="sxs-lookup"><span data-stu-id="f330a-157">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="f330a-158">Usare [**SRModeID**](srmodeid-property.md) per usare un motore specifico.</span><span class="sxs-lookup"><span data-stu-id="f330a-158">Use the [**SRModeID**](srmodeid-property.md) to use a specific engine.</span></span>

 

<span data-ttu-id="f330a-159">Il funzionamento di questa proprietà dipende dallo stato della proprietà di riconoscimento vocale del server.</span><span class="sxs-lookup"><span data-stu-id="f330a-159">The operation of this property depends on the state of the server's speech recognition property.</span></span> <span data-ttu-id="f330a-160">Ad esempio, se il riconoscimento vocale è disabilitato o non installato, questa proprietà non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="f330a-160">For example, if speech recognition is disabled or not installed, this property has no effect.</span></span>

 

 
