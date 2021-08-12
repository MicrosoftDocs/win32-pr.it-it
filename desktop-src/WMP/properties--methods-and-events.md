---
title: Proprietà, metodi ed eventi
description: Proprietà, metodi ed eventi
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Windows Media Player,proprietà per il modello a oggetti
- Windows Media Player,metodi per il modello a oggetti
- Windows Media Player,eventi per il modello a oggetti
- Windows Media Player a oggetti, proprietà
- Windows Media Player a oggetti, metodi
- Windows Media Player a oggetti, eventi
- modello a oggetti,proprietà
- modello a oggetti,metodi
- modello a oggetti,eventi
- Windows Media Player ActiveX, proprietà per il modello a oggetti
- ActiveX, proprietà per il modello a oggetti
- Windows Media Player Controllo ActiveX per dispositivi mobili, proprietà per il modello a oggetti
- Windows Media Player Mobile, proprietà per il modello a oggetti
- Windows Media Player ActiveX, metodi per il modello a oggetti
- ActiveX, metodi per il modello a oggetti
- Windows Media Player Controllo ActiveX per dispositivi mobili,metodi per il modello a oggetti
- Windows Media Player Mobile, metodi per il modello a oggetti
- Windows Media Player ActiveX, eventi per il modello a oggetti
- ActiveX, eventi per il modello a oggetti
- Windows Media Player Controllo ActiveX per dispositivi mobili,eventi per il modello a oggetti
- Windows Media Player Mobile, eventi per il modello a oggetti
- proprietà, modello Windows Media Player a oggetti
- metodi, modello Windows Media Player a oggetti
- eventi, Windows Media Player a oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbcc07977bc7ddcd2dd162600d4fa3d2822a3f52f38983ea8427f89d9403ecf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571085"
---
# <a name="properties-methods-and-events"></a>Proprietà, metodi ed eventi

Ogni oggetto dispone di metodi e proprietà tramite i quali è possibile programmare il Windows Media Player controllo. Un metodo è un'azione che l'oggetto può eseguire. Una proprietà è un valore di dati che è possibile leggere o modificare. Ad esempio, il **metodo Play** avvia la riproduzione del contenuto e la **proprietà frameRate** indica la frequenza fotogrammi corrente del contenuto in riproduzione.

Inoltre, **l'oggetto Player** genera eventi che offrono la possibilità di eseguire azioni in momenti specifici. Si scrive codice in un gestore eventi che verrà eseguito quando Windows Media Player genera l'evento corrispondente. Ad esempio, è possibile scrivere codice in un gestore dell'evento **PlayStateChange** che determina se la modifica dello stato è che il contenuto multimediale è terminato e, in tal caso, visualizzare una finestra di dialogo che chiede agli utenti se vogliono riprodurre nuovamente il contenuto multimediale.

> [!Note]  
> Tutti i metodi nel modello Windows Media Player a oggetti sono asincroni. Se si chiamano due metodi nella stessa routine, il secondo metodo non può basarsi sul primo metodo dopo aver completato l'azione.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> </dl>

 

 




