---
title: funzione glMapGrid1f (GL. h)
description: Definisce una mesh unidimensionale. | funzione glMapGrid1f (GL. h)
ms.assetid: 242c0197-2fa6-4356-b536-627660ebd3a7
keywords:
- funzione glMapGrid1f OpenGL
topic_type:
- apiref
api_name:
- glMapGrid1f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75479e8e25098fbfc5b906ba1785913cba9f2e30
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321208"
---
# <a name="glmapgrid1f-function"></a>glMapGrid1f (funzione)

Definisce una mesh unidimensionale.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glMapGrid1f(
   GLint   un,
   GLfloat u1,
   GLfloat u2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*non* 
</dt> <dd>

Il numero di partizioni nell'intervallo di intervallo della griglia \[ U1, U2 \] . Il valore deve essere positivo.

</dd> <dt>

*U1* 
</dt> <dd>

Valore usato come mapping per il valore di dominio della griglia integer i = 0.

</dd> <dt>

*U2* 
</dt> <dd>

Valore usato come mapping per il valore di dominio della griglia integer i = un.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | Una o *VN* non è *un* valore positivo.<br/>                                                                                      |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Le funzioni **glMapGrid** e [glEvalMesh](glevalmesh-functions.md) vengono usate in tandem per generare e valutare in modo efficiente una serie di valori di dominio mappa uniformemente spazi. La funzione glEvalMesh esegue il passaggio del dominio Integer di una griglia bidimensionale, il cui intervallo è il dominio delle mappe di valutazione specificate da [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md).

Le funzioni [**glMapGrid1**](glmapgrid1d.md) e [**glMapGrid2**](glmapgrid2d.md) specificano i mapping della griglia lineare tra le coordinate di griglia integer i (o i e j), per le coordinate della mappa di valutazione a virgola mobile u (o u e v). Per informazioni dettagliate sulla valutazione delle coordinate di e v, vedere [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md) .

La funzione [**glMapGrid1**](glmapgrid1d.md) specifica un singolo mapping lineare, in modo tale che la *coordinata* della griglia Integer 0 sia mappata esattamente a U1 e che le coordinate della griglia integer non siano corrette per *U2*. Tutte le altre coordinate della griglia integer *di cui è* stato eseguito il mapping:

*u = i (U2 U1)/un + U1*

La funzione [**glMapGrid2**](glmapgrid2d.md) specifica due mapping lineari di questo tipo. Viene eseguito il mapping tra le coordinate della griglia integer *i = 0* esattamente la *U1* e la coordinata di griglia integer *i = un* esattamente con *U2*. L'altra coordinata della griglia di tipo integer *j = 0* esattamente alla *V1* e la coordinata della griglia integer *j = VN* esattamente alla versione *v2*. Sono state mappate altre coordinate della griglia integer i e j

*u = i (U2 U1)/un + U1*

*v = j (v2 v1)/VN + V1*

I mapping specificati da [**glMapGrid**](glmapgrid1d.md) vengono usati in modo identico da [glEvalMesh](glevalmesh-functions.md) e [**glEvalPoint**](glevalpoint.md).

Le funzioni seguenti consentono di recuperare informazioni correlate a [**glMapGrid**](glmapgrid1d.md):

<dl>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Mappa1 \_ Grid \_ Domain  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ map2 \_ Grid \_ Domain  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento dei \_ \_ segmenti della griglia Mappa1 \_  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento dei \_ \_ segmenti della griglia map2 \_  
</dl>

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**Remo**](glend.md)
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

 

 





