---
title: Funzione glTexCoordPointer (Gl.h)
description: La funzione glTexCoordPointer definisce una matrice di coordinate di trama.
ms.assetid: c3640a1b-ccc7-4f1a-94a5-a164f7377dbc
keywords:
- Funzione glTexCoordPointer OpenGL
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
ms.openlocfilehash: 0892f06b3fd5027939710be9ac74a2ae18c0dc0d712572d094b9a54fd6bb5b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888251"
---
# <a name="gltexcoordpointer-function"></a>Funzione glTexCoordPointer

La **funzione glTexCoordPointer** definisce una matrice di coordinate di trama.

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

Numero di coordinate per ogni elemento della matrice. Il valore *di size* deve essere 1, 2, 3 o 4.

</dd> <dt>

*type* 
</dt> <dd>

Tipo di dati di ogni coordinata di trama nella matrice usando le costanti simboliche seguenti: **GL \_ SHORT,** **GL \_ INT,** **GL \_ FLOAT** e **GL \_ DOUBLE.**

</dd> <dt>

*Passo* 
</dt> <dd>

Offset di byte tra elementi consecutivi della matrice. Quando *stride* è zero, gli elementi della matrice sono strettamente imballati nella matrice.

</dd> <dt>

*indicatore di misura* 
</dt> <dd>

Puntatore alla prima coordinata del primo elemento nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                              | Significato                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>  | *type* non è un valore accettato.<br/> |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl> | *size* non è 1, 2, 3 o 4.<br/>     |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl> | *stride* è stato negativo.<br/>            |



## <a name="remarks"></a>Commenti

La **funzione glTexCoordPointer** specifica la posizione e i dati di una matrice di coordinate di trama da usare durante il rendering. Il *parametro size* specifica il numero di coordinate usate per ogni elemento della matrice. Il *parametro di* tipo specifica il tipo di dati di ogni coordinata di trama. Il *parametro stride* determina l'offset dei byte da un elemento della matrice a quello successivo, consentendo la creazione di un pacchetto di vertici e attributi in una singola matrice o archiviazione in matrici separate. In alcune implementazioni l'archiviazione dei vertici e degli attributi in una singola matrice può essere più efficiente rispetto all'uso di matrici separate. Per altre informazioni, vedere [**glInterleavedArrays**](glinterleavedarrays.md). Quando viene specificata una matrice di coordinate di trama, le dimensioni, il tipo, lo stride e il puntatore vengono salvati sullo stato lato client.

Una matrice di coordinate di trama viene abilitata quando si specifica la costante **GL \_ TEXTURE \_ COORD \_ ARRAY** [**con glEnableClientState**](glenableclientstate.md). Se abilitata, [**glDrawArrays,**](gldrawarrays.md) [**glDrawElements**](gldrawelements.md)e [**glArrayElement**](glarrayelement.md) usano la matrice di coordinate della trama. Per impostazione predefinita, la matrice di coordinate della trama è disabilitata.

Non è possibile includere **glTexCoordPointer** negli elenchi di visualizzazione.

Quando si specifica una matrice di coordinate di trama usando **glTexCoordPointer,** i valori di tutti i parametri della matrice di coordinate di trama della funzione vengono salvati in uno stato lato client e gli elementi statici della matrice possono essere memorizzati nella cache. Poiché i parametri della matrice di coordinate della trama sono sullo stato lato client, i relativi valori non vengono salvati o ripristinati da [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md).

Anche se non viene generato alcun errore quando si chiama **glTexCoordPointer all'interno** delle coppie [**glBegin**](glbegin.md) e [**glEnd,**](glend.md) i risultati non sono definiti.

Le funzioni seguenti recuperano informazioni correlate **a glTexCoordPointer:**

[**glIsEnabled con**](glisenabled.md) argomento **GL TEXTURE \_ \_ COORD \_ ARRAY**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento **GL TEXTURE \_ \_ COORD \_ ARRAY \_ SIZE**

**glGet con** argomento **GL TEXTURE \_ \_ COORD \_ ARRAY \_ STRIDE**

**glGet con** argomento **GL TEXTURE \_ \_ COORD \_ ARRAY \_ COUNT**

**glGet con** argomento **GL TEXTURE \_ \_ COORD \_ ARRAY \_ TYPE**

[**glGetPointerv con**](glgetpointerv.md) argomento **GL TEXTURE \_ \_ COORD \_ ARRAY \_ POINTER**

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

 

 





