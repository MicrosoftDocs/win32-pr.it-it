---
description: I messaggi del dispositivo sono messaggi di sistema che notificano le applicazioni e altre funzionalità degli eventi di modifica del dispositivo.
ms.assetid: 4d1ace87-2d02-4ba4-9bcc-da86cf3481db
title: Messaggi del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22fe5b9f8b3f9fcc2a075767aa684bd92962f32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305084"
---
# <a name="device-messages"></a><span data-ttu-id="1c181-103">Messaggi del dispositivo</span><span class="sxs-lookup"><span data-stu-id="1c181-103">Device Messages</span></span>

<span data-ttu-id="1c181-104">I messaggi del dispositivo sono messaggi di sistema che notificano le applicazioni e altre funzionalità degli eventi di modifica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1c181-104">Device messages are system messages that notify applications and other features of device change events.</span></span> <span data-ttu-id="1c181-105">Questi eventi si verificano ogni volta che il sistema rileva una modifica all'hardware del sistema, ad esempio quando l'utente ancora e Disancora un computer portatile, oppure inserisce o rimuove un dispositivo, ad esempio una scheda PCMCIA.</span><span class="sxs-lookup"><span data-stu-id="1c181-105">These events occur whenever the system detects a change to the system hardware, such as when the user docks and undocks a laptop computer, or inserts or removes a device such as a PCMCIA card.</span></span> <span data-ttu-id="1c181-106">Gli eventi del dispositivo possono verificarsi mentre il sistema è in esecuzione o quando il sistema riprende l'operazione dopo la sospensione temporanea.</span><span class="sxs-lookup"><span data-stu-id="1c181-106">Device events can occur while the system is running or when the system resumes operation after temporarily being suspended.</span></span>

<span data-ttu-id="1c181-107">Per garantire che le applicazioni non perdano i dati quando i dispositivi non sono più disponibili, il sistema monitora la configurazione hardware e invia messaggi al dispositivo alle applicazioni per notificare le modifiche e fornire loro la possibilità di preparare le modifiche prima che si verifichino.</span><span class="sxs-lookup"><span data-stu-id="1c181-107">To help ensure that applications do not lose data when devices become unavailable, the system monitors the hardware configuration and sends device messages to the applications to notify them of the changes and to give them the opportunity to prepare for the changes before they occur.</span></span>

<span data-ttu-id="1c181-108">Per ogni evento del dispositivo, il sistema trasmette un messaggio [**WM \_ DEVICECHANGE**](wm-devicechange.md) a tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1c181-108">For each device event, the system broadcasts a [**WM\_DEVICECHANGE**](wm-devicechange.md) message to all applications.</span></span> <span data-ttu-id="1c181-109">In questo messaggio, il parametro *wParam* identifica il [tipo di evento del dispositivo](device-event-types.md) e il parametro *lParam* è un puntatore a dati specifici dell'evento.</span><span class="sxs-lookup"><span data-stu-id="1c181-109">In this message, the *wParam* parameter identifies the [device event type](device-event-types.md) and the *lParam* parameter is a pointer to event-specific data.</span></span>

 

 



