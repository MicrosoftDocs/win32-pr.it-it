---
title: Funzione glMapGrid1d (Gl.h)
description: Definisce una mesh unidimensionale. | Funzione glMapGrid1d (Gl.h)
ms.assetid: a0bc822e-dd98-4586-a322-2779e11f38ca
keywords:
- Funzione glMapGrid1d OpenGL
topic_type:
- apiref
api_name:
- glMapGrid1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71fcf2ac8871ab1008a5f0e31c6264383cc790edaebd3decc29dbc2ca39845fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128261"
---
# <a name="glmapgrid1d-function"></a>Funzione glMapGrid1d

Definisce una mesh unidimensionale.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glMapGrid1d(
   GLint    un,
   GLdouble u1,
   GLdouble u2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*un* 
</dt> <dd>

Numero di partizioni nell'intervallo dell'intervallo della griglia \[ u1, u2 \] . Il valore deve essere positivo.

</dd> <dt>

*u1* 
</dt> <dd>

Valore utilizzato come mapping per il valore di dominio della griglia integer i = 0.

</dd> <dt>

*u2* 
</dt> <dd>

Valore utilizzato come mapping per il valore di dominio della griglia integer i = un.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | Un *o* *vn* non era positivo.<br/>                                                                                      |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Usare le **funzioni glMapGrid** e [glEvalMesh](glevalmesh-functions.md) insieme per generare e valutare in modo efficiente una serie di valori di dominio mappa spaziati uniformemente. La funzione glEvalMesh passa attraverso il dominio intero di una griglia uno o bidimensionale, il cui intervallo è il dominio delle mappe di valutazione specificate da [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md).

Le funzioni **glMapGrid1** e [**glMapGrid2**](glmapgrid2d.md) specificano i mapping a griglia lineare tra le coordinate della griglia intere i (o i e j) alle coordinate della mappa di valutazione a virgola mobile u (o u e v). Vedere [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md) per informazioni dettagliate su come vengono valutate le coordinate v e .

La **funzione glMapGrid1** specifica un singolo mapping lineare in modo che la coordinata della griglia integer 0 sia mappata esattamente a u1 e che la *coordinata* della griglia di interi non esezioni il mapping esattamente a *u2*. Tutte le altre coordinate della griglia *intere i* vengono mappate in modo che:

*u = i(u2 u1)/un + u1*

La [**funzione glMapGrid2**](glmapgrid2d.md) specifica due mapping lineari di questo tipo. Una mappa le coordinate della griglia *intere i = 0* esattamente a *u1* e le coordinate della griglia *intere i = un* esattamente a *u2.* L'altra mappa la coordinata della griglia integer *j = 0* esattamente alla *v1* e la coordinata della griglia integer *j = vn* esattamente alla *v2.* Viene eseguito il mapping di altre coordinate della griglia intere i e j in modo che

*u = i(u2 u1)/un + u1*

*v = j (v2 v1)/vn + v1*

I mapping specificati da **glMapGrid** vengono usati in modo identico da [glEvalMesh](glevalmesh-functions.md) e [**glEvalPoint**](glevalpoint.md).

Le funzioni seguenti recuperano informazioni correlate a **glMapGrid**:

<dl>

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ MAP1 \_ GRID \_ DOMAIN  
[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ MAP2 \_ GRID \_ DOMAIN  
[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ MAP1 \_ GRID \_ SEGMENTS  
[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ MAP2 \_ GRID \_ SEGMENTS  
</dl>

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[glEvalMesh](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





