---
title: Funzione glEvalMesh1 (Gl.h)
description: Calcola una griglia unidimensionale di punti o linee.
ms.assetid: 176a4b81-f1a7-42fc-8ecd-bba77a0ec5b3
keywords:
- Funzione glEvalMesh1 OpenGL
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
ms.openlocfilehash: c325134a8a8fd60afdc764eebc8a4de9bd507b5b667ebb8e1b2ab967edcd7e77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625471"
---
# <a name="glevalmesh1-function"></a>Funzione glEvalMesh1

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

Valore che specifica se calcolare una mesh unidimensionale di punti o linee. Vengono accettate le costanti simboliche seguenti: GL \_ POINT e GL \_ LINE.

</dd> <dt>

*i1* 
</dt> <dd>

Primo valore intero per la variabile di dominio della griglia i.

</dd> <dt>

*i2* 
</dt> <dd>

Ultimo valore intero per la variabile di dominio della griglia i.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | Indica che *la modalità* non è un valore accettato. <br/>                                                                            |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md). <br/> |



## <a name="remarks"></a>Commenti

Usare [**glMapGrid e**](glmapgrid-functions.md) [**glEvalMesh insieme**](glevalmesh-functions.md) per generare e valutare in modo efficiente una serie di valori di dominio mappa spaziati uniformemente. La **funzione glEvalMesh** passa attraverso il dominio intero di una griglia uno o bidimensionale, il cui intervallo è il dominio delle mappe di valutazione specificate da [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md). Il parametro mode determina se i vertici risultanti sono connessi come punti, linee o poligoni riempiti.

Nel caso unidimensionale, **glEvalMesh1,** la mesh viene generata come se fosse stato eseguito il frammento di codice seguente:

[**glBegin**](glbegin.md)(*tipo*);

for (i = i1; i <= i2; i += 1)

{

[**glEvalCoord1**](glevalcoord1d.md)(i?u + u1)

}

[**glEnd**](glend.md)( );

dove

?u = (u2 u1) / n

e n, u1 e u2 sono gli argomenti della funzione [**glMapGrid1**](glmapgrid1d.md) più recente. Il *parametro di* tipo è GL POINTS se mode è GL POINT o GL LINES se la modalità è GL \_ \_ \_ \_ LINE. L'unico requisito numerico assoluto è che se i = n, il valore calcolato da i?u + u1 è esattamente u2.

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
</dt> </dl>

 

 





