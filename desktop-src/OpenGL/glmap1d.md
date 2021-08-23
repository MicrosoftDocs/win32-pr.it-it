---
title: Funzione glMap1d (Gl.h)
description: La funzione glMap1d definisce un analizzatore unidimensionale. | Funzione glMap1d (Gl.h)
ms.assetid: 65f8b099-597c-4300-a7d1-3dabdd19e6cb
keywords:
- Funzione glMap1d OpenGL
topic_type:
- apiref
api_name:
- glMap1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90f1d17312cae14da955641d0009235a45fa23e65a3a04e35f692a4bb5418722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520431"
---
# <a name="glmap1d-function"></a>Funzione glMap1d

Le **funzioni glMap1d** [**e glMap1f**](glmap1f.md) definiscono un analizzatore unidimensionale.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glMap1d(
         GLenum   target,
         GLdouble u1,
         GLdouble u2,
         GLint    stride,
         GLint    order,
   const GLdouble *points
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*target* 
</dt> <dd>

Tipo di valori generati dall'analizzatore. Costanti simboliche. Il *parametro* di destinazione è una costante simbolica che indica il tipo di punti di controllo specificati *in* punti e l'output generato quando viene valutata la mappa. Può presupporre uno dei nove valori predefiniti.



| Valore                                                                                                                                                                                          | Significato                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**VERTICE \_ \_ 3 GL MAP1 \_**</dt> </dl>                       | Ogni punto di controllo è rappresentato da tre valori a virgola mobile che rappresentano *x, y* e *z*. I [**comandi interni glVertex3**](glvertex-functions.md) vengono generati quando viene valutata la mappa.<br/>                                                                                                                                         |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**VERTICE \_ \_ 4 GL MAP1 \_**</dt> </dl>                       | Ogni punto di controllo è formato da quattro valori a virgola mobile che rappresentano *x, y, z* e *w*. I [**comandi interni glVertex4**](glvertex-functions.md) vengono generati quando viene valutata la mappa.<br/>                                                                                                                                       |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**INDICE \_ GL MAP1 \_**</dt> </dl>                                 | Ogni punto di controllo è un singolo valore a virgola mobile che rappresenta un indice colori. I [**comandi glIndex**](glindex-functions.md) interni vengono generati quando viene valutata la mappa. Tuttavia, l'indice corrente non viene aggiornato con il valore di questi **comandi glIndex.**<br/>                                                    |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**GL \_ MAP1 \_ COLOR \_ 4**</dt> </dl>                          | Ogni punto di controllo è rappresentato da quattro valori a virgola mobile che rappresentano rosso, verde, blu e alfa. I [**comandi glColor4**](glcolor-functions.md) interni vengono generati quando viene valutata la mappa. Tuttavia, il colore corrente non viene aggiornato con il valore di **questi comandi glColor4.**<br/>                                       |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**GL \_ MAP1 \_ NORMAL**</dt> </dl>                              | Ogni punto di controllo è rappresentato da tre valori a virgola mobile che rappresentano i *componenti x, y* *e z* di un vettore normale. I [**comandi glNormal**](glnormal-functions.md) interni vengono generati quando viene valutata la mappa. Tuttavia, la normale corrente non viene aggiornata con il valore di **questi comandi glNormal.**<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1**</dt> </dl> | Ogni punto di controllo è un singolo valore a virgola mobile che rappresenta la *coordinata della* trama. I [**comandi interni glTexCoord1**](gltexcoord-functions.md) vengono generati quando viene valutata la mappa. Tuttavia, le coordinate di trama correnti non vengono aggiornate con il valore di **questi comandi glTexCoord.**<br/>              |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2**</dt> </dl> | Ogni punto di controllo è rappresentato da due valori a virgola mobile che rappresentano le *coordinate della* trama s *e t.* I [**comandi interni glTexCoord2**](gltexcoord-functions.md) vengono generati quando viene valutata la mappa. Tuttavia, le coordinate di trama correnti non vengono aggiornate con il valore di **questi comandi glTexCoord.**<br/>         |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3**</dt> </dl> | Ogni punto di controllo è rappresentato da tre valori a virgola mobile che rappresentano le coordinate della trama *s, t* e *r.* I [**comandi interni glTexCoord3**](gltexcoord-functions.md) vengono generati quando viene valutata la mappa. Tuttavia, le coordinate di trama correnti non vengono aggiornate con il valore di **questi comandi glTexCoord.**<br/>   |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4**</dt> </dl> | Ogni punto di controllo è formato da quattro valori a virgola mobile che rappresentano le coordinate della trama *s, t, r* e *q.* I [**comandi interni glTexCoord4**](gltexcoord-functions.md) vengono generati quando viene valutata la mappa. Tuttavia, le coordinate di trama correnti non vengono aggiornate con il valore di **questi comandi glTexCoord.**<br/> |



 

</dd> <dt>

*u1* 
</dt> <dd>

Mapping lineare di *u*, come presentato a [**glEvalCoord1,**](glevalcoord-functions.md)a *u*^, variabile valutata dalle equazioni specificate da questo comando.

</dd> <dt>

*u2* 
</dt> <dd>

Mapping lineare di *u*, come presentato a [**glEvalCoord1,**](glevalcoord-functions.md)a *u*^, variabile valutata dalle equazioni specificate da questo comando.

</dd> <dt>

*Passo* 
</dt> <dd>

Numero di valori float o double tra l'inizio di un punto di controllo e l'inizio del successivo nella struttura dei dati a cui si fa riferimento in *punti*. In questo modo i punti di controllo possono essere incorporati in strutture di dati arbitrarie. L'unico vincolo è che i valori per un determinato punto di controllo devono occupare posizioni di memoria contigue.

</dd> <dt>

*order* 
</dt> <dd>

Numero di punti di controllo. Deve essere positivo.

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
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *u1* è uguale a *u2*.<br/>                                                                                                    |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *stride* è minore del numero di valori in un punto di controllo.<br/>                                                            |
| <dl> <dt>**VALORE GL \_ NON \_ VALIDO**</dt> </dl>     | *order* è minore di uno o GL \_ MAX \_ EVAL \_ ORDER.<br/>                                                                         |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Gli analizzatori consentono di usare il mapping polinomiale o polinomiale razionale per produrre vertici, normali, coordinate della trama e colori. I valori prodotti da un analizzatore vengono inviati ad altre fasi dell'elaborazione OpenGL come se fossero stati presentati usando i comandi [**glVertex**](glvertex-functions.md), [**glNormal**](glnormal-functions.md), [**glTexCoord**](gltexcoord-functions.md)e [**glColor,**](glcolor-functions.md) ad eccezione del fatto che i valori generati non aggiornano le coordinate normali correnti, le coordinate della trama o il colore.

Tutte le spline polinomiali o razionali polinomiali di qualsiasi grado (fino al grado massimo supportato dall'implementazione OpenGL) possono essere descritte usando gli analizzatori. Queste includono quasi tutte le spline usate nella grafica computer, tra cui B-spline, curve di Bézier, spline hermite e così via.

Gli analizzatori definiscono le curve in base ai polinomi di Bernstein. Definire **p** () come

![Equazione che mostra la definizione di p ().](images/map01.png)

dove **R**_i_ è un punto di controllo e () è *il polinomio di* Bernstein di grado *n* (*order*  = *n* + 1):

![Equazione che mostra il polinomio di Bernstein di grado n.](images/map02.png)

Tenere a ricordare che

![Equazioni che mostrano l'equivalenza a 1.](images/map03.png)

La **funzione glMap1** viene usata per definire la base e specificare il tipo di valori prodotti. Una volta definita, una mappa può essere abilitata e disabilitata chiamando [**glEnable**](glenable.md) e **glDisable** con il nome della mappa, uno dei nove valori predefiniti per *la* destinazione descritta in precedenza. La [funzione glEvalCoord1](glevalcoord-functions.md) valuta le mappe unidimensionali abilitate. Quando **glEvalCoord1** presenta un valore *u*, le funzioni Bernstein vengono valutate usando *u*^, dove

![Equazione che mostra la definizione dell'utente^.](images/map04.png)

I *parametri stride,* *order* e *points* definiscono l'indirizzamento della matrice per l'accesso ai punti di controllo. Il *parametro points* è la posizione del primo punto di controllo, che occupa una, due, tre o quattro posizioni di memoria contigue, a seconda della mappa definita. Il *parametro order* è il numero di punti di controllo nella matrice. Il *parametro stride* indica quante posizioni float o double far avanzare il puntatore di memoria interno per raggiungere il punto di controllo successivo.

Come nel caso di tutti i comandi OpenGL che accettano puntatori ai dati, è come se il contenuto dei punti fosse stato copiato da **glMap1** prima che fosse restituito.  Le modifiche al contenuto dei *punti non* hanno effetto dopo la chiamata **di glMap1.**

Le funzioni seguenti recuperano informazioni correlate **a glMap1:**

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MAX \_ EVAL \_ ORDER

[**glGetMap**](glgetmap.md)

[**glIsEnabled con**](glisenabled.md) argomento GL \_ MAP1 \_ VERTEX \_ 3

**glIsEnabled con** argomento GL \_ MAP1 \_ VERTEX \_ 4

**glIsEnabled con** argomento GL \_ MAP1 \_ INDEX

**glIsEnabled con** argomento GL \_ MAP1 \_ COLOR \_ 4

**glIsEnabled con** argomento GL \_ MAP1 \_ NORMAL

**glIsEnabled con** argomento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1

**glIsEnabled con** argomento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2

**glIsEnabled con** argomento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3

**glIsEnabled con** argomento GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4

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

 

 





