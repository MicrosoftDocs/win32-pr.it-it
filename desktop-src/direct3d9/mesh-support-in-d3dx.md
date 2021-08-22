---
description: Informazioni sul supporto della mesh in D3DX. D3DX è una libreria di utilità che fornisce servizi helper. Si tratta di un livello sopra il componente Direct3D.
ms.assetid: 7892370f-0807-4ab7-b7cd-a7e1182e3f9c
title: Supporto mesh in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 310f9888a2231f781fabe0820357241318cf5e6d486e688ba9c4a786305a6b9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119240761"
---
# <a name="mesh-support-in-d3dx-direct3d-9"></a>Supporto mesh in D3DX (Direct3D 9)

D3DX è una libreria di utilità che fornisce servizi helper. Si tratta di un livello sopra il componente Direct3D.

## <a name="meshes"></a>Mesh

D3DX implementa il costrutto mesh per caricare, modificare ed eseguire il rendering del contenuto del file con estensione x. Una mesh è fondamentalmente una raccolta di vertici che definiscono una geometria e un set di indici che definiscono i visi. Esistono diversi tipi di mesh.

[**ID3DXBaseMesh**](id3dxbasemesh.md) fornisce le nozioni fondamentali. [**ID3DXMesh**](id3dxmesh.md) eredita da ID3DXBaseMesh e aggiunge l'ottimizzazione della mesh usando la cache dei vertici per chip. [**ID3DXSkinInfo fornisce**](id3dxskininfo.md) il supporto della mesh con interfaccia.

[**ID3DXBaseMesh**](id3dxbasemesh.md) fornisce metodi per modificare ed eseguire query sugli oggetti mesh [**ID3DXMesh,**](id3dxmesh.md) che ereditano dalla mesh di base. Sono incluse le operazioni di adicenza, il recupero del buffer geometrico, le operazioni di blocco/sblocco (vertice e indice) e la copia, il rendering, il viso e le informazioni sui vertici.

> [!Note]  
> Le interfacce ID3DXPMesh e ID3DXSPMesh (per supportare rispettivamente mesh progressive e semplificate) disponibili nelle versioni precedenti di Direct3D 9 sono state eliminate.

 

## <a name="mesh-architecture"></a>Architettura mesh

Una mesh contiene i dati per un modello complesso. Si tratta di un contenitore di dati astratto che contiene risorse quali trame e materiali e attributi quali dati di posizione e dati di adienza. Esistono diverse operazioni di mesh che migliorano le prestazioni di disegno e l'aspetto di una superficie. Sono inoltre disponibili diversi altri concetti di mesh che avranno effetto sulla funzionalità delle operazioni di mesh. La comprensione di questi concetti di mesh in modo da poterli applicare migliorerà le prestazioni della mesh.

## <a name="mesh-object-data"></a>Mesh Object Data

Una mesh contiene un vertex buffer, un index buffer e un buffer di attributi.

-   Il buffer dei vertici contiene i dati dei vertici, ovvero i vertici della mesh.
-   L index buffer contiene indici dei vertici per l'accesso al vertex buffer. In questo modo è possibile ridurre le dimensioni del buffer dei vertici riducendo i vertici duplicati. Solo una mesh indicizzata usa il index buffer. Se una mesh è fatta di un elenco di triangoli, ad esempio, non usa il index buffer.
-   Il buffer dell'attributo contiene i dati degli attributi. Gli attributi sono proprietà dei vertici della mesh, in nessun ordine specifico. Una mesh D3DX archivia gli attributi in un gruppo di DWORD, per ogni viso.

### <a name="attribute-tables"></a>Tabelle degli attributi

Una tabella di attributi è una rappresentazione concisa del contenuto di un buffer di attributi. È possibile creare tabelle di attributi chiamando uno dei metodi Optimize con D3DXMESHOPT ATTRSORT, bloccando il buffer dell'attributo e compilando i dati oppure chiamando \_ SetAttributeTable. Una mesh contiene una tabella di attributi quando la mesh viene riordinata in gruppi. Ciò si verifica quando viene chiamato Optimize, presupponendo che sia specificata un'opzione di ordinamento degli attributi (D3DXMESHOPT ATTRSORT o versione \_ successiva). Le mesh D3DX usano elenchi di triangoli indicizzati e vengono pertanto disegnate con [**IDirect3DDevice9::D rawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive).

Le tabelle degli attributi vengono create come risultato della chiamata a Optimize. Non è necessario che i visi siano adiacenti, perché Optimize li riordinerà in modo che siano adiacenti. Ad esempio, le mani di una mesh umana possono usare lo stesso attributo. L'ID consente di ordinare i visi in gruppi. Le mesh dei file con estensione x hanno attributi generati automaticamente per le proprietà del materiale e della trama. Per ottenere prestazioni ottimali, è necessario chiamare Optimize(ATTRSORT) o optimize(VERTEXCACHE) più efficace. Le funzioni di caricamento provano a presentare i dati nel formato esatto in cui sono stati salvati. Se si usa una mesh basata su vertex buffer/index buffer, l'API mesh offre funzioni di ottimizzazione e trasformazioni di skinning con un sovraccarico ridotto.

I tipi di ottimizzazione sono cumulativi, a partire dal meno ottimale (D3DXMESHOPT COMPACT) al più ottimale \_ (D3DXMESHOPT \_ IGNOREVERTS). D3DXMESHOPT \_ STRIPREORDER esegue una compattazione e un ordinamento degli attributi. È sempre consigliabile utilizzare D3DXMESHOPT VERTEXCACHE, anche nei dispositivi \_ senza una vera cache dei vertici.

## <a name="application-data"></a>Dati applicazione

I dati dell'applicazione sono dati mesh gestiti da un'applicazione. Esiste un accoppiamento stretto tra i dati dei vertici della mesh e i dati gestiti da questi buffer.

Il buffer dei materiali contiene n materiali. I materiali vengono restituiti dalla funzione Load quando viene caricato il file con estensione x. Ogni subset può avere materiali e trame propri. Il buffer dei materiali è statico.

Il buffer di adienza contiene informazioni su bordi, visi e visi adiacenti. Alcune operazioni di mesh dipendono dalla conoscenza dei visi adiacenti. Queste informazioni, denominate dati di adizia, vengono conservate in un buffer di adienza. Non fa parte della mesh, ma viene gestita dall'applicazione e deve essere fornita ai metodi mesh quando necessario.

Il buffer dell'istanza degli effetti contiene un elenco di istanze dell'effetto. Un'istanza dell'effetto archivia lo stato. Queste informazioni sullo stato vengono usate per inizializzare la pipeline. Un'istanza dell'effetto contiene coppie nome-valore in un effetto.

## <a name="advanced-mesh-topics"></a>Argomenti avanzati sulla mesh

Le mesh ottimizzate si basano sulla funzionalità mesh di base e aggiungono la funzionalità di ottimizzazione della cache dei vertici con due metodi: Optimize, che crea una nuova mesh, e OptimizeInPlace, che modifica la mesh originale.

D3DXGeneratePMesh usa l'algoritmo di semplificazione D3DX per generare una mesh progressiva dalla mesh di input. D3DXSimplifyMesh genera una mesh standard del livello di dettaglio specificato da una mesh di input usando lo stesso algoritmo di semplificazione. L'utente ha il controllo sulla metrica di errore usata tramite i pesi specificati per componente per vertice e i pesi specificati per vertice. I pesi per componente vengono moltiplicati rispetto alla parte di errore calcolata per ogni compressione del bordo. I pesi per vertice vengono moltiplicati rispetto al valore della metrica di errore determinato per la rimozione di tale vertice. Ad esempio, se non si vuole mai rimuovere un vertice, impostare il peso di tale vertice specifico su un valore elevato. Viceversa, se si vuole che venga rimosso in precedenza, impostarlo su un valore piccolo (minore di 1).

[**ID3DXSkinInfo**](id3dxskininfo.md) supporta i caratteri con interfaccia. Un carattere con interfaccia è definito da un set di mesh e da un set di ossi che influiscono sui vertici delle mesh. Le erre sono rappresentate come gerarchia di trasformazione. Per ogni mesh è presente una matrice per ogni osso che la interessa, che trasforma la mesh nello spazio locale delle coordinate dell'osso. Questa matrice è la trasformazione dello spazio osseo dell'osso per la mesh. Questo viene definito nel momento in cui lo scheletro è associato alla mesh nel processo di creazione.

### <a name="skinning"></a>Scuoiatura

La skinning è una tecnica per trasformare i vertici della mesh usando le esche. Le ossee sono in genere disposte in uno scheletro gerarchico, proprio come le ossee in un corpo umano. I vertici dell'oggetto vengono quindi associati all'osso, ad esempio associando l'interfaccia all'osso. Quando le esche vengono trasformate, anche l'interfaccia viene trasformata.

Le mesh con interfaccia usano gli ossi per influenzare un numero di vertici. I dati di trasformazione delle ossee vengono forniti dall'utente, per influenzare la modalità di SRT delle ossee. La mesh usa gli ossi trasformati per influenzare i vertici associati alle esche. I palette sono matrici di trasformazioni SRT. I tavolozze vengono spesso implementati come matrici, ma possono contenere valori SRT.

### <a name="progressive-mesh-trimming"></a>Trimming mesh progressivo

Le aree con dettagli bassi possono permettersi di perdere i vertici che non modificano l'aspetto sottoposto a rendering della superficie. Ciò vale soprattutto per gli oggetti che si spostano più lontano dalla fotocamera. Questa operazione viene definita livello di dettaglio. Gli utenti hanno controlli di rendering a livello di API per impostare il livello di dettaglio per ottimizzare l'efficienza del rendering.

Gli oggetti mesh progressivi iniziano con un numero elevato di visi e usano la semplificazione per ridurre il numero di visi. Una mesh progressiva indipendente dalla visualizzazione viene definita mesh progressiva indipendente dalla visualizzazione (VIPM).

Un altro modo per ridurre il numero di visi è il taglio. In questo modo i vertici e i visi vengono effettivamente rimossi dalla mesh. Il trimming può essere eseguito all'estremità alta (per limitare il numero massimo di visi) o all'estremità bassa (per limitare il numero minimo di visi). Il trimming migliora le prestazioni di disegno, tuttavia è consigliabile usare attenzione per mantenere la qualità dell'oggetto visivo. Il trimming è illustrato nell'esempio progressive mesh SDK.

Per le aree con visibilità elevata, la risoluzione può essere aumentata usando il livello di dettaglio progressivo (PLOD). Si tratta di una tecnica per suddividere un singolo viso in due visi.

### <a name="patch-meshes"></a>Applicare patch alle mesh

Sono supportati anche due tipi specializzati di mesh patch: patch rettangolari e triangoli. La mesh patch rettangolare è una mesh patch i cui punti di controllo sono disposti in una sequenza rettangolare tortuosa. Le patch rettangolari e triangolo vengono usate per creare superfici di alto ordine. Non vengono comunemente usati come mesh a triangolo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 
