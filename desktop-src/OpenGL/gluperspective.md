---
title: funzione gluPerspective (Glu. h)
description: La funzione gluPerspective imposta una matrice di proiezione prospettica.
ms.assetid: 125e2828-a2d7-4c6c-9370-eb21a581ced8
keywords:
- funzione gluPerspective OpenGL
topic_type:
- apiref
api_name:
- gluPerspective
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf30fc7dc4c6ba5a56efd3def6a5a7178f81ed49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400821"
---
# <a name="gluperspective-function"></a>gluPerspective (funzione)

La funzione **gluPerspective** imposta una matrice di proiezione prospettica.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluPerspective(
   GLdouble fovy,
   GLdouble aspect,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fovy* 
</dt> <dd>

Campo dell'angolo di visualizzazione, in gradi, nella direzione y.

</dd> <dt>

*aspect* 
</dt> <dd>

Proporzioni che determinano il campo di visualizzazione nella direzione x. La proporzioni è il rapporto tra *x* (width) e *y* (Height).

</dd> <dt>

*zNear* 
</dt> <dd>

Distanza dal visualizzatore al piano di ritaglio vicino (sempre positivo).

</dd> <dt>

*zFar* 
</dt> <dd>

Distanza tra il visualizzatore e il piano di ritaglio (sempre positivo).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluPerspective** specifica un tronco di visualizzazione nel sistema di coordinate globali. In generale, le proporzioni in **gluPerspective** devono corrispondere alle proporzioni del viewport associato. Ad esempio, *aspect* = 2,0 indica che l'angolo di visualizzazione del visualizzatore è due volte più ampio in *x* come si trova in *y*. Se il riquadro di visualizzazione è a larghezza doppia rispetto all'altezza, viene visualizzata l'immagine senza distorsione.

La matrice generata da **gluPerspective** viene moltiplicata per la matrice corrente, esattamente come se [**glMultMatrix**](glmultmatrix.md) venisse chiamato con la matrice generata. Per caricare la matrice della prospettiva nello stack della matrice corrente, anteporre al metodo la chiamata a **gluPerspective** con una chiamata a [**glLoadIdentity**](glloadidentity.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**gluOrtho2D**](gluortho2d.md)
</dt> </dl>

 

 





