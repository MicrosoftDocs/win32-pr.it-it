---
title: Funzione gluTessVertex (Glu.h)
description: La funzione gluTessVertex specifica un vertice in un poligono.
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
keywords:
- Funzione gluTessVertex OpenGL
topic_type:
- apiref
api_name:
- gluTessVertex
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b3b1dd666fd965e7b6536a20a794481c534ed3e42594017093ee161a067e15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488421"
---
# <a name="glutessvertex-function"></a>Funzione gluTessVertex

La **funzione gluTessVertex** specifica un vertice in un poligono.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluTessVertex(
   GLUtesselator *tess,
   GLdouble      coords[3],
   void          *data
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tess* 
</dt> <dd>

Oggetto a tessellazione (creato con [**gluNewTess).**](glunewtess.md)

</dd> <dt>

*Coords* 
</dt> <dd>

Posizione del vertice.

</dd> <dt>

*data* 
</dt> <dd>

Puntatore passato di nuovo al programma con il callback del vertice (come specificato da [*gluTessCallback).*](glutess.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La **funzione gluTessVertex** descrive un vertice in un poligono definito dall'utente. Le **chiamate gluTessVertex** successive descrivono un contorno chiuso. Ad esempio, per descrivere un quadrilatero, chiamare **gluTessVertex** quattro volte. È possibile chiamare **gluTessVertex** solo tra [**gluTessBeginContour**](glutessbegincontour.md) e [**gluTessEndContour.**](glutessendcontour.md)

Il *parametro* di dati in genere punta a una struttura contenente la posizione del vertice, nonché ad altri attributi per vertice, ad esempio colore e normale. Questo puntatore viene passato di nuovo al programma tramite il callback GLU VERTEX dopo la \_ sfalsatura (vedere [*gluTessCallback).*](glutess.md)

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

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[**gluTessBeginPolygon**](glubeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessNormal**](glutessnormal.md)
</dt> <dt>

[**GluTessProperty**](glutessproperty.md)
</dt> </dl>

 

 





