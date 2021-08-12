---
title: Funzione glDrawArrays (Gl.h)
description: La funzione glDrawArrays specifica più primitive di cui eseguire il rendering.
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
keywords:
- Funzione glDrawArrays OpenGL
topic_type:
- apiref
api_name:
- glDrawArrays
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 349ba3407d84d66afd431d14c3fc97b151661f4f783a05734a55d9ba1dc313ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616993"
---
# <a name="gldrawarrays-function"></a>Funzione glDrawArrays

La **funzione glDrawArrays** specifica più primitive di cui eseguire il rendering.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glDrawArrays(
   GLenum  mode,
   GLint   first,
   GLsizei count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mode* 
</dt> <dd>

Tipo di primitive di cui eseguire il rendering. Le costanti seguenti specificano tipi accettabili di primitive: \_ GL POINTS, GL \_ LINE \_ STRIP, GL LINE \_ \_ \_ LOOP, GL LINES, GL \_ TRIANGLE \_ STRIP, GL TRIANGLE \_ \_ FAN, GL \_ TRIANGLES, GL \_ QUAD \_ STRIP, GL \_ QUADS e GL \_ POLYGON.

</dd> <dt>

*first* 
</dt> <dd>

Indice iniziale nelle matrici abilitate.

</dd> <dt>

*count* 
</dt> <dd>

Numero di indici di cui eseguire il rendering.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *count* è negativo.<br/>                                                                                                      |
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *mode* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Con **glDrawArrays** è possibile specificare più primitive geometriche di cui eseguire il rendering. Anziché chiamare funzioni OpenGL separate per passare ogni singolo vertice, normale o colore, è possibile specificare matrici separate di vertici, normali e colori per definire una sequenza di primitive (tutte dello stesso tipo) con una singola chiamata a **glDrawArrays.**

Quando si chiama **glDrawArrays,** gli elementi sequenziali count di ogni matrice abilitata vengono usati per costruire una sequenza di primitive geometriche, a partire dal *primo* elemento.  Il *parametro mode* specifica il tipo di primitiva da costruire e come usare gli elementi della matrice per costruire le primitive.

Dopo **il ritorno di glDrawArrays,** i valori degli attributi dei vertici modificati da **glDrawArrays** non sono definiti. Ad esempio, se GL COLOR ARRAY è abilitato, il valore del colore corrente non è definito dopo \_ \_ il ritorno di **glDrawArrays.** Gli attributi non modificati **da glDrawArrays** rimangono definiti. Quando GL \_ VERTEX ARRAY non è abilitato, non vengono generate primitive geometriche, ma gli attributi corrispondenti alle \_ matrici abilitate vengono modificati.

È possibile includere **glDrawArrays negli** elenchi di visualizzazione. Quando si include **glDrawArrays** in un elenco di visualizzazione, i dati di matrice necessari, determinati dai puntatori di matrice e da enables, vengono generati e immessi nell'elenco di visualizzazione. I valori dei puntatori a matrice e di abilita vengono determinati durante la creazione di elenchi di visualizzazione.

È possibile leggere i dati di matrice statici in qualsiasi momento. Se vengono modificati elementi statici della matrice e la matrice non viene specificata di nuovo, i risultati di tutte le chiamate successive a **glDrawArrays** non sono definiti.

Anche se non viene generato alcun errore quando si specifica una matrice più di una volta all'interno di [**coppie glBegin**](glbegin.md) e [**arrayd,**](glend.md) i risultati non sono definiti.

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

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





