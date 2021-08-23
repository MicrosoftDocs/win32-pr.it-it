---
title: Funzione glPushAttrib (Gl.h)
description: Inserisce lo stack di attributi.
ms.assetid: 3c7b93cc-2112-4771-b422-a244821447e5
keywords:
- Funzione glPushAttrib OpenGL
topic_type:
- apiref
api_name:
- glPushAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252859065ddae0439441acb6afd797d26bbed44a246b628b4f0350d7f3b1e2d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519991"
---
# <a name="glpushattrib-function"></a>Funzione glPushAttrib

Inserisce lo stack di attributi.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPushAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Maschera* 
</dt> <dd>

Maschera che indica gli attributi da salvare. Le costanti della maschera simbolica e il relativo stato OpenGL associato sono i seguenti (i paragrafi con rientro elencano gli attributi salvati):

<dl> <dt>

<span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>BIT \_ DEL BUFFER ACCUM \_ GL \_ 
</dt> <dd>

Valore di cancellazione del buffer di accumulo

</dd> <dt>

<span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>BIT DEL \_ \_ BUFFER DEI COLORI GL \_
</dt> <dd>

Bit \_ di abilitazione GL ALPHA \_ TEST

Funzione di test alfa e valore di riferimento

Bit di abilitazione di GL \_ BLEND

Fusione di funzioni di origine e di destinazione

Bit \_ di abilitazione di GL DITHER

Impostazione \_ di GL DRAW \_ BUFFER

Bit \_ di abilitazione di GL LOGIC \_ OP

Funzione logic op

Valori non crittografati in modalità colore e in modalità indice

Maschera di scrittura in modalità colore e in modalità indice

</dd> <dt>

<span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>GL \_ CURRENT \_ BIT
</dt> <dd>

Colore RGBA corrente

Indice colori corrente

Vettore normale corrente

Coordinate correnti della trama

Posizione raster corrente GL \_ CURRENT \_ RASTER \_ POSITION FLAG \_ VALIDO

Colore RGBA associato alla posizione raster corrente

Indice dei colori associato alla posizione raster corrente

Coordinate di trama associate alla posizione raster corrente

Flag FLAG EDGE GL \_ \_

</dd> <dt>

<span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>BIT DEL \_ \_ BUFFER DI PROFONDITÀ GL \_
</dt> <dd>

Bit di abilitazione di GL \_ DEPTH \_ TEST

Funzione di test del buffer di profondità

Valore di cancellazione del buffer di profondità

Bit \_ di abilitazione di GL DEPTH \_ WRITEMASK

</dd> <dt>

<span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>BIT \_ DI ABILITAZIONE GL \_
</dt> <dd>

Flag \_ GL ALPHA \_ TEST

Flag GL \_ AUTO \_ NORMAL

Flag \_ GL BLEND

Abilitare i bit per i piani di ritaglio definibili dall'utente

MATERIALE A COLORI GL \_ \_

Flag \_ GL CULL \_ FACE

\_Flag GL DEPTH \_ TEST

Flag \_ DITHER GL

Flag \_ GL FOG

GL \_ LIGHT *i* dove 0 <= *i <* GL MAX \_ \_ LIGHTS

Flag \_ GL LIGHTING

Flag GL \_ LINE \_ SMOOTH

\_Flag GL LINE \_ STIPPLE

\_Flag GL COLOR LOGIC \_ \_ OP

\_Flag OP PER LA LOGICA \_ \_ DELL'INDICE GL

GL \_ MAP1 \_ x dove x è un tipo di mappa

GL \_ MAP2 \_ x dove x è un tipo di mappa

Flag \_ GL NORMALIZE

Flag SMOOTH di GL \_ POINT \_

Flag LINE \_ \_ OFFSET \_ POLIGONO GL

FLAG DI \_ \_ RIEMPIMENTO OFFSET \_ POLIGONO GL

Flag \_ PUNTO DI OFFSET \_ \_ POLIGONO GL

FLAG SMOOTH \_ \_ POLIGONO GL

Flag \_ \_ STIPPLE POLIGONO GL

\_Flag TEST DI GL SCISSOR \_

Flag \_ GL STENCIL \_ TEST

Flag \_ GL TEXTURE \_ 1D

Flag \_ GL TEXTURE \_ 2D

Flag GL \_ TEXTURE GEN x dove x è \_ \_ S, T, R o Q

</dd> <dt>

<span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>GL \_ EVAL \_ BIT
</dt> <dd>

GL \_ MAP1 \_ x abilitare i bit, dove x è un tipo di mappa

GL \_ MAP2 \_ x abilitare i bit, dove x è un tipo di mappa

Endpoint e divisioni della griglia 1D

Endpoint e divisioni della griglia 2D

Bit \_ di abilitazione GL AUTO \_ NORMAL

</dd> <dt>

<span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>GL \_ BIT DI \_ OSANNA
</dt> <dd>

Flag \_ di abilitazione GL FOG

Colore osanna

Densità della nebbia

Inizio lineare della nebbia

Fine lineare della nebbia

Indice delle nebbie

Valore \_ GL FOG \_ MODE

</dd> <dt>

<span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>GL \_ HINT \_ BIT
</dt> <dd>

IMPOSTAZIONE \_ \_ DELL'HINT DI \_ CORREZIONE DELLA PROSPETTIVA GL

Impostazione \_ \_ DELL'HINT SMOOTH DI GL POINT \_

Impostazione DI GL \_ LINE \_ SMOOTH \_ HINT

IMPOSTAZIONE \_ \_ DELL'HINT SMOOTH \_ POLIGONO GL

Impostazione \_ HINT GL FOG \_

</dd> <dt>

<span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>BIT DI \_ ILLUMINAZIONE GL \_
</dt> <dd>

Bit \_ di abilitazione di GL COLOR \_ MATERIAL

Gl \_ COLOR MATERIAL FACE \_ \_ value

Parametri del materiale di colore che tracciano il colore corrente

Colore della scena di ambiente

Valore \_ GL LIGHT MODEL LOCAL \_ \_ \_ VIEWER

Impostazione \_ GL LIGHT MODEL TWO \_ \_ \_ SIDE

Bit di abilitazione di GL \_ LIGHTING

Abilitare il bit per ogni luce

Intensità ambientale, diffusa e speculare per ogni luce

Direzione, posizione, esponente e angolo di taglio per ogni luce

Fattori di attenuazione costanti, lineari e quadratici per ogni luce

Colore ambientale, diffuso, speculare ed emissivo per ogni materiale

Indici di colore ambientale, diffuso e speculare per ogni materiale

Esponente speculare per ogni impostazione GL SHADE MODEL del \_ \_ materiale

</dd> <dt>

<span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>GL \_ LINE \_ BIT 
</dt> <dd>

Flag GL \_ LINE \_ SMOOTH

Bit di abilitazione di GL \_ LINE \_ STIPPLE

Modello di punta della linea e contatore di ripetizione

Spessore linea

</dd> <dt>

<span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>BIT \_ DELL'ELENCO \_ DI CONTABILITÀ GENERALE
</dt> <dd>

Impostazione \_ DI BASE DI GL LIST \_

</dd> <dt>

<span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>BIT DELLA MODALITÀ PIXEL GL \_ \_ \_
</dt> <dd>

Impostazioni \_ GL RED BIAS e GL RED \_ \_ \_ SCALE

GL \_ GREEN BIAS e GL GREEN \_ \_ \_ SCALE

GL \_ BLUE BIAS e GL BLUE \_ \_ \_ SCALE

GL \_ ALPHA BIAS e GL ALPHA \_ \_ \_ SCALE

GL \_ DEPTH BIAS e GL DEPTH \_ \_ \_ SCALE

Valori GL \_ INDEX OFFSET e GL INDEX \_ \_ \_ SHIFT

Flag GL \_ MAP COLOR e GL MAP \_ \_ \_ STENCIL

Fattori GL \_ ZOOM X e GL ZOOM \_ \_ \_ Y

Impostazione \_ GL READ \_ BUFFER

</dd> <dt>

<span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>BIT \_ DEL PUNTO GL \_
</dt> <dd>

Flag SMOOTH di GL \_ POINT \_

Dimensioni dei punti

</dd> <dt>

<span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>BIT \_ POLIGONO GL \_
</dt> <dd>

Bit \_ di abilitazione DI GL CULL \_ FACE

Valore \_ GL CULL \_ FACE \_ MODE

Indicatore \_ FRONT FACE GL \_

Impostazione \_ MODALITÀ \_ POLIGONO GL

FLAG SMOOTH \_ \_ POLIGONO GL

Bit di abilitazione di GL \_ POLYGON \_ STIPPLE

FLAG \_ DI RIEMPIMENTO OFFSET \_ \_ POLIGONO GL

Flag LINE \_ \_ OFFSET \_ POLIGONO GL

Flag \_ PUNTO DI OFFSET \_ \_ POLIGONO GL

FATTORE DI \_ \_ OFFSET POLIGONO GL \_

UNITÀ DI \_ \_ OFFSET POLIGONO GL \_

</dd> <dt>

<span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>BIT \_ \_ STIPPLE POLIGONO GL \_
</dt> <dd>

Immagine della punta del poligono

</dd> <dt>

<span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>GL \_ SCISSOR \_ BIT
</dt> <dd>

\_Flag TEST DI GL SCISSOR \_

Casella di forbice

</dd> <dt>

<span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>BIT \_ DEL BUFFER DELLO \_ STENCIL \_ GL
</dt> <dd>

BIT \_ DI ABILITAZIONE DI GL STENCIL \_ TEST

Funzione Stencil e valore di riferimento

Maschera del valore dello stencil

Azioni di passaggio del buffer di profondità, passaggio e esito negativo dello stencil

Valore di cancellazione del buffer di stencil

Maschera di scrittura del buffer di stencil

</dd> <dt>

<span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>BIT DI TRAMA GL \_ \_
</dt> <dd>

Abilitare i bit per le quattro coordinate di trama

Colore del bordo per ogni immagine della trama

Funzione minification per ogni immagine di trama

Funzione di ingrandimento per ogni immagine di trama

Coordinate di trama e modalità di ritorno a capo per ogni immagine di trama

Colore e modalità per ogni ambiente di trama

Abilitare i bit GL \_ TEXTURE \_ GEN \_ *x*; *x* è S, T, R e Q

Impostazione \_ GL TEXTURE GEN MODE per \_ \_ S, T, R e Q

Equazioni del piano glTexGen per S, T, R e Q

</dd> <dt>

<span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>BIT \_ DI TRASFORMAZIONE GL \_
</dt> <dd>

Coefficienti dei sei piani di ritaglio

Abilitare i bit per i piani di ritaglio definibili dall'utente

Valore \_ GL MATRIX \_ MODE

Flag \_ GL NORMALIZE

</dd> <dt>

<span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>BIT \_ DEL VIEWPORT \_ GL
</dt> <dd>

Intervallo di profondità (vicino e lontano)

Origine ed extent del viewport

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla [**funzione glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OVERFLOW DELLO STACK GL \_ \_**</dt> </dl>    | La funzione è stata chiamata mentre lo stack di attributi era pieno.<br/>                                                                |
| <dl> <dt>**OPERAZIONE GL \_ NON \_ VALIDA**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La **funzione glPushAttrib** accetta un argomento, una maschera che indica i gruppi di variabili di stato da salvare nello stack di attributi. Le costanti simboliche vengono usate per impostare i bit nella maschera. Il parametro mask viene in genere costruito applicando **l'operazione OR** logica a diverse di queste costanti. È possibile usare la maschera speciale GL \_ ALL \_ ATTRIB \_ BITS per salvare tutti gli stati impilabili.

La [**funzione glPopAttrib**](glpopattrib.md) ripristina i valori delle variabili di stato salvate con l'ultimo **comando glPushAttrib.** Quelli non salvati vengono lasciati invariati.

È un errore eseguire il push degli attributi in uno stack completo o rimuovere gli attributi da uno stack vuoto. In entrambi i casi, il flag di errore è impostato e non vengono apportate altre modifiche allo stato OpenGL.

Inizialmente, lo stack di attributi è vuoto.

Non tutti i valori per lo stato OpenGL possono essere salvati nello stack di attributi. Ad esempio, non è possibile salvare il pacchetto pixel e decomprimere lo stato, lo stato della modalità di rendering e selezionare e lo stato del feedback.

La profondità dello stack di attributi dipende dall'implementazione, ma deve essere almeno 16.

Le funzioni seguenti recuperano informazioni correlate **a glPushAttrib** e [**glPopAttrib**](glpopattrib.md):

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ ATTRIB \_ STACK \_ DEPTH

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) argomento GL \_ MAX \_ ATTRIB STACK \_ \_ DEPTH

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glGetClipPlane**](glgetclipplane.md)
</dt> <dt>

[**glGetError**](glgeterror.md)
</dt> <dt>

[**glGetLight**](glgetlight.md)
</dt> <dt>

[**glGetMap**](glgetmap.md)
</dt> <dt>

[**glGetMaterial**](glgetmaterial.md)
</dt> <dt>

[**glGetPixelMap**](glgetpixelmap.md)
</dt> <dt>

[**glGetPolygonStipple**](glgetpolygonstipple.md)
</dt> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**glGetTexEnv**](glgettexenv.md)
</dt> <dt>

[**glGetTexGen**](glgettexgen.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
</dt> <dt>

[**glGetTexLevelParameter**](glgettexlevelparameter.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> </dl>

 

 





