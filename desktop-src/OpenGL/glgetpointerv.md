---
title: funzione glGetPointerv (GL. h)
description: La funzione glGetPointerv restituisce l'indirizzo di una matrice di dati vertex.
ms.assetid: 6f85c508-9335-4474-8cc5-e67c7421a8e4
keywords:
- funzione glGetPointerv OpenGL
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
ms.openlocfilehash: 569861922514af88835fbb4e313dab3286b7c47d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302192"
---
# <a name="glgetpointerv-function"></a>glGetPointerv (funzione)

La funzione **glGetPointerv** restituisce l'indirizzo di una matrice di dati vertex.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetPointerv(
   GLenum pname,
   GLvoid **params
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pname* 
</dt> <dd>

Il tipo di puntatore di matrice da restituire dalle costanti simboliche seguenti: puntatore alla matrice di colori GL, puntatore alla matrice del flag Edge GL, puntatore del buffer del feedback GL, puntatore della matrice di \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ indici GL, puntatore di matrice GL Normal, puntatore della matrice Coord della trama GL, \_ \_ \_ puntatore al \_ \_ \_ \_ \_ \_ \_ \_ \_ buffer di selezione GL \_ e puntatore alla matrice del \_ vertice GL \_ \_ .

</dd> <dt>

*params* 
</dt> <dd>

Restituisce il valore del puntatore di matrice specificato da *pname*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                             | Significato                                       |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl> | *pname* non è un valore accettato.<br/> |



## <a name="remarks"></a>Commenti

La funzione **glGetPointerv** restituisce informazioni sul puntatore alla matrice. Il parametro *pname* è una costante simbolica che specifica il tipo di puntatore alla matrice da restituire e *params* è un puntatore a una posizione in cui inserire i dati restituiti.

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

 

 





