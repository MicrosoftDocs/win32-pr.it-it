---
description: Curve parametro
ms.assetid: c073e7d0-c119-4c36-a5b2-b31dd6326ac8
title: Curve parametro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c482112c8bd76217f5cbdabdf3cda13b09c3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125016"
---
# <a name="parameter-curves"></a>Curve parametro

I parametri del supporto sono in grado di seguire una curva nel tempo. Ogni curva è descritta da una formula matematica e da due punti finali. Ogni endpoint è definito da un'ora di riferimento e dal valore della curva in quel momento. La formula viene utilizzata per calcolare i valori intermedi tra i punti e determina la forma della curva. Le curve possibili sono:

-   Saltare
-   Lineari
-   Square
-   Quadrato inverso
-   Seno

"Jump" significa passare direttamente al valore finale. Le altre curve sono illustrate nella figura seguente.

![curve parametro](images/param-curves01.png)

In matematica, le curve funzionano come segue. Si supponga che una curva inizi all'ora *t*₀ con il valore *v*₀ e termini al momento *t*₁ con il valore *v*₁. I due punti che definiscono la curva sono (*t*₀, *v*₀) e (*t*₁, *v*₁).

-   Consentire a Δ *t* di essere la durata totale della curva, *t*₁ –*t*₀.
-   Consentire a Δ *v* di essere l'intervallo tra i valori iniziale e finale, *v*₁ –*v*₀.
-   In qualsiasi momento *t* tale che *t*₀ <= *t*  <=  *t*₁, Let Δ *t'*= *t*–*t*₀.

![calcolo parametri](images/param-curves02.png)

Il valore del parametro all'ora *t* è:

*v* = f (δ *t*'/δ *t* ) \* Δ *v*  +  *v*₀

dove f (x) è una funzione determinata dal tipo di curva:

-   Lineare: y = x
-   Quadrato: y = x ^ 2
-   Quadrato inverso: y = sqrt (x)
-   Seno: y = \[ sin (πx-π/2) + 1 \] /2

Osservare che Δ *t'*< δ *t*, quindi il termine δ *t*'/δ *t* è compreso tra 0 e 1. F (x), quindi, è compreso tra 0 e 1 e *v* è sempre compreso tra *v*₀ e *v*₁. Questo vale se *v*₀ < *v*₁ o viceversa. In altre parole, la curva è vincolata dal rettangolo (*t*₀, *v*₀, *t*₁, *v*₁).

Per la curva seno, il valore di (πx-π/2) è compreso tra-π/2 e π/2, il che significa che sin (πx-π/2) è compreso tra-1 e 1. Il risultato viene quindi normalizzato in modo che f (x) rientri nell'intervallo (0-1).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Parametri dei supporti](media-parameters.md)
</dt> </dl>

 

 



