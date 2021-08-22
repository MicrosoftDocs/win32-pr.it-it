---
title: Funzione gluSphere (Glu.h)
description: La funzione gluSphere disegna una sfera.
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
keywords:
- Funzione gluSphere OpenGL
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
ms.openlocfilehash: 590c4b7335fe0596c5b5b0f3dc709998fafc21f7be78f493a05f6520ed9fd368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488731"
---
# <a name="glusphere-function"></a>Funzione gluSphere

La **funzione gluSphere** disegna una sfera.

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

Oggetto quadric (creato con [**gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*Raggio* 
</dt> <dd>

Raggio della sfera.

</dd> <dt>

*Fette* 
</dt> <dd>

Numero di suddivisioni intorno all'asse z (simili alle linee di longitudine).

</dd> <dt>

*Pile* 
</dt> <dd>

Numero di suddivisioni lungo l'asse z (simili alle linee di latitudine).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluSphere** disegna una sfera del raggio specificato centrata intorno all'origine. La sfera è suddivisa intorno all'asse z in sezioni e lungo l'asse z in stack (simili a linee di longitudine e latitudine).

Se l'orientamento è impostato su GLU \_ OUTSIDE (con **gluQuadricOrientation),** tutte le normali generate si allontanano dal centro della sfera. In caso contrario, puntano verso il centro della sfera.

Se la texturing è attivata (con **gluQuadricTexture):** le coordinate della trama vengono generate in modo che *t* sia compreso tra 0,0 in *z* =*-* raggio a 1,0 in corrispondenza del raggio *z*(t aumenta linearmente lungo le linee longitudinali); e s è compreso tra 0,0 e l'asse y positivo, a 0,25 in corrispondenza dell'asse x positivo, a 0,5 in corrispondenza dell'asse y negativo, a 0,75 in corrispondenza dell'asse x negativo e di nuovo a  =   1,0 in corrispondenza dell'asse y positivo. 

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

 

 





