---
description: Direct3D applica le formule seguenti ai componenti DU e DV in ogni pixel della mappa a rilievo.
ms.assetid: ae1de432-d1cc-45a5-b25f-b669cd30af3b
title: Formule di bump mapping (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86035a28966c841f7d593cb46c7c7d969f7b2addaacb6cf43e25ceebdca83ff2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805858"
---
# <a name="bump-mapping-formulas-direct3d-9"></a>Formule di bump mapping (Direct3D 9)

Direct3D applica le formule seguenti ai componenti D<sub>U</sub> e D<sub>V</sub> in ogni pixel della mappa di rilievo.

![formule delle trasformazioni della matrice di mapping delle urti](images/dudv-transform.png)

In queste formule, le variabili D<sub>U</sub> e D<sub>V</sub> vengono prese direttamente da un pixel della mappa di rilievo e trasformate da una matrice 2x2 per produrre i valori differenziali di output D<sub>U</sub>' e D<sub>V</sub>'. Il sistema usa i valori di output per modificare le coordinate della trama che si indirizzano alla mappa dell'ambiente nella fase successiva della trama. I coefficienti della matrice di trasformazione vengono impostati con gli stati di fase della trama D3DTSS \_ BUMPENVMAT00, D3DTSS \_ BUMPENVMAT10, D3DTSS \_ BUMPENVMAT01 e D3DTSS \_ BUMPENVMAT11.

Oltre ai valori delta di you e v, il sistema può calcolare un valore di luminance che usa per modulare il colore della mappa dell'ambiente nella fase di fusione successiva, come illustrato nella formula seguente.

![formula per la luminanza di output, calcolata dal fattore di scala e dall'offset](images/l-transform.png)

In questa formula, L' è la luminanza di output calcolata. La variabile L è il valore di luminance tratto da un pixel della mappa di rilievo, moltiplicato per il fattore di scala S e l'offset per il valore nella variabile O. Gli stati di fase della trama \_ D3DTSS BUMPENVLSCALE e D3DTSS BUMPENVLOFFSET controllano i valori per le variabili S e \_ O nella formula. Questa formula viene applicata solo quando l'operazione di fusione della trama per la fase che contiene la mappa di rilievo è impostata su D3DTOP \_ BUMPENVMAPLUMINANCE. Quando si usa D3DTOP BUMPENVMAP, il sistema usa il valore \_ 1.0 per L'.

Dopo aver calcolato i valori differenziali di output D<sub>U</sub>' e D<sub>V',</sub>il sistema li aggiunge alle coordinate della trama nella fase successiva della trama e modula il colore scelto dalla luminanza per produrre il colore applicato al poligono.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bump Mapping](bump-mapping.md)
</dt> </dl>

 

 



