---
title: Spazio indirizzi disponibile per le risorse affiancate
description: Questa sezione specifica lo spazio degli indirizzi virtuali disponibile per le risorse affiancate.
ms.assetid: A3D08564-3C7A-4578-BC38-EE202045580A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5753fdb9d700689c6ebfffdae4368399c0e4bb36d328c9ff1a8cfc284005214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734283"
---
# <a name="address-space-available-for-tiled-resources"></a>Spazio indirizzi disponibile per le risorse affiancate

Questa sezione specifica lo spazio degli indirizzi virtuali disponibile per le risorse affiancate.

Nei sistemi operativi a 64 bit sono disponibili almeno 40 bit di spazio degli indirizzi virtuali (1 Terabyte).

Per i sistemi operativi a 32 bit, lo spazio indirizzi è a 32 bit (4 GB). Per i sistemi ARM a 32 bit, la creazione di singole risorse affiancate può non riuscire se l'allocazione usa più di 27 bit di spazio degli indirizzi (128 MB). Ciò include la spaziatura interna nascosta nello spazio degli indirizzi che l'hardware può usare per le mipmap, la spaziatura interna delle sezioni impacchetto ed eventualmente le dimensioni della superficie di riempimento su 2.

Nei sistemi di grafica con una tabella di pagine separata per l'unità di elaborazione grafica (GPU), la maggior parte di questo spazio indirizzi sarà disponibile per le risorse GPU effettuate dall'applicazione, anche se le allocazioni gpu effettuate dal driver di visualizzazione rientrano nello stesso spazio.

Nei sistemi futuri con una tabella di pagine condivisa tra CPU e GPU, lo spazio indirizzi disponibile viene condiviso tra tutte le allocazioni di CPU e GPU in un processo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Parametri di creazione di risorse affiancate](tiled-resource-creation-parameters.md)
</dt> </dl>

 

 




