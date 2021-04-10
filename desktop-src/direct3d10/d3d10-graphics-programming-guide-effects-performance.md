---
description: Considerazioni sulle prestazioni (Direct3D 10)
ms.assetid: 9f029be5-4ce0-46ca-909b-adaa980398e7
title: Considerazioni sulle prestazioni (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ba2dbe00475efebdb6ff5d772b3eccd6cd4263a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049135"
---
# <a name="performance-considerations-direct3d-10"></a>Considerazioni sulle prestazioni (Direct3D 10)

## <a name="using-effect-pools"></a>Uso di pool di effetti

Per il rendering di pipeline è comune usare molti shader per eseguire il rendering di tipi di oggetto e effetti speciali diversi. Lo shader è costituito da una combinazione di stati comuni tra tutti gli shader, ad esempio una matrice globale o una posizione chiara e un altro stato specifico per ogni shader, ad esempio il colore diffuso di un oggetto o il calcolo dell'evidenziazione speculare. Un pool di effetti è una posizione in memoria per archiviare lo stato utilizzato in molti shader, oltre a oggetti dispositivo comuni, ad esempio shader, oggetti di stato di rendering e buffer costanti. Il miglioramento delle prestazioni risulta dall'aggiornamento dello stato comune per tutti gli shader che necessitano di tale stato.

Un pool di effetti è una posizione di memoria condivisa per lo stato dell'effetto. Un pool viene creato in modo analogo a un effetto; è possibile crearla dalla memoria (oppure da un file o una risorsa). Questo comporta due diversi tipi di effetti: un effetto globale che non dipende dallo stato in altro effetto rispetto a un effetto figlio che dipende dallo stato in un altro effetto.

Si specifica se un effetto è un effetto globale (caso predefinito) o un effetto figlio (specificando il flag dell' [effetto \_ \_ \_ \_ figlio compila effetto D3D10](d3d10-effect.md) ) quando viene creato l'effetto. Un effetto globale può fungere da pool di effetti; un effetto figlio non può essere un pool di effetti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un effetto](d3d10-graphics-programming-guide-effects-render.md)
</dt> <dt>

[Effetti (Direct3D 10)](d3d10-graphics-programming-guide-effects.md)
</dt> </dl>

 

 



