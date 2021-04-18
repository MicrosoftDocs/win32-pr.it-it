---
title: funzione glLineWidth (GL. h)
description: La funzione glLineWidth specifica la larghezza delle linee rasterizzate.
ms.assetid: 13a69fd7-5eee-42ec-bd05-5bd3c838d4d7
keywords:
- funzione glLineWidth OpenGL
topic_type:
- apiref
api_name:
- glLineWidth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa4cecafc9e5d8e0f55c6e9d0dbfe49924d54f14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302712"
---
# <a name="gllinewidth-function"></a>glLineWidth (funzione)

La funzione **glLineWidth** specifica la larghezza delle linee rasterizzate.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glLineWidth(
   GLfloat width
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*width* 
</dt> <dd>

Larghezza delle linee rasterizzate. Il valore predefinito è 1,0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | la *larghezza* era minore o uguale a zero.<br/>                                                                                    |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glLineWidth** specifica la larghezza rasterizzata delle righe con alias e con alias. L'uso di una lunghezza di riga diversa da 1,0 ha effetti diversi, a seconda che sia abilitata l'anti-aliasing della linea. L'anti-aliasing della linea viene controllato chiamando [**glEnable**](glenable.md) e **glDisable** con l'argomento GL \_ line \_ Smooth.

Se l'anti-aliasing della riga è disabilitato, la larghezza effettiva viene determinata dall'arrotondamento della larghezza fornita all'intero più vicino. Se l'arrotondamento ha come risultato il valore 0,0, è come se la lunghezza della linea fosse 1,0) Se \| ? x \|  =  \| ? y \| , *i* pixel vengono compilati in ogni colonna rasterizzata, dove  è il valore arrotondato della *larghezza*. In caso contrario, *i* pixel vengono compilati in ogni riga rasterizzata.

Se l'anti-aliasing è abilitato, la rasterizzazione delle righe produce un frammento per ogni quadrato di pixel che interseca l'area che si trova all'interno del rettangolo con larghezza uguale alla lunghezza riga corrente, lunghezza uguale alla lunghezza effettiva della linea e centrata sul segmento di linea matematico. Il valore di code coverage per ogni frammento è l'area delle coordinate della finestra dell'intersezione dell'area rettangolare con il quadrato pixel corrispondente. Questo valore viene salvato e utilizzato nel passaggio di rasterizzazione finale.

Non è possibile supportare tutte le larghezze quando è abilitato l'anti-aliasing della riga. Se viene richiesta una larghezza non supportata, viene utilizzata la larghezza supportata più vicina. È garantita solo la larghezza 1,0; altre dipendono dall'implementazione di. È possibile eseguire una query sull'intervallo di larghezze supportate e sulla differenza di dimensione tra le larghezze supportate all'interno dell'intervallo chiamando **glGet** con gli argomenti \_ linea di lunghezza riga GL \_ \_ e \_ \_ granularità di lunghezza linea GL \_ .

La lunghezza riga specificata da **glLineWidth** viene sempre restituita quando \_ viene eseguita una query sulla lunghezza della riga GL \_ . Il bloccaggio e l'arrotondamento per le linee con alias e con alias non hanno effetto sul valore specificato.

La lunghezza della linea non con alias può essere fissata a un valore massimo dipendente dall'implementazione. Sebbene non sia possibile eseguire query su questo valore massimo, il valore non deve essere minore del valore massimo per le righe con alias, arrotondato al valore intero più vicino.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glLineWidth**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con \_ lunghezza riga argomento \_ GL

**glGet** con argomento di \_ lunghezza riga linea GL \_ \_

**glGet** con \_ \_ granularità di lunghezza riga argomento GL \_

[**glIsEnabled**](glisenabled.md) con argomento GL \_ line \_ Smooth

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

[**glEnable**](glenable.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





