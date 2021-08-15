---
title: Funzione glMap2d (Gl.h)
description: La funzione glMap2d definisce un analizzatore bidimensionale. | Funzione glMap2d (Gl.h)
ms.assetid: d8645d19-bec1-4efd-a657-6e7d52d706a9
keywords:
- Funzione glMap2d OpenGL
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
ms.openlocfilehash: c86699f3d1a897476b33d15aec857228c6293d9bd66e260528cdaf468d664252
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359044"
---
# <a name="glmap2d-function"></a>Funzione glMap2d

Le **funzioni glMap2d** [**e glMap2f**](glmap2f.md) definiscono un analizzatore bidimensionale.

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

Tipo di valori generati dall'analizzatore. Vengono accettate le costanti simboliche seguenti.



| Valore                                                                                                                                                                                          | Significato                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**VERTICE \_ GL MAP2 \_ \_ 3**</dt> </dl>                       | Ogni punto di controllo è rappresentato da tre valori a virgola mobile che rappresentano *x, y* e *z*. I [**comandi interni glVertex3**](glvertex-functions.md) vengono generati quando viene valutata la mappa.<br/>                                                                                                                                         |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**VERTICE \_ GL MAP2 \_ \_ 4**</dt> </dl>                       | Ogni punto di controllo è formato da quattro valori a virgola mobile che rappresentano *x, y, z* e *w*. I [**comandi interni glVertex4**](glvertex-functions.md) vengono generati quando viene valutata la mappa.<br/>                                                                                                                                       |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**INDICE \_ GL MAP2 \_**</dt> </dl>                                 | Ogni punto di controllo è un singolo valore a virgola mobile che rappresenta un indice colori. I [**comandi glIndex**](glindex-functions.md) interni vengono generati quando viene valutata la mappa. L'indice corrente non viene tuttavia aggiornato con il valore di **questi comandi glIndex.**<br/>                                                    |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**GL \_ MAP2 \_ COLOR \_ 4**</dt> </dl>                          | Ogni punto di controllo è rappresentato da quattro valori a virgola mobile che rappresentano rosso, verde, blu e alfa. I [**comandi glColor4**](glcolor-functions.md) interni vengono generati quando viene valutata la mappa. Il colore corrente non viene tuttavia aggiornato con il valore di **questi comandi glColor4.**<br/>                                       |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**GL \_ MAP2 \_ NORMAL**</dt> </dl>                              | Ogni punto di controllo è rappresentato da tre valori a virgola mobile che rappresentano i *componenti x, y* *e z* di un vettore normale. I [**comandi glNormal**](glnormal-functions.md) interni vengono generati quando viene valutata la mappa. La normale corrente non viene tuttavia aggiornata con il valore di **questi comandi glNormal.**<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 1**</dt> </dl> | Ogni punto di controllo è un singolo valore a virgola mobile che rappresenta la *coordinata della* trama. I [**comandi interni glTexCoord1**](gltexcoord-functions.md) vengono generati quando viene valutata la mappa. Le coordinate di trama correnti non vengono tuttavia aggiornate con il valore di **questi comandi glTexCoord.**<br/>              |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2**</dt> </dl> | Ogni punto di controllo è rappresentato da due valori a virgola mobile che rappresentano le *coordinate della* trama s *e t.* I [**comandi interni glTexCoord2**](gltexcoord-functions.md) vengono generati quando viene valutata la mappa. Le coordinate di trama correnti non vengono tuttavia aggiornate con il valore di **questi comandi glTexCoord.**<br/>         |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3**</dt> </dl> | Ogni punto di controllo è rappresentato da tre valori a virgola mobile che rappresentano le coordinate della trama *s, t* e *r.* I [**comandi interni glTexCoord3**](gltexcoord-functions.md) vengono generati quando viene valutata la mappa. Le coordinate di trama correnti non vengono tuttavia aggiornate con il valore di **questi comandi glTexCoord.**<br/>   |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**GL \_ MAP2 \_ TEXTURE \_ COORD \_ 4**</dt> </dl> | Ogni punto di controllo è formato da quattro valori a virgola mobile che rappresentano le coordinate della trama *s, t, r* e *q.* I [**comandi interni glTexCoord4**](gltexcoord-functions.md) vengono generati quando viene valutata la mappa. Le coordinate di trama correnti non vengono tuttavia aggiornate con il valore di **questi comandi glTexCoord.**<br/> |



 

</dd> <dt>

*u1* 
</dt> <dd>

Mapping lineare di *u*, come presentato a [**glEvalCoord2,**](glevalcoord-functions.md)a *u*^, una delle due variabili valutate dalle equazioni specificate da questo comando.

</dd> <dt>

*u2* 
</dt> <dd>

Mapping lineare di *u*, come presentato a [**glEvalCoord2,**](glevalcoord-functions.md)a *u*^, una delle due variabili valutate dalle equazioni specificate da questo comando.

</dd> <dt>

*ustride* 
</dt> <dd>

Numero di valori float o double tra l'inizio del punto di controllo **R** *ij* e l'inizio del punto di controllo **R** <sub>(i\ +1\ )\ j</sub>, dove *i* e *j* sono rispettivamente gli indici dei punti di controllo *u* e *v.* In questo modo i punti di controllo possono essere incorporati in strutture di dati arbitrarie. L'unico vincolo è che i valori per un determinato punto di controllo devono occupare posizioni di memoria contigue.

</dd> <dt>

*uorder* 
</dt> <dd>

Dimensione della matrice di punti di controllo nell'asse *u.* Deve essere positivo.

</dd> <dt>

*v1* 
</dt> <dd>

Mapping lineare di *v*, presentato a [**glEvalCoord2,**](glevalcoord-functions.md)a *v*^, una delle due variabili valutate dalle equazioni specificate da questo comando.

</dd> <dt>

*v2* 
</dt> <dd>

Mapping lineare di *v*, presentato a [**glEvalCoord2,**](glevalcoord-functions.md)a *v*^, una delle due variabili valutate dalle equazioni specificate da questo comando.

</dd> <dt>

*vstride* 
</dt> <dd>

Numero di valori float o double tra l'inizio del punto di controllo **R** *ij* e l'inizio del punto di controllo **R** <sub>i(j\ +1\ )</sub>, dove *i* e *j* sono rispettivamente gli indici dei punti di controllo *u* e *v.* In questo modo i punti di controllo possono essere incorporati in strutture di dati arbitrarie. L'unico vincolo è che i valori per un determinato punto di controllo devono occupare posizioni di memoria contigue.

</dd> <dt>

*vorder* 
</dt> <dd>

Dimensione della matrice di punti di controllo nell'asse *v.* Deve essere positivo.

</dd> <dt>

*punti* 
</dt> <dd>

Puntatore alla matrice di punti di controllo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *target* non è un valore accettato.<br/>                                                                                        |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *u1* è uguale a *u2* o *v1* è uguale a *v2.*<br/>                                                                         |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *Ustride* o *vstride* è minore del numero di valori in un punto di controllo.<br/>                                       |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | Uorder *o* *vorder* è minore di uno o GL \_ MAX \_ EVAL \_ ORDER.<br/>                                                     |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Gli analizzatori consentono di usare il mapping polinomiale o polinomiale razionale per produrre vertici, normali, coordinate della trama e colori. I valori prodotti da un analizzatore vengono inviati ad altre fasi dell'elaborazione OpenGL esattamente come se fossero stati presentati usando i comandi [**glVertex**](glvertex-functions.md), [**glNormal**](glnormal-functions.md), [**glTexCoord**](gltexcoord-functions.md)e [**glColor,**](glcolor-functions.md) ad eccezione del fatto che i valori generati non aggiornano le normali coordinate correnti, le coordinate della trama o il colore.

Tutte le spline polinomiali o razionali polinomiali di qualsiasi grado (fino al grado massimo supportato dall'implementazione OpenGL) possono essere descritte usando gli analizzatori. Queste includono quasi tutte le superfici usate nella grafica computer, incluse le superfici B-spline, le superfici NURBS, le superfici di Bézier e così via.

Gli analizzatori definiscono le superfici in base ai polinomi bivariati di Bernstein. Definire **p** (*u*^,*v*^) come

![Equazione che mostra la definizione di p ().](images/map05.png)

dove **R** *ij* è un punto di controllo, () è *il polinomio i* th Bernstein di grado

*n* (*uorder*  =  *n* + 1)

![Equazione che mostra il polinomio di Bernstein di grado n.](images/map06.png)

e () è il polinomio *j* th Bernstein di grado *m* (*vorder*  =  *m* + 1)

![Equazione che mostra il polinomio di Bernstein di grado m.](images/map07.png)

Tenere a ricordare che

![Equazioni che mostrano l'equivalenza a 1.](images/map08.png)

La **funzione glMap2** viene usata per definire la base e specificare il tipo di valori prodotti. Una volta definita, una mappa può essere abilitata e disabilitata chiamando [**glEnable**](glenable.md) e **glDisable** con il nome della mappa, uno dei nove valori predefiniti per *target*, descritto in precedenza. Quando [**glEvalCoord2**](glevalcoord-functions.md) presenta i valori *u* e *v*, i polinomi bivariati di Bernstein vengono valutati usando *u*^ *e v*^, dove

![Equazione che mostra la definizione dell'utente^.](images/map09.png)

e

![Equazione che mostra la definizione di v^.](images/map10.png)

Il *parametro* di destinazione è una costante simbolica che indica il tipo di punti di controllo specificati *in* punti e l'output generato quando viene valutata la mappa.

I *parametri ustride*, *uorder*, *vstride*, *vorder* e *points* definiscono l'indirizzamento della matrice per l'accesso ai punti di controllo. Il *parametro points* è la posizione del primo punto di controllo, che occupa una, due, tre o quattro posizioni di memoria contigue, a seconda della mappa definita. Nella matrice sono presenti punti di controllo *uorder* x *vorder.* Il *parametro ustride* indica quante posizioni float o double vengono ignorate per far avanzare il puntatore di memoria interna dal punto **di** controllo R *ij* al punto di controllo **R** <sub>(\ i+1\ )j</sub>. Il *parametro vstride* indica quante posizioni float o double vengono ignorate per far avanzare il puntatore di memoria interno dal punto **di** controllo R *ij* al punto di controllo **R**<sub>i(j\ +1\ )</sub>.

Come nel caso di tutti i comandi OpenGL che accettano puntatori ai dati, è come se il contenuto dei punti fosse stato copiato da **glMap2** prima che venga restituito.  Le modifiche al contenuto dei *punti non* hanno alcun effetto dopo la chiamata **a glMap2.**

Le funzioni seguenti recuperano informazioni correlate a **glMap2:**

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ MAX \_ EVAL \_ ORDER

[**glGetMap**](glgetmap.md)

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP2 \_ VERTEX \_ 3

**glIsEnabled con** argomento GL \_ MAP2 \_ VERTEX \_ 4

**glIsEnabled con** argomento GL \_ MAP2 \_ INDEX

**glIsEnabled con** argomento GL \_ MAP2 \_ COLOR \_ 4

**glIsEnabled con** argomento GL \_ MAP2 \_ NORMAL

**glIsEnabled con** argomento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 1

**glIsEnabled con** argomento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2

**glIsEnabled con** argomento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3

**glIsEnabled con** argomento GL \_ MAP2 \_ TEXTURE \_ COORD \_ 4

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
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

 

 





