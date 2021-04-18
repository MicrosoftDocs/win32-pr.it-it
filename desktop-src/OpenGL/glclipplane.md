---
title: funzione glClipPlane (GL. h)
description: La funzione glClipPlane specifica un piano in base al quale viene ritagliata tutta la geometria.
ms.assetid: b70d2c30-7502-4399-8c08-5ec9a2a1919c
keywords:
- funzione glClipPlane OpenGL
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
ms.openlocfilehash: 33380203b30b7a3a2e37ee5d58a47fec845cbc1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301928"
---
# <a name="glclipplane-function"></a>glClipPlane (funzione)

La funzione **glClipPlane** specifica un piano in base al quale viene ritagliata tutta la geometria.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glClipPlane(
         GLenum   plane,
   const GLdouble *equation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*aereo* 
</dt> <dd>

Il piano di ritaglio in corso di posizionamento. I nomi simbolici del formato GL \_ clip \_ plane *i*, dove *i* è un numero intero compreso tra 0 e GL \_ Max clip plane \_ \_ -1, vengono accettati.

</dd> <dt>

*equazione* 
</dt> <dd>

Indirizzo di una matrice di quattro valori a virgola mobile e precisione doppia. Questi valori vengono interpretati come un'equazione del piano.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | il *piano* non è un valore accettato.<br/>                                                                                         |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La geometria viene sempre tagliata in base ai limiti di un tronco a sei piani in *x*, *y* e *z*. La funzione **glClipPlane** consente di specificare piani aggiuntivi, non necessariamente perpendicolari all'asse *x*, asse *y* o asse *z*, in base al quale viene ritagliata tutta la geometria. È possibile specificare fino a GL max piani di \_ \_ ritaglio dei piani \_ , dove GL \_ Max \_ clip \_ Planes è almeno sei in tutte le implementazioni. Poiché l'area di visualizzazione risultante è l'intersezione tra gli spazi vuoti definiti, è sempre convessa.

La funzione **glClipPlane** specifica una metà dello spazio usando un'equazione del piano a quattro componenti. Quando si chiama **glClipPlane**, l'*equazione* viene trasformata dall'inverso della matrice Modelview e archiviata nelle coordinate oculari risultanti. Le modifiche successive alla matrice Modelview non hanno effetto sui componenti dell'equazione del piano archiviati. Se il prodotto a punti delle coordinate oculari di un vertice con i componenti dell'equazione del piano archiviato è positivo o zero, il vertice si trova in rispetto al piano di ritaglio. In caso contrario, è out.

Usare le funzioni [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) per abilitare e disabilitare i piani di ritaglio. Chiamare i piani di ritaglio con l'argomento GL \_ clip \_ plane *i*, dove *i* è il numero del piano.

Per impostazione predefinita, tutti i piani di ritaglio sono definiti come (0, 0, 0, 0) nelle coordinate degli occhi e sono disabilitati.

È sempre il caso GL \_ clip \_ plane *i* = GL \_ clip \_ PLANE0 + *i*.

Le funzioni seguenti consentono di recuperare informazioni correlate a **glClipPlane**:

[**glGetClipPlane**](glgetclipplane.md)

[**glIsEnabled**](glisenabled.md) con argomento GL \_ clip \_ plane *i*

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





