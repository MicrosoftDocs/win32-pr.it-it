---
title: funzione glIndexPointer (GL. h)
description: La funzione glIndexPointer definisce una matrice di indici dei colori.
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- funzione glIndexPointer OpenGL
topic_type:
- apiref
api_name:
- glIndexPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca6858d7d1e3f13e4155bd40307a53b22e80a56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475262"
---
# <a name="glindexpointer-function"></a>glIndexPointer (funzione)

La funzione **glIndexPointer** definisce una matrice di indici dei colori.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glIndexPointer(
         GLenum  type,
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*type* 
</dt> <dd>

Il tipo di dati di ogni indice dei colori nella matrice usando le costanti simboliche seguenti: GL \_ short, GL \_ int, GL \_ float, GL \_ Double.

</dd> <dt>

*stride* 
</dt> <dd>

Offset dei byte tra indici di colore consecutivi. Quando *stride* è zero, gli indici dei colori sono strettamente compressi nella matrice.

</dd> <dt>

*indicatore di misura* 
</dt> <dd>

Puntatore al primo indice dei colori nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                              | Significato                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>  | il *tipo* non è un valore accettato.<br/> |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl> | *stride* o *count* è negativo.<br/> |



## <a name="remarks"></a>Commenti

La funzione **glIndexPointer** specifica il percorso e i dati di una matrice di indici dei colori da usare durante il rendering. Il parametro di *tipo* specifica il tipo di dati di ogni indice di colore e *stride* determina l'offset dei byte da un indice di colore alla successiva, abilitando la compressione di vertici e attributi in una singola matrice o archiviazione in matrici separate. In alcune implementazioni, l'archiviazione dei vertici e degli attributi in una singola matrice può essere più efficiente rispetto all'utilizzo di matrici separate. Per ulteriori informazioni, vedere [**glInterleavedArrays**](glinterleavedarrays.md).

Una matrice di indice dei colori viene abilitata quando si specifica \_ la \_ costante della matrice di indice GL con [**glEnableClientState**](glenableclientstate.md). Quando è abilitata, [**glDrawArrays**](gldrawarrays.md) e [**glArrayElement**](glarrayelement.md) usano la matrice di indicizzazione dei colori. Per impostazione predefinita, la matrice di indice dei colori è disabilitata.

Non è possibile includere **glIndexPointer** negli elenchi di visualizzazione.

Quando si specifica una matrice di indice dei colori utilizzando **glIndexPointer**, i valori di tutti i parametri della matrice di indice dei colori della funzione vengono salvati in uno stato lato client e gli elementi della matrice statica possono essere memorizzati nella cache. Poiché i parametri della matrice di indice dei colori sono stati lato client, i relativi valori non vengono salvati né ripristinati da [**glPushAttrib**](glpushattrib.md) e **glPopAttrib**.

Sebbene non venga generato alcun errore quando si chiama **glIndexPointer** all'interno di coppie [**glBegin**](glbegin.md) e **glEnd** , i risultati non sono definiti.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glIndexPointer**:

[**glIsEnabled**](glisenabled.md) con argomento \_ Array GL index \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ matrice di indice GL \_ \_

**glGet** con argomento \_ numero di \_ matrici di indice GL \_

**glGet** con tipo di \_ matrice di indice GL dell'argomento \_ \_

**glGet** con le \_ dimensioni della \_ matrice dell'indice GL dell'argomento \_

[**glGetPointerv**](glgetpointerv.md) con puntatore alla \_ matrice di indice GL degli argomenti \_ \_

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

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





