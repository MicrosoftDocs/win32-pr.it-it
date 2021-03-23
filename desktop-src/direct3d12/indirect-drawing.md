---
title: Disegno indiretto
description: Il disegno indiretto consente lo spostamento da parte della CPU alla GPU di alcuni attraversamenti della scena, che possono migliorare le prestazioni. Il buffer dei comandi può essere generato dalla CPU o dalla GPU.
ms.assetid: F8D6C88A-101E-4F66-999F-43206F6527B6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7731a662bc6064e635d68942e6b0b222adf1eda8
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/19/2020
ms.locfileid: "104548793"
---
# <a name="indirect-drawing"></a>Disegno indiretto

Il disegno indiretto consente lo spostamento da parte della CPU alla GPU di alcuni attraversamenti della scena, che possono migliorare le prestazioni. Il buffer dei comandi può essere generato dalla CPU o dalla GPU.

-   [Firme del comando](#command-signatures)
-   [Strutture di buffer di argomenti indiretti](#indirect-argument-buffer-structures)
-   [Creazione della firma del comando](#command-signature-creation)
    -   [Nessun argomento modificato](#no-argument-changes)
    -   [Costanti radice e buffer dei vertici](#root-constants-and-vertex-buffers)
-   [Argomenti correlati](#related-topics)

## <a name="command-signatures"></a>Firme del comando

L'oggetto della firma del comando ([**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature)) consente alle app di specificare il disegno indiretto, in particolare impostando quanto segue:

-   Formato del buffer dell'argomento indiretto.
-   Tipo di comando che verrà usato (dai metodi [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) [**DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced), [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)o [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)).
-   Il set di associazioni di risorse che cambieranno la chiamata per ogni comando rispetto al set che verrà ereditato.

All'avvio, un'app crea un piccolo set di **firme dei comandi**. In fase di esecuzione, l'applicazione riempie un buffer con i comandi (tramite qualsiasi altro strumento scelto dallo sviluppatore di app). I comandi contengono facoltativamente lo stato da impostare per le visualizzazioni dei buffer di vertici, le visualizzazioni dei buffer di indice, le costanti radice e i descrittori radice (non elaborato o strutturato SRV/UAV/CBVs). Questi layout degli argomenti non sono specifici dell'hardware, quindi le app possono generare direttamente i buffer. La firma del comando eredita lo stato rimanente dall'elenco dei comandi. L'app chiama quindi [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) per indicare alla GPU di interpretare il contenuto del buffer di argomenti indiretto in base al formato definito da una particolare firma del comando.

Se la firma del comando modifica qualsiasi argomento radice, viene archiviato nella firma del comando come subset di una firma radice.

Si noti che nessuno stato della firma del comando perde l'elenco dei comandi al termine dell'esecuzione.

Si supponga, ad esempio, che uno sviluppatore di app voglia specificare una costante radice univoca per la chiamata per ogni progetto nel buffer degli argomenti indiretti. L'app crea una firma del comando che consente al buffer di argomenti indiretto di specificare i seguenti parametri per chiamata di traccia:

-   Valore di una costante radice.
-   Argomenti di estrazione (conteggio vertici, numero di istanze e così via).

Il buffer di argomento indiretto generato dall'applicazione conterrà una matrice di record di dimensioni fisse. Ogni struttura corrisponde a una chiamata di progetto. Ogni struttura contiene gli argomenti del disegno e il valore della costante radice. Il numero di chiamate di progetto viene specificato in un buffer visibile GPU separato.

Di seguito è riportato un esempio di buffer dei comandi generato dall'app:

![formato del buffer dei comandi](images/indirect-drawing-command-buffer.png)

## <a name="indirect-argument-buffer-structures"></a>Strutture di buffer di argomenti indiretti

Le strutture seguenti definiscono la modalità di visualizzazione di argomenti specifici in un buffer di argomento indiretto. Queste strutture non vengono visualizzate in alcuna API D3D12. Le applicazioni usano queste definizioni durante la scrittura in un buffer di argomenti indiretto (con CPU o GPU):

-   [**Argomenti di D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments)
-   [**D3D12 \_ creare \_ argomenti indicizzati \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments)
-   [**\_Argomenti dispatch \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dispatch_arguments)
-   [**\_ \_ Visualizzazione buffer vertex \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)
-   [**\_ \_ Visualizzazione buffer dell'indice D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view)
-   \_ \_ Indirizzo virtuale della GPU D3D12 \_ (sinonimo di UInt64).
-   [**\_ \_ Visualizzazione buffer costante \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc)

## <a name="command-signature-creation"></a>Creazione della firma del comando

Per creare una firma del comando, usare gli elementi API seguenti:

-   [**ID3D12Device:: CreateCommandSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) (restituisce un [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature))
-   [**\_Tipo di \_ argomento INdiretto D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_indirect_argument_type)
-   [**\_Desc D3D12 \_ argomento indiretto \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc)
-   [**\_Descrizione della \_ firma del comando D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc)

L'ordinamento degli argomenti all'interno di un buffer di argomento indiretto viene definito in modo da corrispondere esattamente all'ordine degli argomenti specificato nel parametro *pArguments* della [**firma del \_ comando D3D12 \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc). Tutti gli argomenti per una chiamata/dispatch (Compute) di un grafico (calcolo) all'interno di un buffer di argomento indiretto sono strettamente compressi. Tuttavia, le applicazioni possono specificare uno stride di byte arbitrario tra i comandi di estrazione/invio in un buffer di argomento indiretto.

La firma radice deve essere specificata solo se la firma del comando modifica uno degli argomenti radice.

Per la radice SRV/UAV/CBV, le dimensioni specificate per l'applicazione sono in byte. Il livello di debug convaliderà le restrizioni seguenti per l'indirizzo:

-   CBV: l'indirizzo deve essere un multiplo di 256 byte.
-   SRV/UAV non elaborato: l'indirizzo deve essere un multiplo di 4 byte.
-   SRV/UAV strutturato: l'indirizzo deve essere un multiplo dello stride di byte della struttura (dichiarato nello shader).

Una firma del comando specificata è una firma del comando di calcolo o di traccia. Se una firma del comando contiene un'operazione di disegno, si tratta di una firma del comando grafica. In caso contrario, la firma del comando deve contenere un'operazione di invio ed è una firma del comando COMPUTE.

Le sezioni seguenti illustrano alcune firme dei comandi di esempio.

### <a name="no-argument-changes"></a>Nessun argomento modificato

In questo esempio, il buffer di argomenti indiretto generato dall'applicazione include una matrice di strutture a 36 byte. Ogni struttura contiene solo i cinque parametri passati a [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) (più la spaziatura interna).

Di seguito è riportato il codice per creare la descrizione della firma del comando:

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[1];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW_INDEXED;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 36;
ProgramDesc.NumArgumentDescs = 1;
ProgramDesc.pArguments = Args;
```

Il layout di una singola struttura all'interno di un buffer di argomento indiretto è:



| Byte | Descrizione           |
|-------|-----------------------|
| 0:3   | IndexCountPerInstance |
| 4:7   | InstanceCount         |
| 8:11  | StartIndexLocation    |
| 12:15 | BaseVertexLocation    |
| 16:19 | StartInstanceLocation |
| 20:35 | Riempimento               |



 

### <a name="root-constants-and-vertex-buffers"></a>Costanti radice e buffer dei vertici

In questo esempio, ogni struttura in un buffer di argomento indiretto modifica due costanti radice, modifica un'associazione di buffer di Vertex ed esegue un'operazione di disegno non indicizzata. Nessun riempimento tra le strutture.

Il codice per creare la descrizione della firma del comando è:

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[4];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[0].Constant.RootParameterIndex = 2;

Args[1].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[1].Constant.RootParameterIndex = 6;

Args[2].Type = D3D12_INDIRECT_ARGUMENT_TYPE_VERTEX_BUFFER_VIEW;
Args[2].VertexBuffer.VBSlot = 3;

Args[3].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW_INSTANCED;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 40;
ProgramDesc.NumArgumentDescs = 4;
ProgramDesc.pArguments = Args;
```

Il layout di una singola struttura all'interno del buffer degli argomenti indiretti è il seguente:



| Byte | Descrizione                     |
|-------|---------------------------------|
| 0:3   | Dati per il parametro root index 2 |
| 4:7   | Dati per il parametro root index 6 |
| 8:15  | Indirizzo virtuale di VB (64 bit)  |
| 16:19 | Dimensioni di VB                         |
| 20:23 | Stride VB                       |
| 24:27 | VertexCountPerInstance          |
| 28:31 | InstanceCount                   |
| 32:35 | StartVertexLocation             |
| 36:39 | StartInstanceLocation           |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esercitazioni video su DirectX Advanced Learning: eseguire l'abbattimento indiretto e asincrono della GPU](https://www.youtube.com/watch?v=fKD-VKJeeds)
</dt> <dt>

[Disegno indiretto e eliminazione della GPU: procedura dettagliata del codice](indirect-drawing-and-gpu-culling-.md)
</dt> <dt>

[Rendering](rendering.md)
</dt> </dl>

 

 