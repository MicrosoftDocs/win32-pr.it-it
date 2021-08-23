---
description: Le mappe di spostamento sono simili alle mappe di trama, ma sono accessibili dal motore dei vertici.
ms.assetid: d6f16ff2-5a66-48a3-82c4-523faaafa6ae
title: Mapping spostamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87b559c2c4758b773c48c0b556b6d61af54549f1b30e5c2693a24c4c27856c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523766"
---
# <a name="displacement-mapping-direct3d-9"></a>Mapping spostamento (Direct3D 9)

Le mappe di spostamento sono simili alle mappe di trama, ma sono accessibili dal motore dei vertici.

## <a name="block-diagram"></a>Diagramma a blocchi

Nella parte iniziale della pipe del vertice è presente una fase di campionamento aggiuntiva, come illustrato nel diagramma seguente, che può campionare una mappa di spostamento per fornire dati di spostamento dei vertici.

![diagramma della fase del campionatore nella pipe del vertice](images/tessellatordx9.png)

Lo stato del campionatore della mappa di spostamento può essere impostato da [**SetSamplerState**](/windows/desktop/api) usando il numero di fase 256, che è un nuovo numero di fase. La trama della mappa di spostamento è impostata [**da SetTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)

La mappa può essere precampionata o meno, il che significa che può essere ordinata in modo da consentire la ricerca dei valori di spostamento senza filtrare.

-   Le mappe di spostamento sono analoghe alle mappe di trama, ma sono accessibili dal motore dei vertici.
-   Nella parte iniziale della pipe del vertice è presente una fase di campionamento aggiuntiva che può campionare una mappa di spostamento. Questa fase è accessibile dalla consueta API SetSamplerState, ma il numero di fase è D3DDMAPSAMPLER = 256.
-   Lo stato del campionatore della mappa di spostamento può essere impostato da SetSamplerState(D3DDMAPSAMPLER, ...) Api.
-   La trama della mappa di spostamento viene impostata dall'API SetTexture(D3DDMAPSAMPLER, texture).
-   La mappa può essere pre-campionata o meno. Ciò significa che può essere ordinato in un modo particolare che consente la ricerca dei valori di spostamento senza filtrare.
-   Le modifiche nella struttura della dichiarazione consentono di specificare la coordinata di trama usata per cercare la mappa di trama. Ad esempio, Stream0, Offset, FLOAT2, LOOKUP, Valore \_ spostamento. Questo indica al tessellatore di usare il vettore float 2D in stream0 in corrispondenza di un determinato offset come coordinata di trama per cercare la mappa di spostamento e associare la semantica di utilizzo del valore di \_ spostamento. La dichiarazione vertex shader conterrà una riga simile a {dcl texture0, v0} che indica che la semantica texture0 deve essere associata al registro di \_ input v0. Il valore di spostamento cercato viene copiato nel registro di input v0.
-   Esiste un tipo speciale di mapping di spostamento, quando la mappa di trama è pre-campionata. L'indice sequenziale dei vertici generati viene usato come coordinata di trama per una mappa di trama. Ad esempio, 0,0,(D3DDECLTYPE)0,D3DDECLMETHOD \_ LOOKUPPRESAMPLED, Usage, UsageIndex.
-   L'output della ricerca è 4 float.
-   Il mapping dello spostamento è supportato solo con le patch N.
-   I driver devono ignorare D3DDMAPSAMPLER in SetTextureStageState se non gestiscono le mappe di spostamento.
-   La modalità di filtro D3DTEXF \_ ANISOTROP non è supportata.
-   Quando D3DSAMP MIPFILTER nel campionatore della mappa di spostamento non è D3DTEXF NONE, il livello di dettaglio viene calcolato come segue (si noti che lo stato a tessellazione adattiva viene usato anche se \_ \_ D3DRS \_ ENABLEADAPTIVETESSELLATION è **FALSE**): Tmax = stato di rendering D3DRS \_ MAXTESSELLATIONLEVEL
-   Calcolare il livello te a tessellazione per un vertice Vi: (Xi, Yi, Zi) nello stesso modo descritto nella sezione "A tessiazione adattiva". Livello di dettaglio L = log2(Tmax) - log2 (Te).
-   Le operazioni di filtro e campionamento delle trame seguono le stesse regole applicate alla pipeline di pixel (distorsione del livello di dettaglio e così via).
-   Non tutti i formati possono essere usati come mappe di spostamento, ma solo quelli che supportano D3DUSAGE \_ DMAP. L'applicazione può eseguire una query con CheckDeviceFormat [**CheckDeviceFormat.**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
-   È necessario specificare D3DUSAGE \_ DMAP in [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) per notificare al driver che questa trama deve essere usata come mappa di spostamento.
-   D3DUSAGE \_ DMAP può essere usato solo con trame. Non può essere utilizzato con mappe di cubi o volumi.
-   Le trame e le destinazioni di rendering create con D3DUSAGE DMAP possono essere impostate in fasi di campionamento regolari \_ e come destinazioni di rendering.
-   Gli stati di rendering per impostare la modalità di ritorno a capo per le coordinate della trama vengono ignorati nel mapping di spostamento. In generale, non sono disponibili modalità di ritorno a capo per il motore a tessellatore.
-   Un campionatore mappa di spostamento ha un comportamento identico a quello dei campionatori di trama pixel. Se viene cercata una trama con meno di quattro canali (ad esempio R32f), i valori cercati passano ai canali appropriati del registro di destinazione (il registro di input del vertex shader contrassegnato con la semantica di esempio), mentre gli altri canali impostano per impostazione predefinita \_ (1, 1, 1). Quando viene cercato, D3DFMT L8 viene trasmesso nei canali R, G, B e A viene impostato sul valore \_ predefinito 1. L'rasterizzazione dei riferimenti contiene i dettagli completi dell'implementazione.

## <a name="pre-sampled-displacement-mapping"></a>Mapping di spostamento pre-campionato

-   È stato introdotto il nuovo stato del campionatore: D3DSAMP \_ DMAPOFFSET (DWORD) - offset (in vertici) in una mappa di spostamento pre-campionata.
-   È stato introdotto il nuovo metodo di dichiarazione D3DDECLMETHOD \_ LOOKUPPRESAMPLED.
-   La funzionalità a tessellazione adattiva deve essere disabilitata.
-   Le impostazioni del filtro della trama vengono ignorate. Il campionamento dei punti viene eseguito. Si presuppone che il filtro di trama mip sia D3DTEXF \_ NONE. Si presuppone che tutte le altre modalità di filtro della trama siano D3DTEXF \_ POINT.
-   Le coordinate della trama vengono calcolate come: U = (Index % TextureWidthInPixeles) / (float)(TextureWidthInPixeles) V = (Index/ TextureWidthInPixeles) / (float)(TextureHeightInPixeles) where Index is a sequential index of generated vertices plus TSS \[ D3DSAMP \_ DMAPOFFSET \] . L'indice sequenziale viene impostato su zero all'inizio di ogni primitiva e viene aumentato dopo la generazione di un vertice.

Queste sono le modifiche dell'API che supportano il mapping dello spostamento.

-   È stato aggiunto un formato a canale singolo, D3DFMT \_ L16.
-   Nuovo flag di utilizzo, D3DUSAGE \_ DMAP.
-   Una fase speciale della trama, usata per impostare una trama della mappa di spostamento, D3DDMAPSAMPLER.
-   Sono stati aggiunti nuovi limiti hardware, D3DDEVCAPS2 \_ DMAPNPATCH e D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH. Vedere [D3DDEVCAPS2.](d3ddevcaps2.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vertex Pipeline](vertex-pipeline.md)
</dt> </dl>

 

 
