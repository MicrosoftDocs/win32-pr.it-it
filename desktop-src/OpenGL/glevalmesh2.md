---
title: funzione glEvalMesh2 (GL. h)
description: Calcola una griglia bidimensionale di punti o linee.
ms.assetid: 21e94388-903e-4b9d-8e54-9c914d0ce372
keywords:
- funzione glEvalMesh2 OpenGL
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
ms.openlocfilehash: 531e9f1f6288116d052c728654cd2cf03f38550a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740671"
---
# <a name="glevalmesh2-function"></a>glEvalMesh2 (funzione)

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

Valore che specifica se calcolare una mesh bidimensionale di punti, linee o poligoni. Sono accettate le costanti simboliche seguenti: GL \_ Point, GL \_ line e GL \_ Fill.

</dd> <dt>

*I1* 
</dt> <dd>

Primo valore integer per la variabile di dominio Grid i.

</dd> <dt>

*I2* 
</dt> <dd>

Ultimo valore integer per la variabile di dominio Grid i.

</dd> <dt>

*J1* 
</dt> <dd>

Primo valore integer per la variabile di dominio Grid j.

</dd> <dt>

*J2* 
</dt> <dd>

Ultimo valore integer per la variabile di dominio Grid j.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | Indica che la *modalità* non è un valore accettato. <br/>                                                                            |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). <br/> |



## <a name="remarks"></a>Commenti

Usare [**glMapGrid**](glmapgrid-functions.md) e [**glEvalMesh**](glevalmesh-functions.md) in tandem per generare e valutare in modo efficiente una serie di valori di dominio mappa uniformemente spazi. La funzione **glEvalMesh** esegue il passaggio del dominio Integer di una griglia bidimensionale, il cui intervallo è il dominio delle mappe di valutazione specificate da [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md). Il parametro mode determina se i vertici risultanti sono connessi come punti, linee o poligoni riempiti.

Nel caso bidimensionale, **glEvalMesh2**, Let

? u = (U2 U1)/n

? v = (v2 v1)/m,

dove n, U1, U2, m, V1 e V2 sono gli argomenti della funzione [**glMapGrid2**](glmapgrid-functions.md) più recente. Quindi, se *mode* è il \_ riempimento GL, **glEvalMesh2** è equivalente a:

per (j = J1; j < J2; j + = 1)

{

[**glBegin**](glbegin.md)(GL \_ Quad \_ Strip);

for (i = I1; i <= I2; i + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), j? v + v1);

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), (j + 1)? v + v1);

}

[**glEnd**](glend.md)(); }

Se *mode* è \_ la riga GL, una chiamata a **glEvalMesh2** è equivalente a:

per (j = J1; j <= J2; j + = 1)

{

[**glBegin**](glbegin.md)( \_ striscia di riga GL \_ );

for (i = I1; i <= I2; i + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);

}

[**glEnd**](glend.md)();

}

for (i = I1; i <= I2; i + = 1)

{

[**glBegin**](glbegin.md)( \_ striscia di riga GL \_ );

per (j = J1; j <= J1; j + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);

}

glEnd ();

}

Infine, se *mode* è \_ il punto GL, una chiamata a **glEvalMesh2** è equivalente a:

[**glBegin**](glbegin.md)( \_ punti GL);

per (j = J1; j <= J2; j + = 1)

{

for (i = I1; i <= I2; i + = 1)

{

[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);

}

}

[**glEnd**](glend.md)();

In tutti e tre i casi, gli unici requisiti numerici assoluti sono che se i = n, il valore calcolato da i? u + U1 è esattamente U2 e se j = m, il valore calcolato da j? v + v1 è esattamente V2. Le funzioni seguenti consentono di recuperare informazioni relative a **glEvalMesh**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Mappa1 \_ Grid \_ Domain

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ map2 \_ Grid \_ Domain

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento dei \_ \_ segmenti della griglia Mappa1 \_

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento dei \_ \_ segmenti della griglia map2 \_

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Libreria<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



 

 





