---
title: Funzione gluPartialDisk (Glu.h)
description: La funzione gluPartialDisk disegna un arco di un disco.
ms.assetid: 46809c15-88c3-40fa-965a-7aeeedc1c598
keywords:
- Funzione gluPartialDisk OpenGL
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
ms.openlocfilehash: 687738cce6bb311d7e8223877b716abdaef180340ab570f430659ee2e98458ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519441"
---
# <a name="glupartialdisk-function"></a>Funzione gluPartialDisk

La **funzione gluPartialDisk** disegna un arco di un disco.

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

Oggetto quadric (creato con [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*innerRadius* 
</dt> <dd>

Raggio interno del disco parziale (può essere zero).

</dd> <dt>

*outerRadius* 
</dt> <dd>

Raggio esterno del disco parziale.

</dd> <dt>

*Fette* 
</dt> <dd>

Numero di suddivisioni intorno all'asse z.

</dd> <dt>

*Loop* 
</dt> <dd>

Numero di anelli concentrici sull'origine in cui il disco parziale è suddiviso.

</dd> <dt>

*startAngle* 
</dt> <dd>

Angolo iniziale, in gradi, della parte del disco.

</dd> <dt>

*sweepAngle* 
</dt> <dd>

Angolo di sweep, in gradi, della parte del disco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluPartialDisk** esegue il rendering di un disco parziale sul *piano z* = 0. Un disco parziale è simile a un disco completo, ad eccezione del fatto che è incluso solo il subset del disco da *startAngle* a *startAngle*  +  *sweepAngle* (dove 0 gradi si trova lungo l'asse y positivo, 90 gradi si trova lungo l'asse x positivo, 180 gradi lungo l'asse y negativo e 270 gradi lungo l'asse x negativo).

Il disco parziale ha un raggio *di outerRadius* e contiene un foro circolare concentrico con un raggio *di innerRadius*. Se *innerRadius* è zero, non viene generato alcun foro. Il disco parziale è suddiviso intorno all'asse z in sezioni (come le sezioni pizza) e anche  sull'asse z in anelli (come specificato rispettivamente da sezioni e cicli). 

Per quanto riguarda l'orientamento, il lato z positivo del disco parziale viene considerato esterno (vedere [**gluQuadricOrientation**](gluquadricorientation.md)). Ciò significa che se l'orientamento è impostato su GLU OUTSIDE, qualsiasi punto generato dalle normali \_ lungo l'asse z positivo.

Se è stata attivata la texturing (con [**gluQuadricTexture),**](gluquadrictexture.md) **gluPartialDisk** genera le coordinate della trama in modo lineare in modo che, dove *r* outerRadius , il valore in  =  (*r*, 0, 0) is (1, 0.5); at (0, *r*, 0) it is (0.5, 1); at (*r*, 0, 0) it is (0, 0.5); and at (0, *r*, 0) it is (0.5, 0).

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

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





