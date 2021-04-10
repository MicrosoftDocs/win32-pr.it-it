---
description: I vertici nello spazio della fotocamera vengono calcolati trasformando i vertici degli oggetti con la matrice di visualizzazione globale.
ms.assetid: 889dd0d8-1933-4901-9bbc-06c3caa26d3e
title: Trasformazioni dello spazio della fotocamera (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e621fa8318fa45023cee13ffc6fcfc65abcf8f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126883"
---
# <a name="camera-space-transformations-direct3d-9"></a>Trasformazioni dello spazio della fotocamera (Direct3D 9)

I vertici nello spazio della fotocamera vengono calcolati trasformando i vertici degli oggetti con la matrice di visualizzazione globale.

V = V \* wvMatrix

Le normali dei vertici, nello spazio della fotocamera, vengono calcolate trasformando le normali dell'oggetto con la trasformazione inversa della matrice di visualizzazione globale. La matrice della vista globale può essere o non essere ortogonale.

N = N \* (wvMatrix ⁻ ¹)<sup>T</sup>

La matrice inversion e la matrice TRANSPOSE operano su una matrice 4x4. L'oggetto Multiply combina il normale con la parte 3x3 della matrice 4x4 risultante.

Se lo stato di rendering, D3DRENDERSTATE \_ NORMALIZENORMALS è impostato su **true**, i vettori normali dei vertici vengono normalizzati dopo la trasformazione nello spazio della fotocamera, come indicato di seguito:

N = Norm (N)

La posizione della luce nello spazio della fotocamera viene calcolata trasformando la posizione di origine della luce con la matrice di visualizzazione.

LP = LP \* vMatrix

La direzione verso la luce nello spazio della fotocamera per una luce direzionale viene calcolata moltiplicando la direzione della sorgente di luce per la matrice di visualizzazione, normalizzando e negando il risultato.

L<sub>dir</sub> =-Norm (L<sub>dir</sub> \* wvMatrix)

Per il \_ punto di D3DLIGHT e D3DLIGHT, \_ la direzione verso la luce viene calcolata nel modo seguente:

L<sub>dir</sub> = Norm (V \* LP), in cui i parametri sono definiti nella tabella seguente.



| Parametro       | Valore predefinito | Tipo      | Descrizione                                               |
|-----------------|---------------|-----------|-----------------------------------------------------------|
| <sub>Dir</sub> | N/D           | D3DVECTOR | Vettore direzione dal vertice dell'oggetto alla luce          |
| V               | N/D           | D3DVECTOR | Posizione vertice nello spazio della fotocamera                           |
| wvMatrix        | Identità      | D3DMATRIX | Matrice composita contenente le trasformazioni globali e di visualizzazione |
| N               | N/D           | D3DVECTOR | Normale vertice                                             |
| LP              | N/D           | D3DVECTOR | Posizione chiara nello spazio della fotocamera                            |
| vMatrix         | Identità      | D3DMATRIX | Matrice contenente la trasformazione visualizzazione                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Matematica dell'illuminazione](mathematics-of-lighting.md)
</dt> </dl>

 

 



