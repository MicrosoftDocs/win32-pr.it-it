---
title: Funzione glOrtho (Gl.h)
description: La funzione glOrtho moltiplica la matrice corrente per una matrice ortografica.
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
keywords:
- Funzione glOrtho OpenGL
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
ms.openlocfilehash: b1e06c1740e908c34652a6d39bc7a2334763199d222ff9d1dc00ae733803ada0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795226"
---
# <a name="glortho-function"></a>Funzione glOrtho

La **funzione glOrtho** moltiplica la matrice corrente per una matrice ortografica.

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

*Sinistra* 
</dt> <dd>

Coordinate per il piano di ritaglio verticale sinistro.

</dd> <dt>

*va bene* 
</dt> <dd>

Coordinate per il piano di ritaglio verticale verticale.

</dd> <dt>

*Fondoschiena* 
</dt> <dd>

Coordinate per il piano di ritaglio orizzontale inferiore.

</dd> <dt>

*top* 
</dt> <dd>

Coordinate per i piani di ritaglio orizzontali in alto.

</dd> <dt>

*zNear* 
</dt> <dd>

Distanza dal piano di ritaglio di profondità più vicino. Questa distanza è negativa se il piano deve essere dietro il visualizzatore.

</dd> <dt>

*zFar* 
</dt> <dd>

Distanza dal piano di ritaglio di profondità più lontano. Questa distanza è negativa se il piano deve essere dietro il visualizzatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glOrtho** descrive una matrice prospettica che produce una proiezione parallela. I parametri (*left*, *bottom*, *near*) e (*right*, *top*, *near*) specificano i punti sul piano di ritaglio vicino mappati rispettivamente agli angoli inferiore sinistro e superiore destro della finestra, presupponendo che l'occhio si trovi in corrispondenza di (0, 0, 0). Il *parametro far* specifica la posizione del piano di ritaglio lontano. Sia *zNear che* *zFar* possono essere positivi o negativi. La matrice corrispondente è illustrata nell'immagine seguente.

![Diagramma che mostra la matrice prospettica descritta dalla funzione glOrtho.](images/ortho1.png)

dove

![Equazioni che descrivono la matrice prospettica.](images/ortho2.png)

La matrice corrente viene moltiplicata per questa matrice con il risultato che sostituisce la matrice corrente. Ciò significa che se M è la matrice corrente e O è la matrice dell'orto, M viene sostituito con M O.

Usare [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix** per salvare e ripristinare lo stack di matrici corrente. Usare [**glMatrixMode**](glmatrixmode.md) per impostare la matrice corrente.

Le funzioni seguenti recuperano informazioni correlate **a glOrtho**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MATRIX \_ MODE

**glGet** con argomento GL \_ MODELVIEW \_ MATRIX

**glGet con** argomento GL \_ PROJECTION \_ MATRIX

**glGet** con argomento GL \_ TEXTURE \_ MATRIX

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

 

 





