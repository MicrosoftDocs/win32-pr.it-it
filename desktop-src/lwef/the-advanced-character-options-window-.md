---
title: Finestra Opzioni carattere avanzato (finestra comandi vocali)
description: Finestra Opzioni carattere avanzato
ms.assetid: c2f784e9-d1c5-4fa3-b3f7-5061c9b7e6d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f481871d3861da99b54829e5c6e1b34c9137060a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104339972"
---
# <a name="advanced-character-options-window-voice-commands-window"></a><span data-ttu-id="af180-103">Finestra Opzioni carattere avanzato (finestra comandi vocali)</span><span class="sxs-lookup"><span data-stu-id="af180-103">Advanced Character Options Window (Voice Commands Window)</span></span>

<span data-ttu-id="af180-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="af180-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="af180-105">Nella finestra Opzioni carattere avanzate sono disponibili opzioni che consentono agli utenti di modificare l'interazione con tutti i caratteri.</span><span class="sxs-lookup"><span data-stu-id="af180-105">The Advanced Character Options window provides options for users to adjust their interaction with all characters.</span></span> <span data-ttu-id="af180-106">Ad esempio, gli utenti possono disabilitare l'input vocale o modificare i parametri di input.</span><span class="sxs-lookup"><span data-stu-id="af180-106">For example, users can disable speech input or change input parameters.</span></span> <span data-ttu-id="af180-107">Gli utenti possono anche modificare le impostazioni di output per la parola fumetto.</span><span class="sxs-lookup"><span data-stu-id="af180-107">Users can also change the output settings for the word balloon.</span></span> <span data-ttu-id="af180-108">Queste impostazioni eseguono l'override di tutti i set da un'applicazione client o impostati come parte della definizione del carattere.</span><span class="sxs-lookup"><span data-stu-id="af180-108">These settings override any set by a client application or set as part of the character definition.</span></span> <span data-ttu-id="af180-109">L'applicazione non può modificare o disabilitare queste opzioni perché si applicano alle preferenze utente generali per il funzionamento di tutti i caratteri.</span><span class="sxs-lookup"><span data-stu-id="af180-109">Your application cannot change or disable these options, because they apply to the general user preferences for operation of all characters.</span></span> <span data-ttu-id="af180-110">Tuttavia, il server invierà una notifica all'applicazione ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) quando l'utente cambia e applica un'opzione.</span><span class="sxs-lookup"><span data-stu-id="af180-110">However, the server will notify your application ([**DefaultCharacterChange**](defaultcharacterchange-event.md)) when the user changes and applies an option.</span></span> <span data-ttu-id="af180-111">È anche possibile visualizzare o chiudere la finestra usando la proprietà [**Visible**](visible-property.md) della finestra e accedere alla relativa posizione tramite le proprietà [**Top**](top-property.md) e [**Left**](left-property.md) .</span><span class="sxs-lookup"><span data-stu-id="af180-111">You can also display or close the window using the window's [**Visible**](visible-property.md) property and access its location through its [**Top**](top-property.md) and [**Left**](left-property.md) properties.</span></span>

<span data-ttu-id="af180-112">Oltre a supportare l'animazione di un carattere, Microsoft Agent supporta l'output audio per il carattere.</span><span class="sxs-lookup"><span data-stu-id="af180-112">In addition to supporting the animation of a character, Microsoft Agent supports audio output for the character.</span></span> <span data-ttu-id="af180-113">Sono inclusi l'output parlato e gli effetti audio.</span><span class="sxs-lookup"><span data-stu-id="af180-113">This includes spoken output and sound effects.</span></span> <span data-ttu-id="af180-114">Per l'output parlato, il server sincronizza automaticamente le immagini mouth definite del carattere nell'output.</span><span class="sxs-lookup"><span data-stu-id="af180-114">For spoken output, the server automatically lip-syncs the character's defined mouth images to the output.</span></span> <span data-ttu-id="af180-115">È possibile scegliere Sintesi vocale (TTS), audio registrato o solo output di testo a fumetti.</span><span class="sxs-lookup"><span data-stu-id="af180-115">You can choose text-to-speech (TTS) synthesis, recorded audio, or only word balloon text output.</span></span>

 

 




