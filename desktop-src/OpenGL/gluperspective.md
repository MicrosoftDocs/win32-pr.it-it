---
title: Funzione gluPerspective (Glu.h)
description: La funzione gluPerspective imposta una matrice di proiezione prospettica.
ms.assetid: 125e2828-a2d7-4c6c-9370-eb21a581ced8
keywords:
- Funzione gluPerspective OpenGL
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
ms.openlocfilehash: 973040fc9d9f23e6cfba5e30ceea89a1c13cfbaab0071cc7905080cfcdf60f12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061589"
---
# <a name="gluperspective-function"></a>Funzione gluPerspective

La **funzione gluPerspective** imposta una matrice di proiezione prospettica.

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

Angolo del campo di visualizzazione, in gradi, nella direzione y.

</dd> <dt>

*aspect* 
</dt> <dd>

Proporzioni che determinano il campo di visualizzazione nella direzione x. Le proporzioni sono il rapporto *tra x* (larghezza) *e y* (altezza).

</dd> <dt>

*zNear* 
</dt> <dd>

Distanza dal visualizzatore al piano di ritaglio vicino (sempre positivo).

</dd> <dt>

*zFar* 
</dt> <dd>

Distanza dal visualizzatore al piano di ritaglio lontano (sempre positivo).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluPerspective** specifica un frustum di visualizzazione nel sistema di coordinate del mondo. In generale, le proporzioni in **gluPerspective** devono corrispondere alle proporzioni del viewport associato. Ad esempio, *aspect* = 2.0 indica che l'angolo di visualizzazione del visualizzatore è due volte più ampio in *x* rispetto a *y*. Se il viewport è il doppio di quello alto, visualizza l'immagine senza distorsione.

La matrice generata **da gluPerspective** viene moltiplicata per la matrice corrente, proprio come se [**glMultMatrix**](glmultmatrix.md) fosse chiamato con la matrice generata. Per caricare invece la matrice prospettica nello stack di matrici corrente, precedere la chiamata a **gluPerspective** con una chiamata a [**glLoadIdentity**](glloadidentity.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
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

 

 





