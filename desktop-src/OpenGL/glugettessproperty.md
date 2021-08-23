---
title: Funzione gluGetTessProperty (Glu.h)
description: La funzione gluGetTessProperty ottiene una proprietà dell'oggetto a tessellazione.
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- Funzione gluGetTessProperty OpenGL
topic_type:
- apiref
api_name:
- gluGetTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d12e7ca8099197b663893b1edcf04dd8fa98348fe4f6d3d324b54f33904e026a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554241"
---
# <a name="glugettessproperty-function"></a>Funzione gluGetTessProperty

La **funzione gluGetTessProperty** ottiene una proprietà dell'oggetto a tessellazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluGetTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tess* 
</dt> <dd>

Oggetto a tessellazione (creato con [**gluNewTess).**](glunewtess.md)

</dd> <dt>

*Che* 
</dt> <dd>

Proprietà il cui valore deve essere recuperato. Sono validi i valori seguenti: GLU \_ TESS \_ WINDING \_ RULE, GLU \_ TESS BOUNDARY ONLY e GLU TESS \_ \_ \_ \_ TOLERANCE.

</dd> <dt>

*value* 
</dt> <dd>

Puntatore alla posizione in cui viene scritto il valore della proprietà denominata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare **gluGetTessProperty per** recuperare le proprietà archiviate in un oggetto a tessellazione. Queste proprietà influiscono sul modo in cui vengono interpretati e sottoposti a rendering gli oggetti a tessellazione. Per informazioni sulle proprietà e sulle relative proprietà, vedere [**gluTessProperty.**](glutessproperty.md)

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

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**GluTessProperty**](glutessproperty.md)
</dt> </dl>

 

 





