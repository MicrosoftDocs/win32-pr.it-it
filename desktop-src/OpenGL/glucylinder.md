---
title: funzione gluCylinder (Glu. h)
description: La funzione gluCylinder disegna un cilindro.
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- funzione gluCylinder OpenGL
topic_type:
- apiref
api_name:
- gluCylinder
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fd201d1ddd720501715d1ead08d94bab72f7b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301918"
---
# <a name="glucylinder-function"></a>gluCylinder (funzione)

La funzione **gluCylinder** disegna un cilindro.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluCylinder(
   GLUquadric *qobj,
   GLdouble   baseRadius,
   GLdouble   topRadius,
   GLdouble   height,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*qobj* 
</dt> <dd>

Oggetto quadrica (creato con [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*baseRadius* 
</dt> <dd>

Raggio del cilindro a *z* = 0.

</dd> <dt>

*Raggio* 
</dt> <dd>

Raggio del cilindro a   =  *altezza* z.

</dd> <dt>

*height* 
</dt> <dd>

Altezza del cilindro.

</dd> <dt>

*fette* 
</dt> <dd>

Numero di suddivisioni intorno all'asse z.

</dd> <dt>

*pile* 
</dt> <dd>

Numero di suddivisioni lungo l'asse z.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluCylinder** disegna un cilindro orientato lungo l'asse z. La base del cilindro viene posizionata in corrispondenza della *z* = 0 e della parte superiore all'  =  *altezza* z. Analogamente a una sfera, un cilindro viene suddiviso in sezioni intorno all'asse z e lungo l'asse z negli stack.

*Si noti che se è* impostato su zero, questa routine genererà un cono.

Se l'orientamento è impostato su GLU \_ all'esterno (con [**gluQuadricOrientation**](gluquadricorientation.md)), eventuali normali generati si allontanano dall'asse z. In caso contrario, puntano verso l'asse z.

Se la texturing è attivata (con [**gluQuadricTexture**](gluquadrictexture.md)): le coordinate di trama vengono generate in modo che *t* sia lineare da 0,0 a *z* = 0 a 1,0 all'   =  *altezza* z; e *s* intervalli da 0,0 sull'asse y positivo, a 0,25 sull'asse x positivo, fino a 0,5 sull'asse y negativo, fino a 0,75 sull'asse x negativo e viceversa a 1,0 sull'asse y positivo.

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

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





