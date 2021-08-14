---
title: Funzione glBegin (Gl.h)
description: Le funzioni glBegin e abred delimitano i vertici di una primitiva o di un gruppo di primitive like. | Funzione glBegin (Gl.h)
ms.assetid: 8e8e98f8-89e8-40f5-89c1-492c9e3bbd74
keywords:
- Funzione glBegin OpenGL
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
ms.openlocfilehash: c497542e345b412bdc7955870405e6ee6cfe0503cee22f9320a031e835853345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361156"
---
# <a name="glbegin-function"></a>Funzione glBegin

Le **funzioni glBegin** [**e abred**](glend.md) delimitano i vertici di una primitiva o di un gruppo di primitive like.

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

Primitive o primitive che verranno create dai vertici presentati tra **glBegin** e il successivo [**oggetto .**](glend.md) Di seguito sono riportate le costanti simboliche accettate e i relativi significati:



| Valore                                                                                                                                                                      | Significato                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <dt>**PUNTI \_ GL**</dt> </dl>                          | Considera ogni vertice come un singolo punto. Vertex *n* definisce il punto *n*. *Vengono disegnati* N punti.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <dt>**RIGHE \_ GL**</dt> </dl>                             | Considera ogni coppia di vertici come segmento di linea indipendente. I vertici *2n - 1* e *2n definiscono* la linea *n*. *Vengono disegnate N/2* linee.<br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <dt>**GL \_ LINE \_ STRIP**</dt> </dl>             | Disegna un gruppo connesso di segmenti di linea dal primo vertice all'ultimo. I vertici *n* e *n+1* definiscono la linea *n*. *N - Vengono disegnate 1* linee.<br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <dt>**GL \_ LINE \_ LOOP**</dt> </dl>                | Disegna un gruppo connesso di segmenti di linea dal primo vertice all'ultimo, quindi di nuovo al primo. I vertici *n* e *n + 1* definiscono la linea *n*. L'ultima riga, tuttavia, è definita dai vertici *N* e *1*. *Vengono disegnate* N linee.<br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <dt>**TRIANGOLI GL \_**</dt> </dl>                 | Considera ogni tripletta di vertici come triangolo indipendente. I vertici *3n - 2*, *3n - 1* e *3n definiscono* il triangolo *n*. *Vengono disegnati triangoli N/3.*<br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <dt>**GL \_ TRIANGLE \_ STRIP**</dt> </dl> | Disegna un gruppo connesso di triangoli. Viene definito un triangolo per ogni vertice presentato dopo i primi due vertici. Per n *dispari,* i vertici *n*, *n + 1* e *n + 2* definiscono il *triangolo n*. Per n *anche*, i vertici *n + 1*, *n* e n *+ 2* definiscono il *triangolo n*. *N - Vengono disegnati 2* triangoli.<br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <dt>**VENTOLA \_ TRIANGOLO GL \_**</dt> </dl>       | Disegna un gruppo connesso di triangoli. Viene definito un triangolo per ogni vertice presentato dopo i primi due vertici. I vertici *1*, *n + 1*, *n + 2* definiscono il *triangolo n*. *N - Vengono disegnati 2* triangoli.<br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <dt>**GL \_ QUADS**</dt> </dl>                             | Considera ogni gruppo di quattro vertici come un quadrilatero indipendente. I vertici *4n - 3*, *4n - 2*, *4n - 1* e *4n* definiscono il quadrilatero *n*. *Vengono disegnati n/4* quadrilateri.<br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <dt>**GL \_ QUAD \_ STRIP**</dt> </dl>             | Disegna un gruppo connesso di quadrilateri. Viene definito un quadrilatero per ogni coppia di vertici presentati dopo la prima coppia. I vertici *2n - 1*, *2n*, *2n + 2* e *2n + 1* definiscono il quadrilatero *n*. *N/2 - Vengono* disegnati 1 quadrilatero. Si noti che l'ordine in cui i vertici vengono usati per costruire un quadrilatero dai dati della striscia è diverso da quello usato con dati indipendenti.<br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <dt>**POLIGONO GL \_**</dt> </dl>                       | Disegna un singolo poligono convesso. I vertici *da 1* a *N* definiscono questo poligono.<br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ \_ NON VALIDA**</dt> </dl>      | *la* modalità è stata impostata su un valore non scettico.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | È stata chiamata una funzione diversa da [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [glEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md)o [**glCallLists**](glcalllists.md) tra **glBegin** e il corrispondente [**.**](glend.md) La funzione **che è stata** chiamata prima della chiamata a **glBegin** corrispondente o **glBegin** è stata chiamata all'interno di una **sequenza di glBegin.** /  <br/> |



## <a name="remarks"></a>Commenti

Le **funzioni glBegin** [**e abred**](glend.md) delimitano i vertici che definiscono una primitiva o un gruppo di primitive like. La **funzione glBegin** accetta un singolo argomento che specifica quale delle dieci primitive compose i vertici. Considerando *n* come numero intero a partire da uno e *N* come numero totale di vertici specificato, le interpretazioni sono le seguenti:

-   È possibile usare solo un subset di funzioni OpenGL tra **glBegin** [**e la funzione .**](glend.md) Le funzioni che è possibile usare sono:

    [**glVertex**](glvertex-functions.md)

     

    [**glColor**](glcolor-functions.md)

     

    [**glIndex**](glindex-functions.md)

     

    [**glNormal**](glnormal-functions.md)

     

    [**glTexCoord**](gltexcoord-functions.md)

     

    [**glEvalCoord**](glevalcoord-functions.md)

     

    [**glEvalPoint**](glevalpoint.md)

     

    [**glMaterial**](glmaterial-functions.md)

     

    [**glEdgeFlag**](gledgeflag-functions.md)

    È anche possibile usare [**glCallList**](glcalllist.md) o [**glCallLists**](glcalllists.md) per eseguire elenchi di visualizzazione che includono solo le funzioni precedenti. Se viene chiamata qualsiasi altra funzione OpenGL tra **glBegin** e [**la funzione ,**](glend.md)il flag di errore viene impostato e la funzione viene ignorata.

-   Indipendentemente dal valore scelto per *mode* in **glBegin**, non esiste alcun limite al numero di vertici che è possibile definire tra **glBegin** e [**il parametro .**](glend.md) Linee, triangoli, quadrilateri e poligoni specificati in modo incompleto non vengono disegnate. La specifica incompleta risulta quando viene specificato un numero troppo piccolo di vertici per specificare anche una singola primitiva o quando viene specificato un multiplo non corretto di vertici. La primitiva incompleta viene ignorata. Vengono disegnate le primitive complete.
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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](/windows/desktop/OpenGL/glend)
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

 

