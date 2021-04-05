---
title: Selezione del motore vocale
description: Selezione del motore vocale
ms.assetid: f5afedc6-093f-4247-a5c8-277d6b2d646c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a548f0201ba37c8acb867091cc690a913277ff06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855978"
---
# <a name="speech-engine-selection"></a><span data-ttu-id="3838b-103">Selezione del motore vocale</span><span class="sxs-lookup"><span data-stu-id="3838b-103">Speech Engine Selection</span></span>

<span data-ttu-id="3838b-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3838b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="3838b-105">L'impostazione dell'ID lingua di un carattere determina la lingua di input vocale predefinita; Microsoft Agent richiede SAPI per un motore installato che corrisponda a tale lingua.</span><span class="sxs-lookup"><span data-stu-id="3838b-105">A character's language ID setting determines its default speech input language; Microsoft Agent requests SAPI for an installed engine that matches that language.</span></span> <span data-ttu-id="3838b-106">Se un'applicazione client non specifica una preferenza per la lingua, Microsoft Agent tenterà di trovare un motore di riconoscimento vocale corrispondente all'ID lingua predefinito dell'utente (usando l'ID lingua principale, quindi l'ID della lingua secondaria).</span><span class="sxs-lookup"><span data-stu-id="3838b-106">If a client application does not specify a language preference, Microsoft Agent will attempt to find a speech recognition engine that matches the user default language ID (using the major language ID, then the minor language ID).</span></span> <span data-ttu-id="3838b-107">Se non è disponibile alcun motore corrispondente a questa lingua, il riconoscimento vocale viene disabilitato per tale carattere.</span><span class="sxs-lookup"><span data-stu-id="3838b-107">If no engine is available matching this language, speech is disabled for that character.</span></span>

<span data-ttu-id="3838b-108">È anche possibile richiedere un motore di riconoscimento vocale specifico specificando l'ID modalità (usando la proprietà Character [**SRModeID**](srmodeid-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="3838b-108">You can also request a specific speech recognition engine by specifying its mode ID (using the character [**SRModeID**](srmodeid-property.md) property).</span></span> <span data-ttu-id="3838b-109">Tuttavia, se l'ID lingua per l'ID modalità non corrisponde all'impostazione della lingua del client, la chiamata avrà esito negativo (genera un errore nel controllo).</span><span class="sxs-lookup"><span data-stu-id="3838b-109">However, if the language ID for that mode ID does not match the client's language setting, the call will fail (raise an error in the control).</span></span> <span data-ttu-id="3838b-110">Il motore di riconoscimento vocale rimarrà quindi l'ultimo motore impostato correttamente dal client o, se non lo è, il motore che corrisponde all'ID lingua del sistema corrente.</span><span class="sxs-lookup"><span data-stu-id="3838b-110">The speech recognition engine will then remain the last successfully set engine by the client, or if none, the engine that matches the current system language ID.</span></span> <span data-ttu-id="3838b-111">Se non è ancora presente alcuna corrispondenza, l'input vocale non è disponibile per quel client.</span><span class="sxs-lookup"><span data-stu-id="3838b-111">If there is still no match, speech input is not available for that client.</span></span>

<span data-ttu-id="3838b-112">Microsoft Agent carica automaticamente un motore di riconoscimento vocale quando l'input vocale viene avviato da un utente che preme la scelta rapida in ascolto o il client di input-attivo chiama il metodo [**Listen**](listen-method.md) .</span><span class="sxs-lookup"><span data-stu-id="3838b-112">Microsoft Agent automatically loads a speech recognition engine when speech input is initiated by a user pressing the Listening hotkey or the input-active client calls the [**Listen**](listen-method.md) method.</span></span> <span data-ttu-id="3838b-113">Tuttavia, è possibile caricare un motore anche quando si imposta o si esegue una query sull'ID modalità, si imposta o si esegue una query sulle proprietà della finestra dei comandi vocali, si esegue una query su [**SRStatus**](srstatus-property.md)o quando la voce vocale è abilitata e l'utente Visualizza la pagina di input vocale delle opzioni per caratteri avanzati.</span><span class="sxs-lookup"><span data-stu-id="3838b-113">However, an engine may also be loaded when setting or querying its mode ID, setting or querying the properties of the Voice Commands Window, querying [**SRStatus**](srstatus-property.md), or when speech is enabled and the user displays the Speech Input page of the Advanced Character Options.</span></span> <span data-ttu-id="3838b-114">Tuttavia, Microsoft Agent mantiene solo i motori di riconoscimento vocale utilizzati dai client.</span><span class="sxs-lookup"><span data-stu-id="3838b-114">However, Microsoft Agent only keeps loaded the speech engines that clients are using.</span></span>

 

 




