---
title: Oggetto CommandsWindow
description: Oggetto CommandsWindow
ms.assetid: f7f37499-f16b-47fb-85d1-23a68171bf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574f803c12779f5ea9e690ca9c7a586d9d5df50e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299607"
---
# <a name="the-commandswindow-object"></a><span data-ttu-id="aa9db-103">Oggetto CommandsWindow</span><span class="sxs-lookup"><span data-stu-id="aa9db-103">The CommandsWindow Object</span></span>

<span data-ttu-id="aa9db-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aa9db-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="aa9db-105">L'oggetto [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) fornisce l'accesso alle proprietà della finestra dei comandi vocali.</span><span class="sxs-lookup"><span data-stu-id="aa9db-105">The [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) object provides access to properties of the Voice Commands Window.</span></span> <span data-ttu-id="aa9db-106">La finestra comandi vocali è una risorsa condivisa progettata principalmente per consentire agli utenti di visualizzare i comandi abilitati per la voce.</span><span class="sxs-lookup"><span data-stu-id="aa9db-106">The Voice Commands Window is a shared resource primarily designed to enable users to view voice-enabled commands.</span></span> <span data-ttu-id="aa9db-107">Se il riconoscimento vocale è disabilitato, la finestra dei comandi vocali viene ancora visualizzata, con il testo "input vocale disabilitato" (nella lingua del carattere).</span><span class="sxs-lookup"><span data-stu-id="aa9db-107">If speech recognition is disabled, the Voice Commands Window still displays, with the text "Speech input disabled" (in the language of the character).</span></span> <span data-ttu-id="aa9db-108">Se non è installato alcun motore vocale che corrisponda all'impostazione della lingua del carattere visualizzata dalla finestra, "input vocale non disponibile".</span><span class="sxs-lookup"><span data-stu-id="aa9db-108">If no speech engine is installed that matches the character's language setting the window displays, "Speech input not available."</span></span> <span data-ttu-id="aa9db-109">Se il client di input-attivo non ha definito parametri vocali per i comandi e ha disabilitato i comandi vocali globali, nella finestra viene visualizzato "nessun comando vocale".</span><span class="sxs-lookup"><span data-stu-id="aa9db-109">If the input-active client has not defined voice parameters for its commands and has disabled global voice commands, the window displays, "No voice commands."</span></span> <span data-ttu-id="aa9db-110">È anche possibile eseguire una query sulle proprietà della finestra dei comandi vocali indipendentemente dal fatto che l'input vocale sia disabilitato o che sia installato un motore di riconoscimento vocale compatibile.</span><span class="sxs-lookup"><span data-stu-id="aa9db-110">You can also query the properties of the Voice Commands Window regardless of whether speech input is disabled or a compatible speech engine is installed.</span></span>

-   [<span data-ttu-id="aa9db-111">Proprietà di CommandsWindow</span><span class="sxs-lookup"><span data-stu-id="aa9db-111">CommandsWindow Properties</span></span>](commandswindow-properties.md)

 

 