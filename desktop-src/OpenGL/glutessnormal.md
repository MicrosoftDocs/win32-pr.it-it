---
title: funzione gluTessNormal (Glu. h)
description: La funzione gluTessNormal specifica un normale per un poligono.
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- funzione gluTessNormal OpenGL
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
ms.openlocfilehash: af04ab2364fafcea709ca36cab2f10a8bea1a96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964827"
---
# <a name="glutessnormal-function"></a>gluTessNormal (funzione)

La funzione **gluTessNormal** specifica un normale per un poligono.

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

Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).

</dd> <dt>

*x* 
</dt> <dd>

Componente della coordinata x di un normale.

</dd> <dt>

*y* 
</dt> <dd>

Componente della coordinata y di un normale.

</dd> <dt>

*z* 
</dt> <dd>

Componente della coordinata z di un normale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluTessNormal** descrive un normale per un poligono definito dall'utente. Tutti i dati di input vengono proiettati su un piano perpendicolare a uno dei tre assi delle coordinate prima dello schema a mosaico e tutti i triangoli di output sono orientati in senso antiorario rispetto al normale. (Per ottenere l'orientamento in senso orario, invertire il segno del normale fornito). Ad esempio, se si è certi che tutti i poligoni si trovano nel piano x-y, chiamare **gluTessNormal**(tess, 0,0, 0,0, 1,0) prima di eseguire il rendering di tutti i poligoni.

Se il valore normale fornito è (0,0, 0,0, 0,0) (il valore predefinito), il normale viene determinato nel modo seguente:

1.  La direzione della normale, fino al segno, viene rilevata mediante l'adattamento di un piano ai vertici, indipendentemente dalla modalità di connessione dei vertici. Si prevede che i dati di input si trovino approssimativamente nel piano; in caso contrario, la proiezione perpendicolare a uno dei tre assi delle coordinate può modificare notevolmente la geometria.
2.  Il segno della normale viene scelto in modo che la somma delle aree firmate di tutti i contorni di input sia non negativo (dove un contorno in senso antiorario ha un'area positiva).

Il normale fornito viene mantenuto finché un'altra chiamata a **gluTessNormal** non la modifica.

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

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> </dl>

 

 





