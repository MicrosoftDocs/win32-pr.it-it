---
description: Quando si esegue il rendering dell'output 2D usando i vertici pre-trasformati, è necessario prestare attenzione per assicurarsi che ogni area di Texel corrisponda correttamente a un'area a singolo pixel. in caso contrario, può verificarsi una distorsione della trama.
ms.assetid: 6faeb1e3-ea6e-4cb1-a1e6-2a9a81b4c0c7
title: Mapping diretto dei Texel ai pixel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f86e9d05acff402128ddb83fc97898ff6a21d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225422"
---
# <a name="directly-mapping-texels-to-pixels-direct3d-9"></a>Mapping diretto dei Texel ai pixel (Direct3D 9)

Quando si esegue il rendering dell'output 2D usando i vertici pre-trasformati, è necessario prestare attenzione per assicurarsi che ogni area di Texel corrisponda correttamente a un'area a singolo pixel. in caso contrario, può verificarsi una distorsione della trama. Comprendendo le nozioni di base del processo seguito da Direct3D durante la rasterizzazione e il texturing dei triangoli, è possibile garantire che l'applicazione Direct3D esegua correttamente il rendering dell'output 2D.

![illustrazione di una visualizzazione della risoluzione 6x6](images/maptex-fig1.png)

Il diagramma precedente Mostra i pixel modellati come quadrati. In realtà, tuttavia, i pixel sono punti, non quadrati. Ogni quadrato nel diagramma precedente indica l'area illuminata dal pixel, ma un pixel è sempre solo un punto al centro di un quadrato. Questa distinzione, sebbene apparentemente piccola, è importante. Il diagramma seguente illustra una migliore illustrazione della stessa visualizzazione.

![illustrazione di una visualizzazione costituita da pixel](images/maptex-fig2.png)

Il diagramma precedente Mostra correttamente ogni pixel fisico come punto al centro di ciascuna cella. La coordinata dello spazio dello schermo (0,0) si trova direttamente sul pixel in alto a sinistra e quindi al centro della cella in alto a sinistra. L'angolo superiore sinistro dello schermo è quindi in (-0,5-0,5) perché è 0,5 celle a sinistra e 0,5 celle verso l'alto dal pixel superiore sinistro. Direct3D eseguirà il rendering di un quad con angoli in (0, 0) e (4, 4), come illustrato nella figura seguente.

![illustrazione di una struttura di un quad non rasterizzato tra (0, 0) e (4, 4)](images/maptex-fig3.png)

L'illustrazione precedente Mostra la posizione in cui il quad matematico è correlato alla visualizzazione, ma non Mostra il risultato del Quad quando Direct3D lo Rasterizza e lo invia alla visualizzazione. Infatti, non è possibile che una visualizzazione raster riempia il quad esattamente come mostrato perché i bordi del quad non coincidono con i limiti tra le celle dei pixel. In altre parole, poiché ogni pixel può visualizzare solo un singolo colore, ogni cella pixel viene riempita con un solo colore. Se lo schermo fosse il rendering del Quad esattamente come illustrato, le celle dei pixel lungo il bordo del quadre dovrebbero mostrare due colori distinti, ovvero blu, in cui il quadrato e il bianco sono visibili solo sullo sfondo.

Al contrario, l'hardware grafico viene utilizzato per determinare i pixel da riempire per approssimare il quad. Questo processo è denominato rasterizzazione ed è descritto in dettaglio nelle [regole di rasterizzazione (Direct3D 9)](rasterization-rules.md). Per questo particolare caso, il quad rasterizzato è illustrato nella figura seguente.

![illustrazione di un quad non con trama disegnato da (0,0) a (4, 4)](images/maptex-fig4.png)

Si noti che il quad passato a Direct3D ha gli angoli in (0,0) e (4, 4), ma l'output rasterizzato (l'illustrazione precedente) ha gli angoli in (-0,5,-0,5) e (3.5, 3.5). Confrontare le due illustrazioni precedenti per le differenze di rendering. È possibile osservare che il rendering effettivamente visualizzato è la dimensione corretta, ma è stato spostato da-0,5 celle nelle direzioni x e y. Tuttavia, fatta eccezione per le tecniche di campionamento multiplo, questa è la migliore approssimazione possibile al quad. Vedere l' [esempio antialias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) per una copertura completa del campionamento multiplo. Tenere presente che se il rasterizzatore riempie ogni cella il quad, l'area risultante sarà della dimensione 5 x 5 anziché quella desiderata 4 x 4.

Se si presuppone che le coordinate dello schermo provengano dall'angolo superiore sinistro della griglia di visualizzazione anziché dal pixel superiore sinistro, il quad viene visualizzato esattamente come previsto. Tuttavia, la differenza diventa evidente quando al quad viene assegnata una trama. Nella figura seguente viene illustrata la trama 4 x 4 di cui si eseguirà il mapping direttamente nel quad.

![illustrazione di una trama 4x4](images/maptex-fig5.png)

Poiché la trama è 4 Texel e il quad è 4 x 4 pixel, è possibile prevedere che il quad con trama appaia esattamente come la trama, indipendentemente dalla posizione sullo schermo in cui viene disegnato il quad. Tuttavia, questo non è il caso. anche le piccole modifiche alla posizione influiscono sulla modalità di visualizzazione della trama. Nell'illustrazione seguente viene mostrato come un quad tra (0, 0) e (4, 4) viene visualizzato dopo essere stato rasterizzato e con trama.

![illustrazione di un quad con trama disegnato da (0, 0) e (4, 4)](images/maptex-fig6.png)

Il quad disegnato nell'illustrazione precedente mostra l'output con trama (con una modalità di filtro lineare e una modalità di indirizzamento del morsetto) con il contorno rasterizzato sovrapposto. Nella parte restante di questo articolo viene spiegato esattamente il motivo per cui l'output è simile al modo in cui viene eseguito anziché sembrare la trama, ma per coloro che desiderano la soluzione qui è: i bordi del Quad di input devono trovarsi sulle linee limite tra le celle dei pixel. Semplicemente spostando le coordinate quadre x e y per-0,5 unità, le celle Texel copriranno perfettamente le celle dei pixel e il quad potrà essere ricreato perfettamente sullo schermo. L'ultima figura in questo argomento illustra il quad alle coordinate corrette.

I dettagli del motivo per cui l'output rasterizzato ha solo una lieve somiglianza alla trama di input sono direttamente correlati al modo in cui le trame degli esempi e degli indirizzi Direct3D. Di seguito si presuppone che si disponga di una conoscenza corretta dello [spazio delle coordinate di trama](texture-coordinates.md) e del [filtraggio bilineare della trama](bilinear-texture-filtering.md).

Tornando all'analisi dello strano output dei pixel, è opportuno tracciare il colore di output nella pixel shader: la pixel shader viene chiamata per ogni pixel selezionato per far parte della forma rasterizzata. Il quad blu a tinta unita raffigurato in un'illustrazione precedente potrebbe avere uno shader particolarmente semplice:


```
float4 SolidBluePS() : COLOR
{ 
    return float4( 0, 0, 1, 1 );
} 
```



Per il quad con trama, è necessario modificare leggermente la pixel shader:


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



Il codice presuppone che la trama 4 x 4 venga archiviata in texture. Come illustrato, il campionatore di trame di Sampler è impostato in modo da eseguire filtri bilineari su texture. Il pixel shader viene chiamato una volta per ogni pixel rasterizzato e ogni volta che il colore restituito è il colore della trama campionata in vTexCoord. Ogni volta che viene chiamata la pixel shader, l'argomento vTexCoord viene impostato sulle coordinate di trama in corrispondenza di tale pixel. Ciò significa che lo shader sta chiedendo il campionatore di trame per il colore della trama filtrata nella posizione esatta del pixel, come descritto nella figura seguente.

![illustrazione dei percorsi di campionamento per le coordinate di trama](images/maptex-fig7.png)

La trama (visualizzata sovrapposta) viene campionata direttamente in posizioni in pixel (visualizzate come punti neri). Le coordinate di trama non sono interessate dalla rasterizzazione (rimangono nello schermo proiettato-spazio del Quad originale). I punti neri mostrano dove si trovano i pixel di rasterizzazione. Le coordinate di trama in ogni pixel sono facilmente determinate mediante l'interpolazione delle coordinate archiviate in ogni vertice: il pixel in corrispondenza di (0, 0) coincide con il vertice in corrispondenza di (0, 0); Pertanto, le coordinate di trama in quel pixel sono semplicemente le coordinate di trama archiviate in quel vertice, UV (0,0, 0,0). Per il pixel in corrispondenza di (3, 1), le coordinate interpolate sono UV (0,75, 0,25) perché il pixel si trova a tre quarti della larghezza della trama e un quarto dell'altezza. Queste coordinate interpolate sono quelle che vengono passate al pixel shader.

I Texel non si allineano con i pixel in questo esempio; ogni pixel (e quindi ogni punto di campionamento) viene posizionato nell'angolo di quattro Texel. Poiché la modalità di filtro è impostata su lineare, il campionatore utilizzerà la media dei quattro texeli che condividono tale angolo. In questo modo si spiega perché il pixel che dovrebbe essere rosso è in realtà costituito da tre quarti di grigio e da un quarto rosso, il pixel che dovrebbe essere verde è uno a metà grigio più uno-quarto rosso più un quarto verde e così via.

Per risolvere il problema, è sufficiente eseguire correttamente il mapping del Quad ai pixel in cui verrà eseguita la rasterizzazione, quindi eseguire correttamente il mapping dei Texel ai pixel. Nella figura seguente vengono illustrati i risultati del disegno dello stesso Quad tra (-0,5,-0,5) e (3,5, 3,5), ovvero il quad previsto dall'inizio.

![illustrazione di un quad con trama che corrisponde al quad rasterizzato](images/maptex-fig8.png)

Nell'illustrazione precedente viene illustrato che il quad (mostrato in (-0,5-0,5) a (3,5, 3,5)) corrisponde esattamente all'area rasterizzata.

## <a name="summary"></a>Riepilogo

In sintesi, i pixel e i Texel sono effettivamente punti, non blocchi solidi. Lo spazio dello schermo ha origine in corrispondenza del pixel in alto a sinistra, ma le coordinate di trama provengono dall'angolo superiore sinistro della griglia della trama. In particolare, ricordarsi di sottrarre 0,5 unità dai componenti x e y delle posizioni dei vertici quando si lavora nello spazio dello schermo trasformato per allineare correttamente i Texel con i pixel.

Il codice seguente è un esempio di offset dei vertici di un quadrato di 256 per 256 per visualizzare correttamente una trama 256 per 256 nello spazio dello schermo trasformato.


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

[Coordinate di trama](texture-coordinates.md)
</dt> </dl>

 

 



