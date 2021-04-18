---
title: Normalizzazione del testo nei motori di sintesi vocale
description: Normalizzazione del testo nei motori di sintesi vocale
ms.assetid: 1974d47b-4877-47e3-89d8-fd70967e7605
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7bda7cb8041e31ef8e741df4d3f5d807610f1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298217"
---
# <a name="text-to-speech-engines-text-normalization"></a><span data-ttu-id="3cd26-103">Normalizzazione del testo nei motori di sintesi vocale</span><span class="sxs-lookup"><span data-stu-id="3cd26-103">Text-to-Speech Engines Text Normalization</span></span>

<span data-ttu-id="3cd26-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3cd26-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="3cd26-105">La normalizzazione è il processo di identificazione di numeri, abbreviazioni, acronimi e idiomatics e di trasformarli in testo completo, in base alle esigenze, in genere in base al contesto della frase.</span><span class="sxs-lookup"><span data-stu-id="3cd26-105">Normalization is the process of identifying numbers, abbreviations, acronyms and idiomatics and transforming them into full text as needed, usually based on the context of the sentence.</span></span>

<span data-ttu-id="3cd26-106">Ad esempio, usando il motore di sintesi vocale L&H TruVoice American English, la frase:</span><span class="sxs-lookup"><span data-stu-id="3cd26-106">For example, using the L&H TruVoice American English TTS Engine, the sentence:</span></span>

<span data-ttu-id="3cd26-107">Il re Giorgio VI d'Inghilterra è morto il 6 febbraio 1952.</span><span class="sxs-lookup"><span data-stu-id="3cd26-107">King George VI of England died on Feb 6, 1952.</span></span>

<span data-ttu-id="3cd26-108">verrà letto nel **contesto normale** come:</span><span class="sxs-lookup"><span data-stu-id="3cd26-108">will be read under **normal context** as:</span></span>

   <span data-ttu-id="3cd26-109">King Giorgio V I di England, è morto il 6 febbraio 19 52.</span><span class="sxs-lookup"><span data-stu-id="3cd26-109">King George V I of England, died on February six, nineteen fifty-two.</span></span>

<span data-ttu-id="3cd26-110">Tuttavia, nel **contesto del messaggio di posta elettronica** verrà letto come:</span><span class="sxs-lookup"><span data-stu-id="3cd26-110">But under **E-mail context**, it will be read as:</span></span>

   <span data-ttu-id="3cd26-111">Re Giorgio il sesto d'Inghilterra, morto il sesto febbraio 19 52.</span><span class="sxs-lookup"><span data-stu-id="3cd26-111">King George the sixth of England, died on February sixth, nineteen fifty-two.</span></span>

<span data-ttu-id="3cd26-112">Per informazioni sull'uso del tag di riconoscimento vocale del **contesto** , vedere la documentazione di programmazione dell'agente tag di output per la [sintesi vocale di Microsoft Agent](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="3cd26-112">Information about using the **Context** speech tag can be found in the Agent programming documentation [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

 

 




