---
title: funzione gluPartialDisk (Glu. h)
description: La funzione gluPartialDisk disegna un arco di un disco.
ms.assetid: 46809c15-88c3-40fa-965a-7aeeedc1c598
keywords:
- funzione gluPartialDisk OpenGL
topic_type:
- apiref
api_name:
- gluPartialDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e35a6ea905f20e1cb30eddc5b270786614403b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300952"
---
# <a name="glupartialdisk-function"></a>gluPartialDisk (funzione)

La funzione **gluPartialDisk** disegna un arco di un disco.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluPartialDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops,
   GLdouble   startAngle,
   GLdouble   sweepAngle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*qobj* 
</dt> <dd>

Oggetto quadrica (creato con [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*innerRadius* 
</dt> <dd>

Raggio interno del disco parziale (può essere zero).

</dd> <dt>

*outerRadius* 
</dt> <dd>

Raggio esterno del disco parziale.

</dd> <dt>

*fette* 
</dt> <dd>

Numero di suddivisioni intorno all'asse z.

</dd> <dt>

*cicli* 
</dt> <dd>

Numero di anelli concentrici sull'origine in cui è suddiviso il disco parziale.

</dd> <dt>

*startAngle* 
</dt> <dd>

Angolo iniziale, in gradi, della parte del disco.

</dd> <dt>

*sweepAngle* 
</dt> <dd>

Angolo dello sweep, in gradi, della parte del disco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluPartialDisk** esegue il rendering di un disco parziale sul piano *z* = 0. Un disco parziale è simile a un disco completo, ad eccezione del fatto che è incluso solo il subset del disco da *startAngle* a *startAngle*  +  *sweepAngle* (dove 0 gradi si trova lungo l'asse y positivo, 90 gradi si trova lungo l'asse x positivo, 180 gradi si trova lungo l'asse y negativo e 270 gradi si trova lungo l'asse x negativo).

Il disco parziale ha un raggio di *OuterRadius* e contiene un foro circolare concentrico con un raggio di *InnerRadius*. Se *InnerRadius* è zero, non viene generato alcun Hole. Il disco parziale viene suddiviso intorno all'asse z in sezioni (ad esempio, sezioni della pizza) e anche sull'asse z negli anelli, come specificato dalle *sezioni* e dai *cicli*, rispettivamente.

Per quanto riguarda l'orientamento, il lato z positivo del disco parziale viene considerato esterno (vedere [**gluQuadricOrientation**](gluquadricorientation.md)). Ciò significa che se l'orientamento è impostato su GLU \_ all'esterno, eventuali normali generano un punto lungo l'asse z positivo.

Se è stata attivata la texturing (con [**gluQuadricTexture**](gluquadrictexture.md)), **gluPartialDisk** genera le coordinate di trama in modo lineare, in modo da dove *r*  =  *OuterRadius*, il valore in (*r*, 0, 0) è (1, 0,5); at (0, *r*, 0) è (0,5, 1); at (*r*, 0, 0) è (0, 0,5); e at (0, *r*, 0) è (0,5, 0).

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

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





