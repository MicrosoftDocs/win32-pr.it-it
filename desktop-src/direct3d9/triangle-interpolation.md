---
description: Durante il rendering, la pipeline interpola i dati dei vertici in ogni triangolo.
ms.assetid: 6fa05e56-c4cd-4623-abe9-2b1c8bbc644b
title: Interpolazione triangolare (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a411f53351ccd5d3407b358b03e705677e9bf5a96a57b162016afe09332bae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746261"
---
# <a name="triangle-interpolation-direct3d-9"></a>Interpolazione triangolare (Direct3D 9)

Durante il rendering, la pipeline interpola i dati dei vertici in ogni triangolo. I dati dei vertici possono essere un'ampia gamma di dati e possono includere (ma non solo): colore diffuso, colore speculare, alfa diffuso (opacità triangolare), alfa speculare e fattore di nebbia (tratto da un alfa speculare per la pipeline dei vertici a funzione fissa e dal registro della nebbia per la pipeline dei vertici programmabili). I dati dei vertici sono definiti dalla [dichiarazione vertex (Direct3D 9).](vertex-declaration.md)

Per alcuni dati sui vertici, l'interpolazione dipende dalla modalità di ombreggiatura corrente, come illustrato nella tabella seguente.



| Modalità ombreggiatura | Descrizione                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Semplice         | Solo il fattore di nebbia viene interpolato in modalità ombreggiatura piana. Per tutti gli altri valori interpolati, il colore del primo vertice nel triangolo viene applicato sull'intero viso. |
| Gouraud      | L'interpolazione lineare viene eseguita tra tutti e tre i vertici.                                                                                                               |



 

Il colore diffuso e il colore speculare vengono trattati in modo diverso, a seconda del modello di colore. Nel modello di colore RGB il sistema usa i componenti di colore rosso, verde e blu nell'interpolazione.

Il componente alfa di un colore viene considerato come un valore interpolato separato perché i driver di dispositivo possono implementare la trasparenza in due modi diversi: usando la fusione delle trame o l'uso di stippling.

Usare il membro ShadeCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) per determinare le forme di interpolazione supportate dal driver di dispositivo corrente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sistemi di coordinate e geometria](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



