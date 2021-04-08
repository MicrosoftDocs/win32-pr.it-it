---
title: funzione glNormalPointer (GL. h)
description: La funzione glNormalPointer definisce una matrice di normali.
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- funzione glNormalPointer OpenGL
topic_type:
- apiref
api_name:
- glNormalPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f3abbfbd989351af647557ec64f8ee3172dc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964959"
---
# <a name="glnormalpointer-function"></a>glNormalPointer (funzione)

La funzione **glNormalPointer** definisce una matrice di normali.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glNormalPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*type* 
</dt> <dd>

Il tipo di dati di ogni coordinata nella matrice usando le costanti simboliche seguenti: GL \_ byte, GL \_ short, GL \_ int, GL \_ float e GL \_ Double.

</dd> <dt>

*stride* 
</dt> <dd>

Offset dei byte tra le normali consecutive. Quando *stride* è zero, le normali sono strettamente compresse nella matrice.

</dd> <dt>

*indicatore di misura* 
</dt> <dd>

Puntatore alla prima normale nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | il *tipo* non è un valore accettato.<br/> |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | *stride* o *count* è negativo.<br/> |



## <a name="remarks"></a>Commenti

La funzione **glNormalPointer** specifica il percorso e i dati di una matrice di normali da usare durante il rendering. Il parametro di *tipo* specifica il tipo di dati di ogni normale coordinata. Il parametro *stride* determina l'offset dei byte da un normale a quello successivo, abilitando la compressione di vertici e attributi in una singola matrice o archiviazione in matrici separate. In alcune implementazioni, l'archiviazione dei vertici e degli attributi in una singola matrice può risultare più efficiente rispetto all'utilizzo di matrici separate; per informazioni dettagliate, vedere [**glInterleavedArrays**](glinterleavedarrays.md) .

Una matrice normale viene abilitata quando si specifica la \_ \_ costante di matrice GL Normal con [**glEnableClientState**](glenableclientstate.md). Quando è abilitata, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md) e [**glArrayElement**](glarrayelement.md) usano la matrice normale. Per impostazione predefinita, la matrice normale è disabilitata.

Non è possibile includere **glNormalPointer** negli elenchi di visualizzazione.

Quando si specifica una matrice normale utilizzando **glNormalPointer**, i valori di tutti i parametri di matrice normali della funzione vengono salvati in uno stato sul lato client. Poiché i normali parametri della matrice vengono salvati in uno stato sul lato client, i relativi valori non vengono salvati né ripristinati da [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).

Sebbene non venga generato alcun errore quando si chiama **glNormalPointer** all'interno di coppie [**glBegin**](glbegin.md) e [**glEnd**](glend.md) , i risultati non sono definiti.

Le funzioni seguenti sono associate a **glNormalPointer**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento con \_ lo \_ stride di matrice normale \_

**glGet** con argomento \_ numero di \_ matrici \_ normali

**glGet** con tipo di \_ matrice Normal GL argomento \_ \_

**glGetPointerv** con puntatore alla matrice di un argomento GL \_ Normal \_ \_

[**glIsEnabled**](glisenabled.md) con matrice GL di argomenti \_ normali \_

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

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glInterleavedArrays**](glinterleavedarrays.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> </dl>

 

 





