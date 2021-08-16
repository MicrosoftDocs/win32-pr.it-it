---
title: Funzione glNormalPointer (Gl.h)
description: La funzione glNormalPointer definisce una matrice di normali.
ms.assetid: 6ffb0522-87cc-4be1-a5b1-f6fd30e04b43
keywords:
- Funzione glNormalPointer OpenGL
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
ms.openlocfilehash: 4f188a65a0a2bff0438188ae7521615de45341147b138a849d2fd375ed8a959b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938410"
---
# <a name="glnormalpointer-function"></a>Funzione glNormalPointer

La **funzione glNormalPointer** definisce una matrice di normali.

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

Tipo di dati di ogni coordinata nella matrice usando le costanti simboliche seguenti: GL \_ BYTE, GL \_ SHORT, GL \_ INT, GL \_ FLOAT e GL \_ DOUBLE.

</dd> <dt>

*Passo* 
</dt> <dd>

Offset di byte tra normali consecutive. Quando *stride* è zero, le normali sono strettamente imballate nella matrice.

</dd> <dt>

*indicatore di misura* 
</dt> <dd>

Puntatore al primo normale nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *il* tipo non è un valore accettato.<br/> |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | *stride* o *count* è negativo.<br/> |



## <a name="remarks"></a>Commenti

La **funzione glNormalPointer** specifica la posizione e i dati di una matrice di normali da usare durante il rendering. Il *parametro* type specifica il tipo di dati di ogni coordinata normale. Il *parametro stride* determina l'offset dei byte da un normale a quello successivo, consentendo la creazione di un pacchetto di vertici e attributi in una singola matrice o archiviazione in matrici separate. In alcune implementazioni l'archiviazione di vertici e attributi in una singola matrice può essere più efficiente rispetto all'uso di matrici separate. Per [**informazioni dettagliate, vedere glInterleavedArrays.**](glinterleavedarrays.md)

Una matrice normale viene abilitata quando si specifica la costante GL \_ NORMAL \_ ARRAY con [**glEnableClientState.**](glenableclientstate.md) Se abilitata, [**glDrawArrays,**](gldrawarrays.md) [**glDrawElements**](gldrawelements.md) e [**glArrayElement**](glarrayelement.md) usano la matrice normale. Per impostazione predefinita, la matrice normale è disabilitata.

Non è possibile includere **glNormalPointer** negli elenchi visualizzati.

Quando si specifica una matrice normale usando **glNormalPointer,** i valori di tutti i parametri di matrice normali della funzione vengono salvati in uno stato lato client. Poiché i parametri di matrice normali vengono salvati in uno stato lato client, i relativi valori non vengono salvati o ripristinati da [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib.**](glpopattrib.md)

Anche se non viene generato alcun errore quando si chiama **glNormalPointer** all'interno delle coppie [**glBegin**](glbegin.md) [**e glEnd,**](glend.md) i risultati non sono definiti.

Le funzioni seguenti sono associate a **glNormalPointer:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ NORMAL \_ ARRAY \_ STRIDE

**glGet** con argomento GL \_ NORMAL \_ ARRAY \_ COUNT

**glGet** con argomento GL \_ NORMAL \_ ARRAY \_ TYPE

**glGetPointerv** con argomento GL \_ NORMAL \_ ARRAY \_ POINTER

[**glIsEnabled con**](glisenabled.md) argomento GL \_ NORMAL \_ ARRAY

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

 

 





