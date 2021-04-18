---
title: funzione glTexCoordPointer (GL. h)
description: La funzione glTexCoordPointer definisce una matrice di coordinate di trama.
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
keywords:
- funzione glTexCoordPointer OpenGL
topic_type:
- apiref
api_name:
- glTexCoordPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: febc9c79bdbc4a1ed1c14380af47f36309f12662
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302755"
---
# <a name="gltexcoordpointer-function"></a>glTexCoordPointer (funzione)

La funzione **glTexCoordPointer** definisce una matrice di coordinate di trama.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glTexCoordPointer(
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

Numero di coordinate per ogni elemento di matrice. Il valore delle *dimensioni* deve essere 1, 2, 3 o 4.

</dd> <dt>

*type* 
</dt> <dd>

Il tipo di dati di ogni coordinata di trama nella matrice usando le costanti simboliche seguenti: **GL \_ short**, **GL \_ int**, **GL \_ float** e **GL \_ Double**.

</dd> <dt>

*stride* 
</dt> <dd>

Offset dei byte tra gli elementi consecutivi della matrice. Quando *stride* è zero, gli elementi della matrice sono strettamente compressi nella matrice.

</dd> <dt>

*indicatore di misura* 
</dt> <dd>

Puntatore alla prima coordinata del primo elemento nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                              | Significato                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>  | il *tipo* non è un valore accettato.<br/> |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl> | *size* non è 1, 2, 3 o 4.<br/>     |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl> | *stride* è negativo.<br/>            |



## <a name="remarks"></a>Commenti

La funzione **glTexCoordPointer** specifica il percorso e i dati di una matrice di coordinate di trama da usare durante il rendering. Il parametro *size* specifica il numero di coordinate usate per ogni elemento della matrice. Il parametro di *tipo* specifica il tipo di dati di ogni coordinata di trama. Il parametro *stride* determina l'offset dei byte da un elemento della matrice alla successiva, abilitando la compressione di vertici e attributi in una singola matrice o archiviazione in matrici separate. In alcune implementazioni, l'archiviazione dei vertici e degli attributi in una singola matrice può essere più efficiente rispetto all'utilizzo di matrici separate. Per ulteriori informazioni, vedere [**glInterleavedArrays**](glinterleavedarrays.md). Quando viene specificata una matrice di coordinate di trama, le dimensioni, il tipo, lo stride e il puntatore vengono salvati sullo stato del lato client.

Una matrice di coordinate di trama viene abilitata quando si specifica la costante della **\_ \_ \_ matrice Coord della trama GL** con [**glEnableClientState**](glenableclientstate.md). Quando Enabled, [**glDrawArrays**](gldrawarrays.md), [**glDrawElements**](gldrawelements.md)e [**glArrayElement**](glarrayelement.md) usano la matrice di coordinate di trama. Per impostazione predefinita, la matrice di coordinate di trama è disabilitata.

Non è possibile includere **glTexCoordPointer** negli elenchi di visualizzazione.

Quando si specifica una matrice di coordinate di trama usando **glTexCoordPointer**, i valori di tutti i parametri della matrice di coordinate di trama della funzione vengono salvati in uno stato lato client ed è possibile memorizzare nella cache elementi statici della matrice. Poiché i parametri della matrice di coordinate di trama sono stati lato client, i relativi valori non vengono salvati né ripristinati da [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).

Sebbene non venga generato alcun errore quando si chiama **glTexCoordPointer** all'interno di coppie [**glBegin**](glbegin.md) e [**glEnd**](glend.md) , i risultati non sono definiti.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glTexCoordPointer**:

[**glIsEnabled**](glisenabled.md) con argomento **GL \_ texture \_ Coord \_ Array**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento **GL \_ texture \_ Coord \_ matrice \_ dimensione**

**glGet** con argomento **GL \_ texture \_ Coord \_ array \_ stride**

**glGet** con argomento **GL \_ texture \_ Coord \_ \_ numero di matrici**

**glGet** con argomento **GL \_ texture \_ Coord \_ \_ tipo matrice**

[**glGetPointerv**](glgetpointerv.md) con argomento **GL \_ trama \_ Coord \_ matrice \_ puntatore**

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

[**glDrawElements**](gldrawelements.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
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

[**glPopClientAttrib**](glpopclientattrib.md)
</dt> <dt>

[**glPushClientAttrib**](glpushclientattrib.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





