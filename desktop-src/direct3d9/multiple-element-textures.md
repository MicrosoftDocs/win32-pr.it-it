---
description: Le trame tradizionali sono considerate trame a elemento singolo.
ms.assetid: 8fe8da80-0879-413a-a7db-617d2f558b28
title: Trame a più elementi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a434d1e6c6a892c794551aa0caf34890f3def9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303720"
---
# <a name="multiple-element-textures-direct3d-9"></a>Trame a più elementi (Direct3D 9)

Le trame tradizionali sono considerate trame a elemento singolo. Le trame a più elementi consentono alle applicazioni di scrivere simultaneamente su più elementi di una trama dalla pixel shader. Il risultato della successiva sessione di rendering è che un'applicazione può usare uno o più elementi come una trama a elemento singolo, ovvero come input per la pixel shader. Questi elementi aggiuntivi possono essere considerati come un archivio temporaneo per i risultati intermedi che verranno usati in un passaggio successivo da parte dell'applicazione.

La prima generazione di hardware che espone questa funzionalità presenta le restrizioni seguenti:

-   Tutte le superfici della trama a più elementi verranno allocate automaticamente. Questa limitazione viene affrontata trattandosi di un nuovo tipo di formato di superficie con più canali RGBA con interfoliazione.
-   Tutti gli elementi della trama a più elementi possono avere la stessa profondità del bit. Questa limitazione è espressa dal nome dei nuovi formati di superficie.
-   Una trama A più elementi non può essere la primaria/visualizzabile. In altre parole, deve essere solo fuori schermo. Questa limitazione è espressa dall'enumerazione del formato di superficie.
-   Non sono consentiti dithering, test alfa, Fogging, blending, raster-op o mascheramento. Non viene eseguita alcuna elaborazione post-pixel shader, ad eccezione del test z-test e dello stencil.
-   La trama non può essere un mipmap. La creazione della catena MIP avrà esito negativo.
-   Non è possibile impostare lo stesso elemento come trama nello stesso momento in cui si tratta di una destinazione di rendering. Tuttavia, elementi diversi della stessa superficie di trama a più elementi possono essere contemporaneamente trame e destinazioni di rendering.
-   Non è supportato l'anti-aliasing.
-   Le superfici della trama a più elementi, quando utilizzate come trama, non possono essere filtrate. Questa limitazione può essere verificata usando [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat).
-   Non è possibile bloccare le superfici della trama a più elementi.
-   È possibile utilizzare contemporaneamente più di una superficie di trama a più elementi assegnando ognuna alle varie fasi, come per le normali trame.
-   Le aree di trama a più elementi supportano la conversione di gamma dalla conversione da 2,2 a 1,0 in un'operazione di lettura, come per gli altri formati di trama.
-   Alcune implementazioni non applicano la maschera di scrittura di output (D3DRS \_ COLORWRITEENABLE). Quelli che possono avere maschere di scrittura a colori indipendenti. Viene espresso usando un nuovo bit di funzionalità. Il numero di maschere di scrittura a colori indipendenti disponibili sarà uguale al numero massimo di elementi di cui il dispositivo è in grado di supportare.
-   [**Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) Cancella tutti gli elementi della trama a più elementi impostati come destinazione di rendering.

L'utilizzo delle trame a più elementi segue questi passaggi:

1.  Le applicazioni individuano il supporto per questa funzionalità verificando la disponibilità dei formati di trama a più elementi.
2.  L'applicazione crea queste superfici chiamando [**createTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture).
3.  L'applicazione imposta la superficie come destinazione di rendering utilizzando la chiamata [**SetRenderTarget**](/windows/desktop/api) . Il pixel shader fornisce l'output alle superfici usando l'istruzione [MOV-PS](../direct3dhlsl/mov---ps.md) .
4.  Per impostare una superficie di trama a più elementi su una particolare fase, viene chiamato [**setexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) . Come per le altre trame, è possibile impostare la stessa superficie su più fasi contemporaneamente.
5.  [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) viene chiamato per impostare D3DSAMP \_ ELEMENTINDEX sul numero di elemento appropriato nella trama a più elementi dalla quale sono campionati gli esempi del campionatore. Il valore predefinito per questo stato è 0, il che significa che le trame non a più elementi funzioneranno. Se si imposta questo stato su un numero inappropriato, si ottiene un comportamento non definito, se la trama a più elementi è a due elementi di grandi dimensioni, ma al campionatore viene richiesto di eseguire il campionamento dal quarto elemento, ad esempio.

## <a name="api-support"></a>Supporto dell'API

Di seguito è riportato un riepilogo degli elementi API che supportano le trame a più elementi:

-   Il formato di superficie [D3DFMT \_ MULTi2 \_ ARGB8](d3dformat.md) esprime la natura Interleaved del formato.
-   Lo \_ stato del campionatore ELEMENTINDEX D3DSAMP indica quale indice dell'elemento utilizzare.
-   Gli Stati di rendering seguenti supportano le trame a più elementi:

    -   \_COLORWRITEENABLE1 D3DRS
    -   \_COLORWRITEENABLE2 D3DRS
    -   \_COLORWRITEENABLE3 D3DRS

    D3DRS \_ COLORWRITEENABLE si applica alla destinazione di rendering (o elemento) zero.

-   Il [flag \_ INDEPENDENTWRITEMASKS di D3DPMISCCAPS](d3dpmisccaps.md) indica che il dispositivo supporta le maschere di scrittura indipendenti per più trame degli elementi o più destinazioni di rendering.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline pixel](pixel-pipeline.md)
</dt> </dl>

 

 
