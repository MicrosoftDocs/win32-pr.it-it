---
title: mul
description: Moltiplica x e y usando la matematica della matrice. Le colonne x e y della dimensione interna devono essere uguali.
ms.assetid: 9945388a-d802-4dbe-bdb7-4eadb8751c39
keywords:
- mul HLSL
topic_type:
- apiref
api_name:
- mul
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6362c734cbbf30defa8fed75f28c6f39397d75977488d9efc170d2647a9b3d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950361"
---
# <a name="mul"></a>mul

Moltiplica x e y usando la matematica della matrice. Le colonne x e y della dimensione interna devono essere uguali.



| ret mul(x, y) |
|---------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                                                           |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Valore di input x. Se x è un vettore, viene considerato come vettore di riga.<br/>    |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Valore di input y. Se y è un vettore, viene considerato come vettore di colonna.<br/> |



 

## <a name="return-value"></a>Valore restituito

Risultato di x x x y. Il risultato ha la dimensione x-rows x y-columns.

## <a name="type-description"></a>Descrizione del tipo

Esistono 9 versioni di overload di questa funzione. Le versioni di overload gestiscono i diversi case per i tipi e le dimensioni degli argomenti di input.



| Versione | Nome | Scopo | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md) | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                                                                     |
|---------|------|---------|---------------------------------------------------------------|----------------------------------------------------------------|--------------------------------------------------------------------------|
| 1       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | scalare                                                        | float, int                                                     | 1                                                                        |
|         | y    | in      | scalare                                                        | uguale all'input x                                                | 1                                                                        |
|         | Ret  | in uscita     | scalare                                                        | uguale all'input x                                                | 1                                                                        |
| 2       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | scalare                                                        | float, int                                                     | 1                                                                        |
|         | y    | in      | vettore                                                        | float, int                                                     | any                                                                      |
|         | Ret  | in uscita     | vettore                                                        | float, int                                                     | stesse dimensioni dell'input y                                             |
| 3       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | scalare                                                        | float, int                                                     | 1                                                                        |
|         | y    | in      | matrix                                                        | float, int                                                     | any                                                                      |
|         | Ret  | in uscita     | matrix                                                        | uguale all'input y                                                | stesse dimensioni dell'input y                                             |
| 4       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vettore                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | scalare                                                        | float, int                                                     | 1                                                                        |
|         | Ret  | in uscita     | vettore                                                        | float, int                                                     | stesse dimensioni dell'input x                                             |
| 5       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vettore                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | vettore                                                        | float, int                                                     | stesse dimensioni dell'input x                                             |
|         | Ret  | in uscita     | scalare                                                        | float, int                                                     | 1                                                                        |
| 6       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | vettore                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | matrix                                                        | float, int                                                     | rows = stesse dimensioni dell'input x, columns = any                       |
|         | Ret  | in uscita     | vettore                                                        | float, int                                                     | stesse dimensioni delle colonne di input y                                     |
| 7       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matrix                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | scalare                                                        | float, int                                                     | 1                                                                        |
|         | Ret  | in uscita     | matrix                                                        | float, int                                                     | stesse dimensioni dell'input x                                             |
| 8       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matrix                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | vettore                                                        | float, int                                                     | numero di colonne nell'input x                                             |
|         | Ret  | in uscita     | vettore                                                        | float, int                                                     | numero di righe nell'input x                                                |
| 9       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in      | matrix                                                        | float, int                                                     | any                                                                      |
|         | y    | in      | matrix                                                        | float, int                                                     | rows = numero di colonne nell'input x                                      |
|         | Ret  | in uscita     | matrix                                                        | float, int                                                     | rows = numero di righe nell'input x, columns = number of columns in input y |



 

## <a name="minimum-shader-model"></a>Modello shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelli shader superiori | sì       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





