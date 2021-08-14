---
title: Funzione glMapGrid2f (Gl.h)
description: Definisce una mesh unidimensionale. | Funzione glMapGrid2f (Gl.h)
ms.assetid: f9bc2b0c-dec5-4762-8c99-46546a81893e
keywords:
- Funzione glMapGrid2f OpenGL
topic_type:
- apiref
api_name:
- glMapGrid2f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f37975e7ca88f829286872b5352ff3e59d84fd4d123d457defb01b6d14003dad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358938"
---
# <a name="glmapgrid2f-function"></a>Funzione glMapGrid2f

Definisce una mesh unidimensionale.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glMapGrid2f(
   GLint   un,
   GLfloat u1,
   GLfloat u2,
   GLint   vn,
   GLfloat v1,
   GLfloat v2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*un* 
</dt> <dd>

Numero di partizioni nell'intervallo della griglia \[ u1, u2 \] . Il valore deve essere positivo.

</dd> <dt>

*u1* 
</dt> <dd>

Valore usato come mapping per il valore di dominio della griglia integer i = 0.

</dd> <dt>

*u2* 
</dt> <dd>

Valore usato come mapping per il valore di dominio della griglia integer i = un.

</dd> <dt>

*Vn* 
</dt> <dd>

Numero di partizioni nell'intervallo della griglia \[ v1, v2 \] .

</dd> <dt>

*v1* 
</dt> <dd>

Valore usato come mapping per il valore di dominio della griglia integer j = 0.

</dd> <dt>

*v2* 
</dt> <dd>

Valore usato come mapping per il valore di dominio della griglia integer j = vn.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | Un *o* *vn non* era positivo.<br/>                                                                                      |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Le **funzioni glMapGrid** [e glEvalMesh](glevalmesh-functions.md) vengono usate in tandem per generare e valutare in modo efficiente una serie di valori di dominio mappa spaziati in modo uniforme. La funzione glEvalMesh attraversa il dominio intero di una griglia unidimensionale o bidimensionale, il cui intervallo è il dominio delle mappe di valutazione specificate da [**glMap1**](glmap1.md) e [**glMap2.**](glmap2.md)

Le [**funzioni glMapGrid1**](glmapgrid1d.md) e [**glMapGrid2**](glmapgrid2d.md) specificano i mapping della griglia lineare tra le coordinate della griglia di interi i (o i e j) alle coordinate u (o you e v) della mappa di valutazione a virgola mobile. Vedere [**glMap1**](glmap1.md) e [**glMap2 per**](glmap2.md) informazioni dettagliate su come vengono valutate le coordinate v e .

La [**funzione glMapGrid1**](glmapgrid1d.md) specifica un singolo mapping lineare in modo che la coordinata della griglia di numeri interi 0 sia mappata esattamente a u1 e che la *coordinata* della griglia di interi unififi esattamente *a u2*. Tutte le altre coordinate della griglia *di interi i* vengono mappate in modo che:

*u = i(u2 u1)/un + u1*

La [**funzione glMapGrid2**](glmapgrid2d.md) specifica due mapping lineari di questo tipo. Uno esegue il mapping delle coordinate della griglia di *interi i = 0* esattamente a *u1* e delle coordinate della griglia di *interi i = un* exactly to *u2*. L'altra mappa le coordinate della griglia integer *j = 0* esattamente a *v1* e le coordinate della griglia integer *j = vn* esattamente a *v2.* Viene eseguito il mapping di altre coordinate della griglia di interi i e j in modo che

*u = i(u2 u1)/un + u1*

*v = j (v2 v1)/vn + v1*

I mapping specificati da [**glMapGrid**](glmapgrid1d.md) vengono usati in modo identico da [glEvalMesh](glevalmesh-functions.md) e [**glEvalPoint.**](glevalpoint.md)

Le funzioni seguenti recuperano informazioni correlate [**a glMapGrid:**](glmapgrid1d.md)

<dl>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MAP1 \_ GRID \_ DOMAIN  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MAP2 \_ GRID \_ DOMAIN  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MAP1 \_ GRID \_ SEGMENTS  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MAP2 \_ GRID \_ SEGMENTS  
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

 

 





