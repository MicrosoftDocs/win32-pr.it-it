---
title: funzione glGetMapdv (GL. h)
description: Le funzioni glGetMapdv, glGetMapfv e glGetMapiv restituiscono parametri di valutazione. | funzione glGetMapdv (GL. h)
ms.assetid: 3b4fc03b-ada4-4f4a-a234-fa6439f2e5c8
keywords:
- funzione glGetMapdv OpenGL
topic_type:
- apiref
api_name:
- glGetMapdv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf7dd5104ce7a47b0d1215221c115a7191f4548
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321421"
---
# <a name="glgetmapdv-function"></a>glGetMapdv (funzione)

Le funzioni **glGetMapdv**, [**glGetMapfv**](glgetmapfv.md)e [**glGetMapiv**](glgetmapiv.md) restituiscono parametri di valutazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetMapdv(
   GLenum   target,
   GLenum   query,
   GLdouble *v
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Nome simbolico di una mappa. I valori accettati sono i seguenti: GL \_ Mappa1 \_ Color \_ 4, GL \_ Mappa1 \_ index, GL \_ Mappa1 \_ Normal, GL \_ Mappa1 \_ texture \_ Coord \_ 1, GL \_ Mappa1 \_ texture \_ Coord \_ 2, GL \_ MAPPA1 \_ texture \_ Coord \_ 3, GL \_ MAPPA1 \_ texture \_ Coord \_ 4, GL \_ Mappa1 \_ Vertex \_ 3, GL \_ Mappa1 \_ Vertex \_ 4, GL \_ map2 \_ Color \_ 4, GL \_ map2 \_ index, GL \_ map2 \_ Normal, GL \_ map2 \_ texture \_ Coord \_ 1, GL \_ map2 \_ texture \_ Coord \_ 2, GL \_ MAP2 texture \_ \_ Coord \_ 3, GL \_ map2 \_ texture \_ Coord \_ 4, GL \_ map2 \_ Vertex \_ 3 e GL \_ map2 \_ Vertex \_ 4.

</dd> <dt>

*query* 
</dt> <dd>

Specifica il parametro da restituire. I nomi simbolici seguenti sono accettati.



| Valore                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <dt>**\_Coeff GL**</dt> </dl>    | Il parametro *v* restituisce i punti di controllo per la funzione di valutazione. Gli analizzatori unidimensionali restituiscono punti di controllo degli *ordini* e gli analizzatori bidimensionali restituiscono punti di controllo *uorder* *x* *Vorder* . Ogni punto di controllo è costituito da un valore a virgola mobile a precisione singola, a due, tre o quattro, a virgola mobile e precisione doppia, a seconda del tipo di analizzatore. I punti di controllo bidimensionali vengono restituiti in ordine di riga, incrementando rapidamente l'indice *uorder* e l'indice *Vorder* dopo ogni riga. I valori integer, se richiesti, vengono calcolati mediante l'arrotondamento dei valori a virgola mobile interni ai valori integer più vicini.<br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <dt>**\_ordine GL**</dt> </dl>    | Il parametro *v* restituisce l'ordine della funzione dell'analizzatore. Gli analizzatori unidimensionali restituiscono un singolo valore, *Order*. Gli analizzatori bidimensionali restituiscono due valori, *uorder* e *Vorder*.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <dt>**\_dominio GL**</dt> </dl> | Il parametro *v* restituisce i parametri di mapping *u* e *v* lineari. Gli analizzatori unidimensionali restituiscono due valori, *u* 1 e *u* 2, come specificato da [**glMap1**](glmap1.md). Gli analizzatori bidimensionali restituiscono quattro valori (*U1*, *U2*, *V1* e *v2*) come specificato da [**glMap2**](glmap2.md). I valori integer, se richiesti, vengono calcolati mediante l'arrotondamento dei valori a virgola mobile interni ai valori integer più vicini.<br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

*v* 
</dt> <dd>

Restituisce i dati richiesti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *target* o *query* non è un valore accettato.<br/>                                                                             |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glGetMap** restituisce i parametri dell'analizzatore. Le funzioni **glMap1** e **glMap2** definiscono gli analizzatori. Il parametro *target* specifica una mappa, *query* seleziona un parametro specifico e *v* punta alla risorsa di archiviazione in cui verranno restituiti i valori.

I valori accettabili per il parametro di *destinazione* sono descritti in [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md).

Se viene generato un errore, non viene apportata alcuna modifica al contenuto di *v*.

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





