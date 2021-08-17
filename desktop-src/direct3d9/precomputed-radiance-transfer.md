---
description: Trasferimento di radiance pre-ricalcolato (Direct3D 9)
ms.assetid: 2a233d23-9a9e-4774-9be0-f3bfe0369b21
title: Trasferimento di radiance pre-ricalcolato (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc18eff66dab9a696a3e441d894a327890c53888da008d72a5f143ca0d345a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798733"
---
# <a name="precomputed-radiance-transfer-direct3d-9"></a>Trasferimento di radiance pre-ricalcolato (Direct3D 9)

## <a name="using-precomputed-radiance-transfer"></a>Uso del trasferimento di radiance pre-ricalcolato

Esistono diverse forme di complessità presenti in scene interessanti, tra cui il modo in cui viene modellato l'ambiente di illuminazione (ovvero i modelli di illuminazione dell'area rispetto a quelli punto/direzionale) e il tipo di effetti globali modellati (ad esempio, ombreggiature, interreflezioni, dispersione sottosociforma). Le tecniche di rendering interattivo tradizionali modellano una quantità limitata di questa complessità. PRT abilita questi effetti con alcune restrizioni significative:

-   Si presuppone che gli oggetti siano rigidi ,ovvero che non siano in formazioni.
-   Si tratta di un approccio incentrato sugli oggetti (a meno che gli oggetti non vengano spostati insieme, questi effetti globali non vengono mantenuti tra di essi).
-   Viene modellata solo l'illuminazione a bassa frequenza (con conseguente ombreggiatura soffice). Per le luci ad alta frequenza (ombreggiature acute), è necessario utilizzare le tecniche tradizionali.

PRT richiede uno dei seguenti elementi, ma non entrambi:

-   modelli a più tessere e rispetto \_ a 1 \_ 1
-   ps \_ 2 \_ 0

### <a name="standard-diffuse-lighting-versus-prt"></a>Illuminazione diffusa standard e PRT

Il rendering della figura seguente viene eseguito usando il modello di illuminazione tradizionale (n · l). Le ombreggiature acute possono essere abilitate usando un altro passaggio e una qualche forma di tecnica di ombreggiatura (mappe di profondità delle ombreggiature o volumi ombreggiati). L'aggiunta di più luci richiederebbe più passaggi (se si devono usare ombreggiature) o shader più complessi con tecniche tradizionali.

![Screenshot di un'illustrazione di cui viene eseguito il rendering usando il modello di illuminazione tradizionale](images/prt-diffuse-cropped.png)

Il rendering della figura successiva viene eseguito con PRT usando l'approssimazione migliore di una singola luce direzionale che può risolvere. Ciò comporta ombreggiature s attenuate che sarebbero difficili da produrre con le tecniche tradizionali. Poiché PRT modella sempre ambienti di illuminazione completi aggiungendo più luci o usando una mappa dell'ambiente, è possibile modificare solo i valori (ma non il numero) delle costanti usate dallo shader.

![Screenshot di un'illustrazione di cui viene eseguito il rendering tramite prt](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a>PRT con interreflezioni

L'illuminazione diretta raggiunge la superficie direttamente dalla luce. Le interreflezioni raggiungono la superficie della luce dopo un certo numero di volte che si è gonfiata su un'altra superficie. PRT può modellare questo comportamento senza modificare le prestazioni in fase di esecuzione semplicemente eseguendo il simulatore con parametri diversi.

La figura seguente viene creata usando solo PRT diretto (0 bounces senza interreflection).

![Screenshot di un'illustrazione di cui viene eseguito il rendering solo con prt diretto](images/prt-nointerreflections.png)

La figura seguente viene creata usando PRT con interreflezioni (2 bounce con interreflezioni).

![screenshot di un'illustrazione di cui viene eseguito il rendering usando prt con interreflezioni](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a>PRT con dispersione subsurface

La dispersione subsurface è una tecnica che modella il modo in cui la luce passa attraverso determinati materiali. Ad esempio, premere una torcia accesa sul palmo della mano. La luce della torcia passa attraverso la mano, lampeggia (cambiando colore nel processo) e esce dall'altro lato della mano. Questa operazione può anche essere modellata con semplici modifiche al simulatore e senza modifiche al runtime.

La figura seguente illustra PRT con la dispersione sotto la superficie.

![screenshot di un'illustrazione di cui viene eseguito il rendering usando prt con la dispersione sotto la superficie](images/prt-subsurface.png)

## <a name="how-prt-works"></a>Funzionamento di PRT

I termini seguenti sono utili per comprendere il funzionamento di PRT, come illustrato nel diagramma seguente.

Radice di origine: la sorgente rappresenta l'ambiente di illuminazione nel suo complesso. In PRT un ambiente arbitrario viene approssimato usando la base sferica aricale: si presuppone che questa illuminazione sia distante rispetto all'oggetto (lo stesso presupposto che viene fatto con le mappe dell'ambiente).

Uscita luminosità: la luce di uscita è la luce che esce da un punto sulla superficie da qualsiasi possibile sorgente (luce riflessa, dispersione sottosurface, emissione).

Vettori di trasferimento: i vettori di trasferimento mappano la radice di origine alla radice di uscita e vengono pre-ricalcolati offline usando una simulazione di trasporto di luce complessa.

![diagramma del funzionamento di prt](images/prt-lightingpicture.png)

PRT fattorizza il processo di rendering in due fasi, come illustrato nel diagramma seguente:

1.  Una simulazione di trasporto leggero dispendiosa pre-ricalcola i coefficienti di trasferimento che possono essere usati in fase di esecuzione.
2.  Una fase di run-time relativamente leggera prima approssima l'ambiente di illuminazione usando la base sferica arica, quindi usa questi coefficienti di illuminazione e i coefficienti di trasferimento pre-ricalcolati (dalla fase 1) con uno shader semplice, determinando la luminosità di uscita (la luce che lascia l'oggetto).

![diagramma del flusso di dati PRT](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a>Come usare l'API PRT

1.  Calcolare i vettori di trasferimento con uno dei valori di Calcolo... Metodi di [**ID3DXPRTEngine.**](id3dxprtengine.md)

    La gestione diretta di questi vettori di trasferimento richiede una quantità significativa di memoria e il calcolo dello shader. La compressione riduce significativamente la quantità di memoria e il calcolo dello shader necessari.

    I valori di illuminazione finali vengono calcolati in un vertex shader che implementa l'equazione di rendering compresso seguente.

    ![equazione del rendering prt](images/prt-shaderequation.png)

    Dove:

    

    | Parametro      | Descrizione                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | Rp             | Un singolo canale di radiazione di uscita al vertice p e viene valutato a ogni vertice della mesh.                     |
    | Mk             | Media per il cluster k. Si tratta di un vettore Di ordine dei coefficienti.                                               |
    | k              | ID cluster per il vertice p.                                                                                    |
    | L<sup>'</sup>  | Approssimazione della radice di origine nelle funzioni di base di SH. Si tratta di un vettore Di ordine dei coefficienti. |
    | j              | Intero che somma il numero di vettori PCA.                                                            |
    | w<sub>pj</sub> | Peso jth PCA per il punto p. Si tratta di un singolo coefficiente.                                                   |
    | B<sub>kj</sub> | Vettore di base JTH PCA per il cluster k. Si tratta di un vettore Di ordine dei coefficienti.                               |

    

     

    L'estrazione... I metodi [**di ID3DXPRTCompBuffer forniscono**](id3dxprtcompbuffer.md) l'accesso ai dati compressi dalla simulazione.

2.  Calcolare la radice di origine.

    Nell'API sono disponibili diverse funzioni helper per gestire un'ampia gamma di scenari di illuminazione comuni.

    

    | Funzione                                                         | Scopo                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [**D3DXSHEvalDirectionalLight**](d3dxshevaldirectionallight.md) | Approssima una luce direzionale convenzionale.                                                              |
    | [**D3DXSHEvalSphericalLight**](d3dxshevalsphericallight.md)     | Approssima le sorgenti di luce sferica locale. Si noti che PRT funziona solo con ambienti di illuminazione a distanza. |
    | [**D3DXSHEvalConeLight**](d3dxshevalconelight.md)               | Approssima una sorgente di luce di un'area distante. Un esempio è il sole (angolo cono molto piccolo).              |
    | [**D3DXSHEvalHemisphereLight**](d3dxshevalhemispherelight.md)   | Valuta una luce che è un'interpolazione lineare tra due colori (uno su ogni polifo di una sfera).         |

    

     

3.  Calcolare la radice di uscita.

    L'equazione 1 deve ora essere valutata in ogni punto usando un vertice o pixel shader. Prima che lo shader possa essere valutato, le costanti devono essere pre-ricalcolate e caricate nella tabella delle costanti (per informazioni dettagliate, vedere l'esempio [demo PRT).](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) Lo shader stesso è un'implementazione semplice di questa equazione.

    ```
    struct VS_OUTPUT
    {
        float4 Position   : POSITION;   // vertex position 
        float2 TextureUV  : TEXCOORD0;  // vertex texture coordinates 
        float4 Diffuse    : COLOR0;     // vertex diffuse color
    };

    VS_OUTPUT Output;   
    Output.Position = mul(vPos, mWorldViewProjection);

    float4 vExitR = float4(0,0,0,0);
    float4 vExitG = float4(0,0,0,0);
    float4 vExitB = float4(0,0,0,0);
        
    for (int i=0; i < (NUM_PCA_VECTORS/4); i++) 
    {
       vExitR += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*0];
       vExitG += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*1];
       vExitB += vPCAWeights[i] * 
           vClusteredPCA[iClusterOffset+i+1+(NUM_PCA_VECTORS/4)*2];
    }
       
    float4 vExitRadiance = vClusteredPCA[iClusterOffset];
    vExitRadiance.r += dot(vExitR,1);
    vExitRadiance.g += dot(vExitG,1);
    vExitRadiance.b += dot(vExitB,1);

    Output.Diffuse = vExitRadiance;
    ```

    

## <a name="references"></a>Riferimenti

Per altre informazioni sul PRT e sugli sferici armenici, vedere i documenti seguenti:


```
Precomputed Radiance Transfer for Real-Time Rendering in Dynamic, 
Low-Frequency Lighting Environments 
P.-P. Sloan, J. Kautz, J. Snyder
SIGGRAPH 2002 

Clustered Principal Components for Precomputed Radiance Transfer 
P.-P. Sloan, J. Hall, J. Hart, J. Snyder 
SIGGRAPH 2003 

Efficient Evaluation of Irradiance Environment Maps 
P.-P. Sloan 
ShaderX 2,  W. Engel 

Spherical Harmonic Lighting: The Gritty Details 
R. Green 
GDC 2003 

An Efficient Representation for Irradiance Environment Maps 
R. Ramamoorthi, P. Hanrahan 

A Practical Model for Subsurface Light Transport 
H. W. Jensen, S. R. Marschner, M. Levoy, and P. Hanrahan 
SIGGRAPH 2001 

Bi-Scale Radiance Transfer 
P.-P. Sloan, X. Liu, H.-Y. Shum, J. Snyder
SIGGRAPH 2003 

Fast, Arbitrary BRDF Shading for Low-Frequency Lighting Using Spherical 
Harmonics 
J. Kautz, P.-P. Sloan, J. Snyder
12th Eurographics Workshop on Rendering 

Precomputing Interactive Dynamic Deformable Scenes 
D. James, K. Fatahalian 
SIGGRAPH 2003 

All-Frequency Shadows Using Non-linear Wavelet Lighting Approximation 
R. Ng, R. Ramamoorth, P. Hanrahan 
SIGGRAPH 2003 

Matrix Radiance Transfer 
J. Lehtinen, J. Kautz
SIGGRAPH 2003 

Math World 
E. W. Weisstein, Wolfram Research, Inc. 

Quantum Theory of Angular Momentum 
D. A. Varshalovich, A.N. Moskalev, V.K. Khersonskii 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti avanzati](advanced-topics.md)
</dt> <dt>

[Equazioni PRT (Direct3D 9)](prt-equations.md)
</dt> <dt>

[Rappresentazione di PRT con trame (Direct3D 9)](representing-prt-with-textures.md)
</dt> <dt>

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md)
</dt> <dt>

[**ID3DXPRTEngine**](id3dxprtengine.md)
</dt> <dt>

[**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md)
</dt> <dt>

[Funzioni di trasferimento della radiance pre-ricalcolate](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 



