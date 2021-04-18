---
title: funzione gluSphere (Glu. h)
description: La funzione gluSphere disegna una sfera.
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
keywords:
- funzione gluSphere OpenGL
topic_type:
- apiref
api_name:
- gluSphere
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899ff4833c705aae34fdb7830c264fee91414116
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478016"
---
# <a name="glusphere-function"></a>gluSphere (funzione)

La funzione **gluSphere** disegna una sfera.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluSphere(
   GLUquadric *qobj,
   GLdouble   radius,
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

*raggio* 
</dt> <dd>

Raggio della sfera.

</dd> <dt>

*fette* 
</dt> <dd>

Numero di suddivisioni intorno all'asse z (simili alle linee di longitudine).

</dd> <dt>

*pile* 
</dt> <dd>

Il numero di suddivisioni lungo l'asse z, simile alle linee di latitudine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluSphere** disegna una sfera del raggio specificato centrata intorno all'origine. La sfera viene suddivisa in sezioni intorno all'asse z e lungo l'asse z negli stack (in modo analogo alle linee di longitudine e latitudine).

Se l'orientamento è impostato su GLU \_ all'esterno (con **gluQuadricOrientation**), eventuali normali generate fanno riferimento al centro della sfera. In caso contrario, puntano verso il centro della sfera.

Se la texturing è attivata (con **gluQuadricTexture**): le coordinate di trama vengono generate in modo che *t* sia compreso tra 0,0 e *z* =-*RADIUS* e 1,0 al   =  *raggio* z (*t* aumenta in modo lineare lungo le linee longitudinali); e *è* compreso tra 0,0 e l'asse y positivo, fino a 0,25 sull'asse x positivo, a 0,5 sull'asse y negativo, a 0,75 sull'asse x negativo e viceversa a 1,0 sull'asse y positivo.

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

[**gluCylinder**](glucylinder.md)
</dt> <dt>

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





