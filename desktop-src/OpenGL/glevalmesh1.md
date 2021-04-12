---
title: funzione glEvalMesh1 (GL. h)
description: Calcola una griglia unidimensionale di punti o linee.
ms.assetid: 176a4b81-f1a7-42fc-8ecd-bba77a0ec5b3
keywords:
- funzione glEvalMesh1 OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8950dcf397816fca8eb5a6add45c45512c48866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518094"
---
# <a name="glevalmesh1-function"></a>glEvalMesh1 (funzione)

Calcola una griglia unidimensionale di punti o linee.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glEvalMesh1(
   GLenum mode,
   GLint  i1,
   GLint  i2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mode* 
</dt> <dd>

Valore che specifica se calcolare una mesh unidimensionale di punti o linee. Sono accettate le costanti simboliche seguenti: GL \_ Point e GL \_ line.

</dd> <dt>

*I1* 
</dt> <dd>

Primo valore integer per la variabile di dominio Grid i.

</dd> <dt>

*I2* 
</dt> <dd>

Ultimo valore integer per la variabile di dominio Grid i.

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

Usare [**glMapGrid**](glmapgrid-functions.md) e [**glEvalMesh**](glevalmesh-functions.md) insieme per generare e valutare in modo efficiente una serie di valori di dominio mappa uniformemente spazi. La funzione **glEvalMesh** esegue il passaggio del dominio Integer di una griglia bidimensionale, il cui intervallo è il dominio delle mappe di valutazione specificate da [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md). Il parametro mode determina se i vertici risultanti sono connessi come punti, linee o poligoni riempiti.

Nel caso unidimensionale, **glEvalMesh1**, la mesh viene generata come se fosse stato eseguito il frammento di codice seguente:

[**glBegin**](glbegin.md)(*tipo*);

for (i = I1; i <= I2; i + = 1)

{

[**glEvalCoord1**](glevalcoord1d.md)(i? u + U1)

}

[**glEnd**](glend.md)();

dove

? u = (U2 U1)/n

e n, U1 e U2 sono gli argomenti della funzione [**glMapGrid1**](glmapgrid1d.md) più recente. Il parametro di *tipo* è \_ punti GL se Mode è il \_ punto GL oppure GL \_ Lines If mode è GL \_ line. Un requisito numerico assoluto è che se i = n, il valore calcolato da i? u + U1 è esattamente U2.

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
</dt> </dl>

 

 





