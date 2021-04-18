---
title: IAgentCommand
description: IAgentCommand
ms.assetid: bee06616-26bf-4e1e-89da-6765dd77fb02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36bed7e86cb93824fc26c770c1d01336077fda39
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299724"
---
# <a name="iagentcommandsetvoice"></a><span data-ttu-id="304b6-103">IAgentCommand:: sevoice</span><span class="sxs-lookup"><span data-stu-id="304b6-103">IAgentCommand::SetVoice</span></span>

<span data-ttu-id="304b6-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="304b6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoice(
   BSTR bszVoice  // voice text setting for Command
);
```

<span data-ttu-id="304b6-105">Imposta la proprietà [**Voice**](voice-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="304b6-105">Sets the [**Voice**](voice-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="304b6-106">Restituisce \_ OK per indicare che l'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="304b6-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="304b6-107"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span><span class="sxs-lookup"><span data-stu-id="304b6-107"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="304b6-108">BSTR che specifica il testo per la proprietà [**Voice**](voice-property.md) di un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="304b6-108">A BSTR that specifies the text for the [**Voice**](voice-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="304b6-109">Un [**comando**](/windows/desktop/lwef/the-command-object) deve avere la proprietà [**Voice**](voice-property.md) e la proprietà [**Enabled**](enabled-property.md) impostate per essere accessibile tramite voce.</span><span class="sxs-lookup"><span data-stu-id="304b6-109">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Voice**](voice-property.md) property and [**Enabled**](enabled-property.md) property set to be voice-accessible.</span></span> <span data-ttu-id="304b6-110">Inoltre, la proprietà [**VoiceCaption**](voicecaption-property.md) deve essere impostata per essere visualizzata nella **finestra dei comandi vocali**.</span><span class="sxs-lookup"><span data-stu-id="304b6-110">It also must have its [**VoiceCaption**](voicecaption-property.md) property set to appear in the **Voice Commands Window**.</span></span> <span data-ttu-id="304b6-111">(Per compatibilità con le versioni precedenti, se non esiste alcun **VoiceCaption**, viene utilizzata l'impostazione del [**titolo**](caption-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="304b6-111">(For backward compatibility, if there is no **VoiceCaption**, the [**Caption**](caption-property.md) setting is used.)</span></span>

<span data-ttu-id="304b6-112">L'espressione BSTR fornita può includere caratteri di parentesi quadre ( \[ \] ) per indicare parole facoltative e caratteri barra verticale ( \| ) per indicare stringhe alternative.</span><span class="sxs-lookup"><span data-stu-id="304b6-112">The BSTR expression you supply can include square bracket characters (\[ \]) to indicate optional words and vertical bar characters (\|) to indicate alternative strings.</span></span> <span data-ttu-id="304b6-113">Le alternative devono essere racchiuse tra parentesi.</span><span class="sxs-lookup"><span data-stu-id="304b6-113">Alternates must be enclosed in parentheses.</span></span> <span data-ttu-id="304b6-114">Ad esempio, "(Hello \[ There \] \| HI)" indica al motore di riconoscimento vocale di accettare "Hello", "Hello there" o "Hi" per il comando.</span><span class="sxs-lookup"><span data-stu-id="304b6-114">For example, "(hello \[there\] \| hi)" tells the speech engine to accept "hello," "hello there," or "hi" for the command.</span></span> <span data-ttu-id="304b6-115">Ricordarsi di includere spazi appropriati tra il testo racchiuso tra parentesi quadre o le parentesi e il testo che non è racchiuso tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="304b6-115">Remember to include appropriate spaces between the text that's in brackets or parentheses and the text that's not in brackets or parentheses.</span></span>

<span data-ttu-id="304b6-116">È possibile usare l'operatore Star ( \* ) per specificare zero o più istanze delle parole incluse nel gruppo o l'operatore più (+) per specificare una o più istanze.</span><span class="sxs-lookup"><span data-stu-id="304b6-116">You can use the star (\*) operator to specify zero or more instances of the words included in the group or the plus (+) operator to specify one or more instances.</span></span> <span data-ttu-id="304b6-117">Ad esempio, di seguito viene riportata una grammatica che supporta "try this", "try this" e "try this", with Unlimited iteraziones of "Please":</span><span class="sxs-lookup"><span data-stu-id="304b6-117">For example, the following results in a grammar that supports "try this", "please try this", and "please please try this", with unlimited iterations of "please":</span></span>

``` syntax
   "please* try this"
```

<span data-ttu-id="304b6-118">Il formato di grammatica seguente esclude "try this" perché l'operatore + definisce almeno un'istanza di "Please":</span><span class="sxs-lookup"><span data-stu-id="304b6-118">The following grammar format excludes "try this" because the + operator defines at least one instance of "please":</span></span>

``` syntax
   "please+ try this"
```

<span data-ttu-id="304b6-119">Gli operatori di ripetizione seguono le normali regole di precedenza e si applicano all'elemento di testo immediatamente precedente.</span><span class="sxs-lookup"><span data-stu-id="304b6-119">The repetition operators follow normal rules of precedence and apply to the immediately preceding text item.</span></span> <span data-ttu-id="304b6-120">Ad esempio, la grammatica seguente restituisce "New York" e "New York York", ma non "New York New York":</span><span class="sxs-lookup"><span data-stu-id="304b6-120">For example, the following grammar results in "New York" and "New York York", but not "New York New York":</span></span>

``` syntax
   "New York+"
```

<span data-ttu-id="304b6-121">Pertanto, in genere si desidera utilizzare questi operatori con i caratteri di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="304b6-121">Therefore, you will typically want to use these operators with the grouping characters.</span></span> <span data-ttu-id="304b6-122">Ad esempio, la grammatica seguente include sia "New York" sia "New York New York":</span><span class="sxs-lookup"><span data-stu-id="304b6-122">For example, the following grammar includes both "New York" and "New York New York":</span></span>

``` syntax
   "(New York)+"
```

<span data-ttu-id="304b6-123">Gli operatori di ripetizione sono utili quando si desidera comporre una grammatica che includa una sequenza ripetuta, ad esempio un numero di telefono o una specifica di un elenco di elementi:</span><span class="sxs-lookup"><span data-stu-id="304b6-123">Repetition operators are useful when you want to compose a grammar that includes a repeated sequence such as a phone number or specification of a list of items:</span></span>

``` syntax
   "call (one|two|three|four|five|six|seven|eight|nine|zero|oh)*"
   "I'd like (cheese|pepperoni|pineapple|canadian bacon|mushrooms|and)+"
```

<span data-ttu-id="304b6-124">Anche se gli operatori possono essere utilizzati anche con le parentesi quadre (un carattere di raggruppamento facoltativo), in questo modo è possibile ridurre l'efficienza dell'elaborazione della grammatica da parte dell'agente.</span><span class="sxs-lookup"><span data-stu-id="304b6-124">Although the operators can also be used with the square brackets (an optional grouping character), doing so may reduce the efficiency of Agent's processing of the grammar.</span></span>

<span data-ttu-id="304b6-125">È anche possibile usare i puntini di sospensione (...) per supportare l' *individuazione* di parole, ovvero indicare al motore di riconoscimento vocale di ignorare le parole pronunciate in questa posizione nella frase (talvolta denominata *Garbage* Word).</span><span class="sxs-lookup"><span data-stu-id="304b6-125">You can also use an ellipsis (...) to support *word spotting*, that is, telling the speech recognition engine to ignore words spoken in this position in the phrase (sometimes called *garbage* words).</span></span> <span data-ttu-id="304b6-126">Pertanto, il motore di riconoscimento vocale riconosce solo parole specifiche nella stringa, indipendentemente dal fatto che vengano pronunciate parole o frasi adiacenti.</span><span class="sxs-lookup"><span data-stu-id="304b6-126">Therefore, the speech engine recognizes only specific words in the string regardless of when spoken with adjacent words or phrases.</span></span> <span data-ttu-id="304b6-127">Se ad esempio si imposta questa proprietà su " \[ ... \] controllare la posta elettronica \[ ... \] "il motore di riconoscimento vocale corrisponde a frasi come" controllare la posta elettronica "o" selezionare la posta elettronica "per questo comando.</span><span class="sxs-lookup"><span data-stu-id="304b6-127">For example, if you set this property to "\[...\] check mail \[...\]" the speech recognition engine will match phrases like "please check mail" or "check mail please" to this command.</span></span> <span data-ttu-id="304b6-128">I puntini di sospensione possono essere usati in qualsiasi punto all'interno di una stringa.</span><span class="sxs-lookup"><span data-stu-id="304b6-128">Ellipses can be used anywhere within a string.</span></span> <span data-ttu-id="304b6-129">Tuttavia, prestare attenzione utilizzando questa tecnica, perché le impostazioni vocali con ellissi possono aumentare il potenziale di corrispondenze indesiderate.</span><span class="sxs-lookup"><span data-stu-id="304b6-129">However, be careful using this technique, because voice settings with ellipses may increase the potential of unwanted matches.</span></span>

<span data-ttu-id="304b6-130">Quando si definiscono le parole e la grammatica del comando, assicurarsi sempre di includere almeno una parola richiesta. ovvero evitare di fornire solo parole facoltative.</span><span class="sxs-lookup"><span data-stu-id="304b6-130">When defining the words and grammar for your command, always make sure that you include at least one word that is required; that is, avoid supplying only optional words.</span></span> <span data-ttu-id="304b6-131">Assicurarsi inoltre che la parola includa solo parole e lettere pronunciabili.</span><span class="sxs-lookup"><span data-stu-id="304b6-131">In addition, make sure that the word includes only pronounceable words and letters.</span></span> <span data-ttu-id="304b6-132">Per i numeri, è preferibile scrivere la parola anziché usare la rappresentazione numerica.</span><span class="sxs-lookup"><span data-stu-id="304b6-132">For numbers, it is better to spell out the word rather than using the numeric representation.</span></span> <span data-ttu-id="304b6-133">Omettere anche segni di punteggiatura o simboli.</span><span class="sxs-lookup"><span data-stu-id="304b6-133">Also, omit any punctuation or symbols.</span></span> <span data-ttu-id="304b6-134">Ad esempio, invece di "The \# $1 10 pizza!", usare "The number 1 10 Dollar pizza".</span><span class="sxs-lookup"><span data-stu-id="304b6-134">For example, instead of "the \#1 $10 pizza!", use "the number one ten dollar pizza".</span></span> <span data-ttu-id="304b6-135">L'inclusione di caratteri o simboli non pronunciabili per un comando può causare la mancata compilazione della grammatica da parte del motore vocale per tutti i comandi.</span><span class="sxs-lookup"><span data-stu-id="304b6-135">Including non-pronounceable characters or symbols for one command may cause the speech engine to fail to compile the grammar for all your commands.</span></span> <span data-ttu-id="304b6-136">Infine, impostare il parametro Voice come più ragionevolmente possibile da altri comandi vocali definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="304b6-136">Finally, make your voice parameter as distinct as reasonably possible from other voice commands you define.</span></span> <span data-ttu-id="304b6-137">Maggiore è la somiglianza tra la grammatica vocale per i comandi, più probabile verrà creato un errore di riconoscimento da parte del motore di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="304b6-137">The greater the similarity between the voice grammar for commands, the more likely the speech engine will make a recognition error.</span></span> <span data-ttu-id="304b6-138">È anche possibile usare i punteggi di confidenza per distinguere meglio tra due comandi che possono avere una grammatica vocale simile o simile.</span><span class="sxs-lookup"><span data-stu-id="304b6-138">You can also use the confidence scores to better distinguish between two commands that may have similar or similar-sounding voice grammar.</span></span>

<span data-ttu-id="304b6-139">L'impostazione della proprietà [**Voice**](voice-property.md) per un [**comando**](/windows/desktop/lwef/the-command-object) Abilita automaticamente i servizi di riconoscimento vocale di Agent, rendendo disponibili il tasto ascolto e il suggerimento di ascolto.</span><span class="sxs-lookup"><span data-stu-id="304b6-139">Setting the [**Voice**](voice-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object) automatically enables Agent's speech services, making the Listening key and Listening Tip available.</span></span> <span data-ttu-id="304b6-140">Tuttavia, non carica il motore di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="304b6-140">However, it does not load the speech recognition engine.</span></span>

> [!Note]  
> <span data-ttu-id="304b6-141">Le funzionalità di grammatica disponibili possono dipendere dal motore di riconoscimento vocale.</span><span class="sxs-lookup"><span data-stu-id="304b6-141">The grammar features available may depend on the speech recognition engine.</span></span> <span data-ttu-id="304b6-142">Si consiglia di verificare con il fornitore del motore di determinare quali opzioni di grammatica sono supportate.</span><span class="sxs-lookup"><span data-stu-id="304b6-142">You may want to check with the engine's vendor to determine what grammar options are supported.</span></span> <span data-ttu-id="304b6-143">Usare [**IAgentCharacterEx:: SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) per specificare un motore.</span><span class="sxs-lookup"><span data-stu-id="304b6-143">Use [**IAgentCharacterEx::SRModeID**](https://www.bing.com/search?q=**IAgentCharacterEx::SRModeID**) to specify an engine.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="304b6-144">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="304b6-144">See Also</span></span>

<span data-ttu-id="304b6-145">[**IAgentCommand:: getvoice**](iagentcommand--getvoice.md), [**IAgentCommand:: Caption**](iagentcommand--setcaption.md), [**IAgentCommand:: seenabled**](iagentcommand--setenabled.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="304b6-145">[**IAgentCommand::GetVoice**](iagentcommand--getvoice.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 