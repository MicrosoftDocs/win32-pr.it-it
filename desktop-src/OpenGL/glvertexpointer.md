---
title: funzione glVertexPointer (GL. h)
description: La funzione glVertexPointer definisce una matrice di dati dei vertici.
ms.assetid: e5f97fdc-9448-4389-8533-3855a3213feb
keywords:
- funzione glVertexPointer OpenGL
topic_type:
- apiref
api_name:
- glVertexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422dd1a7938cc5adb183ff7e17c59a8f52eb4909
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478227"
---
# <a name="glvertexpointer-function"></a>glVertexPointer (funzione)

La funzione **glVertexPointer** definisce una matrice di dati dei vertici.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glVertexPointer(
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

Numero di coordinate per vertice. Il valore delle *dimensioni* deve essere 2, 3 o 4.

</dd> <dt>

*type* 
</dt> <dd>

Il tipo di dati di ogni coordinata nella matrice usando le costanti simboliche seguenti: GL \_ short, GL \_ int, GL \_ float e GL \_ Double.

</dd> <dt>

*stride* 
</dt> <dd>

Offset dei byte tra i vertici consecutivi. Quando *stride* è zero, i vertici sono strettamente compressi nella matrice.

</dd> <dt>

*indicatore di misura* 
</dt> <dd>

Puntatore alla prima coordinata del primo vertice nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                              | Significato                                       |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl> | *size* non è 2, 3 o 4. <br/>        |
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>  | il *tipo* non è un valore accettato.<br/>  |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl> | *stride* o *count* è negativo. <br/> |



## <a name="remarks"></a>Commenti

La funzione **glVertexPointer** specifica il percorso e i dati di una matrice di coordinate del vertice da usare durante il rendering. Il parametro *size* specifica il numero di coordinate per vertice. Il parametro di *tipo* specifica il tipo di dati di ogni coordinata del vertice. Il parametro *stride* determina l'offset dei byte da un vertice a quello successivo, abilitando la compressione di vertici e attributi in una singola matrice o archiviazione in matrici separate. In alcune implementazioni, l'archiviazione dei vertici e degli attributi in una singola matrice può essere più efficiente rispetto all'uso di matrici separate (vedere [**glInterleavedArrays**](glinterleavedarrays.md)).

Una matrice di vertici viene abilitata quando si specifica la \_ costante della matrice di vertici GL \_ con [**glEnableClientState**](glenableclientstate.md). Se abilitata, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md)e [**glArrayElement**](glarrayelement.md) usano la matrice di vertici. Per impostazione predefinita, la matrice di vertici è disabilitata.

Non è possibile includere **glVertexPointer** negli elenchi di visualizzazione.

Quando si specifica una matrice di vertici utilizzando **glVertexPointer**, i valori di tutti i parametri della matrice di vertici della funzione vengono salvati in uno stato lato client ed è possibile memorizzare nella cache elementi statici della matrice. Poiché i parametri della matrice Vertex sono stati lato client, i relativi valori non vengono salvati né ripristinati da [**glPushAttrib**](glpushattrib.md) e **glPopAttrib**.

Sebbene non venga generato alcun errore se si chiama **glVertexPointer** nelle coppie [**glBegin**](glbegin.md) e [**glEnd**](glend.md) , i risultati non sono definiti.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glVertexPointer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con dimensione della \_ matrice di vertici dell'argomento GL \_ \_

**glGet** con argomento della \_ matrice di vertici dell'argomento GL \_ \_

**glGet** con argomento \_ numero di matrici di vertici \_ \_

**glGet** con tipo di \_ matrice di vertici GL argomento \_ \_

[**glGetPointerv**](glgetpointerv.md) con puntatore alla \_ matrice del vertice GL dell'argomento \_ \_

[**glIsEnabled**](glisenabled.md) con argomento \_ matrice di vertici GL \_

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

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> </dl>

 

 





