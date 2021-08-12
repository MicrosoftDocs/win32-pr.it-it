---
title: Funzione glEnd (Gl.h)
description: Le funzioni glBegin e glend delimitano i vertici di una primitiva o di un gruppo di primitive simili. | Funzione glEnd (Gl.h)
ms.assetid: 040f8573-683c-4a8a-ae51-66abb0541ac4
keywords:
- Funzione glEnd OpenGL
topic_type:
- apiref
api_name:
- glEnd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0817bec7874b9a3a58e28653ff10497eb1e3f5e5170c57dbe2c26a6b20b64460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616553"
---
# <a name="glend-function"></a>Funzione glEnd

Le [**funzioni glBegin**](glbegin.md) **e glend** delimitano i vertici di una primitiva o di un gruppo di primitive simili.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glEnd(void);
```



## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Il codice di errore seguente può essere recuperato dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | Una funzione diversa da **glVertex**, **glColor**, **glIndex**, **glNormal**, **glTexCoord**, **glEvalCoord**, **glEvalPoint**, **glMaterial**, **glEdgeFlag**, **glCallList** o **glCallLists** è stata chiamata tra **glBegin** e il **glEnd corrispondente.** La funzione **glEnd è** stata chiamata prima della chiamata **di glBegin** corrispondente oppure **glBegin** è stata chiamata all'interno di una **sequenza glBegin** / **glEnd.** <br/> |



## <a name="remarks"></a>Commenti

Le [**funzioni glBegin**](glbegin.md) **e glend** delimitano i vertici che definiscono una primitiva o un gruppo di primitive simili. La **funzione glBegin** accetta un singolo argomento che specifica quale delle dieci primitive compose i vertici. Considerando *n* come numero intero a partire da uno e *N* come numero totale di vertici specificati, le interpretazioni sono le seguenti:

-   È possibile usare solo un subset di funzioni OpenGL tra **glBegin** e **glEnd**. Le funzioni che è possibile usare sono:

    -   [**glVertex**](glvertex-functions.md)
    -   [**glColor**](glcolor-functions.md)
    -   [**glIndex**](glindex-functions.md)
    -   [**glNormal**](glnormal-functions.md)
    -   [**glTexCoord**](gltexcoord-functions.md)
    -   [**glEvalCoord**](glevalcoord-functions.md)
    -   [**glEvalPoint**](glevalpoint.md)
    -   [**glMaterial**](glmaterial-functions.md)
    -   [**glEdgeFlag**](gledgeflag-functions.md)

    È anche possibile usare [**glCallList**](glcalllist.md) o [**glCallLists**](glcalllists.md) per eseguire elenchi di visualizzazione che includono solo le funzioni precedenti. Se viene chiamata qualsiasi altra funzione OpenGL tra **glBegin** e **glEnd**, il flag di errore viene impostato e la funzione viene ignorata.

-   Indipendentemente dal valore scelto per *mode* in **glBegin**, non esiste alcun limite al numero di vertici che è possibile definire tra **glBegin** e **glEnd**. Le linee, i triangoli, i quadrilateri e i poligoni specificati in modo incompleto non vengono tracciati. La specifica incompleta risulta quando viene fornito un numero troppo piccolo di vertici per specificare anche una singola primitiva o quando viene specificato un multiplo non corretto di vertici. La primitiva incompleta viene ignorata. vengono disegnate le primitive complete.
-   La specifica minima dei vertici per ogni primitiva è: 

    | Numero minimo di vertici | Tipo di primitiva |
    |----------------------------|-------------------|
    | 1                          | point             |
    | 2                          | line              |
    | 3                          | triangolo          |
    | 4                          | Quadrilatero     |
    | 3                          | polygon           |

    

     

-   Le modalità che richiedono un determinato multiplo di vertici sono GL \_ LINES (2), GL \_ TRIANGLES (3), GL \_ QUADS (4) e GL \_ QUAD STRIP \_ (2).

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

[**glBegin**](/windows/desktop/OpenGL/glbegin)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

