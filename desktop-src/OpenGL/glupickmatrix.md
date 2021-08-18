---
title: Funzione gluPickMatrix (Glu.h)
description: La funzione gluPickMatrix definisce un'area di selezione.
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
keywords:
- Funzione gluPickMatrix OpenGL
topic_type:
- apiref
api_name:
- gluPickMatrix
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 394e10c460b406e510b1423f299b4a8724492f5a5b180212ff121f4ad593041e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061579"
---
# <a name="glupickmatrix-function"></a>Funzione gluPickMatrix

La **funzione gluPickMatrix** definisce un'area di selezione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluPickMatrix(
   GLdouble x,
   GLdouble y,
   GLdouble height,
   GLdouble width,
   GLint    viewport[4]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*x* 
</dt> <dd>

Coordinata x della finestra di un'area di selezione.

</dd> <dt>

*y* 
</dt> <dd>

Coordinata della finestra y di un'area di selezione.

</dd> <dt>

*height* 
</dt> <dd>

Altezza dell'area di selezione nelle coordinate della finestra.

</dd> <dt>

*width* 
</dt> <dd>

Larghezza dell'area di selezione nelle coordinate della finestra.

</dd> <dt>

*Finestra* 
</dt> <dd>

Viewport corrente (come da una [**chiamata glGetIntegerv).**](glgetintegerv.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluPickMatrix** crea una matrice di proiezione che è possibile usare per limitare il disegno a una piccola area del viewport.

1.  Usare **gluPickMatrix** per limitare il disegno a una piccola area intorno al cursore.
2.  Immettere la modalità di selezione [**(con glRenderMode**](glrendermode.md)) e quindi eseguire nuovamente il rerender della scena.

    Tutte le primitive disegnate vicino al cursore vengono identificate e archiviate nel buffer di selezione.

La matrice creata da **gluPickMatrix** viene moltiplicata per la matrice corrente come se [**glMultMatrix**](glmultmatrix.md) fosse chiamato con la matrice generata.

1.  Chiamare [**glLoadIdentity**](glloadidentity.md) per caricare una matrice di identità nello stack della matrice prospettica.
2.  Chiamare **gluPickMatrix**.
3.  Chiamare una funzione ( ad esempio [**gluPerspective**](gluperspective.md)) per moltiplicare la matrice prospettica per la matrice di selezione.

Quando si **usa gluPickMatrix** per selezionare B-Spline razionale non uniforme [(NURBS),](using-nurbs-curves-and-surfaces.md)prestare attenzione a disattivare la proprietà NURBS GLU \_ AUTO LOAD \_ \_ MATRIX. Se GLU AUTO LOAD MATRIX non è disattivato, qualsiasi superficie NURBS sottoposta a rendering viene suddivisa in modo diverso con la matrice di selezione da come è stata suddivisa senza la matrice \_ \_ di \_ selezione.

## <a name="examples"></a>Esempio

Quando si esegue il rendering di una scena, seguire questa procedura:


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



Il codice seguente seleziona una parte del viewport:


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPickMatrix(x, y, width, height, viewport);  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



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

[**glGetIntegerv**](glgetintegerv.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





