---
title: Requisiti per i motori di riconoscimento vocale
description: Requisiti per i motori di riconoscimento vocale
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9214f13b11a071ec8d8599f0b6dd542884ae05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955721"
---
# <a name="requirements-for-speech-recognition-engines"></a><span data-ttu-id="adeb7-103">Requisiti per i motori di riconoscimento vocale</span><span class="sxs-lookup"><span data-stu-id="adeb7-103">Requirements for Speech Recognition Engines</span></span>

<span data-ttu-id="adeb7-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="adeb7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="adeb7-105">Un motore di riconoscimento vocale deve anche essere un motore di comando e controllo completamente compatibile (C&C) in base a SAPI 4,0.</span><span class="sxs-lookup"><span data-stu-id="adeb7-105">A speech recognition engine must also be a fully compliant Command and Control (C&C) engine according to SAPI 4.0.</span></span> <span data-ttu-id="adeb7-106">Deve supportare più grammatiche nel formato binario descritto nella specifica e consentire l'attivazione o la disattivazione di tali grammatiche in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="adeb7-106">It must support multiple grammars in the binary format described in the specification and allow those grammars to be activated or deactivated in real time.</span></span>

<span data-ttu-id="adeb7-107">Si noti che SAPI 4,0 richiede che i motori di riconoscimento vocale supportino le interfacce Unicode a caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="adeb7-107">Note that SAPI 4.0 requires that speech recognition engines support the wide character, Unicode interfaces.</span></span> <span data-ttu-id="adeb7-108">Tuttavia, nel supportare queste interfacce, il motore non deve dipendere dalla conversione dei dati Unicode in ANSI, perché il motore potrebbe non funzionare correttamente in alcuni sistemi.</span><span class="sxs-lookup"><span data-stu-id="adeb7-108">However, in supporting these interfaces, the engine should not depend on converting Unicode data to ANSI, as the engine may not function correctly on some systems.</span></span> <span data-ttu-id="adeb7-109">Ad esempio, un motore giapponese che converte Unicode in ANSI potrebbe non funzionare in un sistema Microsoft Windows 95 in lingua inglese.</span><span class="sxs-lookup"><span data-stu-id="adeb7-109">For example, a Japanese engine that converts Unicode to ANSI may not work on an English-language Microsoft Windows 95 system.</span></span>

<span data-ttu-id="adeb7-110">Inoltre, per essere considerato conforme a Microsoft Agent, il motore deve restituire oggetti results dopo il riconoscimento corretto di una frase (tramite ISRGramNotifySinkW::P hraseFinish).</span><span class="sxs-lookup"><span data-stu-id="adeb7-110">In addition, to be considered Microsoft Agent-compliant, the engine must return results objects upon the successful recognition of a phrase (through ISRGramNotifySinkW::PhraseFinish).</span></span> <span data-ttu-id="adeb7-111">Questi oggetti risultati devono supportare ISRResBasic, come richiesto dalla specifica.</span><span class="sxs-lookup"><span data-stu-id="adeb7-111">These results objects must support ISRResBasic, as the specification requires.</span></span> <span data-ttu-id="adeb7-112">Inoltre, devono supportare ISRResScore.</span><span class="sxs-lookup"><span data-stu-id="adeb7-112">In addition, they should support ISRResScore.</span></span> <span data-ttu-id="adeb7-113">Anche se Microsoft Agent verrà eseguito con un motore che supporta solo ISRResBasic o anche con un motore che non restituisce alcun oggetto di risultati, le prestazioni sono in genere significativamente più scarse con tali motori.</span><span class="sxs-lookup"><span data-stu-id="adeb7-113">Although Microsoft Agent will run with an engine that supports only ISRResBasic, or even with an engine that returns no results objects whatsoever, performance will usually be significantly poorer with such engines.</span></span> <span data-ttu-id="adeb7-114">Molte applicazioni usano i valori di confidenza forniti dal motore per controllare la modalità di risposta ai vari comandi.</span><span class="sxs-lookup"><span data-stu-id="adeb7-114">Many applications use the confidence values provided by the engine to control how they respond to various commands.</span></span>

 

 




