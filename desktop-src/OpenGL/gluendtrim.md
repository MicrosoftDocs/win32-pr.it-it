---
title: funzione gluEndTrim (Glu. h)
description: Le funzioni gluBeginTrim e gluEndTrim delimitano una definizione del ciclo di taglio razionale B-spline (NURBS) non uniforme. | funzione gluEndTrim (Glu. h)
ms.assetid: e85cc60b-4492-441d-b778-31a3d52b398a
keywords:
- funzione gluEndTrim OpenGL
topic_type:
- apiref
api_name:
- gluEndTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4105cc911105f0444ba17c6b57a3deb048bc96d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058526"
---
# <a name="gluendtrim-function"></a>gluEndTrim (funzione)

Le funzioni [**gluBeginTrim**](glubegintrim.md) e **gluEndTrim** delimitano una definizione del ciclo di taglio razionale B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluEndTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*juje* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare [**gluBeginTrim**](glubegintrim.md) per contrassegnare l'inizio di un ciclo di trimming e **gluEndTrim** per contrassegnare la fine di un ciclo di taglio. Un ciclo di taglio è un set di segmenti orientati a curva (forma di curva chiusa) che definiscono i limiti di una superficie NURBS. Includere questi cicli di taglio nella definizione di una superficie NURBS, tra le chiamate a [**gluBeginSurface**](glubeginsurface.md) e [**gluEndSurface**](gluendsurface.md).

La definizione di una superficie NURBS può contenere molti cicli di trimming. Se, ad esempio, si scrive una definizione per una superficie NURBS simile a un rettangolo con un foro punzonato, la definizione conterrebbe due cicli di trimming. Un ciclo definisce il bordo esterno del rettangolo. l'altro definisce il foro punzonato. Le definizioni di ognuno di questi cicli di taglio sono racchiuse tra parentesi [](glubegintrim.md)da una coppia di  /  **gluEndTrim** gluBeginTrim.

La definizione di un singolo ciclo di taglio chiuso può essere costituita da più segmenti di curva, ciascuno dei quali viene descritto come una serie di segmenti lineari che formano una curva lineare (vedere [**gluPwlCurve**](glupwlcurve.md)), come una singola curva NURBS (vedere [**gluNurbsCurve**](glunurbscurve.md)) o come una combinazione di entrambi in qualsiasi ordine. Le uniche chiamate di libreria che possono essere visualizzate in una definizione del ciclo di Trimming (tra le chiamate a [**gluBeginTrim**](glubegintrim.md) e **GluEndTrim**) sono **gluPwlCurve** e **gluNurbsCurve**.

L'area visualizzata della superficie NURBS è l'area del dominio a sinistra della curva di taglio Man mano che aumenta il parametro della curva. Pertanto, l'area mantenuta della superficie NURBS si trova all'interno di un ciclo di trimming in senso antiorario e al di fuori di un ciclo di taglio Per il rettangolo indicato in precedenza, il ciclo di taglio per il bordo esterno del rettangolo viene eseguito in senso antiorario, mentre il ciclo di taglio per il foro punzonato viene eseguito in senso orario.

Se si usa più di una curva per definire un singolo ciclo di taglio, i segmenti di curva devono formare un ciclo chiuso (ovvero, l'endpoint di ogni curva deve essere il punto iniziale della curva successiva e l'endpoint della curva finale deve essere il punto iniziale della prima curva). Se gli endpoint della curva sono sufficientemente vicini, ma non esattamente coincidenti, saranno costretti a trovare una corrispondenza. Se gli endpoint non sono sufficientemente vicini, viene restituito un errore (vedere [*gluNurbsCallback*](glunurbs.md)).

Se una definizione del ciclo di trimming contiene più curve, la direzione delle curve deve essere coerente, ovvero l'interno deve trovarsi a sinistra di tutte le curve. È possibile usare i cicli di trimming nidificati purché gli orientamenti della curva si alternano correttamente. Le curve di trimming non possono essere autointersecate, né possono intersecarsi tra loro (o risultati di errore).

Se per una superficie NURBS non vengono fornite informazioni di taglio, viene disegnata l'intera superficie.

## <a name="examples"></a>Esempio

Questo frammento di codice definisce un ciclo di trimming costituito da una curva lineare a tratti e due curve NURBS:

``` syntax
gluBeginTrim(nobj); 
    gluPwlCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_3);  
gluEndTrim(nobj);
```

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

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluEndSurface**](gluendsurface.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> <dt>

[*gluNurbsCallback*](glunurbs.md)
</dt> <dt>

[**gluNurbsCurve**](glunurbscurve.md)
</dt> <dt>

[**gluPwlCurve**](glupwlcurve.md)
</dt> </dl>

 

 





