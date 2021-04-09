---
title: funzione glBegin (GL. h)
description: Le funzioni glBegin e glEnd delimitano i vertici di una primitiva o di un gruppo di primitive like. | funzione glBegin (GL. h)
ms.assetid: 8e8e98f8-89e8-40f5-89c1-492c9e3bbd74
keywords:
- funzione glBegin OpenGL
topic_type:
- apiref
api_name:
- glBegin
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8227d30adf97bf27fecc19603a5e5e32e4f44822
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969176"
---
# <a name="glbegin-function"></a>glBegin (funzione)

Le funzioni **glBegin** e [**glEnd**](glend.md) delimitano i vertici di una primitiva o di un gruppo di primitive like.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glBegin(
   GLenum mode
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mode* 
</dt> <dd>

Primitive o primitive che verranno create dai vertici presentati tra **glBegin** e il [**glEnd**](glend.md)successivo. Di seguito sono riportate le costanti simboliche accettate e i relativi significati:



| Valore                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <dt>**\_punti GL**</dt> </dl>                          | Considera ogni vertice come un singolo punto. Il vertice *n* definisce il punto *n*. Vengono disegnati *N* punti.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <dt>**\_righe GL**</dt> </dl>                             | Considera ogni coppia di vertici come un segmento di linea indipendente. I vertici *2n-1* e *2n* definiscono la riga *n*. Vengono disegnate le righe *N/2* .<br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <dt>**\_striscia linea \_ GL**</dt> </dl>             | Disegna un gruppo connesso di segmenti di linea dal primo vertice all'ultimo. I vertici *n* e *n + 1* definiscono la riga *n*. Vengono disegnate *N-1* righe.<br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <dt>**\_ciclo linea \_ GL**</dt> </dl>                | Disegna un gruppo connesso di segmenti di linea dal primo vertice all'ultimo, quindi di nuovo alla prima. I vertici *n* e *n + 1* definiscono la riga *n*. L'ultima riga, tuttavia, è definita dai vertici *N* e *1*. Vengono disegnate *N* righe.<br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <dt>**triangoli GL \_**</dt> </dl>                 | Considera ogni tripletta di vertici come un triangolo indipendente. I vertici *3N-2*, *3N-1* e *3N* definiscono il triangolo *n*. Vengono disegnati i triangoli *N/3* .<br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <dt>**\_striscia del triangolo GL \_**</dt> </dl> | Disegna un gruppo di triangoli connessi. Un triangolo viene definito per ogni vertice presentato dopo i primi due vertici. Per Odd *n*, vertici *n*, *n + 1* e *n + 2* definiscono il triangolo *n*. Per even *n*, vertici *n + 1*, *n* e *n + 2* definiscono il triangolo *n*. Vengono disegnati *N-2* triangoli.<br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <dt>**\_ventola del triangolo GL \_**</dt> </dl>       | Disegna un gruppo di triangoli connessi. un triangolo viene definito per ogni vertice presentato dopo i primi due vertici. I vertici *1*, *n + 1*, *n + 2* definiscono il triangolo *n*. Vengono disegnati *N-2* triangoli.<br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <dt>**\_Quad GL**</dt> </dl>                             | Considera ogni gruppo di quattro vertici come un quadrilatero indipendente. Vertici *4N-3*, *4N-2*, *4n-1* e *4N* definiscono il quadrilatero *n*. Vengono disegnati i quadrilateri *N/4* .<br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <dt>**\_ \_ striping GL quad**</dt> </dl>             | Disegna un gruppo di quadrilateri connesso. Un quadrilatero viene definito per ogni coppia di vertici presentati dopo la prima coppia. I vertici *2n-1*, *2n*, *2n + 2* e *2n + 1* definiscono il quadrilatero *n*. Vengono disegnati i quadrilateri *N/2-1* . Si noti che l'ordine in cui i vertici vengono usati per costruire un quadrilatero dai dati della striscia sono diversi da quelli usati con dati indipendenti.<br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <dt>**\_poligono GL**</dt> </dl>                       | Disegna un singolo poligono convesso. I vertici da *1* a *N* definiscono questo poligono.<br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | la *modalità* è stata impostata su un valore non accettato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | Una funzione diversa da [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [GlEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md)o [**glCallLists**](glcalllists.md) è stata chiamata tra **glBegin** e l'oggetto [**glEnd**](glend.md)corrispondente. La funzione **glEnd** è stata chiamata prima della chiamata del **glBegin** corrispondente oppure **glBegin** è stato chiamato all'interno di una sequenza **glBegin** / **glEnd** . <br/> |



## <a name="remarks"></a>Commenti

Le funzioni **glBegin** e [**glEnd**](glend.md) delimitano i vertici che definiscono una primitiva o un gruppo di primitive like. La funzione **glBegin** accetta un solo argomento che specifica quale delle dieci primitive i vertici compongono. Accettando *n* come numero intero a partire da uno e *n* come numero totale di vertici specificati, le interpretazioni sono le seguenti:

-   È possibile usare solo un subset di funzioni OpenGL tra **glBegin** e [**glEnd**](glend.md). Le funzioni che è possibile usare sono:

    [**glVertex**](glvertex-functions.md)

     

    [**glColor**](glcolor-functions.md)

     

    [**glIndex**](glindex-functions.md)

     

    [**glNormal**](glnormal-functions.md)

     

    [**glTexCoord**](gltexcoord-functions.md)

     

    [**glEvalCoord**](glevalcoord-functions.md)

     

    [**glEvalPoint**](glevalpoint.md)

     

    [**glMaterial**](glmaterial-functions.md)

     

    [**glEdgeFlag**](gledgeflag-functions.md)

    È anche possibile usare [**glCallList**](glcalllist.md) o [**glCallLists**](glcalllists.md) per eseguire gli elenchi di visualizzazione che includono solo le funzioni precedenti. Se viene chiamata una qualsiasi altra funzione OpenGL tra **glBegin** e [**glEnd**](glend.md), viene impostato il flag di errore e la funzione viene ignorata.

-   Indipendentemente dal valore scelto per la *modalità* in **glBegin**, non esiste alcun limite al numero di vertici che è possibile definire tra **glBegin** e [**glEnd**](glend.md). Le linee, i triangoli, i quadrilateri e i poligoni specificati in un punto non completo non vengono disegnati. Risultati di specifica incompleti quando vengono forniti un numero troppo basso di vertici per specificare anche una singola primitiva o quando viene specificato un multiplo errato di vertici. La primitiva incompleta viene ignorata; vengono disegnate le primitive complete.
-   La specifica minima dei vertici per ogni primitiva è la seguente: 

    | Numero minimo di vertici | Tipo di primitiva |
    |----------------------------|-------------------|
    | 1                          | point             |
    | 2                          | line              |
    | 3                          | triangolo          |
    | 4                          | Quadrilatero     |
    | 3                          | polygon           |

    

     

-   Le modalità che richiedono un determinato multiplo di vertici sono GL \_ Lines (2), GL \_ triangoli (3), GL \_ quad (4) e GL \_ Quad \_ Strip (2).

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**Remo**](/windows/desktop/OpenGL/glend)
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

 

