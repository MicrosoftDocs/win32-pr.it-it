---
description: Trasferimento Radiance pre-calcolato (Direct3D 9)
ms.assetid: 2a233d23-9a9e-4774-9be0-f3bfe0369b21
title: Trasferimento Radiance pre-calcolato (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94829a2559888c61ae795309bac5d1ab699d7f27
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104554736"
---
# <a name="precomputed-radiance-transfer-direct3d-9"></a>Trasferimento Radiance pre-calcolato (Direct3D 9)

## <a name="using-precomputed-radiance-transfer"></a>Uso del trasferimento Radiance pre-calcolato

Negli scenari interessanti sono presenti diverse forme di complessità, tra cui il modo in cui l'ambiente di illuminazione è modellato (ovvero i modelli di illuminazione ad area rispetto ai punti/direzionali) e il tipo di effetti globali che vengono modellati (ad esempio, ombre, interriflettenze, scattering di sottosuperficie). Le tecniche di rendering interattive tradizionali modellano una quantità limitata di questa complessità. Il PRT Abilita questi effetti con alcune restrizioni significative:

-   Si presuppone che gli oggetti siano rigidi (ovvero nessuna deformazione).
-   Si tratta di un approccio incentrato sugli oggetti (a meno che gli oggetti non vengano spostati insieme, questi effetti globali non vengono mantenuti tra di essi).
-   Viene modellata solo l'illuminazione a bassa frequenza (che produce ombre morbide). Per le luci ad alta frequenza (ombre acute), è necessario utilizzare tecniche tradizionali.

Per PRT è necessario uno dei seguenti, ma non entrambi:

-   modelli altamente tassellati e vs \_ 1 \_ 1
-   PS \_ 2 \_ 0

### <a name="standard-diffuse-lighting-versus-prt"></a>Illuminazione standard diffusa rispetto a PRT

Viene eseguito il rendering dell'illustrazione seguente usando il modello di illuminazione tradizionale (n · l). È possibile abilitare le ombreggiature nitide usando un altro passaggio e una forma di tecnica di ombreggiatura (mappe di profondità ombreggiatura o volumi shadow). L'aggiunta di più luci richiederebbe più passaggi (se è necessario usare le ombreggiature) o più shader complessi con tecniche tradizionali.

![Screenshot di un'illustrazione sottoposta a rendering usando il modello di illuminazione tradizionale](images/prt-diffuse-cropped.png)

L'illustrazione successiva viene sottoposta a rendering con PRT usando la migliore approssimazione di una singola luce direzionale che può risolvere. In questo modo si otterrà un'ombreggiatura soft che sarebbe difficile da produrre con le tecniche tradizionali. Poiché PRT modella sempre gli ambienti di illuminazione completi che aggiungono più luci o usando una mappa dell'ambiente, è possibile modificare solo i valori (ma non il numero) delle costanti usate dallo shader.

![Screenshot di un'illustrazione sottoposta a rendering usando PRT](images/prt-diffuseshadows-cropped.png)

### <a name="prt-with-interreflections"></a>PRT con interriflettenze

L'illuminazione diretta raggiunge la superficie direttamente dalla luce. Le interriflettenze sono chiare che raggiungono la superficie dopo il rimbalzo di un'altra superficie per un certo numero di volte. Il PRT può modellare questo comportamento senza modificare le prestazioni in fase di esecuzione eseguendo semplicemente il simulatore con parametri diversi.

La figura seguente viene creata usando solo il PRT diretto (0 rimbalzi senza interriflettenze).

![Screenshot di un'illustrazione di cui è stato eseguito il rendering usando solo la PRT diretta](images/prt-nointerreflections.png)

La figura seguente viene creata usando PRT con le interspecchiazioni (2 rimbalzi con le interdipendenze).

![Screenshot di un'illustrazione sottoposta a rendering usando PRT con interriflettenze](images/prt-interreflections.png)

### <a name="prt-with-subsurface-scattering"></a>PRT con scattering della sottosuperficie

La dispersione della sottosuperficie è una tecnica che modella il modo in cui la luce passa attraverso determinati materiali. Ad esempio, premere una torcia accesa sul Palm della mano. La luce della torcia passa attraverso la mano, rimbalza (cambiando colore nel processo) ed esce dall'altra parte della mano. Questo può essere modellato anche con semplici modifiche al simulatore e nessuna modifica al runtime.

Nella figura seguente viene illustrato PRT con la dispersione della sottosuperficie.

![Screenshot di un'illustrazione sottoposta a rendering usando PRT con scattering della sottosuperficie](images/prt-subsurface.png)

## <a name="how-prt-works"></a>Funzionamento di PRT

I termini seguenti sono utili per comprendere il funzionamento di PRT, come illustrato nel diagramma seguente.

Radiance di origine: la luminosità di origine rappresenta l'ambiente di illuminazione nel suo complesso. In PRT un ambiente arbitrario viene approssimato usando la base armonica sferica. questa illuminazione si presuppone che sia distante rispetto all'oggetto (lo stesso presupposto per le mappe dell'ambiente).

Radiance di uscita: l'uscita Radiance è la luce che esce da un punto sulla superficie da qualsiasi origine possibile (Radiance riflesso, scattering di sottosuperficie, emissione).

Transfer vectors: i vettori di trasferimento eseguono il mapping della luminosità del codice sorgente al radiatore di uscita e vengono precalcolati offline usando una simulazione di trasporto leggero complessa.

![diagramma del funzionamento di PRT](images/prt-lightingpicture.png)

PRT determina il processo di rendering in due fasi, come illustrato nel diagramma seguente:

1.  Una simulazione di trasporto leggero costosa Precalcola i coefficienti di trasferimento che possono essere usati in fase di esecuzione.
2.  Una fase di runtime relativamente leggera approssimatamente si avvicina all'ambiente di illuminazione usando la base armonica sferica, quindi usa questi coefficienti di illuminazione e i coefficienti di trasferimento pre-calcolati (dalla fase 1) con uno shader semplice, con conseguente uscita Radiance (luce che esce dall'oggetto).

![diagramma del flusso di dati PRT](images/prt-dataflow.png)

### <a name="how-to-use-the-prt-api"></a>Come usare l'API PRT

1.  Calcola i vettori di trasferimento con una delle risorse di calcolo... metodi di [**ID3DXPRTEngine**](id3dxprtengine.md).

    La gestione diretta di questi vettori di trasferimento richiede una quantità significativa di calcolo della memoria e dello shader. La compressione riduce significativamente la quantità di memoria e il calcolo dello shader necessari.

    I valori di illuminazione finali vengono calcolati in un vertex shader che implementa la seguente equazione di rendering compresso.

    ![equazione di rendering PRT](images/prt-shaderequation.png)

    Dove:

    

    | Parametro      | Descrizione                                                                                                     |
    |----------------|-----------------------------------------------------------------------------------------------------------------|
    | RP             | Un singolo canale di uscita Radiance al vertice p e viene valutato in ogni vertice della mesh.                     |
    | MK             | Media per il cluster k. Si tratta di un vettore Order ² di coefficienti.                                               |
    | k              | ID del cluster per il vertice p.                                                                                    |
    | L<sup>'</sup>  | Approssimazione della luminosità di origine nelle funzioni di base SH. Si tratta di un vettore Order ² di coefficienti. |
    | j              | Intero che somma il numero di vettori PCA.                                                            |
    | w<sub>PJ</sub> | Peso PCA JTH per il punto p. Si tratta di un singolo coefficiente.                                                   |
    | B<sub>kJ</sub> | Vettore di base di JTH PCA per il cluster k. Si tratta di un vettore Order ² di coefficienti.                               |

    

     

    Estrazione... i metodi di [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) forniscono l'accesso ai dati compressi dalla simulazione.

2.  Calcolo della luminosità di origine.

    Sono disponibili diverse funzioni helper nell'API per gestire un'ampia gamma di scenari di illuminazione comuni.

    

    | Funzione                                                         | Scopo                                                                                                     |
    |------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
    | [**D3DXSHEvalDirectionalLight**](d3dxshevaldirectionallight.md) | Si avvicina a una luce direzionale convenzionale.                                                              |
    | [**D3DXSHEvalSphericalLight**](d3dxshevalsphericallight.md)     | Approssima le fonti di luce sferiche locali. Si noti che PRT funziona solo con gli ambienti di illuminazione della distanza. |
    | [**D3DXSHEvalConeLight**](d3dxshevalconelight.md)               | Si avvicina a una sorgente di luce dell'area distante. Un esempio è la luce solare (angolo conico molto piccolo).              |
    | [**D3DXSHEvalHemisphereLight**](d3dxshevalhemispherelight.md)   | Valuta una luce che rappresenta un'interpolazione lineare tra due colori (uno in ogni polo di una sfera).         |

    

     

3.  Calcolo della luminosità di uscita.

    L'equazione 1 deve ora essere valutata in ogni punto usando un vertice o un pixel shader. Prima di poter valutare lo shader, le costanti devono essere pre-calcolate e caricate nella tabella Constant (vedere l' [esempio di demo PRT](https://msdn.microsoft.com/library/Ee418763(v=VS.85).aspx) per informazioni dettagliate). Lo shader è una semplice implementazione di questa equazione.

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

Per ulteriori informazioni sulle armoniche PRT e sferiche, vedere i seguenti documenti:


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

[Funzioni di trasferimento Radiance pre-calcolate](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[Funzioni matematiche](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 



