---
title: funzione glEnableClientState (GL. h)
description: Le funzioni glEnableClientState e glDisableClientState abilitano e disabilitano rispettivamente le matrici. | funzione glEnableClientState (GL. h)
ms.assetid: 02520f81-0b0d-4774-b1e2-713cf226347f
keywords:
- funzione glEnableClientState OpenGL
topic_type:
- apiref
api_name:
- glEnableClientState
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e333a51d4c1fe0a5ff11c717790e03aa6d054a09
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353321"
---
# <a name="glenableclientstate-function"></a>glEnableClientState (funzione)

Le funzioni **glEnableClientState** e [**glDisableClientState**](gldisableclientstate.md) abilitano e disabilitano rispettivamente le matrici.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glEnableClientState(
   GLenum array
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*array* 
</dt> <dd>

Costante simbolica per la matrice che si vuole abilitare o disabilitare. Questo parametro può assumere uno dei valori seguenti.



| Valore                                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**\_matrice di colori GL \_**</dt> </dl>                          | Se abilitata, usare le matrici di colore con le chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).<br/> Vedere anche [**glColorPointer**](glcolorpointer.md).<br/>                    |
| <span id="GL_EDGE_FLAG_ARRAY"></span><span id="gl_edge_flag_array"></span><dl> <dt>**\_matrice di \_ flag \_ Edge GL**</dt> </dl>             | Se abilitata, usare matrici di flag Edge con chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).<br/> Vedere anche [**glEdgeFlagPointer**](gledgeflagpointer.md).<br/>          |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**\_matrice di indici GL \_**</dt> </dl>                          | Se abilitata, usare le matrici di indice con le chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).<br/> Vedere anche [**glIndexPointer**](glindexpointer.md).<br/>                    |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**\_matrice normale \_ GL**</dt> </dl>                       | Se abilitata, usare matrici normali con chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).<br/> Vedere anche [**glNormalPointer**](glnormalpointer.md).<br/>                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**\_ \_ matrice Coord trama \_ GL**</dt> </dl> | Se abilitata, usare le matrici di coordinate di trama con chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).<br/> Vedere anche [**glTexCoordPointer**](gltexcoordpointer.md).<br/> |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**\_matrice di vertici GL \_**</dt> </dl>                       | Se abilitata, usare matrici di vertici con chiamate a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md).<br/> Vedere anche [**glVertexPointer**](glvertexpointer.md).<br/>                 |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                             | Significato                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl> | la *matrice* non è un valore accettato.<br/> |



## <a name="remarks"></a>Commenti

Le funzioni **glEnableClientState** e **glDisableClientState** abilitano e disabilitano varie matrici singole. Usare [**glIsEnabled**](glisenabled.md) o [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) per determinare l'impostazione corrente di tutte le funzionalità.

La chiamata di **glEnableClientState** e **glDisableClientState** tra le chiamate a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md) può causare un errore. Se non viene generato alcun errore, il comportamento non è definito.

> [!Note]  
> Le funzioni **glEnableClientState** e **glDisableClientState** sono disponibili solo in OpenGL versione 1,1 o successiva.

 

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDisableClientState**](gldisableclientstate.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glInterleavedArrays**](glinterleavedarrays.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





