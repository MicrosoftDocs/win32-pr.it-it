---
title: Conversione colori e corrispondenza colori
description: Il processo di conversione dei colori da uno spazio colore a un altro viene definito conversione di colori.
ms.assetid: 52f68779-d4d6-4f1e-88a4-f872e9e90054
keywords:
- Windows Color System (WCS), conversione colori
- WCS (sistema di colori Windows), conversione colori
- Gestione colori immagine, conversione colori
- Gestione colori, conversione colori
- colori, conversione colori
- Conversione colori
- Windows Color System (WCS), corrispondenza colori
- WCS (sistema di colori Windows), corrispondenza colori
- Gestione colori immagine, corrispondenza colori
- gestione dei colori, corrispondenza dei colori
- colori, corrispondenza colori
- corrispondenza colori
- Sistema colori Windows (WCS), mapping colori
- WCS (sistema di colori Windows), mapping colori
- Gestione colori immagine, mapping colori
- Gestione colori, mapping colori
- colori, mapping colori
- mapping colori
- punto bianco
- coloranti
- correzione di gamma
- gamma
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74de95238472f58d49c5033a601c6d5458773c8
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/26/2021
ms.locfileid: "106320146"
---
# <a name="color-conversion-and-color-matching"></a>Conversione colori e corrispondenza colori

Il processo di conversione dei colori da uno [spazio colore](c.md) a un altro viene definito *conversione di colori*. Tutti i colori in uno spazio colore sono fissi rispetto al [punto bianco](w.md)dello spazio dei colori. Poiché il punto bianco di uno spazio di colore varia da dispositivo a dispositivo, è necessario trovare una corrispondenza tra il colore convertito e il colore più vicino a quello visuale nello spazio dei colori di destinazione. Questo processo è denominato *mapping dei colori*.

Se, ad esempio, si dispone di un'immagine digitale creata sullo schermo, potrebbe trovarsi in uno spazio di colore RGB dipendente dal dispositivo. Se si desidera stamparlo su una stampante, è necessario convertirlo nello spazio dei colori della stampante. Poiché la stampante usa probabilmente uno spazio colore CMYK dipendente dal dispositivo, tutti i valori RGB devono essere convertiti in CYMK. Si tratta della [conversione di colori](c.md). Una volta specificati i valori in termini di spazio CYMK, è necessario che corrispondano al colore più vicino che la stampante può produrre. Questa operazione è denominata mapping dei colori o [corrispondenza dei colori](c.md).

Sia la conversione dei colori che la mappatura dei colori devono prendere in considerazione alcuni fattori specifici del dispositivo. Ad esempio, i blocchi predefiniti delle immagini dello schermo sono pixel. Ogni pixel ha un numero impostato di bit per archiviare il valore di indice colore o colore. Il numero di bit per pixel dipende dal tipo di visualizzazione e dall'adattatore di visualizzazione utilizzati e dalla modalità di impostazione dell'adapter. La maggior parte di ogni tipo di stampante usa diversi [coloranti](c.md) e stampa con risoluzioni specifiche.

Inoltre, le caratteristiche di tono fisico di un dispositivo sono spesso diverse in dispositivi diversi. Se, ad esempio, i colori sono prodotti da monitoraggi computer, è possibile che vengano visualizzati diversi da quelli generati in caso di stampa. Un fattore di correzione, denominato *correzione gamma*, viene spesso usato per compensare tali differenze.

Il risultato di questi fattori dipendenti dal dispositivo è che ogni dispositivo di colore dispone di un particolare set di colori che può produrre. Questo set di colori è noto come *gamut*. Per eseguire la conversione dei colori e il mapping dei colori, è necessario convertire i colori di un'immagine dallo spazio di colore e dalla gamma del dispositivo di origine allo spazio dei colori del dispositivo di destinazione. Viene quindi abbinata alla gamma del dispositivo di destinazione.

 

 




