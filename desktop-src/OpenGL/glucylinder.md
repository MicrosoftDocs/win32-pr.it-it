---
title: Funzione gluCylinder (Glu.h)
description: La funzione gluCylinder disegna un cilindro.
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- Funzione gluCylinder OpenGL
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
ms.openlocfilehash: 1a09ff92aec17a13f03ecb1cbaaf118398b2b88dea76936454d527bb9c37032f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061609"
---
# <a name="glucylinder-function"></a>Funzione gluCylinder

La **funzione gluCylinder** disegna un cilindro.

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

Oggetto quadric (creato con [**gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*baseRadius* 
</dt> <dd>

Raggio del cilindro in *z* = 0.

</dd> <dt>

*topRadius* 
</dt> <dd>

Raggio del cilindro *all'altezza z.*  =  

</dd> <dt>

*height* 
</dt> <dd>

Altezza del cilindro.

</dd> <dt>

*Fette* 
</dt> <dd>

Numero di suddivisioni intorno all'asse z.

</dd> <dt>

*Pile* 
</dt> <dd>

Numero di suddivisioni lungo l'asse z.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluCylinder** disegna un cilindro orientato lungo l'asse z. La base del cilindro viene posizionata in *corrispondenza di z* = 0 e la parte superiore all'altezza *z*  =  . Come una sfera, un cilindro viene suddiviso intorno all'asse z in sezioni e lungo l'asse z in stack.

Si noti che se *topRadius* è impostato su zero, questa routine genererà un cono.

Se l'orientamento è impostato su GLU \_ OUTSIDE (con [**gluQuadricOrientation),**](gluquadricorientation.md)tutte le normali generate puntano all'asse z. In caso contrario, puntano verso l'asse z.

Se la texturing è attivata (con [**gluQuadricTexture):**](gluquadrictexture.md)le coordinate della trama vengono generate in modo che *t* intervalli linearmente da 0,0 a *z* = 0 a 1,0 all'altezza *z*; e s intervalli da  =  0,0 all'asse y positivo, a 0,25 in corrispondenza dell'asse x positivo, a 0,5 in corrispondenza dell'asse y negativo, a 0,75 in corrispondenza dell'asse x negativo e di nuovo a 1,0 in corrispondenza dell'asse y  positivo.

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

 

 





