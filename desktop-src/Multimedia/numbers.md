---
title: Numeri (Windows Multimedia)
description: Numeri
ms.assetid: d416c4c2-a3e1-45a2-9ae1-82050a5e471b
keywords:
- mixer audio, controlli
- mixer audio, numeri
- mixer, controlli
- mixer, numeri
- controlli numero
- Struttura MIXERCONTROLDETAILS_SIGNED
- Struttura MIXERCONTROLDETAILS_UNSIGNED
- controllo decibel
- Percentuale controllo
- controllo firmato
- controllo senza segno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02c4ffd40f1058fae51af3798135840394be918
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118778"
---
# <a name="numbers-windows-multimedia"></a>Numeri (Windows Multimedia)

I controlli numero consentono all'utente di immettere dati numerici associati a una riga. I dati numerici sono espressi come interi con segno, interi senza segno o valori di decibel interi. Questi controlli utilizzano le strutture [**MIXERCONTROLDETAILS \_ firmate**](/previous-versions//dd757297(v=vs.85)) e [**MIXERCONTROLDETAILS \_ senza segno**](/previous-versions//dd757298(v=vs.85)) per recuperare e impostare le proprietà del controllo. Nella tabella seguente vengono descritti i tipi di controlli numerici.



| Controllo  | Descrizione                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| Firmato   | Consente valori interi immessi nell'intervallo compreso tra-231 e (231-1).                                                               |
| Senza segno | Consente valori interi immessi nell'intervallo compreso tra 0 e (232-1).                                                                   |
| Decibel  | Consente l'immissione di valori integer in decibel, in decimi di decibel. L'intervallo di valori per questo controllo è compreso tra-32.768 e 32.767. |
| Percentuale  | Consente di immettere valori come percentuali.                                                                                         |



 

 

 
