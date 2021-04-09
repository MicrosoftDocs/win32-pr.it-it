---
description: La nebbia dei pixel ottiene il nome dal fatto che viene calcolato in base ai singoli pixel nel driver di dispositivo.
ms.assetid: 6fcfb9fa-cacc-4dbc-bfc6-85d533dbfbf8
title: Nebbia pixel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f62a597820fa009207d8dda7836d161cdf34c88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875962"
---
# <a name="pixel-fog-direct3d-9"></a>Nebbia pixel (Direct3D 9)

La nebbia dei pixel ottiene il nome dal fatto che viene calcolato in base ai singoli pixel nel driver di dispositivo. Questa operazione è diversa dalla nebbia dei vertici, calcolata dalla pipeline durante i calcoli di trasformazione e illuminazione. La nebbia dei pixel è talvolta denominata nebbia della tabella perché alcuni driver usano una tabella di ricerca precalcolata per determinare il fattore di nebbia, usando la profondità di ogni pixel da applicare ai calcoli di fusione. Può essere applicato usando qualsiasi formula di nebbia identificata dai membri del tipo enumerato [**D3DFOGMODE**](./d3dfogmode.md) . Le implementazioni di queste formule sono specifiche del driver. Se un driver non supporta una formula di nebbia complessa, dovrebbe riportare una formula meno complessa.

## <a name="eye-relative-vs-z-based-depth"></a>Profondità basata su Eye-Relative rispetto a Z

Per alleviare gli artefatti grafici correlati alla nebbia causati da una distribuzione non uniforme di valori z in un buffer di profondità, la maggior parte dei dispositivi hardware usa la profondità relativa agli occhi anziché i valori di profondità basati su z per la nebbia dei pixel. La profondità relativa agli occhi è essenzialmente l'elemento w da un set di coordinate omogeneo. Microsoft Direct3D accetta il reciproco dell'elemento RHW da un set di coordinate dello spazio del dispositivo per riprodurre true w. Se un dispositivo supporta la nebbia relativa agli occhi, imposta il flag **D3DPRASTERCAPS \_ WFOG** nel membro RasterCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) quando si chiama il metodo [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) . Fatta eccezione per l'unità di rasterizzazione dei riferimenti, i dispositivi software utilizzano sempre z per calcolare gli effetti della nebbia dei pixel.

Quando la nebbia relativa agli occhi è supportata, il sistema usa automaticamente la profondità relativa agli occhi anziché la profondità basata sulla z Se la matrice di proiezione fornita produce valori z nello spazio globale equivalenti ai valori w nello spazio del dispositivo. È possibile impostare la matrice di proiezione chiamando il metodo [**IDirect3DDevice9:: setransform**](/windows/desktop/api) , usando il \_ valore di proiezione D3DTS e passando una struttura [**D3DMATRIX**](d3dmatrix.md) che rappresenta la matrice desiderata. Se la matrice di proiezione non è conforme a questo requisito, gli effetti di nebbia non vengono applicati correttamente. Per informazioni dettagliate sulla creazione di una matrice conforme, vedere [trasformazione della proiezione (Direct3D 9)](projection-transform.md).

Direct3D usa la matrice di proiezione attualmente impostata nei calcoli di profondità basati su w. Di conseguenza, un'applicazione deve impostare una matrice di proiezione conforme per ricevere le funzionalità basate su w desiderate, anche se non utilizza la pipeline di trasformazione Direct3D.

Direct3D controlla la quarta colonna della matrice di proiezione. Se i coefficienti sono \[ 0, 0, 0, 1 \] (per una proiezione affine), il sistema utilizzerà valori di profondità basati su z per la nebbia. In questo caso, è necessario specificare anche le distanze di inizio e fine per gli effetti di nebbia lineare nello spazio del dispositivo, che varia da 0,0 al punto più vicino all'utente e 1,0 al punto più lontano.

## <a name="using-pixel-fog"></a>Uso della nebbia pixel

Usare la procedura seguente per abilitare la nebbia dei pixel nell'applicazione.

1.  Abilitare la fusione di nebbia impostando lo \_ stato di rendering FOGENABLE di D3DRS su **true**.
2.  Impostare il colore di nebbia desiderato nello \_ stato di rendering FogColor di D3DRS.
3.  Scegliere la formula di nebbia da usare impostando lo \_ stato di rendering FOGTABLEMODE di D3DRS sul membro corrispondente del tipo enumerato [**D3DFOGMODE**](./d3dfogmode.md) .
4.  Impostare i parametri di nebbia come desiderato per la modalità di nebbia selezionata negli Stati di rendering associati. Sono incluse le distanze iniziale e finale per la nebbia lineare e la densità di nebbia per la modalità di nebbia esponenziale.

Nell'esempio seguente vengono illustrati i passaggi che possono essere simili nel codice.


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupPixelFog(DWORD Color, DWORD Mode)
{
    float Start   = 0.5f;    // For linear mode
    float End     = 0.8f;
    float Density = 0.66f;   // For exponential modes
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if( Mode == D3DFOG_LINEAR )
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }
```



Alcuni parametri di nebbia sono necessari come valori a virgola mobile, anche se il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta solo valori DWORD nel secondo parametro. Nell'esempio precedente vengono forniti i valori a virgola mobile in **IDirect3DDevice9:: SetRenderState** senza conversione dei dati eseguendo il cast degli indirizzi delle variabili a virgola mobile come puntatori DWORD, quindi dereferenziarli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di nebbia](fog-types.md)
</dt> </dl>

 

 
