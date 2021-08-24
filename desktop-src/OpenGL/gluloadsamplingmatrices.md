---
title: Funzione gluLoadSamplingMatrices (Glu.h)
description: La funzione gluLoadSamplingMatrices carica le matrici di campionamento e culling di B-Spline (NURBS) razionali non uniformi.
ms.assetid: 7fdbc4e2-a037-4f07-bb03-e51feea42775
keywords:
- Funzione gluLoadSamplingMatrices OpenGL
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
ms.openlocfilehash: e41b2f6b25e0cecf0d13d87760a941d5ea68baa1fdd85495c8a316e862c77aec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777531"
---
# <a name="gluloadsamplingmatrices-function"></a>Funzione gluLoadSamplingMatrices

La **funzione gluLoadSamplingMatrices** carica le matrici di campionamento e di culling di B-Spline razionali non uniformi ([NURBS).](using-nurbs-curves-and-surfaces.md)

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

*nobj* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*modelMatrix* 
</dt> <dd>

Matrice modelview (come da una [**chiamata glGetFloatv).**](glgetfloatv.md)

</dd> <dt>

*projMatrix* 
</dt> <dd>

Matrice di proiezione (come da una **chiamata glGetFloatv).**

</dd> <dt>

*Finestra* 
</dt> <dd>

Un viewport (come da una [**chiamata glGetIntegerv).**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluLoadSamplingMatrices** usa *modelMatrix*, *projMatrix* e *viewport* per ricalcolare le matrici di campionamento ed culling archiviate in *nobj*. La matrice di campionamento determina in che modo una curva o una superficie NURBS deve essere a tessellata per soddisfare la tolleranza di campionamento (come determinato dalla proprietà GLU \_ SAMPLING \_ TOLERANCE). La matrice di culling viene usata per decidere se una curva o una superficie NURBS deve essere cullato prima del rendering (quando la proprietà GLU \_ CULLING è attivata).

La **funzione gluLoadSamplingMatrices** è necessaria solo se la proprietà GLU AUTO LOAD MATRIX è disattivata \_ \_ \_ (vedere [**gluNurbsProperty**](glunurbsproperty.md)). Anche se può essere utile lasciare attivata la proprietà GLU AUTO LOAD MATRIX, questa operazione richiede un round trip al server OpenGL per ottenere i valori correnti della matrice modelview, della matrice di proiezione e del \_ \_ \_ viewport.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
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

 

 





