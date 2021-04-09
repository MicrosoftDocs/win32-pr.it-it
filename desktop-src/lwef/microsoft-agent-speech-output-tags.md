---
title: Tag output sintesi vocale agente Microsoft
description: Tag output sintesi vocale agente Microsoft
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d365d4837df3e3a5afb57c355e229f21ade0b5a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856213"
---
# <a name="microsoft-agent-speech-output-tags"></a><span data-ttu-id="916e9-103">Tag output sintesi vocale agente Microsoft</span><span class="sxs-lookup"><span data-stu-id="916e9-103">Microsoft Agent Speech Output Tags</span></span>

<span data-ttu-id="916e9-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="916e9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="916e9-105">I servizi di Microsoft Agent supportano la modifica dell'output vocale tramite tag speciali inseriti nella stringa di testo vocale.</span><span class="sxs-lookup"><span data-stu-id="916e9-105">The Microsoft Agent services support modifying speech output through special tags inserted in the speech text string.</span></span> <span data-ttu-id="916e9-106">Questi tag consentono di modificare le caratteristiche dell'espressione di output del carattere.</span><span class="sxs-lookup"><span data-stu-id="916e9-106">These tags help you change the characteristics of the output expression of the character.</span></span>

<span data-ttu-id="916e9-107">I tag di output vocale utilizzano le regole di sintassi seguenti:</span><span class="sxs-lookup"><span data-stu-id="916e9-107">Speech output tags use the following rules of syntax:</span></span>

-   <span data-ttu-id="916e9-108">Tutti i tag iniziano e terminano con un carattere barra rovesciata ( \) .</span><span class="sxs-lookup"><span data-stu-id="916e9-108">All tags begin and end with a backslash character (\).</span></span>
-   <span data-ttu-id="916e9-109">Il carattere barra rovesciata singola non è abilitato in un tag.</span><span class="sxs-lookup"><span data-stu-id="916e9-109">The single backslash character is not enabled within a tag.</span></span> <span data-ttu-id="916e9-110">Per includere un carattere barra rovesciata in un parametro di testo di un tag, utilizzare una doppia barra rovesciata ( \\ \) .</span><span class="sxs-lookup"><span data-stu-id="916e9-110">To include a backslash character in a text parameter of a tag, use a double backslash (\\\).</span></span>
-   <span data-ttu-id="916e9-111">I tag non fanno distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="916e9-111">Tags are case-insensitive.</span></span> <span data-ttu-id="916e9-112">Ad esempio, \\ Pit \\ è lo stesso di \\ Pit \\ .</span><span class="sxs-lookup"><span data-stu-id="916e9-112">For example, \\pit\\ is the same as \\PIT\\.</span></span>
-   <span data-ttu-id="916e9-113">I tag sono dipendenti da spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="916e9-113">Tags are whitespace-dependent.</span></span> <span data-ttu-id="916e9-114">Ad esempio, \\ RST \\ non è uguale a \\ RST \\ .</span><span class="sxs-lookup"><span data-stu-id="916e9-114">For example, \\Rst\\ is not the same as \\ Rst \\.</span></span>

<span data-ttu-id="916e9-115">Se non diversamente specificato o modificato da un altro tag, l'output vocale mantiene il set di caratteristiche dal tag all'interno del testo specificato in un singolo metodo [**Speak**](speak-method.md) .</span><span class="sxs-lookup"><span data-stu-id="916e9-115">Unless otherwise specified or modified by another tag, the speech output retains the characteristic set by the tag within the text specified in a single [**Speak**](speak-method.md) method.</span></span> <span data-ttu-id="916e9-116">L'output vocale viene reimpostato automaticamente tramite i parametri definiti dall'utente dopo il completamento di un metodo **Speak** .</span><span class="sxs-lookup"><span data-stu-id="916e9-116">Speech output is automatically reset through the user-defined parameters after a **Speak** method is completed.</span></span>

<span data-ttu-id="916e9-117">Alcuni tag includono stringhe tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="916e9-117">Some tags include quoted strings.</span></span> <span data-ttu-id="916e9-118">Per alcuni linguaggi di programmazione, ad esempio Visual Basic Scripting Edition (VBScript) e Visual Basic, ciò significa che potrebbe essere necessario utilizzare due virgolette per definire il parametro del tag o concatenare un carattere di virgolette doppie come parte della stringa.</span><span class="sxs-lookup"><span data-stu-id="916e9-118">For some programming languages, such as Visual Basic Scripting Edition (VBScript) and Visual Basic, this means that you may have to use two quote marks to designate the tag's parameter or concatenate a double-quote character as part of the string.</span></span> <span data-ttu-id="916e9-119">Il secondo è illustrato in questo Visual Basic esempio:</span><span class="sxs-lookup"><span data-stu-id="916e9-119">The latter is shown in this Visual Basic example:</span></span>


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



<span data-ttu-id="916e9-120">Per la programmazione in C, C++ e Java™, precede le barre rovesciate e le virgolette doppie con una barra rovesciata.</span><span class="sxs-lookup"><span data-stu-id="916e9-120">For C, C++, and Java™ programming, precede backslashes and double quotes with a backslash.</span></span> <span data-ttu-id="916e9-121">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="916e9-121">For example:</span></span>


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



<span data-ttu-id="916e9-122">Per le lingue straniere che supportano i caratteri DBCS (Double-byte character set), è possibile utilizzare caratteri a byte doppio per specificare i parametri di stringa.</span><span class="sxs-lookup"><span data-stu-id="916e9-122">For foreign languages that support double-byte character set (DBCS) characters, you can use double-byte characters to specify string parameters.</span></span> <span data-ttu-id="916e9-123">Usare tuttavia caratteri a byte singolo per tutti gli altri parametri e caratteri usati per definire il tag, incluso il tag stesso.</span><span class="sxs-lookup"><span data-stu-id="916e9-123">However, use single-byte characters for all other parameters and characters that are used to define the tag, including the tag itself.</span></span>

<span data-ttu-id="916e9-124">I seguenti tag sono supportati:</span><span class="sxs-lookup"><span data-stu-id="916e9-124">The following tags are supported:</span></span>

-   [<span data-ttu-id="916e9-125">**Chr**</span><span class="sxs-lookup"><span data-stu-id="916e9-125">**Chr**</span></span>](chr-tag.md)
-   [<span data-ttu-id="916e9-126">**CTX**</span><span class="sxs-lookup"><span data-stu-id="916e9-126">**Ctx**</span></span>](ctx-tag.md)
-   [<span data-ttu-id="916e9-127">**EMP**</span><span class="sxs-lookup"><span data-stu-id="916e9-127">**Emp**</span></span>](emp-tag.md)
-   [<span data-ttu-id="916e9-128">**LST**</span><span class="sxs-lookup"><span data-stu-id="916e9-128">**Lst**</span></span>](lst-tag.md)
-   [<span data-ttu-id="916e9-129">**Mappa**</span><span class="sxs-lookup"><span data-stu-id="916e9-129">**Map**</span></span>](map-tag.md)
-   [<span data-ttu-id="916e9-130">**MRK**</span><span class="sxs-lookup"><span data-stu-id="916e9-130">**Mrk**</span></span>](mrk-tag.md)
-   [<span data-ttu-id="916e9-131">**Pau**</span><span class="sxs-lookup"><span data-stu-id="916e9-131">**Pau**</span></span>](pau-tag.md)
-   [<span data-ttu-id="916e9-132">**Pit**</span><span class="sxs-lookup"><span data-stu-id="916e9-132">**Pit**</span></span>](pit-tag.md)
-   [<span data-ttu-id="916e9-133">**RST**</span><span class="sxs-lookup"><span data-stu-id="916e9-133">**Rst**</span></span>](rst-tag.md)
-   [<span data-ttu-id="916e9-134">**SPD**</span><span class="sxs-lookup"><span data-stu-id="916e9-134">**Spd**</span></span>](spd-tag.md)
-   [<span data-ttu-id="916e9-135">**Vol**</span><span class="sxs-lookup"><span data-stu-id="916e9-135">**Vol**</span></span>](vol-tag.md)

<span data-ttu-id="916e9-136">I tag sono progettati principalmente per la regolazione dell'output generato da sintesi vocale (TTS).</span><span class="sxs-lookup"><span data-stu-id="916e9-136">The tags are primarily designed for adjusting text-to-speech (TTS)-generated output.</span></span> <span data-ttu-id="916e9-137">Solo i tag [**MRK**](mrk-tag.md) e [**Map**](map-tag.md) possono essere usati con l'output parlato basato su file audio.</span><span class="sxs-lookup"><span data-stu-id="916e9-137">Only the [**Mrk**](mrk-tag.md) and [**Map**](map-tag.md) tags can be used with sound file-based spoken output.</span></span>

> [!Note]  
> <span data-ttu-id="916e9-138">Microsoft Agent non supporta tutti i tag documentati in Microsoft Speech SDK.</span><span class="sxs-lookup"><span data-stu-id="916e9-138">Microsoft Agent does not support all the tags documented in the Microsoft Speech SDK.</span></span> <span data-ttu-id="916e9-139">I parametri possono variare anche a seconda del motore TTS selezionato.</span><span class="sxs-lookup"><span data-stu-id="916e9-139">Parameters may also vary depending on the TTS engine selected.</span></span> <span data-ttu-id="916e9-140">È possibile impostare un motore TTS specifico usando [**TTSModeID**](ttsmodeid-property.md).</span><span class="sxs-lookup"><span data-stu-id="916e9-140">You can set a specific TTS engine using [**TTSModeID**](ttsmodeid-property.md).</span></span>

 

 

 




