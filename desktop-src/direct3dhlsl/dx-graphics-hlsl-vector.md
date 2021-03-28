---
title: Tipo Vector (HLSL)
description: Un vettore contiene tra uno e quattro componenti scalari; ogni componente di un vettore deve essere dello stesso tipo.
ms.assetid: 16e66f3c-c513-4d03-8adf-463dc8d83e12
keywords:
- Vettore di tipo HLSL
topic_type:
- apiref
api_name:
- Vector Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76d07da5d22dfb44215f70a7620d6519b5c8a802
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "104995261"
---
# <a name="vector-type"></a>Tipo di vettore

Un vettore contiene tra uno e quattro componenti scalari; ogni componente di un vettore deve essere dello stesso tipo.



|                     |
|---------------------|
| **Nome TypeNumber** |



 


```
TypeComponents Name
```



## <a name="components"></a>Componenti



| Elemento                                                                                                                             | Descrizione                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TypeComponents"></span><span id="typecomponents"></span><span id="TYPECOMPONENTS"></span>**TypeComponents**<br/> | Nome singolo che contiene due parti. La prima parte è uno dei tipi [scalari](dx-graphics-hlsl-data-types.md) . La seconda parte è il numero di componenti, che deve essere compreso tra 1 e 4 inclusi.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**<br/>                                         | Stringa ASCII che identifica in modo univoco il nome della variabile.<br/>                                                                                                                                                |



 

## <a name="examples"></a>Esempio

Ecco alcuni esempi:


```
bool    bVector;   // scalar containing 1 Boolean
int1    iVector = 1;
float3  fVector = { 0.2f, 0.3f, 0.4f };
```



Un vettore può essere dichiarato utilizzando anche questa sintassi:


```
vector <Type, Number> VariableName
```



Ecco alcuni esempi:


```
vector <int,    1> iVector = 1;
vector <double, 4> dVector = { 0.2, 0.3, 0.4, 0.5 };
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Tipi di dati (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





