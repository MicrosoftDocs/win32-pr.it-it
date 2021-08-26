---
description: Curve dei parametri
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: Curve dei parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5130cf158271ffe3cb3da5e4e16b5fffa8a5a6994b14b9f8766fe20cdf1510ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997383"
---
# <a name="parameter-curves"></a>Curve dei parametri

I parametri multimediali possono seguire una curva nel tempo. Ogni curva è descritta da una formula matematica e da due punti finali. Ogni punto finale è definito da un'ora di riferimento e dal valore della curva in quel momento. La formula viene usata per calcolare i valori intermedi tra i punti e determina la forma della curva. Le curve possibili sono:

-   Saltare
-   Lineari
-   Square
-   Quadrato inverso
-   Seno

"Jump" significa passare direttamente al valore finale. Le altre curve sono illustrate nel diagramma seguente.

![curve dei parametri](images/param-curves01.png)

Matematicamente, le curve funzionano come segue. Si supponga che una curva inizi in ₀ t con un valore di  *v*₀ e termini in corrispondenza del ₁ con un valore *di v*₁. I due punti che definiscono la curva sono (*t*₀, *v*₀) e (*t ₁,* *v*₁).

-   Si Δ *che sia* la durata totale della curva, *t ₁-**t ₀.*
-   Si Δ *v sia* l'intervallo tra i valori iniziale e finale, *v ₁-**v ₀.*
-   In qualsiasi momento *t in* modo che *t ₀ <*= t *t*  <=  *₁,* Δ *t*' = *t*–*t ₀.*

![calcolo dei parametri](images/param-curves02.png)

Il valore del parametro al momento *t* è:

*v* = f( Δ *t*' / Δ *t* ) Δ \* *v*  +  *v*₀

dove f(x) è una funzione determinata dal tipo di curva:

-   Lineare: y = x
-   Quadrato: y = x^2
-   Quadrato inverso: y = sqrt(x)
-   Seno: y = \[ sin(πx – π/2) + \] 1/2

Osservare che Δ *t*' < Δ *t*, quindi il termine Δ *t*'/Δ *t* è compreso tra 0 e 1. Pertanto, anche f(x) è compreso tra 0 e 1 e *v* è sempre compreso tra *v*₀ *e v*₁. Questo vale se *v ₀ <* *v ₁* o viceversa. In altre parole, la curva è delimitata dal rettangolo (*t*₀, *v*₀, *t ₁,* *v*₁).

Per la curva sinone, il valore di (πx - π/2) è compreso tra -π/2 e π/2, il che significa che sin(πx – π/2) è compreso tra -1 e 1. Il risultato viene quindi normalizzato in modo che f(x) sia compreso nell'intervallo (0-1).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Parametri dei supporti](media-parameters.md)
</dt> </dl>

 

 



