---
title: funzione glShadeModel (GL. h)
description: La funzione glShadeModel seleziona l'ombreggiatura piatta o smussata.
ms.assetid: 52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e
keywords:
- funzione glShadeModel OpenGL
topic_type:
- apiref
api_name:
- glShadeModel
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142ac518c91c6378f1606235e25502be8c06dd6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301460"
---
# <a name="glshademodel-function"></a>glShadeModel (funzione)

La funzione **glShadeModel** seleziona l'ombreggiatura piatta o smussata.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glShadeModel(
   GLenum mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mode* 
</dt> <dd>

Valore simbolico che rappresenta una tecnica di ombreggiatura. I valori accettati sono GL \_ flat e GL \_ Smooth. Il valore predefinito è GL \_ Smooth.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *mode* è un valore diverso da GL \_ glat o GL \_ Smooth.<br/>                                                                      |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Le primitive OpenGL possono avere ombreggiatura piatta o smussata. L'ombreggiatura uniforme, il valore predefinito, causa l'interpolazione dei colori calcolati dei vertici quando la primitiva viene rasterizzata, assegnando in genere colori diversi a ogni frammento di pixel risultante. Ombreggiatura piatta consente di selezionare il colore calcolato di un solo vertice e di assegnarlo a tutti i frammenti di pixel generati dalla rasterizzazione di una singola primitiva. In entrambi i casi, il colore calcolato di un vertice è il risultato dell'illuminazione, se l'illuminazione è abilitata o è il colore corrente al momento in cui è stato specificato il vertice, se l'illuminazione è disabilitata.

L'ombreggiatura piatta e liscia non è distinguibile per i punti. Conteggio dei vertici e delle primitive da uno, a partire dal momento in cui viene emesso [**glBegin**](glbegin.md) , ogni segmento di linea ombreggiato a *cui* viene assegnato il colore calcolato del vertice *i* + 1, il secondo vertice. Per il conteggio analogo da uno, a ogni poligono ombreggiato viene assegnato il colore calcolato del vertice elencato nella tabella seguente. Si tratta dell'ultimo vertice che consente di specificare il poligono in tutti i casi tranne i poligoni singoli, in cui il primo vertice specifica il colore con ombreggiatura piatta.



| Tipo primitivo del poligono i | Vertice   |
|-----------------------------|----------|
| Poligono singolo (*I*= 1)      | 1        |
| Striscia triangolare              | *i* + 2  |
| Ventola triangolo                | *i* + 2  |
| Triangolo indipendente        | 3 *I*     |
| Striping quad                  | 2 *i* + 2 |
| Quad indipendente            | 4 *I*     |



 

Le ombreggiature flat e Smooth vengono specificate da **glShadeModel** con la *modalità* impostata rispettivamente su GL \_ flat e GL \_ Smooth.

La funzione seguente recupera le informazioni correlate a **glShadeModel**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ modello di ombreggiatura GL \_

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





