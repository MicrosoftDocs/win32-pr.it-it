---
title: Funzione gluTessEndContour (Glu.h)
description: Le funzioni gluTessBeginContour e gluTessEndContour delimitano una descrizione del contorno. | Funzione gluTessEndContour (Glu.h)
ms.assetid: 115db079-cbcb-48e1-8bab-0eb4814afb82
keywords:
- Funzione gluTessEndContour OpenGL
topic_type:
- apiref
api_name:
- gluTessEndContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d0685a4af264dd2d4093fbb754c09d2124ecb2689063b61280bf55337ebb305
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777411"
---
# <a name="glutessendcontour-function"></a>Funzione gluTessEndContour

Le [**funzioni gluTessBeginContour**](glutessbegincontour.md) e **gluTessEndContour** delimitano una descrizione del contorno.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluTessEndContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tess* 
</dt> <dd>

Oggetto a tessellazione (creato con [**gluNewTess).**](glunewtess.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Le [**funzioni gluTessBeginContour**](glutessbegincontour.md) e **gluTessEndContour** delimitano la definizione di un contorno poligono. All'interno di ogni coppia **gluTessBeginContour** / **gluTessEndContour** possono essere presenti zero o più chiamate a [**gluTessVertex.**](glutessvertex.md) I vertici specificano un contorno chiuso (l'ultimo vertice di ogni contorno viene collegato automaticamente al primo). È possibile chiamare **gluTessBeginContour** solo tra [**gluTessBeginPolygon**](glutessbeginpolygon.md) [**e gluTessEndPolygon.**](glutessendpolygon.md)

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

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**GluTessProperty**](glutessproperty.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





