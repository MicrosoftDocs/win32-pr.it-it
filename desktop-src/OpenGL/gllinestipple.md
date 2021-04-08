---
title: funzione glLineStipple (GL. h)
description: La funzione glLineStipple specifica il modello di riga stipple.
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
keywords:
- funzione glLineStipple OpenGL
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
ms.openlocfilehash: b47202b25c0779a3daa0bd801900b1d29e0b37b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739799"
---
# <a name="gllinestipple-function"></a>glLineStipple (funzione)

La funzione **glLineStipple** specifica il modello di riga stipple.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glLineStipple(
   GLint    factor,
   GLushort pattern
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Factor* 
</dt> <dd>

Moltiplicatore per ogni bit nello schema stipple della riga. Se *Factor* è 3, ad esempio, ogni bit del modello verrà usato tre volte prima del bit successivo nel modello. Il parametro *Factor* viene bloccato nell'intervallo \[ 1, 256 e il \] valore predefinito è uno.

</dd> <dt>

*pattern* 
</dt> <dd>

Intero a 16 bit il cui modello di bit determina quali frammenti di una linea verranno disegnati quando la riga viene rasterizzata. Viene usato per primo il bit zero e il criterio predefinito è tutti quelli.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glLineStipple** specifica il modello di riga stipple. Line punteggiatura maschera alcuni frammenti prodotti dalla rasterizzazione; questi frammenti non verranno disegnati. La maschera viene eseguita utilizzando tre parametri, ovvero *il modello di pattern stipple* a 16 bit, il *fattore* di ripetizione del conteggio e *un contatore di* stipple Integer.

Counter *s* viene reimpostato su zero ogni volta che viene chiamato [**glBegin**](glbegin.md) e prima che venga generato ogni segmento di riga di una sequenza **glBegin**(GL \_ Lines)/**glEnd** . Viene incrementato dopo la generazione di ogni frammento di un segmento di linea con alias di larghezza unità o dopo che sono stati generati *i* frammenti di un segmento di linea *i* /o. I frammenti di *i* associati ai conteggi *vengono* mascherati se il mod 16 dei bitdel *modello*  /  è zero. In caso contrario, questi frammenti vengono inviati al framebuffer. Bit zero del *modello* è il bit meno significativo.

Le linee con anti-aliasing vengono considerate come una sequenza di rettangoli con *larghezza* 1 a scopo di punteggiatura. Il rettangolo *s* è rasterizzato o non basato sulla regola del frammento descritta per le righe con alias. conta i rettangoli anziché i gruppi di frammenti.

La riga punteggiatura è abilitata o disabilitata usando [**glEnable**](glenable.md) e **glDisable** con l'argomento GL \_ line \_ stipple. Se abilitata, il modello di stipple di riga viene applicato come descritto in precedenza. Quando è disabilitato, è come se il modello fosse tutti quelli. Inizialmente, la riga punteggiatura è disabilitata.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glLineStipple**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ modello di \_ stipple \_ linea GL

**glGet** con argomento della \_ riga GL \_ stipple \_ Repeat

[**glIsEnabled**](glisenabled.md) con argomento GL \_ line \_ stipple

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

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> </dl>

 

 





