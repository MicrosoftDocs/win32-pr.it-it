---
title: Funzione gluQuadricTexture (Glu.h)
description: La funzione gluQuadricTexture specifica se è necessario eseguire la trama dei quadric.
ms.assetid: 11681497-f099-4856-a0ac-6a44abd3e1a1
keywords:
- Funzione gluQuadricTexture OpenGL
topic_type:
- apiref
api_name:
- gluQuadricTexture
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbde88e0a878fd59e01ad0a450cf4cbe9831c4ad867c8029373586a8efe830eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937482"
---
# <a name="gluquadrictexture-function"></a>Funzione gluQuadricTexture

La **funzione gluQuadricTexture** specifica se è necessario eseguire la trama dei quadric.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluQuadricTexture(
   GLUquadric *quadObject,
   GLboolean  textureCoords
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*quadObject* 
</dt> <dd>

Oggetto quadric (creato con [**gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*TextureCoords* 
</dt> <dd>

Flag che indica se devono essere generate le coordinate della trama. I valori seguenti sono validi.



| Valore                                                                                                                                          | Significato                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="GL_TRUE"></span><span id="gl_true"></span><dl> <dt>**GL \_ TRUE**</dt> </dl>    | Generare le coordinate della trama.<br/>                                   |
| <span id="GL_FALSE"></span><span id="gl_false"></span><dl> <dt>**GL \_ FALSE**</dt> </dl> | Non generare coordinate di trama. Si tratta del valore predefinito.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluQuadricTexture** specifica se le coordinate della trama devono essere generate per quadrics di cui viene eseguito il rendering con **quadObject**.

Il modo in cui vengono generate le coordinate della trama dipende dal quadric rendering specifico.

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
</dt> </dl>

 

 





