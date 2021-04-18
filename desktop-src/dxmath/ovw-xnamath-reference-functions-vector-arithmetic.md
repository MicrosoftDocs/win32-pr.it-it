---
description: Elenca le funzioni aritmetiche del vettore.
ms.assetid: d7ed4516-74a6-81ec-79a2-2e39cf112d11
title: Funzioni aritmetiche Vector
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ad5149153b736ddf6d2f2af5b9671e32651f86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309286"
---
# <a name="vector-arithmetic-functions"></a>Funzioni aritmetiche Vector

Elenca le funzioni aritmetiche del vettore.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                   | Descrizione                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**XMVectorAbs**](/windows/win32/api/directxmath/nf-directxmath-xmvectorabs)<br/>                                           | Calcola il valore assoluto di ogni componente di un [**XMVECTOR**](xmvector-data-type.md).<br/>                    |
| [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)<br/>                                           | Calcola la somma di due vettori.<br/>                                                                               |
| [**XMVectorAddAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectoraddangles)<br/>                               | Aggiunge due vettori che rappresentano gli angoli.<br/>                                                                          |
| [**XMVectorCeiling**](/windows/win32/api/directxmath/nf-directxmath-xmvectorceiling)<br/>                                   | Calcola il limite massimo di ogni componente di un [**XMVECTOR**](xmvector-data-type.md).<br/>                           |
| [**XMVectorClamp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorclamp)<br/>                                       | Blocca i componenti di un vettore a un intervallo minimo e massimo specificato.<br/>                                    |
| [**XMVectorDivide**](/windows/win32/api/directxmath/nf-directxmath-xmvectordivide)<br/>                                     | Divide un'istanza di `XMVECTOR` per una seconda istanza, restituendo il risultato in una terza istanza.<br/>             |
| [**XMVectorFloor**](/windows/win32/api/directxmath/nf-directxmath-xmvectorfloor)<br/>                                       | Calcola il piano di ogni componente di un [**XMVECTOR**](xmvector-data-type.md).<br/>                             |
| [**XMVectorIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisinfinite)<br/>                             | Esegue un test per componente per l'infinito di +/-in un vettore.<br/>                                                    |
| [**XMVectorIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisnan)<br/>                                       | Esegue un test NaN per componente in un vettore.<br/>                                                                 |
| [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)<br/>                                           | Esegue un confronto per componente tra due vettori e restituisce un vettore contenente i componenti più grandi.<br/>  |
| [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)<br/>                                           | Esegue un confronto per componente tra due vettori e restituisce un vettore contenente i componenti più piccoli.<br/> |
| [**XMVectorMod**](/windows/win32/api/directxmath/nf-directxmath-xmvectormod)<br/>                                           | Calcola il resto a virgola mobile per componente del quoziente di due vettori.<br/>                            |
| [**XMVectorModAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectormodangles)<br/>                               | Calcola il modulo angolo per componente 2 Π.<br/>                                                                   |
| [**XMVectorMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiply)<br/>                                 | Calcola il prodotto per componente di due vettori.<br/>                                                             |
| [**XMVectorMultiplyAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiplyadd)<br/>                           | Calcola il prodotto dei primi due vettori aggiunti al terzo vettore.<br/>                                       |
| [**XMVectorNegate**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegate)<br/>                                     | Calcola la negazione di un vettore.<br/>                                                                             |
| [**XMVectorNegativeMultiplySubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegativemultiplysubtract)<br/> | Calcola la differenza tra un terzo vettore e il prodotto dei primi due vettori.<br/>                            |
| [**XMVectorPow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)<br/>                                           | Calcolo *V1* elevato alla potenza di *v2*.<br/>                                                                     |
| [**XMVectorReciprocal**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocal)<br/>                             | Calcola il reciproco per componente di un vettore.<br/>                                                             |
| [**XMVectorReciprocalEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalest)<br/>                       | Stima il reciproco per componente di un vettore.<br/>                                                            |
| [**XMVectorReciprocalSqrt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrt)<br/>                     | Calcola la radice quadrata reciproca per componente di un vettore.<br/>                                                 |
| [**XMVectorReciprocalSqrtEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrtest)<br/>               | Stima la radice quadrata reciproca per componente di un vettore.<br/>                                                |
| [**XMVectorRound**](/windows/win32/api/directxmath/nf-directxmath-xmvectorround)<br/>                                       | Arrotonda ogni componente di un vettore all'intero più vicino.<br/>                                                      |
| [**XMVectorSaturate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsaturate)<br/>                                 | Satura ogni componente di un vettore nell'intervallo 0,0 f a 1,0 f.<br/>                                                |
| [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)<br/>                                       | Scalar moltiplica un vettore per un valore a virgola mobile.<br/>                                                          |
| [**XMVectorSqrt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrt)<br/>                                         | Calcola la radice quadrata per componente di un vettore.<br/>                                                            |
| [**XMVectorSqrtEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrtest)<br/>                                   | Stima la radice quadrata per componente di un vettore.<br/>                                                           |
| [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)<br/>                                 | Calcola la differenza tra due vettori.<br/>                                                                        |
| [**XMVectorSubtractAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtractangles)<br/>                     | Sottrae due vettori che rappresentano gli angoli.<br/>                                                                     |
| [**XMVectorSum**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsum)<br/>                                           | Calcola la somma orizzontale dei componenti di un [**XMVECTOR**](xmvector-data-type.md).<br/>                    |
| [**XMVectorTruncate**](/windows/win32/api/directxmath/nf-directxmath-xmvectortruncate)<br/>                                 | Arrotonda ogni componente di un vettore al valore intero più vicino nella direzione di zero.<br/>                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni Vector della libreria DirectXMath](ovw-xnamath-reference-functions-vector.md)
</dt> </dl>

 

 
