---
description: Le mappe di spostamento sono simili alle mappe di trama, ma sono accessibili dal motore di vertici.
ms.assetid: d6f16ff2-5a66-48a3-82c4-523faaafa6ae
title: Mapping di spostamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b687583b0109223d8c2dac807425e235ddf280e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482077"
---
# <a name="displacement-mapping-direct3d-9"></a>Mapping di spostamento (Direct3D 9)

Le mappe di spostamento sono simili alle mappe di trama, ma sono accessibili dal motore di vertici.

## <a name="block-diagram"></a>Diagramma a blocchi

Una fase del campionatore aggiuntiva è presente nella parte iniziale della pipe dei vertici, come illustrato nel diagramma seguente, in cui è possibile campionare una mappa di spostamento per fornire i dati di spostamento del vertice.

![diagramma della fase del campionatore nella pipe del vertice](images/tessellatordx9.png)

Lo stato del campionatore della mappa di spostamento può essere impostato da [**SetSamplerState**](/windows/desktop/api) usando la fase numero 256, che è un nuovo numero di fase. La trama della mappa di spostamento viene impostata da [**texture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).

La mappa può essere precampionata o meno, il che significa che può essere ordinata in modo da consentire la ricerca dei valori di spostamento senza filtrare.

-   Le mappe di spostamento sono analoghe alle mappe di trama, ma sono accessibili dal motore di vertici.
-   Una fase del campionatore aggiuntiva è presente nella parte iniziale della pipe dei vertici che può campionare una mappa di spostamento. Questa fase è accessibile dalla consueta API SetSamplerState, ma il numero di fase è D3DDMAPSAMPLER = 256.
-   Lo stato del campionatore della mappa di spostamento può essere impostato da SetSamplerState (D3DDMAPSAMPLER,...) API.
-   La trama della mappa di spostamento viene impostata dall'API setrame (D3DDMAPSAMPLER, texture).
-   La mappa può essere pre-campionata o meno. Ciò significa che può essere ordinato in un modo specifico che consente la ricerca dei valori di spostamento senza filtro.
-   Le modifiche nella struttura della dichiarazione consentono la specifica della coordinata di trama utilizzata per cercare la mappa della trama. Ad esempio, Stream0, offset, FLOAT2, LOOKUP, valore di spostamento \_ . Ciò indica a mosaico di usare il vettore float 2D in stream0 in un determinato offset come coordinata di trama per cercare la mappa di spostamento e associare la relativa \_ semantica di utilizzo al valore di spostamento. La dichiarazione vertex shader contiene una riga simile a {DCL \_ Texture0, V0} che indica che la semantica Texture0 deve essere associata al registro di input V0. Il valore di spostamento cercato viene copiato nel registro di input V0.
-   È disponibile un tipo speciale di mapping di spostamento, quando la mappa di trama è pre-campionata. L'indice sequenziale dei vertici generati viene usato come coordinata di trama a una mappa di trama. Ad esempio, 0, 0, (D3DDECLTYPE) 0, D3DDECLMETHOD \_ LOOKUPPRESAMPLED, Usage, UsageIndex.
-   L'output della ricerca è 4 float.
-   Il mapping di spostamento è supportato solo con N-patch.
-   I driver devono ignorare D3DDMAPSAMPLER in SetTextureStageState se non gestiscono le mappe di spostamento.
-   \_La modalità filtro D3DTEXF anisotropico non è supportata.
-   Quando D3DSAMP \_ MIPFILTER nel campionatore della mappa di spostamento non è D3DTEXF \_ nessuno, il livello di dettaglio viene calcolato come segue (si noti che lo stato del mosaico adattivo viene usato anche se D3DRS \_ ENABLEADAPTIVETESSELLATION è **false**): tmax = render state D3DRS \_ MAXTESSELLATIONLEVEL
-   Livello mosaico di calcolo te per un vertice vi: (XI, Yi, Zi) come descritto nella sezione "mosaico adattivo". Livello di dettaglio L = log2 (tmax)-log2 (te).
-   Le operazioni di filtro e campionamento della trama seguono le stesse regole della pipeline pixel (il livello di dettaglio (LOD) viene applicato e così via).
-   Non tutti i formati possono essere usati come mappe di spostamento, ma solo quelli che supportano il \_ DMAP D3DUSAGE. L'applicazione può eseguire una query con il [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)CheckDeviceFormat.
-   \_È necessario specificare D3DUSAGE DMAP in [**createTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) per notificare al driver che questa trama deve essere utilizzata come mappa di spostamento.
-   D3DUSAGE \_ DMAP può essere usato solo con le trame. Non può essere utilizzato con mappe o volumi del cubo.
-   Le trame e le destinazioni di rendering create con D3DUSAGE \_ DMAP possono essere impostate in fasi normali del campionatore e come destinazioni di rendering.
-   Gli Stati di rendering per impostare la modalità di wrapping per le coordinate di trama vengono ignorati nel mapping di spostamento. In generale, non sono disponibili modalità a capo per il motore mosaico.
-   Un Sampler della mappa di spostamento presenta un comportamento identico a quello dei campionatori di trama pixel. Se viene cercata una trama con meno di quattro canali (ad esempio R32f), i valori di ricerca vengono indirizzati ai canali appropriati del registro di destinazione (il registro di input del vertex shader contrassegnato con la \_ semantica di esempio), mentre gli altri canali vengono predefiniti (1, 1, 1). Una volta cercato, D3DFMT \_ L8 viene trasmesso nei canali R, G, B e un valore predefinito è 1. L'rasterizzazione dei riferimenti presenta i dettagli di implementazione completi.

## <a name="pre-sampled-displacement-mapping"></a>Mapping di spostamento pre-campionato

-   Viene introdotto il nuovo stato del campionatore: D3DSAMP \_ DMAPOFFSET (DWORD)-offset (in vertici) in una mappa di spostamento pre-campionata.
-   È stato introdotto il nuovo metodo di dichiarazione: D3DDECLMETHOD \_ LOOKUPPRESAMPLED.
-   Il mosaico adattivo deve essere disabilitato.
-   Le impostazioni del filtro di trama vengono ignorate. Il campionamento di punti è terminato. Si presuppone che il filtro di trama MIP sia D3DTEXF \_ None. Si presuppone che tutte le altre modalità di filtro di trama siano D3DTEXF \_ punto.
-   Le coordinate di trama vengono calcolate come: U = (indice% TextureWidthInPixeles)/(float) (TextureWidthInPixeles) V = (index/TextureWidthInPixeles)/(float) (TextureHeightInPixeles) dove index è un indice sequenziale dei vertici generati più TSS \[ D3DSAMP \_ DMAPOFFSET \] . L'indice sequenziale è impostato su zero all'inizio di ogni primitiva e viene aumentato dopo la generazione di un vertice.

Si tratta delle modifiche apportate all'API che supportano il mapping di spostamento.

-   È stato aggiunto un solo formato di canale, D3DFMT \_ L16.
-   Un nuovo flag di utilizzo, D3DUSAGE \_ dmap.
-   Una fase di trama speciale, utilizzata per impostare una trama della mappa di spostamento, D3DDMAPSAMPLER.
-   Sono stati aggiunti nuovi tappi hardware, D3DDEVCAPS2 \_ DMAPNPATCH e D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH. Vedere [D3DDEVCAPS2](d3ddevcaps2.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline Vertex](vertex-pipeline.md)
</dt> </dl>

 

 
