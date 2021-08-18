---
description: Quando si esegue il rendering dell'output 2D usando vertici pre-trasformati, è necessario assicurarsi che ogni area texel corrisponda correttamente a un'area a pixel singolo. In caso contrario, può verificarsi una distorsione della trama.
ms.assetid: 6faeb1e3-ea6e-4cb1-a1e6-2a9a81b4c0c7
title: Mapping diretto di Texel ai pixel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7294b88fb8b672aea980dbb23cb4e7c5bbd2bfdbf4d33a5078a09dbfa3084d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988259"
---
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a>Mapping diretto di Texel ai pixel (Direct3D 9)

Quando si esegue il rendering dell'output 2D usando vertici pre-trasformati, è necessario assicurarsi che ogni area texel corrisponda correttamente a un'area a pixel singolo. In caso contrario, può verificarsi una distorsione della trama. Comprendendo le nozioni di base del processo seguito da Direct3D durante l'rasterizzazione e la creazione di testo dei triangoli, è possibile assicurarsi che l'applicazione Direct3D esegua correttamente il rendering dell'output 2D.

![illustrazione di uno schermo con risoluzione 6x6](images/maptex-fig1.png)

Il diagramma precedente mostra i pixel modellati come quadrati. In realtà, tuttavia, i pixel sono punti, non quadrati. Ogni quadrato nel diagramma precedente indica l'area illuminata dal pixel, ma un pixel è sempre un punto al centro di un quadrato. Questa distinzione, anche se apparentemente piccola, è importante. Un'illustrazione migliore della stessa visualizzazione è illustrata nel diagramma seguente.

![illustrazione di una visualizzazione costituita da pixel](images/maptex-fig2.png)

Il diagramma precedente mostra correttamente ogni pixel fisico come punto al centro di ogni cella. La coordinata dello spazio dello schermo (0, 0) si trova direttamente in corrispondenza del pixel in alto a sinistra e quindi al centro della cella superiore sinistra. L'angolo superiore sinistro dello schermo è quindi in corrispondenza di (-0,5, -0,5) perché si tratta di 0,5 celle a sinistra e di 0,5 celle verso l'alto dal pixel superiore sinistro. Direct3D eseguirà il rendering di un quad con angoli in corrispondenza di (0, 0) e (4, 4), come illustrato nella figura seguente.

![illustrazione di un contorno di un quad non strutturato compreso tra (0, 0) e (4, 4)](images/maptex-fig3.png)

La figura precedente mostra dove il quad matematico è in relazione allo schermo, ma non mostra l'aspetto che avrà il quad quando Direct3D lo rasterizza e lo invia allo schermo. In realtà, è impossibile che uno schermo raster riempia il quad esattamente come illustrato perché i bordi del quad non coincidono con i limiti tra le celle in pixel. In altre parole, poiché ogni pixel può visualizzare un solo colore, ogni cella pixel viene riempita con un solo colore; Se lo schermo eseguisse il rendering del quad esattamente come illustrato, le celle in pixel lungo il bordo del quad dovevano mostrare due colori distinti: blu dove è coperto dal quad e bianco dove è visibile solo lo sfondo.

Al contrario, l'hardware grafico ha il compito di determinare quali pixel devono essere riempiti per approssimare il quad. Questo processo è detto rasterizzazione ed è descritto in dettaglio in [Regole di rasterizzazione (Direct3D 9).](rasterization-rules.md) Per questo caso specifico, il quad rasterizzato è illustrato nella figura seguente.

![illustrazione di un quad senza testo disegnato da (0,0) a (4,4)](images/maptex-fig4.png)

Si noti che il quad passato a Direct3D ha angoli in corrispondenza di (0, 0) e (4, 4), ma l'output rasterizzato (figura precedente) ha angoli in (-0,5,-0,5) e (3,5,3,5). Confrontare le due illustrazioni precedenti per le differenze di rendering. È possibile vedere che le dimensioni effettivamente visualizzate dalla visualizzazione sono corrette, ma sono state spostate di -0,5 celle nelle direzioni x e y. Tuttavia, ad eccezione delle tecniche di campionamento multiplo, questa è l'approssimazione migliore possibile al quad. Per una descrizione completa del campionamento [multiplo,](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) vedere l'esempio di antialias. Tenere presente che se il rasterizzatore riempie ogni cella attraversata dal quad, l'area risultante sarà di dimensione 5 x 5 anziché 4 x 4 desiderata.

Se si presuppone che le coordinate dello schermo provenino dall'angolo superiore sinistro della griglia di visualizzazione anziché dal pixel superiore sinistro, il quad viene visualizzato esattamente come previsto. Tuttavia, la differenza diventa chiara quando al quad viene data una trama. La figura seguente mostra la trama 4 x 4 che verrà mappata direttamente sul quad.

![illustrazione di una trama 4x4](images/maptex-fig5.png)

Poiché la trama è 4 x 4 texel e il quad è 4 x 4 pixel, è possibile che il quad con trama venga visualizzato esattamente come la trama indipendentemente dalla posizione sullo schermo in cui viene disegnato il quad. Tuttavia, questo non è il caso. anche lievi variazioni di posizione influiscono sulla modalità di visualizzazione della trama. La figura seguente mostra come viene visualizzato un quad compreso tra (0, 0) e (4, 4) dopo essere stato rasterizzato e con trama.

![illustrazione di un quad con trama disegnato da (0, 0) e (4, 4)](images/maptex-fig6.png)

Il quad disegnato nell'illustrazione precedente mostra l'output con trama (con una modalità di filtro lineare e una modalità di indirizzamento a forma di chiusura) con il contorno rasterizzato sovrapposto. Nella parte restante di questo articolo viene illustrato esattamente il motivo per cui l'output ha un aspetto simile a quello della trama, ma per coloro che vogliono la soluzione, ecco: i bordi del quad di input devono trovarsi sulle linee limite tra le celle di pixel. Spostando semplicemente le coordinate dei quad x e y di -0,5 unità, le celle texel coprono perfettamente le celle in pixel e il quad può essere ricreato perfettamente sullo schermo. L'ultima illustrazione di questo argomento mostra il quad in corrispondenza delle coordinate corrette.

I dettagli del motivo per cui l'output rasterizzato ha solo una leggera somiglianza con la trama di input sono direttamente correlati al modo in cui Direct3D indirizza ed estrae le trame. Ciò che segue presuppone che si abbia una buona conoscenza dello spazio delle coordinate della [trama e](texture-coordinates.md) del filtro [bilineare della trama.](bilinear-texture-filtering.md)

Tornando all'analisi dell'output di pixel strano, è opportuno tracciare il colore di output all'pixel shader: il pixel shader viene chiamato per ogni pixel selezionato come parte della forma rasterizzata. Il quad blu a tinta unita illustrato in una figura precedente potrebbe avere uno shader particolarmente semplice:


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



Per il quad con trama, il pixel shader deve essere leggermente modificato:


```
texture MyTexture;

sampler MySampler = 
sampler_state 
{ 
    Texture = <MyTexture>;
    MinFilter = Linear;
    MagFilter = Linear;
    AddressU = Clamp;
    AddressV = Clamp;
};

float4 TextureLookupPS( float2 vTexCoord : TEXCOORD0 ) : COLOR
{
    return tex2D( MySampler, vTexCoord );
} 
```



Questo codice presuppone che la trama 4 x 4 sia archiviata in MyTexture. Come illustrato, il campionatore di trama MySampler è impostato per l'esecuzione di filtri bilineari su MyTexture. Il pixel shader viene chiamato una volta per ogni pixel rasterizzato e ogni volta che il colore restituito è il colore della trama campionata in vTexCoord. Ogni volta che pixel shader viene chiamato, l'argomento vTexCoord viene impostato su coordinate di trama in corrispondenza di tale pixel. Ciò significa che lo shader chiede al campionatore di trama il colore della trama filtrato nella posizione esatta del pixel, come illustrato nella figura seguente.

![illustrazione delle posizioni di campionamento per le coordinate di trama](images/maptex-fig7.png)

La trama (mostrata come sovrapposta) viene campionata direttamente in posizioni pixel (visualizzate come punti neri). Le coordinate della trama non sono interessate dalla rasterizzazione (rimangono nello spazio dello schermo proiettato del quad originale). I punti neri mostrano la posizione dei pixel di rasterizzazione. Le coordinate della trama in ogni pixel sono facilmente determinate interpolando le coordinate archiviate in ogni vertice: il pixel in corrispondenza di (0,0) coincide con il vertice in (0, 0); Pertanto, le coordinate della trama in corrispondenza di tale pixel sono semplicemente le coordinate di trama archiviate in corrispondenza di tale vertice, UV (0.0, 0.0). Per il pixel in corrispondenza di (3, 1), le coordinate interpolate sono UV (0,75, 0,25) perché tale pixel si trova a tre quarto della larghezza della trama e a un quarto della sua altezza. Queste coordinate interpolate vengono passate al pixel shader.

I texel non sono allineati con i pixel in questo esempio. ogni pixel (e pertanto ogni punto di campionamento) è posizionato in corrispondenza dell'angolo di quattro texel. Poiché la modalità di filtro è impostata su Lineare, il campionatore media i colori dei quattro texel che condividono tale angolo. Questo spiega perché il pixel previsto per essere rosso è in realtà grigio a tre quarto più un quarto rosso, il pixel che dovrebbe essere verde è di mezzo grigio più un quarto rosso più un quarto verde e così via.

Per risolvere questo problema, è necessario eseguire correttamente il mapping del quad ai pixel in cui verrà rasterizzato e quindi eseguire correttamente il mapping dei texel ai pixel. La figura seguente mostra i risultati del disegno dello stesso quad tra (-0,5, -0,5) e (3.5, 3.5), ovvero il quad previsto fin dall'inizio.

![illustrazione di un quad con trama che corrisponde al quad rasterizzato](images/maptex-fig8.png)

La figura precedente dimostra che il quad (indicato da (-0.5, -0.5) a (3.5, 3.5)) corrisponde esattamente all'area rasterizzata.

## <a name="summary"></a>Riepilogo

In breve, pixel e texel sono effettivamente punti, non blocchi a tinta unita. Lo spazio dello schermo ha origine nel pixel superiore sinistro, ma le coordinate della trama hanno origine nell'angolo superiore sinistro della griglia della trama. Soprattutto, ricordarsi di sottrarre 0,5 unità dai componenti x e y delle posizioni dei vertici quando si lavora nello spazio dello schermo trasformato per allineare correttamente i texel ai pixel.

Il codice seguente è un esempio di offset dei vertici di un quadrato 256 per 256 per visualizzare correttamente una trama 256 per 256 nello spazio dello schermo trasformato.


```C++
//define FVF with vertex values in transformed screen space
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZRHW|D3DFVF_TEX1)

struct CUSTOMVERTEX
{
    FLOAT x, y, z, rhw; // position
    FLOAT tu, tv;       // texture coordinates
};

//unadjusted vertex values
float left = 0.0f;
float right = 255.0f;
float top = 0.0f;
float bottom = 255.0f;


//256 by 256 rectangle matching 256 by 256 texture
CUSTOMVERTEX vertices[] =
{
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f}, // x, y, z, rhw, u, v
    { right, top,    0.5f, 1.0f, 1.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  top,    0.5f, 1.0f, 0.0f, 0.0f},
    { right, bottom, 0.5f, 1.0f, 1.0f, 1.0f},
    { left,  bottom, 0.5f, 1.0f, 0.0f, 1.0f},
    
};
```




```C++
//adjust all the vertices to correctly line up texels with pixels 
for (int i=0; i<6; i++)
{
    vertices[i].x -= 0.5f;
    vertices[i].y -= 0.5f;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Coordinate della trama](texture-coordinates.md)
</dt> </dl>

 

 



