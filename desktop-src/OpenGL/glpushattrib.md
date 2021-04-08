---
title: funzione glPushAttrib (GL. h)
description: Inserisce lo stack dell'attributo.
ms.assetid: 3c7b93cc-2112-4771-b422-a244821447e5
keywords:
- funzione glPushAttrib OpenGL
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
ms.openlocfilehash: 9e0bc15b85ddca3bdbe5f6774b5368c6f0cde8dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048047"
---
# <a name="glpushattrib-function"></a>glPushAttrib (funzione)

Inserisce lo stack dell'attributo.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI glPushAttrib(
   GLbitfield mask
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*maschera* 
</dt> <dd>

Maschera che indica gli attributi da salvare. Le costanti di maschera simbolica e il relativo stato OpenGL associato sono le seguenti, ovvero l'elenco dei paragrafi rientrati in cui vengono salvati gli attributi:

<dl> <dt>

<span id="GL_ACCUM_BUFFER_BIT_"></span><span id="gl_accum_buffer_bit_"></span>\_bit del buffer di accut GL \_ \_ 
</dt> <dd>

Valore Clear buffer accumulo

</dd> <dt>

<span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span>\_bit del \_ buffer dei colori GL \_
</dt> <dd>

\_Bit di \_ Abilitazione test GL Alpha

Funzione di test Alpha e valore di riferimento

\_Bit di abilitazione di Blend GL

Fusione di funzioni di origine e destinazione

\_Bit di abilitazione dithering GL

Impostazione del buffer di \_ estrazione GL \_

\_Bit di \_ Abilitazione della logica GL

Funzione logica op

Valori cancellati in modalità colore e indice

Writemasks modalità colore e indice

</dd> <dt>

<span id="GL_CURRENT_BIT"></span><span id="gl_current_bit"></span>\_bit corrente \_ GL
</dt> <dd>

Colore RGBA corrente

Indice colori corrente

Vettore normale corrente

Coordinate di trama correnti

Flag di posizione corrente della posizione raster corrente GL \_ \_ \_ \_

Colore RGBA associato alla posizione raster corrente

Indice dei colori associato alla posizione raster corrente

Coordinate di trama associate alla posizione raster corrente

\_Flag di \_ flag Edge GL

</dd> <dt>

<span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span>\_ \_ bit buffer di profondità GL \_
</dt> <dd>

\_Bit di \_ Abilitazione test di profondità GL

Funzione di test del buffer di profondità

Valore Clear buffer Depth

\_Bit di \_ Abilitazione WRITEMASK Depth

</dd> <dt>

<span id="GL_ENABLE_BIT"></span><span id="gl_enable_bit"></span>\_bit di abilitazione GL \_
</dt> <dd>

\_Flag di \_ test GL Alpha

\_Flag di \_ normalizzazione automatica GL

\_Flag di Blend GL

Abilita BITS per i piani di ritaglio definibili dall'utente

\_materiale colore \_ GL

\_Flag della faccia di abbattimento GL \_

\_Flag di \_ test profondità GL

\_Flag di dithering GL

\_Flag di nebbia GL

GL \_ Light *i* where 0 <= *i* < GL \_ Max \_ Lights

\_Flag di illuminazione GL

\_ \_ Flag uniforme linea GL

\_ \_ Flag stipple linea GL

\_ \_ Flag op della logica colori GL \_

\_ \_ Flag op logica indice GL \_

GL \_ Mappa1 \_ x dove x è un tipo di mappa

GL \_ map2 \_ x dove x è un tipo di mappa

\_Flag di normalizzazione GL

\_Flag uniforme del punto GL \_

\_Flag di \_ linea offset POLIGONo GL \_

\_Flag di \_ riempimento offset POLIGONo GL \_

\_Flag del \_ punto di offset del POLIGONo GL \_

\_Flag uniforme poligono GL \_

\_Flag GL poligono \_ stipple

\_Flag di test della forbice GL \_

\_Flag di \_ test stencil GL

\_Flag di trama GL \_ 1D

\_ \_ Flag 2D trama GL

Flag GL \_ trama \_ gen \_ x dove x è S, T, R o Q

</dd> <dt>

<span id="GL_EVAL_BIT"></span><span id="gl_eval_bit"></span>BIT valutazione GL \_ \_
</dt> <dd>

GL \_ Mappa1 \_ x Abilita BITS, dove x è un tipo di mappa

GL \_ map2 \_ x Abilita BITS, dove x è un tipo di mappa

endpoint e divisioni della griglia da 1 a D

endpoint e divisioni della griglia 2D

\_Bit di \_ attivazione normale automatica GL

</dd> <dt>

<span id="GL_FOG_BIT"></span><span id="gl_fog_bit"></span>\_bit di nebbia GL \_
</dt> <dd>

\_Flag di abilitazione della nebbia GL

Colore nebbia

Densità di nebbia

Inizio nebbia lineare

Fine nebbia lineare

Indice nebbia

Valore della modalità di \_ nebbia GL \_

</dd> <dt>

<span id="GL_HINT_BIT"></span><span id="gl_hint_bit"></span>\_bit suggerimento \_ GL
</dt> <dd>

\_Impostazione dell' \_ hint di correzione prospettiva GL \_

\_Impostazione del \_ Suggerimento smussato del punto GL \_

\_Impostazione dell' \_ hint uniforme linea \_ GL

\_Impostazione dell' \_ hint Smooth POLIGONo GL \_

Impostazione del suggerimento di \_ nebbia GL \_

</dd> <dt>

<span id="GL_LIGHTING_BIT"></span><span id="gl_lighting_bit"></span>\_bit di illuminazione GL \_
</dt> <dd>

\_Bit di \_ Abilitazione materiale colore GL

\_ \_ Valore viso materiale colore GL \_

Parametri del materiale colori che verificano il colore corrente

Colore della scena ambiente

\_ \_ \_ Valore del visualizzatore locale per GL Light Model \_

\_ \_ \_ Impostazione lato due del modello GL Light \_

\_Bit di abilitazione dell'illuminazione GL

Abilita bit per ogni luce

Intensità di ambiente, diffusa e speculare per ogni luce

Direzione, posizione, esponente e angolo di taglio per ogni luce

Fattori di attenuazione costanti, lineari e quadratici per ogni luce

Colore di ambiente, diffuso, speculare e emissivo per ogni materiale

Indici di colore ambient, Diffusion e speculare per ogni materiale

Esponente speculare per ogni impostazione del modello GL \_ Shade del materiale \_

</dd> <dt>

<span id="GL_LINE_BIT_"></span><span id="gl_line_bit_"></span>\_bit linea \_ GL 
</dt> <dd>

\_ \_ Flag uniforme linea GL

\_Bit di \_ Abilitazione della riga GL stipple

Modello stipple linea e Ripeti contatore

Spessore linea

</dd> <dt>

<span id="GL_LIST_BIT"></span><span id="gl_list_bit"></span>\_bit elenco \_ GL
</dt> <dd>

\_ \_ Impostazione base elenco GL

</dd> <dt>

<span id="GL_PIXEL_MODE_BIT"></span><span id="gl_pixel_mode_bit"></span>\_bit in \_ modalità GL pixel \_
</dt> <dd>

\_Impostazioni della \_ \_ scala rossa e della distorsione GL rosse \_

Valori della scala verde GL \_ \_ e della distorsione GL \_ \_

\_Bias blu GL \_ e \_ scala GL blu \_

\_ \_ Polarizzazione GL Alpha e \_ scala GL Alpha \_

\_ \_ Distorsione di profondità GL e \_ scala di profondità GL \_

\_Offset indice GL \_ e \_ \_ valori MAIUSC di indice GL

\_Colori della mappa GL \_ e \_ flag di stencil della mappa GL \_

\_Fattori zoom \_ X e GL \_ Zoom \_ Y

Impostazione del buffer di \_ lettura GL \_

</dd> <dt>

<span id="GL_POINT_BIT"></span><span id="gl_point_bit"></span>\_bit punto \_ GL
</dt> <dd>

\_Flag uniforme del punto GL \_

Dimensioni dei punti

</dd> <dt>

<span id="GL_POLYGON_BIT"></span><span id="gl_polygon_bit"></span>\_bit poligono GL \_
</dt> <dd>

\_Bit di \_ Abilitazione della faccia di selezione GL

\_ \_ Valore modalità della faccia di selezione GL \_

\_ \_ Indicatore viso anteriore GL

\_Impostazione della modalità poligono GL \_

\_Flag uniforme poligono GL \_

\_Bit di \_ Abilitazione stipple POLIGONo GL

\_Flag di \_ riempimento offset POLIGONo GL \_

\_Flag di \_ linea offset POLIGONo GL \_

\_Flag del \_ punto di offset del POLIGONo GL \_

\_fattore di \_ offset POLIGONo GL \_

\_unità offset poligono GL \_ \_

</dd> <dt>

<span id="GL_POLYGON_STIPPLE_BIT"></span><span id="gl_polygon_stipple_bit"></span>\_bit stipple poligono GL \_ \_
</dt> <dd>

Immagine stipple poligono

</dd> <dt>

<span id="GL_SCISSOR_BIT"></span><span id="gl_scissor_bit"></span>\_bit a forbice GL \_
</dt> <dd>

\_Flag di test della forbice GL \_

Casella Scissor

</dd> <dt>

<span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span>\_ \_ bit buffer dello stencil GL \_
</dt> <dd>

\_Bit di \_ Abilitazione test stencil GL

Funzione stencil e valore di riferimento

Maschera valore stencil

Azioni di passaggio del buffer di errore, passaggio e profondità dello stencil

Valore cancellazione buffer dello stencil

Writemask buffer dello stencil

</dd> <dt>

<span id="GL_TEXTURE_BIT"></span><span id="gl_texture_bit"></span>\_bit trama \_ GL
</dt> <dd>

Abilita BITS per le quattro coordinate di trama

Colore del bordo per ogni immagine di trama

Funzione minification per ogni immagine di trama

Funzione di ingrandimento per ogni immagine di trama

Coordinate di trama e modalità a capo per ogni immagine di trama

Colore e modalità per ogni ambiente di trama

Abilita BITS GL \_ texture \_ gen \_ *x*; *x* è S, T, R e Q

\_ \_ \_ Impostazione della modalità di generazione della trama GL per S, T, R e Q

equazioni del piano glTexGen per S, T, R e Q

</dd> <dt>

<span id="GL_TRANSFORM_BIT"></span><span id="gl_transform_bit"></span>\_bit di trasformazione GL \_
</dt> <dd>

Coefficienti dei sei piani di ritaglio

Abilita BITS per i piani di ritaglio definibili dall'utente

\_Valore della \_ modalità matrice GL

\_Flag di normalizzazione GL

</dd> <dt>

<span id="GL_VIEWPORT_BIT"></span><span id="gl_viewport_bit"></span>\_bit del viewport GL \_
</dt> <dd>

Intervallo di profondità (quasi e lontano)

Origine e extent del viewport

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significato                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_overflow dello stack GL \_**</dt> </dl>    | La funzione è stata chiamata mentre lo stack dell'attributo era pieno.<br/>                                                                |
| <dl> <dt>**\_operazione GL non valida \_**</dt> </dl> | La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Commenti

La funzione **glPushAttrib** accetta un argomento, una maschera che indica i gruppi di variabili di stato da salvare nello stack di attributi. Le costanti simboliche vengono utilizzate per impostare i bit nella maschera. Il parametro mask viene in genere costruito applicando l' **operazione or** logica a diverse di queste costanti. È possibile utilizzare la speciale maschera GL \_ tutti \_ i \_ bit attrib per salvare tutti gli Stati impilabili.

La funzione [**glPopAttrib**](glpopattrib.md) Ripristina i valori delle variabili di stato salvate con l'ultimo comando **glPushAttrib** . Quelli non salvati vengono lasciati invariati.

Non è possibile eseguire il push degli attributi in uno stack completo oppure per estrarre gli attributi da uno stack vuoto. In entrambi i casi, viene impostato il flag di errore e non viene apportata alcuna modifica allo stato OpenGL.

Inizialmente, lo stack dell'attributo è vuoto.

Non tutti i valori per lo stato OpenGL possono essere salvati nello stack di attributi. Ad esempio, non è possibile salvare il pacchetto di pixel e decomprimere lo stato, la modalità di rendering e lo stato di selezione e di feedback.

La profondità dello stack di attributi dipende dall'implementazione, ma deve essere almeno 16.

Le funzioni seguenti recuperano informazioni relative a **glPushAttrib** e [**glPopAttrib**](glpopattrib.md):

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ profondità dello stack \_ attrib

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ profondità massima \_ \_ dello stack \_ attrib

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

[**Remo**](glend.md)
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

 

 





