---
description: I vertici nello spazio della fotocamera vengono calcolati trasformando i vertici dell'oggetto con la matrice di visualizzazione globale.
ms.assetid: 889dd0d8-1933-4901-9bbc-06c3caa26d3e
title: Trasformazioni dello spazio della fotocamera (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: effb7af72decad711d9fc392e53f7aba05f48b3c69394dbfb3ae5f9f06e2def7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241851"
---
# <a name="camera-space-transformations-direct3d-9"></a>Trasformazioni dello spazio della fotocamera (Direct3D 9)

I vertici nello spazio della fotocamera vengono calcolati trasformando i vertici dell'oggetto con la matrice di visualizzazione globale.

V = V \* wvMatrix

Le normali dei vertici, nello spazio della fotocamera, vengono calcolate trasformando le normali dell'oggetto con il trasposto inverso della matrice di visualizzazione globale. La matrice di visualizzazione globale può essere o meno ortogonale.

N = N \* (wvMatrix⁻¹)<sup>T</sup>

L'inversione della matrice e la trasposizione della matrice operano su una matrice 4x4. La moltiplicazione combina la normale con la parte 3x3 della matrice 4x4 risultante.

Se lo stato di rendering, D3DRENDERSTATE NORMALIZENORMALS è impostato su TRUE, i vettori normali dei vertici vengono normalizzati dopo la trasformazione nello spazio della fotocamera come \_ indicato di seguito: 

N = norm(N)

La posizione della luce nello spazio della fotocamera viene calcolata trasformando la posizione della sorgente di luce con la matrice di visualizzazione.

Lp = Lp \* vMatrix

La direzione della luce nello spazio della fotocamera per una luce direzionale viene calcolata moltiplicando la direzione della sorgente di luce per la matrice di visualizzazione, normalizzando e negando il risultato.

L<sub>dir</sub> = -norm(L<sub>dir</sub> \* wvMatrix)

Per D3DLIGHT POINT e D3DLIGHT SPOT la direzione verso la luce viene \_ \_ calcolata nel modo seguente:

L<sub>dir</sub> = norm(V \* Lp), dove i parametri sono definiti nella tabella seguente.



| Parametro       | Valore predefinito | Tipo      | Descrizione                                               |
|-----------------|---------------|-----------|-----------------------------------------------------------|
| L<sub>dir</sub> | N/A           | D3DVECTOR | Vettore di direzione dal vertice dell'oggetto alla luce          |
| V               | N/A           | D3DVECTOR | Posizione dei vertici nello spazio della fotocamera                           |
| wvMatrix        | Identità      | D3DMATRIX | Matrice composita contenente le trasformazioni world e view |
| N               | N/A           | D3DVECTOR | Normale vertice                                             |
| Lp              | N/A           | D3DVECTOR | Posizione della luce nello spazio della fotocamera                            |
| vMatrix         | Identità      | D3DMATRIX | Matrice contenente la trasformazione della visualizzazione                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Matematica dell'illuminazione](mathematics-of-lighting.md)
</dt> </dl>

 

 



