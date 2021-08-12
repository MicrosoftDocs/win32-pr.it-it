---
title: Funzione glPolygonOffset (Gl.h)
description: La funzione glPolygonOffset imposta la scala e le unità utilizzate da OpenGL per calcolare i valori di profondità.
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- Funzione glPolygonOffset OpenGL
topic_type:
- apiref
api_name:
- glPolygonOffset
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 314372c0ce87ef5b75db24e4482d6b621422546abe0c71a34cc9821cb4391997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118614917"
---
# <a name="glpolygonoffset-function"></a>Funzione glPolygonOffset

La **funzione glPolygonOffset** imposta la scala e le unità utilizzate da OpenGL per calcolare i valori di profondità.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Fattore* 
</dt> <dd>

Specifica un fattore di scala utilizzato per creare un offset di profondità variabile per ogni poligono. Il valore iniziale è zero.

</dd> <dt>

*Unità* 
</dt> <dd>

Specifica un valore moltiplicato per un valore specifico dell'implementazione per creare un offset di profondità costante. Il valore iniziale è 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Quando GL POLYGON OFFSET è abilitato, il valore di profondità di ogni frammento verrà offset dopo essere stato interpolato dai valori di profondità \_ \_ dei vertici appropriati. Il valore dell'offset è *il* fattore ?z + r units , dove ?z è una misura della variazione di profondità rispetto all'area dello schermo del poligono e r è il valore più piccolo garantito per produrre un offset risolvibile per \* una determinata \* implementazione. L'offset viene aggiunto prima dell'esecuzione del test di profondità e prima che il valore venga scritto nel buffer di profondità.

La **funzione glPolygonOffset** è utile per il rendering di immagini con linee nascoste, per l'applicazione di decalcomanie alle superfici e per il rendering di solidi con bordi evidenziati.

La **funzione glPolygonOffset** non ha alcun effetto sulle coordinate di profondità posizionate nel buffer di feedback. Non ha alcun effetto sulla selezione.

Le funzioni seguenti recuperano informazioni correlate **a glPolygonOffset**:

-   [**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ POLYGON OFFSET \_ \_ FACTOR
-   [**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ POLYGON OFFSET \_ \_ UNITS
-   [**glIsEnabled con**](glisenabled.md) argomento GL \_ POLYGON OFFSET \_ \_ FILL
-   [**glIsEnabled con**](glisenabled.md) argomento GL \_ POLYGON OFFSET \_ \_ LINE
-   [**glIsEnabled con**](glisenabled.md) l'argomento GL \_ POLYGON OFFSET \_ \_ POINT

> [!Note]  
> La **funzione glPolygonOffset** è disponibile solo in OpenGl versione 1.1 o successiva.

 

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

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> </dl>

 

 





