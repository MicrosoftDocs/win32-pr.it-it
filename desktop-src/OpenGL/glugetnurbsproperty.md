---
title: funzione gluGetNurbsProperty (Glu. h)
description: La funzione gluGetNurbsProperty ottiene una proprietà di logica B-spline (NURBS) non uniforme.
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- funzione gluGetNurbsProperty OpenGL
topic_type:
- apiref
api_name:
- gluGetNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583da688e3495ebc2eb9d6f71972658c6426469c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119531"
---
# <a name="glugetnurbsproperty-function"></a>gluGetNurbsProperty (funzione)

La funzione **gluGetNurbsProperty** ottiene una proprietà di logica B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluGetNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  *value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*juje* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*property* 
</dt> <dd>

Proprietà di cui è necessario recuperare il valore. Sono validi i valori seguenti: \_ tolleranza di campionamento Glu \_ , modalità di \_ visualizzazione Glu \_ , \_ abbattimento Glu, GLU \_ auto \_ Load \_ Matrix, Glu \_ parametrica \_ tolerance, Glu \_ Sampling \_ Method, Glu \_ U \_ Step e Glu \_ V \_ Step.

</dd> <dt>

*value* 
</dt> <dd>

Puntatore alla posizione in cui viene scritto il valore della proprietà denominata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Utilizzare **gluGetNurbsProperty** per recuperare le proprietà archiviate in un oggetto NURBS. Queste proprietà influiscono sulla modalità di rendering delle curve e delle superfici NURBS. Per informazioni sulle proprietà NURBS, vedere [**gluNurbsProperty**](glunurbsproperty.md).

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

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[**gluNurbsProperty**](glunurbsproperty.md)
</dt> </dl>

 

 





