---
title: funzione glDrawElements (GL. h)
description: La funzione glDrawElements esegue il rendering di primitive da dati di matrice.
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
keywords:
- funzione glDrawElements OpenGL
topic_type:
- apiref
api_name:
- glDrawElements
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976e779235dc330467d610406156534b5e72841d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518100"
---
# <a name="gldrawelements-function"></a>glDrawElements (funzione)

La funzione **glDrawElements** esegue il rendering di primitive da dati di matrice.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glDrawElements(
         GLenum  mode,
         GLsizei count,
         GLenum  type,
   const GLvoid  *indices
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mode* 
</dt> <dd>

Tipo di primitive di cui eseguire il rendering. Può assumere uno dei valori simbolici seguenti: GL \_ Points, GL \_ line \_ Strip, GL \_ line \_ loop, GL \_ Lines, GL \_ triangolo \_ Strip, GL \_ Triangle \_ fan, GL \_ triangoli, GL \_ Quad \_ Strip, GL \_ Quads e GL \_ Polygon.

</dd> <dt>

*count* 
</dt> <dd>

Numero di elementi di cui eseguire il rendering.

</dd> <dt>

*type* 
</dt> <dd>

Tipo dei valori negli indici. Deve essere uno dei byte senza segno GL, GL unsigned \_ \_ \_ \_ short o GL \_ unsigned \_ int.

</dd> <dt>

*indici* 
</dt> <dd>

Puntatore alla posizione in cui vengono archiviati gli indici.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *modalità* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *count* è un valore negativo.<br/>                                                                                              |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glDrawElements** consente di specificare più primitive geometriche con pochissime chiamate di funzione. Anziché chiamare una funzione OpenGL per passare ogni singolo vertice, normale o colore, è possibile specificare in anticipo matrici separate di vertici, normali e colori e usarle per definire una sequenza di primitive (tutti dello stesso tipo) con una singola chiamata a **glDrawElements**.

Quando si chiama la funzione **glDrawElements** , viene usato il *conteggio* degli elementi sequenziali degli *indici* per costruire una sequenza di primitive geometriche. Il parametro *mode* specifica il tipo di primitive da costruire e la modalità di utilizzo degli elementi di matrice per costruire tali primitive. Se \_ \_ la matrice di vertici GL non è abilitata, non viene generata alcuna primitiva geometrica.

Gli attributi Vertex modificati da **glDrawElements** hanno un valore non specificato dopo la restituzione di **glDrawElements** . Se, ad esempio, \_ \_ la matrice di colori GL è abilitata, il valore del colore corrente non è definito dopo l'esecuzione di **glDrawElements** . Gli attributi che non vengono modificati rimangono invariati.

È possibile includere la funzione **glDrawElements** negli elenchi di visualizzazione. Quando **glDrawElements** è incluso in un elenco di visualizzazione, vengono immessi anche i dati di matrice necessari, determinati dai puntatori alla matrice e abilitati, nell'elenco di visualizzazione. Poiché i puntatori di matrice e le abilitazioni sono variabili di stato sul lato client, i relativi valori influiscono sugli elenchi di visualizzazione quando vengono creati gli elenchi, non quando vengono eseguiti gli elenchi.

> [!Note]  
> La funzione **glDrawElements** è disponibile solo in OpenGL versione 1,1 o successiva.

 

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

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGetPointerv**](glgetpointerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glVertexPointer**](glvertexpointer.md)
</dt> </dl>

 

 





