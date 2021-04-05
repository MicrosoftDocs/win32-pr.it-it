---
title: Arresto, sospensione e ripresa di un dispositivo
description: Arresto, sospensione e ripresa di un dispositivo
ms.assetid: df9ca4ab-4711-44dd-a058-909f291a1652
keywords:
- Comando MCI_STOP
- Comando MCI_PAUSE
- Comando MCI_RESUME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddcd9618608226dec108d62754964fe6401d429
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710702"
---
# <a name="stopping-pausing-and-resuming-a-device"></a><span data-ttu-id="290d8-106">Arresto, sospensione e ripresa di un dispositivo</span><span class="sxs-lookup"><span data-stu-id="290d8-106">Stopping, Pausing, and Resuming a Device</span></span>

<span data-ttu-id="290d8-107">Il comando [**Stop**](stop.md) ([**MCI \_ Stop**](mci-stop.md)) sospende la riproduzione o la registrazione di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="290d8-107">The [**stop**](stop.md) ([**MCI\_STOP**](mci-stop.md)) command suspends the playing or recording of a device.</span></span> <span data-ttu-id="290d8-108">Molti dispositivi supportano anche il comando [**Sospendi**](pause.md) ([**\_ pausa MCI**](mci-pause.md)).</span><span class="sxs-lookup"><span data-stu-id="290d8-108">Many devices also support the [**pause**](pause.md) ([**MCI\_PAUSE**](mci-pause.md)) command.</span></span> <span data-ttu-id="290d8-109">La differenza tra l' **arresto** e la **pausa** dipende dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="290d8-109">The difference between **stop** and **pause** depends on the device.</span></span> <span data-ttu-id="290d8-110">In genere **Sospendi** sospende l'operazione ma lascia il dispositivo pronto per riprendere la riproduzione o la registrazione immediatamente.</span><span class="sxs-lookup"><span data-stu-id="290d8-110">Usually **pause** suspends operation but leaves the device ready to resume playing or recording immediately.</span></span>

<span data-ttu-id="290d8-111">L'uso del comando [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)) o [**record**](record.md) ([**\_ record MCI**](mci-record.md)) per riavviare un dispositivo Reimposta i percorsi specificati con i flag "to" (MCI \_ to) e "from" (MCI \_ from) prima che il dispositivo sia stato sospeso o arrestato.</span><span class="sxs-lookup"><span data-stu-id="290d8-111">Using the [**play**](play.md) ([**MCI\_PLAY**](mci-play.md)) or [**record**](record.md) ([**MCI\_RECORD**](mci-record.md)) command to restart a device resets the locations specified with the "to" (MCI\_TO) and "from" (MCI\_FROM) flags before the device was paused or stopped.</span></span> <span data-ttu-id="290d8-112">Senza il flag "from", questi comandi reimpostano la posizione iniziale sulla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="290d8-112">Without the "from" flag, these commands reset the starting location to the current position.</span></span> <span data-ttu-id="290d8-113">Senza il flag "a", reimpostano la posizione finale alla fine del supporto.</span><span class="sxs-lookup"><span data-stu-id="290d8-113">Without the "to" flag, they reset the ending location to the end of the media.</span></span> <span data-ttu-id="290d8-114">Per continuare a eseguire la riproduzione o la registrazione senza reimpostare una posizione di arresto precedentemente specificata, usare il flag "to" del comando **Play** o **record** per specificare una posizione finale.</span><span class="sxs-lookup"><span data-stu-id="290d8-114">To continue playing or recording without resetting a previously specified stop position, use the **play** or **record** command's "to" flag to specify an ending position.</span></span>

<span data-ttu-id="290d8-115">Alcuni dispositivi supportano il comando [**Resume**](resume.md) ([**MCI \_ Resume**](mci-resume.md)) per riavviare un dispositivo sospeso.</span><span class="sxs-lookup"><span data-stu-id="290d8-115">Some devices support the [**resume**](resume.md) ([**MCI\_RESUME**](mci-resume.md)) command to restart a paused device.</span></span> <span data-ttu-id="290d8-116">Questo comando non modifica i percorsi "to" e "from" specificati con il comando **Play** o **record** che precedeva il comando [**pause**](pause.md) .</span><span class="sxs-lookup"><span data-stu-id="290d8-116">This command does not change the "to" and "from" locations specified with the **play** or **record** command that preceded the [**pause**](pause.md) command.</span></span>

 

 




