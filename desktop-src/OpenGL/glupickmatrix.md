---
title: funzione gluPickMatrix (Glu. h)
description: La funzione gluPickMatrix definisce un'area di selezione.
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
keywords:
- funzione gluPickMatrix OpenGL
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
ms.openlocfilehash: c54e62f82f52fedc7de7c7c4af1cd3ed1ccdf149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963733"
---
# <a name="glupickmatrix-function"></a>gluPickMatrix (funzione)

La funzione **gluPickMatrix** definisce un'area di selezione.

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

*Viewport* 
</dt> <dd>

Viewport corrente (come da una chiamata [**glGetIntegerv**](glgetintegerv.md) ).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluPickMatrix** crea una matrice di proiezione che è possibile usare per limitare il disegno a una piccola area del viewport.

1.  Usare **gluPickMatrix** per limitare il disegno a una piccola area attorno al cursore.
2.  Immettere la modalità di selezione (con [**glRenderMode**](glrendermode.md)) e quindi eseguire nuovamente il rendering della scena.

    Tutte le primitive che sarebbero state disegnate accanto al cursore vengono identificate e archiviate nel buffer di selezione.

La matrice creata da **gluPickMatrix** viene moltiplicata per la matrice corrente esattamente come se [**glMultMatrix**](glmultmatrix.md) venisse chiamato con la matrice generata.

1.  Chiamare [**glLoadIdentity**](glloadidentity.md) per caricare una matrice di identità nello stack della matrice della prospettiva.
2.  Chiamare **gluPickMatrix**.
3.  Chiamare una funzione (ad esempio [**gluPerspective**](gluperspective.md)) per moltiplicare la matrice della prospettiva per la matrice di selezione.

Quando si usa **gluPickMatrix** per selezionare una spline B-spline razionale non uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)), prestare attenzione a disattivare la proprietà NURBS, Glu \_ auto \_ Load \_ Matrix. Se \_ \_ la matrice di caricamento automatico Glu non è disattivata \_ , qualsiasi superficie NURBS sottoposta a rendering viene suddivisa in modo diverso rispetto alla matrice di selezione rispetto alla relativa suddivisione senza la matrice di selezione.

## <a name="examples"></a>Esempio

Quando si esegue il rendering di una scena come segue:


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



il codice seguente seleziona una parte del viewport:


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
| Intestazione<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
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

 

 





