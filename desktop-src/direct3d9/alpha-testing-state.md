---
description: Le applicazioni C++ possono usare il test alfa per controllare quando i pixel vengono scritti nella superficie di destinazione del rendering.
ms.assetid: 368c3d12-2c8b-43e3-94c3-bccfe6c73e66
title: Stato di test alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b853eb779860d5fc490f4061fde03c852a9c3d9f7bda48baa8e5a84ebd43173c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989441"
---
# <a name="alpha-testing-state-direct3d-9"></a>Stato di test alfa (Direct3D 9)

Le applicazioni C++ possono usare il test alfa per controllare quando i pixel vengono scritti nella superficie di destinazione del rendering. Usando lo stato di rendering [**D3DRS \_ ALPHATESTENABLE,**](./d3drenderstatetype.md) l'applicazione imposta il dispositivo Direct3D corrente in modo da testare ogni pixel in base a una funzione di test alfa. Se il test ha esito positivo, il pixel viene scritto sulla superficie. In caso contrario, Direct3D ignora il pixel. Selezionare la funzione di test alfa con lo stato di rendering **D3DRS \_ ALPHAFUNC.** L'applicazione può impostare un valore alfa di riferimento per tutti i pixel da confrontare usando lo stato di rendering **\_ ALPHAREF D3DRS.**

L'uso più comune per i test alfa è migliorare le prestazioni quando si rasterizzano oggetti quasi trasparenti. Se i dati sui colori rasterizzati sono più opachi rispetto al colore in un determinato pixel (D3DPCMPCAPS \_ GREATEREQUAL), il pixel viene scritto. In caso contrario, il rasterizzatore ignora completamente il pixel, salvando l'elaborazione necessaria per unire i due colori. L'esempio di codice seguente verifica se una determinata funzione di confronto è supportata e, in tal caso, imposta i parametri della funzione di confronto necessari per migliorare le prestazioni durante il rendering.


```
// This code example assumes that pCaps is a
// D3DCAPS9 structure that was filled with a 
// previous call to IDirect3D9::GetDeviceCaps.

if (pCaps.AlphaCmpCaps & D3DPCMPCAPS_GREATEREQUAL)
{
    dev->SetRenderState(D3DRS_ALPHAREF, (DWORD)0x00000001);
    dev->SetRenderState(D3DRS_ALPHATESTENABLE, TRUE); 
    dev->SetRenderState(D3DRS_ALPHAFUNC, D3DCMP_GREATEREQUAL);
}

// If the comparison is not supported, render anyway. 
// The only drawback is no performance gain.
```



Non tutti i componenti hardware supportano tutte le funzionalità di test alfa. È possibile controllare le funzionalità del dispositivo chiamando il [**metodo IDirect3D9::GetDeviceCaps.**](/windows/desktop/api) Dopo aver recuperate le funzionalità del dispositivo, controllare il membro AlphaCmpCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) associata per la funzione di confronto desiderata. Se il membro AlphaCmpCaps contiene solo la funzionalità D3DPCMPCAPS ALWAYS o solo la funzionalità \_ D3DPCMPCAPS NEVER, il driver non supporta i test \_ alfa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 
