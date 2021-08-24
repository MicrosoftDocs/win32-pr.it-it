---
title: Supporto dei driver per i comandi MCI
description: Supporto dei driver per i comandi MCI
ms.assetid: 1adea076-c04e-4613-a793-60de41b2e9db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2aa2bb806e869adcf4355b8b43ac529240a5c35dfc8ce49d43672baf0bd976
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526291"
---
# <a name="driver-support-for-mci-commands"></a>Supporto dei driver per i comandi MCI

I driver MCI forniscono la funzionalità per i comandi MCI. Il software di sistema esegue alcune attività di gestione dei dati di base, ma tutta la riproduzione multimediale, la presentazione e la registrazione vengono gestite dai singoli driver MCI.

I driver variano nel supporto per i comandi MCI e i flag di comando. Poiché i dispositivi multimediali possono avere funzionalità molto diverse, MCI è progettato per consentire ai singoli driver di estendere o ridurre i set di comandi in modo che corrispondano alle funzionalità del dispositivo. Ad esempio, il [**comando record**](record.md) ([**MCI \_ RECORD**](mci-record.md)) fa parte del set di comandi per i sequencer MIDI, ma il driver MCISEQ incluso in Windows non supporta questo comando. L'argomento di riferimento per il comando record spiega che i dispositivi del tipo di dispositivo **sequencer** riconoscono il comando. questo non significa che tutti i dispositivi di questo tipo supportino il comando . Le applicazioni devono usare [**la funzionalità**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) per determinare le funzionalità di un determinato dispositivo.

 

 




