---
title: Funzione glGetMapfv (Gl.h)
description: Le funzioni glGetMapdv, glGetMapfv e glGetMapiv restituiscono parametri dell'analizzatore. | Funzione glGetMapfv (Gl.h)
ms.assetid: dc93e468-7b76-4b5d-a46c-63920ed05568
keywords:
- Funzione glGetMapfv OpenGL
topic_type:
- apiref
api_name:
- glGetMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1bedb1b5ff07b7331eb740c46392e80ad324c6cef7f843978d9a5a41edf8da1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741591"
---
# <a name="glgetmapfv-function"></a>Funzione glGetMapfv

Le [**funzioni glGetMapdv**](glgetmapdv.md), **glGetMapfv** e [**glGetMapiv**](glgetmapiv.md) restituiscono parametri dell'analizzatore.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glGetMapfv(
   GLenum  target,
   GLenum  query,
   GLfloat *v
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Nome simbolico di una mappa. I valori accettati sono i seguenti: GL \_ MAP1 \_ COLOR \_ 4, GL \_ MAP1 \_ INDEX, GL \_ MAP1 \_ NORMAL, GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 3, \_ GL MAP1 TEXTURE \_ \_ COORD \_ 4, \_ GL \_ MAP1 VERTEX \_ 3, GL \_ MAP1 \_ VERTEX \_ 4, \_ GL MAP2 COLOR \_ \_ 4, GL \_ MAP2 \_ INDEX, GL \_ MAP2 \_ NORMAL, GL \_ MAP2 TEXTURE \_ \_ \_ COORD 1, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 2, GL \_ \_ MAP2 TEXTURE \_ COORD \_ 3, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 4, GL \_ MAP2 \_ VERTEX 3 e \_ GL \_ MAP2 \_ VERTEX \_ 4.

</dd> <dt>

*query* 
</dt> <dd>

Specifica il parametro da restituire. Vengono accettati i nomi simbolici seguenti.



| Valore                                                                                                                                             | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <dt>**GL \_ COEFF**</dt> </dl>    | Il *parametro v* restituisce i punti di controllo per la funzione dell'analizzatore. Gli analizzatori unidimensionali *restituiscono* punti di controllo dell'ordine e gli analizzatori bidimensionali restituiscono punti di controllo *uorder* *x* *vorder.* Ogni punto di controllo è costituito da uno, due, tre o quattro valori integer, a virgola mobile a precisione singola o a precisione doppia, a seconda del tipo dell'analizzatore. I punti di controllo bidimensionali vengono restituiti nell'ordine principale della riga, incrementando rapidamente l'indice *dell'ordine* utente e l'indice *vorder* dopo ogni riga. I valori interi, quando richiesti, vengono calcolati arrotondando i valori a virgola mobile interni ai valori interi più vicini.<br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <dt>**ORDINE \_ GL**</dt> </dl>    | Il *parametro v* restituisce l'ordine della funzione dell'analizzatore. Gli analizzatori unidimensionali restituiscono un singolo valore, *order*. Gli analizzatori bidimensionali restituiscono due valori, *uorder* e *vorder.*<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <dt>**DOMINIO \_ GL**</dt> </dl> | Il *parametro v* restituisce i parametri di mapping *lineari u* e *v.* Gli analizzatori unidimensionali restituiscono due valori, *u* 1 e *u* 2, come specificato da [**glMap1.**](glmap1.md) Gli analizzatori bidimensionali restituiscono quattro valori (*u1*, *u2*, *v1* e *v2*) come specificato da [**glMap2**](glmap2.md). I valori interi, quando richiesti, vengono calcolati arrotondando i valori a virgola mobile interni ai valori interi più vicini.<br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

*v* 
</dt> <dd>

Restituisce i dati richiesti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *target* o *query* non è un valore accettato.<br/>                                                                             |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glGetMap** restituisce i parametri dell'analizzatore. Le **funzioni glMap1** e **glMap2** definiscono gli analizzatori. Il *parametro target* specifica una mappa, la *query* seleziona un parametro specifico e *v* punta all'archiviazione in cui verranno restituiti i valori.

I valori accettabili per il *parametro di* destinazione sono descritti in [**glMap1**](glmap1.md) e [**glMap2.**](glmap2.md)

Se viene generato un errore, non viene apportata alcuna modifica al contenuto di *v*.

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





