---
title: funzione glDeleteTextures (GL. h)
description: La funzione glDeleteTextures Elimina le trame denominate.
ms.assetid: 300eb99a-9ee5-4495-9489-7e084db9c6c1
keywords:
- funzione glDeleteTextures OpenGL
topic_type:
- apiref
api_name:
- glDeleteTextures
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37893874f143a210bde0099caa7b5ec266f8948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475676"
---
# <a name="gldeletetextures-function"></a>glDeleteTextures (funzione)

La funzione **glDeleteTextures** Elimina le trame denominate.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glDeleteTextures(
         GLsizei n,
   const GLuint  *textures
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*n* 
</dt> <dd>

Numero di trame da eliminare.

</dd> <dt>

*trame* 
</dt> <dd>

Matrice di trame da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *n* è un valore negativo.<br/>                                                                                                  |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glDeleteTextures** Elimina *n* trame denominate dagli elementi delle *trame* della matrice. Una volta eliminata, la trama non presenta alcun contenuto o dimensionalità e il nome è disponibile per il riutilizzo (ad esempio, da **glGenTextures**). La funzione **glDeleteTextures** ignora gli zeri e i nomi che non corrispondono alle trame esistenti.

Se una trama attualmente associata viene eliminata, l'associazione viene ripristinata su zero (trama predefinita).

Non è possibile includere chiamate a **glDeleteTextures** negli elenchi di visualizzazione.

> [!Note]  
> La funzione **glDeleteTextures** è disponibile solo in OpenGL versione 1,1 o successiva.

 

La funzione seguente recupera le informazioni correlate a **glDeleteTextures**:

-   [**glIsTexture**](glistexture.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glAreTexturesResident**](glaretexturesresident.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGenTextures**](glgentextures.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsTexture**](glistexture.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





