---
title: Funzione glClipPlane (Gl.h)
description: La funzione glClipPlane specifica un piano rispetto al quale viene ritagliata tutta la geometria.
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- Funzione glClipPlane OpenGL
topic_type:
- apiref
api_name:
- glClipPlane
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb55edd88b8c8dcd6b4481e60dfc05a012bb79f4f484fde8987e9ed23239d837
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618041"
---
# <a name="glclipplane-function"></a>Funzione glClipPlane

La **funzione glClipPlane** specifica un piano rispetto al quale viene ritagliata tutta la geometria.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Aereo* 
</dt> <dd>

Piano di ritaglio che viene posizionato. I nomi simbolici nel formato GL CLIP PLANE i , dove i è un numero intero compreso tra 0 e \_ \_ GL MAX CLIP  \_ \_ \_ PLANES - 1, sono accettati.

</dd> <dt>

*Equazione* 
</dt> <dd>

Indirizzo di una matrice di quattro valori a virgola mobile e precisione doppia. Questi valori vengono interpretati come equazioni del piano.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *plane* non è un valore accettato.<br/>                                                                                         |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La geometria viene sempre ritagliata rispetto ai limiti di un frustum a sei piani in *x*, *y* e *z*. La **funzione glClipPlane** consente di specificare piani aggiuntivi, non necessariamente perpendicolari all'asse *x,* *y o* *z,* rispetto al quale viene ritagliata tutta la geometria. È possibile specificare fino a un massimo di piani CLIP PLANES MAX, dove GL MAX CLIP PLANES è almeno \_ sei in tutte le \_ \_ \_ \_ \_ implementazioni. Poiché l'area di ritaglio risultante è l'intersezione dei semi spazi definiti, è sempre convessa.

La **funzione glClipPlane** specifica un mezzo spazio usando un'equazione del piano a quattro componenti. Quando si chiama **glClipPlane,** l'equazione viene trasformata dall'inverso della matrice della visualizzazione modello e archiviata nelle coordinate oculare risultanti. Le successive modifiche alla matrice di modelview non hanno alcun effetto sui componenti dell'equazione del piano archiviati. Se il prodotto del punto delle coordinate oculare di un vertice con i componenti dell'equazione del piano archiviati è positivo o zero, il vertice si trova rispetto al piano di ritaglio. In caso contrario, è out.

Usare le [**funzioni glEnable**](glenable.md) e [**glDisable**](gldisable.md) per abilitare e disabilitare i piani di ritaglio. Chiamare i piani di ritaglio con l'argomento GL \_ CLIP \_ PLANE *i*, dove *i* è il numero del piano.

Per impostazione predefinita, tutti i piani di ritaglio sono definiti come (0,0,0,0) nelle coordinate oculare e sono disabilitati.

È sempre il caso in cui GL \_ CLIP \_ PLANE *i* = GL \_ CLIP \_ PLANE0 + *i*.

Le funzioni seguenti recuperano informazioni correlate **a glClipPlane:**

[**glGetClipPlane**](glgetclipplane.md)

[**glIsEnabled con**](glisenabled.md) argomento GL \_ CLIP PLANE \_ *i*

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





