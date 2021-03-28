---
title: mul
description: Moltiplica x e y con la matematica della matrice. Le colonne x e y della dimensione interna devono essere uguali.
ms.assetid: 9945388a-d802-4dbe-bdb7-4eadb8751c39
keywords:
- HLSL mul
topic_type:
- apiref
api_name:
- mul
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2e9fe545cb16f8ac1fef1935b9d7e97075521b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045522"
---
# <a name="mul"></a>mul

Moltiplica x e y con la matematica della matrice. Le colonne x e y della dimensione interna devono essere uguali.



| Mul RET (x, y) |
|---------------|



 

## <a name="parameters"></a>Parametri



| Elemento                                                   | Descrizione                                                                           |
|--------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[nel \] valore di input x. Se x è un vettore, viene considerato come un vettore di riga.<br/>    |
| <span id="y"></span><span id="Y"></span>*y*<br/> | \[nel \] valore di input y. Se y è un vettore, viene trattato come un vettore di colonna.<br/> |



 

## <a name="return-value"></a>Valore restituito

Risultato di x volte y. Il risultato contiene le colonne x-Rows x y.

## <a name="type-description"></a>Descrizione del tipo

Sono disponibili 9 versioni di overload di questa funzione; le versioni di overload gestiscono i diversi casi per i tipi e le dimensioni degli argomenti di input.



| Versione | Nome | Scopo | [**Tipo di modello**](dx-graphics-hlsl-intrinsic-functions.md) | [**Tipo di componente**](dx-graphics-hlsl-intrinsic-functions.md) | Dimensione                                                                     |
|---------|------|---------|---------------------------------------------------------------|----------------------------------------------------------------|--------------------------------------------------------------------------|
| 1       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in ingresso      | scalare                                                        | float, int                                                     | 1                                                                        |
|         | y    | in ingresso      | scalare                                                        | uguale all'input x                                                | 1                                                                        |
|         | RET  | in uscita     | scalare                                                        | uguale all'input x                                                | 1                                                                        |
| 2       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in ingresso      | scalare                                                        | float, int                                                     | 1                                                                        |
|         | y    | in ingresso      | vettore                                                        | float, int                                                     | any                                                                      |
|         | RET  | in uscita     | vettore                                                        | float, int                                                     | le stesse dimensioni di input y                                             |
| 3       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in ingresso      | scalare                                                        | float, int                                                     | 1                                                                        |
|         | y    | in ingresso      | matrix                                                        | float, int                                                     | any                                                                      |
|         | RET  | in uscita     | matrix                                                        | uguale all'input y                                                | le stesse dimensioni di input y                                             |
| 4       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in ingresso      | vettore                                                        | float, int                                                     | any                                                                      |
|         | y    | in ingresso      | scalare                                                        | float, int                                                     | 1                                                                        |
|         | RET  | in uscita     | vettore                                                        | float, int                                                     | le stesse dimensioni di input x                                             |
| 5       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in ingresso      | vettore                                                        | float, int                                                     | any                                                                      |
|         | y    | in ingresso      | vettore                                                        | float, int                                                     | le stesse dimensioni di input x                                             |
|         | RET  | in uscita     | scalare                                                        | float, int                                                     | 1                                                                        |
| 6       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in ingresso      | vettore                                                        | float, int                                                     | any                                                                      |
|         | y    | in ingresso      | matrix                                                        | float, int                                                     | righe = stesse dimensioni come input x, colonne = any                       |
|         | RET  | in uscita     | vettore                                                        | float, int                                                     | le stesse dimensioni delle colonne di input y                                     |
| 7       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in ingresso      | matrix                                                        | float, int                                                     | any                                                                      |
|         | y    | in ingresso      | scalare                                                        | float, int                                                     | 1                                                                        |
|         | RET  | in uscita     | matrix                                                        | float, int                                                     | le stesse dimensioni di input x                                             |
| 8       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in ingresso      | matrix                                                        | float, int                                                     | any                                                                      |
|         | y    | in ingresso      | vettore                                                        | float, int                                                     | numero di colonne nell'input x                                             |
|         | RET  | in uscita     | vettore                                                        | float, int                                                     | numero di righe nell'input x                                                |
| 9       |      |         |                                                               |                                                                |                                                                          |
|         | x    | in ingresso      | matrix                                                        | float, int                                                     | any                                                                      |
|         | y    | in ingresso      | matrix                                                        | float, int                                                     | Rows = numero di colonne nell'input x                                      |
|         | RET  | in uscita     | matrix                                                        | float, int                                                     | Rows = numero di righe nell'input x, colonne = numero di colonne nell'input y |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                                                       | Supportato |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) e modelli shader più elevati | sì       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni intrinseche (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





