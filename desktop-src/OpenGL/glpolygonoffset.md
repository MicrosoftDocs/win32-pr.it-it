---
title: funzione glPolygonOffset (GL. h)
description: La funzione glPolygonOffset imposta la scala e le unità che OpenGL USA per calcolare i valori di profondità.
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- funzione glPolygonOffset OpenGL
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
ms.openlocfilehash: 84fa7d130fcc300fc1ebe33d091253e33f2d1e03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400701"
---
# <a name="glpolygonoffset-function"></a>glPolygonOffset (funzione)

La funzione **glPolygonOffset** imposta la scala e le unità che OpenGL USA per calcolare i valori di profondità.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Factor* 
</dt> <dd>

Specifica un fattore di scala utilizzato per creare un offset della profondità della variabile per ogni poligono. Il valore iniziale è zero.

</dd> <dt>

*unità* 
</dt> <dd>

Specifica un valore moltiplicato per un valore specifico dell'implementazione per creare un offset di profondità costante. Il valore iniziale è 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Quando l' \_ offset del poligono GL \_ è abilitato, il valore di profondità di ogni frammento verrà sfalsato dopo l'interpolazione tra i valori di profondità dei vertici appropriati. Il valore dell'offset è *Factor* \* ? z + r \* *Units*, dove? z è una misurazione della variazione di profondità rispetto all'area dello schermo del poligono e r è il valore più piccolo garantito per produrre un offset risolvibile per una determinata implementazione. L'offset viene aggiunto prima che il test di profondità venga eseguito e prima che il valore venga scritto nel buffer di profondità.

La funzione **glPolygonOffset** è utile per il rendering di immagini a linee nascoste, per l'applicazione di decalcomanie alle superfici e per il rendering di solidi con bordi evidenziati.

La funzione **glPolygonOffset** non ha effetto sulle coordinate di profondità inserite nel buffer di feedback. Inoltre, non ha alcun effetto sulla selezione.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glPolygonOffset**:

-   [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con \_ \_ fattore offset poligono \_ GL
-   [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con l'argomento \_ \_ unità di offset poligono GL \_
-   [**glIsEnabled**](glisenabled.md) con \_ \_ riempimento offset poligono \_ GL
-   [**glIsEnabled**](glisenabled.md) con argomento \_ linea di \_ offset poligono GL \_
-   [**glIsEnabled**](glisenabled.md) con punto di \_ offset del poligono GL argomento \_ \_

> [!Note]  
> La funzione **glPolygonOffset** è disponibile solo in OpenGl versione 1,1 o successiva.

 

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

 

 





