---
title: funzione gluTessVertex (Glu. h)
description: La funzione gluTessVertex specifica un vertice in un poligono.
ms.assetid: 9c555b32-5257-4eeb-9323-ccad59591097
keywords:
- funzione gluTessVertex OpenGL
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
ms.openlocfilehash: 546bbad2be1205f62c7889fbb18f23d5b0e38b8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518856"
---
# <a name="glutessvertex-function"></a>gluTessVertex (funzione)

La funzione **gluTessVertex** specifica un vertice in un poligono.

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

Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).

</dd> <dt>

*CoOrds* 
</dt> <dd>

Posizione del vertice.

</dd> <dt>

*data* 
</dt> <dd>

Puntatore passato al programma con il callback del vertice (come specificato da [*gluTessCallback*](glutess.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione **gluTessVertex** descrive un vertice in un poligono che l'utente sta definendo. Le chiamate **gluTessVertex** successive descrivono un contorno chiuso. Per descrivere un quadrilatero, ad esempio, chiamare **gluTessVertex** quattro volte. È possibile chiamare **gluTessVertex** solo tra [**gluTessBeginContour**](glutessbegincontour.md) e [**gluTessEndContour**](glutessendcontour.md).

Il parametro *Data* in genere punta a una struttura che contiene la posizione del vertice, oltre ad altri attributi per vertice, ad esempio colore e normale. Questo puntatore viene passato di nuovo al programma tramite il \_ callback del vertice Glu dopo la suddivisione a mosaico (vedere [*gluTessCallback*](glutess.md)).

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

[**gluTessProperty**](glutessproperty.md)
</dt> </dl>

 

 





