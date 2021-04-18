---
title: funzione glDisable (GL. h)
description: Le funzioni glEnable e glDisable abilitano o disabilitano le funzionalità di OpenGL. | funzione glDisable (GL. h)
ms.assetid: 094f730e-5e2b-485e-8d9d-fee2902d3d5f
keywords:
- funzione glDisable OpenGL
topic_type:
- apiref
api_name:
- glDisable
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eff5c12e53eb060777f75ad537bed265401a7a26
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321854"
---
# <a name="gldisable-function"></a>glDisable (funzione)

Le funzioni [**glEnable**](glenable.md) e **glDisable** abilitano o disabilitano le funzionalità di OpenGL.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glDisable(
   GLenum cap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*limite* 
</dt> <dd>

Costante simbolica che indica una funzionalità OpenGL.

Per informazioni sui valori che possono essere accettati da *Cap* , vedere la sezione Osservazioni riportata di seguito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumerazione GL non valida \_**</dt> </dl>      | *Cap* non è uno dei valori elencati nella sezione Osservazioni precedente.<br/>                                                   |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Le funzioni [**glEnable**](glenable.md) e **glDisable** abilitano e disabilitano diverse funzionalità grafiche OpenGL. Usare [**glIsEnabled**](glisenabled.md) o [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) per determinare l'impostazione corrente di tutte le funzionalità.

Sia [**glEnable**](glenable.md) che **glDisable** accettano un solo argomento, *Cap*, che può assumere uno dei valori seguenti:



| Valore                       | Significato                                                                                                                                                                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_test GL Alpha \_             | Se abilitata, eseguire il test alfa. Vedere [**glAlphaFunc**](glalphafunc.md).                                                                                                                                                                                       |
| GL \_ auto \_ normale            | Se abilitata, calcola i vettori normali della superficie di calcolo in modo analitico quando i \_ vertici di GL map2 \_ Vertex \_ 3 o GL \_ map2 \_ sono stati \_ generati. Vedere [**glMap2**](glmap2.md).                                                                                        |
| \_Blend GL                   | Se abilitata, combina i valori dei colori RGBA in ingresso con i valori nei buffer dei colori. Vedere [**glBlendFunc**](glblendfunc.md).                                                                                                                              |
| \_Piano di ritaglio GL \_ *i*          | Se abilitata, ritagliare la geometria rispetto *al piano di* ritaglio definito dall'utente. Vedere [**glClipPlane**](glclipplane.md).                                                                                                                                                  |
| \_operazione di \_ logica \_ colori GL        | Se abilitata, applicare l'operazione logica corrente ai valori del buffer dei colori e del colore RGBA in ingresso. Vedere [**glLogicOp**](gllogicop.md).                                                                                                                     |
| \_materiale colore \_ GL         | Se abilitata, avere uno o più parametri Material tenere traccia del colore corrente. Vedere [**glColorMaterial**](glcolormaterial.md).                                                                                                                                   |
| superficie di selezione GL \_ \_              | Se abilitata, i poligoni vengono raccolti in base al relativo avvolgimento nelle coordinate della finestra. Vedere [**glCullFace**](glcullface.md).                                                                                                                                               |
| \_test di profondità GL \_             | Se abilitata, eseguire confronti di profondità e aggiornare il buffer di profondità. Vedere [**glDepthFunc**](gldepthfunc.md) e [**glDepthRange**](gldepthrange.md).                                                                                                              |
| \_dithering GL                  | Se abilitata, i componenti di colore o gli indici di dithering prima che vengano scritti nel buffer dei colori.                                                                                                                                                                 |
| \_nebbia GL                     | Se abilitata, fondere un colore di nebbia al colore di post-texturing. Vedere [**glFog**](glfog.md).                                                                                                                                                                    |
| \_ \_ operazione logica indice \_ GL        | Se abilitata, applicare l'operazione logica corrente agli indici indici in ingresso e al buffer dei colori. Vedere [**glLogicOp**](gllogicop.md).                                                                                                                         |
| GL \_ Light *i*                | Se abilitata, includere la luce *i* nella valutazione dell'equazione di illuminazione. Vedere [**glLightModel**](gllightmodel-functions.md) e [**glLight**](gllight-functions.md).                                                                                      |
| \_illuminazione GL                | Se abilitata, usare i parametri di illuminazione correnti per calcolare il colore o l'indice del vertice. Se disabilitato, associare il colore o l'indice corrente a ogni vertice. Vedere [**glMaterial**](glmaterial-functions.md), **glLightModel** e **glLight**.                |
| \_linea GL \_ smussata            | Se abilitata, creare linee con filtri corretti. Se è disabilitata, creare linee con alias. Vedere [**glLineWidth**](gllinewidth.md).                                                                                                                                     |
| \_stipple linea \_ GL           | Se abilitata, usare il modello stipple di riga corrente quando si disegnano le linee. Vedere [**glLineStipple**](gllinestipple.md).                                                                                                                                            |
| \_op logica \_ GL               | Se abilitata, applicare l'operazione logica attualmente selezionata agli indici del buffer di colore e in ingresso. Vedere [**glLogicOp**](gllogicop.md).                                                                                                                    |
| \_Mappa1 \_ colore \_ 4 GL          | Se abilitata, le chiamate a [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano valori RGBA. Vedere anche [**glMap1**](glmap1.md).                                           |
| \_Indice MAPPA1 \_ GL             | Se abilitata, le chiamate a **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** generano indici colori. Vedere anche **glMap1**.                                                                                                                                   |
| \_Normale MAPPA1 \_ GL            | Se abilitata, le chiamate a [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano normali. Vedere anche [**glMap1**](glmap1.md).                                               |
| \_Trama GL \_ Mappa1 \_ Coord \_ 1 | Se abilitata, le chiamate a **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** generano le coordinate di trama *s* . Vedere anche **glMap1**.                                                                                                                         |
| \_ \_ Coord trama GL \_ Mappa1 \_ 2 | Se abilitata, le chiamate a [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano le coordinate di trama *s* e *t* . Vedere anche [**glMap1**](glmap1.md).                       |
| \_Trama GL \_ Mappa1 \_ Coord \_ 3 | Se abilitata, le chiamate a **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** generano le coordinate di trama *s*, *t* e *r* . Vedere anche **glMap1**.                                                                                                           |
| \_Trama GL \_ Mappa1 \_ Coord \_ 4 | Se abilitata, le chiamate a [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano le coordinate di trama *s*, *t*, *r* e *q* . Vedere anche [**glMap1**](glmap1.md).                    |
| \_Vertice GL \_ Mappa1 \_ 3         | Se abilitata, le chiamate a **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** generano coordinate di vertice *x*, *y* e *z* . Vedere anche **glMap1**.                                                                                                            |
| \_Mappa1 \_ Vertex \_ 4         | Se abilitate, le chiamate a [**glEvalCoord1**](glevalcoord-functions.md), [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano coordinate di vertice *x*, *y*, *z* e *w* omogenee. Vedere anche [**glMap1**](glmap1.md). |
| \_Map2 \_ colore \_ 4 GL          | Se abilitata, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano valori RGBA. Vedere anche [**glMap2**](glmap2.md).                                           |
| \_Indice map2 \_ GL             | Se abilitata, le chiamate a **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** generano indici colori. Vedere anche **glMap2**.                                                                                                                                   |
| \_Normale map2 \_ GL            | Se abilitata, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano normali. Vedere anche [**glMap2**](glmap2.md).                                               |
| \_Trama GL \_ map2 \_ Coord \_ 1 | Se abilitata, le chiamate a **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** generano le coordinate di trama *s* . Vedere anche **glMap2**.                                                                                                                         |
| \_ \_ Coord trama GL \_ map2 \_ 2 | Se abilitata, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano le coordinate di trama *s* e *t* . Vedere anche [**glMap2**](glmap2.md).                       |
| \_Trama GL \_ map2 \_ Coord \_ 3 | Se abilitata, le chiamate a **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** generano le coordinate di trama *s*, *t* e *r* . Vedere anche **glMap2**.                                                                                                           |
| \_Trama GL \_ map2 \_ Coord \_ 4 | Se abilitata, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano le coordinate di trama *s*, *t*, *r* e *q* . Vedere anche [**glMap2**](glmap2.md).            |
| \_Vertice GL \_ map2 \_ 3         | Se abilitata, le chiamate a **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** generano coordinate di vertice *x*, *y* e *z* . Vedere anche **glMap2**.                                                                                                            |
| \_Map2 \_ Vertex \_ 4         | Se abilitate, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano coordinate di vertice *x*, *y*, *z* e *w* omogenee. Vedere anche [**glMap2**](glmap2.md). |
| \_normalizzare GL               | Se abilitata, i vettori normali specificati con **glNormal** vengono ridimensionati alla lunghezza dell'unità dopo la trasformazione. Vedere [**glNormal**](glnormal-functions.md).                                                                                                          |
| \_punto GL \_ smussato           | Se abilitata, creare punti con filtro appropriato. Se disabilitato, creare punti con alias. Vedere [**glPointSize**](glpointsize.md).                                                                                                                                    |
| \_riempimento offset poligono GL \_ \_   | Se abilitata e se viene eseguito il rendering del poligono in \_ modalità di riempimento GL, viene aggiunto un offset ai valori di profondità dei frammenti di un poligono prima che venga eseguito il confronto di profondità. Vedere [**glPolygonOffset**](glpolygonoffset.md)**.**                                      |
| \_linea offset poligono GL \_ \_   | Se abilitata e se viene eseguito il rendering del poligono in \_ modalità linea GL, viene aggiunto un offset ai valori di profondità dei frammenti di un poligono prima che venga eseguito il confronto di profondità. Vedere **glPolygonOffset**.                                                                 |
| \_punto di offset del poligono GL \_ \_  | Se abilitata, viene aggiunto un offset ai valori di profondità dei frammenti di un poligono prima che venga eseguito il confronto di profondità, se il poligono viene sottoposto a rendering in \_ modalità punto GL. Vedere [**glPolygonOffset**](glpolygonoffset.md).                                             |
| \_poligono GL \_ smussato         | Se abilitata, creare poligoni con filtri appropriati. Se disabilitato, creare poligoni con alias. Vedere [**glPolygonMode**](glpolygonmode.md).                                                                                                                            |
| \_stipple poligono GL \_        | Se abilitata, usare il modello stipple del poligono corrente durante il rendering dei poligoni. Vedere [**glPolygonStipple**](glpolygonstipple.md).                                                                                                                              |
| \_test della forbice GL \_           | Se abilitata, eliminare i frammenti esterni al rettangolo a forbice. Vedere [**glScissor**](glscissor.md).                                                                                                                                                   |
| \_test stencil \_ GL           | Se abilitata, eseguire il test dello stencil e aggiornare il buffer dello stencil. Vedere [**glStencilFunc**](glstencilfunc.md) e [**glStencilOp**](glstencilop.md).                                                                                                            |
| \_Trama GL \_ 1D             | Se abilitata, viene eseguita la texturing unidimensionale (a meno che non sia abilitata anche la texturing bidimensionale). Vedere [**glTexImage1D**](glteximage1d.md).                                                                                                            |
| \_Trama GL \_ 2D             | Se abilitata, viene eseguita la texturing bidimensionale. Vedere [**glTexImage2D**](glteximage2d.md).                                                                                                                                                               |
| \_generazione trama \_ GL \_ Q         | Se abilitata, la coordinata di trama *q* viene calcolata usando la funzione di generazione della trama definita con [**glTexGen**](gltexgen-functions.md). In caso contrario, viene utilizzata la coordinata di trama *q* corrente.                                                        |
| \_generazione trama \_ GL \_ R         | Se abilitata, la coordinata di trama *r* viene calcolata usando la funzione di generazione della trama definita con [**glTexGen**](gltexgen-functions.md). Se è disabilitata, viene utilizzata la coordinata di trama *r* corrente.                                                      |
| \_generazione trama \_ GL \_         | Se abilitata, la coordinata di trama *s* viene calcolata usando la funzione di generazione della trama definita con **glTexGen**. Se è disabilitata, viene utilizzata la coordinata *di trama corrente* .                                                                                |
| \_gen trama \_ GL \_ T         | Se abilitata, la coordinata di trama *t* viene calcolata usando la funzione di generazione della trama definita con [**glTexGen**](gltexgen-functions.md). Se è disabilitata, viene utilizzata la coordinata di trama *t* corrente.                                                      |



 

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

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glArrayElement**](glarrayelement.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glClipPlane**](glclipplane.md)
</dt> <dt>

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glColorPointer**](glcolorpointer.md)
</dt> <dt>

[**glCullFace**](glcullface.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glDepthRange**](gldepthrange.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**Remo**](glend.md)
</dt> <dt>

[**glEvalCoord1**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalMesh1**](glevalmesh-functions.md)
</dt> <dt>

[**glEvalPoint1**](glevalpoint.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndexPointer**](glindexpointer.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glNormalPointer**](glnormalpointer.md)
</dt> <dt>

[**glPointSize**](glpointsize.md)
</dt> <dt>

[**glPolygonMode**](glpolygonmode.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> <dt>

[**glTexCoordPointer**](gltexcoordpointer.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





