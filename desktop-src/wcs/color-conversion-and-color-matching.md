---
title: Conversione dei colori e corrispondenza colori
description: Il processo di conversione dei colori da uno spazio colori a un altro è detto conversione dei colori.
ms.assetid: 52f68779-d4d6-4f1e-88a4-f872e9e90054
keywords:
- Windows Sistema di colori (WCS), conversione dei colori
- WCS (Windows Color System),conversione dei colori
- gestione del colore delle immagini, conversione dei colori
- gestione dei colori, conversione dei colori
- colori, conversione dei colori
- conversione dei colori
- Windows Sistema di colori (WCS), corrispondenza colori
- WCS (Windows Color System),corrispondenza colori
- gestione dei colori delle immagini, corrispondenza dei colori
- gestione dei colori, corrispondenza colori
- colori, corrispondenza colori
- corrispondenza colori
- Windows Sistema di colori (WCS), mapping dei colori
- WCS (Windows Color System),mapping dei colori
- gestione dei colori delle immagini, mapping dei colori
- gestione dei colori, mapping dei colori
- colori, mapping dei colori
- mapping dei colori
- punto bianco
- Coloranti
- correzione di gamma
- Gamma
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0071e15c2d572c134d61aee7a018b41c8d09507e87963eeeed1488909cdafeba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110801"
---
# <a name="color-conversion-and-color-matching"></a>Conversione dei colori e corrispondenza colori

Il processo di conversione dei colori da uno [spazio colori](c.md) a un altro è detto *conversione dei colori.* Tutti i colori in uno spazio colori sono fissi rispetto al punto bianco [dello spazio colori.](w.md) Poiché il punto bianco di uno spazio colore varia da dispositivo a dispositivo, è necessario associare un colore convertito al colore visivamente più vicino nello spazio colori di destinazione. Questo processo è denominato *mapping dei colori.*

Ad esempio, se si dispone di un'immagine digitale creata sullo schermo, potrebbe essere in uno spazio colore RGB dipendente dal dispositivo. Se si desidera stamparlo su una stampante, è necessario convertirlo nello spazio colore della stampante. Poiché la stampante usa probabilmente uno spazio colore CMYK dipendente dal dispositivo, tutti i valori RGB devono essere convertiti in CYMK. Si tratta della [conversione dei colori.](c.md) Dopo aver specificato i valori in termini di spazio CYMK, è necessario associare i valori al colore più vicino che la stampante può produrre. Questa operazione è detta mapping dei colori o [corrispondenza dei colori.](c.md)

Sia la conversione dei colori che il mapping dei colori devono prendere in considerazione diversi fattori specifici del dispositivo. Ad esempio, i blocchi predefiniti delle immagini dello schermo sono pixel. Ogni pixel ha un numero impostato di bit per archiviare il valore di indice del colore o del colore. Il numero di bit per pixel dipende dal tipo di scheda di visualizzazione e di scheda di visualizzazione in uso e dalla modalità su cui è impostata l'adattatore. La maggior parte di ogni tipo di [stampante usa colori diversi](c.md) e stampa a risoluzioni particolari.

Inoltre, le caratteristiche del tono fisico di un dispositivo sono spesso diverse in dispositivi diversi. Ad esempio, quando i colori vengono prodotti dai monitor dei computer, possono apparire diversi da quelli prodotti su una pressa da stampa. Un fattore di correzione, denominato *correzione gamma,* viene spesso usato per compensare tali differenze.

Il risultato di questi fattori dipendenti dal dispositivo è che ogni dispositivo a colori ha un particolare set di colori che può produrre. Questo set di colori è noto come *gamut.* Per eseguire la conversione dei colori e il mapping dei colori, i colori in un'immagine devono essere convertiti dallo spazio colori e dalla gamma del dispositivo di origine nello spazio dei colori del dispositivo di destinazione. Vengono quindi abbinati alla gamma del dispositivo di destinazione.

 

 




