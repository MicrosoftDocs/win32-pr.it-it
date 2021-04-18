---
title: funzione gluLoadSamplingMatrices (Glu. h)
description: La funzione gluLoadSamplingMatrices carica matrici di campionamento B-spline (NURBS) non uniformi e matrici di abbattimento.
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
keywords:
- funzione gluLoadSamplingMatrices OpenGL
topic_type:
- apiref
api_name:
- gluLoadSamplingMatrices
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 293b8bace0dff7d89bfcffa2af33738e0e59de7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301355"
---
# <a name="gluloadsamplingmatrices-function"></a>gluLoadSamplingMatrices (funzione)

La funzione **gluLoadSamplingMatrices** carica matrici di campionamento B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniformi e matrici di abbattimento.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluLoadSamplingMatrices(
         GLUnurbs *nobj,
   const GLfloat  modelMatrix[16],
   const GLfloat  projMatrix[16],
   const GLint    viewport[4]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*juje* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*modelMatrix* 
</dt> <dd>

Matrice Modelview (come da una chiamata [**glGetFloatv**](glgetfloatv.md) ).

</dd> <dt>

*projMatrix* 
</dt> <dd>

Una matrice di proiezione, come da una chiamata **glGetFloatv** .

</dd> <dt>

*Viewport* 
</dt> <dd>

Viewport (come da una chiamata [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluLoadSamplingMatrices** USA *modelMatrix*, *projMatrix* e *viewport* per ricalcolare le matrici di campionamento e di eliminazione archiviate in *juje*. La matrice di campionamento determina il modo in cui una curva o una superficie NURBS deve essere tassellati per soddisfare la tolleranza di campionamento, come determinato dalla \_ proprietà di tolleranza del campionamento Glu \_ . La matrice di abbattimento viene usata per decidere se una curva o una superficie NURBS deve essere rilevata prima del rendering (quando la \_ proprietà di abbattimento di Glu è attivata).

La funzione **gluLoadSamplingMatrices** è necessaria solo se la \_ proprietà della matrice di caricamento automatico Glu \_ \_ è spenta (vedere [**gluNurbsProperty**](glunurbsproperty.md)). Sebbene possa essere utile lasciare attiva la proprietà della \_ matrice di caricamento automatico Glu \_ , questa \_ operazione richiede un round trip al server OpenGL per ottenere i valori correnti della matrice Modelview, della matrice di proiezione e del viewport.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glGetFloatv**](glgetfloatv.md)
</dt> <dt>

[**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**gluGetNurbsProperty**](glugetnurbsproperty.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





