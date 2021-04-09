---
title: funzione glEdgeFlagPointer (GL. h)
description: La funzione glEdgeFlagPointer definisce una matrice di flag perimetrali.
ms.assetid: e0e7e442-533d-4c41-addd-a215ce0b1c56
keywords:
- funzione glEdgeFlagPointer OpenGL
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
ms.openlocfilehash: 4390a9838fef418763aa4bcafbf815ab0cdf3466
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742207"
---
# <a name="gledgeflagpointer-function"></a>glEdgeFlagPointer (funzione)

La funzione **glEdgeFlagPointer** definisce una matrice di flag perimetrali.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glEdgeFlagPointer(
         GLsizei stride,
   const GLvoid  *pointer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*stride* 
</dt> <dd>

Offset dei byte tra i flag Edge consecutivi. Quando *stride* è zero, i flag perimetrali sono strettamente compressi nella matrice.

</dd> <dt>

*indicatore di misura* 
</dt> <dd>

Puntatore al primo flag di bordo nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                             | Significato                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl> | *stride* o *count* è negativo.<br/> |



## <a name="remarks"></a>Commenti

La funzione **glEdgeFlagPointer** specifica il percorso e i dati di una matrice di flag perimetrali booleani da usare durante il rendering. Il parametro *stride* determina l'offset dei byte da un flag Edge a quello successivo, che consente di comprimere i vertici e gli attributi in una singola matrice o nello spazio di archiviazione in matrici separate. In alcune implementazioni, l'archiviazione dei vertici e degli attributi in una singola matrice può essere più efficiente rispetto all'utilizzo di matrici separate.

Una matrice di flag Edge viene abilitata quando si specifica la \_ \_ costante array del flag di bordo GL \_ con [**glEnableClientState**](glenableclientstate.md). Se abilitata, [**glDrawArrays**](gldrawarrays.md) o [**glArrayElement**](glarrayelement.md) usa la matrice del flag Edge. Per impostazione predefinita, la matrice del flag Edge è disabilitata.

Usare **glDrawArrays** per costruire una sequenza di primitive (tutti dello stesso tipo) dalle matrici di attributi Vertex e vertex specificati. Usare **glArrayElement** per specificare le primitive indicizzando i vertici e gli attributi dei vertici e [**glDrawElements**](gldrawelements.md) per costruire una sequenza di primitive indicizzando i vertici e gli attributi dei vertici.

Non è possibile includere **glEdgeFlagPointer** negli elenchi di visualizzazione.

Quando si specifica una matrice di flag Edge usando **glEdgeFlagPointer**, i valori di tutti i parametri della matrice del flag Edge della funzione vengono salvati in uno stato lato client e gli elementi della matrice statica possono essere memorizzati nella cache. Poiché i parametri della matrice del flag Edge sono in uno stato lato client, [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) non salvano o ripristinano i valori.

Sebbene la chiamata a **glEdgeFlagPointer** all'interno di una coppia [**glBegin**](glbegin.md) / [**glEnd**](glend.md) non generi un errore, i risultati non sono definiti.

Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glEdgeFlagPointer** :

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento di \_ matrice di flag Edge GL \_ \_ \_ stride

**glGet** con argomento \_ numero di \_ matrici di flag Edge \_ \_

[](glgetpointerv.md) puntatore alla matrice del \_ flag Edge GL dell'argomento glGetPointerv \_ \_ \_

[**glIsEnabled**](glisenabled.md) con argomento \_ matrice di \_ flag \_ Edge GL

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

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEnableClientState**](glenableclientstate.md)
</dt> <dt>

[**Remo**](glend.md)
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

 

 





