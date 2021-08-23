---
title: Funzione glEnable (Gl.h)
description: Le funzioni glEnable e glDisable abilitano o disabilitano le funzionalità OpenGL. | Funzione glEnable (Gl.h)
ms.assetid: cd4590dd-ae41-47c9-9861-10d72318840f
keywords:
- Funzione glEnable OpenGL
topic_type:
- apiref
api_name:
- glEnable
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4ef13323f72efd516a0c5321cb410885904ac5245b5198b21ea9e4a4b29f3c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625631"
---
# <a name="glenable-function"></a>Funzione glEnable

Le **funzioni glEnable** [**e glDisable**](gldisable.md) abilitano o disabilitano le funzionalità OpenGL.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glEnable(
   GLenum cap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Cap* 
</dt> <dd>

Costante simbolica che indica una funzionalità OpenGL.

Per informazioni sui valori *che possono essere* accettati, vedere la sezione Osservazioni seguente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERAZIONE GL \_ NON \_ VALIDA**</dt> </dl>      | *cap* non è uno dei valori elencati nella sezione Osservazioni precedente.<br/>                                                   |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

Le **funzioni glEnable** **e glDisable** abilitano e disabilitano varie funzionalità grafiche OpenGL. Usare [**glIsEnabled**](glisenabled.md) o [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) per determinare l'impostazione corrente di qualsiasi funzionalità.

Sia **glEnable che** **glDisable** accettano un solo argomento, *cap*, che può assumere uno dei valori seguenti:



| Valore                       | Significato                                                                                                                                                                                                                                                     |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TEST \_ ALFA GL \_             | Se abilitata, eseguire il test alfa. Vedere [**glAlphaFunc**](glalphafunc.md).                                                                                                                                                                                       |
| GL \_ AUTO \_ NORMAL            | Se abilitata, i vettori normali della superficie di calcolo vengono calcolati in modo analitico quando GL \_ MAP2 \_ VERTEX 3 o \_ GL \_ MAP2 \_ VERTEX \_ 4 ha generato vertici. Vedere [**glMap2**](glmap2.md).                                                                                        |
| GL \_ BLEND                   | Se abilitata, unire i valori di colore RGBA in ingresso con i valori nei buffer dei colori. Vedere [**glBlendFunc**](glblendfunc.md).                                                                                                                              |
| GL \_ CLIP \_ PLANE *i*          | Se abilitata, ritagliare la geometria rispetto al piano di ritaglio definito *dall'utente i*. Vedere [**glClipPlane**](glclipplane.md).                                                                                                                                                  |
| GL \_ COLOR \_ LOGIC \_ OP        | Se abilitata, applicare l'operazione logica corrente ai valori del buffer dei colori e dei colori RGBA in ingresso. Vedere [**glLogicOp**](gllogicop.md).                                                                                                                     |
| MATERIALE COLORE GL \_ \_         | Se abilitata, fare in modo che uno o più parametri di materiale monitorino il colore corrente. Vedere [**glColorMaterial**](glcolormaterial.md).                                                                                                                                   |
| VISO \_ GL CULL \_              | Se abilitata, cullare i poligoni in base alla loro avvolgimento nelle coordinate della finestra. Vedere [**glCullFace**](glcullface.md).                                                                                                                                               |
| TEST DI \_ PROFONDITÀ GL \_             | Se abilitata, eseguire confronti di profondità e aggiornare il buffer di profondità. Vedere [**glDepthFunc**](gldepthfunc.md) e [**glDepthRange**](gldepthrange.md).                                                                                                              |
| \_DITHERING GL                  | Se abilitata, eseguire il dithering dei componenti o degli indici dei colori prima che siano scritti nel buffer dei colori.                                                                                                                                                                 |
| GL \_ OSA                     | Se abilitata, sfumare un colore osa nel colore post-texturing. Vedere [**glFog**](glfog.md).                                                                                                                                                                    |
| GL \_ INDEX \_ LOGIC \_ OP        | Se abilitata, applicare l'operazione logica corrente agli indici dell'indice e del buffer dei colori in ingresso. Vedere [**glLogicOp**](gllogicop.md).                                                                                                                         |
| GL \_ LIGHT *i*                | Se abilitata, includere luce *i* nella valutazione dell'equazione di illuminazione. Vedere [**glLightModel**](gllightmodel-functions.md) e [**glLight**](gllight-functions.md).                                                                                      |
| ILLUMINAZIONE \_ GL                | Se abilitata, usare i parametri di illuminazione correnti per calcolare il colore o l'indice dei vertici. Se disabilitato, associare il colore o l'indice corrente a ogni vertice. Vedere [**glMaterial**](glmaterial-functions.md), **glLightModel** e **glLight**.                |
| GL \_ LINE \_ SMOOTH            | Se abilitata, disegnare linee con il filtro corretto. Se disabilitata, disegnare linee con alias. Vedere [**glLineWidth**](gllinewidth.md).                                                                                                                                     |
| GL \_ LINE \_ STIPPLE           | Se abilitata, usare il modello di punta della linea corrente durante il disegno delle linee. Vedere [**glLineStipple**](gllinestipple.md).                                                                                                                                            |
| GL \_ LOGIC \_ OP               | Se abilitata, applicare l'operazione logica attualmente selezionata agli indici in ingresso e buffer dei colori. Vedere [**glLogicOp**](gllogicop.md).                                                                                                                    |
| GL \_ MAP1 \_ COLOR \_ 4          | Se abilitata, le chiamate [**a glEvalCoord1,**](glevalcoord-functions.md) [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano valori RGBA. Vedere anche [**glMap1**](glmap1.md).                                           |
| INDICE \_ GL MAP1 \_             | Se abilitata, le chiamate **a glEvalCoord1,** **glEvalMesh1** e **glEvalPoint1** generano indici dei colori. Vedere anche **glMap1**.                                                                                                                                   |
| GL \_ MAP1 \_ NORMAL            | Se abilitata, le chiamate [**a glEvalCoord1,**](glevalcoord-functions.md) [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano valori normali. Vedere anche [**glMap1**](glmap1.md).                                               |
| GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1 | Se abilitata, le chiamate **a glEvalCoord1,** **glEvalMesh1** e **glEvalPoint1** generano *coordinate di trama.* Vedere anche **glMap1**.                                                                                                                         |
| GL \_ MAP1 \_ TEXTURE \_ COORD \_ 2 | Se abilitata, le chiamate a [**glEvalCoord1,**](glevalcoord-functions.md) [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano *coordinate di* trama s e *t.* Vedere anche [**glMap1**](glmap1.md).                       |
| GL \_ MAP1 \_ TEXTURE \_ COORD \_ 3 | Se abilitata, le chiamate a **glEvalCoord1**, **glEvalMesh1** e **glEvalPoint1** generano le coordinate *di* trama s , *t* e *r.* Vedere anche **glMap1**.                                                                                                           |
| GL \_ MAP1 \_ TEXTURE \_ COORD \_ 4 | Se abilitata, le chiamate a [glEvalCoord1](glevalcoord-functions.md), [glEvalMesh1](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano le coordinate della trama *s*, *t*, *r* *e q.* Vedere anche [**glMap1**](glmap1.md).                    |
| VERTICE \_ \_ 3 GL MAP1 \_         | Se abilitata, le chiamate a **glEvalCoord1,** **glEvalMesh1** e **glEvalPoint1** generano le coordinate dei vertici *x,* *y* e *z.* Vedere anche **glMap1**.                                                                                                            |
| VERTICE \_ \_ 4 GL MAP1 \_         | Se abilitata, le chiamate a [**glEvalCoord1,**](glevalcoord-functions.md) [**glEvalMesh1**](glevalmesh-functions.md)e [**glEvalPoint1**](glevalpoint.md) generano coordinate dei vertici *x,* *y,* *z* *e w* omogenee. Vedere anche [**glMap1**](glmap1.md). |
| GL \_ MAP2 \_ COLOR \_ 4          | Se abilitata, le chiamate [**a glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano valori RGBA. Vedere anche [**glMap2**](glmap2.md).                                           |
| INDICE \_ GL MAP2 \_             | Se abilitata, le chiamate **a glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** generano indici dei colori. Vedere anche **glMap2**.                                                                                                                                   |
| GL \_ MAP2 \_ NORMAL            | Se abilitata, le chiamate [**a glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano valori normali. Vedere anche [**glMap2**](glmap2.md).                                               |
| GL \_ MAP2 \_ TEXTURE \_ COORD \_ 1 | Se abilitata, le chiamate **a glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** generano coordinate di trama *s.* Vedere anche **glMap2**.                                                                                                                         |
| GL \_ MAP2 \_ TEXTURE \_ COORD \_ 2 | Se abilitata, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano *coordinate di* trama s e *t.* Vedere anche [**glMap2**](glmap2.md).                       |
| GL \_ MAP2 \_ TEXTURE \_ COORD \_ 3 | Se abilitata, le chiamate a **glEvalCoord2**, **glEvalMesh2** e **glEvalPoint2** generano le coordinate *di* trama s , *t* e *r.* Vedere anche **glMap2**.                                                                                                           |
| GL \_ MAP2 \_ TEXTURE \_ COORD \_ 4 | Se abilitata, le chiamate a [**glEvalCoord2**](glevalcoord-functions.md), [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano le coordinate della trama *s*, *t*, *r* *e q.* Vedere anche [**glMap2**](glmap2.md).            |
| VERTICE \_ GL MAP2 \_ \_ 3         | Se abilitata, le chiamate a **glEvalCoord2,** **glEvalMesh2** e **glEvalPoint2** generano le coordinate dei vertici *x,* *y* e *z.* Vedere anche **glMap2**.                                                                                                            |
| VERTICE \_ GL MAP2 \_ \_ 4         | Se abilitata, le chiamate a [**glEvalCoord2,**](glevalcoord-functions.md) [**glEvalMesh2**](glevalmesh-functions.md)e [**glEvalPoint2**](glevalpoint.md) generano coordinate dei vertici *x,* *y,* *z* *e w* omogenee. Vedere anche [**glMap2**](glmap2.md). |
| GL \_ NORMALIZE               | Se abilitata, i vettori normali specificati con **glNormal** vengono ridimensionati in base alla lunghezza unità dopo la trasformazione. Vedere [**glNormal**](glnormal-functions.md).                                                                                                          |
| ARROTONDAMENTO DEL PUNTO GL \_ \_           | Se abilitata, disegnare punti con un filtro appropriato. Se disabilitata, disegnare punti con alias. Vedere [**glPointSize**](glpointsize.md).                                                                                                                                    |
| RIEMPIMENTO \_ OFFSET \_ POLIGONO GL \_   | Se abilitata e se il rendering del poligono viene eseguito in modalità GL FILL, viene aggiunto un offset ai valori di profondità dei frammenti di un poligono prima che venga eseguito il confronto \_ della profondità. Vedere [**glPolygonOffset**](glpolygonoffset.md)**.**                                      |
| LINEA DI \_ \_ OFFSET POLIGONO GL \_   | Se abilitata e se il rendering del poligono viene eseguito in modalità GL LINE, viene aggiunto un offset ai valori di profondità dei frammenti di un poligono prima che venga eseguito il confronto \_ della profondità. Vedere **glPolygonOffset**.                                                                 |
| PUNTO DI \_ \_ OFFSET POLIGONO GL \_  | Se abilitata, viene aggiunto un offset ai valori di profondità dei frammenti di un poligono prima che venga eseguito il confronto della profondità, se il rendering del poligono viene eseguito in modalità PUNTO \_ GL. Vedere [**glPolygonOffset**](glpolygonoffset.md).                                             |
| ARROTONDAMENTO \_ POLIGONO GL \_         | Se abilitata, disegnare poligoni con un filtro appropriato. Se disabilitato, disegnare poligoni con alias. Vedere [**glPolygonMode**](glpolygonmode.md).                                                                                                                            |
| \_ \_ STIPPLE POLIGONO GL        | Se abilitata, usare il modello di punta del poligono corrente durante il rendering dei poligoni. Vedere [**glPolygonStipple**](glpolygonstipple.md).                                                                                                                              |
| TEST \_ DI SCISSOR \_ GL           | Se abilitata, rimuovere i frammenti esterni al rettangolo della forbice. Vedere [**glScissor**](glscissor.md).                                                                                                                                                   |
| TEST DI STENCIL GL \_ \_           | Se abilitata, eseguire il test degli stencil e aggiornare il buffer degli stencil. Vedere [**glStencilFunc**](glstencilfunc.md) e [**glStencilOp**](glstencilop.md).                                                                                                            |
| TRAMA \_ GL \_ 1D             | Se abilitata, viene eseguita la texturing unidimensionale (a meno che non sia abilitata anche la texturing bidimensionale). Vedere [**glTexImage1D**](glteximage1d.md).                                                                                                            |
| GL \_ TEXTURE \_ 2D             | Se abilitata, viene eseguita la texturing bidimensionale. Vedere [**glTexImage2D**](glteximage2d.md).                                                                                                                                                               |
| GL \_ TEXTURE \_ GEN \_ Q         | Se abilitata, la coordinata di trama *q* viene calcolata usando la funzione di generazione della trama definita con [**glTexGen**](gltexgen-functions.md). In caso contrario, viene usata la coordinata di trama *q* corrente.                                                        |
| GL \_ TEXTURE \_ GEN \_ R         | Se abilitata, la *coordinata* della trama r viene calcolata usando la funzione di generazione della trama definita con [**glTexGen**](gltexgen-functions.md). Se disabilitata, viene usata la *coordinata* di trama r corrente.                                                      |
| GL \_ TEXTURE \_ GEN \_ S         | Se abilitata, la *coordinata* di trama s viene calcolata usando la funzione di generazione della trama definita con **glTexGen**. Se disabilitata, viene usata *la* coordinata di trama corrente.                                                                                |
| GL \_ TEXTURE \_ GEN \_ T         | Se abilitata, la *coordinata* della trama t viene calcolata usando la funzione di generazione della trama definita con [**glTexGen**](gltexgen-functions.md). Se disabilitata, viene usata la *coordinata* di trama t corrente.                                                      |



 

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

[**glDisable**](gldisable.md)
</dt> <dt>

[**glDrawArrays**](gldrawarrays.md)
</dt> <dt>

[**glEdgeFlagPointer**](gledgeflagpointer.md)
</dt> <dt>

[**glEnd**](glend.md)
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

 

 





