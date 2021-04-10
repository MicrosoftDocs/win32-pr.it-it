---
title: funzione gluTessCallback (Glu. h)
description: La funzione gluTessCallback definisce un callback per un oggetto a mosaico.
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
keywords:
- funzione gluTessCallback OpenGL
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
ms.openlocfilehash: 17cdba8b9dd9a3e762a93923a3c353fbc9578377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964828"
---
# <a name="glutesscallback-function"></a>gluTessCallback (funzione)

La funzione **gluTessCallback** definisce un callback per un oggetto a mosaico.

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

Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).

</dd> <dt>

*che* 
</dt> <dd>

Callback da definire. Sono validi i valori seguenti: GLU \_ Tess \_ Begin, Glu \_ Tess \_ Begin \_ data, Glu \_ Tess \_ Edge \_ flag, Glu \_ tesse \_ Edge \_ \_ data flag, Glu \_ Tess \_ vertex, GLU \_ Tess \_ Vertex \_ data, Glu \_ Tess \_ end, Glu \_ Tess \_ End \_ data, Glu Tess, di Glu Tess, Glu Tess \_ \_ \_ \_ \_ \_ \_ Error e Glu \_ Tess, dati di \_ errore \_ .

Per ulteriori informazioni su questi callback, vedere la sezione Osservazioni riportata di seguito.

</dd> <dt>

*FN* 
</dt> <dd>

Funzione da chiamare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Utilizzare **gluTessCallback** per specificare un callback che deve essere utilizzato da un oggetto a mosaico. Se il callback specificato è già definito, viene sostituito. Se *FN* è **null**, il callback esistente diventa non definito.

L'oggetto mosaico utilizza questi callback per descrivere il modo in cui un poligono specificato viene suddiviso in triangoli.

Sono disponibili due versioni di ogni callback, una con dati Polygon che è possibile definire e una senza. Se vengono specificate entrambe le versioni di un particolare callback, verrà usato il callback con i dati del poligono specificati. Il parametro di *\_ dati Polygon* di [**gluTessBeginPolygon**](glutessbeginpolygon.md) è una copia del puntatore che è stato specificato al momento della chiamata di **gluTessBeginPolygon** .

Di seguito sono riportati i callback validi:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Callback</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GLU_TESS_BEGIN</td>
<td>Il callback GLU_TESS_BEGIN viene richiamato come <a href="glbegin.md"><strong>glBegin</strong></a> per indicare l'inizio di una primitiva (triangolo). La funzione accetta un solo argomento di tipo <strong>GLEnum</strong>. Se si imposta la proprietà GLU_TESS_BOUNDARY_ONLY su GL_FALSE, l'argomento viene impostato su GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP o GL_TRIANGLES. Se si imposta la proprietà GLU_TESS_BOUNDARY_ONLY su GL_TRUE, l'argomento viene impostato su GL_LINE_LOOP. Il prototipo di funzione per questo callback è il seguente: <strong>void</strong> <strong>Begin</strong> ( <em>tipo</em><strong>GLEnum</strong> );<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_BEGIN_DATA</td>
<td>GLU_TESS_BEGIN_DATA è uguale al callback GLU_TESS_BEGIN ad eccezione del fatto che accetta un argomento puntatore aggiuntivo. Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Il prototipo di funzione per questo callback è: <strong>void</strong> <strong>beginData</strong> (<strong>glenum</strong> <em>Type</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_EDGE_FLAG</td>
<td>Il callback GLU_TESS_EDGE_FLAG è simile a <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>. La funzione accetta un singolo flag booleano che indica quali bordi si trovano sul limite del poligono. Se il flag è GL_TRUE, ogni vertice che segue inizia un bordo che si trova sul limite del poligono; ovvero un bordo che separa un'area interna da uno esterno. Se il flag è GL_FALSE, ogni vertice che segue inizia un bordo che si trova nell'interno del poligono. Il callback GLU_TESS_EDGE_FLAG (se definito) viene richiamato prima che venga eseguito il primo callback del vertice. Poiché le ventole del triangolo e le strisce triangolari non supportano i flag Edge, il callback Begin non viene chiamato con GL_TRIANGLE_FAN o GL_TRIANGLE_STRIP se viene fornito un callback del flag Edge. Al contrario, le ventole e le strisce vengono convertite in triangoli indipendenti. Il prototipo di funzione per questo callback è:<br/> <strong>void</strong> <strong>edgeFlag</strong> (<strong></strong> <em>flag</em>GLboolean);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_EDGE_FLAG_DATA</td>
<td>Il callback GLU_TESS_EDGE_FLAG_DATA è uguale al callback GLU_TESS_EDGE_FLAG ad eccezione del fatto che accetta un argomento puntatore aggiuntivo. Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Il prototipo di funzione per questo callback è: <strong>void</strong> <strong>edgeFlagData</strong> (<strong>GLboolean</strong> <em>flag</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_VERTEX</td>
<td>Il callback GLU_TESS_VERTEX viene richiamato tra i callback Begin e end. È simile a glVertex e definisce i vertici dei triangoli creati dal processo a mosaico. La funzione accetta un puntatore come unico argomento. Questo puntatore è identico al puntatore opaco fornito quando è stato definito il vertice (vedere <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>). Il prototipo di funzione per questo callback è: <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> * <em>vertex_data</em>);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_VERTEX_DATA</td>
<td>Il GLU_TESS_VERTEX_DATA è uguale al callback GLU_TESS_VERTEX ad eccezione del fatto che accetta un argomento puntatore aggiuntivo. Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Il prototipo di funzione per questo callback è: <strong>void</strong>  <strong>vertexData</strong> (void * <em>vertex_data</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_END</td>
<td>Il callback GLU_TESS_END ha lo stesso scopo di <a href="glend.md"><strong>glEnd</strong></a>. Indica la fine di una primitiva e non accetta argomenti. Il prototipo di funzione per questo callback è: <strong>void</strong> <strong>end</strong> (<strong>void</strong>);<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_END_DATA</td>
<td>Il callback GLU_TESS_END_DATA è uguale al callback GLU_TESS_END ad eccezione del fatto che accetta un argomento puntatore aggiuntivo. Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Il prototipo di funzione per questo callback è: <strong>void</strong> <strong>endData</strong> (<strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_COMBINE</td>
<td>Chiamare il callback GLU_TESS_COMBINE per creare un nuovo vertice quando lo schema a mosaico rileva un'intersezione o per unire le funzionalità. La funzione accetta quattro argomenti: una matrice di tre elementi, ognuno di tipo Gldouble.<br/> Matrice di quattro puntatori.<br/> Matrice di quattro elementi, ognuno di tipo GLfloat.<br/> Puntatore a un puntatore.<br/> Il prototipo di funzione per questo callback è: <br/> <strong>void</strong> <strong>combine</strong>(<strong>GLdouble</strong> <em>Coordinate</em>[3], <strong>void</strong> * <em>vertex_data</em>[4], <strong>GLfloat</strong> <em>Weight</em>[4], <strong>void</strong>  ** <em>OutData</em>);<br/> Il vertice viene definito come una combinazione lineare di un massimo di quattro vertici esistenti, archiviati in vertex_data. I coefficienti della combinazione lineare vengono assegnati in base al peso; questi pesi vengono sempre sommati a 1,0. Tutti i puntatori ai vertici sono validi anche quando alcuni pesi sono pari a zero. Il parametro coordinate fornisce la posizione del nuovo vertice.<br/> Allocare un altro vertice, interpolare i parametri usando vertex_data e il peso e restituire il nuovo puntatore del vertice in OutData. Questo handle viene fornito durante il rendering di callback. Liberare la memoria qualche minuto dopo la chiamata a <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.<br/> Se, ad esempio, il poligono si trova in un piano arbitrario in uno spazio tridimensionale e si associa un colore a ogni vertice, il callback GLU_TESS_COMBINE potrebbe essere simile al seguente:<br/>
<pre data-space="preserve"><code>void myCombine( GLdouble coords[3], VERTEX *d[4], 
                GLfloat w[4], VERTEX **dataOut ) 
{ 
    VERTEX *newVertex = new_vertex(); 
    newVertex->x = coords[0]; 
    newVertex->y = coords[1]; 
    newVertex->z = coords[2]; 
    newVertex->r = w[0]*d[0]->r + w[1]*d[1]->r + w[2]*d[2]->r + 
                   w[3]*d[3]->r; 
    newVertex->g = w[0]*d[0]->g + w[1]*d[1]->g + w[2]*d[2]->g + 
                   w[3]*d[3]->g; 
    newVertex->b = w[0]*d[0]->b + w[1]*d[1]->b + w[2]*d[2]->b + 
                   w[3]*d[3]->b; 
    newVertex->a = w[0]*d[0]->a + w[1]*d[1]->a + w[2]*d[2]->a + 
                   w[3]*d[3]->a; 
    *dataOut = newVertex; 
}</code></pre>
Quando lo schema a mosaico rileva un'intersezione, è necessario definire il callback di GLU_TESS_COMBINE o di GLU_TESS_COMBINE_DATA (vedere di seguito) e scrivere un puntatore non<strong>null</strong> in dati. In caso contrario, si verifica l'errore GLU_TESS_NEED_COMBINE_CALLBACK e non viene generato alcun output. Si tratta dell'unico errore che può verificarsi durante il mosaico e il rendering.<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_COMBINE_DATA</td>
<td>Il callback GLU_TESS_COMBINE_DATA è uguale al callback GLU_TESS_COMBINE ad eccezione del fatto che accetta un argomento puntatore aggiuntivo. Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Il prototipo di funzione per questo callback è: <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>Coordinate</em>[3], <strong>void</strong> *<em>vertex_data</em>[4], <strong>GLfloat</strong> <em>Weight</em>[4 <strong>], void</strong>  ** <em>OutData</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
<tr class="odd">
<td>GLU_TESS_ERROR</td>
<td>Il callback GLU_TESS_ERROR viene chiamato quando viene rilevato un errore. Il primo argomento è di tipo <strong>GLEnum</strong>; indica l'errore specifico che si è verificato ed è impostato su uno dei seguenti elementi: GLU_TESS_MISSING_BEGIN_POLYGON<br/> GLU_TESS_MISSING_END_POLYGON<br/> GLU_TESS_MISSING_BEGIN_CONTOUR<br/> GLU_TESS_MISSING_END_CONTOUR<br/> GLU_TESS_COORD_TOO_LARGE<br/> GLU_TESS_NEED_COMBINE_CALLBACK<br/> Chiamare gluErrorString per recuperare le stringhe di caratteri che descrivono questi errori. Il prototipo di funzione per questo callback è il seguente:<br/> <strong></strong> <strong>errore</strong> void (<strong>GLEnum</strong> <em>errno</em>);<br/> La libreria GLU esegue il ripristino dai primi quattro errori inserendo la chiamata o le chiamate mancanti. GLU_TESS_COORD_TOO_LARGE indica che alcune coordinate del vertice hanno superato la costante predefinita GLU_TESS_MAX_COORD in un valore assoluto e che il valore è stato bloccato. (I valori delle coordinate devono essere sufficientemente piccoli da poter moltiplicare due elementi senza overflow). GLU_TESS_NEED_COMBINE_CALLBACK indica che il mosaico ha rilevato un'intersezione tra due bordi nei dati di input e non è stato fornito il callback GLU_TESS_COMBINE o GLU_TESS_COMBINE_DATA. Non verrà generato alcun output.<br/></td>
</tr>
<tr class="even">
<td>GLU_TESS_ERROR_DATA</td>
<td>Il callback GLU_TESS_ERROR_DATA è uguale al callback GLU_TESS_ERROR, ad eccezione del fatto che accetta un argomento puntatore aggiuntivo. Questo puntatore è identico al puntatore opaco fornito quando si chiama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>. Il prototipo di funzione per questo callback è: <strong>void</strong> <strong>ErrorData</strong> (<strong>glenum</strong> <em>errno</em>, <strong>void</strong> * <em>polygon_data</em>);<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**Remo**](glend.md)
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

 

 





