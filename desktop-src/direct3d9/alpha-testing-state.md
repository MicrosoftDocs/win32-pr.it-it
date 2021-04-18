---
description: Le applicazioni C++ possono usare il test alfa per controllare quando i pixel vengono scritti nell'area di destinazione di rendering.
ms.assetid: 368c3d12-2c8b-43e3-94c3-bccfe6c73e66
title: Stato test Alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020322ee31bc08352dbb2796ea5e7141d03c77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305061"
---
# <a name="alpha-testing-state-direct3d-9"></a>Stato test Alfa (Direct3D 9)

Le applicazioni C++ possono usare il test alfa per controllare quando i pixel vengono scritti nell'area di destinazione di rendering. Utilizzando lo stato di rendering [**\_ ALPHATESTENABLE di D3DRS**](./d3drenderstatetype.md) , l'applicazione imposta il dispositivo Direct3D corrente in modo che verifichi ogni pixel in base a una funzione di test alfa. Se il test ha esito positivo, il pixel viene scritto sulla superficie. In caso contrario, Direct3D ignora il pixel. Selezionare la funzione di test alfa con lo stato di rendering **\_ ALPHAFUNC di D3DRS** . L'applicazione può impostare un valore alfa di riferimento per tutti i pixel da confrontare utilizzando lo stato di rendering **\_ ALPHAREF di D3DRS** .

L'uso più comune per i test alfa è quello di migliorare le prestazioni durante la rasterizzazione di oggetti quasi trasparenti. Se i dati di colore da rasterizzare sono più opachi del colore in un determinato pixel (D3DPCMPCAPS \_ GREATEREQUAL), viene scritto il pixel. In caso contrario, il rasterizzatore ignora completamente il pixel, salvando l'elaborazione necessaria per fondere i due colori. Nell'esempio di codice seguente viene verificato se una determinata funzione di confronto è supportata e, in tal caso, vengono impostati i parametri della funzione di confronto necessari per migliorare le prestazioni durante il rendering.


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



Non tutti i componenti hardware supportano tutte le funzionalità di test alfa. È possibile controllare le funzionalità del dispositivo chiamando il metodo [**IDirect3D9:: GetDeviceCaps**](/windows/desktop/api) . Dopo aver recuperato le funzionalità del dispositivo, controllare il membro AlphaCmpCaps della struttura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) associata per la funzione di confronto desiderata. Se il membro AlphaCmpCaps contiene solo la \_ funzionalità D3DPCMPCAPS Always o solo la \_ funzionalità D3DPCMPCAPS mai, il driver non supporta i test alfa.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 
