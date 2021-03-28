---
title: Tipo matrice
description: Una matrice è un tipo di dati speciale che contiene tra uno e sedici componenti. Ogni componente di una matrice deve essere dello stesso tipo.
ms.assetid: 728eb472-103d-4c7f-b6f6-e515fc024801
keywords:
- Tipo matrice HLSL
topic_type:
- apiref
api_name:
- Matrix Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c580706a2ddae3e4a94c138a1ca0f6932457732a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045524"
---
# <a name="matrix-type"></a>Tipo matrice

Una matrice è un tipo di dati speciale che contiene tra uno e sedici componenti. Ogni componente di una matrice deve essere dello stesso tipo.



|                         |
|-------------------------|
| **Nome TypeComponents** |



 

## <a name="components"></a>Componenti



| Elemento                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**<br/> | Nome singolo che contiene tre parti. La prima parte è uno dei tipi [scalari](dx-graphics-hlsl-data-types.md) . La seconda parte è il numero di righe. La terza parte è il numero di colonne. Il numero di righe e colonne è un numero intero positivo compreso tra 1 e 4.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**<br/>                                         | Stringa ASCII che identifica in modo univoco il nome della variabile.<br/>                                                                                                                                                                                                                            |



 

## <a name="examples"></a>Esempio

Ecco alcuni esempi:


```
int1x1    iMatrix;   // integer matrix with 1 row,  1 column
int4x1    iMatrix;   // integer matrix with 4 rows, 1 column
int1x4    iMatrix;   // integer matrix with 1 row, 4 columns
double3x3 dMatrix;   // double matrix with 3 rows, 3 columns

float2x2 fMatrix = { 0.0f, 0.1, // row 1
                     2.1f, 2.2f // row 2
                   };   
```



Una matrice può essere dichiarata utilizzando anche questa sintassi:


```
matrix <Type, Number> VariableName
```



Il tipo di matrice utilizza le parentesi acute per specificare il tipo, il numero di righe e il numero di colonne. In questo esempio viene creata una matrice a virgola mobile, con due righe e due colonne. È possibile utilizzare qualsiasi tipo di dati scalari.

Ecco un esempio:


```
matrix <float, 2, 2> fMatrix = { 0.0f, 0.1, // row 1
                                 2.1f, 2.2f // row 2
                               };
```



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





