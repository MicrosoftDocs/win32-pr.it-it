---
title: Funzione gluQuadricDrawStyle (Glu.h)
description: La funzione gluQuadricDrawStyle specifica lo stile di disegno desiderato per quadric.
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- Funzione gluQuadricDrawStyle OpenGL
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
ms.openlocfilehash: 7a873ed4f4ceaff4aa3dad678dbb4c1fd7a635b0ce41d7a9480af84278c8360c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061559"
---
# <a name="gluquadricdrawstyle-function"></a>Funzione gluQuadricDrawStyle

La **funzione gluQuadricDrawStyle** specifica lo stile di disegno desiderato per quadric.

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

Oggetto quadric (creato con [**gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*drawStyle* 
</dt> <dd>

Stile di disegno desiderato. I valori seguenti sono validi.



| Valore                                                                                                                                                            | Significato                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <dt>**GLU \_ FILL**</dt> </dl>                   | Il rendering dei quadric viene eseguito con primitive poligonali. I poligoni vengono disegnati in senso antiorario rispetto alle normali (come definito con [**gluQuadricOrientation**](gluquadricorientation.md)).<br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <dt>**LINEA \_ GLU**</dt> </dl>                   | Il rendering dei quadric viene eseguito come set di righe.<br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <dt>**GLU \_ ESEREA**</dt> </dl> | Il rendering dei quadric viene eseguito come un set di linee, ad eccezione del fatto che i bordi che separano i visi coplanari non verranno disegnati.<br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <dt>**PUNTO \_ GLU**</dt> </dl>                | Il rendering dei quadric viene eseguito come set di punti.<br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluQuadricDrawStyle** specifica lo stile di disegno per quadrics sottoposto a rendering con **quadObject**.

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

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





