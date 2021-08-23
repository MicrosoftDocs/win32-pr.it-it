---
title: Funzione glFrustum (Gl.h)
description: La funzione glFrustum moltiplica la matrice corrente per una matrice prospettica.
ms.assetid: aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3
keywords:
- Funzione glFrustum OpenGL
topic_type:
- apiref
api_name:
- glFrustum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1ca2375206165576405c96528d0590596f4d4d870121f0a30884c8e448ca93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625275"
---
# <a name="glfrustum-function"></a>Funzione glFrustum

La **funzione glFrustum** moltiplica la matrice corrente per una matrice prospettica.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glFrustum(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Sinistra* 
</dt> <dd>

Coordinata per il piano di ritaglio verticale a sinistra.

</dd> <dt>

*va bene* 
</dt> <dd>

Coordinata per il piano di ritaglio verticale destro.

</dd> <dt>

*Fondoschiena* 
</dt> <dd>

Coordinata per il piano di ritaglio orizzontale inferiore.

</dd> <dt>

*top* 
</dt> <dd>

Coordinata per il piano di ritaglio orizzontale inferiore.

</dd> <dt>

*zNear* 
</dt> <dd>

Distanza dal piano di ritaglio vicino alla profondità. Deve essere positivo.

</dd> <dt>

*zFar* 
</dt> <dd>

Distanze ai piani di ritaglio di profondità. Deve essere positivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *zNear* o *zFar* non era postitivo.<br/>                                                                                       |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glFrustum** descrive una matrice prospettica che produce una proiezione prospettica. I parametri (*left*, *bottom*, *zNear*) e (*right*, *top*, *zNear*) specificano i punti sul piano di ritaglio vicino mappati rispettivamente agli angoli inferiore sinistro e superiore destro della finestra, presupponendo che l'occhio si trovi in corrispondenza di (0,0,0). Il *parametro zFar* specifica la posizione del piano di ritaglio lontano. Sia *zNear* che *zFar* devono essere positivi. La matrice corrispondente è illustrata nell'immagine seguente.

![Diagramma che mostra la matrice prospettica che produce una proiezione prospettica.](images/frust01.png)![Equazioni che mostrano la funzione glFrustum che descrive una matrice prospettica.](images/frust02.png)

La **funzione glFrustum** moltiplica la matrice corrente per questa matrice, con il risultato che sostituisce la matrice corrente. In altre informazioni, se M è la matrice corrente e F è la matrice prospettica frustum, **glFrustum** sostituisce M con M F.

Usare [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) per salvare e ripristinare lo stack di matrici corrente.

La precisione del buffer di profondità è interessata dai valori specificati per *zNear* e *zFar.* Maggiore è il rapporto *tra zFar* e *zNear,* meno efficace sarà il buffer di profondità a distinguere tra le superfici vicine. Se

![Equazione che mostra il rapporto tra lontano e vicino.](images/frust03.png)

Circa 2 *(**r*) bit di precisione del buffer di profondità vengono persi. Poiché *r* si avvicina all'infinito quando *zNear* si avvicina a zero, non è mai necessario *impostare zNear* su zero.

Le funzioni seguenti recuperano informazioni **su glFrustum**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ MATRIX \_ MODE

**glGet con** argomento GL \_ MODELVIEW \_ MATRIX

**glGet con** argomento GL \_ PROJECTION \_ MATRIX

**glGet con** argomento GL \_ TEXTURE \_ MATRIX

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

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glOrtho**](glortho.md)
</dt> <dt>

[**glPopMatrix**](glpopmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





