---
title: Funzione glPolygonMode (Gl.h)
description: La funzione glPolygonMode seleziona una modalità di rasterizzazione poligono.
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
keywords:
- Funzione glPolygonMode OpenGL
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
ms.openlocfilehash: f040b3e44ee34d819752bae5deffbf1a02f0d38ab1249f2e32de67c262bd5f2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118615207"
---
# <a name="glpolygonmode-function"></a>Funzione glPolygonMode

La **funzione glPolygonMode** seleziona una modalità di rasterizzazione poligono.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPolygonMode(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Faccia* 
</dt> <dd>

Poligoni a cui *si applica* la modalità. Deve essere GL FRONT per i poligoni frontali, GL BACK per i poligoni rivolti all'indietro o GL FRONT E BACK per i poligoni \_ \_ \_ \_ \_ front-facing e back-facing.

</dd> <dt>

*mode* 
</dt> <dd>

Modalità di rasterizzazione dei poligoni. Le modalità seguenti sono definite e possono essere specificate in *modalità*. Il valore predefinito è GL FILL per i poligoni anteriore \_ e posteriore.



| Valore                                                                                                                                          | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINT"></span><span id="gl_point"></span><dl> <dt>**PUNTO \_ GL**</dt> </dl> | I vertici poligoni contrassegnati come inizio di un bordo limite vengono disegnati come punti. Gli attributi punto, ad esempio GL \_ POINT SIZE e GL POINT \_ \_ \_ SMOOTH, controllano la rasterizzazione dei punti. Gli attributi di rasterizzazione dei poligoni diversi da GL \_ POLYGON MODE non hanno alcun \_ effetto.<br/>                                                                                                                                                    |
| <span id="GL_LINE"></span><span id="gl_line"></span><dl> <dt>**GL \_ LINE**</dt> </dl>    | I bordi limite del poligono vengono disegnati come segmenti di linea. Vengono considerati come segmenti di linea connessi per lo stippling delle linee; Il contatore dello stipple di linea e il modello non vengono reimpostati tra i segmenti (vedere [**glLineStipple).**](gllinestipple.md) Gli attributi di linea, ad esempio GL \_ LINE WIDTH e GL LINE \_ \_ \_ SMOOTH, controllano la rasterizzazione delle linee. Gli attributi di rasterizzazione dei poligoni diversi da GL \_ POLYGON MODE non hanno alcun \_ effetto.<br/> |
| <span id="GL_FILL"></span><span id="gl_fill"></span><dl> <dt>**GL \_ FILL**</dt> </dl>    | L'interno del poligono viene riempito. Gli attributi poligoni, ad esempio GL \_ POLYGON \_ STIPPLE e GL \_ POLYGON \_ SMOOTH, controllano la rasterizzazione del poligono.<br/>                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | Il *viso* o *la modalità* non è un valore accettato.<br/>                                                                         |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glPolygonMode** controlla l'interpretazione dei poligoni per la rasterizzazione. Il *parametro viso* descrive  a quale modalità poligoni si applica: poligoni frontali (GL FRONT), poligoni rivolti all'indietro (GL BACK) o entrambi \_ \_ (GL \_ FRONT E \_ \_ BACK). La modalità poligono influisce solo sulla rasterizzazione finale dei poligoni. In particolare, i vertici di un poligono sono accesi e il poligono viene ritagliato ed eventualmente ritagliato prima dell'applicazione di queste modalità.

Per disegnare una superficie con poligoni rivolti all'indietro riempiti e poligoni frontali delineati, chiamare

**glPolygonMode**(GL \_ FRONT, GL \_ LINE);

I vertici sono contrassegnati come limite o non associati con un flag di bordo. I flag di bordo vengono generati internamente da OpenGL quando scompone i poligoni e possono essere impostati in modo esplicito usando [**glEdgeFlag**](gledgeflag-functions.md).

La funzione seguente recupera informazioni correlate a **glPolygonMode**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ POLYGON \_ MODE

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

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glPointSize**](glpointsize.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> </dl>

 

 





