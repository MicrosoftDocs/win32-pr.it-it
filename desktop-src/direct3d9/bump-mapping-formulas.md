---
description: Direct3D applica le formule seguenti ai componenti DU e DV in ogni pixel della mappa Bump.
ms.assetid: ae1de432-d1cc-45a5-b25f-b669cd30af3b
title: Formule di mapping di Bump (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436aee9689d78b8b706bb98d908f2e3fbc05ca6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127779"
---
# <a name="bump-mapping-formulas-direct3d-9"></a>Formule di mapping di Bump (Direct3D 9)

Direct3D applica le formule seguenti ai componenti D<sub>U</sub> e d<sub>V</sub> in ogni pixel della mappa.

![formule di trasformazioni di matrici di mapping Bump](images/dudv-transform.png)

In queste formule, le variabili D<sub>u</sub> e d<sub>v</sub> vengono ricavate direttamente da un pixel della mappa a urto e trasformate da una matrice 2x2 per produrre i valori delta di output D<sub>U</sub>"e d<sub>V</sub>". Il sistema usa i valori di output per modificare le coordinate di trama che indirizzano la mappa dell'ambiente nella fase di trama successiva. I coefficienti della matrice di trasformazione vengono impostati tramite gli \_ Stati della fase della trama D3DTSS BUMPENVMAT00, D3DTSS \_ BUMPENVMAT10, D3DTSS \_ BUMPENVMAT01 e D3DTSS BUMPENVMAT11 \_ .

Oltre ai valori Delta utente e v, il sistema è in grado di calcolare un valore di luminanza utilizzato per modulare il colore della mappa dell'ambiente nella fase di Blend successiva, come illustrato nella formula seguente.

![formula per la luminanza di output, calcolata dal fattore di scala e dall'offset](images/l-transform.png)

In questa formula, L'è la luminanza di output calcolata. La variabile L è il valore di luminanza tratto da un pixel della mappa Bump, moltiplicato per il fattore di scala, S e offset in base al valore nella variabile O. Gli \_ Stati della fase D3DTSS BUMPENVLSCALE e D3DTSS \_ BUMPENVLOFFSET texture controllano i valori per le variabili S e O nella formula. Questa formula viene applicata solo quando l'operazione di combinazione di trame per la fase che contiene la mappa Bump è impostata su D3DTOP \_ BUMPENVMAPLUMINANCE. Quando si usa D3DTOP \_ BUMPENVMAP, il sistema usa un valore di 1,0 per L.

Dopo aver calcolato i valori delta di output D<sub>U</sub>e d<sub>V</sub>, il sistema li aggiunge alle coordinate di trama nella successiva fase della trama e modula il colore scelto dalla luminanza per produrre il colore applicato al poligono.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Bump mapping](bump-mapping.md)
</dt> </dl>

 

 



