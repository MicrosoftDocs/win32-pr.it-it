---
title: Supporto dei driver per i comandi MCI
description: Supporto dei driver per i comandi MCI
ms.assetid: 1adea076-c04e-4613-a793-60de41b2e9db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b57e28feaa3fd1e0b4d7f3edc7c95df3f00e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709586"
---
# <a name="driver-support-for-mci-commands"></a><span data-ttu-id="948fa-103">Supporto dei driver per i comandi MCI</span><span class="sxs-lookup"><span data-stu-id="948fa-103">Driver Support for MCI Commands</span></span>

<span data-ttu-id="948fa-104">I driver MCI forniscono la funzionalità per i comandi MCI.</span><span class="sxs-lookup"><span data-stu-id="948fa-104">MCI drivers provide the functionality for MCI commands.</span></span> <span data-ttu-id="948fa-105">Il software di sistema esegue alcune attività di gestione dei dati di base, ma tutte le funzionalità di riproduzione, presentazione e registrazione multimediali vengono gestite dai singoli driver MCI.</span><span class="sxs-lookup"><span data-stu-id="948fa-105">The system software performs some basic data-management tasks, but all the multimedia playback, presentation, and recording is handled by the individual MCI drivers.</span></span>

<span data-ttu-id="948fa-106">I driver variano in base al supporto per i comandi MCI e i flag di comando.</span><span class="sxs-lookup"><span data-stu-id="948fa-106">Drivers vary in their support for MCI commands and command flags.</span></span> <span data-ttu-id="948fa-107">Poiché i dispositivi multimediali possono avere funzionalità molto diverse, MCI è progettato per consentire ai singoli driver di estendere o ridurre i set di comandi in modo che corrispondano alle funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="948fa-107">Because multimedia devices can have widely different capabilities, MCI is designed to let individual drivers extend or reduce the command sets to match the capabilities of the device.</span></span> <span data-ttu-id="948fa-108">Ad esempio, il comando [**record**](record.md) ([**\_ record MCI**](mci-record.md)) fa parte del set di comandi per i sequencer MIDI, ma il driver mciseq incluso in Windows non supporta questo comando.</span><span class="sxs-lookup"><span data-stu-id="948fa-108">For example, the [**record**](record.md) ([**MCI\_RECORD**](mci-record.md)) command is part of the command set for MIDI sequencers, but the MCISEQ driver included with Windows does not support this command.</span></span> <span data-ttu-id="948fa-109">L'argomento di riferimento per il comando record spiega che i dispositivi del tipo di dispositivo **sequencer** riconoscono il comando. Ciò non significa che tutti i dispositivi di questo tipo supportano il comando.</span><span class="sxs-lookup"><span data-stu-id="948fa-109">The reference topic for the record command explains that devices of the **sequencer** device type recognize the command; this does not mean that all devices of this type support the command.</span></span> <span data-ttu-id="948fa-110">Le applicazioni devono usare il comando [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) per determinare le funzionalità di un determinato dispositivo.</span><span class="sxs-lookup"><span data-stu-id="948fa-110">Applications should use the [**capability**](capability.md) ([**MCI\_GETDEVCAPS**](mci-getdevcaps.md)) command to determine the capabilities of a particular device.</span></span>

 

 




