---
title: Funzione glPointSize (Gl.h)
description: La funzione glPointSize specifica il diametro dei punti rasterizzati.
ms.assetid: efa35fa8-721a-48e5-bf59-d33b9bbe7f73
keywords:
- Funzione glPointSize OpenGL
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
ms.openlocfilehash: 127618e483a300024201798f7c8728d9ab8c0c0807e6dcac07ba580798a1ea4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132822"
---
# <a name="glpointsize-function"></a>Funzione glPointSize

La **funzione glPointSize** specifica il diametro dei punti rasterizzati.

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

Diametro dei punti rasterizzati. Il valore predefinito è 1.0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *size* è minore o uguale a zero.<br/>                                                                                     |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glPointSize** specifica il diametro rasterizzato di entrambi i punti con alias e antialias. L'uso di una dimensione in punti diversa da 1.0 ha effetti diversi, a seconda che sia abilitato l'antialiasing dei punti. L'antialiasing dei punti viene controllato chiamando [**glEnable**](glenable.md) **e glDisable con** l'argomento GL \_ POINT \_ SMOOTH.

Se l'antialiasing dei punti è disabilitato, le dimensioni effettive vengono determinate arrotondando le dimensioni fornite all'intero più vicino. Se l'arrotondamento ha come risultato il valore 0, è come se la dimensione del punto fosse 1. Se la dimensione arrotondata è dispari, il punto centrale (*x*,*y*) del frammento di pixel che rappresenta il punto viene calcolato come

(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)

dove *w* pedices indicano le coordinate della finestra. Tutti i pixel che si trovano all'interno della griglia quadrata delle dimensioni arrotondate centrate in corrispondenza di (*x*,*y*) costituiscono il frammento. Se le dimensioni sono pari, il punto centrale è

(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)

e i centri del frammento rasterizzato sono le coordinate della finestra semestrale all'interno del quadrato delle dimensioni arrotondate centrate in corrispondenza di (*x*,*y*). A tutti i frammenti di pixel prodotti durante la rasterizzazione di un punto non allineato vengono assegnati gli stessi dati associati. quella del vertice corrispondente al punto.

Se l'antialiasing è abilitato, la rasterizzazione dei punti produce un frammento per ogni quadrato di pixel che interseca l'area che si trova all'interno del cerchio con diametro uguale alle dimensioni del punto corrente e centrata in corrispondenza dei punti (*x*<sub>w</sub> ,*y*<sub>w</sub> ). Il valore di copertura per ogni frammento è l'area delle coordinate della finestra dell'intersezione dell'area circolare con il quadrato in pixel corrispondente. Questo valore viene salvato e usato nel passaggio di rasterizzazione finale. I dati associati a ogni frammento sono i dati associati al punto da rasterizzarsi.

Non tutte le dimensioni sono supportate quando è abilitato l'antialiasing dei punti. Se viene richiesta una dimensione non supportata, viene usata la dimensione supportata più vicina. È garantito che sia supportata solo la dimensione 1.0. altri dipendono dall'implementazione. È possibile eseguire query sull'intervallo di dimensioni supportate e sulla differenza tra le dimensioni supportate all'interno dell'intervallo chiamando [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con gli argomenti GL POINT SIZE RANGE e \_ GL POINT SIZE \_ \_ \_ \_ \_ GRANULARITY.

La dimensione del punto specificata da **glPointSize** viene sempre restituita quando viene eseguita una query su GL \_ POINT \_ SIZE. La chiusura e l'arrotondamento per i punti con alias e antialias non hanno alcun effetto sul valore specificato.

Le dimensioni dei punti non antialias possono essere ridotte a un valore massimo dipendente dall'implementazione. Anche se non è possibile eseguire query su questo valore massimo, non deve essere inferiore al valore massimo per i punti antialias, arrotondato al valore intero più vicino.

Le funzioni seguenti recuperano informazioni correlate a **glPointSize**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ POINT \_ SIZE

**glGet con** argomento GL \_ POINT SIZE \_ \_ RANGE

**glGet con** l'argomento GL \_ POINT SIZE \_ \_ GRANULARITY

[**glIsEnabled con**](glisenabled.md) argomento GL \_ POINT \_ SMOOTH

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

 

 





