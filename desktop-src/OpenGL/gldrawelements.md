---
title: Funzione glDrawElements (Gl.h)
description: La funzione glDrawElements esegue il rendering delle primitive dai dati della matrice.
ms.assetid: fb433294-106e-48d5-ad49-4434934fe072
keywords:
- Funzione glDrawElements OpenGL
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
ms.openlocfilehash: b260c1112f7ec588b4d83655e5d0aa465b63682164f2ca745b63d3f421e5794c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616573"
---
# <a name="gldrawelements-function"></a>Funzione glDrawElements

La **funzione glDrawElements** esegue il rendering delle primitive dai dati della matrice.

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

Tipo di primitive di cui eseguire il rendering. Può presupporre uno dei valori simbolici seguenti: GL \_ POINTS, GL \_ LINE \_ STRIP, GL \_ LINE \_ LOOP, GL LINE \_ LINES, GL TRIANGLE \_ \_ STRIP, GL TRIANGLE \_ \_ FAN, GL \_ TRIANGLES, GL \_ QUAD \_ STRIP, GL \_ QUADS e GL \_ POLYGON.

</dd> <dt>

*count* 
</dt> <dd>

Numero di elementi di cui eseguire il rendering.

</dd> <dt>

*type* 
</dt> <dd>

Tipo dei valori negli indici. Deve essere di TIPO GL \_ UNSIGNED \_ BYTE, GL \_ UNSIGNED \_ SHORT o GL \_ UNSIGNED \_ INT.

</dd> <dt>

*Indici* 
</dt> <dd>

Puntatore alla posizione in cui sono archiviati gli indici.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *mode* non è un valore accettato.<br/>                                                                                          |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *count* è un valore negativo.<br/>                                                                                              |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glDrawElements** consente di specificare più primitive geometriche con pochissime chiamate di funzione. Anziché chiamare una funzione OpenGL per passare in anticipo ogni singolo vertice, normale o colore, è possibile specificare matrici separate di vertici, normali e colori e usarle per definire una sequenza di primitive (tutte dello stesso tipo) con una singola chiamata a **glDrawElements**.

Quando si chiama la **funzione glDrawElements,** usa gli elementi sequenziali count dagli *indici* per costruire una sequenza di primitive geometriche.  Il *parametro mode* specifica il tipo di primitive costruite e il modo in cui gli elementi della matrice vengono usati per costruire queste primitive. Se GL \_ VERTEX \_ ARRAY non è abilitato, non vengono generate primitive geometriche.

Gli attributi dei vertici modificati da **glDrawElements** hanno un valore non specificato dopo il ritorno **di glDrawElements.** Ad esempio, se GL COLOR ARRAY è abilitato, il valore del colore corrente non è definito dopo l'esecuzione di \_ \_ **glDrawElements.** Gli attributi che non vengono modificati rimangono invariati.

È possibile includere la **funzione glDrawElements** negli elenchi di visualizzazione. Quando **glDrawElements** è incluso in un elenco di visualizzazione, nell'elenco di visualizzazione vengono immessi anche i dati di matrice necessari (determinati dai puntatori di matrice e abilitati). Poiché i puntatori di matrice e abilita sono variabili di stato sul lato client, i relativi valori influiscono sugli elenchi di visualizzazione quando vengono creati gli elenchi, non quando gli elenchi vengono eseguiti.

> [!Note]  
> La **funzione glDrawElements** è disponibile solo in OpenGL versione 1.1 o successiva.

 

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

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnd**](glend.md)
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

 

 





