---
title: funzione glPointSize (GL. h)
description: La funzione glPointSize specifica il diametro dei punti rasterizzati.
ms.assetid: efa35fa8-721a-48e5-bf59-d33b9bbe7f73
keywords:
- funzione glPointSize OpenGL
topic_type:
- apiref
api_name:
- glPointSize
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e6b9525e302cad1eb940184eb5eb83e11744bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301795"
---
# <a name="glpointsize-function"></a>glPointSize (funzione)

La funzione **glPointSize** specifica il diametro dei punti rasterizzati.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPointSize(
   GLfloat size
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*size* 
</dt> <dd>

Diametro dei punti rasterizzati. Il valore predefinito è 1,0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *dimensioni* minori o uguali a zero.<br/>                                                                                     |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glPointSize** specifica il diametro rasterizzato dei punti con alias e con alias. L'uso di una dimensione del punto diversa da 1,0 ha effetti diversi, a seconda che sia abilitato l'anti-aliasing del punto. L'anti-aliasing del punto viene controllato chiamando [**glEnable**](glenable.md) e **glDisable** con l'argomento GL \_ Point \_ Smooth.

Se l'anti-aliasing del punto è disabilitato, le dimensioni effettive vengono determinate mediante l'arrotondamento della dimensione fornita all'intero più vicino. Se l'arrotondamento restituisce il valore 0, è come se la dimensione del punto fosse 1. Se le dimensioni arrotondate sono dispari, il punto centrale (*x*,*y*) del frammento di pixel che rappresenta il punto viene calcolato come

(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)

dove gli indici *w* indicano le coordinate della finestra. Tutti i pixel che si trovano all'interno della griglia quadrata della dimensione arrotondata al centro, ovvero *x*,*y*, costituiscono il frammento. Se le dimensioni sono pari, il punto centrale è

(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)

e i centri dei frammenti rasterizzati sono le coordinate della finestra a metà Integer all'interno del quadrato della dimensione arrotondata al centro in corrispondenza di (*x*,*y*). A tutti i frammenti di pixel prodotti nella rasterizzazione di un punto nonantialiased vengono assegnati gli stessi dati associati; oggetto del vertice che corrisponde al punto.

Se l'anti-aliasing è abilitato, la rasterizzazione dei punti produce un frammento per ogni quadrato di pixel che interseca l'area che si trova all'interno del cerchio con diametro uguale alle dimensioni del punto corrente e centrato ai punti (*x*<sub>w</sub> ,*y*<sub>w</sub> ). Il valore di code coverage per ogni frammento è l'area delle coordinate della finestra dell'intersezione dell'area circolare con il quadrato pixel corrispondente. Questo valore viene salvato e utilizzato nel passaggio di rasterizzazione finale. I dati associati a ogni frammento sono i dati associati al punto che si sta rasterizzando.

Quando l'anti-aliasing del punto è abilitato, non sono supportate tutte le dimensioni. Se viene richiesta una dimensione non supportata, vengono usate le dimensioni più vicine supportate. È garantita la garanzia che siano supportate solo le dimensioni 1,0; altre dipendono dall'implementazione di. È possibile eseguire una query sull'intervallo di dimensioni supportate e sulla differenza di dimensioni tra le dimensioni supportate nell'intervallo chiamando [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con gli argomenti \_ intervallo di dimensioni del punto GL \_ \_ e \_ granularità delle dimensioni del punto GL \_ \_ .

La dimensione in punti specificata da **glPointSize** viene sempre restituita \_ quando \_ viene eseguita una query sulle dimensioni del punto GL. Il bloccaggio e l'arrotondamento per i punti con alias e con alias non hanno effetto sul valore specificato.

Le dimensioni del punto non con alias possono essere fissate a un valore massimo dipendente dall'implementazione. Sebbene non sia possibile eseguire query su questo valore massimo, il valore non deve essere minore del valore massimo per i punti con alias, arrotondato al valore intero più vicino.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glPointSize**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con \_ dimensione punto GL \_ argomento

**glGet** con intervallo di \_ dimensioni punti GL \_ \_

**glGet** con \_ \_ granularità delle dimensioni dei punti GL degli argomenti \_

[**glIsEnabled**](glisenabled.md) con l'argomento \_ punto GL \_ smussato

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

 

 





