---
title: funzione glMap1f (GL. h)
description: La funzione glMap1f definisce un analizzatore unidimensionale. | funzione glMap1f (GL. h)
ms.assetid: c016ad80-b507-4e21-829f-f173d5c8dee6
keywords:
- funzione glMap1f OpenGL
topic_type:
- apiref
api_name:
- glMap1f
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eafcbfc40b3359cd8faa6f52f6635c1c86f03f17
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104553843"
---
# <a name="glmap1f-function"></a>glMap1f (funzione)

Le funzioni [**glMap1d**](glmap1d.md) e **glMap1f** definiscono un analizzatore unidimensionale.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glMap1f(
         GLenum  target,
         GLfloat u1,
         GLfloat u2,
         GLint   stride,
         GLint   order,
   const GLfloat *points
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Tipo di valori generati dall'analizzatore. Costanti simboliche. Il parametro *target* è una costante simbolica che indica il tipo di punti di controllo che viene fornito nei *punti* e l'output generato quando viene valutata la mappa. Può assumere uno dei nove valori predefiniti.



| Valore                                                                                                                                                                                          | Significato                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**\_Vertice GL \_ Mappa1 \_ 3**</dt> </dl>                       | Ogni punto di controllo è a tre valori a virgola mobile che rappresentano *x, y* e *z*. Quando viene valutata la mappa vengono generati i comandi [**glVertex3**](glvertex-functions.md) interni.<br/>                                                                                                                                         |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**\_Mappa1 \_ Vertex \_ 4**</dt> </dl>                       | Ogni punto di controllo è rappresentato da quattro valori a virgola mobile che rappresentano *x, y, z* e *w*. Quando viene valutata la mappa vengono generati i comandi [**glVertex4**](glvertex-functions.md) interni.<br/>                                                                                                                                       |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**\_Indice MAPPA1 \_ GL**</dt> </dl>                                 | Ogni punto di controllo è un singolo valore a virgola mobile che rappresenta un indice colori. Quando viene valutata la mappa vengono generati i comandi [**glIndex**](glindex-functions.md) interni. Tuttavia, l'indice corrente non viene aggiornato con il valore di questi comandi di **glIndex** .<br/>                                                    |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**\_Mappa1 \_ colore \_ 4 GL**</dt> </dl>                          | Ogni punto di controllo è rappresentato da quattro valori a virgola mobile che rappresentano rosso, verde, blu e alfa. Quando viene valutata la mappa vengono generati i comandi [**glColor4**](glcolor-functions.md) interni. Tuttavia, il colore corrente non viene aggiornato con il valore di questi comandi di **glColor4** .<br/>                                       |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**\_Normale MAPPA1 \_ GL**</dt> </dl>                              | Ogni punto di controllo è costituito da tre valori a virgola mobile che rappresentano i componenti *x, y* e *z* di un vettore normale. Quando viene valutata la mappa vengono generati i comandi [**glNormal**](glnormal-functions.md) interni. Tuttavia, la normale corrente non viene aggiornata con il valore di questi comandi di **glNormal** .<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**\_Trama GL \_ Mappa1 \_ Coord \_ 1**</dt> </dl> | Ogni punto di controllo è un singolo valore a virgola mobile che rappresenta la coordinata di trama *s* . Quando viene valutata la mappa vengono generati i comandi [**glTexCoord1**](gltexcoord-functions.md) interni. Tuttavia, le coordinate di trama correnti non vengono aggiornate con il valore di questi comandi di **glTexCoord** .<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**\_ \_ Coord trama GL \_ Mappa1 \_ 2**</dt> </dl> | Ogni punto di controllo è costituito da due valori a virgola mobile che rappresentano le coordinate di trama *s* e *t* . Quando viene valutata la mappa vengono generati i comandi [**glTexCoord2**](gltexcoord-functions.md) interni. Tuttavia, le coordinate di trama correnti non vengono aggiornate con il valore di questi comandi di **glTexCoord** .<br/>         |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**\_Trama GL \_ Mappa1 \_ Coord \_ 3**</dt> </dl> | Ogni punto di controllo è costituito da tre valori a virgola mobile che rappresentano le coordinate di trama *s, t* e *r* . Quando viene valutata la mappa vengono generati i comandi [**glTexCoord3**](gltexcoord-functions.md) interni. Tuttavia, le coordinate di trama correnti non vengono aggiornate con il valore di questi comandi di **glTexCoord** .<br/>   |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**\_Trama GL \_ Mappa1 \_ Coord \_ 4**</dt> </dl> | Ogni punto di controllo è costituito da quattro valori a virgola mobile che rappresentano le coordinate di trama *s, t, r* e *q* . Quando viene valutata la mappa vengono generati i comandi [**glTexCoord4**](gltexcoord-functions.md) interni. Tuttavia, le coordinate di trama correnti non vengono aggiornate con il valore di questi comandi di **glTexCoord** .<br/> |



 

</dd> <dt>

*U1* 
</dt> <dd>

Un mapping lineare di *u*, come presentato a [**glEvalCoord1**](glevalcoord-functions.md), a *u*^, la variabile valutata dalle equazioni specificate da questo comando.

</dd> <dt>

*U2* 
</dt> <dd>

Un mapping lineare di *u*, come presentato a [**glEvalCoord1**](glevalcoord-functions.md), a *u*^, la variabile valutata dalle equazioni specificate da questo comando.

</dd> <dt>

*stride* 
</dt> <dd>

Numero di valori float o doppi tra l'inizio di un punto di controllo e l'inizio della successiva nella struttura di dati a cui si fa riferimento nei *punti*. In questo modo è possibile incorporare i punti di controllo in strutture di dati arbitrarie. L'unico vincolo è che i valori per un determinato punto di controllo debbano occupare posizioni di memoria contigue.

</dd> <dt>

*order* 
</dt> <dd>

Numero di punti di controllo. Deve essere un valore positivo.

</dd> <dt>

*punti* 
</dt> <dd>

Puntatore alla matrice di punti di controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *target* non è un valore accettato.<br/>                                                                                        |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *U1* era uguale a *U2*.<br/>                                                                                                    |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *stride* è inferiore al numero di valori in un punto di controllo.<br/>                                                            |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | l' *ordine* è inferiore a un ordine di valutazione massimo o GL \_ \_ \_ .<br/>                                                                         |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Gli analizzatori forniscono un modo per usare il mapping polinomiale o per la logica per produrre vertici, normali, coordinate di trama e colori. I valori prodotti da un analizzatore vengono inviati ad altre fasi dell'elaborazione OpenGL come se fossero stati presentati usando i comandi [**glVertex**](glvertex-functions.md), [**glNormal**](glnormal-functions.md), [**glTexCoord**](gltexcoord-functions.md)e [**glColor**](glcolor-functions.md) , ad eccezione del fatto che i valori generati non aggiornano la normale, le coordinate di trama o il colore corrente.

Tutte le spline polinomiali o razionali di qualsiasi grado (fino al grado massimo supportato dall'implementazione di OpenGL) possono essere descritte usando gli analizzatori. Sono incluse quasi tutte le spline usate nei computer grafici, incluse le spline B, le curve di Bezier, le spline eremite e così via.

Gli analizzatori definiscono le curve in base ai polinomi di Bernstein. Definire **p** () come

![Equazione che mostra la definizione di p ().](images/map01.png)

dove **R**_i_ è un punto di controllo e () è il polinomio di *Bernstein del grado* *n* (*Order*  = *n* + 1):

![Equazione che mostra il polinomio di Bernstein del grado n.](images/map02.png)

Ricordare che

![Equazioni che mostrano l'equivalenza a 1.](images/map03.png)

La funzione **glMap1** viene usata per definire la base e per specificare il tipo di valori da produrre. Una volta definita, una mappa può essere abilitata e disabilitata chiamando [**glEnable**](glenable.md) e **glDisable** con il nome della mappa, uno dei nove valori predefiniti per la *destinazione* descritta in precedenza. La funzione [glEvalCoord1](glevalcoord-functions.md) valuta le mappe unidimensionali abilitate. Quando **glEvalCoord1** presenta un valore *u*, le funzioni Bernstein vengono valutate usando *u*^, dove

![Equazione che mostra la definizione di ^.](images/map04.png)

I parametri *stride*, *Order* e *Points* definiscono l'indirizzamento della matrice per l'accesso ai punti di controllo. Il parametro *Points* è la posizione del primo punto di controllo, che occupa una, due, tre o quattro posizioni di memoria contigue, a seconda della mappa da definire. Il parametro *Order* indica il numero di punti di controllo nella matrice. Il parametro *stride* indica il numero di posizioni float o Double per far avanzare il puntatore alla memoria interna per raggiungere il punto di controllo successivo.

Come nel caso di tutti i comandi OpenGL che accettano puntatori ai dati, è come se il contenuto dei *punti* venisse copiato da **glMap1** prima della restituzione. Le modifiche apportate al contenuto dei *punti* non hanno effetto dopo la chiamata a **glMap1** .

Le funzioni seguenti consentono di recuperare informazioni correlate a **glMap1**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Max \_ eval \_ Order

[**glGetMap**](glgetmap.md)

[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Vertex \_ 3

**glIsEnabled** con argomento GL \_ Mappa1 \_ Vertex \_ 4

**glIsEnabled** con argomento GL \_ Mappa1 \_ index

**glIsEnabled** con argomento GL \_ Mappa1 \_ Color \_ 4

**glIsEnabled** con argomento GL \_ Mappa1 \_ Normal

**glIsEnabled** con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 1

**glIsEnabled** con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 2

**glIsEnabled** con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 3

**glIsEnabled** con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 4

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





