---
title: Proprietà, metodi ed eventi
description: Proprietà, metodi ed eventi
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Media Player di Windows, proprietà del modello a oggetti
- Windows Media Player, metodi per il modello a oggetti
- Windows Media Player, eventi per il modello a oggetti
- Windows Media Player modello a oggetti, proprietà
- Modello a oggetti di Windows Media Player, metodi
- Modello a oggetti di Windows Media Player, eventi
- modello a oggetti, proprietà
- modello a oggetti, metodi
- modello a oggetti, eventi
- Controllo ActiveX di Windows Media Player, proprietà per il modello a oggetti
- Controllo ActiveX, proprietà per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, proprietà per il modello a oggetti
- Windows Media Player Mobile, proprietà del modello a oggetti
- Controllo ActiveX di Windows Media Player, metodi per il modello a oggetti
- Controllo ActiveX, metodi per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, metodi per il modello a oggetti
- Windows Media Player Mobile, metodi per il modello a oggetti
- Controllo ActiveX di Windows Media Player, eventi per il modello a oggetti
- Controllo ActiveX, eventi per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, eventi per il modello a oggetti
- Windows Media Player Mobile, eventi per il modello a oggetti
- Proprietà, modello a oggetti di Windows Media Player
- metodi, modello a oggetti di Windows Media Player
- eventi, modello a oggetti di Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e06a860d04bfc1a5ccd5b33c0604a0ef818a0127
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116845"
---
# <a name="properties-methods-and-events"></a>Proprietà, metodi ed eventi

Ogni oggetto dispone di metodi e proprietà tramite i quali è possibile programmare il controllo Media Player di Windows. Un metodo è un'azione che può essere eseguita dall'oggetto. Una proprietà è un valore di dati che è possibile leggere o modificare. Ad esempio, il metodo **Play** avvia la riproduzione del contenuto e la proprietà **framerate** indica la frequenza dei fotogrammi corrente del contenuto che viene riprodotto.

Inoltre, l'oggetto **Player** genera eventi che offrono la possibilità di eseguire azioni in momenti specifici. È possibile scrivere codice in un gestore eventi che verrà eseguito quando Windows Media Player genera l'evento corrispondente. Ad esempio, è possibile scrivere il codice in un gestore eventi **PlayStateChange** che determina se la modifica dello stato è che i supporti sono terminati e in tal caso viene visualizzata una finestra di dialogo in cui viene chiesto agli utenti se desiderano riprodurre nuovamente i supporti.

> [!Note]  
> Tutti i metodi del modello a oggetti di Windows Media Player sono asincroni. Se si chiamano due metodi nella stessa procedura, il secondo metodo non può basarsi sul primo metodo che ha completato l'azione.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> </dl>

 

 




