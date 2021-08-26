---
description: La pagina seguente offre una struttura di base delle differenze principali tra Direct3D 9 e Direct3D 10. La struttura seguente offre alcune informazioni utili agli sviluppatori con l'esperienza Direct3D 9 per esplorare e correlare a Direct3D 10.
ms.assetid: 283b54e0-94cb-47a8-8cfc-5798e0538b9f
title: Considerazioni da Direct3D 9 a Direct3D 10 (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6c2dac7da24184bb5cc6a78f8e7d391c7d0f8b7000107915ba5a606188dcf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120011"
---
# <a name="direct3d-9-to-direct3d-10-considerations-direct3d-10"></a>Considerazioni da Direct3D 9 a Direct3D 10 (Direct3D 10)

La pagina seguente offre una struttura di base delle differenze principali tra Direct3D 9 e Direct3D 10. La struttura seguente offre alcune informazioni utili agli sviluppatori con l'esperienza Direct3D 9 per esplorare e correlare a Direct3D 10.

Anche se le informazioni in questo argomento confrontano Direct3D 9 con Direct3D 10, poiché Direct3D 11 si basa sui miglioramenti apportati in Direct3D 10 e 10.1, queste informazioni sono necessarie anche per eseguire la migrazione da Direct3D 9 a Direct3D 11. Per informazioni sul passaggio da Direct3D 10 a Direct3D 11, vedere [Migrazione a Direct3D 11.](../direct3d11/d3d11-programming-guide-migrating.md)

-   [Panoramica delle principali modifiche strutturali in Direct3D 10](#overview-of-the-major-structural-changes-in-direct3d-10)
    -   [Rimozione della funzione fissa](#removal-of-fixed-function)
    -   [Convalida dell'ora di creazione dell'oggetto dispositivo](#device-object-creation-time-validation)
-   [Astrazioni motore/Separazione](/windows)
    -   [Rimozione diretta delle dipendenze Direct3D 9](#direct-removal-of-direct3d-9-dependencies)
-   [Consigli per la risoluzione rapida dei problemi di compilazione delle applicazioni](#tricks-for-quickly-resolving-application-build-issues)
    -   [Override dei tipi Direct3D 9](#overriding-direct3d-9-types)
    -   [Risoluzione dei problemi di collegamento](#resolving-link-issues)
    -   [Simulazione di CAP del dispositivo](#simulating-device-caps)
-   [Gestione dell'API Direct3D 10](#driving-the-direct3d-10-api)
    -   [Creazione di risorse](#resource-creation)
    -   [Visualizzazioni](#views)
    -   [Accesso a risorse statiche e dinamiche](#static-versus-dynamic-resource-access)
    -   [Effetti Direct3D 10](#direct3d-10-effects)
    -   [HLSL senza effetti](#hlsl-without-effects)
    -   [Compilazione shader](#shader-compilation)
    -   [Creazione di risorse shader](#creation-of-shader-resources)
    -   [Interfaccia del livello reflection shader](#shader-reflection-layer-interface)
    -   [Layout dell'assembler di input - Collegamento vertex shader/flusso di input](/windows)
    -   [Impatto della rimozione del codice in errore dello shader](#impact-of-shader-dead-code-removal)
    -   [Esempio di struttura di input vertex shader](#vertex-shader-input-structure-example)
    -   [Creazione di oggetti di stato](#state-object-creation)
-   [Porting di trame](#porting-textures)
    -   [Formati di file supportati](#file-formats-supported)
    -   [Mapping dei formati di trama](#mapping-texture-formats)
-   [Porting di shader](#porting-shaders)
    -   [Gli shader Direct3D 10 vengono creati in HLSL](#direct3d-10-shaders-are-authored-in-hlsl)
    -   [Firme e collegamento shader](#shader-signatures-and-linkage)
    -   [Collegamenti alla fase dello shader HLSL](#hlsl-shader-stage-linkages)
    -   [Buffer costanti](#constant-buffers)
    -   [Piani di ritaglio utente in HLSL a livello di funzionalità 9 e superiore](#user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Altre differenze di Direct3D 10 da controllare](#additional-direct3d-10-differences-to-watch-for)
    -   [Numeri interi come input](#integers-as-input)
    -   [Cursori del mouse](#mouse-cursors)
    -   [Mapping di Texel ai pixel in Direct3D 10](#mapping-texels-to-pixels-in-direct3d-10)
    -   [Modifiche al comportamento del conteggio dei riferimenti](#reference-counting-behavior-changes)
    -   [Testare il livello cooperativo](#test-cooperative-level)
    -   [StretchRect](#stretchrect)
-   [Differenze aggiuntive di Direct3D 10.1](#additional-direct3d-101-differences)
-   [Argomenti correlati](#related-topics)

## <a name="overview-of-the-major-structural-changes-in-direct3d-10"></a>Panoramica delle principali modifiche strutturali in Direct3D 10

-   [Rimozione della funzione fissa](#removal-of-fixed-function)
-   [Convalida dell'ora di creazione dell'oggetto dispositivo](#device-object-creation-time-validation)

Il processo di rendering con il dispositivo Direct3D 10 è strutturalmente simile a Direct3D 9.

-   Impostare un'origine flusso vertice
-   Impostare il layout di input in Direct3D 10 (impostare la dichiarazione del flusso dei vertici in Direct3D 9)
-   Dichiarare la topologia primitiva
-   Impostare le trame
-   Impostare gli oggetti di stato
-   Impostare shader
-   Disegna

La [**chiamata Draw**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw) consente di riunire le operazioni. L'ordinamento delle chiamate prima della chiamata Draw è arbitrario. Le principali differenze nella progettazione dell'API Direct3D 10 sono le seguenti:

-   Rimozione della funzione fissa
-   Rimozione dei bit CAPS: il set di funzionalità di base di Direct3D 10 è garantito
-   Gestione più rigida di: accesso alle risorse, stato del dispositivo, costanti shader, collegamento di shader (input e output agli shader) tra le fasi
-   Le modifiche del nome del punto di ingresso api riflettono l'uso della memoria GPU virtuale (Map() anziché Lock()).
-   È possibile aggiungere un livello di debug al dispositivo al momento della creazione
-   La topologia primitiva è ora uno stato esplicito (separato dalla [**chiamata Draw)**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw)
-   Le costanti shader esplicite vengono ora archiviate in buffer costanti
-   La creazione di shader viene eseguita interamente in HLSL. Il compilatore HLSL si trova ora nella DLL Direct3D 10 primaria.
-   Nuova fase programmabile: geometry shader
-   Rimozione di BeginScene()/EndScene()
-   Funzionalità comuni di gestione 2D, dello stato attivo e dell'adapter implementate in un nuovo componente: DXGI

### <a name="removal-of-fixed-function"></a>Rimozione della funzione fissa

A volte è sorprendente che anche in un motore Direct3D 9 che sfrutta completamente la pipeline programmabile rimangano diverse aree che dipendono dalla pipeline a funzione fissa (FF). Le aree più comuni sono in genere correlate al rendering allineato allo spazio dello schermo per l'interfaccia utente. È per questo motivo che è probabile che sia necessario compilare uno shader di emulazione FF o un set di shader che forniscono i comportamenti di sostituzione necessari.

Questa documentazione contiene un white paper che contiene origini shader sostitutive per i comportamenti FF più comuni (vedere [Fixed Function EMU Sample](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx)). Alcuni comportamenti dei pixel a funzione fissa, incluso il test alfa, sono stati spostati negli shader.

### <a name="device-object-creation-time-validation"></a>Convalida dell'ora di creazione dell'oggetto dispositivo

La pipeline Direct3D 10 è stata riprogettata da zero nell'hardware e nel software con l'intenzione principale di ridurre il sovraccarico della CPU (in fase di disegno). Per ridurre i costi, a tutti i tipi di dati del dispositivo è stato assegnato un oggetto con metodi di creazione espliciti forniti dal dispositivo stesso. In questo modo viene abilitata la convalida dei dati rigida al momento della creazione dell'oggetto anziché durante la chiamata di disegno, come accade spesso con Direct3D 9.

## <a name="engine-abstractions--separation"></a>Astrazioni motore/Separazione

Le applicazioni, inclusi i giochi, che vogliono supportare Sia Direct3D 9 che Direct3D 10 devono avere i livelli di rendering astratti dal resto della codebase. Esistono molti modi per ottenere questo risultato, ma la chiave per tutti è la progettazione del livello di astrazione per il dispositivo Direct3D di livello inferiore. Tutti i sistemi devono comunicare con l'hardware tramite il livello comune, progettato per fornire risorse GPU e la gestione dei tipi di basso livello.

### <a name="direct-removal-of-direct3d-9-dependencies"></a>Rimozione diretta delle dipendenze Direct3D 9

Quando si esegue la portabilità di codebase di grandi dimensioni testate in precedenza, è importante ridurre al minimo la quantità di modifiche del codice a quelle assolutamente necessarie per mantenere i comportamenti testati in precedenza nel codice. Le procedure consigliate includono la documentazione chiara dei casi in cui gli elementi cambiano usando i commenti. È spesso utile avere uno standard di commenti per questo lavoro che consente di passare rapidamente attraverso la codebase.

Di seguito è riportato un elenco di esempio di commenti standard a riga singola/blocco iniziale che possono essere usati per questo lavoro.



| Elemento                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="___Direct3D_10_REMOVED"></span><span id="___direct3d_10_removed"></span><span id="___DIRECT3D_10_REMOVED"></span>Direct3D 10 RIMOSSO<br/>                     | Usare questa opzione quando vengono rimosse righe/blocchi di codice<br/>                                                                                                                                                                                                                                                                   |
| <span id="___Direct3D_10_NEEDS_UPDATE"></span><span id="___direct3d_10_needs_update"></span><span id="___DIRECT3D_10_NEEDS_UPDATE"></span>Direct3D 10 NEEDS UPDATE<br/> | Consente di aggiungere altre note al commento NEED UPDATE che suggerisce il lavoro o la nuova API da usare per le visite successive al codice per la conversione del comportamento. È consigliabile usare anche assert(**false**) quando si verifica l'aggiornamento di \\ DIRECT3D 10 NEEDS UPDATE per assicurarsi di non eseguire inconsapevolmente \\ codice errante<br/> |
| <span id="___Direct3D_10_CHANGED"></span><span id="___direct3d_10_changed"></span><span id="___DIRECT3D_10_CHANGED"></span>Direct3D 10 MODIFICATO<br/>                     | Le aree in cui sono state apportate modifiche importanti devono essere mantenute per riferimento futuro, ma impostare come commento<br/>                                                                                                                                                                                                                       |
| <span id="___Direct3D_10_END"></span><span id="___direct3d_10_end"></span><span id="___DIRECT3D_10_END"></span>Direct3D 10 END<br/>                                     | Qualificatore del blocco di codice finale<br/>                                                                                                                                                                                                                                                                                            |



 

Per più righe di origine è consigliabile usare anche i commenti //in stile C, ma aggiungere i commenti di inizio/fine pertinenti \* \* per queste aree.

## <a name="tricks-for-quickly-resolving-application-build-issues"></a>Consigli per la risoluzione rapida dei problemi di compilazione delle applicazioni

-   [Override dei tipi Direct3D 9](#overriding-direct3d-9-types)
-   [Risoluzione dei problemi di collegamento](#resolving-link-issues)
-   [Simulazione di CAP del dispositivo](#simulating-device-caps)

### <a name="overriding-direct3d-9-types"></a>Override dei tipi Direct3D 9

Può essere utile inserire un file di intestazione di alto livello contenente definizioni/override dei tipi per i tipi di base Direct3D 9 che non sono più supportati dalle intestazioni Direct3D 10. Ciò consente di ridurre al minimo la quantità di modifiche nel codice e nelle interfacce in cui è presente un mapping diretto da un tipo Direct3D 9 al tipo Direct3D 10 appena definito. Questo approccio è utile anche per mantenere insieme i comportamenti del codice in un unico file di origine. In questo caso, è consigliabile definire tipi indipendenti dalla versione o denominati in genere che descrivono costrutti comuni usati per il rendering, ma si estendono su entrambe le API Direct3D 9 e Direct3D 10. Esempio:


```
#if defined(D3D9)
typedef IDirect3DIndexBuffer9   IDirect3DIndexBuffer;
typedef IDirect3DVertexBuffer9  IDirect3DVertexBuffer;
#else //D3D10
typedef ID3D10Buffer            IDirect3DIndexBuffer;
typedef ID3D10Buffer            IDirect3DVertexBuffer
#endif
```



Altri esempi specifici di Direct3D 10 includono:


```
typedef ID3D10TextureCube   IDirect3DCubeTexture;
typedef ID3D10Texture3D     IDirect3DVolumeTexture;
typedef D3D10_VIEWPORT      D3DVIEWPORT;
typedef ID3D10VertexShader  IDirect3DVertexShader;
typedef ID3D10PixelShader   IDirect3DPixelShader;
```



### <a name="resolving-link-issues"></a>Risoluzione dei problemi di collegamento

È consigliabile sviluppare applicazioni Direct3D 10 e Windows Vista usando la versione più recente di Microsoft Visual Studio. Tuttavia, è possibile compilare un'applicazione Windows Vista che dipende da Direct3D 10 usando la versione precedente 2003 di Visual Studio. Direct3D 10 è un componente della piattaforma Windows Vista con dipendenze (come con l'SDK della piattaforma Server 2003 SP1) nella libreria seguente: BufferOverflowU.lib è necessario per risolvere eventuali problemi del linker di controllo di sicurezza del \_ buffer.

### <a name="simulating-device-caps"></a>Simulazione di CAP del dispositivo

Molte applicazioni contengono aree di codice che dipendono dai dati CAPS del dispositivo disponibili. Per risolvere questo problema, eseguire l'override dell'enumerazione dei dispositivi e forzare i CAP del dispositivo a valori sensibili. Pianificare di visitare di nuovo le aree in cui sono presenti dipendenze da CAPS in un secondo momento per la rimozione completa di CAPS, laddove possibile.

## <a name="driving-the-direct3d-10-api"></a>Gestione dell'API Direct3D 10

Questa sezione è incentrata sulle modifiche del comportamento causate dall'API Direct3D 10.

-   [Creazione di risorse](#resource-creation)
-   [Visualizzazioni](#views)
-   [Accesso a risorse statiche e dinamiche](#static-versus-dynamic-resource-access)
-   [Effetti Direct3D 10](#direct3d-10-effects)
-   [HLSL senza effetti](#hlsl-without-effects)
-   [Compilazione shader](#shader-compilation)
-   [Creazione di risorse shader](#creation-of-shader-resources)
-   [Interfaccia del livello reflection shader](#shader-reflection-layer-interface)
-   [Layout dell'assembler di input - Collegamento vertex shader/flusso di input](/windows)
-   [Impatto della rimozione del codice in errore dello shader](#impact-of-shader-dead-code-removal)
-   [Esempio di struttura di input vertex shader](#vertex-shader-input-structure-example)
-   [Creazione di oggetti di stato](#state-object-creation)

### <a name="resource-creation"></a>Creazione di risorse

L'API Direct3D 10 ha progettato le risorse come tipi di buffer generici che hanno flag di associazione specifici in base all'utilizzo pianificato. Questo punto di progettazione è stato scelto per facilitare l'accesso quasi comune alle risorse nella pipeline per scenari come il rendering in un buffer dei vertici, quindi per disegnare immediatamente i risultati senza interrompere la CPU. L'esempio seguente illustra l'allocazione di buffer dei vertici e index buffer in cui è possibile vedere che la descrizione della risorsa differisce solo per i flag di associazione di risorse GPU.

L'API Direct3D 10 ha fornito metodi helper di trama per creare in modo esplicito le risorse del tipo di trama, ma come si può immaginare, si tratta di funzioni helper.

-   CreateTexture2D()
-   CreateTextureCube()
-   CreateTexture3D()

Quando si usa Direct3D 10 come destinazione, è probabile che si voglia allocare più elementi durante la creazione delle risorse rispetto a quelli usati con Direct3D 9. Questo diventerà più evidente con la creazione di buffer di destinazione di rendering e trame in cui è necessario creare anche una visualizzazione per l'accesso al buffer e l'impostazione della risorsa nel dispositivo.

[Esercitazione 1: Nozioni di base su Direct3D 10](https://msdn.microsoft.com/library/Ee416436(v=VS.85).aspx)

> [!Note]  
> Direct3D 10 e versioni successive di Direct3D estendono il formato di file DDS per supportare nuovi formati DXGI, matrici di trame e matrici di mappe cubi. Per altre informazioni sull'estensione di formato di file DDS, vedere la [Guida alla programmazione per DDS.](../direct3ddds/dx-graphics-dds-pguide.md)

 

### <a name="views"></a>Viste

Una visualizzazione è un'interfaccia tipiata in modo specifico per i dati archiviati in un buffer pixel. Una risorsa può avere diverse visualizzazioni allocate contemporaneamente e questa funzionalità è evidenziata nell'esempio Single Pass Render to Cubemap contenuto in questo SDK.

[Pagina della Guida per i programmatori sull'accesso alle risorse](d3d10-graphics-programming-guide-resources-access-views.md)

[Esempio cubeMap](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)

### <a name="static-versus-dynamic-resource-access"></a>Accesso a risorse statiche e dinamiche

Per prestazioni ottimali, le applicazioni devono partizionare l'uso dei dati in termini di natura statica e dinamica dei dati. Direct3D 10 è stato progettato per sfruttare questo approccio e, di conseguenza, le regole di accesso per le risorse sono state notevolmente limitate rispetto a Direct3D 9. Per le risorse statiche è consigliabile popolare la risorsa con i relativi dati durante la fase di creazione. Se il motore è stato progettato in base al punto di progettazione Crea, Blocca, Riempi, Sblocca di Direct3D 9, è possibile rinviare il popolamento da Ora di creazione usando una risorsa di staging e il metodo UpdateSubResource nell'interfaccia della risorsa.

### <a name="direct3d-10-effects"></a>Effetti Direct3D 10

L'uso del sistema di effetti Direct3D 10 non rientra nell'ambito di questo articolo. Il sistema è stato scritto per sfruttare appieno i vantaggi a livello di architettura offerti da Direct3D 10. Per altri dettagli sull'uso, vedere la sezione Effetti [(Direct3D 10).](d3d10-graphics-programming-guide-effects.md)

### <a name="hlsl-without-effects"></a>HLSL senza effetti

La pipeline shader Direct3D 10 può essere guidata senza l'uso del sistema di effetti Direct3D 10. Si noti che in questa istanza tutte le associazioni costanti di buffer, shader, campionatore e trama devono essere gestite dall'applicazione stessa. Per altri dettagli, vedere il collegamento di esempio e le sezioni seguenti di questo documento:

[Esempio di HLSL senza effetti](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)

### <a name="shader-compilation"></a>Compilazione shader

Il compilatore HLSL Direct3D 10 introduce miglioramenti alla definizione del linguaggio HLSL e pertanto è in grado di operare in due modalità. Per il supporto completo delle funzioni intrinseche e della semantica in stile Direct3D 9, la compilazione deve essere richiamata usando il flag COMPATIBILITY MODE che può essere specificato in base alla compilazione.

La semantica del linguaggio HLSL specifica del modello shader 4.0 e le funzioni intrinseche per Direct3D 10 sono disponibili in [HLSL.](../direct3dhlsl/dx-graphics-hlsl.md) Le principali modifiche alla sintassi da Direct3D 9 HLSL per tenere presente che si tratta di un'area di accesso alla trama. La nuova sintassi è l'unica forma supportata dal compilatore al di fuori della modalità di compatibilità.

> [!Note]  
> Le API di tipo compilatore [**Direct3D 10 ( D3D10CompileShader**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10compileshader) e [**D3D10CompileEffectFromMemory**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10compileeffectfrommemory)) vengono fornite dai runtime Direct3D 10, 10.1 e 11 eseguiti in Windows Vista e versioni successive. Le API di tipo compilatore Direct3D 10 hanno le stesse funzionalità del compilatore HLSL fornito in DirectX SDK (dicembre 2006). Questo compilatore HLSL non supporta i profili Direct3D 10.1 (vs \_ 4 \_ 1, ps \_ 4 \_ 1, gs \_ 4 \_ 1, fx \_ 4 \_ 1) e non include una serie di ottimizzazioni e miglioramenti. È possibile ottenere un compilatore HLSL che supporta i profili Direct3D 10.1 dalla versione legacy più recente [di DirectX SDK.](/previous-versions/windows/apps/hh452744(v=win.10)) Per informazioni su DirectX SDK legacy, vedere [Dove si trova DirectX SDK?](../directx-sdk--august-2009-.md). È possibile ottenere la versione più recente di HLSL Fxc.exe compilatore da riga di comando e le API [D3DCompiler](../direct3dhlsl/dx-graphics-d3dcompiler-reference.md) da Windows SDK.

 

### <a name="creation-of-shader-resources"></a>Creazione di risorse shader

La creazione di istanze di shader compilate all'esterno del sistema di effetti Direct3D 10 viene eseguita in modo molto simile a Direct3D 9, ma in Direct3D 10 è importante mantenere la firma di Input shader per un uso successivo. La firma viene restituita per impostazione predefinita come parte del BLOB dello shader, ma può essere estratta per ridurre i requisiti di memoria, se necessario. Per altri dettagli, vedere [Uso degli shader in Direct3D 10.](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md)

### <a name="shader-reflection-layer-interface"></a>Interfaccia del livello reflection shader

Il livello di reflection shader è l'interfaccia tramite la quale è possibile ottenere informazioni sui requisiti dello shader. Ciò è particolarmente utile quando si creano collegamenti all'assembly di input (vedere di seguito) in cui potrebbe essere necessario attraversare i requisiti di input dello shader per assicurarsi di fornire la struttura di input corretta allo shader. È possibile creare un'istanza dell'interfaccia del livello di reflection contemporaneamente alla creazione di un'istanza di uno shader compilato.

Il livello di reflection shader sostituisce i metodi D3DX9 che forniscono funzionalità simili. Ad [**esempio, IsParameterUsed**](../direct3d9/id3dxeffect--isparameterused.md) viene sostituito dal [**metodo GetDesc.**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-id3d10shaderreflectionvariable-getdesc)

### <a name="input-assembler-layouts---vertex-shader--input-stream-linkage"></a>Layout dell'assembler di input - Collegamento vertex shader/flusso di input

L'assembler di input (IA) sostituisce la dichiarazione del flusso vertice in stile Direct3D 9 e la struttura della descrizione è molto simile nel formato. La differenza principale dell'IA è che l'oggetto layout IA creato deve eseguire direttamente il mapping a un formato specifico della firma di input dello shader. L'oggetto mapping creato per collegare il flusso di input allo shader può essere usato in un numero qualsiasi di shader in cui la firma di input dello shader corrisponde a quella dello shader usato per creare il layout di input.

Per guidare al meglio la pipeline con dati statici, è consigliabile considerare le permutazioni del formato del flusso di input per possibili firme di input shader e creare le istanze dell'oggetto layout IA il prima possibile e riutilizzarle laddove possibile.

### <a name="impact-of-shader-dead-code-removal"></a>Impatto della rimozione del codice in errore dello shader

La sezione seguente indica una differenza significativa tra Direct3D 9 e Direct3D 10 che probabilmente richiederà un'attenta gestione nel codice del motore. Gli shader che contengono espressioni condizionali spesso hanno determinati percorsi di codice rimossi come parte del processo di compilazione. In Direct3D 9 è possibile rimuovere due tipi di input (contrassegnati per la rimozione) quando non vengono usati: input di firma (come nell'esempio seguente) e input costanti. Se la fine del buffer costante contiene voci non utilizzate, la dichiarazione delle dimensioni nello shader rifletterà le dimensioni del buffer costante senza le voci inutilizzate alla fine. Entrambi questi tipi di input rimangono nelle firme o nei buffer costanti Direct3D 10, con un'eccezione speciale nel caso di input costanti inutilizzati alla fine di un buffer costante. Ciò può influire sul motore quando si gestisce shader di grandi dimensioni e si creano layout di input. Gli elementi rimossi dalle ottimizzazioni del codice non valido nel compilatore devono comunque essere dichiarati nella struttura di input. Questo concetto è illustrato nell'esempio seguente:

### <a name="vertex-shader-input-structure-example"></a>Esempio di struttura di input vertex shader


```
struct VS_INPUT
{
float4 pos: SV_Position;
float2 uv1 : Texcoord1;
float2 uv2 : Texcoord2; *
};
```



\* La rimozione del codice non gestito Direct3D 9 rimuove la dichiarazione nello shader a causa della rimozione condizionale del codice non valido


```
float4x4  g_WorldViewProjMtx;
static const bool g_bLightMapped = false; // define a compile time constant

VS_INPUT main(VS_INPUT i) 
{
    VS_INPUT o;
    o.pos = mul( i.pos, g_WorldViewProjMtx);
    o.uv1 = i.uv1;
    if ( g_bLightMapped )
    {
        o.uv2 = i.uv2;
    }
    return o;
}
```



In caso contrario, è possibile rendere ancora più evidente che la costante è una costante in fase di compilazione con la dichiarazione seguente:


```
#define LIGHT_MAPPED false
```



Nell'esempio precedente, in Direct3D 9, l'elemento uv2 verrebbe rimosso a causa di ottimizzazioni del codice non valido nel compilatore. In Direct3D 10 il codice non disponibile verrà comunque rimosso, ma il layout dell'assembler di input shader richiede la definizione dei dati di input. Il livello di reflection shader offre i mezzi per gestire questa situazione in modo generico, in base al quale è possibile attraversare i requisiti di input dello shader e assicurarsi di fornire una descrizione completa del flusso di input per il mapping della firma shader.

Ecco una funzione di esempio per rilevare l'esistenza di un nome/indice semantico in una firma di funzione:


```
// Returns true if the SemanticName / SemanticIndex is used in the input signature.
// pReflector is a previously acquired shader reflection interface.
bool IsSignatureElementExpected(ID3D10ShaderReflection *pReflector, const LPCSTR SemanticName, UINT SemanticIndex)
{
    D3D10_SHADER_DESC               shaderDesc;
    D3D10_SIGNATURE_PARAMETER_DESC  paramDesc;

    Assert(pReflector);
    Assert(SemanticName);

    pReflector->GetDesc(&shaderDesc);

    for (UINT k=0; k<shaderDesc.InputParameters; k++)
    {
        pReflector->GetInputParameterDesc( k, &paramDesc);
        if (wcscmp( SemanticName, paramDesc.SemanticName)==0 && paramDesc.SemanticIndex == SemanticIndex) 
            return true;
    }

    return false;
}
```



### <a name="state-object-creation"></a>Creazione di oggetti di stato

Quando si esegue la porting del codice del motore, può essere utile usare inizialmente un set predefinito di oggetti di stato e disabilitare tutte le impostazioni dello stato di rendering/stato della trama del dispositivo Direct3D 9. Ciò causerà il rendering degli artefatti, ma è il modo più rapido per rendere le operazioni in esecuzione. In un secondo momento è possibile costruire un sistema di gestione degli oggetti di stato che può usare una chiave composta per consentire il riutilizzo massimo del numero di oggetti di stato in uso.

## <a name="porting-textures"></a>Porting trame

### <a name="file-formats-supported"></a>Formati di file supportati

Le funzioni **D3DXxxCreateXXX** e **D3DXxxSaveXXX** che creano o salvano una trama da o in un file di grafica (ad [**esempio, D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)) supportano un set diverso di formati di file in Direct3D 10 rispetto a Direct3D 9:



| Formato file | Direct3D 9 | Direct3D 10 |
|-------------|------------|-------------|
| bmp        | x          | x           |
| jpg        | x          | x           |
| .tga        | x          |             |
| png        | x          | x           |
| .dds        | x          | x           |
| PPM        | x          |             |
| dib        | x          |             |
| .hdr        | x          |             |
| .pfm        | x          |             |
| tiff       |            | x           |
| gif        |            | x           |
| tif        |            | x           |



 

Per informazioni dettagliate, confrontare le enumerazioni Direct3D 9 [**D3DXIMAGE \_ FILEFORMAT**](../direct3d9/d3dximage-fileformat.md) con le enumerazioni [**D3DX10 \_ IMAGE FILE \_ \_ FORMAT**](d3dx10-image-file-format.md) per Direct3D 10.

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8. Per l'elaborazione di file di trama, è consigliabile usare [DirectXTex](https://github.com/Microsoft/DirectXTex).

 

### <a name="mapping-texture-formats"></a>Mapping dei formati di trama

La tabella seguente illustra il mapping dei formati di trama da Direct3D 9 a Direct3D 10. Qualsiasi contenuto in formati non disponibili in DXGI dovrà essere convertito dalle routine dell'utilità.



| Formato Direct3D 9                   | Formato Direct3D 10                                                                                                                                                                                                                                   |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DFMT \_ UNKNOWN                     | FORMATO DXGI \_ \_ SCONOSCIUTO                                                                                                                                                                                                                                |
| D3DFMT \_ R8G8B8                      | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ A8R8G8B8                    | FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM & DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB¹                                                                                                                                                                                 |
| D3DFMT \_ X8R8G8B8                    | FORMATO DXGI \_ \_ B8G8R8X8X8 \_ UNORM & FORMATO DXGI \_ \_ B8G8R8X8 \_ UNORM \_ SRGB¹                                                                                                                                                                                 |
| D3DFMT \_ R5G6B5                      | FORMATO DXGI \_ \_ B5G6R5 \_ UNORM²                                                                                                                                                                                                                         |
| D3DFMT \_ X1R5G5B5                    | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ A1R5G5B5                    | FORMATO DXGI \_ \_ B5G5R5A1 \_ UNORM²                                                                                                                                                                                                                       |
| D3DFMT \_ A4R4G4B4                    | FORMATO DXGI \_ \_ B4G4R4A4 \_ UNORM³                                                                                                                                                                                                                       |
| D3DFMT \_ R3G3B2                      | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ A8                          | FORMATO DXGI \_ \_ A8 \_ UNORM                                                                                                                                                                                                                              |
| D3DFMT \_ A8R3G3B2                    | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ X4R4G4B4                    | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ A2B10G10R10                 | FORMATO DXGI \_ \_ R10G10B10A2                                                                                                                                                                                                                            |
| D3DFMT \_ A8B8G8R8                    | DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM & DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB                                                                                                                                                                                  |
| D3DFMT \_ X8B8G8R8                    | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ G16R16                      | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| D3DFMT \_ A2R10G10B10                 | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ A16B16G16R16                | FORMATO DXGI \_ \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| D3DFMT \_ A8P8                        | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ P8                          | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ L8                          | DXGI FORMAT R8 UNORM Nota: usare lo swizzle .r nello shader per duplicare il rosso in altri componenti per ottenere il \_ \_ comportamento \_ D3D9.                                                                                                                                    |
| D3DFMT \_ A8L8                        | DXGI \_ FORMAT \_ R8G8 UNORM Nota: usare swizzle .rrrg nello shader per duplicare il rosso e spostare il verde nei componenti alfa per ottenere il \_ comportamento D3D9.                                                                                                            |
| D3DFMT \_ A4L4                        | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ V8U8                        | DXGI \_ FORMAT \_ R8G8 \_ SNORM                                                                                                                                                                                                                            |
| D3DFMT \_ L6V5U5                      | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ X8L8V8U8                    | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ Q8W8V8U8                    | DXGI \_ FORMAT \_ R8G8B8A8 \_ SNORM                                                                                                                                                                                                                        |
| D3DFMT \_ V16U16                      | DXGI \_ FORMAT \_ R16G16 \_ SNORM                                                                                                                                                                                                                          |
| D3DFMT \_ W11V11U10                   | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ A2W10V10U10                 | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ UYVY                        | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ R8G8 \_ B8G8                  | \_DXGI FORMAT G8R8 G8B8 UNORM (in DX9 i dati sono stati ridimensionati di \_ \_ 255,0f, ma questo può essere gestito nel codice \_ dello shader).                                                                                                                                   |
| D3DFMT \_ YUY2                        | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ G8R8 \_ G8B8                  | DXGI \_ FORMAT R8G8 B8G8 UNORM (in DX9 i dati sono stati ridimensionati di \_ \_ 255,0f, ma questo può essere gestito nel codice \_ dello shader).                                                                                                                                   |
| D3DFMT \_ DXT1                        | FORMATO DXGI \_ \_ BC1 \_ UNORM & DXGI \_ FORMAT \_ BC1 \_ UNORM \_ SRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT2                        | DXGI \_ FORMAT \_ BC1 \_ UNORM & DXGI \_ FORMAT \_ BC1 \_ UNORM \_ SRGB Nota: DXT1 e DXT2 sono gli stessi dal punto di vista api/hardware... L'unica differenza era "alfa premoltimulati", che può essere monitorato da un'applicazione e non richiede un formato separato. |
| D3DFMT \_ DXT3                        | FORMATO DXGI \_ \_ BC2 \_ UNORM & DXGI \_ FORMAT \_ BC2 \_ UNORM \_ SRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT4                        | DXGI \_ FORMAT \_ BC2 \_ UNORM & DXGI \_ FORMAT \_ BC2 \_ UNORM \_ SRGB Nota: DXT3 e DXT4 sono gli stessi dal punto di vista api/hardware... L'unica differenza era "alfa premoltimulati", che può essere monitorato da un'applicazione e non richiede un formato separato. |
| D3DFMT \_ DXT5                        | FORMATO DXGI \_ \_ BC3 \_ UNORM & DXGI \_ FORMAT \_ BC3 \_ UNORM \_ SRGB                                                                                                                                                                                            |
| D3DFMT \_ D16 & D3DFMT \_ D16 \_ LOCKABLE | FORMATO DXGI \_ \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ D32                         | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ D15S1                       | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ D24S8                       | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X8                       | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X4S4                     | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ D16                         | FORMATO DXGI \_ \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ D32F \_ LOCKABLE              | FORMATO DXGI \_ \_ D32 \_ FLOAT                                                                                                                                                                                                                             |
| D3DFMT \_ D24FS8                      | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ S1D15                       | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ S8D24                       | DXGI \_ FORMAT \_ D24 \_ UNORM \_ S8 \_ UINT                                                                                                                                                                                                                   |
| D3DFMT \_ X8D24                       | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ X4S4D24                     | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ L16                         | DXGI FORMAT R16 UNORM Nota: usare lo swizzle .r nello shader per duplicare il rosso in altri componenti per ottenere il \_ \_ comportamento \_ D3D9.                                                                                                                                   |
| D3DFMT \_ INDEX16                     | DXGI \_ FORMAT \_ R16 \_ UINT                                                                                                                                                                                                                              |
| D3DFMT \_ INDEX32                     | DXGI \_ FORMAT \_ R32 \_ UINT                                                                                                                                                                                                                              |
| D3DFMT \_ Q16W16V16U16                | DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM                                                                                                                                                                                                                    |
| D3DFMT \_ MULTI2 \_ ARGB8               | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ R16F                        | FORMATO DXGI \_ \_ R16 \_ FLOAT                                                                                                                                                                                                                             |
| D3DFMT \_ G16R16F                     | FORMATO DXGI \_ \_ R16G16 \_ FLOAT                                                                                                                                                                                                                          |
| D3DFMT \_ A16B16G16R16F               | FORMATO DXGI \_ \_ R16G16B16A16 \_ FLOAT                                                                                                                                                                                                                    |
| D3DFMT \_ R32F                        | FORMATO DXGI \_ \_ R32 \_ FLOAT                                                                                                                                                                                                                             |
| D3DFMT \_ G32R32F                     | FORMATO DXGI \_ \_ R32G32 \_ FLOAT                                                                                                                                                                                                                          |
| D3DFMT \_ A32B32G32R32F               | FORMATO DXGI \_ \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                                                                    |
| D3DFMT \_ CxV8U8                      | Non disponibile                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT1                 | FORMATO DXGI \_ \_ R32 \_ FLOAT                                                                                                                                                                                                                             |
| D3DDECLTYPE \_ FLOAT2                 | FORMATO DXGI \_ \_ R32G32 \_ FLOAT                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT3                 | FORMATO DXGI \_ \_ R32G32B32 \_ FLOAT                                                                                                                                                                                                                       |
| D3DDECLTYPE \_ FLOAT4                 | FORMATO DXGI \_ \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                                                                    |
| D3DDECLTYPED3DCOLOR                 | Non disponibile                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ UBYTE4                 | DXGI FORMAT R8G8B8A8 UINT Nota: shader ottiene i valori UINT, ma se sono necessari float integrali in stile \_ \_ \_ Direct3D 9 (0,0f, 1,0f... 255.f), UINT può essere semplicemente convertito in float32 nello shader.                                                               |
| D3DDECLTYPE \_ SHORT2                 | DXGI \_ FORMAT R16G16 SINT Nota: lo shader ottiene i valori SINT, ma se sono necessari float integrali in stile \_ Direct3D 9, SINT può essere semplicemente convertito \_ in float32 nello shader.                                                                                       |
| D3DDECLTYPE \_ SHORT4                 | DXGI \_ FORMAT \_ R16G16B16A16 SINT Nota: lo shader ottiene valori SINT, ma se sono necessari float integrali in stile Direct3D 9, SINT può essere semplicemente convertito \_ in float32 nello shader.                                                                                 |
| D3DDECLTYPE \_ UBYTE4N                | FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ SHORT2N                | DXGI \_ FORMAT \_ R16G16 \_ SNORM                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ SHORT4N                | DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ USHORT2N               | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ USHORT4N               | FORMATO DXGI \_ \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ UDEC3                  | Non disponibile                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ DEC3N                  | Non disponibile                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2             | FORMATO DXGI \_ \_ R16G16 \_ FLOAT                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4             | FORMATO DXGI \_ \_ R16G16B16A16 \_ FLOAT                                                                                                                                                                                                                    |
| FourCC 'ATI1'                       | FORMATO DXGI \_ \_ BC4 \_ UNORM                                                                                                                                                                                                                             |
| FourCC 'ATI2'                       | DXGI \_ FORMAT \_ BC5 \_ UNORM                                                                                                                                                                                                                             |



 

¹DXGI 1.1, incluso nel runtime Direct3D 11, include i formati BGRA. Tuttavia, il supporto per questi formati è facoltativo per i dispositivi Direct3D 10 e 10.1 con driver implementati nel modello WDDM (Windows Display Driver Model) per Windows Vista (WDDM 1.0). Prendere in considerazione l'uso di DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM. In alternativa, è possibile creare il dispositivo con [**D3D10 \_ CREATE \_ DEVICE \_ BGRA \_ SUPPORT**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) per assicurarsi di supportare solo i computer con il runtime Direct3D 11.0 e un driver WDDM 1.1 o versione successiva installato.

²DXGI 1.0 ha definito i formati 5:6:5 e 5:5:5:1, ma non sono supportati dal runtime Direct3D 10.x o Direct3D 11.0. Questi formati sono supportati facoltativamente con DXGI 1.2 nel runtime DirectX 11.1, necessario per le schede video di livello 11.1 e i driver WDDM 1.2 (modello di driver di visualizzazione a partire da Windows 8) e già supportati nei livelli di funzionalità 10level9.

³DXGI 1.2 ha introdotto il formato 4:4:4:4:4. Questo formato è supportato facoltativamente nel runtime DirectX 11.1, necessario per le schede video di livello 11.1 e i driver WDDM 1.2 e già supportato nei livelli di funzionalità 10level9.

Per i formati non compressi, DXGI ha limitato il supporto per modelli di formato pixel arbitrari; tutti i formati non compressi devono essere di tipo RGBA. Potrebbe essere necessario eseguire lo swizzling dei formati pixel degli asset esistenti, che è consigliabile calcolare come passaggio di pre-elaborazione offline, laddove possibile.

## <a name="porting-shaders"></a>Porting shader

### <a name="direct3d-10-shaders-are-authored-in-hlsl"></a>Gli shader Direct3D 10 sono creati in HLSL

Direct3D 10 limita l'uso del linguaggio assembly solo a scopo di debug, pertanto tutti gli shader di assembly scritti a mano usati in Direct3D 9 dovranno essere convertiti in HLSL.

### <a name="shader-signatures-and-linkage"></a>Firme shader e collegamento

I requisiti per il collegamento dell'assembly di input alle firme di input vertex shader sono stati illustrati in precedenza in questo documento (vedere sopra). Si noti che anche il runtime Direct3D 10 ha stretto i requisiti per il collegamento tra fasi e fasi tra shader. Questa modifica influirà sulle origini shader in cui l'associazione tra le fasi potrebbe non essere stata descritta completamente in Direct3D 9. Esempio:


```
VS_OUTPUT                       PS_INPUT
float4   pos : SV_POSITION;     float4 pos : SV_POSITION;
float4   uv1 : TEXCOORD1;       float4 uv1 : TEXCOORD1;
float4x3 tangentSp : TEXCOORD2; float4 tangent : TEXCOORD2; *
float4   Color : TEXCOORD6;     float4 color : TEXCOORD6;
```



\* Vs interrotto - Collegamento PS: anche se il pixel shader potrebbe non essere interessato alla matrice completa, il collegamento deve specificare l'intero float4x3.

Si noti che la semantica di collegamento tra le fasi deve corrispondere esattamente, ma gli input delle fasi di destinazione possono essere un prefisso dei valori restituiti. Nell'esempio precedente, il pixel shader potrebbe avere position e texcoord1 come unici input, ma non la posizione e texcoord2 come unici input a causa dei vincoli di ordinamento.

### <a name="hlsl-shader-stage-linkages"></a>Collegamenti della fase shader HLSL

Il collegamento tra shader può verificarsi in uno dei punti seguenti della pipeline:

-   Assembler di input per Vertex Shader
-   Vertex Shader in Pixel Shader
-   Vertex Shader in Geometry Shader
-   Output da vertex shader a flusso
-   Da Geometry Shader a Pixel Shader
-   Shader Geometry da trasmettere in streaming

### <a name="constant-buffers"></a>Buffer costanti

Per semplificare il porting del contenuto da Direct3D 9, un approccio iniziale alla gestione costante all'esterno del sistema Effects potrebbe comportare la creazione di un singolo buffer costante contenente tutte le costanti necessarie. È importante che le prestazioni ordinino le costanti nei buffer in base alla frequenza prevista di aggiornamento. Questa organizzazione ridurrà al minimo la quantità di set di costanti ridondanti.

### <a name="user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Piani di ritaglio utente in HLSL a livello di funzionalità 9 e versioni successive

A partire da Windows 8, è possibile usare l'attributo della [](../direct3dhlsl/dx-graphics-hlsl-function-syntax.md) funzione **clipplanes** in una dichiarazione di funzione HLSL anziché [SV \_ ClipDistance](../direct3dhlsl/dx-graphics-hlsl-semantics.md) per far funzionare lo shader sul livello di funzionalità [9](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) x e sul livello di funzionalità 10 e versioni \_ successive. Per altre informazioni, vedere [Piani di ritaglio utente nell'hardware del livello di funzionalità 9.](../direct3dhlsl/user-clip-planes-on-10level9.md)

## <a name="additional-direct3d-10-differences-to-watch-for"></a>Differenze aggiuntive di Direct3D 10 da controllare

### <a name="integers-as-input"></a>Numeri interi come input

In Direct3D 9 non era disponibile alcun supporto hardware reale per i tipi di dati Integer, ma l'hardware Direct3D 10 supporta tipi integer espliciti. Se nel vertex buffer sono presenti dati a virgola mobile, è necessario avere un input float. In caso contrario, un tipo integer sarà la rappresentazione del modello di bit del valore a virgola mobile. Un tipo integer non è consentito per un input pixel shader a meno che il valore non sia contrassegnato per nessuna interpolazione (vedere [Modificatori di interpolazione](../direct3dhlsl/dx-graphics-hlsl-struct.md)).

### <a name="mouse-cursors"></a>Cursori del mouse

Nelle versioni precedenti di Windows, le routine del cursore del mouse GDI standard non funzionava correttamente in tutti i dispositivi esclusivi a schermo intero. Per gestire questi casi sono state aggiunte le API [**SetCursorProperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties), [**ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)e [**SetCursorPosition.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition) Poiché Windows versione di GDI di Vista comprende completamente le superfici [DXGI,](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md) non è necessaria questa API del cursore del mouse specializzata, quindi non è disponibile alcun equivalente direct3D 10. Le applicazioni Direct3D 10 devono invece usare le routine del [cursore del mouse GDI](../menurc/cursors.md) standard per i cursori del mouse.

### <a name="mapping-texels-to-pixels-in-direct3d-10"></a>Mapping di Texels a Pixel in Direct3D 10

In Direct3D 9 i centri texel e i centri pixel erano a metà unità di distanza (vedere Mapping diretto dei texel ai pixel [(Direct3D 9).](../direct3d9/directly-mapping-texels-to-pixels.md) In Direct3D 10 i centri texel sono già a metà unità, quindi non è necessario spostare le coordinate dei vertici.

Il rendering dei quad a schermo intero è più diretto con Direct3D 10. I quad a schermo intero devono essere definiti nello spazio di ritaglio (-1,1) e semplicemente passati attraverso il vertex shader senza modifiche. In questo modo, non è necessario ricaricare il vertex buffer ogni volta che cambia la risoluzione dello schermo e non è necessario eseguire operazioni aggiuntive nel pixel shader modificare le coordinate della trama.

### <a name="reference-counting-behavior-changes"></a>Modifiche al comportamento del conteggio dei riferimenti

A differenza delle versioni precedenti di Direct3D, le varie funzioni Set non conteneranno un riferimento agli oggetti devices. Ciò significa che l'applicazione deve assicurarsi di contenere un riferimento sull'oggetto per tutto il tempo che desidera che tale oggetto sia associato alla pipeline. Quando il conteggio dei riferimenti dell'oggetto scende a zero, l'oggetto verrà scollegato dalla pipeline quando viene eliminato. Questo stile di controllo dei riferimenti è noto anche come debol-reference holding, quindi ogni posizione di associazione nell'oggetto Device contiene un riferimento debole all'interfaccia o all'oggetto. Se non diversamente indicato in modo esplicito, questo comportamento deve essere assunto per tutti i metodi Set. Ogni volta che la distruzione di un oggetto causa l'impostazione di un punto di associazione su **NULL,** il livello di debug genera un avviso. Si noti che le chiamate ai metodi Device Get, ad [**esempio OMGetRenderTargets,**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omgetrendertargets) aumentano il conteggio dei riferimenti degli oggetti restituiti.

### <a name="test-cooperative-level"></a>Livello cooperativo di test

La funzionalità dell'API Direct3D 9 [**TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel) è analoga all'impostazione di [DXGI \_ PRESENT \_ TEST](../direct3ddxgi/dxgi-present.md) quando si chiama [**Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present).

### <a name="stretchrect"></a>StretchRect

Una funzione simile al metodo Direct3D 9 [**IDirect3DDevice9::StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) non è disponibile in Direct3D 10 e 10.1. Per copiare le superfici delle risorse, [**usare ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion). Per le operazioni di ridimensionamento, eseguire il rendering in una trama usando il filtro trame. Per convertire le superfici MSAA in superfici non MSAA, usare [**ID3D10Device::ResolveSubresource**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-resolvesubresource).

## <a name="additional-direct3d-101-differences"></a>Differenze aggiuntive di Direct3D 10.1

Windows Vista con Service Pack 1 (SP1) include un aggiornamento secondario a Direct3D 10 e Direct3D 10.1, che ha esposto le funzionalità hardware aggiuntive seguenti:

-   SHADER MSAA per campione
-   Read-back di profondità MSAA
-   Modalità di blend indipendenti per ogni destinazione di rendering
-   Matrici di mappe del cubo
-   Eseguire il rendering in formati compressi a blocchi (BC)

L'aggiornamento direct3D 10.1 ha aggiunto il supporto per le nuove interfacce seguenti, derivate dalle interfacce esistenti:

-   [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)
-   [**ID3D10BlendState1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)
-   [**ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1)

L'aggiornamento direct3D 10.1 include anche le strutture aggiuntive seguenti:

-   [**D3D10 \_ RENDER \_ TARGET \_ BLEND \_ DESC1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_render_target_blend_desc1)
-   [**D3D10 \_ BLEND \_ DESC1**](/windows/desktop/api/D3D10_1/ns-d3d10_1-d3d10_blend_desc1)
-   [**VISUALIZZAZIONE DELLE RISORSE DELLO SHADER D3D10 \_ \_ \_ \_ DESC1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_shader_resource_view_desc1)

L'API Direct3D 10.1 include un nuovo concetto denominato livello di funzionalità. Questo concetto significa che è possibile usare l'API Direct3D 10.1 per guidare l'hardware Direct3D 10.0 ([**D3D10 \_ FEATURE \_ LEVEL \_ 10 \_ 0**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)) o Direct3D 10.1 ([**D3D10 \_ FEATURE LEVEL \_ \_ 10 \_ 1).**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1) Poiché l'API Direct3D 10.1 deriva dalle interfacce Direct3D 10, le applicazioni possono creare un dispositivo Direct3D 10.1, quindi usarlo come dispositivo Direct3D 10.0, ad eccezione dei casi in cui sono necessarie nuove funzionalità specifiche di 10.1 (a condizione che il livello di funzionalità **D3D10 \_ FEATURE \_ LEVEL \_ \_ 10 1** sia presente e supporti queste funzionalità).

> [!Note]  
> I dispositivi Direct3D 10.1 possono usare i profili shader HLSL 10.0 esistenti (vs \_ 4 \_ 0, ps \_ 4 0, gs 4 0) e i nuovi profili \_ \_ \_ 10.1 (vs \_ 4 \_ 1, ps \_ 4 \_ 1, gs \_ 4 1) con \_ istruzioni e funzionalità HLSL aggiuntive.

 

Windows 7 conteneva un aggiornamento secondario dell'API Direct3D 10.1 incluso nel runtime direct3D 11. Questo aggiornamento aggiunge il supporto per i livelli di funzionalità seguenti:

-   [**D3D10 \_ FEATURE \_ LEVEL \_ 9 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**D3D10 \_ FEATURE \_ LEVEL \_ 9 \_ 2**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**D3D10 \_ FEATURE \_ LEVEL \_ 9 \_ 3**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)

Windows 7 ha aggiunto anche il supporto per Direct3D 10.1 [per Windows Advanced Rasterization Platform (WARP).](../direct3darticles/directx-warp.md) È possibile specificare un driver WARP usando [**D3D10 \_ DRIVER \_ TYPE \_ WARP**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).

Per altre informazioni su Direct3D 10.1, vedere [Funzionalità direct3D 10.1](d3d10-graphics-programming-guide-10-1.md) e [**l'enumerazione D3D10 \_ FEATURE \_ LEVEL1.**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori per Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
