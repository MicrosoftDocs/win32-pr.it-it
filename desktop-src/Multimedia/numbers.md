---
title: Numeri (Windows Multimediali)
description: Numeri
ms.assetid: d416c4c2-a3e1-45a2-9ae1-82050a5e471b
keywords:
- mixer audio, controlli
- mixer audio, numeri
- mixer, controlli
- mixer, numeri
- controlli numerici
- MIXERCONTROLDETAILS_SIGNED struttura
- MIXERCONTROLDETAILS_UNSIGNED struttura
- controllo decibel
- controllo percentuale
- controllo firmato
- controllo senza segno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c9e1bacdea3f52129d78eea2f0bc7134df08b7077c83510bd8de824777e524
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806621"
---
# <a name="numbers-windows-multimedia"></a>Numeri (Windows Multimediali)

I controlli numerici consentono all'utente di immettere dati numerici associati a una riga. I dati numerici vengono espressi come interi con segno, interi senza segno o valori decibel integer. Questi controlli usano le strutture [**MIXERCONTROLDETAILS \_ SIGNED**](/previous-versions//dd757297(v=vs.85)) e [**MIXERCONTROLDETAILS \_ UNSIGNED**](/previous-versions//dd757298(v=vs.85)) per recuperare e impostare le proprietà del controllo. Nella tabella seguente vengono descritti i tipi di controlli numerici.



| Controllo  | Descrizione                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| Firmato   | Consente valori interi immessi nell'intervallo compreso tra - 231 e (231 –1).                                                               |
| Senza segno | Consente valori interi immessi nell'intervallo compreso tra 0 e (232 -1).                                                                   |
| Decibel  | Consente l'immissione di valori decibel interi, in decibel. L'intervallo di valori per questo controllo è compreso tra -32.768 e 32.767. |
| Percentuale  | Consente l'immissione di valori come percentuali.                                                                                         |



 

 

 
