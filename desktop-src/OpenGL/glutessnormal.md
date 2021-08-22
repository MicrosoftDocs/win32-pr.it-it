---
title: Funzione gluTessNormal (Glu.h)
description: La funzione gluTessNormal specifica una normale per un poligono.
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- Funzione gluTessNormal OpenGL
topic_type:
- apiref
api_name:
- gluTessNormal
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2db848c6971fe2893f2bc2cd4ca33e96811dda0d44e81e8a852cd441a6478d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488471"
---
# <a name="glutessnormal-function"></a>Funzione gluTessNormal

La **funzione gluTessNormal** specifica una normale per un poligono.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluTessNormal(
   GLUtesselator *tess,
   GLdouble      x,
   GLdouble      y,
   GLdouble      z
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tess* 
</dt> <dd>

Oggetto a tassellamento (creato con [**gluNewTess).**](glunewtess.md)

</dd> <dt>

*x* 
</dt> <dd>

Componente della coordinata x di una normale.

</dd> <dt>

*y* 
</dt> <dd>

Componente della coordinata y di una normale.

</dd> <dt>

*z* 
</dt> <dd>

Componente della coordinata z di una normale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluTessNormal** descrive una normale per un poligono definito. Tutti i dati di input vengono proiettati su un piano perpendicolare a uno dei tre assi di coordinate prima della tessellazione e tutti i triangoli di output sono orientati in senso antiorario rispetto alla normale. Per ottenere l'orientamento in senso orario, invertire il segno della normale fornita. Ad esempio, se si sa che tutti i poligoni si trovano nel piano x-y, chiamare **gluTessNormal**(tess, 0.0, 0.0, 1.0) prima di eseguire il rendering dei poligoni.

Se la normale fornita è (0.0, 0.0, 0.0) (valore predefinito), la normale viene determinata come segue:

1.  La direzione della normale, fino al segno, si trova adattando un piano ai vertici, indipendentemente dalla modalità di connessione dei vertici. Si prevede che i dati di input si trovano approssimativamente nel piano. In caso contrario, la proiezione perpendicolare a uno dei tre assi delle coordinate può modificare sostanzialmente la geometria.
2.  Il segno della normale viene scelto in modo che la somma delle aree firmate di tutti i contorni di input non sia negativa (dove un contorno in senso antiorario ha un'area positiva).

Il valore normal fornito persiste fino a quando non viene modificato da un'altra chiamata a **gluTessNormal.**

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

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> </dl>

 

 





