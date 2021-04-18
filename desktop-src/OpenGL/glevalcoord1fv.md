---
title: funzione glEvalCoord1fv (GL. h)
description: La funzione glEvalCoord1fv valuta i mapping unidimensionali abilitati.
ms.assetid: d5c1cc99-ecf6-4d78-99bb-953b4c362ff4
keywords:
- funzione glEvalCoord1fv OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord1fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9acb1f7060367b02fa836fb149151b8278b7274
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301922"
---
# <a name="glevalcoord1fv-function"></a>glEvalCoord1fv (funzione)

La funzione **glEvalCoord1fv** valuta i mapping unidimensionali abilitati.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glEvalCoord1fv(
   const GLfloat *u
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*u* 
</dt> <dd>

Puntatore a una matrice che contiene la coordinata di dominio *u*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La funzione [**glEvalCoord1fv**](glevalcoord1dv.md) valuta le mappe unidimensionali abilitate all'argomento *u*. Definire Maps con [**glMap1**](glmap1.md). Abilitarli o disabilitarli con [**glEnable**](glenable.md) e [**glDisable**](gldisable.md).

Quando viene eseguita una delle funzioni **glEvalCoord** , vengono valutate tutte le mappe attualmente abilitate della dimensione indicata. Quindi, per ogni mappa abilitata, è come se la funzione OpenGL corrispondente venisse eseguita con il valore calcolato. Ovvero, se \_ \_ è abilitato l'indice GL MAPPA1 o GL \_ map2 \_ , viene simulata una funzione [**glIndex**](glindex-functions.md) . Se GL \_ Mappa1 \_ Color \_ 4 o GL \_ map2 \_ Color \_ 4 è abilitato, viene simulata una funzione **glcolor** . Se GL \_ Mappa1 \_ Normal o GL \_ map2 \_ Normal è abilitato, viene prodotto un vettore normale e, se è presente una \_ MAPPA1 \_ trama \_ Coord \_ 1, GL \_ Mappa1 \_ trama \_ Coord \_ 2, GL \_ Mappa1 \_ texture \_ Coord \_ 3, GL \_ Mappa1 \_ texture \_ Coord \_ 4, GL \_ map2 \_ texture \_ Coord \_ 1, GL \_ map2 \_ texture \_ Coord \_ 2, GL \_ map2 \_ texture \_ Coord \_ 3 e GL \_ map2 \_ texture \_ Coord \_ 4 è abilitato, viene simulata una funzione [**glTexCoord**](gltexcoord-functions.md) appropriata.

OpenGL usa i valori valutati anziché i valori correnti per le valutazioni abilitate e i valori correnti in caso contrario, per le coordinate di colore, indice dei colori, normale e trama. Tuttavia, i valori valutati non aggiornano i valori correnti. Pertanto, se le funzioni [**glVertex**](glvertex-functions.md) sono intercalate con le funzioni **glEvalCoord** , le coordinate di colore, normali e di trama associate alle funzioni **glVertex** non sono interessate dai valori generati dalle funzioni **glEvalCoord** , ma solo dalle funzioni [**glColor**](glcolor-functions.md) [**, glIndex,**](glindex-functions.md) [**glNormal**](glnormal-functions.md)e [**glTexCoord**](gltexcoord-functions.md) più recenti.

Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glEvalCoord1fv** :

[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Vertex \_ 3

[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Vertex \_ 4

[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ index

[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Color \_ 4

[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Normal

[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 1

[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 2

[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 3

[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 4

[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Vertex \_ 3

[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Vertex \_ 4

[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ index

[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Color \_ 4

[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Normal

[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 1

[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 2

[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 3

[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 4

[**glIsEnabled**](glisenabled.md) con argomento GL \_ auto \_ Normal

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





