---
description: Quando il sistema esegue la funzione di fogging dei vertici, applica i calcoli del poligono a ogni vertice in un poligono e quindi interpola i risultati sulla faccia del poligono durante la rasterizzazione.
ms.assetid: 76989eb3-cd95-4dfc-ba0f-7563860b531c
title: VertexBie (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76196ba0489ac58529bcb5c0500a269c8ee27b87040ec96f64ef228377dc8abd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068977"
---
# <a name="vertex-fog-direct3d-9"></a>VertexBie (Direct3D 9)

Quando il sistema esegue la funzione di fogging dei vertici, applica i calcoli del poligono a ogni vertice in un poligono e quindi interpola i risultati sulla faccia del poligono durante la rasterizzazione. Gli effetti dell'effetto vertice sono calcolati dal motore di illuminazione e trasformazione Direct3D. Per altre informazioni, vedere [Parameters (Direct3D 9) .](fog-parameters.md)

Se l'applicazione non usa Direct3D per la trasformazione e l'illuminazione, l'applicazione deve eseguire calcoli in più. In questo caso, posizionare il fattore di riempimento calcolato nel componente alfa del colore speculare per ogni vertice. È possibile usare qualsiasi formula desiderata: basata su intervallo, volumetrica o altro. Direct3D usa il fattore di riempimento fornito per interpolare il viso di ogni poligono. Anche le applicazioni che eseguono la propria trasformazione e illuminazione devono eseguire i propri calcoli del vertice. Di conseguenza, un'applicazione di questo tipo deve solo abilitare la fusione e impostare il colore color attraverso gli stati di rendering associati, come descritto in Blending Di [Blending (Direct3D 9)](fog-blending.md) e [Color (Direct3D 9)](fog-color.md).

> [!Note]  
> Quando si usa un vertex shader, è necessario usare vertex shader. Questa operazione viene eseguita usando il vertex shader per scrivere l'intensità dell'intensità per vertice nel registro oFog. Al termine pixel shader, i dati oFog vengono usati per eseguire l'interpolazione lineare con il colore dei colori. Questa intensità non è disponibile in un pixel shader.

 

## <a name="range-based-fog"></a>Range-Based Unanimi

> [!Note]  
> Direct3D usa i calcoli di stile basato su intervalli solo quando si usa vertex con il motore di trasformazione e illuminazione Direct3D. Ciò è dovuto al fatto che pixel pixel pixel viene implementato nel driver di dispositivo e non esiste attualmente alcun hardware per supportare il dispositivo basato su intervalli per pixel. Se l'applicazione esegue la propria trasformazione e illuminazione, deve eseguire i propri calcoli, basati su intervalli o altro.

 

In alcuni casi, l'uso di affollamento può introdurre artefatti grafici che causano la fusione degli oggetti con il colore della tinta unita in modi non intuitivi. Si immagini, ad esempio, una scena in cui sono presenti due oggetti visibili: uno sufficientemente distante da essere interessato dal tatto e l'altro abbastanza vicino da non essere interessato. Se l'area di visualizzazione ruota sul posto, gli effetti apparenti possono cambiare, anche se gli oggetti sono stazionari. Il diagramma seguente mostra una visualizzazione dall'alto verso il basso di una situazione di questo tipo.

![diagramma di due punti di vista e del modo in cui influiscono sul modello per due oggetti](images/artifog.png)

La rappresentazione basata su intervalli è un altro modo, più accurato, per determinare gli effetti di questo effetto. Nell'ambiente basato su intervalli, Direct3D usa la distanza effettiva dal punto di vista a un vertice per i calcoli dei suoi giorni. Direct3D aumenta l'effetto dell'effetto dell'emisura con l'aumentare della distanza tra i due punti, anziché della profondità del vertice all'interno della scena, evitando così artefatti rotazionali.

Se il dispositivo corrente supporta il dispositivo basato su intervalli, imposterà il valore D3DPRASTERCAPSRANGE nel membro \_ RasterCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) quando si chiama il metodo [**IDirect3DDevice9::GetDeviceCaps.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) Per abilitare il modello basato su intervallo, impostare lo stato di rendering D3DRS \_ RANGEFOGENABLE su **TRUE.**

Il modello basato su intervalli viene calcolato da Direct3D durante la trasformazione e l'illuminazione. Anche le applicazioni che non usano il motore di trasformazione e illuminazione Direct3D devono eseguire i propri calcoli relativi al vertice. In questo caso, specificare il fattore di riempimento basato su intervalli nel componente alfa del componente speculare per ogni vertice.

## <a name="using-vertex-fog"></a>Uso di Vertex Coordinate

Usare la procedura seguente per abilitare vertex vertice nell'applicazione.

1.  Abilitare la fusione delle sfumature impostando D3DRS \_ FOGENABLE su **TRUE.**
2.  Impostare il colore dello stato di rendering \_ D3DRSCOLOR.
3.  Scegliere la formula desiderata impostando lo stato di rendering D3DRSBIEVERTEXMODE su un membro del \_ [**tipo enumerato D3DFOGMODE.**](./d3dfogmode.md)
4.  Impostare i parametri desiderati per la formula del colore selezionato negli stati di rendering.

L'esempio seguente, scritto in C++, mostra l'aspetto di questi passaggi nel codice.


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupVertexFog(DWORD Color, DWORD Mode, BOOL UseRange, FLOAT Density)
{
    float Start = 0.5f,    // Linear fog distances
          End   = 0.8f;
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if(D3DFOG_LINEAR == Mode)
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }

    // Enable range-based fog if desired (only supported for
    //   vertex fog). For this example, it is assumed that UseRange
    //   is set to a nonzero value only if the driver exposes the 
    //   D3DPRASTERCAPS_FOGRANGE capability.
    // Note: This is slightly more performance intensive
    //   than non-range-based fog.
    if(UseRange)
        g_pDevice->SetRenderState(D3DRS_RANGEFOGENABLE, TRUE);
}
```



Alcuni parametri sono obbligatori come valori a virgola mobile, anche se il metodo [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta solo valori DWORD nel secondo parametro. Questo esempio fornisce correttamente i valori a virgola mobile a questi metodi senza conversione dei dati eseguendo il cast degli indirizzi delle variabili a virgola mobile come puntatori DWORD e quindi dereferenziandoli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi Disami](fog-types.md)
</dt> </dl>

 

 
