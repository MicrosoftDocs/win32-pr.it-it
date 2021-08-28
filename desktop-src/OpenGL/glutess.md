---
title: Funzione gluTessCallback (Glu.h)
description: La funzione gluTessCallback definisce un callback per un oggetto a tessellazione.
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
keywords:
- Funzione gluTessCallback OpenGL
topic_type:
- apiref
api_name:
- gluTessCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 310ffe6b59e0b3fab307d1103f29c8fe619f0385
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481937"
---
# <a name="glutesscallback-function"></a>Funzione gluTessCallback

La **funzione gluTessCallback** definisce un callback per un oggetto a tessellazione.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI gluTessCallback(
   GLUtesselator *tess,
   GLenum        which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tess* 
</dt> <dd>

Oggetto a tassellamento (creato con [**gluNewTess).**](glunewtess.md)

</dd> <dt>

*Che* 
</dt> <dd>

Callback da definire. I valori seguenti sono validi: GLU \_ TESS \_ BEGIN, GLU \_ TESS BEGIN \_ \_ DATA, GLU TESS EDGE FLAG, GLU TESS EDGE \_ FLAG \_ \_ \_ \_ \_ \_ \_ DATA, GLU TESS \_ VERTEX, GLU \_ TESS \_ VERTEX \_ DATA, GLU TESS \_ \_ END, GLU TESS END \_ \_ \_ DATA, GLU TESS \_ \_ COMBINE, GLU TESS COMBINE \_ \_ \_ DATA, GLU TESS COMBINE DATA, GLU \_ TESS ERROR E GLU TESS ERROR \_ \_ \_ \_ DATA.

Per altre informazioni su questi callback, vedere la sezione Osservazioni seguente.

</dd> <dt>

*Fn* 
</dt> <dd>

Funzione da chiamare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare **gluTessCallback** per specificare un callback che deve essere usato da un oggetto a tessellazione. Se il callback specificato è già definito, viene sostituito. Se *fn* è **NULL,** il callback esistente diventa indefinito.

L'oggetto a tessellazione usa questi callback per descrivere come un poligono specificato viene suddiviso in triangoli.

Esistono due versioni di ogni callback, una con dati poligonali che è possibile definire e una senza. Se vengono specificate entrambe le versioni di un particolare callback, verrà usato il callback con i dati poligono specificati. Il *parametro \_ di dati* polygon di [**gluTessBeginPolygon**](glutessbeginpolygon.md) è una copia del puntatore specificato quando è stato chiamato **gluTessBeginPolygon.**

Di seguito sono riportati i callback validi:




| Callback | Descrizione | 
|----------|-------------|
| GLU_TESS_BEGIN | Il GLU_TESS_BEGIN callback viene richiamato come <a href="glbegin.md"><strong>glBegin</strong></a> per indicare l'inizio di una primitiva (triangolo). La funzione accetta un singolo argomento di tipo <strong>GLenum</strong>. Se si imposta la proprietà GLU_TESS_BOUNDARY_ONLY su GL_FALSE, l'argomento viene impostato su GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP o GL_TRIANGLES. Se si imposta la proprietà GLU_TESS_BOUNDARY_ONLY su GL_TRUE, l'argomento viene impostato su GL_LINE_LOOP. Il prototipo di funzione per questo callback è il seguente: <strong>void</strong><strong>begin</strong> ( tipo<strong>GLenum</strong><em>);</em><br /> | 
| GLU_TESS_BEGIN_DATA | GLU_TESS_BEGIN_DATA è uguale al callback GLU_TESS_BEGIN, ad eccezione del fatto che accetta un argomento puntatore aggiuntivo. Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Il prototipo di funzione per questo callback è: <strong>void</strong><strong>beginData</strong> (<strong>tipo GLenum</strong><em>,</em>void <strong></strong>  *  <em>polygon_data</em>);<br /> | 
| GLU_TESS_EDGE_FLAG | Il GLU_TESS_EDGE_FLAG callback è simile a <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>. La funzione accetta un singolo flag booleano che indica quali bordi si trovano sul limite del poligono. Se il flag è GL_TRUE, ogni vertice che segue inizia un bordo che si trova sul limite del poligono; ovvero un bordo che separa un'area interna da una esterna. Se il flag è GL_FALSE, ogni vertice che segue inizia un bordo che si trova all'interno del poligono. Il GLU_TESS_EDGE_FLAG callback di vertice (se definito) viene richiamato prima che venga eseguito il primo callback del vertice. Poiché le ventole triangolo e le strisce triangolare non supportano i flag di bordo, il callback begin non viene chiamato con GL_TRIANGLE_FAN o GL_TRIANGLE_STRIP se viene fornito un callback del flag di bordo. Le ventole e le strisce vengono invece convertite in triangoli indipendenti. Il prototipo di funzione per questo callback è:<br /><strong>void</strong><strong>edgeFlag</strong> (<em>flag</em><strong>GLboolean</strong>);<br /> | 
| GLU_TESS_EDGE_FLAG_DATA | Il GLU_TESS_EDGE_FLAG_DATA callback è uguale al callback GLU_TESS_EDGE_FLAG, ad eccezione del fatto che accetta un argomento puntatore aggiuntivo. Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Il prototipo di funzione per questo callback è: <strong>void</strong><strong>edgeFlagData</strong> (<em>flag</em><strong>GLboolean,</strong> <strong>void</strong>  *  <em>polygon_data</em>);<br /> | 
| GLU_TESS_VERTEX | Il GLU_TESS_VERTEX callback viene richiamato tra i callback di inizio e fine. È simile a glVertex e definisce i vertici dei triangoli creati dal processo a tessellazione. La funzione accetta un puntatore come unico argomento. Questo puntatore è identico al puntatore opaco specificato quando è stato definito il vertice (vedere <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>). Il prototipo di funzione per questo callback è: <strong>void</strong><strong>vertex</strong> (<strong>void</strong>  *  <em>vertex_data</em>);<br /> | 
| GLU_TESS_VERTEX_DATA | Il GLU_TESS_VERTEX_DATA è uguale al callback GLU_TESS_VERTEX, ad eccezione del fatto che accetta un argomento puntatore aggiuntivo. Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Il prototipo di funzione per questo callback è: <strong>void</strong><strong>vertexData</strong> (void * <em>vertex_data</em>, <strong>void</strong>  *  <em>polygon_data</em>);<br /> | 
| GLU_TESS_END | Il GLU_TESS_END callback ha lo stesso scopo di <a href="glend.md"><strong>glEnd</strong></a>. Indica la fine di una primitiva e non accetta argomenti. Il prototipo di funzione per questo callback è: <strong>void</strong><strong>end</strong> (<strong>void</strong>);<br /> | 
| GLU_TESS_END_DATA | Il GLU_TESS_END_DATA callback è uguale al callback GLU_TESS_END, ad eccezione del fatto che accetta un argomento puntatore aggiuntivo. Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Il prototipo di funzione per questo callback è: <strong>void</strong><strong>endData</strong> (<strong>void</strong>  *  <em>polygon_data</em>);<br /> | 
| GLU_TESS_COMBINE | Chiamare il callback GLU_TESS_COMBINE per creare un nuovo vertice quando la tessellazione rileva un'intersezione o per unire le funzionalità. La funzione accetta quattro argomenti: una matrice di tre elementi, ognuno di tipo Gldouble.<br /> Matrice di quattro puntatori.<br /> Matrice di quattro elementi, ognuno di tipo GLfloat.<br /> Puntatore a un puntatore.<br /> Il prototipo di funzione per questo callback è: <br /><strong>void</strong><strong>combine</strong>(<strong>GLdouble</strong><em>coords</em>[3], <strong>void</strong>  *  <em>vertex_data</em>[4], <strong>GLfloat</strong><em>weight</em>[4], <strong>void</strong>  ** <em>outData</em>);<br /> Il vertice è definito come una combinazione lineare di un massimo di quattro vertici esistenti, archiviati in vertex_data. I coefficienti della combinazione lineare sono dati dal peso; questi pesi sommano sempre a 1,0. Tutti i puntatori ai vertici sono validi anche quando alcuni pesi sono pari a zero. Il parametro coords fornisce la posizione del nuovo vertice.<br /> Allocare un altro vertice, interpolare i parametri usando vertex_data e peso e restituire il nuovo puntatore al vertice in outData. Questo handle viene fornito durante i callback di rendering. Liberare la memoria a volte dopo aver chiamato <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.<br /> Ad esempio, se il poligono si trova in un piano arbitrario nello spazio tridimensionale e si associa un colore a ogni vertice, il callback GLU_TESS_COMBINE potrebbe essere simile al seguente:<br /><pre data-space="preserve"><code>void myCombine( GLdouble coords[3], VERTEX *d[4],                 GLfloat w[4], VERTEX **dataOut ) {     VERTEX *newVertex = new_vertex();     newVertex-&gt;x = coords[0];     newVertex-&gt;y = coords[1];     newVertex-&gt;z = coords[2];     newVertex-&gt;r = w[0]*d[0]-&gt;r + w[1]*d[1]-&gt;r + w[2]*d[2]-&gt;r +                    w[3]*d[3]-&gt;r;     newVertex-&gt;g = w[0]*d[0]-&gt;g + w[1]*d[1]-&gt;g + w[2]*d[2]-&gt;g +                    w[3]*d[3]-&gt;g;     newVertex-&gt;b = w[0]*d[0]-&gt;b + w[1]*d[1]-&gt;b + w[2]*d[2]-&gt;b +                    w[3]*d[3]-&gt;b;     newVertex-&gt;a = w[0]*d[0]-&gt;a + w[1]*d[1]-&gt;a + w[2]*d[2]-&gt;a +                    w[3]*d[3]-&gt;a;     *dataOut = newVertex; }</code></pre>Quando la tessellazione rileva un'intersezione, il callback GLU_TESS_COMBINE o GLU_TESS_COMBINE_DATA (vedere di seguito) deve essere definito e deve scrivere un puntatore non<strong>NULL</strong> in dataOut. In caso contrario, GLU_TESS_NEED_COMBINE_CALLBACK si verifica un errore e non viene generato alcun output. Si tratta dell'unico errore che può verificarsi durante la tessellazione e il rendering.<br /> | 
| GLU_TESS_COMBINE_DATA | Il GLU_TESS_COMBINE_DATA callback è uguale al callback GLU_TESS_COMBINE, ad eccezione del fatto che accetta un argomento puntatore aggiuntivo. Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Il prototipo di funzione per questo callback è: <strong>void</strong><strong>combineData</strong> (<strong>GLdouble</strong><em>coords</em>[3], <strong>void</strong>  * <em>vertex_data</em>[4], <strong>GLfloat</strong><em>weight</em>[4], <strong>void</strong>  ** <em>outData</em>, <strong>void</strong>  *  <em>polygon_data</em>);<br /> | 
| GLU_TESS_ERROR | Il GLU_TESS_ERROR callback viene chiamato quando viene rilevato un errore. L'unico argomento è di <strong>tipo GLenum</strong>; indica l'errore specifico che si è verificato ed è impostato su uno degli elementi seguenti: GLU_TESS_MISSING_BEGIN_POLYGON<br /> GLU_TESS_MISSING_END_POLYGON<br /> GLU_TESS_MISSING_BEGIN_CONTOUR<br /> GLU_TESS_MISSING_END_CONTOUR<br /> GLU_TESS_COORD_TOO_LARGE<br /> GLU_TESS_NEED_COMBINE_CALLBACK<br /> Chiamare gluErrorString per recuperare le stringhe di caratteri che descrivono questi errori. Il prototipo di funzione per questo callback è il seguente:<br /><strong>Errore void</strong><strong>(</strong> <strong>GLenum</strong><em>errno</em>);<br /> La libreria GLU recupera i primi quattro errori inserendo la chiamata o le chiamate mancanti. GLU_TESS_COORD_TOO_LARGE indica che alcune coordinate dei vertici hanno superato il valore GLU_TESS_MAX_COORD costante predefinito in valore assoluto e che il valore è stato ancorato. I valori delle coordinate devono essere sufficientemente piccoli da poter essere moltiplicati tra loro senza overflow. GLU_TESS_NEED_COMBINE_CALLBACK indica che la tessellazione ha rilevato un'intersezione tra due bordi nei dati di input e il callback GLU_TESS_COMBINE o GLU_TESS_COMBINE_DATA non è stato fornito. Non verrà generato alcun output.<br /> | 
| GLU_TESS_ERROR_DATA | Il GLU_TESS_ERROR_DATA callback è uguale al callback GLU_TESS_ERROR, ad eccezione del fatto che accetta un argomento puntatore aggiuntivo. Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Il prototipo di funzione per questo callback è: <strong>void</strong><strong>errorData</strong> (<strong>GLenum</strong><em>errno,</em> <strong>void</strong>  *  <em>polygon_data</em>);<br /> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> <dt>

[**gluDeleteTess**](gludeletetess.md)
</dt> <dt>

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





