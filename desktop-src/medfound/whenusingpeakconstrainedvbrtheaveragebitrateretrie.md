---
description: Quando si usa il valore VBR con vincoli di picco, la velocità in bit media recuperata dall'oggetto codec è maggiore della velocità in bit massima.
ms.assetid: 5fc344f8-4492-4878-802a-94606c5f33e0
title: Quando si usa il valore VBR con vincoli di picco, la velocità in bit media recuperata dall'oggetto codec è maggiore della velocità in bit massima. Come è possibile?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2bb2e09f5210baf8817553377fc832b9826b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344841"
---
# <a name="when-i-use-peak-constrained-vbr-the-average-bit-rate-retrieved-from-the-codec-object-is-larger-than-the-peak-bit-rate-how-is-that-possible"></a>Quando si usa il valore VBR con vincoli di picco, la velocità in bit media recuperata dall'oggetto codec è maggiore della velocità in bit massima. Come è possibile?

La relazione tra la velocità in bit media e la velocità in bit massima è spesso fraintesa. La velocità in bit massima descrive un vincolo di buffer in un periodo di tempo specificato dalla finestra del buffer di picco. La velocità in bit media per VBR a due passaggi (non vincolata o con picco) corrisponde alla media di bit al secondo per la durata del file.

Come descritto nel [modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md), la velocità in bit effettiva utilizzata in un periodo di tempo uguale alla finestra del buffer può avvicinarsi al doppio della velocità in bit. Questo perché il buffer, definito come un numero di bit uguale alla velocità in bit per la finestra del buffer (in secondi), viene svuotato a una velocità costante.

Ad esempio, in un secondo di un flusso di 56 Kbps, il codificatore crea esempi totali di 59 KB. Quindi, 56 KB di dati vengono rimossi dal buffer in quel secondo, lasciando 3 KB nel buffer. Se il flusso ha una finestra del buffer di tre secondi e pertanto una dimensione del buffer totale di 168 KB, il riempimento del buffer richiederà circa 40 secondi. Velocità in bit media per il flusso (se la durata è inferiore al tempo necessario per riempire il buffer) è 59 kbps, anche se la velocità in bit è impostata su 56 Kbps.

Lo stesso fenomeno si applica ai vincoli di velocità in bit massimi. Per contenuto breve, la velocità in bit media calcolata dall'oggetto codec dopo il completamento della codifica può essere maggiore della velocità in bit massima.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Domande frequenti](frequentlyaskedquestions.md)
</dt> </dl>

 

 



