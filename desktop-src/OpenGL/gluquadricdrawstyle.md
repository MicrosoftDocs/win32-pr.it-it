---
title: funzione gluQuadricDrawStyle (Glu. h)
description: La funzione gluQuadricDrawStyle specifica lo stile di estrazione desiderato per quadriche.
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- funzione gluQuadricDrawStyle OpenGL
topic_type:
- apiref
api_name:
- gluQuadricDrawStyle
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a1b44b7894ea9762b450c5a5d6c2b022c5e02f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964601"
---
# <a name="gluquadricdrawstyle-function"></a>gluQuadricDrawStyle (funzione)

La funzione **gluQuadricDrawStyle** specifica lo stile di estrazione desiderato per quadriche.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluQuadricDrawStyle(
   GLUquadric *quadObject,
   GLenum     drawStyle
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*quadObject* 
</dt> <dd>

Oggetto quadrica (creato con [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*drawStyle* 
</dt> <dd>

Stile di disegni desiderato. I valori seguenti sono validi.



| Valore                                                                                                                                                            | Significato                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <dt>**\_riempimento Glu**</dt> </dl>                   | Viene eseguito il rendering di quadriche con primitive poligonali. I poligoni vengono disegnati in senso antiorario rispetto alle normali (come definito con [**gluQuadricOrientation**](gluquadricorientation.md)).<br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <dt>**\_linea Glu**</dt> </dl>                   | Il rendering di quadriche viene eseguito come un set di righe.<br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <dt>**\_Siluetta Glu**</dt> </dl> | Il rendering di quadriche viene eseguito come set di righe, ad eccezione del fatto che i bordi che separano i visi complanari non verranno disegnati<br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <dt>**punto di GLU \_**</dt> </dl>                | Il rendering di quadriche viene eseguito come un set di punti.<br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluQuadricDrawStyle** specifica lo stile di disegna per quadriche di cui è stato eseguito il rendering con **quadObject**.

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

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





