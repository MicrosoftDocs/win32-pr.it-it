---
title: Funzione glEvalPoint2 (Gl.h)
description: Le funzioni glEvalPoint1 e glEvalPoint2 generano e valutano un singolo punto in una mesh. | Funzione glEvalPoint2 (Gl.h)
ms.assetid: babae9c7-84a8-4a7e-b6f9-97c4e8bd42fe
keywords:
- Funzione glEvalPoint2 OpenGL
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
ms.openlocfilehash: 6f0c188ec5f3e8171b8035e58b235bc0c5942e221d6d85a6dd4e5a8ff1786c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675561"
---
# <a name="glevalpoint2-function"></a>Funzione glEvalPoint2

Le [**funzioni glEvalPoint1**](glevalpoint.md) **e glEvalPoint2** generano e valutano un singolo punto in una mesh.

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

Valore intero per la variabile di dominio della griglia *i*.

</dd> <dt>

*j* 
</dt> <dd>

Valore intero per la variabile di dominio della griglia *j* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Le [**funzioni glMapGrid**](glmapgrid-functions.md) [**e glEvalMesh**](glevalmesh-functions.md) vengono usate in tandem per generare e valutare in modo efficiente una serie di valori di dominio mappa spaziati in modo uniforme. È possibile usare **glEvalPoint** per valutare un singolo punto della griglia nello stesso spazio della griglia che viene attraversato da **glEvalMesh.** Chiamare [**glEvalPoint1**](glevalpoint.md) equivale a chiamare

**glEvalCoord1** (*i* ?*u*  + *u* 1 );

dove

? *u* = (*u* 2 *u* 1 )/*n*

e *n*, *u* 1 e *u* 2 sono gli argomenti per la funzione **glMapGrid1 più** recente. L'unico requisito numerico assoluto è che, *se i*  =  *n*, il valore calcolato da (*i ?* *u* + u1 ) è esattamente *u* 2 .

Nel caso bidimensionale **glEvalPoint2**,

? *u* = (*u* 2 *u* 1 )/*n*

? *v* = (*v* 2 *v* 1 )/*m*

dove *n*, *u* 1 , *u* 2 , *m*, *v* 1 e *v* 2 sono gli argomenti della funzione **glMapGrid2 più** recente. La funzione **glEvalPoint2** equivale quindi alla chiamata a

**glEvalCoord2** (*i* ?*u*  +  *u* 1 , *j* ?*v*  +  *1*);

Gli unici requisiti numerici assoluti sono che, *se i* = *n*, il valore calcolato da (*i ?* *u*  +  *u* 1 ) è esattamente u2 e, se *j*  =  *m*, il valore calcolato da (*j* ?*v*  +  *v* 1 ) è esattamente *v* 2 .

Le funzioni seguenti recuperano informazioni relative [**a glEvalPoint1**](glevalpoint.md) e **glEvalPoint2:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MAP1 \_ GRID \_ DOMAIN

**glGet** con argomento GL \_ MAP2 \_ GRID \_ DOMAIN

**glGet** con argomento GL \_ MAP1 \_ GRID \_ SEGMENTS

**glGet** con argomento GL \_ MAP2 \_ GRID \_ SEGMENTS

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
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

 

 





