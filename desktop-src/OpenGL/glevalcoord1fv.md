---
title: Funzione glEvalCoord1fv (Gl.h)
description: La funzione glEvalCoord1fv valuta le mappe unidimensionali abilitate.
ms.assetid: d5c1cc99-ecf6-4d78-99bb-953b4c362ff4
keywords:
- Funzione glEvalCoord1fv OpenGL
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
ms.openlocfilehash: 2093925d26471f8f9127382661a6e502b020680d3f67314fecd7a5d28fe77632
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616218"
---
# <a name="glevalcoord1fv-function"></a>Funzione glEvalCoord1fv

La **funzione glEvalCoord1fv** valuta le mappe unidimensionali abilitate.

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

Puntatore a una matrice contenente la coordinata di dominio *u*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

La [**funzione glEvalCoord1fv**](glevalcoord1dv.md) valuta le mappe unidimensionali abilitate nell'argomento *u*. Definire le mappe [**con glMap1.**](glmap1.md) Abilitarli o disabilitarli [**con glEnable**](glenable.md) [**e glDisable**](gldisable.md).

Quando viene emessa **una delle funzioni glEvalCoord,** vengono valutate tutte le mappe attualmente abilitate della dimensione indicata. Quindi, per ogni mappa abilitata, è come se la funzione OpenGL corrispondente fosse stata rilasciata con il valore calcolato. Ciò significa che se GL \_ MAP1 INDEX o GL MAP2 INDEX è \_ \_ \_ abilitato, viene simulata una funzione [**glIndex.**](glindex-functions.md) Se GL \_ MAP1 \_ COLOR 4 o GL MAP2 COLOR 4 è abilitato, viene simulata una funzione \_ \_ \_ \_ **glcolor.** Se GL MAP1 NORMAL o GL MAP2 NORMAL è abilitato, Viene prodotto un vettore normale e, se uno qualsiasi tra \_ \_ GL \_ \_ \_ MAP1 TEXTURE \_ \_ COORD \_ 1, GL \_ MAP1 TEXTURE \_ \_ \_ COORD 2, GL \_ MAP1 TEXTURE \_ \_ \_ \_ COORD 3, GL MAP1 \_ TEXTURE \_ COORD \_ 4, \_ GL \_ \_ \_ \_ MAP2 TEXTURE COORD 1, GL MAP2 \_ TEXTURE \_ COORD \_ 2, GL \_ MAP2 TEXTURE \_ COORD 3 e GL MAP2 TEXTURE COORD 4 \_ \_ \_ \_ \_ \_ [](gltexcoord-functions.md) è abilitata, viene simulata una funzione glTexCoord appropriata.

OpenGL usa i valori valutati anziché i valori correnti per le valutazioni abilitate e i valori correnti in caso contrario, per le coordinate di colore, indice dei colori, normale e trama. Tuttavia, i valori valutati non aggiornano i valori correnti. Pertanto, se le funzioni [**glVertex**](glvertex-functions.md) sono intersperse con funzioni **glEvalCoord,** le coordinate di colore, normale e trama associate alle funzioni **glVertex** non sono interessate dai valori generati dalle funzioni **glEvalCoord,** ma solo dalle funzioni [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md)e [**glTexCoord**](gltexcoord-functions.md) più recenti.

Le funzioni seguenti recuperano informazioni correlate **alla funzione glEvalCoord1fv:**

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP1 \_ VERTEX \_ 3

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP1 \_ VERTEX \_ 4

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP1 \_ INDEX

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP1 \_ COLOR \_ 4

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP1 \_ NORMAL

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP2 \_ VERTEX \_ 3

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP2 \_ VERTEX \_ 4

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP2 \_ INDEX

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP2 \_ COLOR \_ 4

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP2 \_ NORMAL

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 1

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 4

[**glIsEnabled con**](glisenabled.md) argomento GL \_ AUTO \_ NORMAL

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
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

 

 





