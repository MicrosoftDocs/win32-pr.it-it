---
title: funzione gluDisk (Glu. h)
description: La funzione gluDisk disegna un disco.
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- funzione gluDisk OpenGL
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
ms.openlocfilehash: a9a9e8b547790049c93360f060e944aafcea4511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048332"
---
# <a name="gludisk-function"></a>gluDisk (funzione)

La funzione **gluDisk** disegna un disco.

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

Oggetto quadrica (creato con [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*innerRadius* 
</dt> <dd>

Raggio interno del disco (può essere zero).

</dd> <dt>

*outerRadius* 
</dt> <dd>

Raggio esterno del disco.

</dd> <dt>

*fette* 
</dt> <dd>

Numero di suddivisioni intorno all'asse z.

</dd> <dt>

*cicli* 
</dt> <dd>

Numero di anelli concentrici sull'origine in cui è suddiviso il disco.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluDisk** esegue il rendering di un disco sul piano *z* = 0. Il disco ha un raggio di *OuterRadius* e contiene un foro circolare concentrico con un raggio di *InnerRadius*. Se *InnerRadius* è 0, non viene generato alcun Hole. Il disco viene suddiviso in sezioni intorno all'asse z in sezioni, ad esempio le sezioni della pizza, e anche sull'asse z negli anelli, come specificato dalle *sezioni* e dai *cicli*, rispettivamente.

Per quanto riguarda l'orientamento, il lato *z* positivo del disco è considerato *esterno* (vedere [**gluQuadricOrientation**](gluquadricorientation.md)). Ciò significa che se l'orientamento è impostato su GLU \_ all'esterno, eventuali normali generano un punto lungo l'asse z positivo.

Se la texturing è attivata (con [**gluQuadricTexture**](gluquadrictexture.md)), le coordinate di trama vengono generate linearmente in modo tale che, dove *r*  =  *OuterRadius*, il valore in (*r*, 0, 0) è (1, 0,5); at (0, *r*, 0) it is (0,5,1); at (-*r*, 0, 0) è (0, 0,5) e at (0,-*r*, 0) è (0,5, 0).

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

 

 





