---
description: Sviluppo di codificatori e decodificatori
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: Sviluppo di codificatori e decodificatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8619225f5d4df9596523724259eb4eee1a9b3bb4c978a3fc400156bc9ee56a4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015819"
---
# <a name="encoder-and-decoder-development"></a>Sviluppo di codificatori e decodificatori

Questa sezione contiene articoli sullo sviluppo di codificatori e decodificatori per DirectShow. Questi argomenti non sono rilevanti per gli sviluppatori di applicazioni.

Un decodificatore software che supporta l'accelerazione video DirectX deve essere implementato come filtro di trasformazione DirectShow copia. Se il decodificatore non supporta DirectX VA, può essere implementato anche come Oggetto multimediale DirectX (DMO). Un decodificatore che si connette a un renderer video non deve essere implementato come filtro trans-in-place, perché ciò comporta una riduzione significativa delle prestazioni. Per informazioni su come scrivere un filtro di trasformazione di copia, vedere [Scrittura di filtri di trasformazione.](writing-transform-filters.md)

I codificatori software possono essere implementati come filtri di trasformazione o DMO. I codificatori non usano DirectX VA, poiché DirectX VA attualmente viene usato solo per la decompressione. La specifica dell'API del codificatore descritta in questa sezione è rilevante per i codificatori hardware e software.

Questa sezione contiene i seguenti argomenti:

-   [API del codificatore](encoder-api.md)
-   [Interfacce e specifiche del decodificatore](decoder-interfaces-and-specifications.md)
-   [Decodificatore Impostazioni per Windows Media Center Edition](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della macchina virtuale per gli sviluppatori DirectShow filtri](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



