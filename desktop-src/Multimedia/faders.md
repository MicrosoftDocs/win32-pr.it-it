---
title: Fader
description: Fader
ms.assetid: 2ca6be9f-9825-44d9-99c1-abcf6f0b42f7
keywords:
- mixer audio, controlli
- mixer audio, dissolvenze
- mixer, controlli
- mixer, dissolvenze
- Fader
- MIXERCONTROLDETAILS_UNSIGNED struttura
- controllo della dissolvenza del volume
- Controllo dissolvenza volume volume
- controllo dissolvenza volume acuto
- controllo equalizer grafico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a72b33387da77f7dfcd773abc874562d2f401b4865443a3cd6701a24ecd87e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526141"
---
# <a name="faders"></a>Fader

I controlli fader sono in genere controlli verticali che possono essere regolati verso l'alto o verso il basso. Questi controlli hanno una scala lineare e usano la [**struttura MIXERCONTROLDETAILS \_ UNSIGNED**](/previous-versions//dd757298(v=vs.85)) per recuperare e impostare i dettagli del controllo. La tabella seguente descrive i tipi di dissolvenza.



| Controllo   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fader     | Controllo generale della dissolvenza. L'intervallo di valori accettabili è compreso tra 0 e 65.535.                                                                                                                                                                                                                                                                                                                                       |
| Volume    | Controllo generale della dissolvenza del volume. L'intervallo di valori accettabili è compreso tra 0 e 65.535. Per informazioni sulla modifica di questo intervallo, vedere la documentazione per il dispositivo mixer.                                                                                                                                                                                                                                        |
| Basso      | Controllo della dissolvenza del volume del volume. L'intervallo di valori accettabili è compreso tra 0 e 65.535. I limiti della banda di frequenza di frequenza sono specifici dell'hardware. Per informazioni sui limiti di banda, vedere la documentazione per il dispositivo mixer.                                                                                                                                                                                      |
| Alti    | Controllo dissolvenza volume acuto. L'intervallo di valori accettabili è compreso tra 0 e 65.535. I limiti della banda di frequenza acuto sono specifici dell'hardware. Per informazioni sui limiti di banda, vedere la documentazione per il dispositivo mixer.                                                                                                                                                                              |
| Equalizer | Controllo equalizzatore grafico. L'intervallo di valori accettabili per una banda dell'equalizzatore è compreso tra 0 e 65.535. Il numero di bande di equalizer e i relativi limiti sono specifici dell'hardware. Per informazioni sull'equalizzatore, vedere la documentazione per il dispositivo mixer. È possibile usare la [**struttura MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) per recuperare le etichette di testo per l'equalizzatore. |



 

 

 