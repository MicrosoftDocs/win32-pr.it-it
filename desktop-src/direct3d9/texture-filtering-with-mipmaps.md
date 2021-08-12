---
description: Una mipmap è una sequenza di trame, ognuna delle quali è una rappresentazione con risoluzione progressivamente inferiore della stessa immagine.
ms.assetid: b64abca9-0efb-4939-849d-e75a8d0dc10b
title: Filtro trame con Mipmap (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68f98c1189f130261981fdd309bb3f06bcca1e66f6e23a70e141a5abfe32f4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291650"
---
# <a name="texture-filtering-with-mipmaps-direct3d-9"></a>Filtro trame con Mipmap (Direct3D 9)

Una mipmap è una sequenza di trame, ognuna delle quali è una rappresentazione con risoluzione progressivamente inferiore della stessa immagine. L'altezza e la larghezza di ogni immagine, o livello, nella mappa mipmap è una potenza di due più piccola del livello precedente. Le mipmap non devono essere quadrate.

Un'immagine mipmap ad alta risoluzione viene usata per gli oggetti vicini all'utente. Le immagini a risoluzione inferiore vengono usate quando l'oggetto viene visualizzato più lontano. Mipmapping migliora la qualità delle trame sottoposte a rendering a scapito dell'uso di una maggiore quantità di memoria.

Direct3D rappresenta le mipmap come catena di superfici collegate. La trama con risoluzione più alta si trova nella parte superiore della catena e ha il livello successivo della mappa mipmap come allegato. A sua volta, tale livello ha un allegato che è il livello successivo nella mappa mipmap e così via, fino al livello di risoluzione più basso del mipmap.

Le illustrazioni seguenti illustrano un esempio di questi livelli. Le trame bitmap rappresentano un segno su un contenitore in un gioco in prima persona 3D. Quando viene creata come mipmap, la trama con la risoluzione più alta è la prima nel set. Ogni trama che ha esito positivo nel set mipmap è più piccola in altezza e larghezza di una potenza di 2. In questo caso, la mipmap con risoluzione massima è di 256 pixel per 256 pixel. La trama successiva è 128x128. L'ultima trama nella catena è 64x64.

Questo segno ha una distanza massima da cui è visibile. Se l'utente inizia lontano dal segno, il gioco visualizza la trama più piccola nella catena mipmap, che in questo caso la trama 64x64.

![illustrazione di una trama 64x64 di un segno di pericolo](images/mip1.jpg)

Quando l'utente sposta il punto di vista più vicino al segno, vengono usate trame con risoluzione progressivamente superiore nella catena mipmap. La risoluzione nella figura seguente è 128x128.

![illustrazione di una trama 128x128 di un segno di pericolo](images/mip2.jpg)

La trama con risoluzione più alta viene usata quando il punto di vista dell'utente è alla distanza minima consentita dal segno, come illustrato nella figura seguente.

![illustrazione di una trama 256x256 di un segno di pericolo](images/mip3.jpg)

Si tratta di un modo più efficiente per simulare la prospettiva per le trame. Anziché eseguire il rendering di una singola trama a molte risoluzioni, è più veloce usare più trame a risoluzioni variabili.

Direct3D può valutare quale trama in un set mipmap è la risoluzione più vicina all'output desiderato e può eseguire il mapping dei pixel nel relativo spazio texel. Se la risoluzione dell'immagine finale è compresa tra le risoluzioni delle trame nel set mipmap, Direct3D può esaminare i texel in entrambe le mipmap e sfumarne i valori di colore.

Per usare mipmap, l'applicazione deve compilare un set di mipmap. Le applicazioni applicano le mipmap selezionando il set mipmap come prima trama nel set di trame correnti. Per altre informazioni, vedere [Texture Blending (Direct3D 9)](texture-blending.md).

Successivamente, l'applicazione deve impostare il metodo di filtro utilizzato da Direct3D per campionare i texel. Il metodo più rapido per filtrare mipmap è fare in modo che Direct3D seleziona il texel più vicino. Usare il valore enumerato D3DTEXF \_ POINT per selezionarlo. Direct3D può produrre risultati di filtro migliori se l'applicazione usa il valore enumerato D3DTEXF \_ LINEAR. Viene selezionata la mipmap più vicina e quindi viene calcolata una media ponderata dei texel che circondano la posizione nella trama a cui viene mappato il pixel corrente.

Le trame Mipmap vengono usate nelle scene 3D per ridurre il tempo necessario per il rendering di una scena. Migliorano anche il realistico della scena. Tuttavia, spesso richiedono grandi quantità di memoria.

## <a name="creating-a-set-of-mipmaps"></a>Creazione di un set di mipmap

L'esempio seguente illustra come l'applicazione può chiamare il metodo [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) per compilare una catena di cinque livelli mipmap: 256x256, 128x128, 64x64, 32x32 e 16x16.


```
// This code example assumes that m_d3dDevice is a
// valid pointer to a IDirect3DDevice9 interface

IDirect3DTexture9 * pMipMap;
m_pD3DDevice->CreateTexture(256, 256, 5, 0, D3DFMT_R8G8B8, 
    D3DPOOL_MANAGED, &pMipMap);
```



I primi due parametri accettati da [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) sono le dimensioni e la larghezza della trama di primo livello. Il terzo parametro specifica il numero di livelli nella trama. Se si imposta questa proprietà su zero, Direct3D crea una catena di superfici, ognuna di due dimensioni inferiori a quella precedente, fino alla dimensione minima possibile di 1x1. Il quarto parametro specifica l'utilizzo per questa risorsa. In questo caso, viene specificato 0 per indicare l'assenza di un utilizzo specifico per la risorsa. Il quinto parametro specifica il formato della superficie per la trama. Usare un valore del [tipo enumerato D3DFORMAT](d3dformat.md) per questo parametro. Il sesto parametro specifica un membro del [**tipo enumerato D3DPOOL**](./d3dpool.md) che indica la classe di memoria in cui inserire la risorsa creata. A meno che non si utilizzino trame dinamiche, è consigliabile usare D3DPOOL \_ MANAGED. Il parametro finale accetta l'indirizzo di un puntatore a [**un'interfaccia IDirect3DTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)

> [!Note]  
> Ogni superficie in una catena mipmap ha dimensioni che sono metà della superficie precedente nella catena. Se il mipmap di primo livello ha dimensioni di 256x128, le dimensioni del mipmap di secondo livello sono 128x64, il terzo livello è 64x32 e così via, fino a 1x1. Non è possibile richiedere un numero di livelli mipmap in Livelli che causano una larghezza o un'altezza di qualsiasi mipmap nella catena inferiore a 1. Nel caso semplice di una superficie mipmap di primo livello 4x2, il valore massimo consentito per Livelli è tre. Le dimensioni di primo livello sono 4x2, le dimensioni di secondo livello sono 2x1 e le dimensioni per il terzo livello sono 1x1. Un valore maggiore di 3 in Livelli comporta un valore frazionario nell'altezza del mipmap di secondo livello e pertanto non è consentito.

 

## <a name="selecting-and-displaying-a-mipmap"></a>Selezione e visualizzazione di un mipmap

Chiamare il [**metodo IDirect3DDevice9::SetTexture**](/windows/desktop/api) per impostare il set di trame mipmap come prima trama nell'elenco delle trame correnti. Per altre informazioni, vedere [Texture Blending (Direct3D 9)](texture-blending.md).

Dopo che l'applicazione ha selezionato il set di trame mipmap, deve assegnare i valori del tipo enumerato [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) allo stato del \_ campionatore MIPFILTER D3DSAMP. Direct3D esegue quindi automaticamente il filtro delle trame mipmap. L'abilitazione del filtro trame mipmap è illustrata nell'esempio di codice seguente.


```
m_pD3DDevice->SetTexture(0, pMipMap);
m_pD3DDevice->SetSamplerState(0, D3DSAMP_MIPFILTER, D3DTEXF_POINT);
```



L'applicazione può anche attraversare manualmente una catena di superfici mipmap usando il metodo [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) e specificando il livello mipmap da recuperare. L'esempio seguente attraversa una catena mipmap dalle risoluzioni più alte a più basse.


```
IDirect3DSurface9 * pSurfaceLevel;
for (int iLevel = 0; iLevel < pMipMap->GetLevelCount(); iLevel++)
{
    pMipMap->GetSurfaceLevel(iLevel, &pSurfaceLevel);
    // Process this level
    pSurfaceLevel->Release();
}
```



Le applicazioni devono attraversare manualmente una catena mipmap per caricare i dati bitmap in ogni superficie della catena. Questo è in genere l'unico motivo per attraversare la catena. Un'applicazione può recuperare il numero di livelli in un mipmap chiamando [**IDirect3DBaseTexture9::GetLevelCount**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-getlevelcount).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtro trame](texture-filtering.md)
</dt> </dl>

 

 
