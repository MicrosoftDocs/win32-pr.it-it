---
title: Funzione gluBeginTrim (Glu.h)
description: Le funzioni gluBeginTrim e gluEndTrim delimitano una definizione di ciclo di taglio B-Spline razionale non uniforme (NURBS). | Funzione gluBeginTrim (Glu.h)
ms.assetid: 636402d0-8f6d-4ad8-84c6-66364025d788
keywords:
- Funzione gluBeginTrim OpenGL
topic_type:
- apiref
api_name:
- gluBeginTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebf103a2476aa856b55319e0eca42b8708da169fcedb34e48362062689727ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937884"
---
# <a name="glubegintrim-function"></a>Funzione gluBeginTrim

Le **funzioni gluBeginTrim** e [**gluEndTrim**](gluendtrim.md) delimitano una definizione di ciclo di taglio B-Spline razionale non uniforme ([NURBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluBeginTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nobj* 
</dt> <dd>

Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare **gluBeginTrim** per contrassegnare l'inizio di un ciclo di taglio e **gluEndTrim** per contrassegnare la fine di un ciclo di taglio. Un ciclo di taglio è un set di segmenti di curva orientati (formando una curva chiusa) che definiscono i limiti di una superficie NURBS. Questi cicli di taglio vengono inclusi nella definizione di una superficie NURBS, tra le chiamate a [**gluBeginSurface**](glubeginsurface.md) [**e gluEndSurface**](gluendsurface.md).

La definizione di una superficie NURBS può contenere molti cicli di taglio. Ad esempio, se si scrive una definizione per una superficie NURBS simile a un rettangolo con un foro perforato, la definizione conterrà due cicli di taglio. Un ciclo definisce il bordo esterno del rettangolo; l'altro definisce il foro perforato. Le definizioni di ognuno di questi cicli di taglio verrebbero racchiuse tra parentesi quadre da una coppia **gluBeginTrim**  /  **gluEndTrim.**

La definizione di un singolo ciclo di taglio chiuso può essere costituita da più segmenti di curva, ognuno descritto come una serie di segmenti di linea che formano una curva lineare (vedere [**gluPwlCurve**](glupwlcurve.md)), come singola curva NURBS (vedere [**gluNurbsCurve**](glunurbscurve.md)) o come combinazione di entrambi in qualsiasi ordine. Le uniche chiamate di libreria che possono essere visualizzate in una definizione di ciclo di trimming (tra le chiamate a **gluBeginTrim** e **gluEndTrim**) sono **gluPwlCurve** e **gluNurbsCurve**.

L'area visualizzata della superficie NURBS è l'area del dominio a sinistra della curva di taglio man mano che il parametro della curva aumenta. Di conseguenza, l'area mantenuta della superficie NURBS si trova all'interno di un ciclo di taglio in senso antiorario e all'esterno di un ciclo di taglio in senso orario. Per il rettangolo indicato in precedenza, il ciclo di taglio per il bordo esterno del rettangolo viene eseguito in senso antiorario, mentre il ciclo di taglio per il foro perforato viene eseguito in senso orario.

Se si usano più curve per definire un singolo ciclo di taglio, i segmenti di curva devono formare un ciclo chiuso, ovvero l'endpoint di ogni curva deve essere il punto iniziale della curva successiva e l'endpoint della curva finale deve essere il punto iniziale della prima curva. Se gli endpoint della curva sono sufficientemente vicini ma non esattamente coincidenti, verranno forzati a corrispondere. Se gli endpoint non sono sufficientemente vicini, viene restituito un errore (vedere [*gluNurbsCallback*](glunurbs.md)).

Se una definizione di ciclo di taglio contiene più curve, la direzione delle curve deve essere coerente, ovvero l'interno deve essere a sinistra di tutte le curve. È possibile usare cicli di taglio annidati purché gli orientamenti della curva si alternano correttamente. Le curve di taglio non possono essere autointersecanti, né intersecarsi tra loro (o risultati di un errore).

Se non vengono fornite informazioni di taglio per una superficie NURBS, viene disegnata l'intera superficie.

## <a name="examples"></a>Esempio

Questo frammento di codice definisce un ciclo di taglio costituito da una curva lineare a senso unico e da due curve NURBS:

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
| Intestazione<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
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

 

 





