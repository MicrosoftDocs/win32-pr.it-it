---
title: funzione glMap2d (GL. h)
description: La funzione glMap2d definisce un analizzatore bidimensionale. | funzione glMap2d (GL. h)
ms.assetid: d8645d19-bec1-4efd-a657-6e7d52d706a9
keywords:
- funzione glMap2d OpenGL
topic_type:
- apiref
api_name:
- glMap2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e072635c411c7a3e28977316c388a9b1597fcd1f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234644"
---
# <a name="glmap2d-function"></a>glMap2d (funzione)

Le funzioni **glMap2d** e [**glMap2f**](glmap2f.md) definiscono un analizzatore bidimensionale.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glMap2d(
         GLenum   target,
         GLdouble u1,
         GLdouble u2,
         GLint    ustride,
         GLint    uorder,
         GLdouble v1,
         GLdouble v2,
         GLint    vstride,
         GLint    vorder,
   const GLdouble *points
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Tipo di valori generati dall'analizzatore. Vengono accettate le seguenti costanti simboliche.



| Valore                                                                                                                                                                                          | Significato                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**\_Vertice GL \_ map2 \_ 3**</dt> </dl>                       | Ogni punto di controllo è a tre valori a virgola mobile che rappresentano *x, y* e *z*. Quando viene valutata la mappa vengono generati i comandi [**glVertex3**](glvertex-functions.md) interni.<br/>                                                                                                                                         |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**\_Map2 \_ Vertex \_ 4**</dt> </dl>                       | Ogni punto di controllo è rappresentato da quattro valori a virgola mobile che rappresentano *x, y, z* e *w*. Quando viene valutata la mappa vengono generati i comandi [**glVertex4**](glvertex-functions.md) interni.<br/>                                                                                                                                       |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**\_Indice map2 \_ GL**</dt> </dl>                                 | Ogni punto di controllo è un singolo valore a virgola mobile che rappresenta un indice colori. Quando viene valutata la mappa vengono generati i comandi [**glIndex**](glindex-functions.md) interni. Tuttavia, l'indice corrente non viene aggiornato con il valore di questi comandi di **glIndex** .<br/>                                                    |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**\_Map2 \_ colore \_ 4 GL**</dt> </dl>                          | Ogni punto di controllo è rappresentato da quattro valori a virgola mobile che rappresentano rosso, verde, blu e alfa. Quando viene valutata la mappa vengono generati i comandi [**glColor4**](glcolor-functions.md) interni. Tuttavia, il colore corrente non viene aggiornato con il valore di questi comandi di **glColor4** .<br/>                                       |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**\_Normale map2 \_ GL**</dt> </dl>                              | Ogni punto di controllo è costituito da tre valori a virgola mobile che rappresentano i componenti *x, y* e *z* di un vettore normale. Quando viene valutata la mappa vengono generati i comandi [**glNormal**](glnormal-functions.md) interni. Tuttavia, la normale corrente non viene aggiornata con il valore di questi comandi di **glNormal** .<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**\_Trama GL \_ map2 \_ Coord \_ 1**</dt> </dl> | Ogni punto di controllo è un singolo valore a virgola mobile che rappresenta la coordinata di trama *s* . Quando viene valutata la mappa vengono generati i comandi [**glTexCoord1**](gltexcoord-functions.md) interni. Tuttavia, le coordinate di trama correnti non vengono aggiornate con il valore di questi comandi di **glTexCoord** .<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**\_ \_ Coord trama GL \_ map2 \_ 2**</dt> </dl> | Ogni punto di controllo è costituito da due valori a virgola mobile che rappresentano le coordinate di trama *s* e *t* . Quando viene valutata la mappa vengono generati i comandi [**glTexCoord2**](gltexcoord-functions.md) interni. Tuttavia, le coordinate di trama correnti non vengono aggiornate con il valore di questi comandi di **glTexCoord** .<br/>         |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**\_Trama GL \_ map2 \_ Coord \_ 3**</dt> </dl> | Ogni punto di controllo è costituito da tre valori a virgola mobile che rappresentano le coordinate di trama *s, t* e *r* . Quando viene valutata la mappa vengono generati i comandi [**glTexCoord3**](gltexcoord-functions.md) interni. Tuttavia, le coordinate di trama correnti non vengono aggiornate con il valore di questi comandi di **glTexCoord** .<br/>   |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**\_Trama GL \_ map2 \_ Coord \_ 4**</dt> </dl> | Ogni punto di controllo è costituito da quattro valori a virgola mobile che rappresentano le coordinate di trama *s, t, r* e *q* . Quando viene valutata la mappa vengono generati i comandi [**glTexCoord4**](gltexcoord-functions.md) interni. Tuttavia, le coordinate di trama correnti non vengono aggiornate con il valore di questi comandi di **glTexCoord** .<br/> |



 

</dd> <dt>

*U1* 
</dt> <dd>

Un mapping lineare di *u*, come presentato a [**glEvalCoord2**](glevalcoord-functions.md), a *u*^, una delle due variabili valutate dalle equazioni specificate da questo comando.

</dd> <dt>

*U2* 
</dt> <dd>

Un mapping lineare di *u*, come presentato a [**glEvalCoord2**](glevalcoord-functions.md), a *u*^, una delle due variabili valutate dalle equazioni specificate da questo comando.

</dd> <dt>

*ustride* 
</dt> <dd>

Numero di valori float o doppi tra l'inizio del punto di controllo **r** *IJ* e l'inizio del punto di controllo **r** <sub>(i \ + 1 \) \ j</sub>, dove *i* e *j* sono rispettivamente gli indici del punto di controllo *u* e *v* . In questo modo è possibile incorporare i punti di controllo in strutture di dati arbitrarie. L'unico vincolo è che i valori per un determinato punto di controllo debbano occupare posizioni di memoria contigue.

</dd> <dt>

*uorder* 
</dt> <dd>

Dimensione della matrice del punto di controllo nell'asse *u*. Deve essere un valore positivo.

</dd> <dt>

*v1* 
</dt> <dd>

Mapping lineare di *v*, come presentato a [**glEvalCoord2**](glevalcoord-functions.md), a *v*^, una delle due variabili valutate dalle equazioni specificate da questo comando.

</dd> <dt>

*v2* 
</dt> <dd>

Mapping lineare di *v*, come presentato a [**glEvalCoord2**](glevalcoord-functions.md), a *v*^, una delle due variabili valutate dalle equazioni specificate da questo comando.

</dd> <dt>

*vstride* 
</dt> <dd>

Numero di valori float o doppi tra l'inizio del punto di controllo **r** *IJ* e l'inizio del punto di controllo **r** <sub>i (j \ + 1 \)</sub>, dove *i* e *j* sono rispettivamente gli indici del punto di controllo *u* e *v* . In questo modo è possibile incorporare i punti di controllo in strutture di dati arbitrarie. L'unico vincolo è che i valori per un determinato punto di controllo debbano occupare posizioni di memoria contigue.

</dd> <dt>

*Vorder* 
</dt> <dd>

Dimensione della matrice del punto di controllo nell'asse *v*. Deve essere un valore positivo.

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
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *U1* era uguale a *U2* oppure *V1* era uguale a *v2*.<br/>                                                                         |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | *Ustride* o *vstride* è inferiore al numero di valori in un punto di controllo.<br/>                                       |
| <dl> <dt>**\_valore GL non valido \_**</dt> </dl>     | Il valore di *uorder* o *Vorder* è minore di uno o di un ordine di valutazione \_ massimo \_ \_ .<br/>                                                     |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Gli analizzatori forniscono un modo per usare il mapping polinomiale o per la logica per produrre vertici, normali, coordinate di trama e colori. I valori prodotti da un analizzatore vengono inviati ad altre fasi dell'elaborazione OpenGL esattamente come se fossero stati presentati usando i comandi [**glVertex**](glvertex-functions.md), [**glNormal**](glnormal-functions.md), [**glTexCoord**](gltexcoord-functions.md)e [**glColor**](glcolor-functions.md) , ad eccezione del fatto che i valori generati non aggiornano la normale, le coordinate di trama o il colore corrente.

Tutte le spline polinomiali o razionali di qualsiasi grado (fino al grado massimo supportato dall'implementazione di OpenGL) possono essere descritte usando gli analizzatori. Sono incluse quasi tutte le superfici utilizzate nella grafica del computer, incluse le superfici della spline B, le superfici NURBS, le superfici di Bezier e così via.

Gli analizzatori definiscono le superfici in base ai polinomi bivariati di Bernstein. Definire **p** (*u*^,*v*^) come

![Equazione che mostra la definizione di p ().](images/map05.png)

dove **R** *IJ* è un punto di controllo, () è il polinomio di *i* TH Bernstein del grado

*n* (*uorder*  =  *n* + 1)

![Equazione che mostra il polinomio di Bernstein del grado n.](images/map06.png)

e () è il polinomio *j* TH Bernstein di Degree *m* (*Vorder*  =  *m* + 1)

![Equazione che mostra il polinomio Bernstein di Degree m.](images/map07.png)

Ricordare che

![Equazioni che mostrano l'equivalenza a 1.](images/map08.png)

La funzione **glMap2** viene usata per definire la base e per specificare il tipo di valori da produrre. Una volta definita, una mappa può essere abilitata e disabilitata chiamando [**glEnable**](glenable.md) e **glDisable** con il nome della mappa, uno dei nove valori predefiniti per *target*, descritti in precedenza. Quando [**glEvalCoord2**](glevalcoord-functions.md) presenta i valori *u* e *v*, i polinomi di bivariate Bernstein vengono valutati usando *u*^ e *v*^, dove

![Equazione che mostra la definizione di ^.](images/map09.png)

e

![Equazione che mostra la definizione di v ^.](images/map10.png)

Il parametro *target* è una costante simbolica che indica il tipo di punti di controllo che viene fornito nei *punti* e l'output generato quando viene valutata la mappa.

I parametri *ustride*, *uorder*, *vstride*, *Vorder* e *Points* definiscono l'indirizzamento della matrice per l'accesso ai punti di controllo. Il parametro *Points* è la posizione del primo punto di controllo, che occupa una, due, tre o quattro posizioni di memoria contigue, a seconda della mappa da definire. Sono presenti punti di controllo *uorder* x *Vorder* nella matrice. Il parametro *ustride* indica il numero di posizioni float o Double ignorate per far avanzare il puntatore di memoria interno dal punto di controllo **r** *IJ* al punto di controllo **r** <sub>(\ i + 1 \) j</sub>. Il parametro *vstride* indica il numero di posizioni float o Double ignorate per far avanzare il puntatore di memoria interno dal punto di controllo **r** *IJ* al punto di controllo **r**<sub>i (j \ + 1 \)</sub>.

Come nel caso di tutti i comandi OpenGL che accettano puntatori ai dati, è come se il contenuto dei *punti* venisse copiato da **glMap2** prima della restituzione. Le modifiche apportate al contenuto dei *punti* non hanno effetto dopo la chiamata a **glMap2** .

Le funzioni seguenti consentono di recuperare informazioni correlate a **glMap2**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Max \_ eval \_ Order

[**glGetMap**](glgetmap.md)

[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Vertex \_ 3

**glIsEnabled** con argomento GL \_ map2 \_ Vertex \_ 4

**glIsEnabled** con argomento GL \_ map2 \_ index

**glIsEnabled** con argomento GL \_ map2 \_ Color \_ 4

**glIsEnabled** con argomento GL \_ map2 \_ Normal

**glIsEnabled** con argomento GL \_ map2 \_ trama \_ Coord \_ 1

**glIsEnabled** con argomento GL \_ map2 \_ trama \_ Coord \_ 2

**glIsEnabled** con argomento GL \_ map2 \_ trama \_ Coord \_ 3

**glIsEnabled** con argomento GL \_ map2 \_ trama \_ Coord \_ 4

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

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMapGrid**](glmapgrid-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

 





