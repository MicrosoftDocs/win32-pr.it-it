---
description: Un mipmap è una sequenza di trame, ognuna delle quali è una rappresentazione di risoluzione progressivamente inferiore della stessa immagine.
ms.assetid: b64abca9-0efb-4939-849d-e75a8d0dc10b
title: Filtraggio delle trame con mipmap (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc109ae6de93a26b5d5e5b90e948761e92ee92c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104561441"
---
# <a name="texture-filtering-with-mipmaps-direct3d-9"></a>Filtraggio delle trame con mipmap (Direct3D 9)

Un mipmap è una sequenza di trame, ognuna delle quali è una rappresentazione di risoluzione progressivamente inferiore della stessa immagine. L'altezza e la larghezza di ogni immagine, o livello, in mipmap sono una potenza di due dimensioni inferiori al livello precedente. Non è necessario che mipmap sia quadrato.

Per gli oggetti vicini all'utente viene utilizzata un'immagine mipmap ad alta risoluzione. Le immagini con risoluzione inferiore vengono utilizzate quando l'oggetto viene visualizzato più lontano. Mapping MIP migliora la qualità delle trame di cui è stato eseguito il rendering a scapito dell'utilizzo di più memoria.

Direct3D rappresenta mipmap come una catena di superfici collegate. La trama con la risoluzione più elevata si trova all'inizio della catena e ha il livello successivo del mipmap come allegato. A sua volta, tale livello ha un allegato che rappresenta il livello successivo in mipmap e così via, fino al livello di risoluzione più basso di mipmap.

Le illustrazioni seguenti mostrano un esempio di questi livelli. Le trame bitmap rappresentano un segno di un contenitore in un gioco di prima persona 3D. Quando viene creato come mipmap, la trama con la risoluzione più alta è la prima nel set. Ogni trama successiva nel set di mipmap è più piccola in altezza e larghezza per una potenza di 2. In questo caso, la mipmap di risoluzione massima è 256 pixel di 256 pixel. La trama successiva è 128x128. L'ultima trama nella catena è 64x64.

Questo segno ha una distanza massima da cui è visibile. Se l'utente inizia a distanza dal segno, il gioco Visualizza la trama più piccola nella catena mipmap, che in questo caso è la trama 64x64.

![illustrazione di una trama 64x64 di un segno di pericolo](images/mip1.jpg)

Quando l'utente sposta il punto di vista più vicino al segno, vengono usate trame a risoluzione progressiva più elevata nella catena mipmap. La risoluzione nella figura seguente è 128x128.

![illustrazione di una trama 128x128 di un segno di pericolo](images/mip2.jpg)

La trama con la risoluzione più elevata viene utilizzata quando il punto di visualizzazione dell'utente è alla distanza minima consentita dal segno, come illustrato nella figura seguente.

![illustrazione di una trama 256x256 di un segno di pericolo](images/mip3.jpg)

Si tratta di un modo più efficiente per simulare la prospettiva per le trame. Anziché eseguire il rendering di una singola trama a molte risoluzioni, è più veloce usare più trame con diverse risoluzioni.

Direct3D può valutare quale trama in un set di mipmap è la risoluzione più vicina all'output desiderato ed è in grado di mappare i pixel nello spazio Texel. Se la risoluzione dell'immagine finale è compresa tra le risoluzioni delle trame nel set di mipmap, Direct3D può esaminare i Texel in entrambi i mipmap e fondere i valori dei colori.

Per usare mipmap, l'applicazione deve compilare un set di mipmap. Le applicazioni applicano mipmap selezionando il mipmap impostato come prima trama nel set di trame correnti. Per altre informazioni, vedere [blending di trame (Direct3D 9)](texture-blending.md).

Successivamente, l'applicazione deve impostare il metodo di filtro usato da Direct3D per campionare Texel. Il metodo più veloce per filtrare mipmap consiste nel fare in modo che Direct3D selezioni il Texel più vicino. Usare il \_ valore enumerato Point D3DTEXF per selezionare questa. Direct3D può produrre risultati di filtro migliori se l'applicazione usa il \_ valore enumerato D3DTEXF lineare. Viene selezionato il mipmap più vicino, quindi viene calcolata una media ponderata dei Texel che circonda la posizione nella trama a cui viene eseguito il mapping del pixel corrente.

Le trame mipmap vengono usate nelle scene 3D per ridurre il tempo necessario per eseguire il rendering di una scena. Inoltre, migliorano il realismo della scena. Tuttavia, spesso richiedono grandi quantità di memoria.

## <a name="creating-a-set-of-mipmaps"></a>Creazione di un set di mipmap

L'esempio seguente mostra come l'applicazione può chiamare il metodo [**IDirect3DDevice9:: createTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) per compilare una catena di cinque livelli mipmap: 256x256, 128x128, 64x64, 32x32 e 16x16.


```
// This code example assumes that m_d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface

IDirect3DTexture9 * pMipMap;
m_pD3DDevice->CreateTexture(256, 256, 5, 0, D3DFMT_R8G8B8, 
    D3DPOOL_MANAGED, &pMipMap);
```



I primi due parametri accettati da [**IDirect3DDevice9:: createTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) sono le dimensioni e la larghezza della trama di primo livello. Il terzo parametro specifica il numero di livelli nella trama. Se si imposta questo valore su zero, Direct3D crea una catena di superfici, ciascuna con una potenza di due minore di quella precedente, fino alla dimensione minima possibile di 1x1. Il quarto parametro specifica l'utilizzo della risorsa. in questo caso, viene specificato 0 per indicare nessun utilizzo specifico per la risorsa. Il quinto parametro specifica il formato di superficie per la trama. Usare un valore dal tipo enumerato [D3DFORMAT](d3dformat.md) per questo parametro. Il sesto parametro specifica un membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) che indica la classe di memoria in cui inserire la risorsa creata. A meno che non si stiano usando trame dinamiche, \_ è consigliabile gestire D3DPOOL. Il parametro finale accetta l'indirizzo di un puntatore a un'interfaccia [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .

> [!Note]  
> Ogni superficie in una catena mipmap ha dimensioni che sono una metà della superficie precedente della catena. Se il mipmap di primo livello ha dimensioni di con dimensioni 256x128, le dimensioni del mipmap di secondo livello sono 128x64, il terzo livello è 64x32 e così via, fino a 1x1. Non è possibile richiedere un numero di livelli di mipmap in livelli che causerebbero la larghezza o l'altezza di qualsiasi mipmap nella catena inferiore a 1. Nel caso più semplice di una superficie mipmap di primo livello 4x2, il valore massimo consentito per i livelli è tre. Le dimensioni di primo livello sono 4x2, le dimensioni di secondo livello sono 2x1 e le dimensioni del terzo livello sono 1x1. Un valore maggiore di 3 in livelli restituisce un valore frazionario nell'altezza del mipmap di secondo livello e pertanto non è consentito.

 

## <a name="selecting-and-displaying-a-mipmap"></a>Selezione e visualizzazione di un mipmap

Chiamare il metodo [**IDirect3DDevice9:: setexture**](/windows/desktop/api) per impostare il set di trame mipmap come prima trama nell'elenco delle trame correnti. Per altre informazioni, vedere [blending di trame (Direct3D 9)](texture-blending.md).

Dopo che l'applicazione ha selezionato il set di trama mipmap, deve assegnare i valori dal tipo enumerato [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) allo \_ stato del campionatore MIPFILTER D3DSAMP. Direct3D esegue quindi automaticamente il filtro della trama mipmap. L'abilitazione del filtro della trama mipmap è illustrata nell'esempio di codice seguente.


```
m_pD3DDevice->SetTexture(0, pMipMap);
m_pD3DDevice->SetSamplerState(0, D3DSAMP_MIPFILTER, D3DTEXF_POINT);
```



L'applicazione può anche attraversare manualmente una catena di superfici mipmap usando il metodo [**IDirect3DTexture9:: GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) e specificando il livello mipmap da recuperare. Nell'esempio seguente viene attraversata una catena mipmap dalla risoluzione più alta alla più bassa.


```
IDirect3DSurface9 * pSurfaceLevel;
for (int iLevel = 0; iLevel < pMipMap->GetLevelCount(); iLevel++)
{
    pMipMap->GetSurfaceLevel(iLevel, &pSurfaceLevel);
    // Process this level
    pSurfaceLevel->Release();
}
```



Le applicazioni devono attraversare manualmente una catena mipmap per caricare i dati bitmap in ogni superficie della catena. Si tratta in genere dell'unico motivo per attraversare la catena. Un'applicazione può recuperare il numero di livelli in un mipmap chiamando [**IDirect3DBaseTexture9:: GetLevelCount**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-getlevelcount).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtraggio trama](texture-filtering.md)
</dt> </dl>

 

 
