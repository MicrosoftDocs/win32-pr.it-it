---
title: Tag di output vocale di Microsoft Agent
description: Tag di output vocale di Microsoft Agent
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e712285b8160cf12817890ac42c4d49e95d72a2b
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386800"
---
# <a name="microsoft-agent-speech-output-tags"></a><span data-ttu-id="44f2d-103">Tag di output vocale di Microsoft Agent</span><span class="sxs-lookup"><span data-stu-id="44f2d-103">Microsoft Agent Speech Output Tags</span></span>

<span data-ttu-id="44f2d-104">\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="44f2d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="44f2d-105">I servizi Microsoft Agent supportano la modifica dell'output vocale tramite tag speciali inseriti nella stringa di testo vocale.</span><span class="sxs-lookup"><span data-stu-id="44f2d-105">The Microsoft Agent services support modifying speech output through special tags inserted in the speech text string.</span></span> <span data-ttu-id="44f2d-106">Questi tag consentono di modificare le caratteristiche dell'espressione di output del carattere.</span><span class="sxs-lookup"><span data-stu-id="44f2d-106">These tags help you change the characteristics of the output expression of the character.</span></span>

<span data-ttu-id="44f2d-107">I tag di output vocale usano le regole di sintassi seguenti:</span><span class="sxs-lookup"><span data-stu-id="44f2d-107">Speech output tags use the following rules of syntax:</span></span>

-   <span data-ttu-id="44f2d-108">Tutti i tag iniziano e terminano con una barra rovesciata ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="44f2d-108">All tags begin and end with a backslash character (\\).</span></span>
-   <span data-ttu-id="44f2d-109">Il carattere barra rovesciata singola non è abilitato all'interno di un tag.</span><span class="sxs-lookup"><span data-stu-id="44f2d-109">The single backslash character is not enabled within a tag.</span></span> <span data-ttu-id="44f2d-110">Per includere un carattere barra rovesciata in un parametro di testo di un tag, usare una doppia barra rovesciata ( \\ \\ ).</span><span class="sxs-lookup"><span data-stu-id="44f2d-110">To include a backslash character in a text parameter of a tag, use a double backslash (\\\\).</span></span>
-   <span data-ttu-id="44f2d-111">Per i tag non viene fatto distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="44f2d-111">Tags are case-insensitive.</span></span> <span data-ttu-id="44f2d-112">Ad esempio, \\ pit è uguale a PIT \\ \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="44f2d-112">For example, \\pit\\ is the same as \\PIT\\.</span></span>
-   <span data-ttu-id="44f2d-113">I tag dipendono da spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="44f2d-113">Tags are whitespace-dependent.</span></span> <span data-ttu-id="44f2d-114">Ad esempio, \\ Rst \\ non corrisponde a \\ Rst \\ .</span><span class="sxs-lookup"><span data-stu-id="44f2d-114">For example, \\Rst\\ is not the same as \\ Rst \\.</span></span>

<span data-ttu-id="44f2d-115">Se non diversamente specificato o modificato da un altro tag, l'output vocale mantiene la caratteristica impostata dal tag all'interno del testo specificato in un singolo [**metodo Speak.**](speak-method.md)</span><span class="sxs-lookup"><span data-stu-id="44f2d-115">Unless otherwise specified or modified by another tag, the speech output retains the characteristic set by the tag within the text specified in a single [**Speak**](speak-method.md) method.</span></span> <span data-ttu-id="44f2d-116">L'output vocale viene reimpostato automaticamente tramite i parametri definiti dall'utente dopo il **completamento di** un metodo Speak.</span><span class="sxs-lookup"><span data-stu-id="44f2d-116">Speech output is automatically reset through the user-defined parameters after a **Speak** method is completed.</span></span>

<span data-ttu-id="44f2d-117">Alcuni tag includono stringhe tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="44f2d-117">Some tags include quoted strings.</span></span> <span data-ttu-id="44f2d-118">Per alcuni linguaggi di programmazione, ad esempio Visual Basic Scripting Edition (VBScript) e Visual Basic, potrebbe essere necessario usare due virgolette per designare il parametro del tag o concatenare un carattere virgolette doppie come parte della stringa.</span><span class="sxs-lookup"><span data-stu-id="44f2d-118">For some programming languages, such as Visual Basic Scripting Edition (VBScript) and Visual Basic, this means that you may have to use two quote marks to designate the tag's parameter or concatenate a double-quote character as part of the string.</span></span> <span data-ttu-id="44f2d-119">Quest'ultimo è illustrato in questo Visual Basic esempio:</span><span class="sxs-lookup"><span data-stu-id="44f2d-119">The latter is shown in this Visual Basic example:</span></span>


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



<span data-ttu-id="44f2d-120">Per la programmazione C, C++ e Java™, far precedere le barre rovesciate e le virgolette doppie con una barra rovesciata.</span><span class="sxs-lookup"><span data-stu-id="44f2d-120">For C, C++, and Java™ programming, precede backslashes and double quotes with a backslash.</span></span> <span data-ttu-id="44f2d-121">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="44f2d-121">For example:</span></span>


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



<span data-ttu-id="44f2d-122">Per le lingue estere che supportano caratteri DBCS (Double Byte Character Set), è possibile usare caratteri a byte doppio per specificare i parametri di stringa.</span><span class="sxs-lookup"><span data-stu-id="44f2d-122">For foreign languages that support double-byte character set (DBCS) characters, you can use double-byte characters to specify string parameters.</span></span> <span data-ttu-id="44f2d-123">Tuttavia, usare caratteri a byte singolo per tutti gli altri parametri e caratteri usati per definire il tag, incluso il tag stesso.</span><span class="sxs-lookup"><span data-stu-id="44f2d-123">However, use single-byte characters for all other parameters and characters that are used to define the tag, including the tag itself.</span></span>

<span data-ttu-id="44f2d-124">I seguenti tag sono supportati:</span><span class="sxs-lookup"><span data-stu-id="44f2d-124">The following tags are supported:</span></span>

-   [<span data-ttu-id="44f2d-125">**Chr**</span><span class="sxs-lookup"><span data-stu-id="44f2d-125">**Chr**</span></span>](chr-tag.md)
-   [<span data-ttu-id="44f2d-126">**Ctx**</span><span class="sxs-lookup"><span data-stu-id="44f2d-126">**Ctx**</span></span>](ctx-tag.md)
-   [<span data-ttu-id="44f2d-127">**Emp**</span><span class="sxs-lookup"><span data-stu-id="44f2d-127">**Emp**</span></span>](emp-tag.md)
-   [<span data-ttu-id="44f2d-128">**Lst**</span><span class="sxs-lookup"><span data-stu-id="44f2d-128">**Lst**</span></span>](lst-tag.md)
-   [<span data-ttu-id="44f2d-129">**Mappa**</span><span class="sxs-lookup"><span data-stu-id="44f2d-129">**Map**</span></span>](map-tag.md)
-   [<span data-ttu-id="44f2d-130">**Mrk**</span><span class="sxs-lookup"><span data-stu-id="44f2d-130">**Mrk**</span></span>](mrk-tag.md)
-   [<span data-ttu-id="44f2d-131">**Pau**</span><span class="sxs-lookup"><span data-stu-id="44f2d-131">**Pau**</span></span>](pau-tag.md)
-   [<span data-ttu-id="44f2d-132">**fossa**</span><span class="sxs-lookup"><span data-stu-id="44f2d-132">**Pit**</span></span>](pit-tag.md)
-   [<span data-ttu-id="44f2d-133">**Rst**</span><span class="sxs-lookup"><span data-stu-id="44f2d-133">**Rst**</span></span>](rst-tag.md)
-   [<span data-ttu-id="44f2d-134">**Spd**</span><span class="sxs-lookup"><span data-stu-id="44f2d-134">**Spd**</span></span>](spd-tag.md)
-   [<span data-ttu-id="44f2d-135">**Vol**</span><span class="sxs-lookup"><span data-stu-id="44f2d-135">**Vol**</span></span>](vol-tag.md)

<span data-ttu-id="44f2d-136">I tag sono progettati principalmente per la regolazione dell'output generato dalla sintesi vocale.</span><span class="sxs-lookup"><span data-stu-id="44f2d-136">The tags are primarily designed for adjusting text-to-speech (TTS)-generated output.</span></span> <span data-ttu-id="44f2d-137">Solo i [**tag Mrk**](mrk-tag.md) [**e Map**](map-tag.md) possono essere usati con l'output parlato basato su file audio.</span><span class="sxs-lookup"><span data-stu-id="44f2d-137">Only the [**Mrk**](mrk-tag.md) and [**Map**](map-tag.md) tags can be used with sound file-based spoken output.</span></span>

> [!Note]  
> <span data-ttu-id="44f2d-138">Microsoft Agent non supporta tutti i tag documentati in Microsoft Speech SDK.</span><span class="sxs-lookup"><span data-stu-id="44f2d-138">Microsoft Agent does not support all the tags documented in the Microsoft Speech SDK.</span></span> <span data-ttu-id="44f2d-139">I parametri possono anche variare a seconda del motore TTS selezionato.</span><span class="sxs-lookup"><span data-stu-id="44f2d-139">Parameters may also vary depending on the TTS engine selected.</span></span> <span data-ttu-id="44f2d-140">È possibile impostare un motore TTS specifico usando [**TTSModeID**](ttsmodeid-property.md).</span><span class="sxs-lookup"><span data-stu-id="44f2d-140">You can set a specific TTS engine using [**TTSModeID**](ttsmodeid-property.md).</span></span>

 

 

 




