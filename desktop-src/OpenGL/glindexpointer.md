---
title: Funzione glIndexPointer (Gl.h)
description: La funzione glIndexPointer definisce una matrice di indici dei colori.
ms.assetid: b435d950-1f87-4041-93e4-f1f8786cabdb
keywords:
- Funzione glIndexPointer OpenGL
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
ms.openlocfilehash: e27502420121f7373af5425e8aadffe3641ddec539a4521fe6c6bf55e6d807d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012149"
---
# <a name="glindexpointer-function"></a>Funzione glIndexPointer

La **funzione glIndexPointer** definisce una matrice di indici dei colori.

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

Tipo di dati di ogni indice di colore nella matrice usando le costanti simboliche seguenti: GL \_ SHORT, GL \_ INT, GL \_ FLOAT, GL \_ DOUBLE.

</dd> <dt>

*Passo* 
</dt> <dd>

Offset dei byte tra indici di colore consecutivi. Quando *stride* è zero, gli indici dei colori sono strettamente imballati nella matrice.

</dd> <dt>

*indicatore di misura* 
</dt> <dd>

Puntatore al primo indice dei colori nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                              | Significato                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>  | *il* tipo non è un valore accettato.<br/> |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl> | *stride* o *count* è negativo.<br/> |



## <a name="remarks"></a>Commenti

La **funzione glIndexPointer** specifica la posizione e i dati di una matrice di indici di colore da usare durante il rendering. Il  parametro type specifica il tipo di dati di ogni indice di colore e *stride* determina l'offset dei byte da un indice di colore a quello successivo, consentendo la creazione di un pacchetto di vertici e attributi in una singola matrice o archiviazione in matrici separate. In alcune implementazioni l'archiviazione dei vertici e degli attributi in una singola matrice può essere più efficiente rispetto all'uso di matrici separate. Per altre informazioni, vedere [**glInterleavedArrays.**](glinterleavedarrays.md)

Una matrice color-index viene abilitata quando si specifica la costante GL \_ INDEX \_ ARRAY con [**glEnableClientState.**](glenableclientstate.md) Se abilitati, [**glDrawArrays**](gldrawarrays.md) e [**glArrayElement**](glarrayelement.md) usano la matrice color-index. Per impostazione predefinita, la matrice color-index è disabilitata.

Non è possibile includere **glIndexPointer** negli elenchi visualizzati.

Quando si specifica una matrice color-index usando **glIndexPointer,** i valori di tutti i parametri della matrice color-index della funzione vengono salvati in uno stato lato client e gli elementi statici della matrice possono essere memorizzati nella cache. Poiché i parametri della matrice color-index sono sullo stato lato client, i relativi valori non vengono salvati o ripristinati da [**glPushAttrib**](glpushattrib.md) e **glPopAttrib.**

Anche se non viene generato alcun errore quando si chiama **glIndexPointer** all'interno delle coppie [**glBegin**](glbegin.md) **e glEnd,** i risultati non sono definiti.

Le funzioni seguenti recuperano informazioni correlate **a glIndexPointer:**

[**glIsEnabled con**](glisenabled.md) argomento GL \_ INDEX \_ ARRAY

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ INDEX ARRAY \_ \_ STRIDE

**glGet** con argomento GL \_ INDEX \_ ARRAY \_ COUNT

**glGet** con argomento GL \_ INDEX \_ ARRAY \_ TYPE

**glGet** con argomento GL \_ INDEX \_ ARRAY \_ SIZE

[**glGetPointerv**](glgetpointerv.md) con argomento GL \_ INDEX \_ ARRAY \_ POINTER

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

 

 





