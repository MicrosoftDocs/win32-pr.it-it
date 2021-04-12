---
title: Supporto per fumetti di Word
description: Supporto per fumetti di Word
ms.assetid: deac032f-0480-4a0d-bc69-e26f12666bbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78316c509ece6fc8f9b0cefd50b1564a50697a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221193"
---
# <a name="word-balloon-support"></a><span data-ttu-id="611e9-103">Supporto per fumetti di Word</span><span class="sxs-lookup"><span data-stu-id="611e9-103">Word Balloon Support</span></span>

<span data-ttu-id="611e9-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="611e9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="611e9-105">L'output parlato può anche apparire come output testuale sotto forma di fumetto di parole.</span><span class="sxs-lookup"><span data-stu-id="611e9-105">Spoken output can also appear as textual output in the form of a cartoon word balloon.</span></span> <span data-ttu-id="611e9-106">Questo può essere usato per integrare l'output parlato di un carattere o come alternativa all'output audio quando si usa il metodo [**Speak**](speak-method.md) .</span><span class="sxs-lookup"><span data-stu-id="611e9-106">This can be used to supplement the spoken output of a character or as an alternative to audio output when you use the [**Speak**](speak-method.md) method.</span></span>

![Sì fumetto Word Master](images/f3ballon.gif)

<span data-ttu-id="611e9-108">È anche possibile usare un fumetto di Word per comunicare il tipo di carattere "Thinking" usando il metodo [**think**](think-method.md) .</span><span class="sxs-lookup"><span data-stu-id="611e9-108">You can also use a word balloon to communicate what a character is "thinking" using the [**Think**](think-method.md) method.</span></span> <span data-ttu-id="611e9-109">Viene visualizzato il testo fornito in un fumetto ancora "pensato".</span><span class="sxs-lookup"><span data-stu-id="611e9-109">This displays the text you supply in a still "thought" balloon.</span></span> <span data-ttu-id="611e9-110">Il metodo **think** differisce anche dal metodo [**Speak**](speak-method.md) in quanto non produce alcun output audio.</span><span class="sxs-lookup"><span data-stu-id="611e9-110">The **Think** method also differs from the [**Speak**](speak-method.md) method in that it produces no audio output.</span></span>

<span data-ttu-id="611e9-111">I fumetti di Word supportano solo la comunicazione con didascalia dal carattere, non l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="611e9-111">Word balloons support only captioned communication from the character, not user input.</span></span> <span data-ttu-id="611e9-112">Pertanto, la parola Balloon non supporta i controlli di input.</span><span class="sxs-lookup"><span data-stu-id="611e9-112">Therefore, the word balloon does not support input controls.</span></span> <span data-ttu-id="611e9-113">Tuttavia, è possibile fornire facilmente l'input dell'utente per un carattere, usando le interfacce del linguaggio di programmazione o gli altri servizi di input forniti da Microsoft Agent, ad esempio il menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="611e9-113">However, you can easily provide user input for a character, using interfaces from your programming language or the other input services provided by Microsoft Agent, such as the pop-up menu.</span></span>

<span data-ttu-id="611e9-114">Quando si definisce un carattere, è possibile specificare se includere il supporto per i fumetti di Word.</span><span class="sxs-lookup"><span data-stu-id="611e9-114">When you define a character, you can specify whether to include word balloon support.</span></span> <span data-ttu-id="611e9-115">Tuttavia, se si usa un carattere che include il supporto di Word Balloon, non è possibile disabilitare il supporto.</span><span class="sxs-lookup"><span data-stu-id="611e9-115">However, if you use a character that includes word balloon support, you cannot disable the support.</span></span>

 

 




