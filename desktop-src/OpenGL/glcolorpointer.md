---
title: Funzione glColorPointer (Gl.h)
description: La funzione glColorPointer definisce una matrice di colori.
ms.assetid: 4d9d05fb-691d-4b71-b079-c42dc7103055
keywords:
- Funzione glColorPointer OpenGL
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
ms.openlocfilehash: b8e08f046cc1bd41293a076f36389506320e85025e415b264bed1ed0de14f9a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081711"
---
# <a name="glcolorpointer-function"></a>Funzione glColorPointer

La **funzione glColorPointer** definisce una matrice di colori.

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

Tipo di dati di ogni componente colore in una matrice di colori. I tipi di dati accettabili vengono specificati con le costanti seguenti: \_ GL BYTE, GL \_ UNSIGNED \_ BYTE, GL \_ SHORT, GL \_ UNSIGNED \_ SHORT, GL \_ INT, GL \_ UNSIGNED \_ INT, GL \_ FLOAT o GL \_ DOUBLE.

</dd> <dt>

*Passo* 
</dt> <dd>

Offset dei byte tra colori consecutivi. Quando *stride* è zero, i colori sono strettamente imballati nella matrice.

</dd> <dt>

*indicatore di misura* 
</dt> <dd>

Puntatore al primo componente del primo elemento colore in una matrice di colori.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                              | Significato                                      |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl> | *size* non è 3 o 4.<br/>            |
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>  | *il* tipo non è un valore accettato.<br/> |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl> | *stride* o *count* è negativo.<br/> |



## <a name="remarks"></a>Commenti

La **funzione glColorPointer** specifica la posizione e il formato dei dati di una matrice di componenti di colore da usare durante il rendering. Il *parametro stride* determina l'offset dei byte da un colore a quello successivo, consentendo la creazione di un pacchetto di attributi vertice in una singola matrice o archiviazione in matrici separate. In alcune implementazioni l'archiviazione degli attributi dei vertici in una singola matrice può essere più efficiente rispetto all'uso di matrici separate.

È stata abilitata la matrice di colori specificando la \_ costante GL COLOR ARRAY con \_ [**glEnableClientState.**](glenableclientstate.md) Chiamando [**glArrayElement**](glarrayelement.md), [**glDrawElements**](gldrawelements.md)o [**glDrawArrays**](gldrawarrays.md) viene utilizzata la matrice di colori abilitata. Per impostazione predefinita, la matrice di colori è disabilitata. Le **chiamate glColorPointer** non possono essere immesse negli elenchi di visualizzazione.

Quando si specifica una matrice di colori usando **glColorPointer,** i valori di tutti i parametri della matrice di colori della funzione vengono salvati in uno stato lato client ed è possibile memorizzare nella cache gli elementi statici della matrice. Poiché i parametri della matrice di colori sono in uno stato lato client, [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) non salvano o ripristinano i valori dei parametri.

Anche se la specifica della matrice di colori [**all'interno di glBegin**](glbegin.md) [**e delle coppie di colori non**](glend.md) genera un errore, i risultati non sono definiti.

Le funzioni seguenti recuperano informazioni correlate alla **funzione glColorPointer:**

[**glIsEnabled con**](glisenabled.md) argomento GL \_ COLOR \_ ARRAY

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ COLOR ARRAY \_ \_ SIZE

**glGet** con argomento GL \_ COLOR \_ ARRAY \_ TYPE

**glGet con** argomento GL \_ COLOR ARRAY \_ \_ STRIDE

**glGet con** argomento GL \_ COLOR ARRAY \_ \_ COUNT

[**glGetPointerv con**](glgetpointerv.md) argomento GL \_ COLOR ARRAY \_ \_ POINTER

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
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

 

 





