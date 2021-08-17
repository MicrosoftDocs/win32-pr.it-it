---
description: Elenca le funzioni aritmetiche dei vettori.
ms.assetid: d7ed4516-74a6-81ec-79a2-2e39cf112d11
title: Funzioni aritmetiche vettoriali
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 783e60ad3ca17b7394fc801baaeedd61d89649b2f4ae5ccd3b3fa7e774ff6a4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118500351"
---
# <a name="vector-arithmetic-functions"></a>Funzioni aritmetiche vettoriali

Elenca le funzioni aritmetiche dei vettori.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                   | Descrizione                                                                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**XMVectorAbs**](/windows/win32/api/directxmath/nf-directxmath-xmvectorabs)<br/>                                           | Calcola il valore assoluto di ogni componente di [**un oggetto XMVECTOR.**](xmvector-data-type.md)<br/>                    |
| [**XMVectorAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)<br/>                                           | Calcola la somma di due vettori.<br/>                                                                               |
| [**XMVectorAddAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectoraddangles)<br/>                               | Aggiunge due vettori che rappresentano gli angoli.<br/>                                                                          |
| [**XMVectorCeiling**](/windows/win32/api/directxmath/nf-directxmath-xmvectorceiling)<br/>                                   | Calcola il limite massimo di ogni componente di [**un oggetto XMVECTOR.**](xmvector-data-type.md)<br/>                           |
| [**XMVectorClamp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorclamp)<br/>                                       | Stringe i componenti di un vettore a un intervallo minimo e massimo specificato.<br/>                                    |
| [**XMVectorDivide**](/windows/win32/api/directxmath/nf-directxmath-xmvectordivide)<br/>                                     | Divide un'istanza di `XMVECTOR` per una seconda istanza, restituisce il risultato in una terza istanza.<br/>             |
| [**XMVectorFloor**](/windows/win32/api/directxmath/nf-directxmath-xmvectorfloor)<br/>                                       | Calcola il piano di ogni componente di [**un oggetto XMVECTOR.**](xmvector-data-type.md)<br/>                             |
| [**XMVectorIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisinfinite)<br/>                             | Esegue un test per componente per +/- infinito su un vettore.<br/>                                                    |
| [**XMVectorIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmvectorisnan)<br/>                                       | Esegue un test NaN per componente su un vettore.<br/>                                                                 |
| [**XMVectorMax**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)<br/>                                           | Esegue un confronto per componente tra due vettori e restituisce un vettore contenente i componenti più grandi.<br/>  |
| [**XMVectorMin**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)<br/>                                           | Esegue un confronto per componente tra due vettori e restituisce un vettore contenente i componenti più piccoli.<br/> |
| [**XMVectorMod**](/windows/win32/api/directxmath/nf-directxmath-xmvectormod)<br/>                                           | Calcola il resto a virgola mobile per componente del quoziente di due vettori.<br/>                            |
| [**XMVectorModAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectormodangles)<br/>                               | Calcola l'angolo per componente modulo 2PI.<br/>                                                                   |
| [**XMVectorMultiply**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiply)<br/>                                 | Calcola il prodotto per componente di due vettori.<br/>                                                             |
| [**XMVectorMultiplyAdd**](/windows/win32/api/directxmath/nf-directxmath-xmvectormultiplyadd)<br/>                           | Calcola il prodotto dei primi due vettori aggiunti al terzo vettore.<br/>                                       |
| [**XMVectorNegate**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegate)<br/>                                     | Calcola la negazione di un vettore.<br/>                                                                             |
| [**XMVectorNegativeMultiplySubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectornegativemultiplysubtract)<br/> | Calcola la differenza di un terzo vettore e del prodotto dei primi due vettori.<br/>                            |
| [**XMVectorPow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)<br/>                                           | Calcola *V1* elevato alla potenza della *versione 2.*<br/>                                                                     |
| [**XMVectorReciprocal**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocal)<br/>                             | Calcola il reciproco per componente di un vettore.<br/>                                                             |
| [**XMVectorReciprocalEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalest)<br/>                       | Stima il reciproco per componente di un vettore.<br/>                                                            |
| [**XMVectorReciprocalSqrt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrt)<br/>                     | Calcola la radice quadrata reciproca per componente di un vettore.<br/>                                                 |
| [**XMVectorReciprocalSqrtEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreciprocalsqrtest)<br/>               | Stima la radice quadrata reciproca per componente di un vettore.<br/>                                                |
| [**XMVectorRound**](/windows/win32/api/directxmath/nf-directxmath-xmvectorround)<br/>                                       | Arrotonda ogni componente di un vettore all'intero più vicino.<br/>                                                      |
| [**XMVectorSaturate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsaturate)<br/>                                 | Satura ogni componente di un vettore nell'intervallo da 0,0f a 1,0f.<br/>                                                |
| [**XMVectorScale**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)<br/>                                       | Scalare moltiplica un vettore per un valore a virgola mobile.<br/>                                                          |
| [**XMVectorSqrt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrt)<br/>                                         | Calcola la radice quadrata per componente di un vettore.<br/>                                                            |
| [**XMVectorSqrtEst**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsqrtest)<br/>                                   | Stima la radice quadrata per componente di un vettore.<br/>                                                           |
| [**XMVectorSubtract**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)<br/>                                 | Calcola la differenza di due vettori.<br/>                                                                        |
| [**XMVectorSubtractAngles**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtractangles)<br/>                     | Sottrae due vettori che rappresentano gli angoli.<br/>                                                                     |
| [**XMVectorSum**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsum)<br/>                                           | Calcola la somma orizzontale dei componenti di [**un oggetto XMVECTOR.**](xmvector-data-type.md)<br/>                    |
| [**XMVectorTruncate**](/windows/win32/api/directxmath/nf-directxmath-xmvectortruncate)<br/>                                 | Arrotonda ogni componente di un vettore al valore intero più vicino nella direzione di zero.<br/>                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni vettoriali della libreria DirectXMath](ovw-xnamath-reference-functions-vector.md)
</dt> </dl>

 

 
