---
title: Fader
description: Fader
ms.assetid: 2ca6be9f-9825-44d9-99c1-abcf6f0b42f7
keywords:
- mixer audio, controlli
- mixer audio, cursori
- mixer, controlli
- mixer, fader
- fader
- Struttura MIXERCONTROLDETAILS_UNSIGNED
- controllo dissolvenza volume
- controllo Fade volume bass
- controllo Fade volume Treble
- controllo equalizzatore grafico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b560b61a694089b947b0cfda7a54b486f1e3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956393"
---
# <a name="faders"></a>Fader

I controlli fader sono in genere controlli verticali che possono essere regolati verso l'alto o verso il basso. Questi controlli hanno una scala lineare e usano la [**struttura \_ senza segno MIXERCONTROLDETAILS**](/previous-versions//dd757298(v=vs.85)) per recuperare e impostare i dettagli del controllo. Nella tabella seguente vengono descritti i tipi di fader.



| Controllo   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fader     | Controllo di dissolvenza generale. L'intervallo di valori accettabili è compreso tra 0 e 65.535.                                                                                                                                                                                                                                                                                                                                       |
| Volume    | Controllo di dissolvenza generale del volume. L'intervallo di valori accettabili è compreso tra 0 e 65.535. Per informazioni sulla modifica di questo intervallo, vedere la documentazione relativa al dispositivo mixer.                                                                                                                                                                                                                                        |
| Basso      | Controllo dissolvenza volume basso. L'intervallo di valori accettabili è compreso tra 0 e 65.535. I limiti della banda di frequenza bassi sono specifici dell'hardware. Per informazioni sui limiti delle bande, vedere la documentazione relativa al dispositivo mixer.                                                                                                                                                                                      |
| Acuti    | Controllo Fade volume Treble. L'intervallo di valori accettabili è compreso tra 0 e 65.535. I limiti della banda di frequenze acute sono specifici dell'hardware. Per informazioni sui limiti della banda, vedere la documentazione relativa al dispositivo mixer.                                                                                                                                                                              |
| Equalizer | Controllo equalizzatore grafico. L'intervallo di valori accettabili per una banda dell'equalizzatore è compreso tra 0 e 65.535. Il numero di bande di equalizzatore e i relativi limiti sono specifici dell'hardware. Per informazioni sull'equalizzatore, vedere la documentazione relativa al dispositivo mixer. È possibile usare la [**struttura \_ LISTTEXT di MIXERCONTROLDETAILS**](/previous-versions//dd757296(v=vs.85)) per recuperare le etichette di testo per l'equalizzatore. |



 

 

 