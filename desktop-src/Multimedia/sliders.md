---
title: Dispositivi di scorrimento (Windows Multimedia)
description: Dispositivi di scorrimento
ms.assetid: cfd82672-5b22-4b59-82b5-15ca68a451fc
keywords:
- mixer audio, controlli
- mixer audio, dispositivi di scorrimento
- mixer, controlli
- mixer, dispositivi di scorrimento
- scorrimento (controlli)
- Struttura MIXERCONTROLDETAILS_SIGNED
- controllo Pan
- Controllo Pan QSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d7644255e2fa9ee6384cbb5102df81c2a1eb0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400110"
---
# <a name="sliders-windows-multimedia"></a>Dispositivi di scorrimento (Windows Multimedia)

I controlli dispositivo di scorrimento sono in genere controlli orizzontali che possono essere modificati a sinistra o a destra. Questi controlli utilizzano la struttura con [**\_ firma MIXERCONTROLDETAILS**](/previous-versions//dd757297(v=vs.85)) per recuperare e impostare le proprietà del controllo. Nella tabella seguente vengono descritti i tipi di dispositivi di scorrimento.



| Controllo    | Descrizione                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| Slider     | Ha un intervallo compreso tra-32.768 e 32.767. Il driver del mixer definisce i limiti di questo controllo.                               |
| Dettaglio        | Ha un intervallo compreso tra-32.768 e 32.767. Il driver del mixer definisce i limiti di questo controllo, con 0 come valore medio. |
| Panoramica di QSound | Fornisce il controllo audio espanso tramite QSound. Questo controllo ha un intervallo compreso tra-15 e 15.                               |



 

 

 
