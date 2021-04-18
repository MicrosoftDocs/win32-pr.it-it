---
title: funzione glEvalPoint2 (GL. h)
description: Le funzioni glEvalPoint1 e glEvalPoint2 generano e valutano un singolo punto in una rete mesh. | funzione glEvalPoint2 (GL. h)
ms.assetid: babae9c7-84a8-4a7e-b6f9-97c4e8bd42fe
keywords:
- funzione glEvalPoint2 OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fafe728249f988462b0929873bbb195fed1e7c9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321891"
---
# <a name="glevalpoint2-function"></a>glEvalPoint2 (funzione)

Le funzioni [**glEvalPoint1**](glevalpoint.md) e **glEvalPoint2** generano e valutano un singolo punto in una rete mesh.

## <a name="syntax"></a>Sintassi


```C++
void glEvalPoint2(
   GLint i,
   GLint j
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*i* 
</dt> <dd>

Valore integer per la variabile di dominio Grid *i*.

</dd> <dt>

*j* 
</dt> <dd>

Valore integer per la variabile di dominio Grid *j* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Le funzioni [**glMapGrid**](glmapgrid-functions.md) e [**glEvalMesh**](glevalmesh-functions.md) vengono usate in tandem per generare e valutare in modo efficiente una serie di valori di dominio mappa uniformemente spazi. È possibile utilizzare **glEvalPoint** per valutare un singolo punto della griglia nello stesso Gridspace attraversato da **glEvalMesh**. La chiamata a [**glEvalPoint1**](glevalpoint.md) equivale alla chiamata a

**glEvalCoord1** (*i* ?*u*  + *u* 1);

dove

? *u* = (*u* 2 *u* 1)/*n*

e *n*, *u* 1 e *u* 2 sono gli argomenti della funzione **glMapGrid1** più recente. Il requisito numerico assoluto è che se *i*  =  *n*, il valore calcolato da (*i* ?*u* + U1) è esattamente *u* 2.

Nel caso bidimensionale, **glEvalPoint2**, Let

? *u* = (*u* 2 *u* 1)/*n*

? *v* = (*v* 2 *v* 1)/*m*

dove *n*, *u* 1, *u* 2, *m*, *v* 1 e *v* 2 sono gli argomenti della funzione **glMapGrid2** più recente. Quindi la funzione **glEvalPoint2** equivale a chiamare

**glEvalCoord2** (*i* ?*u*  +  *u* 1, *j* ?*v*  +  *v* 1);

Gli unici requisiti numerici assoluti sono che se *i* = *n*, il valore calcolato da (*i* ?*u*  +  *u* 1) è esattamente U2 e se *j*  =  *m*, il valore calcolato da (*j* ?*v*  +  *v* 1) è esattamente *v* 2.

Le funzioni seguenti consentono di recuperare informazioni relative a [**glEvalPoint1**](glevalpoint.md) e **glEvalPoint2**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Mappa1 \_ Grid \_ Domain

**glGet** con argomento GL \_ map2 \_ Grid \_ Domain

**glGet** con argomento dei \_ \_ segmenti della griglia Mappa1 \_

**glGet** con argomento dei \_ \_ segmenti della griglia map2 \_

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> </dl>

 

 





