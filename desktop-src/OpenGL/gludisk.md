---
title: Funzione gluDisk (Glu.h)
description: La funzione gluDisk disegna un disco.
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- Funzione gluDisk OpenGL
topic_type:
- apiref
api_name:
- gluDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83abb24f665cbcbf978a6423868751794371606cf412f609876a8f17d42c115a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489531"
---
# <a name="gludisk-function"></a>Funzione gluDisk

La **funzione gluDisk** disegna un disco.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*qobj* 
</dt> <dd>

Oggetto quadric (creato con [**gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*innerRadius* 
</dt> <dd>

Raggio interno del disco (può essere zero).

</dd> <dt>

*outerRadius* 
</dt> <dd>

Raggio esterno del disco.

</dd> <dt>

*Fette* 
</dt> <dd>

Numero di suddivisioni intorno all'asse z.

</dd> <dt>

*Loop* 
</dt> <dd>

Numero di anelli concentrici relativi all'origine in cui il disco è suddiviso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluDisk** esegue il rendering di un disco *sul piano z* = 0. Il disco ha un raggio di *outerRadius* e contiene un foro circolare concentrico con un raggio *di innerRadius.* Se *innerRadius è* 0, non viene generato alcun foro. Il disco è suddiviso intorno all'asse z in sezioni (come le fette di pizza) e  anche intorno all'asse z in anelli (come specificato rispettivamente da sezioni e cicli ).

Per quanto riguarda l'orientamento, il lato *z* positivo del disco viene considerato esterno *(vedere* [**gluQuadricOrientation).**](gluquadricorientation.md) Ciò significa che se l'orientamento è impostato su GLU OUTSIDE, qualsiasi punto generato dalle normali \_ lungo l'asse z positivo.

Se la texturing è attivata (con [**gluQuadricTexture**](gluquadrictexture.md)), le coordinate della trama vengono generate in modo lineare in modo che, dove *r* outerRadius , il valore in  =  (*r*, 0, 0) è (1, 0,5); in (0, *r*, 0) è (0,5, 1), in (-*r*, 0, 0) è (0, 0,5) e in (0, -*r*, 0) è (0,5, 0).

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

 

 





