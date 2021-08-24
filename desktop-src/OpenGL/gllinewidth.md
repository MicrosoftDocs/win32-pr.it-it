---
title: Funzione glLineWidth (Gl.h)
description: La funzione glLineWidth specifica la larghezza delle linee rasterizzate.
ms.assetid: 13a69fd7-5eee-42ec-bd05-5bd3c838d4d7
keywords:
- Funzione glLineWidth OpenGL
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
ms.openlocfilehash: cad5af24170f47125136e87e055413a576821bf75d3f5f87532d026d0bb2fd0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119492971"
---
# <a name="gllinewidth-function"></a>Funzione glLineWidth

La **funzione glLineWidth** specifica la larghezza delle linee rasterizzate.

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

Larghezza delle linee rasterizzate. Il valore predefinito è 1.0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *width* è minore o uguale a zero.<br/>                                                                                    |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glLineWidth** specifica la larghezza rasterizzata delle linee con alias e antialias. L'uso di uno spessore di linea diverso da 1.0 ha effetti diversi, a seconda che l'antialiasing delle linee sia abilitato o meno. L'anti-aliasing delle righe viene controllato chiamando [**glEnable**](glenable.md) **e glDisable con** l'argomento GL \_ LINE \_ SMOOTH.

Se l'antialiasing delle linee è disabilitato, la larghezza effettiva viene determinata arrotondando la larghezza fornita all'intero più vicino. Se l'arrotondamento ha come risultato il valore 0,0, è come se lo spessore della linea fosse 1,0. Se \| ? x \|  =  \| ? y \| , *i* pixel vengono riempiti in ogni colonna rasterizzata, dove *i* è il valore arrotondato di *width*. In caso *contrario,* i pixel vengono riempiti in ogni riga rasterizzata.

Se l'antialiasing è abilitato, l'rasterizzazione delle linee produce un frammento per ogni quadrato di pixel che interseca l'area all'interno del rettangolo con larghezza uguale alla larghezza della linea corrente, lunghezza uguale alla lunghezza effettiva della linea e centrato sul segmento di linea matematica. Il valore di copertura per ogni frammento è l'area delle coordinate della finestra dell'intersezione dell'area rettangolare con il quadrato di pixel corrispondente. Questo valore viene salvato e usato nel passaggio di rasterizzazione finale.

Non tutte le larghezze possono essere supportate quando è abilitato l'antialiasing delle linee. Se viene richiesta una larghezza non supportata, viene usata la larghezza supportata più vicina. È garantito il supporto solo della larghezza 1.0. altri dipendono dall'implementazione. È possibile eseguire query sull'intervallo di larghezze supportate e sulla differenza di dimensioni tra le larghezze supportate all'interno dell'intervallo chiamando **glGet** con gli argomenti GL LINE WIDTH RANGE e \_ GL LINE WIDTH \_ \_ \_ \_ \_ GRANULARITY.

Lo spessore di riga specificato da **glLineWidth** viene sempre restituito quando viene eseguita una query su GL \_ LINE \_ WIDTH. Il controllo e l'arrotondamento per le righe con alias e con antialias non hanno alcun effetto sul valore specificato.

Lo spessore di linea non antialias può essere fissato a un valore massimo dipendente dall'implementazione. Anche se non è possibile eseguire query su questo valore massimo, non deve essere minore del valore massimo per le righe con antialias, arrotondato al valore intero più vicino.

Le funzioni seguenti recuperano informazioni correlate **a glLineWidth**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ LINE \_ WIDTH

**glGet con** argomento GL \_ LINE WIDTH \_ \_ RANGE

**glGet con** argomento GL \_ LINE WIDTH \_ \_ GRANULARITY

[**glIsEnabled con**](glisenabled.md) argomento GL \_ LINE \_ SMOOTH

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

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





