---
title: Metri
description: Metri
ms.assetid: 11a98d2a-7cdd-4249-bba9-7edc51d7f8b0
keywords:
- mixer audio, controlli
- mixer audio, contatori
- mixer, controlli
- mixer, contatori
- controlli contatore
- Struttura MIXERCONTROLDETAILS_BOOLEAN
- Struttura MIXERCONTROLDETAILS_SIGNED
- Struttura MIXERCONTROLDETAILS_UNSIGNED
- Controllo booleano
- picco di controllo
- controllo firmato
- controllo senza segno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36f1bebfca22b963e5c1eb6fede3f2786b35199
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473115"
---
# <a name="meters"></a>Metri

Il contatore controlla i dati delle misure che passano attraverso una linea audio. Questi controlli utilizzano le strutture [**MIXERCONTROLDETAILS \_ Boolean**](/previous-versions//dd757295(v=vs.85)), [**MIXERCONTROLDETAILS \_ signed**](/previous-versions//dd757297(v=vs.85))e [**MIXERCONTROLDETAILS \_ senza segno**](/previous-versions//dd757298(v=vs.85)) per recuperare e impostare le proprietà del controllo. Nella tabella seguente vengono descritti i tipi di contatori.



| Controllo  | Descrizione                                                                                                                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boolean  | Misura se un valore intero è FALSE/OFF (zero) o TRUE/ON (diverso da zero).                                                                            |
| Peak     | Misura la deflessione da 0 in entrambe le direzioni positivo e negativo. L'intervallo di valori integer per il contatore massimo è da-32.768 a 32.767. |
| Firmato   | Misura i valori interi nell'intervallo compreso tra-231 e (231-1). Il driver del mixer definisce i limiti di questo contatore.                                     |
| Senza segno | Misura i valori interi nell'intervallo compreso tra 0 e (232-1). Il driver del mixer definisce i limiti di questo contatore.                                        |



 

 

 