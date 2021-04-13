---
description: Usare la raccolta SasHostParameterValue per definire la raccolta di valori dell'applicazione host, nonché il tipo e i membri esposti agli effetti.
ms.assetid: 3fef353d-323a-4cc1-a8c9-2bf154754835
title: Data binding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b67305d4acc8a4ed9e0827203e4602db26a99da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341541"
---
# <a name="data-binding"></a>Data binding

Usare la [raccolta SasHostParameterValue](#sashostparametervalue-collection) per definire la raccolta di valori dell'applicazione host, nonché il tipo e i membri esposti agli effetti. Utilizzare l'annotazione [SasBindAddress](#sasbindaddress) in un file di effetti per associare un parametro di effetto al parametro corrispondente nell'applicazione host.

## <a name="sashostparametervalue-collection"></a>Raccolta SasHostParameterValue

SasHostParameterValue viene definito usando la sintassi dei file effetti (con estensione FX). Sebbene la sintassi sia molto simile alla sintassi dei file di effetti, esistono alcune differenze. Ad esempio, i tipi di oggetto, ad esempio Texture2D, Samplers e Strings, non sono validi nei file effettivi, ma sono validi in SasHostParameterValue. Un'applicazione host può implementare SasHostParameterValue in qualsiasi modo, purché sia conforme alla descrizione riportata di seguito. la definizione effettiva si trova nel file di inclusione degli effetti standard DXSAS ( \[ /Utilities/source/SAS/SAS.fxh radice SDK \] ).

Si noti che le matrici in SasHostParameterValue, ad esempio luci o fotocamere, hanno una lunghezza illimitata. Ciò significa che gli effetti possono essere associati a qualsiasi indice arbitrario in tali matrici e le applicazioni host devono fornire valori predefiniti significativi nei casi in cui non è possibile fornire alcun valore di applicazione.

Alcuni tipi e costanti devono essere definiti nell'inclusione standard DXSAS, come indicato nella definizione dell'inclusione standard. Ciò consente agli effetti di associare facilmente i valori aggregati da SasHostParameterValue a parametri di effetto strutturati.



| Raccolta SasHostParameterValue    | Tipo            | Membro                                       |
|-------------------------------------|-----------------|----------------------------------------------|
| [Time](#time)                       | float           | SAS. Time. Now                                 |
|                                     | float           | SAS. Time. Last                                |
|                                     | INT             | SAS. Time. NumeroFrame                         |
| [Mappa ambiente](#environment-map) | textureCUBE     | SAS. EnvironmentMap                           |
| [Fotocamera](#camera)                   | SasCamera       | SAS. camera                                   |
|                                     | float4x4        | SAS. camera. WorldToView                       |
|                                     | float4x4        | SAS. camera. Projection                        |
|                                     | float2          | SAS. camera. NearFarClipping                   |
| [Chiaro](#light)                     | SasAmbientLight | AmbientLight \[ ZeroOrMore \] ;                  |
|                                     | INT             | SAS. NumAmbientLights                         |
|                                     | SasAmbientLight | DirectionalLight \[ ZeroOrMore \] ;              |
|                                     | INT             | SAS. NumDirectionalLights                     |
|                                     | SasAmbientLight | PointLight \[ ZeroOrMore \] ;                    |
|                                     | INT             | SAS. NumPointLights                           |
|                                     | SasAmbientLight | \[ZeroOrMore Spotlight \] ;                     |
|                                     | INT             | SAS. NumSpotLights                            |
| [Shadow](#shadow)                   | float4x4        | ZeroOrMore SAS. \[ shadow \] . WorldToShadow       |
|                                     | texture2D       | ZeroOrMore SAS. \[ shadow \] . ShadowMap           |
| [Struttura](#skeleton)               | float4x4        | SAS. Skeleton. MeshToJointToWorld \[ OneOrMore\] |
|                                     | INT             | SAS. Skeleton. NumJoints                       |



 

### <a name="time"></a>Tempo

Valore dell'ora o dell'orologio virtuale dell'applicazione host. I membri includono:

-   SAS. Time. Now: valore del clock virtuale dell'applicazione host nel punto in cui verrà eseguito il rendering dell'effetto.
-   SAS. Time. Last: valore di Now al rendering precedente.
-   SAS. Time. NumeroFrame: valore del contatore che viene incrementato una volta per ogni frame sottoposto a rendering.

Gli effetti devono gestire correttamente il fatto che i valori di questi membri possono potenzialmente eseguire il wrapping durante i tempi di esecuzione estremamente lunghi. Ora e l'ultimo possono avere valori molto grandi.

### <a name="environment-map"></a>Mappa ambiente

Mappa dell'ambiente cubica. Se un effetto tenta di eseguire l'associazione a SAS. EnvironmentMap, le applicazioni host devono fornire una trama del cubo valida.

### <a name="camera"></a>Fotocamera

Fotocamera di cui è in corso il rendering. I membri includono:

-   SAS. camera. WorldToView: matrice di visualizzazione globale composita per la fotocamera.
-   SAS. camera. Projection: matrice di proiezione per la fotocamera.
-   SAS. camera. NearFarClipping: valori dei piani di ritaglio vicini e lontani.

### <a name="light"></a>Chiaro

Una o più luci della scena. La raccolta di luci viene dichiarata come una matrice in cui:

-   Color: colore RGB. Il valore predefinito è (0,0,0).
-   Direzione: direzione della luce. Il valore predefinito è (0,0,0).
-   Intervallo: distanza dalla luce in cui i raggi luminosi non hanno effetto sulla scena. Il valore predefinito è 0.
-   Theta: angolo del cono interno di un Spotlight, misurato in radianti. Il valore predefinito è 0.
-   Phi: angolo del cono esterno di un Spotlight, misurato in radianti. Il valore predefinito è 0.

Il numero di luci deve essere impostato sul numero di luci associate alla matrice associata. Gli effetti possono scegliere di ignorare il numero di luci e di associarle a qualsiasi elemento di una delle matrici chiare. Pertanto, le applicazioni host devono fornire un'associazione valida per gli elementi oltre il numero di spie nella matrice.

ZeroOrMore implica che la matrice può contenere un numero qualsiasi di elementi.

### <a name="shadow"></a>Ombreggiatura

Buffer Shadow che è costituito da:

-   WorldToShadow: matrice di matrici.
-   ShadowMap: file di trama 2D.

ZeroOrMore implica che la matrice può contenere un numero qualsiasi di elementi (zero indica una matrice vuota).

Un effetto dichiarerebbe un campionatore come segue:


```
texture2D Shadow 
<
  string SasBindAddress = "Sas.Shadow[0].ShadowMap";
>;

sampler ShadowSampler = shadow_sampler(Shadow);
```



### <a name="skeleton"></a>Struttura

Set di frame che costituiscono l'oggetto attualmente in fase di rendering. Gli esempi di frame sono Bones e Transforms. ad esempio:

-   MeshToJointToWorld: matrice di matrici.
-   NumJoints: numero di giunzioni nello scheletro.

OneOrMore implica che la matrice ha almeno un oggetto e può contenere un numero qualsiasi di elementi.

La definizione supporta sia gli oggetti mesh rigidi che quelli con skin usando lo stesso set di valori di [raccolta SasHostParameterValue](#sashostparametervalue-collection) con un'interpretazione diversa.

## <a name="sasbindaddress"></a>SasBindAddress

Questa annotazione viene aggiunta all'inizio di un file di effetti per associare un parametro di effetto al parametro corrispondente definito nella [raccolta SasHostParameterValue](#sashostparametervalue-collection). L'annotazione è dichiarata come segue:


```
string SasBindAddress = "SasHostParameterValue";
```



Questo esempio associa la matrice globale degli effetti alla matrice MeshToJointToWorld:


```
float4x3 World
<
  string SasBindAddress = "Sas.Skeleton.MeshToJointToWorld[0]";
>;
```



Questa annotazione indica all'applicazione host che è necessario impostare il valore della matrice globale degli effetti utilizzando i dati nella matrice MeshToJointToWorld.

La sintassi dell'annotazione dell'indirizzo di binding è stata definita molto simile alla sintassi usata da [**ID3DXEffect**](id3dxeffect.md) per ottenere e impostare i parametri di effetto. L'unica differenza tra la grammatica DXSAS e i metodi **ID3DXEffect** è l'aggiunta del token di indice asterisco. Di seguito è riportato un altro esempio di utilizzo dell'indice asterisco:


```
float3 LightColors[6]
<
  string SasBindAddress = "Sas.Light[*].Color";
>;
```



Il token di indice asterisco indica che tutti gli elementi della matrice di valori envirnmant host specifica (in questo caso il colore) devono essere associati nel parametro associato. Più token di indice asterisco consentono di associare effetti a sottoelementi di una matrice di strutture senza che sia necessario associare l'intera struttura. Questo esempio associa i valori dei colori delle prime sei luci a un parametro Effect.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla semantica e le annotazioni standard DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



