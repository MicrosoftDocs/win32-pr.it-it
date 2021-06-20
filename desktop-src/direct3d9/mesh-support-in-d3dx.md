---
description: Informazioni sul supporto di mesh in D3DX. D3DX è una libreria di utilità che fornisce servizi helper. Si tratta di un livello sopra il componente Direct3D.
ms.assetid: 7892370f-0807-4ab7-b7cd-a7e1182e3f9c
title: Supporto mesh in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1600b372432d59357a7431c70ce70ce2958002c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408134"
---
# <a name="mesh-support-in-d3dx-direct3d-9"></a>Supporto mesh in D3DX (Direct3D 9)

D3DX è una libreria di utilità che fornisce servizi helper. Si tratta di un livello sopra il componente Direct3D.

## <a name="meshes"></a>Mesh

D3DX implementa il costrutto mesh per caricare, modificare ed eseguire il rendering del contenuto del file con estensione x. Una mesh è fondamentalmente una raccolta di vertici che definiscono una geometria e un set di indici che definiscono i visi. Esistono diversi tipi di mesh.

[**ID3DXBaseMesh**](id3dxbasemesh.md) fornisce le nozioni fondamentali. [**ID3DXMesh**](id3dxmesh.md) eredita da ID3DXBaseMesh e aggiunge l'ottimizzazione mesh usando la cache dei vertici per chip. [**ID3DXSkinInfo fornisce**](id3dxskininfo.md) il supporto per mesh con interfaccia.

[**ID3DXBaseMesh**](id3dxbasemesh.md) fornisce metodi per modificare ed eseguire query sugli oggetti mesh [**ID3DXMesh,**](id3dxmesh.md) che ereditano dalla mesh di base. Sono incluse le operazioni di adizia, il recupero del buffer geometrico, le operazioni di blocco/sblocco (vertice e indice) e la copia, il rendering, il viso e le informazioni sui vertici.

> [!Note]  
> Le interfacce ID3DXPMesh e ID3DXSPMesh (per supportare rispettivamente mesh progressive e semplificate) disponibili nelle versioni precedenti di Direct3D 9 sono state eliminate.

 

## <a name="mesh-architecture"></a>Architettura mesh

Una mesh contiene i dati per un modello complesso. Si tratta di un contenitore di dati astratto che contiene risorse quali trame e materiali e attributi come i dati di posizione e i dati di adizia. Esistono diverse operazioni di mesh che migliorano le prestazioni di disegno e l'aspetto di una superficie. Esistono anche diversi altri concetti di mesh che avranno effetto sulla funzionalità delle operazioni di mesh. La comprensione di questi concetti di mesh in modo da poterli applicare migliorerà le prestazioni della mesh.

## <a name="mesh-object-data"></a>Dati oggetto mesh

Una mesh contiene un buffer dei vertici, un index buffer e un buffer dell'attributo.

-   Il buffer dei vertici contiene i dati dei vertici, ovvero i vertici della mesh.
-   L index buffer contiene gli indici dei vertici per l'accesso al buffer dei vertici. In questo modo è possibile ridurre le dimensioni del buffer dei vertici riducendo i vertici duplicati. Solo una mesh indicizzata usa il index buffer. Se ad esempio una mesh è costituito da un elenco di triangoli, non usa il index buffer.
-   Il buffer dell'attributo contiene i dati dell'attributo. Gli attributi sono proprietà dei vertici mesh, in nessun ordine particolare. Una mesh D3DX archivia gli attributi in un gruppo di DWORD per ogni viso.

### <a name="attribute-tables"></a>Tabelle degli attributi

Una tabella di attributi è una rappresentazione concisa del contenuto di un buffer di attributi. Le tabelle degli attributi possono essere create chiamando uno dei metodi Optimize con D3DXMESHOPT ATTRSORT, bloccando il buffer dell'attributo e compilando i dati oppure chiamando \_ SetAttributeTable. Una mesh contiene una tabella di attributi quando la mesh viene riordinata in gruppi. Ciò si verifica quando viene chiamato Optimize, presupponendo che sia specificata un'opzione di ordinamento degli attributi (D3DXMESHOPT \_ ATTRSORT o versione successiva). Le mesh D3DX usano elenchi di triangoli indicizzati e pertanto vengono disegnate con [**IDirect3DDevice9::D rawIndexedPrimitive.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)

Le tabelle degli attributi vengono create come risultato della chiamata a Optimize. Non è necessario che i visi siano adiacenti, perché Optimize ne riordina l'ordine in modo che siano adiacenti. Ad esempio, le mani di una mesh umana possono usare lo stesso attributo. L'ID consente di ordinare i visi in gruppi. Le mesh dei file con estensione x hanno attributi generati automaticamente per le proprietà dei materiali e delle trame. È necessario chiamare Optimize(ATTRSORT) o optimize(VERTEXCACHE) più efficace per ottenere prestazioni ottimali. Le funzioni di caricamento tentano di presentare i dati nel formato esatto in cui sono stati salvati. Se si usa una mesh basata su vertex buffer/index buffer, l'API mesh fornisce funzioni di ottimizzazione e trasformazioni di interfaccia con un sovraccarico minimo.

I tipi di ottimizzazione sono cumulativi, a partire dal meno ottimale (D3DXMESHOPT COMPACT) al più ottimale \_ (D3DXMESHOPT \_ IGNOREVERTS). D3DXMESHOPT \_ STRIPREORDER esegue una compattazione e un ordinamento degli attributi. D3DXMESHOPT VERTEXCACHE è sempre consigliato, anche nei dispositivi \_ senza una vera cache dei vertici.

## <a name="application-data"></a>Dati applicazione

I dati dell'applicazione sono dati mesh gestiti da un'applicazione. Esiste un accoppiamento stretto tra i dati dei vertici della mesh e i dati gestiti da questi buffer.

Il buffer materials contiene n materiali. I materiali vengono restituiti dalla funzione Load quando viene caricato il file con estensione x. Ogni subset può avere materiali e trame propri. Il buffer materials è statico.

Il buffer di adienza contiene informazioni su bordi, visi e visi adiacenti. Alcune operazioni di mesh dipendono dalla conoscenza dei visi adiacenti. Queste informazioni, denominate dati di adizia, vengono mantenute in un buffer di adienze. Non fa parte della mesh, ma viene gestita dall'applicazione e deve essere fornita ai metodi mesh quando necessario.

Il buffer dell'istanza degli effetti contiene un elenco di istanze dell'effetto. Un'istanza dell'effetto archivia lo stato. Queste informazioni sullo stato vengono usate per inizializzare la pipeline. Un'istanza dell'effetto contiene coppie nome-valore in un effetto.

## <a name="advanced-mesh-topics"></a>Argomenti avanzati su Mesh

Le mesh ottimizzate si basano sulla funzionalità della mesh di base e aggiungono la funzionalità di ottimizzazione della cache dei vertici con due metodi: Optimize, che crea una nuova mesh, e OptimizeInPlace, che modifica la mesh originale.

D3DXGeneratePMesh usa l'algoritmo di semplificazione D3DX per generare una mesh progressiva dalla mesh di input. D3DXSimplifyMesh genera una mesh standard del livello di dettaglio specificato da una mesh di input usando lo stesso algoritmo di semplificazione. L'utente ha il controllo sulla metrica di errore usata tramite i pesi specificati per componente per vertice e i pesi specificati per vertice. I pesi per componente vengono moltiplicati rispetto alla parte di errore dei componenti calcolata per ogni compressione degli bordi. I pesi per vertice vengono moltiplicati rispetto al valore della metrica di errore determinato per la rimozione di tale vertice. Ad esempio, se non si vuole mai rimuovere un vertice, impostare il peso del vertice specifico su un valore elevato. Viceversa, se si vuole che venga rimosso in precedenza, impostarlo su un valore ridotto (minore di 1).

[**ID3DXSkinInfo**](id3dxskininfo.md) supporta i caratteri con interfaccia. Un carattere con interfaccia è definito da un set di mesh e da un set di elementi che influiscono sui vertici delle mesh. L'elemento è rappresentato come una gerarchia di trasformazione. Per ogni mesh, è presente una matrice per ogni elemento che la interessa, che trasforma la mesh nello spazio delle coordinate locale dell'elemento. Questa matrice è la trasformazione spazio-spazio dell'elemento per la mesh. Questo valore viene definito nel momento in cui lo scheletro è associato alla mesh nel processo di creazione.

### <a name="skinning"></a>Scuoiatura

L'interfacciatura è una tecnica per trasformare i vertici mesh usando la superficie. Gli scheletri sono in genere disposti in uno scheletro gerarchico, in modo molto simile a quello di un corpo umano. I vertici degli oggetti vengono quindi associati all'elemento, ad esempio collegando l'interfaccia all'elemento. Quando l'aspetto viene trasformato, viene trasformata anche l'interfaccia.

Le mesh con interfaccia usano la tonalità per influenzare un numero di vertici. I dati di trasformazione della trasformazione della trasformazione vengono forniti dall'utente, per influenzare il modo in cui eseguire il SRT. La mesh usa l'effetto trasformato per influenzare i vertici associati all'elemento. Le tavolozze sono matrici di trasformazioni SRT. Le tavolozze vengono spesso implementate come matrici, ma possono contenere valori SRT.

### <a name="progressive-mesh-trimming"></a>Trimming mesh progressivo

Le aree con dettagli bassi possono permettersi di perdere i vertici che non modificano l'aspetto di rendering della superficie. Ciò vale soprattutto per gli oggetti che si spostano più lontano dalla fotocamera. Questo livello viene definito livello di dettaglio. Gli utenti hanno controlli di rendering a livello di API per impostare il livello di dettaglio per ottimizzare l'efficienza del rendering.

Gli oggetti mesh progressiva iniziano con un numero elevato di visi e usano la semplificazione per ridurre il numero di visi. Una mesh progressiva indipendente dalla visualizzazione viene definita mesh progressiva indipendente dalla visualizzazione (VIPM).

Un altro modo per ridurre il numero di visi è tagliando. In questo modo i vertici e le visi vengono effettivamente rimossi dalla mesh. Il taglio può essere eseguito all'estremità superiore (per limitare il numero massimo di visi) o all'estremità inferiore (per limitare il numero minimo di visi). Il trimming migliora le prestazioni di disegno, tuttavia è necessario fare attenzione a mantenere la qualità visiva. Il trimming è illustrato nell'esempio progressive mesh SDK.

Per le aree con visibilità elevata, la risoluzione può essere aumentata usando il livello di dettaglio progressivo (PLOD). Si tratta di una tecnica per suddividere un singolo viso in due visi.

### <a name="patch-meshes"></a>Applicare patch alle mesh

Sono supportati anche due tipi specializzati di mesh patch: patch rettangolari e triangoli. La mesh patch rettangolare è una mesh patch i cui punti di controllo sono disposti in una sequenza rettangolare tortuosa. Le patch rettangolari e triangolo vengono usate per creare superfici di alto ordine. Non vengono comunemente usati come mesh a triangolo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 
