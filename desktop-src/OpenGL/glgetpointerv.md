---
title: Funzione glGetPointerv (Gl.h)
description: La funzione glGetPointerv restituisce l'indirizzo di una matrice di dati dei vertici.
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- Funzione glGetPointerv OpenGL
topic_type:
- apiref
api_name:
- glGetPointerv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdbef5cc17a547e82dfa55876d927ef9fed87f106d9e5fa0d5d1c36a5ce269b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493921"
---
# <a name="glgetpointerv-function"></a>Funzione glGetPointerv

La **funzione glGetPointerv** restituisce l'indirizzo di una matrice di dati dei vertici.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pname* 
</dt> <dd>

Tipo di puntatore a matrice da restituire dalle costanti simboliche seguenti: GL \_ COLOR \_ ARRAY \_ \_ POINTER, GL EDGE FLAG ARRAY \_ \_ \_ POINTER, GL FEEDBACK BUFFER \_ \_ \_ POINTER, GL INDEX ARRAY \_ \_ \_ POINTER, GL NORMAL ARRAY \_ \_ \_ POINTER, GL TEXTURE \_ \_ COORD \_ ARRAY \_ POINTER, GL SELECTION BUFFER POINTER \_ e GL \_ \_ \_ VERTEX ARRAY \_ \_ POINTER.

</dd> <dt>

*params* 
</dt> <dd>

Restituisce il valore del puntatore di matrice specificato da *pname*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                             | Significato                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | *pname* non è un valore accettato.<br/> |



## <a name="remarks"></a>Commenti

La **funzione glGetPointerv** restituisce informazioni sul puntatore di matrice. Il *parametro pname* è una costante simbolica che specifica il tipo di puntatore di matrice da restituire e *params* è un puntatore a una posizione in cui inserire i dati restituiti.

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

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





