---
title: funzione glColorPointer (GL. h)
description: La funzione glColorPointer definisce una matrice di colori.
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
keywords:
- funzione glColorPointer OpenGL
topic_type:
- apiref
api_name:
- glColorPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abced52f0d0664e998ad8380e33d43d4af36bcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475845"
---
# <a name="glcolorpointer-function"></a>glColorPointer (funzione)

La funzione **glColorPointer** definisce una matrice di colori.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glColorPointer(
         GLint   size,
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*size* 
</dt> <dd>

Numero di componenti per colore. Il valore deve essere 3 o 4.

</dd> <dt>

*type* 
</dt> <dd>

Tipo di dati di ogni componente colore in una matrice di colori. I tipi di dati accettabili sono specificati con le costanti seguenti: GL \_ byte, GL \_ unsigned \_ byte, GL \_ short, GL \_ unsigned \_ short, GL \_ int, GL \_ unsigned \_ int, GL \_ float o GL \_ Double.

</dd> <dt>

*stride* 
</dt> <dd>

Offset dei byte tra i colori consecutivi. Quando *stride* è zero, i colori sono strettamente compressi nella matrice.

</dd> <dt>

*indicatore di misura* 
</dt> <dd>

Puntatore al primo componente del primo elemento di colore in una matrice di colori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                              | Significato                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl> | *size* non è 3 o 4.<br/>            |
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>  | il *tipo* non è un valore accettato.<br/> |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl> | *stride* o *count* è negativo.<br/> |



## <a name="remarks"></a>Commenti

La funzione **glColorPointer** specifica il percorso e il formato dati di una matrice di componenti colore da usare durante il rendering. Il parametro *stride* determina l'offset dei byte da un colore all'altro, abilitando la compressione degli attributi dei vertici in una singola matrice o archiviazione in matrici separate. In alcune implementazioni, l'archiviazione degli attributi dei vertici in una singola matrice può essere più efficiente rispetto all'utilizzo di matrici separate.

Abilitare la matrice di colori specificando la \_ costante della matrice di colori GL \_ con [**glEnableClientState**](glenableclientstate.md). La chiamata a [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md) usa la matrice di colori che è quindi abilitata. Per impostazione predefinita, la matrice di colori è disabilitata. Le chiamate **glColorPointer** non possono essere immesse negli elenchi di visualizzazione.

Quando si specifica una matrice di colori utilizzando **glColorPointer**, i valori di tutti i parametri della matrice di colori della funzione vengono salvati in uno stato sul lato client ed è possibile memorizzare nella cache gli elementi della matrice statica. Poiché i parametri della matrice di colori sono in uno stato lato client, [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) non salvano o ripristinano i valori dei parametri.

Sebbene l'impostazione della matrice di colori all'interno delle coppie [**glBegin**](glbegin.md) e [**glEnd**](glend.md) non generi un errore, i risultati non sono definiti.

Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glColorPointer** :

[**glIsEnabled**](glisenabled.md) con matrice di \_ colori GL argomento \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con le \_ dimensioni della \_ matrice di colori GL argomento \_

**glGet** con tipo di \_ matrice di colori GL argomento \_ \_

**glGet** con argomento di \_ matrice dei colori GL \_ \_

**glGet** con argomento \_ conteggio delle \_ matrici di colori GL \_

[**glGetPointerv**](glgetpointerv.md) con puntatore alla \_ matrice di colori GL argomento \_ \_

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

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





