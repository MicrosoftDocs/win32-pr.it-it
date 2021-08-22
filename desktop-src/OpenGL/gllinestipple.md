---
title: Funzione glLineStipple (Gl.h)
description: La funzione glLineStipple specifica il modello di punta della riga.
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
keywords:
- Funzione glLineStipple OpenGL
topic_type:
- apiref
api_name:
- glLineStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f350611afa0621c1bf883e8f2ac7dc24e50362912296f15d1443e2c638b7bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493021"
---
# <a name="gllinestipple-function"></a>Funzione glLineStipple

La **funzione glLineStipple** specifica il modello di punta della riga.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glLineStipple(
   GLint    factor,
   GLushort pattern
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Fattore* 
</dt> <dd>

Moltiplicatore per ogni bit nel modello di punta della riga. Se *il* fattore è 3, ad esempio, ogni bit nel modello verrà usato tre volte prima che venga usato il bit successivo nel modello. Il *parametro factor* è impostato sull'intervallo \[ 1, 256 e il \] valore predefinito è uno.

</dd> <dt>

*pattern* 
</dt> <dd>

Intero a 16 bit il cui modello di bit determina quali frammenti di una linea verranno disegnati quando la linea viene rasterizzata. Il bit zero viene usato per primo e il modello predefinito è tutti uno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glLineStipple** specifica il modello di punta della riga. Lo stippling delle linee maschera alcuni frammenti prodotti dalla rasterizzazione; questi frammenti non verranno disegnati. La maschera viene ottenuta usando tre parametri: il modello a 16 bit dello stipple di *riga,* il fattore di conteggio delle ripetizioni e un contatore dello stipple *integer.*

I *contatori* vengono reimpostati su zero ogni volta che viene chiamato [**glBegin**](glbegin.md) e prima che venga generato ogni segmento di riga di una sequenza **glBegin**(GL \_ LINES)/glEnd. Viene incrementato dopo la generazione di ogni frammento di un segmento di linea con alias di larghezza unità o dopo la generazione di ogni *frammento i* di un segmento di linea di larghezza *i.* I *frammenti i* associati a count *s* vengono mascherati se il bit *del* modello (*s*  /  *factor*) mod 16 è zero. In caso contrario, questi frammenti vengono inviati al framebuffer. Il bit zero *di pattern* è il bit meno significativo.

Le linee antialias vengono considerate come una sequenza di rettangoli di larghezza 1x ai fini dello stippling. Il *rettangolo s* viene rasterizzato o meno in base alla regola del frammento descritta per le linee con alias. conta rettangoli anziché gruppi di frammenti.

Lo stippling delle righe è abilitato o disabilitato usando [**glEnable**](glenable.md) **e glDisable con** l'argomento GL \_ LINE \_ STIPPLE. Se abilitata, il modello di punta della linea viene applicato come descritto in precedenza. Quando è disabilitato, è come se il modello fosse tutto uno. Inizialmente, lo stippling delle righe è disabilitato.

Le funzioni seguenti recuperano informazioni correlate a **glLineStipple:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ LINE \_ STIPPLE \_ PATTERN

**glGet con** argomento GL \_ LINE \_ STIPPLE \_ REPEAT

[**glIsEnabled con**](glisenabled.md) argomento GL \_ LINE \_ STIPPLE

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

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> </dl>

 

 





