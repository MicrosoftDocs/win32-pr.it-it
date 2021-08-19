---
description: Nella pipeline dei vertici della funzione fissa, l'elaborazione dei vertici in un buffer dei vertici applica le matrici di trasformazione correnti per il dispositivo.
ms.assetid: a882a5c5-b05e-4659-9040-92d3e2ccd89c
title: Elaborazione dei vertici delle funzioni fisse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827a293a4fbd552327d93076de773aec90dbd895faf3c086f4794036978984fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988021"
---
# <a name="fixed-function-vertex-processing-direct3d-9"></a>Elaborazione dei vertici delle funzioni fisse (Direct3D 9)

Nella pipeline dei vertici della funzione fissa, l'elaborazione dei vertici in un buffer dei vertici applica le matrici di trasformazione correnti per il dispositivo. È anche possibile applicare operazioni sui vertici, ad esempio illuminazione, generazione di flag di ritaglio ed extent di aggiornamento, facoltativamente. Quando si usa l'elaborazione dei vertici di funzione fissa, la modifica degli elementi nel vertex buffer di destinazione è controllata dal flag [ \_ DONOTCOPYDATA D3DPV.](other-direct3d-constants.md) Questo flag si applica solo all'elaborazione dei vertici delle funzioni fisse. [**L'interfaccia IDirect3DDevice9**](/windows/desktop/api) espone il metodo [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) per elaborare i vertici. È possibile elaborare i vertici da un vertex shader al set di flussi di dati di input, generando un singolo flusso di dati dei vertici interleaved nel vertex buffer di destinazione chiamando il metodo **IDirect3DDevice9::P rocessVertices.** Il metodo accetta cinque parametri che descrivono la posizione e la quantità di vertici a cui il metodo è destinato, il vertex buffer di destinazione e le opzioni di elaborazione. Dopo la chiamata, il buffer di destinazione contiene i dati dei vertici elaborati.

Il primo, il secondo e il terzo parametro, SrcStartIndex, DestIndex e VertexCount, riflettono rispettivamente l'indice del primo vertice da caricare, l'indice all'interno del buffer di destinazione in cui verranno inseriti i vertici e il numero totale di vertici da elaborare e inserire rispettivamente nel buffer di destinazione. Il quarto parametro, pDestBuffer, deve essere impostato sull'indirizzo dell'interfaccia [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) dell'oggetto vertex buffer che riceverà i vertici di origine. Il parametro SrcStartIndex specifica l'indice in corrispondenza del quale il metodo deve avviare l'elaborazione dei vertici.

Il parametro finale, Flags, determina le opzioni di elaborazione speciali per il metodo. È possibile impostare questo parametro su 0 per l'elaborazione dei vertici predefinita o su [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) per ottimizzare l'elaborazione in alcune situazioni. È anche possibile combinare il valore D3DPV DONOTCOPYDATA con uno o più \_ [valori D3DLOCK](d3dlock.md) appropriati per il buffer di destinazione. Quando si imposta Flag su 0, i componenti dei vertici del formato dei vertici del vertex buffer di destinazione non interessati dall'operazione di vertice vengono comunque copiati dal vertex shader o impostati su 0. Tuttavia, quando si usa D3DPV \_ DONOTCOPYDATA, [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) non sovrascrive le informazioni sul colore e sulle coordinate della trama nel buffer di destinazione a meno che questi dati non vengano generati da Direct3D. Il colore diffuso viene generato quando l'illuminazione è abilitata, vale a significa che D3DRS \_ LIGHTING è impostato su **TRUE.** Il colore speculare viene generato quando l'illuminazione è abilitata e la specularità è abilitata, vale a significa che D3DRS \_ SPECULARENABLE e D3DRS \_ LIGHTING sono impostati su **TRUE.** Il colore speculare viene generato anche quando è abilitata la nebbia. Le coordinate di trama vengono generate quando è abilitata la trasformazione della trama o la generazione di trame. **IDirect3DDevice9::P rocessVertices** usa gli stati di rendering correnti per determinare quale elaborazione dei vertici deve essere eseguita.

## <a name="fvf-usage-settings-for-destination-vertex-buffers"></a>Utilizzo FVF Impostazioni per i vertex buffer di destinazione

Il [**metodo IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) richiede impostazioni specifiche per [D3DFVF](d3dfvf.md) del vertex buffer di destinazione. Le impostazioni di utilizzo FVF devono essere compatibili con le impostazioni correnti per l'elaborazione dei vertici.

Per l'elaborazione dei vertici delle funzioni fisse, [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) richiede le impostazioni FVF seguenti:

-   Il tipo di posizione è sempre [D3DFVF \_ XYZRHW;](d3dfvf.md) pertanto, D3DFVF \_ XYZ e D3DFVF \_ XYZB1 fino a D3DFVF \_ XYZB5 non sono validi.
-   I [flag D3DFVF \_ NORMAL](d3dfvf.md), D3DFVF RESERVED0 e \_ D3DFVF RESERVED2 non \_ devono essere impostati.
-   Il flag [DIFFUSE \_ D3DFVF](d3dfvf.md) deve essere impostato se un'operazione OR delle condizioni seguenti restituisce true:
    -   L'illuminazione è abilitata; vale a fare in modo che D3DRS \_ LIGHTING sia **TRUE.**
    -   L'illuminazione è disabilitata, il colore diffuso è presente nei flussi dei vertici di input e [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) non è impostato.
-   Il flag [ \_ SPECULAR D3DFVF](d3dfvf.md) deve essere impostato se un'operazione OR delle condizioni seguenti restituisce true:
    -   L'illuminazione è abilitata e il colore speculare è abilitato; vale a significa che D3DRS \_ SPECULARENABLE è **TRUE.**
    -   L'illuminazione è disabilitata, il colore speculare è presente nei flussi dei vertici di input e [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) non è impostato.
    -   Vertex osa è abilitato; in altri, D3DRS \_ FOGVERTEXMODE non è impostato su D3DFOG \_ NONE.

Inoltre, il conteggio delle coordinate della trama deve essere impostato nel modo seguente:

-   Se la trasformazione della trama e la generazione della trama sono disabilitate per tutte le fasi attive della trama e [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) non è impostato, il numero e il tipo di coordinate della trama di output sono necessari per corrispondere a quelle delle coordinate della trama dei vertici di input. Se d3DPV DONOTCOPYDATA è impostato e la trasformazione della trama e la generazione della trama sono \_ disabilitate, le coordinate della trama di output vengono ignorate.
-   Se la trasformazione di trama o la generazione di trame è abilitata per tutte le fasi attive della trama, il vertice di output potrebbe dover contenere più set di coordinate di trama rispetto al vertice di input. Ciò è dovuto alla proliferazione di coordinate di trama da quelle generate dalla generazione di trame o derivate dalle trasformazioni di trama. Si noti che una proliferazione simile di coordinate di trama si verifica durante le chiamate [**IDirect3DDevice9::D rawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) ma non è visibile al programmatore dell'applicazione. In questo caso, Direct3D genera un nuovo set di coordinate di trama. Il nuovo set di coordinate di trama viene derivato passando attraverso le fasi della trama e analizzando le impostazioni per la generazione di trame, la trasformazione della trama e l'indice delle coordinate di trama per determinare se è necessario un set univoco di coordinate di trama per tale fase. Ogni volta che è necessario un nuovo set, viene allocato in ordine crescente. Si noti che il requisito massimo e tipico è un set per fase, anche se potrebbe essere inferiore a causa della condivisione di coordinate di trama non trasformate tramite D3DTSS \_ TEXCOORDINDEX.

Pertanto, per ogni fase della trama, viene generato un nuovo set di coordinate di trama se una trama è associata a tale fase e si verifica una delle condizioni seguenti:

-   La generazione di trame è abilitata per tale fase.
-   La trasformazione trama è abilitata per tale fase.
-   Per la prima volta, le coordinate della trama di input non trasformate vengono referenziate tramite D3DTSS \_ TEXCOORDINDEX.

Quando Direct3D genera coordinate di trama, l'applicazione deve eseguire le azioni seguenti:

1.  Usare un vertex buffer di destinazione con l'utilizzo FVF appropriato.
2.  Riprogrammare D3DTSS TEXCOORDINDEX della fase della trama in base alla posizione delle coordinate \_ della trama post-elaborazione. Si noti che la riprogrammazione dell'impostazione D3DTSS TEXCOORDINDEX si verifica quando il vertex buffer elaborato viene usato nelle chiamate \_ [**IDirect3DDevice9::D rawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) e [**IDirect3DDevice9::D rawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) successive.

Infine, la dimensionalità delle coordinate della trama ([da D3DFVF \_ TEX0](d3dfvf.md) a D3DFVF TEX8 ) deve essere impostata \_ nel modo seguente:

-   Per ogni set di coordinate di trama, se la trasformazione della trama e la generazione della trama sono disabilitate, la dimensionalità delle coordinate della trama di output deve corrispondere all'input. Se la trasformazione trama è abilitata, la dimensionalità di output deve corrispondere al conteggio definito dalle impostazioni \_ D3DTTFF COUNT1, D3DTTFF \_ COUNT2, D3DTTFF COUNT3 o \_ D3DTTFF \_ COUNT4. Se la trasformazione della trama è disabilitata e la generazione di trame è abilitata, la dimensionalità dell'output deve corrispondere alle impostazioni per la modalità di generazione della trama. attualmente tutte le modalità generano tre valori float.

Quando [**IDirect3DDevice9::P rocessVertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) ha esito negativo a causa di un codice FVF del vertex buffer di destinazione incompatibile, il codice previsto viene stampato nell'output di debug (solo build di debug).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Vertex Buffer](vertex-buffers.md)
</dt> </dl>

 

 
