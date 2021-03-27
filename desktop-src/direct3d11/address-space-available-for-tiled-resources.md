---
title: Spazio degli indirizzi disponibile per le risorse affiancate
description: In questa sezione viene specificato lo spazio degli indirizzi virtuale disponibile per le risorse affiancate.
ms.assetid: A3D08564-3C7A-4578-BC38-EE202045580A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c774c697cf5d3bf575d01ce5751dc413c1d14b0
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/13/2019
ms.locfileid: "103719327"
---
# <a name="address-space-available-for-tiled-resources"></a>Spazio degli indirizzi disponibile per le risorse affiancate

In questa sezione viene specificato lo spazio degli indirizzi virtuale disponibile per le risorse affiancate.

Nei sistemi operativi a 64 bit sono disponibili almeno 40 bit di spazio degli indirizzi virtuali (1 terabyte).

Per i sistemi operativi a 32 bit, lo spazio degli indirizzi è 32 bit (4 GB). Per i sistemi ARM a 32 bit, la creazione di singole risorse affiancate può non riuscire se l'allocazione utilizzerà più di 27 bit di spazio degli indirizzi (128 MB). Sono incluse eventuali spaziatura interna nascosta nello spazio degli indirizzi che l'hardware può usare per mipmap, riempimento affiancato e possibilmente dimensioni della superficie di riempimento a potenze di 2.

Nei sistemi grafici con una tabella di pagina separata per l'unità di elaborazione grafica (GPU), la maggior parte di questo spazio di indirizzi sarà disponibile per le risorse GPU eseguite dall'applicazione, sebbene le allocazioni GPU eseguite dal driver di visualizzazione rientrino nello stesso spazio.

Nei sistemi futuri con una tabella di pagina condivisa tra la CPU e la GPU, lo spazio degli indirizzi disponibile viene condiviso tra tutte le allocazioni di CPU e GPU in un processo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Parametri per la creazione di risorse affiancate](tiled-resource-creation-parameters.md)
</dt> </dl>

 

 




