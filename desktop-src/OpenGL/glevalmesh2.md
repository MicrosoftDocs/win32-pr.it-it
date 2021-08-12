---
title: Funzione glEvalMesh2 (Gl.h)
description: Calcola una griglia bidimensionale di punti o linee.
ms.assetid: 21e94388-903e-4b9d-8e54-9c914d0ce372
keywords:
- Funzione glEvalMesh2 OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d5f1a16b1ceda2c13f24a779032b0e920d364db46167a9dc02ca2b27277262
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616107"
---
# <a name="glevalmesh2-function"></a>Funzione glEvalMesh2

Calcola una griglia bidimensionale di punti o linee.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glEvalMesh2(
   GLenum mode,
   GLint  i1,
   GLint  i2,
   GLint  j1,
   GLint  j2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mode* 
</dt> <dd>

Valore che specifica se calcolare una mesh bidimensionale di punti, linee o poligoni. Sono accettate le costanti simboliche seguenti: GL \_ POINT, GL \_ LINE e GL \_ FILL.

</dd> <dt>

*i1* 
</dt> <dd>

Primo valore intero per la variabile di dominio della griglia i.

</dd> <dt>

*i2* 
</dt> <dd>

Ultimo valore intero per la variabile di dominio della griglia i.

</dd> <dt>

*j1* 
</dt> <dd>

Primo valore intero per la variabile di dominio della griglia j.

</dd> <dt>

*j2* 
</dt> <dd>

Ultimo valore intero per la variabile di dominio della griglia j.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | Indica che *la modalità* non è un valore accettato. <br/>                                                                            |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). <br/> |



## <a name="remarks"></a>Commenti

Usare [**glMapGrid**](glmapgrid-functions.md) e [**glEvalMesh**](glevalmesh-functions.md) in tandem per generare e valutare in modo efficiente una serie di valori di dominio mappa spaziati in modo uniforme. La **funzione glEvalMesh** attraversa il dominio intero di una griglia unidimensionale o bidimensionale, il cui intervallo è il dominio delle mappe di valutazione specificate da [**glMap1**](glmap1.md) e [**glMap2.**](glmap2.md) Il parametro mode determina se i vertici risultanti sono connessi come punti, linee o poligoni riempiti.

Nel caso bidimensionale **glEvalMesh2**,

? u = (u2 u1)/n

? v = (v2 v1)/m,

dove n, u1, u2, m, v1 e v2 sono gli argomenti della funzione [**glMapGrid2 più**](glmapgrid-functions.md) recente. Quindi, se *mode* è GL \_ FILL, **glEvalMesh2** equivale a:

for (j = j1; j < j2; j += 1)

{

[**glBegin**](glbegin.md)(GL \_ QUAD \_ STRIP);

for (i = i1; i <= i2; i += 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , j ? v + v1);

[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , (j+1) ? v + v1);

}

[**glEnd**](glend.md)( ); }

Se *mode* è GL \_ LINE, una chiamata a **glEvalMesh2** equivale a:

for (j = j1; j <= j2; j += 1)

{

[**glBegin**](glbegin.md)(GL \_ LINE \_ STRIP);

for (i = i1; i <= i2; i += 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);

}

[**glEnd**](glend.md)( );

}

for (i = i1; i <= i2; i += 1)

{

[**glBegin**](glbegin.md)(GL \_ LINE \_ STRIP);

for (j = j1; j <= j1; j += 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);

}

glEnd( );

}

Infine, se *mode* è GL \_ POINT, una chiamata a **glEvalMesh2** equivale a:

[**glBegin**](glbegin.md)(GL \_ POINTS);

for (j = j1; j <= j2; j += 1)

{

for (i = i1; i <= i2; i += 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);

}

}

[**glEnd**](glend.md)( );

In tutti e tre i casi, gli unici requisiti numerici assoluti sono che se i = n, il valore calcolato da i? u + u1 è esattamente u2 e se j = m, il valore calcolato da j? v + v1 è esattamente v2. Le funzioni seguenti recuperano informazioni relative **a glEvalMesh:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MAP1 \_ GRID \_ DOMAIN

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MAP2 \_ GRID \_ DOMAIN

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MAP1 \_ GRID \_ SEGMENTS

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MAP2 \_ GRID \_ SEGMENTS

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

 





