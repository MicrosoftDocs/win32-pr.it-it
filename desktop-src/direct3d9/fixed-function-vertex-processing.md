---
description: Nella pipeline del vertice della funzione fissa, l'elaborazione dei vertici in un buffer dei vertici applica le matrici di trasformazione correnti per il dispositivo.
ms.assetid: a882a5c5-b05e-4659-9040-92d3e2ccd89c
title: Elaborazione del vertice della funzione fissa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da30dd0fb6cf6e055d8b1bbb31fdfdb01d9e1e20
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124017"
---
# <a name="fixed-function-vertex-processing-direct3d-9"></a>Elaborazione del vertice della funzione fissa (Direct3D 9)

Nella pipeline del vertice della funzione fissa, l'elaborazione dei vertici in un buffer dei vertici applica le matrici di trasformazione correnti per il dispositivo. È anche possibile applicare operazioni sui vertici, ad esempio l'illuminazione, la generazione di flag di ritaglio e l'aggiornamento degli extent, facoltativamente. Quando si usa l'elaborazione del vertice della funzione fissa, la modifica degli elementi nel buffer dei vertici di destinazione viene controllata dal flag [ \_ DONOTCOPYDATA di D3DPV](other-direct3d-constants.md) . Questo flag si applica solo all'elaborazione del vertice della funzione fissa. L'interfaccia [**IDirect3DDevice9**](/windows/desktop/api) espone il metodo [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) per elaborare i vertici. Si elaborano i vertici da un vertex shader al set di flussi di dati di input, generando un singolo flusso di dati dei vertici con interfoliazione nel buffer dei vertici di destinazione chiamando il metodo **IDirect3DDevice9::P rocessvertices** . Il metodo accetta cinque parametri che descrivono la posizione e la quantità di vertici a cui è destinato il metodo, il buffer del vertice di destinazione e le opzioni di elaborazione. Dopo la chiamata, il buffer di destinazione contiene i dati dei vertici elaborati.

Il primo, il secondo e il terzo parametro, SrcStartIndex, DestIndex e VertexCount, riflettono l'indice del primo vertice da caricare, l'indice all'interno del buffer di destinazione in corrispondenza del quale verranno inseriti i vertici e il numero totale di vertici da elaborare e inserire rispettivamente nel buffer di destinazione. Il quarto parametro, pDestBuffer deve essere impostato sull'indirizzo dell'interfaccia [**IDirect3DVertexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9) dell'oggetto vertex buffer che riceverà i vertici di origine. Il parametro SrcStartIndex specifica l'indice in corrispondenza del quale il metodo deve iniziare a elaborare i vertici.

Il parametro finale, Flags, determina opzioni di elaborazione speciali per il metodo. È possibile impostare questo parametro su 0 per l'elaborazione dei vertici predefiniti oppure su [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) per ottimizzare l'elaborazione in alcune situazioni. È anche possibile combinare il \_ valore DONOTCOPYDATA di D3DPV con uno o più valori [D3DLOCK](d3dlock.md) appropriati per il buffer di destinazione. Quando si impostano i flag su 0, i componenti Vertex del formato Vertex del buffer dei vertici di destinazione che non sono interessati dall'operazione Vertex vengono comunque copiati dal vertex shader o impostati su 0. Tuttavia, quando si usa D3DPV \_ DONOTCOPYDATA, [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) non sovrascrive le informazioni sulle coordinate di colore e trama nel buffer di destinazione, a meno che questi dati non vengano generati da Direct3D. Il colore diffuso viene generato quando è abilitata l'illuminazione, ovvero D3DRS \_ Lighting è impostato su **true**. Il colore speculare viene generato quando è abilitata l'illuminazione e viene abilitato il specularità, ovvero D3DRS \_ SPECULARENABLE e D3DRS \_ Lighting sono impostati su **true**. Quando è abilitata la nebbia, viene generato anche il colore speculare. Le coordinate di trama vengono generate quando è abilitata la trasformazione della trama o la generazione della trama. **IDirect3DDevice9::P rocessvertices** usa gli Stati di rendering correnti per determinare quale elaborazione del vertice è necessario eseguire.

## <a name="fvf-usage-settings-for-destination-vertex-buffers"></a>Impostazioni di utilizzo di FVF per i buffer dei vertici di destinazione

Il metodo [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) richiede impostazioni specifiche per il [D3DFVF](d3dfvf.md) del buffer del vertice di destinazione. Le impostazioni di utilizzo di FVF devono essere compatibili con le impostazioni correnti per l'elaborazione dei vertici.

Per l'elaborazione dei vertici della funzione fissa, [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) richiede le impostazioni FVF seguenti:

-   Il tipo di posizione è sempre [D3DFVF \_ XYZRHW](d3dfvf.md) ; pertanto, D3DFVF \_ XYZ e D3DFVF \_ XYZB1 tramite D3DFVF \_ XYZB5 non sono validi.
-   I flag [D3DFVF \_ Normal](d3dfvf.md), D3DFVF \_ RESERVED0 e D3DFVF \_ RESERVED2 non devono essere impostati.
-   È necessario impostare il flag [D3DFVF \_ Diffusion](d3dfvf.md) se un'operazione o delle condizioni seguenti restituisce true:
    -   Illuminazione abilitata; ovvero, D3DRS \_ Lighting è **true**.
    -   L'illuminazione è disabilitata, il colore diffuso è presente nei flussi dei vertici di input e [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) non è impostato.
-   Il flag [D3DFVF \_ Specular](d3dfvf.md) deve essere impostato se un'operazione o delle condizioni seguenti restituisce true:
    -   L'illuminazione è abilitata e il colore speculare è abilitato; ovvero, D3DRS \_ SPECULARENABLE è **true**.
    -   L'illuminazione è disabilitata, il colore speculare è presente nei flussi dei vertici di input e [D3DPV \_ DONOTCOPYDATA](other-direct3d-constants.md) non è impostato.
    -   La nebbia del vertice è abilitata; ovvero, D3DRS \_ FOGVERTEXMODE non è impostato su D3DFOG \_ None.

Inoltre, il conteggio delle coordinate di trama deve essere impostato nel modo seguente:

-   Se la trasformazione di trama e la generazione di trama sono disabilitate per tutte le fasi della trama attive e il [ \_ DONOTCOPYDATA D3DPV](other-direct3d-constants.md) non è impostato, il numero e il tipo delle coordinate di trama di output devono corrispondere a quelli delle coordinate di trama dei vertici di input. Se D3DPV \_ DONOTCOPYDATA è impostato e la trasformazione della trama e la generazione della trama sono disabilitate, le coordinate di trama di output vengono ignorate.
-   Se la trasformazione trama o la generazione di trama è abilitata per le fasi di trama attive, il vertice di output potrebbe dover contenere più set di coordinate di trama rispetto al vertice di input. Ciò è dovuto alla proliferazione di coordinate di trama da quelle generate dalla generazione di trama o derivate da trasformazioni di trama. Si noti che si verifica una proliferazione simile delle coordinate di trama durante [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) chiamate, ma non è visibile al programmatore dell'applicazione. In questo caso, Direct3D genera un nuovo set di coordinate di trama. Il nuovo set di coordinate di trama viene derivato eseguendo le fasi di trama e analizzando le impostazioni per la generazione della trama, la trasformazione della trama e l'indice delle coordinate di trama per determinare se per la fase è necessario un set univoco di coordinate di trama. Ogni volta che un nuovo set è necessario, viene allocato in ordine crescente. Si noti che il requisito massimo, e tipico, è un set per fase, anche se può essere minore a causa della condivisione di coordinate di trama non trasformate tramite D3DTSS \_ TEXCOORDINDEX.

Per ogni fase della trama viene quindi generato un nuovo set di coordinate di trama se una trama è associata a tale fase e si verifica una delle condizioni seguenti:

-   La generazione di trama è abilitata per la fase.
-   La trasformazione trama è abilitata per la fase.
-   Si fa riferimento alle coordinate di trama di input non trasformate tramite D3DTSS \_ TEXCOORDINDEX per la prima volta.

Quando Direct3D genera coordinate di trama, l'applicazione è necessaria per eseguire le azioni seguenti:

1.  Usare un vertex buffer di destinazione con l'utilizzo di FVF appropriato.
2.  Riprogrammare il \_ TEXCOORDINDEX D3DTSS della fase della trama in base alla posizione delle coordinate di trama rielaborate. Si noti che la riprogrammazione dell' \_ impostazione TEXCOORDINDEX di D3DTSS si verifica quando il buffer vertex elaborato viene usato nelle chiamate successive a [**IDirect3DDevice9::D Rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) e [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) .

Infine, è necessario impostare la dimensionalità delle coordinate di trama ([D3DFVF \_ TEX0](d3dfvf.md) tramite D3DFVF \_ TEX8) nel modo seguente:

-   Per ogni set di coordinate di trama, se la trasformazione di trama e la generazione di trama sono disabilitate, la dimensionalità delle coordinate di trama di output deve corrispondere all'input. Se la trasformazione trama è abilitata, la dimensionalità di output deve corrispondere al numero definito dalle \_ Impostazioni D3DTTFF COUNT1, D3DTTFF \_ COUNT2, D3DTTFF \_ COUNT3 o D3DTTFF \_ COUNT4. Se la trasformazione trama è disabilitata e la generazione della trama è abilitata, la dimensionalità di output deve corrispondere alle impostazioni per la modalità di generazione della trama; Attualmente tutte le modalità generano tre valori float.

Quando [**IDirect3DDevice9::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) ha esito negativo a causa di un codice FVF del buffer dei vertici di destinazione incompatibile, il codice previsto viene stampato nell'output di debug (solo build di debug).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Buffer vertici](vertex-buffers.md)
</dt> </dl>

 

 
