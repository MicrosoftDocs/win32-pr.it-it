---
title: funzione glFrustum (GL. h)
description: La funzione glFrustum moltiplica la matrice corrente in base a una matrice di prospettive.
ms.assetid: aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3
keywords:
- funzione glFrustum OpenGL
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
ms.openlocfilehash: ce67879ca20819713e61a9392bf77be2f15211d5
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104563948"
---
# <a name="glfrustum-function"></a>glFrustum (funzione)

La funzione **glFrustum** moltiplica la matrice corrente in base a una matrice di prospettive.

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

*sinistra* 
</dt> <dd>

Coordinata per il piano di ritaglio verticale verso sinistra.

</dd> <dt>

*Ok* 
</dt> <dd>

Coordinata per il piano di ritaglio verticale a destra.

</dd> <dt>

*parte inferiore* 
</dt> <dd>

Coordinata per il piano di ritaglio orizzontale inferiore.

</dd> <dt>

*top* 
</dt> <dd>

Coordinata per il piano di ritaglio orizzontale inferiore.

</dd> <dt>

*zNear* 
</dt> <dd>

Distanze rispetto al piano di ritaglio quasi approfondito. Deve essere un valore positivo.

</dd> <dt>

*zFar* 
</dt> <dd>

Distanze per i piani di ritaglio molto profondi. Deve essere un valore positivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *zNear* o *zFar* non è postitive.<br/>                                                                                       |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glFrustum** descrive una matrice di prospettive che produce una proiezione prospettica. I parametri (*Left*, *Bottom*, *zNear*) e (*right*, *Top*, *zNear*) specificano i punti sul piano di ritaglio vicino di cui è stato eseguito il mapping rispettivamente agli angoli inferiore sinistro e superiore destro della finestra, supponendo che l'occhio si trovi in (0, 0, 0). Il parametro *zFar* specifica il percorso del piano di ritaglio estremo. Sia *zNear* che *zFar* devono essere positivi. La matrice corrispondente è illustrata nell'immagine seguente.

![Diagramma che mostra la matrice della prospettiva che produce una proiezione prospettica.](images/frust01.png)![Equazioni che mostrano la funzione glFrustum che descrive una matrice di prospettive.](images/frust02.png)

La funzione **glFrustum** moltiplica la matrice corrente in base a questa matrice, con il risultato che sostituisce la matrice corrente. Ovvero, se M è la matrice corrente e F è la matrice della prospettiva tronco, **glFrustum** sostituisce M con m F.

Usare [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) per salvare e ripristinare lo stack della matrice corrente.

La precisione del buffer di profondità è interessata dai valori specificati per *zNear* e *zFar*. Maggiore è il rapporto tra *zFar* e *zNear* , minore è il buffer di profondità che si distingue tra le superfici che si avvicinano tra loro. Se

![Equazione che mostra il rapporto tra distanza e prossimità.](images/frust03.png)

approssimativamente i bit di *log* 2 (*r*) della precisione del buffer di profondità vanno persi. Poiché *r* si avvicina a infinito perché *zNear* si avvicina a zero, è consigliabile non impostare mai *zNear* su zero.

Le funzioni seguenti recuperano informazioni su **glFrustum**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_

**glGet** con argomento GL \_ MODELVIEW \_ Matrix

**glGet** con matrice di \_ proiezione GL argomento \_

**glGet** con argomento della \_ matrice di trama GL \_

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

 

 





