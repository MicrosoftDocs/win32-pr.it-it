---
title: Disegno indiretto
description: Il disegno indiretto consente di spostare parte dell'attraversamento e del culling della scena dalla CPU alla GPU, migliorando le prestazioni. Il buffer dei comandi può essere generato dalla CPU o dalla GPU.
ms.assetid: F8D6C88A-101E-4F66-999F-43206F6527B6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa474a469d5789d4b31830400d981ea771db2e8
ms.sourcegitcommit: b9a7a48e52219bf8d33e6b8171fc9f8b52151e92
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/21/2021
ms.locfileid: "112421879"
---
# <a name="indirect-drawing"></a>Disegno indiretto

Il disegno indiretto consente di spostare parte dell'attraversamento e del culling della scena dalla CPU alla GPU, migliorando le prestazioni. Il buffer dei comandi può essere generato dalla CPU o dalla GPU.

-   [Firme dei comandi](#command-signatures)
-   [Strutture di buffer degli argomenti indiretti](#indirect-argument-buffer-structures)
-   [Creazione della firma del comando](#command-signature-creation)
    -   [Nessuna modifica dell'argomento](#no-argument-changes)
    -   [Costanti radice e vertex buffer](#root-constants-and-vertex-buffers)
-   [Argomenti correlati](#related-topics)

## <a name="command-signatures"></a>Firme dei comandi

L'oggetto firma del comando ([**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature)) consente alle app di specificare il disegno indiretto, in particolare impostando quanto segue:

-   Formato del buffer dell'argomento indiretto.
-   Tipo di comando che verrà usato (dai metodi [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) [**DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced), [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)o [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)).
-   Set di associazioni di risorse che modificherà la chiamata per comando rispetto al set che verrà ereditato.

All'avvio, un'app crea un piccolo set di **firme di comando**. In fase di esecuzione, l'applicazione riempie un buffer con comandi (tramite qualsiasi mezzo scelto dallo sviluppatore dell'app). I comandi contengono facoltativamente lo stato da impostare per le viste del buffer dei vertici, le visualizzazioni index buffer, le costanti radice e i descrittori radice (SRV/UAV/CBV non elaborati o strutturati). Questi layout di argomento non sono specifici dell'hardware, quindi le app possono generare direttamente i buffer. La firma del comando eredita lo stato rimanente dall'elenco dei comandi. L'app chiama [**quindi ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) per indicare alla GPU di interpretare il contenuto del buffer degli argomenti indiretti in base al formato definito da una firma di comando specifica.

Se la firma del comando modifica gli argomenti radice, questo viene archiviato all'interno della firma del comando come subset di una firma radice.

Si noti che lo stato della firma del comando non torna all'elenco dei comandi al termine dell'esecuzione.

Si supponga, ad esempio, che uno sviluppatore di app voglia che una costante radice univoca sia specificata per ogni chiamata di disegno nel buffer degli argomenti indiretti. L'app creerebbe una firma di comando che consente al buffer degli argomenti indiretti di specificare i parametri seguenti per ogni chiamata di disegno:

-   Valore di una costante radice.
-   Argomenti di disegno (conteggio vertici, numero di istanze e così via).

Il buffer dell'argomento indiretto generato dall'applicazione conterrà una matrice di record a dimensione fissa. Ogni struttura corrisponde a una chiamata di disegno. Ogni struttura contiene gli argomenti di disegno e il valore della costante radice. Il numero di chiamate di disegno è specificato in un buffer separato visibile alla GPU.

Di seguito è riportato un esempio di buffer dei comandi generato dall'app:

![formato del buffer dei comandi](images/indirect-drawing-command-buffer.png)

## <a name="indirect-argument-buffer-structures"></a>Strutture di buffer degli argomenti indiretti

Le strutture seguenti definiscono il modo in cui determinati argomenti vengono visualizzati in un buffer di argomenti indiretti. Queste strutture non vengono visualizzate in alcuna API D3D12. Le applicazioni usano queste definizioni durante la scrittura in un buffer di argomenti indiretti (con CPU o GPU):

-   [**ARGOMENTI DI DISEGNO D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments)
-   [**D3D12 \_ DRAW \_ INDEXED \_ ARGUMENTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments)
-   [**ARGOMENTI DISPATCH D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dispatch_arguments)
-   [**VISTA \_ VERTEX BUFFER \_ D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)
-   [**VISTA BUFFER INDICE D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view)
-   D3D12 \_ GPU \_ VIRTUAL ADDRESS \_ (un sinonimo di typedef di UINT64).
-   [**VISUALIZZAZIONE BUFFER COSTANTE D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc)

## <a name="command-signature-creation"></a>Creazione della firma del comando

Per creare una firma di comando, usare gli elementi API seguenti:

-   [**ID3D12Device::CreateCommandSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) (restituisce un [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature))
-   [**TIPO DI ARGOMENTO \_ INDIRETTO D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_indirect_argument_type)
-   [**D3D12 \_ ARGOMENTO \_ INDIRETTO \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc)
-   [**D3D12 \_ COMMAND \_ SIGNATURE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc)

L'ordinamento degli argomenti all'interno di un buffer di argomenti indiretti è definito in modo che corrisponda esattamente all'ordine degli argomenti specificato nel *parametro pArguments* di [**D3D12 \_ COMMAND SIGNATURE \_ \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc) Tutti gli argomenti per una chiamata di disegno (grafica)/invio (calcolo) all'interno di un buffer di argomenti indiretti sono strettamente imballati. Tuttavia, alle applicazioni è consentito specificare uno stride di byte arbitrario tra i comandi di disegno/invio in un buffer di argomenti indiretti.

La firma radice deve essere specificata solo se la firma del comando modifica uno degli argomenti radice.

Per la radice SRV/UAV/CBV, le dimensioni specificate dall'applicazione sono in byte. Il livello di debug convaliderà le restrizioni seguenti sull'indirizzo:

-   CBV: l'indirizzo deve essere un multiplo di 256 byte.
-   SRV/UAV non elaborato: l'indirizzo deve essere un multiplo di 4 byte.
-   SRV/UAV strutturato: l'indirizzo deve essere un multiplo dello stride di byte della struttura (dichiarato nello shader).

Una firma di comando specificata è una firma di comando di disegno o di calcolo. Se una firma di comando contiene un'operazione di disegno, si tratta di una firma di comando grafica. In caso contrario, la firma del comando deve contenere un'operazione di invio ed è una firma del comando di calcolo.

Le sezioni seguenti illustrano alcune firme di comando di esempio.

### <a name="no-argument-changes"></a>Nessuna modifica dell'argomento

In questo esempio il buffer degli argomenti indiretti generato dall'applicazione contiene una matrice di strutture a 36 byte. Ogni struttura contiene solo i cinque parametri passati a [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) (più la spaziatura interna).

Il codice per creare la descrizione della firma del comando è il seguente:

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[1];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW_INDEXED;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 36;
ProgramDesc.NumArgumentDescs = 1;
ProgramDesc.pArguments = Args;
```

Il layout di una singola struttura all'interno di un buffer di argomenti indiretti è:



| Byte | Descrizione           |
|-------|-----------------------|
| 0:3   | IndexCountPerInstance |
| 4:7   | InstanceCount         |
| 8:11  | StartIndexLocation    |
| 12:15 | BaseVertexLocation    |
| 16:19 | StartInstanceLocation |
| 20:35 | Riempimento               |



 

### <a name="root-constants-and-vertex-buffers"></a>Costanti radice e vertex buffer

In questo esempio, ogni struttura in un buffer di argomenti indiretti modifica due costanti radice, modifica un'associazione al buffer dei vertici ed esegue un'operazione di disegno non indicizzata. Non è presente alcuna spaziatura interna tra le strutture.

Il codice per creare la descrizione della firma del comando è:

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[4];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[0].Constant.RootParameterIndex = 2;
Args[0].Constant.DestOffsetIn32BitValues = 0;
Args[0].Constant.Num32BitValuesToSet = 1;

Args[1].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[1].Constant.RootParameterIndex = 6;
Args[1].Constant.DestOffsetIn32BitValues = 0;
Args[1].Constant.Num32BitValuesToSet = 1;

Args[2].Type = D3D12_INDIRECT_ARGUMENT_TYPE_VERTEX_BUFFER_VIEW;
Args[2].VertexBuffer.Slot = 3;

Args[3].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 40;
ProgramDesc.NumArgumentDescs = 4;
ProgramDesc.pArguments = Args;
```

Il layout di una singola struttura all'interno del buffer degli argomenti indiretti è il seguente:



| Byte | Descrizione                               |
|-------|-------------------------------------------|
| 0:3   | Dati per l'indice del parametro radice 2           |
| 4:7   | Dati per l'indice del parametro radice 6           |
| 8:15  | Indirizzo virtuale di VB nello slot 3 (64 bit)  |
| 16:19 | Dimensioni vb                                   |
| 20:23 | Vb stride                                 |
| 24:27 | VertexCountPerInstance                    |
| 28:31 | InstanceCount                             |
| 32:35 | StartVertexLocation                       |
| 36:39 | StartInstanceLocation                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esercitazioni video sull'apprendimento avanzato di DirectX: Eseguire il culling indiretto e asincrono della GPU](https://www.youtube.com/watch?v=fKD-VKJeeds)
</dt> <dt>

[Disegno indiretto ed culling GPU: procedura dettagliata per il codice](indirect-drawing-and-gpu-culling-.md)
</dt> <dt>

[Rendering](rendering.md)
</dt> </dl>

 

 
