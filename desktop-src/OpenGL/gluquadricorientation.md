---
title: Funzione gluQuadricOrientation (Glu.h)
description: La funzione gluQuadricOrientation specifica l'orientamento interno o esterno per i quadrici.
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
keywords:
- Funzione gluQuadricOrientation OpenGL
topic_type:
- apiref
api_name:
- gluQuadricOrientation
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baa02c3b6d207cbcc2bf487f51c0e96dc2f2dd98748edc81efb58ac957fac4ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937627"
---
# <a name="gluquadricorientation-function"></a>Funzione gluQuadricOrientation

La **funzione gluQuadricOrientation** specifica l'orientamento interno o esterno per i quadrici.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluQuadricOrientation(
   GLUquadric *quadObject,
   GLenum     orientation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*quadObject* 
</dt> <dd>

Oggetto quadric (creato con [**gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*Orientamento* 
</dt> <dd>

Orientamento desiderato. I valori seguenti sono validi.



| Valore                                                                                                                                                   | Significato                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="GLU_OUTSIDE"></span><span id="glu_outside"></span><dl> <dt>**GLU \_ OUTSIDE**</dt> </dl> | Disegnare i quadrifoli con le normali che puntano verso l'esterno. Si tratta del valore predefinito.<br/> |
| <span id="GLU_INSIDE"></span><span id="glu_inside"></span><dl> <dt>**GLU \_ INSIDE**</dt> </dl>    | Disegnare i quadrifoli con le normali che puntano verso l'interno.<br/>                             |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluQuadricOrientation** specifica il tipo di orientamento desiderato per i quadrifoli sottoposti a rendering con **quadObject**. L'interpretazione di verso l'esterno e verso l'interno dipende dal quadrico disegnato.

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

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





