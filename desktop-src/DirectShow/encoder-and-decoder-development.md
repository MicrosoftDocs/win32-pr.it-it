---
description: Sviluppo di codificatori e decodificatori
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: Sviluppo di codificatori e decodificatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe45fc726338e33205831959986178f4527673a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124554"
---
# <a name="encoder-and-decoder-development"></a>Sviluppo di codificatori e decodificatori

Questa sezione contiene articoli relativi allo sviluppo di codificatori e decodificatori per DirectShow. Questi argomenti non sono rilevanti per gli sviluppatori di applicazioni.

Un decodificatore software che supporta l'accelerazione video DirectX (VA) deve essere implementato come filtro di trasformazione copia DirectShow. Se il decodificatore non supporta DirectX VA, può anche essere implementato come un oggetto DMO (DirectX Media Object). Un decodificatore che si connette a un renderer video non deve essere implementato come filtro Trans-on-Place, perché questo comporterà una riduzione significativa delle prestazioni. Per informazioni su come scrivere un filtro di trasformazione copia, vedere [scrittura di filtri di trasformazione](writing-transform-filters.md).

I codificatori software possono essere implementati come filtri di trasformazione o DMOs. I codificatori non usano DirectX VA, perché DirectX VA attualmente usato solo per la decompressione. La specifica dell'API del codificatore descritta in questa sezione è pertinente per codificatori hardware e software.

Questa sezione contiene i seguenti argomenti:

-   [API del codificatore](encoder-api.md)
-   [Specifiche e interfacce del decodificatore](decoder-interfaces-and-specifications.md)
-   [Impostazioni del decodificatore per Windows Media Center Edition](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di VMR per gli sviluppatori di filtri DirectShow](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



