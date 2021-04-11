---
description: Quando il sistema esegue l'offuscamento dei vertici, applica i calcoli di nebbia a ogni vertice in un poligono, quindi interpola i risultati sulla superficie del poligono durante la rasterizzazione.
ms.assetid: 76989eb3-cd95-4dfc-ba0f-7563860b531c
title: Nebbia vertice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35cd880bda7ebffd36bd95bec5f8565e104eaa15
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123336"
---
# <a name="vertex-fog-direct3d-9"></a>Nebbia vertice (Direct3D 9)

Quando il sistema esegue l'offuscamento dei vertici, applica i calcoli di nebbia a ogni vertice in un poligono, quindi interpola i risultati sulla superficie del poligono durante la rasterizzazione. Gli effetti della nebbia dei vertici vengono calcolati dal motore di illuminazione e trasformazione Direct3D. Per altre informazioni, vedere [parametri di nebbia (Direct3D 9)](fog-parameters.md).

Se l'applicazione non usa Direct3D per la trasformazione e l'illuminazione, l'applicazione deve eseguire calcoli di nebbia. In questo caso, inserire il fattore di nebbia calcolato nel componente alfa del colore speculare per ogni vertice. È possibile utilizzare le formule desiderate, in base all'intervallo, al volume volumetrico o in altro modo. Direct3D usa il fattore di nebbia fornito per l'interpolazione tra la faccia di ogni poligono. Anche le applicazioni che eseguono la trasformazione e l'illuminazione devono eseguire i propri calcoli relativi alla nebbia dei vertici. Di conseguenza, un'applicazione di questo tipo deve abilitare solo la fusione di nebbia e impostare il colore di nebbia tramite gli Stati di rendering associati, come descritto in [blending di nebbia (Direct3D 9)](fog-blending.md) e [nebbia color (Direct3D 9)](fog-color.md).

> [!Note]  
> Quando si usa un vertex shader, è necessario usare la nebbia del vertice. Questa operazione viene eseguita usando vertex shader per scrivere l'intensità di nebbia per vertice nel registro oFog. Al termine dell'pixel shader, i dati oFog vengono usati per eseguire l'interpolazione lineare con il colore di nebbia. Questa intensità non è disponibile in un pixel shader.

 

## <a name="range-based-fog"></a>Nebbia Range-Based

> [!Note]  
> Direct3D usa calcoli di nebbia basati su intervallo solo quando si usa la nebbia dei vertici con il motore di trasformazione e illuminazione Direct3D. Questo perché la nebbia dei pixel è implementata nel driver di dispositivo e attualmente non esiste alcun hardware per supportare la nebbia basata sull'intervallo per pixel. Se l'applicazione esegue una trasformazione e un'illuminazione proprie, deve eseguire i propri calcoli di nebbia, basati sull'intervallo o in altro modo.

 

In alcuni casi, l'utilizzo di fog può introdurre artefatti grafici che comportano la fusione di oggetti con il colore di nebbia in modi non intuitivi. Si supponga, ad esempio, una scena in cui sono presenti due oggetti visibili: uno abbastanza distante per essere influenzato dalla nebbia e l'altro sufficientemente vicino a non essere interessato. Se l'area di visualizzazione ruota sul posto, gli effetti di nebbia evidenti possono cambiare anche se gli oggetti sono stazionari. Il diagramma seguente mostra una visualizzazione dall'alto verso il basso di una situazione di questo tipo.

![diagramma di due punti di vista e del modo in cui influiscono sulla nebbia per due oggetti](images/artifog.png)

La nebbia basata sull'intervallo è un altro metodo, più accurato, per determinare gli effetti di nebbia. Nella nebbia basata sull'intervallo, Direct3D usa la distanza effettiva dal punto di vista a un vertice per i calcoli di nebbia. Direct3D aumenta l'effetto della nebbia Man mano che la distanza tra i due punti aumenta, anziché la profondità del vertice all'interno della scena, evitando così gli artefatti rotazionali.

Se il dispositivo corrente supporta la nebbia basata sull'intervallo, verrà impostato il \_ valore D3DPRASTERCAPS FOGRANGE nel membro RasterCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) quando si chiama il metodo [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) . Per abilitare la nebbia basata sull'intervallo, impostare lo \_ stato di rendering RANGEFOGENABLE di D3DRS su **true**.

La nebbia basata sull'intervallo viene calcolata da Direct3D durante la trasformazione e l'illuminazione. Le applicazioni che non usano il motore di trasformazione e di illuminazione Direct3D devono anche eseguire i propri calcoli relativi alla nebbia dei vertici. In questo caso, fornire il fattore di nebbia basato sull'intervallo nel componente alfa del componente speculare per ogni vertice.

## <a name="using-vertex-fog"></a>Uso della nebbia del vertice

Usare la procedura seguente per abilitare la nebbia dei vertici nell'applicazione.

1.  Abilitare la fusione di nebbia impostando D3DRS \_ FOGENABLE su **true**.
2.  Impostare il colore di nebbia nello \_ stato di rendering FogColor di D3DRS.
3.  Scegliere la formula di nebbia desiderata impostando lo \_ stato di rendering FOGVERTEXMODE di D3DRS su un membro del tipo enumerato [**D3DFOGMODE**](./d3dfogmode.md) .
4.  Impostare i parametri di nebbia come desiderato per la formula di nebbia selezionata negli Stati di rendering.

Nell'esempio seguente, scritto in C++, viene illustrato il modo in cui questi passaggi potrebbero essere simili nel codice.


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



Alcuni parametri di nebbia sono necessari come valori a virgola mobile, anche se il metodo [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) accetta solo valori DWORD nel secondo parametro. Questo esempio fornisce correttamente i valori a virgola mobile a questi metodi senza conversione dei dati eseguendo il cast degli indirizzi delle variabili a virgola mobile come puntatori DWORD, quindi dereferenziarli.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di nebbia](fog-types.md)
</dt> </dl>

 

 
