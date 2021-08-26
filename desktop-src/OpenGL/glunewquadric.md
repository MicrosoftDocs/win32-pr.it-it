---
title: Funzione gluNewQuadric (Glu.h)
description: La funzione gluNewQuadric crea un oggetto quadric.
ms.assetid: 5a4289bf-b57a-4c74-b0e3-b7536671e4df
keywords:
- Funzione gluNewQuadric OpenGL
topic_type:
- apiref
api_name:
- gluNewQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66fed28c555d327bffa18d8f9100a6f5e9824b714bff1308e6b2dab20b5d3671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036271"
---
# <a name="glunewquadric-function"></a>Funzione gluNewQuadric

La **funzione gluNewQuadric** crea un oggetto quadric.

## <a name="syntax"></a>Sintassi


```C++
GLUquadric* WINAPI gluNewQuadric(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="remarks"></a>Commenti

La **funzione gluNewQuadric** crea e restituisce un puntatore a un nuovo oggetto quadric. Fare riferimento a questo oggetto quando si chiamano le funzioni di rendering e controllo quadric. Un valore restituito pari a zero indica che la memoria da allocare all'oggetto non è sufficiente.

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

[**gluDeleteQuadric**](gludeletequadric.md)
</dt> <dt>

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[*gluQuadricCallback*](gluquadric.md)
</dt> <dt>

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





