---
title: Funzione glShadeModel (Gl.h)
description: La funzione glShadeModel seleziona un'ombreggiatura semplice o uniforme.
ms.assetid: 52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e
keywords:
- Funzione glShadeModel OpenGL
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
ms.openlocfilehash: 505ff0e2d74f9eb4f252e4e663ceec00fd86469b3d69374623b2763915a08b0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491611"
---
# <a name="glshademodel-function"></a>Funzione glShadeModel

La **funzione glShadeModel** seleziona un'ombreggiatura semplice o uniforme.

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

Valore simbolico che rappresenta una tecnica di ombreggiatura. I valori accettati sono GL \_ FLAT e GL \_ SMOOTH. Il valore predefinito è GL \_ SMOOTH.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *mode* è un valore diverso da GL \_ GLAT o GL \_ SMOOTH.<br/>                                                                      |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Le primitive OpenGL possono avere ombreggiatura piatta o uniforme. L'ombreggiatura smussata, l'impostazione predefinita, fa sì che i colori calcolati dei vertici siano interpolati mentre la primitiva viene rasterizzata, assegnando in genere colori diversi a ogni frammento di pixel risultante. L'ombreggiatura flat seleziona il colore calcolato di un solo vertice e lo assegna a tutti i frammenti di pixel generati rasterizzando una singola primitiva. In entrambi i casi, il colore calcolato di un vertice è il risultato dell'illuminazione, se l'illuminazione è abilitata oppure è il colore corrente al momento in cui è stato specificato il vertice, se l'illuminazione è disabilitata.

L'ombreggiatura piatta e smussata non è distinguibile per i punti. Conteggio di vertici e primitive da uno, a partire da quando viene eseguito [**glBegin,**](glbegin.md) a ogni segmento di linea con ombreggiatura piana *i* viene assegnato il colore calcolato del vertice *i* + 1, il secondo vertice. Contando in modo analogo da uno, a ogni poligono con ombreggiatura piatta viene assegnato il colore calcolato del vertice elencato nella tabella seguente. Si tratta dell'ultimo vertice per specificare il poligono in tutti i casi, ad eccezione dei singoli poligoni, in cui il primo vertice specifica il colore con ombreggiatura piatta.



| Tipo primitivo di poligono i | Vertice   |
|-----------------------------|----------|
| Poligono singolo *(I*=1)      | 1        |
| Striscia triangolare              | *i* + 2  |
| Ventola triangolare                | *i* + 2  |
| Triangolo indipendente        | 3 *I*     |
| Quad strip                  | 2 *i* + 2 |
| Quad indipendente            | 4 *I*     |



 

L'ombreggiatura flat e smussata vengono specificate rispettivamente da **glShadeModel** con *la* modalità impostata su GL FLAT e \_ GL \_ SMOOTH.

La funzione seguente recupera le informazioni correlate a **glShadeModel**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ SHADE \_ MODEL

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





