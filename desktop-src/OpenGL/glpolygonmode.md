---
title: funzione glPolygonMode (GL. h)
description: La funzione glPolygonMode seleziona una modalità di rasterizzazione poligonale.
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
keywords:
- funzione glPolygonMode OpenGL
topic_type:
- apiref
api_name:
- glPolygonMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23d133243c1655432842a939b8da0f3a981fdffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302707"
---
# <a name="glpolygonmode-function"></a>glPolygonMode (funzione)

La funzione **glPolygonMode** seleziona una modalità di rasterizzazione poligonale.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPolygonMode(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*faccia* 
</dt> <dd>

Poligoni a cui si applica la *modalità* . Deve essere di \_ primo piano per i poligoni in primo piano, GL \_ indietro per i poligoni di back-end o GL \_ front \_ e \_ back per i poligoni anteriori e di back-end.

</dd> <dt>

*mode* 
</dt> <dd>

Il modo in cui verranno rasterizzati i poligoni. Le modalità seguenti sono definite e possono essere specificate in *modalità*. Il valore predefinito è \_ riempimento GL per i poligoni di primo e indietro.



| Valore                                                                                                                                          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINT"></span><span id="gl_point"></span><dl> <dt>**\_punto GL**</dt> </dl> | I vertici poligoni contrassegnati come inizio di un bordo limite vengono disegnati come punti. Gli attributi punto, ad \_ esempio \_ le dimensioni del punto GL e \_ il punto GL, \_ controllano la rasterizzazione dei punti. Gli attributi di rasterizzazione Polygon diversi dalla \_ modalità poligono GL \_ non hanno alcun effetto.<br/>                                                                                                                                                    |
| <span id="GL_LINE"></span><span id="gl_line"></span><dl> <dt>**\_linea GL**</dt> </dl>    | I bordi limite del poligono vengono disegnati come segmenti di linea. Vengono trattati come segmenti di linea collegati per la riga punteggiatura; il contatore e il pattern stipple di riga non vengono reimpostati tra segmenti (vedere [**glLineStipple**](gllinestipple.md)). Gli attributi della linea, ad esempio \_ \_ la lunghezza riga GL e \_ la linea GL, \_ controllano la rasterizzazione delle linee. Gli attributi di rasterizzazione Polygon diversi dalla \_ modalità poligono GL \_ non hanno alcun effetto.<br/> |
| <span id="GL_FILL"></span><span id="gl_fill"></span><dl> <dt>**\_riempimento GL**</dt> </dl>    | L'interno del poligono viene riempito. Gli attributi poligono come GL \_ Polygon \_ stipple e GL \_ Polygon \_ Smooth controllano la rasterizzazione del poligono.<br/>                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | La *faccia* o la *modalità* non è un valore accettato.<br/>                                                                         |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glPolygonMode** controlla l'interpretazione dei poligoni per la rasterizzazione. Il parametro *viso* descrive la *modalità* dei poligoni a cui si applicano i poligoni anteriori (GL \_ front), i poligoni di back-facet (GL \_ back) o entrambi (GL \_ front \_ e \_ back). La modalità Polygon ha effetto solo sulla rasterizzazione finale dei poligoni. In particolare, i vertici di un poligono sono illuminati e il poligono viene troncato e possibilmente ritagliato prima dell'applicazione di queste modalità.

Per creare una superficie con i poligoni con riempimento e con i poligoni in primo piano, chiamare

**glPolygonMode**(GL \_ Front, \_ linea GL);

I vertici sono contrassegnati come limite o non delimitatori con un flag Edge. I flag Edge vengono generati internamente da OpenGL quando decompone i poligoni e possono essere impostati in modo esplicito tramite [**glEdgeFlag**](gledgeflag-functions.md).

La funzione seguente recupera le informazioni correlate a **glPolygonMode**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Polygon \_ mode

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

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glPointSize**](glpointsize.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> </dl>

 

 





