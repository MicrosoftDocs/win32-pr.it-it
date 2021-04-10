---
title: funzione glDrawArrays (GL. h)
description: La funzione glDrawArrays specifica più primitive per il rendering.
ms.assetid: 6ebd467b-5a63-43e4-b3fd-242c704d7d13
keywords:
- funzione glDrawArrays OpenGL
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
ms.openlocfilehash: 88b20cf3a3e3b2c96a8172f53f8126815efe16d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964352"
---
# <a name="gldrawarrays-function"></a>glDrawArrays (funzione)

La funzione **glDrawArrays** specifica più primitive per il rendering.

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

Tipo di primitive di cui eseguire il rendering. Le costanti seguenti specificano tipi accettabili di primitive: \_ punti GL, \_ Strip linea GL \_ , \_ ciclo di riga GL, \_ \_ linee GL, striscia del \_ triangolo GL \_ , ventola del \_ triangolo GL \_ , \_ triangoli GL, GL \_ Quad \_ Strip, GL \_ quad e GL \_ Polygon.

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

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *conteggio* negativo.<br/>                                                                                                      |
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *modalità* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Con **glDrawArrays** è possibile specificare più primitive geometriche di cui eseguire il rendering. Anziché chiamare funzioni OpenGL separate per passare ogni singolo vertice, normale o colore, è possibile specificare matrici separate di vertici, normali e colori per definire una sequenza di primitive (tutti dello stesso tipo) con una singola chiamata a **glDrawArrays**.

Quando si chiama **glDrawArrays**, i *conteggi* degli elementi sequenziali di ogni matrice abilitata vengono usati per costruire una sequenza di primitive geometriche, a partire dal *primo* elemento. Il parametro *mode* specifica il tipo di primitiva da costruire e come usare gli elementi della matrice per costruire le primitive.

Dopo la restituzione di **glDrawArrays** , i valori degli attributi Vertex modificati da **glDrawArrays** non sono definiti. Se, ad esempio, \_ \_ la matrice di colori GL è abilitata, il valore del colore corrente non è definito dopo che **glDrawArrays** restituisce. Gli attributi non modificati da **glDrawArrays** rimangono definiti. Quando \_ \_ la matrice di vertici GL non è abilitata, non viene generata alcuna primitiva geometrica, ma gli attributi corrispondenti alle matrici abilitate vengono modificati.

È possibile includere **glDrawArrays** negli elenchi di visualizzazione. Quando si include **glDrawArrays** in un elenco di visualizzazione, i dati di matrice necessari, determinati dai puntatori della matrice e da abilitati, vengono generati e immessi nell'elenco di visualizzazione. I valori dei puntatori di matrice e di abilitazione vengono determinati durante la creazione degli elenchi di visualizzazione.

È possibile leggere i dati della matrice statica in qualsiasi momento. Se gli elementi di una matrice statica vengono modificati e la matrice non viene specificata nuovamente, i risultati di qualsiasi chiamata successiva a **glDrawArrays** non saranno definiti.

Sebbene non venga generato alcun errore quando si specifica una matrice più di una volta all'interno di [**glBegin**](glbegin.md) e delle coppie [**glEnd**](glend.md) , i risultati non sono definiti.

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

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**Remo**](glend.md)
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

 

 





