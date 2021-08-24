---
description: Quando si usa vbr con vincoli di picco, la velocità in bit media recuperata dall'oggetto codec è maggiore della velocità in bit di picco.
ms.assetid: 5fc344f8-4492-4878-802a-94606c5f33e0
title: Quando si usa vbr con vincoli di picco, la velocità in bit media recuperata dall'oggetto codec è maggiore della velocità in bit di picco. Come è possibile?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa27e1a03c12f854486c65d7959c66f6592da4c3fea84936ee671a911f7fa46d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011951"
---
# <a name="when-i-use-peak-constrained-vbr-the-average-bit-rate-retrieved-from-the-codec-object-is-larger-than-the-peak-bit-rate-how-is-that-possible"></a>Quando si usa vbr con vincoli di picco, la velocità in bit media recuperata dall'oggetto codec è maggiore della velocità in bit di picco. Come è possibile?

La relazione tra la velocità in bit media e la velocità in bit di picco è spesso fraintinte. La velocità in bit di picco descrive un vincolo del buffer in un periodo di tempo specificato dalla finestra del buffer di picco. La velocità in bit media per VBR a due passi (senza vincoli o vincolati di picco) è la velocità media di bit al secondo per la durata del file.

Come descritto in [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md), la velocità in bit effettiva usata in un periodo di tempo uguale alla finestra del buffer può essere due volte superiore alla velocità in bit. Ciò è dovuto al fatto che il buffer, definito come un numero di bit uguale alla velocità in bit per la finestra del buffer (in secondi), viene svuotato a una velocità costante.

Ad esempio, in un secondo di un flusso di 56 Kbps, il codificatore crea campioni per un totale di 59 Kb. 56 Kb di dati vengono quindi rimossi dal buffer in quel secondo, lasciando 3 Kb nel buffer. Se il flusso ha una finestra del buffer di tre secondi e quindi una dimensione totale del buffer di 168 Kb, il riempimento del buffer potrebbe richiedere quasi 40 secondi. La velocità in bit media per il flusso (se la durata è inferiore al tempo necessario per riempire il buffer) è di 59 Kbps, anche se la velocità in bit è impostata su 56 Kbps.

Lo stesso fenomeno si applica ai vincoli di velocità in bit di picco. Per il contenuto breve, la velocità in bit media calcolata dall'oggetto codec dopo il completamento della codifica può essere maggiore della velocità in bit di picco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Domande frequenti](frequentlyaskedquestions.md)
</dt> </dl>

 

 



