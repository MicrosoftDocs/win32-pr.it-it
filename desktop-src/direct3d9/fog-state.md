---
description: Gli effetti di nebbia possono dare maggiore realismo a una scena 3D.
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: Stato di nebbia (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d3103cbbd3dfb220e2ddd75078040702fd7557
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401043"
---
# <a name="fog-state-direct3d-9"></a>Stato di nebbia (Direct3D 9)

Gli effetti di nebbia possono dare maggiore realismo a una scena 3D. È possibile utilizzare gli effetti di nebbia per più della simulazione della nebbia. Possono anche ridurre la chiarezza di una scena con distanza. Questo rispecchia ciò che accade nel mondo reale. Poiché gli oggetti diventano più distanti dall'utente, i relativi dettagli sono meno distinti.

Per ulteriori informazioni sull'utilizzo di fog nell'applicazione, vedere [Fog (Direct3D 9)](fog.md).

Un'applicazione C++ controlla la nebbia tramite gli Stati di rendering del dispositivo. Il tipo enumerato [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) include gli Stati per controllare se vengono usati pixel (tabella) o la nebbia dei vertici, il colore, la formula di nebbia applicata dal sistema e i parametri della formula.

Per abilitare la nebbia, impostare lo \_ stato di rendering FOGENABLE di D3DRS su **true**. Il colore di nebbia può essere impostato su qualsiasi valore di colore utilizzando lo \_ stato di rendering FogColor di D3DRS. il componente alfa del colore di nebbia viene ignorato.

Gli \_ Stati di rendering D3DRS FOGTABLEMODE e D3DRS \_ FOGVERTEXMODE controllano la formula di nebbia applicata ai calcoli di nebbia e controllano indirettamente quale tipo di nebbia viene applicato. Entrambi gli Stati di rendering possono essere impostati su un membro del tipo enumerato [**D3DFOGMODE**](./d3dfogmode.md) . L'impostazione dello stato di rendering su D3DFOG \_ none Disabilita rispettivamente il pixel o la nebbia del vertice. Se entrambi gli Stati di rendering sono impostati su modalità valide, il sistema applica solo gli effetti di nebbia dei pixel.

Gli \_ Stati D3DRS FOGSTART e D3DRS \_ FOGEND render controllano i parametri della Formula Fog per la \_ modalità lineare D3DFOG. Lo \_ stato di rendering FOGDENSITY di D3DRS controlla la densità della nebbia nelle modalità di nebbia esponenziale.

Per altre informazioni, vedere [parametri di nebbia (Direct3D 9)](fog-parameters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 
