---
title: Dispositivi di scorrimento (Windows Multimediali)
description: Dispositivi di scorrimento
ms.assetid: cfd82672-5b22-4b59-82b5-15ca68a451fc
keywords:
- mixer audio, controlli
- mixer audio, dispositivi di scorrimento
- mixer, controlli
- mixer, dispositivi di scorrimento
- scorrimento (controlli)
- MIXERCONTROLDETAILS_SIGNED struttura
- Controllo panoramica
- Controllo panoramica QSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e902e3ead0416cb4b2a7d56d289f91779563109cb9494784635affc75069dfe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805351"
---
# <a name="sliders-windows-multimedia"></a>Dispositivi di scorrimento (Windows Multimediali)

I controlli dispositivo di scorrimento sono in genere controlli orizzontali che possono essere regolati a sinistra o a destra. Questi controlli usano la [**struttura MIXERCONTROLDETAILS \_ SIGNED**](/previous-versions//dd757297(v=vs.85)) per recuperare e impostare le proprietà del controllo. La tabella seguente descrive i tipi di dispositivi di scorrimento.



| Controllo    | Descrizione                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| Slider     | Ha un intervallo compreso tra -32.768 e 32.767. Il driver mixer definisce i limiti di questo controllo.                               |
| Dettaglio        | Ha un intervallo compreso tra -32.768 e 32.767. Il driver mixer definisce i limiti di questo controllo, con 0 come valore dell'intervallo intermedio. |
| Panoramica QSound | Offre un controllo audio esteso tramite QSound. Questo controllo ha un intervallo compreso tra -15 e 15.                               |



 

 

 
