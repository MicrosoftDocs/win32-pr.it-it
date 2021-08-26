---
description: Elenca le funzioni del piano fornite da DirectXMath.
ms.assetid: 6505e72e-4af5-5db3-4fc0-f83fa77692b1
title: Funzioni del piano della libreria DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a91e58ddad68c31bcc5579b2727891fdddd5b6737761c89d9db70ca21c56bfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841201"
---
# <a name="directxmath-library-plane-functions"></a>Funzioni del piano della libreria DirectXMath

Elenca le funzioni del piano fornite da DirectXMath.

Queste funzioni usano un vettore XMVECTOR a 4 per rappresentare i coefficienti dell'equazione del piano, Ax+By+Cz+D = 0, dove il componente X è A, il componente Y è B, il componente Z è C e il componente W è D.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                               | Descrizione                                                                                                      |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**XMPlaneDot**](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)<br/>                         | Calcola il prodotto punto tra un piano di input e un vettore 4D.<br/>                                    |
| [**XMPlaneDotCoord**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)<br/>               | Calcola il prodotto punto tra un piano di input e un vettore 3D.<br/>                                    |
| [**XMPlaneDotNormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)<br/>             | Calcola il prodotto del punto tra il vettore normale di un piano e un vettore 3D.<br/>                      |
| [**XMPlaneEqual**](/windows/win32/api/directxmath/nf-directxmath-xmplaneequal)<br/>                     | Determina se due piani sono uguali.<br/>                                                                   |
| [**XMPlaneFromPointNormal**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)<br/> | Calcola l'equazione di un piano costruito da un punto nel piano e da un vettore normale.<br/>           |
| [**XMPlaneFromPoints**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)<br/>           | Calcola l'equazione di un piano costruito da tre punti nel piano.<br/>                          |
| [**XMPlaneIntersectLine**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)<br/>     | Trova l'intersezione tra un piano e una linea.<br/>                                                    |
| [**XMPlaneIntersectPlane**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectplane)<br/>   | Trova l'intersezione di due piani.<br/>                                                                 |
| [**XMPlaneIsInfinite**](/windows/win32/api/directxmath/nf-directxmath-xmplaneisinfinite)<br/>           | Verifica se uno dei coefficienti di un piano è infinito positivo o negativo.<br/>                    |
| [**XMPlaneIsNaN**](/windows/win32/api/directxmath/nf-directxmath-xmplaneisnan)<br/>                     | Verifica se uno dei coefficienti di un piano è nan.<br/>                                            |
| [**XMPlaneNearEqual**](/windows/win32/api/directxmath/nf-directxmath-xmplanenearequal)<br/>             | Determina se due piani sono quasi uguali.<br/>                                                       |
| [**XMPlaneNormalize**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize)<br/>             | Normalizza i coefficienti di un piano in modo che i coefficienti di x, y e z formino un vettore normale unità.<br/> |
| [**XMPlaneNormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)<br/>       | Stima i coefficienti di un piano in modo che i coefficienti di x, y e z formino un vettore normale unità.<br/>  |
| [**XMPlaneNotEqual**](/windows/win32/api/directxmath/nf-directxmath-xmplanenotequal)<br/>               | Determina se due piani non sono uguali.<br/>                                                                 |
| [**XMPlaneTransform**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)<br/>             | Trasforma un piano in base a una matrice specificata.<br/>                                                                 |
| [**XMPlaneTransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)<br/> | Trasforma un flusso di piani in base a una determinata matrice.<br/>                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzioni della libreria DirectXMath](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
