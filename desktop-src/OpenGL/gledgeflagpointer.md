---
title: Funzione glEdgeFlagPointer (Gl.h)
description: La funzione glEdgeFlagPointer definisce una matrice di flag perimetrali.
ms.assetid: e0e7e442-533d-4c41-addd-a215ce0b1c56
keywords:
- Funzione glEdgeFlagPointer OpenGL
topic_type:
- apiref
api_name:
- glEdgeFlagPointer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa648a15542a3f3f2f35f577760991da74bc978c0464c1373c8eddea38941a62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061639"
---
# <a name="gledgeflagpointer-function"></a>Funzione glEdgeFlagPointer

La **funzione glEdgeFlagPointer** definisce una matrice di flag perimetrali.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glEdgeFlagPointer(
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Passo* 
</dt> <dd>

Offset di byte tra flag di bordo consecutivi. Quando *stride* è zero, i flag edge sono strettamente imballati nella matrice.

</dd> <dt>

*indicatore di misura* 
</dt> <dd>

Puntatore al primo flag di bordo nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                             | Significato                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | *stride* o *count* è negativo.<br/> |



## <a name="remarks"></a>Commenti

La **funzione glEdgeFlagPointer** specifica la posizione e i dati di una matrice di flag di bordo booleani da usare durante il rendering. Il *parametro stride* determina l'offset di byte da un flag edge a quello successivo, che consente la creazione di un pacchetto di vertici e attributi in una singola matrice o archiviazione in matrici separate. In alcune implementazioni l'archiviazione dei vertici e degli attributi in una singola matrice può essere più efficiente rispetto all'uso di matrici separate.

Una matrice edge-flag viene abilitata quando si specifica la costante GL \_ EDGE FLAG ARRAY con \_ \_ [**glEnableClientState**](glenableclientstate.md). Se abilitata, [**glDrawArrays**](gldrawarrays.md) o [**glArrayElement**](glarrayelement.md) usa la matrice edge-flag. Per impostazione predefinita, la matrice edge-flag è disabilitata.

Usare **glDrawArrays** per costruire una sequenza di primitive (tutte dello stesso tipo) da matrici di attributi vertice e vertice prespecificate. Usare **glArrayElement** per specificare primitive indicizzando vertici e attributi dei vertici e [**glDrawElements**](gldrawelements.md) per costruire una sequenza di primitive indicizzando vertici e attributi dei vertici.

Non è possibile includere **glEdgeFlagPointer** negli elenchi di visualizzazione.

Quando si specifica una matrice edge-flag usando **glEdgeFlagPointer,** i valori di tutti i parametri della matrice edge-flag della funzione vengono salvati in uno stato lato client e gli elementi statici della matrice possono essere memorizzati nella cache. Poiché i parametri della matrice edge-flag sono in uno stato lato client, [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) non salvano o ripristinano i relativi valori.

Anche se la **chiamata a glEdgeFlagPointer** all'interno di una coppia [**glBegin**](glbegin.md)non genera un errore, i / [](glend.md) risultati non sono definiti.

Le funzioni seguenti recuperano informazioni correlate alla **funzione glEdgeFlagPointer:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ EDGE FLAG ARRAY \_ \_ \_ STRIDE

**glGet con** argomento GL \_ EDGE FLAG ARRAY \_ \_ \_ COUNT

[**glGetPointerv con**](glgetpointerv.md) argomento GL \_ EDGE FLAG ARRAY \_ \_ \_ POINTER

[**glIsEnabled con**](glisenabled.md) argomento GL \_ EDGE FLAG \_ \_ ARRAY

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
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

[**glPopAttrib**](glpopattrib.md)
</dt> <dt>

[**glPushAttrib**](glpushattrib.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





