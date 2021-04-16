---
title: funzione glOrtho (GL. h)
description: La funzione glOrtho moltiplica la matrice corrente in base a una matrice ortogonale.
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
keywords:
- funzione glOrtho OpenGL
topic_type:
- apiref
api_name:
- glOrtho
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46abbb0edd2dfc7fc51aaf7fa6519dc5367b109c
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104550712"
---
# <a name="glortho-function"></a>glOrtho (funzione)

La funzione **glOrtho** moltiplica la matrice corrente in base a una matrice ortogonale.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glOrtho(
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

Coordinate per il piano di ritaglio verticale sinistro.

</dd> <dt>

*Ok* 
</dt> <dd>

Coordinate per il piano di ritaglio verticale giustaper.

</dd> <dt>

*parte inferiore* 
</dt> <dd>

Coordinate per il piano di ritaglio orizzontale inferiore.

</dd> <dt>

*top* 
</dt> <dd>

Coordinate per i primi piani di ritaglio orizzontali.

</dd> <dt>

*zNear* 
</dt> <dd>

Distanze rispetto al piano di ritaglio di profondità più vicino. Questa distanza è negativa se il piano deve trovarsi dietro il visualizzatore.

</dd> <dt>

*zFar* 
</dt> <dd>

Distanze rispetto al piano di ritaglio più profondo. Questa distanza è negativa se il piano deve trovarsi dietro il visualizzatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glOrtho** descrive una matrice di prospettive che produce una proiezione parallela. I parametri (*Left*, *Bottom*, *near*) e (*right*, *Top*, *near*) specificano i punti sul piano di ritaglio vicino di cui è stato eseguito il mapping rispettivamente agli angoli inferiore sinistro e superiore destro della finestra, supponendo che l'occhio si trovi in (0, 0, 0). Il parametro *lontano* specifica il percorso del piano di ritaglio estremo. Sia *zNear* che *zFar* possono essere positivi o negativi. La matrice corrispondente è illustrata nell'immagine seguente.

![Diagramma che mostra la matrice della prospettiva descritta dalla funzione glOrtho.](images/ortho1.png)

dove

![Equazioni che descrivono la matrice della prospettiva.](images/ortho2.png)

La matrice corrente viene moltiplicata per questa matrice con il risultato che sostituisce la matrice corrente. Ovvero, se M è la matrice corrente e O è la matrice Ortho, M viene sostituito con M O.

Usare [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix** per salvare e ripristinare lo stack della matrice corrente. Usare [**glMatrixMode**](glmatrixmode.md) per impostare la matrice corrente.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glOrtho**:

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glMatrixMode**](glmatrixmode.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> <dt>

[**glViewport**](glviewport.md)
</dt> </dl>

 

 





