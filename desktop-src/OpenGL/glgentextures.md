---
title: Funzione glGenTextures (Gl.h)
description: La funzione glGenTextures genera nomi di trama.
ms.assetid: f2491faf-2b33-4b06-9a9f-51ac295690fb
keywords:
- Funzione glGenTextures OpenGL
topic_type:
- apiref
api_name:
- glGenTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b28275bef054b26c2145ab9779ec776297ac7838d0313769123fb1be904a3bd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625231"
---
# <a name="glgentextures-function"></a>Funzione glGenTextures

La **funzione glGenTextures genera** nomi di trama.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGenTextures(
   GLsizei n,
   GLuint  *textures
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*n* 
</dt> <dd>

Numero di nomi di trama da generare.

</dd> <dt>

*Texture* 
</dt> <dd>

Puntatore al primo elemento di una matrice in cui vengono archiviati i nomi di trama generati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *n* è un valore negativo.<br/>                                                                                                  |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glGenTextures** restituisce *n nomi* di trama nel parametro *textures.* I nomi delle trame non sono necessariamente un set contiguo di interi, ma nessuno dei nomi restituiti può essere stato in uso immediatamente prima di chiamare la funzione **glGenTextures.** Le trame generate presuppongono la dimensionalità della destinazione della trama a cui vengono prima associate con [**la funzione glBindTexture.**](glbindtexture.md) I nomi di trama restituiti da **glGenTextures** non vengono restituiti dalle chiamate successive a **glGenTextures** a meno che non vengano prima eliminati chiamando [**glDeleteTextures.**](gldeletetextures.md)

Non è possibile **includere glGenTextures negli** elenchi visualizzati.

> [!Note]  
> La **funzione glGenTextures** è disponibile solo in OpenGL versione 1.1 o successiva.

 

La funzione seguente recupera informazioni correlate a **glGenTextures**:

-   [**glIsTexture**](glistexture.md)

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

[**glDeleteTextures**](gldeletetextures.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





