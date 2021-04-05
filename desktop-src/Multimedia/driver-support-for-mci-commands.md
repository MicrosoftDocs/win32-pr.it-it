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
# <a name="driver-support-for-mci-commands"></a>Supporto dei driver per i comandi MCI

I driver MCI forniscono la funzionalità per i comandi MCI. Il software di sistema esegue alcune attività di gestione dei dati di base, ma tutte le funzionalità di riproduzione, presentazione e registrazione multimediali vengono gestite dai singoli driver MCI.

I driver variano in base al supporto per i comandi MCI e i flag di comando. Poiché i dispositivi multimediali possono avere funzionalità molto diverse, MCI è progettato per consentire ai singoli driver di estendere o ridurre i set di comandi in modo che corrispondano alle funzionalità del dispositivo. Ad esempio, il comando [**record**](record.md) ([**\_ record MCI**](mci-record.md)) fa parte del set di comandi per i sequencer MIDI, ma il driver mciseq incluso in Windows non supporta questo comando. L'argomento di riferimento per il comando record spiega che i dispositivi del tipo di dispositivo **sequencer** riconoscono il comando. Ciò non significa che tutti i dispositivi di questo tipo supportano il comando. Le applicazioni devono usare il comando [**Capability**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) per determinare le funzionalità di un determinato dispositivo.

 

 




