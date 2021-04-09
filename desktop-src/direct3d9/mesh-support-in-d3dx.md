---
description: D3DX è una libreria di utilità che fornisce servizi di supporto. Si tratta di un livello sopra il componente Direct3D.
ms.assetid: 7892370f-0807-4ab7-b7cd-a7e1182e3f9c
title: Supporto mesh in D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0b2b1dd0e5d4c5a212005afe400bb559f1689a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965464"
---
# <a name="mesh-support-in-d3dx-direct3d-9"></a>Supporto mesh in D3DX (Direct3D 9)

D3DX è una libreria di utilità che fornisce servizi di supporto. Si tratta di un livello sopra il componente Direct3D.

## <a name="meshes"></a>Mesh

D3DX implementa il costrutto mesh per caricare, modificare ed eseguire il rendering del contenuto del file con estensione x. Una mesh è fondamentalmente una raccolta di vertici che definiscono alcune geometria e un set di indici che definiscono i visi. Sono disponibili diversi tipi di mesh.

[**ID3DXBaseMesh**](id3dxbasemesh.md) fornisce le nozioni di base. [**ID3DXMesh**](id3dxmesh.md) eredita da ID3DXBaseMesh e aggiunge l'ottimizzazione della mesh usando la cache dei vertici per chip. [**ID3DXSkinInfo**](id3dxskininfo.md) fornisce supporto mesh con skin.

[**ID3DXBaseMesh**](id3dxbasemesh.md) fornisce metodi per modificare ed eseguire query sugli oggetti mesh [**ID3DXMesh**](id3dxmesh.md) che ereditano dalla mesh di base. Sono incluse le operazioni adiacenza, il recupero del buffer di geometria, le operazioni di blocco/sblocco (vertice e indice) e le informazioni di copia, rendering, viso e vertice.

> [!Note]  
> Le interfacce ID3DXPMesh e ID3DXSPMesh (per supportare le mesh progressive e semplificate, rispettivamente) disponibili nelle versioni precedenti di Direct3D 9 sono state eliminate.

 

## <a name="mesh-architecture"></a>Architettura Mesh

Una mesh contiene i dati per un modello complesso. Si tratta di un contenitore di dati astratto che contiene risorse quali trame e materiali e attributi come i dati di posizione e i dati adiacenza. Sono disponibili diverse operazioni di mesh che consentono di migliorare le prestazioni del disegno e l'aspetto di una superficie. Sono inoltre disponibili numerosi altri concetti di mesh che influiscono sulla funzionalità delle operazioni mesh. Comprendere questi concetti di mesh per poterli applicare consente di migliorare le prestazioni della rete.

## <a name="mesh-object-data"></a>Dati oggetto mesh

Una mesh contiene un buffer di vertici, un buffer di indice e un buffer dell'attributo.

-   Il buffer dei vertici contiene i dati dei vertici, ovvero i vertici della mesh.
-   Il buffer di indice contiene gli indici dei vertici per accedere al buffer del vertice. Questo consente di ridurre le dimensioni del buffer dei vertici riducendo i vertici duplicati. Solo una mesh indicizzata usa il buffer di indice. Se una mesh è costituita da un elenco di triangolo, ad esempio, non usa il buffer di indice.
-   Il buffer dell'attributo contiene i dati dell'attributo. Gli attributi sono proprietà dei vertici mesh, in nessun ordine particolare. Una mesh D3DX archivia gli attributi in un gruppo di DWORD, per ogni faccia.

### <a name="attribute-tables"></a>Tabelle degli attributi

Una tabella attribute è una rappresentazione concisa del contenuto di un buffer di attributo. È possibile creare tabelle degli attributi chiamando uno dei metodi optimize con D3DXMESHOPT \_ ATTRSORT, bloccando il buffer dell'attributo e inserendo i dati oppure chiamando SetAttributeTable. Una mesh contiene una tabella di attributi quando la mesh viene riordinata in gruppi. Questo errore si verifica quando viene chiamato Optimize, presupponendo che venga specificata un'opzione di ordinamento degli attributi (D3DXMESHOPT \_ ATTRSORT o versione successiva). Le mesh D3DX usano elenchi di triangolo indicizzati e vengono quindi disegnate con [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive).

Le tabelle degli attributi vengono create come risultato della chiamata a optimize. Non è necessario che i visi siano adiacenti, perché Optimize li riordina per essere adiacenti. Ad esempio, le mani di una mesh umana potrebbero utilizzare lo stesso attributo. L'ID consente di ordinare i visi in gruppi. Le mesh da file con estensione x contengono automaticamente attributi generati per le proprietà Material e texture. Per ottenere prestazioni ottimali, è necessario chiamare Optimize (ATTRSORT) o ottimizzazione più efficace (VERTEXCACHE). Le funzioni di caricamento tentano di presentare i dati nel formato esatto in cui sono stati salvati. Se si usa una mesh basata su vertex buffer/index buffer, l'API mesh fornisce le funzioni di ottimizzazione e le trasformazioni di skinning con un sovraccarico ridotto.

I tipi di ottimizzazione sono cumulativi, a partire dal meno ottimale (D3DXMESHOPT \_ Compact) al più ottimale (D3DXMESHOPT \_ IGNOREVERTS). D3DXMESHOPT \_ STRIPREORDER esegue una compattazione e un ordinamento degli attributi. \_È sempre consigliabile usare D3DXMESHOPT VERTEXCACHE, anche nei dispositivi senza una vera cache dei vertici.

## <a name="application-data"></a>Dati applicazione

I dati dell'applicazione sono dati mesh gestiti da un'applicazione. Esiste un accoppiamento stretto tra i dati del vertice mesh e i dati gestiti da tali buffer.

Il buffer di materiali contiene n materiali. I materiali vengono restituiti dalla funzione Load quando viene caricato il file con estensione x. Ogni subset può avere materiali e trame propri. Il buffer dei materiali è statico.

Il buffer adiacenza contiene informazioni su bordi, visi e visi adiacenti. Alcune operazioni di mesh dipendono dalla conoscenza dei visi adiacenti. Queste informazioni, denominate dati adiacenza, vengono mantenute in un buffer adiacenza. Non fa parte della mesh, ma viene gestita dall'applicazione e deve essere fornita ai metodi Mesh quando necessario.

Il buffer dell'istanza di Effects contiene un elenco di istanze di effetto. Un'istanza dell'effetto archivia lo stato. Queste informazioni sullo stato vengono usate per inizializzare la pipeline. Un'istanza dell'effetto contiene coppie nome-valore in un effetto.

## <a name="advanced-mesh-topics"></a>Argomenti su mesh avanzati

Le reti ottimizzate si basano sulla funzionalità mesh di base e aggiungono funzionalità di ottimizzazione della cache Vertex con due metodi: Optimize, che crea una nuova mesh e OptimizeInPlace, che modifica la mesh originale.

D3DXGeneratePMesh usa l'algoritmo di semplificazione D3DX per generare una mesh progressiva dalla mesh di input. D3DXSimplifyMesh genera una mesh standard del livello di dettaglio specificato da una mesh di input usando lo stesso algoritmo di semplificazione. L'utente ha il controllo sulla metrica di errore usata nei pesi specificati per componente e pesi specificati per vertice. Il peso dei singoli componenti viene moltiplicato per la parte relativa ai componenti dell'errore calcolato per ogni compressione perimetrale. I pesi per vertice vengono moltiplicati per il valore della metrica di errore determinato per la rimozione del vertice. Se, ad esempio, non si vuole mai rimuovere un vertice, impostare il peso di tale vertice su un valore elevato. Viceversa, se si vuole che venga rimossa in precedenza, impostarla su un valore ridotto (minore di 1).

[**ID3DXSkinInfo**](id3dxskininfo.md) supporta caratteri con skinning. Un carattere con skinning viene definito da un set di mesh e da un set di ossa che interessano i vertici dei mesh. Le ossa sono rappresentate come una gerarchia di trasformazione. Per ogni mesh è presente una matrice per ogni osso che lo influiscono, che trasforma la mesh nello spazio delle coordinate locale dell'osso. Questa matrice è la trasformazione dello spazio osseo dell'osso per la mesh. Questa operazione viene definita nel momento in cui lo scheletro è associato alla mesh nel processo di creazione.

### <a name="skinning"></a>Scuoiatura

Il skining è una tecnica per trasformare i vertici mesh usando Bones. Le ossa vengono in genere disposte in una struttura gerarchica, in modo analogo alle ossa in un corpo umano. I vertici degli oggetti vengono quindi associati alle ossa, ad esempio l'associazione dell'interfaccia all'osso. Quando si trasformano le ossa, viene anche trasformata l'interfaccia.

Le mesh con skin usano le ossa per influenzare un certo numero di vertici. I dati della trasformazione ossea vengono forniti dall'utente per influenzare come SRT le ossa. La mesh usa le ossa trasformate per influenzare i vertici associati alle ossa. Le tavolozze sono matrici di trasformazioni SRT. Le tavolozze vengono spesso implementate come matrici, ma possono contenere valori SRT.

### <a name="progressive-mesh-trimming"></a>Trimming progressivo della rete

Le aree con dettagli limitati possono permettersi di perdere i vertici che non modificano l'aspetto di rendering della superficie. Ciò vale soprattutto per gli oggetti man mano che si spostano più lontano dalla fotocamera. Questa operazione viene definita come livello di dettaglio. Gli utenti dispongono di controlli di rendering a livello di API per l'impostazione del livello di dettaglio per ottimizzare l'efficienza del rendering.

Gli oggetti mesh progressivi iniziano con un numero elevato di visi e usano la semplificazione per ridurre il numero di visi. Una mesh progressiva indipendente dalla visualizzazione è indicata come una mesh progressiva indipendente dalla visualizzazione (VIPM).

Un altro modo per ridurre il numero di visi consiste nel taglio. Questa operazione rimuove effettivamente i vertici e i visi dalla mesh. Il trimming può essere eseguito alla fine superiore (per limitare il numero massimo di visi) o nell'estremità inferiore (per limitare il numero minimo di visi). Il trimming migliora le prestazioni di elaborazione, tuttavia è consigliabile usare la cura per mantenere la qualità visiva. Il trimming è illustrato nell'esempio progressive mesh SDK.

Per le aree con visibilità elevata, è possibile aumentare la risoluzione utilizzando il livello di dettaglio progressivo (ARRANCARE). Si tratta di una tecnica per suddividere una singola faccia in due visi.

### <a name="patch-meshes"></a>Mesh patch

Sono supportati anche due tipi specializzati di mesh di patch, ovvero le patch rettangolo e triangolo. La mesh patch rettangolo è una mesh di patch i cui punti di controllo sono disposti in una sequenza rettangolare di avvolgimento. Le patch rettangolari e triangolari vengono usate per creare superfici di ordine superiore. Non sono comunemente usati come mesh di triangolo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 
