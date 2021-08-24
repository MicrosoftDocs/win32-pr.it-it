---
description: Gli effetti di nebbia possono dare a una scena 3D maggiore realistico.
ms.assetid: 26fe4f7c-7bb3-4a52-b539-5de2b11256e9
title: Stato della nebbia (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84004b8f261f9a6dc4c9b800ba5baa1f9a3c3e528db2b94e86286c3752414729
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564241"
---
# <a name="fog-state-direct3d-9"></a>Stato della nebbia (Direct3D 9)

Gli effetti di nebbia possono dare a una scena 3D maggiore realistico. È possibile usare gli effetti della simulare la simulare la nebbia. Possono anche ridurre la chiarezza di una scena con la distanza. Ciò rispecchia ciò che accade nel mondo reale; Quando gli oggetti diventano più distanti dall'utente, i relativi dettagli sono meno distinti.

Per altre informazioni sull'uso di osa nell'applicazione, vedere [Nebbia (Direct3D 9)](fog.md).

Un'applicazione C++ controlla la nebbia attraverso gli stati di rendering del dispositivo. Il tipo enumerato [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) include gli stati per controllare se vengono usati pixel (tabella) o vertice, il colore, la formula della nebbia applicata dal sistema e i parametri della formula.

Per abilitare la nebbia, impostare lo stato di rendering DI D3DRS \_ FOGENABLE su **TRUE.** Il colore della nebbia può essere impostato su qualsiasi valore di colore usando lo stato di rendering D3DRS FOGCOLOR. Il componente alfa del colore della nebbia \_ viene ignorato.

Gli stati di rendering \_ D3DRS FOGTABLEMODE e D3DRS FOGVERTEXMODE controllano la formula della nebbia applicata per i calcoli della nebbia e controllano indirettamente il tipo di nebbia \_ applicata. Entrambi gli stati di rendering possono essere impostati su un membro del [**tipo enumerato D3DFOGMODE.**](./d3dfogmode.md) L'impostazione dello stato di rendering su D3DFOG NONE disabilita rispettivamente i pixel o \_ i vertici. Se entrambi gli stati di rendering sono impostati su modalità valide, il sistema applica solo effetti di nebbia pixel.

Gli stati di rendering D3DRS FOGSTART e D3DRS FOGEND controllano i parametri della formula della nebbia per \_ \_ la modalità LINEARE D3DFOG. \_ Lo stato di rendering D3DRS \_ FOGDENSITY controlla la densità della nebbia nelle modalità di nebbia esponenziale.

Per altre informazioni, vedere [Parametri di nebbio (Direct3D 9).](fog-parameters.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 
