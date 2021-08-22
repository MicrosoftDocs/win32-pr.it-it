---
title: Funzione glIsTexture (Gl.h)
description: La funzione glIsTexture determina se un nome corrisponde a una trama.
ms.assetid: 89d06642-ff28-4a67-ac7f-ca58150f301e
keywords:
- Funzione glIsTexture OpenGL
topic_type:
- apiref
api_name:
- glIsTexture
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db28b6892d5aa0e9eaf98aec50b02ad102db8ba549474c673c6c0d918d799d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493351"
---
# <a name="glistexture-function"></a>Funzione glIsTexture

La **funzione glIsTexture** determina se un nome corrisponde a una trama.

## <a name="syntax"></a>Sintassi


```C++
GLboolean WINAPI glIsTexture(
   GLuint texture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Texture* 
</dt> <dd>

Valore che rappresenta il nome di una trama.

</dd> </dl>

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Se il *parametro texture* è attualmente il nome di una trama, la **funzione glIsTexture** restituisce GL \_ TRUE. La **funzione glIsTexture** restituisce GL \_ FALSE se *texture* è zero. Restituisce anche GL FALSE se è un valore diverso da zero che non è attualmente il nome di una trama o \_ se si verifica un errore.

Non è possibile includere chiamate **a glIsTexture** negli elenchi di visualizzazione.

> [!Note]  
> La **funzione glIsTexture** è disponibile solo in OpenGL versione 1.1 o successiva.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGenTextures**](glgentextures.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





