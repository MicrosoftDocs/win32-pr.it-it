---
description: Nella pagina seguente viene fornita una descrizione di base delle differenze principali tra Direct3D 9 e Direct3D 10. La struttura seguente fornisce alcune informazioni utili per aiutare gli sviluppatori con esperienza Direct3D 9 a esplorare e mettere in relazione a Direct3D 10.
ms.assetid: 283b54e0-94cb-47a8-8cfc-5798e0538b9f
title: Considerazioni su Direct3D 9 a Direct3D 10 (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467ceefe7784a9b408bb36c8bed13217cb6de7c4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748023"
---
# <a name="direct3d-9-to-direct3d-10-considerations-direct3d-10"></a>Considerazioni su Direct3D 9 a Direct3D 10 (Direct3D 10)

Nella pagina seguente viene fornita una descrizione di base delle differenze principali tra Direct3D 9 e Direct3D 10. La struttura seguente fornisce alcune informazioni utili per aiutare gli sviluppatori con esperienza Direct3D 9 a esplorare e mettere in relazione a Direct3D 10.

Sebbene le informazioni in questo argomento confrontano Direct3D 9 con Direct3D 10, perché Direct3D 11 si basa sui miglioramenti apportati a Direct3D 10 e 10,1, queste informazioni sono necessarie anche per la migrazione da Direct3D 9 a Direct3D 11. Per informazioni sul passaggio oltre Direct3D 10 a Direct3D 11, vedere la pagina relativa [alla migrazione a Direct3D 11](../direct3d11/d3d11-programming-guide-migrating.md).

-   [Cenni preliminari sulle principali modifiche strutturali in Direct3D 10](#overview-of-the-major-structural-changes-in-direct3d-10)
    -   [Rimozione della funzione Fixed](#removal-of-fixed-function)
    -   [Convalida dell'ora di creazione dell'oggetto dispositivo](#device-object-creation-time-validation)
-   [Astrazioni/separazione del motore](/windows)
    -   [Rimozione diretta delle dipendenze di Direct3D 9](#direct-removal-of-direct3d-9-dependencies)
-   [Suggerimenti per la risoluzione rapida dei problemi di compilazione dell'applicazione](#tricks-for-quickly-resolving-application-build-issues)
    -   [Override di tipi Direct3D 9](#overriding-direct3d-9-types)
    -   [Risoluzione dei problemi di collegamento](#resolving-link-issues)
    -   [Simulazione dei tappi dei dispositivi](#simulating-device-caps)
-   [Guida dell'API Direct3D 10](#driving-the-direct3d-10-api)
    -   [Creazione di risorse](#resource-creation)
    -   [Visualizzazioni](#views)
    -   [Accesso a risorse statiche e dinamiche](#static-versus-dynamic-resource-access)
    -   [Effetti Direct3D 10](#direct3d-10-effects)
    -   [HLSL senza effetti](#hlsl-without-effects)
    -   [Compilazione shader](#shader-compilation)
    -   [Creazione di risorse shader](#creation-of-shader-resources)
    -   [Interfaccia del livello Reflection dello shader](#shader-reflection-layer-interface)
    -   [Layout assembler input-vertex shader/collegamento flusso di input](/windows)
    -   [Effetti della rimozione del codice non recapitabile dello shader](#impact-of-shader-dead-code-removal)
    -   [Esempio di struttura di input vertex shader](#vertex-shader-input-structure-example)
    -   [Creazione di oggetti stato](#state-object-creation)
-   [Porting di trame](#porting-textures)
    -   [Formati di file supportati](#file-formats-supported)
    -   [Mapping di formati di trama](#mapping-texture-formats)
-   [Porting degli shader](#porting-shaders)
    -   [Gli shader Direct3D 10 sono stati creati in HLSL](#direct3d-10-shaders-are-authored-in-hlsl)
    -   [Firme shader e collegamento](#shader-signatures-and-linkage)
    -   [Collegamenti alla fase HLSL shader](#hlsl-shader-stage-linkages)
    -   [Buffer costanti](#constant-buffers)
    -   [Piani di ritaglio utente in HLSL a livello di funzionalità 9 e superiore](#user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Altre differenze di Direct3D 10 da controllare](#additional-direct3d-10-differences-to-watch-for)
    -   [Integer come input](#integers-as-input)
    -   [Cursori del mouse](#mouse-cursors)
    -   [Mapping dei Texel ai pixel in Direct3D 10](#mapping-texels-to-pixels-in-direct3d-10)
    -   [Conteggio dei riferimenti modifiche del comportamento](#reference-counting-behavior-changes)
    -   [Livello cooperativa di test](#test-cooperative-level)
    -   [StretchRect](#stretchrect)
-   [Differenze aggiuntive con Direct3D 10,1](#additional-direct3d-101-differences)
-   [Argomenti correlati](#related-topics)

## <a name="overview-of-the-major-structural-changes-in-direct3d-10"></a>Cenni preliminari sulle principali modifiche strutturali in Direct3D 10

-   [Rimozione della funzione Fixed](#removal-of-fixed-function)
-   [Convalida dell'ora di creazione dell'oggetto dispositivo](#device-object-creation-time-validation)

Il processo di rendering con il dispositivo Direct3D 10 è strutturalmente simile a Direct3D 9.

-   Impostare un'origine del flusso di vertici
-   Impostare il layout di input in Direct3D 10 (impostare la dichiarazione del flusso di vertici in Direct3D 9)
-   Dichiarare la topologia primitiva
-   Imposta trame
-   Imposta oggetti stato
-   Imposta shader
-   Disegna

La chiamata di [**progetto**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw) unisce le operazioni; l'ordinamento delle chiamate prima della chiamata di progetto è arbitrario. Le principali differenze nella progettazione dell'API Direct3D 10 sono le seguenti:

-   Rimozione della funzione Fixed
-   Rimozione dei bit di CAPS: il set di funzionalità di base di Direct3D 10 è garantito
-   Gestione più restrittiva di: accesso alle risorse, stato del dispositivo, costanti dello shader, collegamento dello shader (input e output agli shader) tra le fasi
-   Le modifiche al nome del punto di ingresso dell'API riflettono l'uso della memoria GPU virtuale (Map () anziché Lock ()).
-   Al dispositivo è possibile aggiungere un livello di debug al momento della creazione
-   La topologia primitiva è ora uno stato esplicito (separato dalla chiamata di [**progetto**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw) )
-   Le costanti shader esplicite vengono ora archiviate in buffer costanti
-   La creazione dello shader viene eseguita interamente in HLSL. Il compilatore HLSL si trova ora nella DLL principale di Direct3D 10.
-   Nuova fase programmabile-geometria shader
-   Rimozione di BeginScene ()/EndScene ()
-   Funzionalità comuni di gestione di elementi 2D, Focus e adapter implementate in un nuovo componente: DXGI

### <a name="removal-of-fixed-function"></a>Rimozione della funzione Fixed

Talvolta è sorprendente che anche in un motore Direct3D 9 che sfrutti completamente la pipeline programmabile, rimangano diverse aree che dipendono dalla pipeline a funzione fissa (FF). Le aree più comuni sono in genere correlate al rendering dello spazio dello schermo allineato per l'interfaccia utente. È per questo motivo che è probabile che sia necessario creare uno shader di emulazione FF o un set di shader che forniscano i comportamenti di sostituzione necessari.

Questa documentazione contiene una white paper contenente le origini shader di sostituzione per i comportamenti FF più comuni (vedere l'esempio relativo a una [funzione Fixed Emu](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx)). Il comportamento dei pixel a funzione fissa, incluso il test alfa, è stato spostato in shader.

### <a name="device-object-creation-time-validation"></a>Convalida dell'ora di creazione dell'oggetto dispositivo

La pipeline Direct3D 10 è stata riprogettata da zero nell'hardware e nel software con l'intenzione principale di ridurre il sovraccarico della CPU (in fase di disegno). Per ridurre i costi, a tutti i tipi di dati del dispositivo è stato assegnato un oggetto con metodi di creazione espliciti forniti dal dispositivo stesso. In questo modo è possibile convalidare i dati in modo rigoroso al momento della creazione dell'oggetto anziché durante la chiamata di progetto, come spesso accade con Direct3D 9

## <a name="engine-abstractions--separation"></a>Astrazioni/separazione del motore

Le applicazioni, inclusi i giochi, che desiderano supportare sia Direct3D 9 sia Direct3D 10 devono disporre dei livelli di rendering estratti dal resto della codebase. Esistono diversi modi per ottenere questo risultato, ma la chiave per tutti questi elementi è la progettazione del livello di astrazione per il dispositivo Direct3D di livello inferiore. Tutti i sistemi devono comunicare con l'hardware tramite il livello comune, progettato per fornire la risorsa GPU e la gestione dei tipi di basso livello.

### <a name="direct-removal-of-direct3d-9-dependencies"></a>Rimozione diretta delle dipendenze di Direct3D 9

Quando si esegue il porting di codice di grandi dimensioni, testato in precedenza, è importante ridurre al minimo la quantità di modifiche del codice a quelle che sono assolutamente necessarie per mantenere i comportamenti testati in precedenza nel codice. Le procedure consigliate includono chiaramente la documentazione relativa alla modifica degli elementi tramite commenti. Spesso è utile avere uno standard di commenti per questo lavoro, che consente la navigazione rapida nella codebase.

Di seguito è riportato un esempio di un elenco di commenti di blocco single line/Start standard che possono essere usati per questa operazione.



| Elemento                                                                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="___Direct3D_10_REMOVED"></span><span id="___direct3d_10_removed"></span><span id="___DIRECT3D_10_REMOVED"></span>Direct3D 10 rimosso<br/>                     | Usare questa posizione per rimuovere righe/blocchi di codice<br/>                                                                                                                                                                                                                                                                   |
| <span id="___Direct3D_10_NEEDS_UPDATE"></span><span id="___direct3d_10_needs_update"></span><span id="___DIRECT3D_10_NEEDS_UPDATE"></span>È necessario aggiornare Direct3D 10<br/> | Consente di aggiungere altre note al commento NEED UPDATE che suggerisce quale lavoro/nuova API deve essere usato per le visite successive al codice per la conversione del comportamento. È inoltre consigliabile utilizzare Assert (**false**) quando \\ \\ si verifica l'aggiornamento di Direct3D 10, per garantire che non si esegua inconsapevolmente codice errato<br/> |
| <span id="___Direct3D_10_CHANGED"></span><span id="___direct3d_10_changed"></span><span id="___DIRECT3D_10_CHANGED"></span>Direct3D 10 modificato<br/>                     | Le aree in cui si sono verificate le modifiche principali devono essere conservate per riferimento futuro, ma impostate come commento<br/>                                                                                                                                                                                                                       |
| <span id="___Direct3D_10_END"></span><span id="___direct3d_10_end"></span><span id="___DIRECT3D_10_END"></span>FINE Direct3D 10<br/>                                     | Termina qualificatore blocchi di codice<br/>                                                                                                                                                                                                                                                                                            |



 

Per più righe di origine è necessario usare anche i commenti//di tipo C \* \* , ma aggiungere i commenti di inizio/fine pertinenti intorno a queste aree.

## <a name="tricks-for-quickly-resolving-application-build-issues"></a>Suggerimenti per la risoluzione rapida dei problemi di compilazione dell'applicazione

-   [Override di tipi Direct3D 9](#overriding-direct3d-9-types)
-   [Risoluzione dei problemi di collegamento](#resolving-link-issues)
-   [Simulazione dei tappi dei dispositivi](#simulating-device-caps)

### <a name="overriding-direct3d-9-types"></a>Override di tipi Direct3D 9

Potrebbe essere utile inserire un file di intestazione di alto livello contenente le definizioni di tipo o le sostituzioni per i tipi di base Direct3D 9 che non sono più supportati dalle intestazioni Direct3D 10. Ciò consentirà di ridurre al minimo la quantità di modifiche nel codice e nelle interfacce in cui è presente un mapping diretto da un tipo Direct3D 9 al tipo Direct3D 10 appena definito. Questo approccio è utile anche per mantenere insieme i comportamenti del codice in un unico file di origine. In questo caso, è consigliabile definire tipi neutri/denominati della versione, che descrivono i costrutti comuni usati per il rendering, ma si estendono anche le API Direct3D 9 e Direct3D 10. Ad esempio:


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

È consigliabile sviluppare applicazioni Direct3D 10 e Windows Vista usando la versione più recente di Microsoft Visual Studio. Tuttavia, è possibile creare un'applicazione Windows Vista che dipende da Direct3D 10 utilizzando la versione 2003 precedente di Visual Studio. Direct3D 10 è un componente della piattaforma Windows Vista che presenta dipendenze (come con Server 2003 SP1 Platform SDK) nella seguente procedura: BufferOverflowU. lib è necessario per risolvere eventuali \_ problemi del linker Verifica sicurezza del buffer.

### <a name="simulating-device-caps"></a>Simulazione dei tappi dei dispositivi

Molte applicazioni contengono aree di codice che dipendono dai dati dei limiti di dispositivo disponibili. Ovviare a questo problema eseguendo l'override dell'enumerazione del dispositivo e forzando i limiti dei dispositivi sui valori sensibili. Pianificare di visitare di nuovo le aree in cui sono presenti dipendenze in seguito per la rimozione completa di CAPS laddove possibile.

## <a name="driving-the-direct3d-10-api"></a>Guida dell'API Direct3D 10

Questa sezione è incentrata sulle modifiche del comportamento causate dall'API Direct3D 10.

-   [Creazione di risorse](#resource-creation)
-   [Visualizzazioni](#views)
-   [Accesso a risorse statiche e dinamiche](#static-versus-dynamic-resource-access)
-   [Effetti Direct3D 10](#direct3d-10-effects)
-   [HLSL senza effetti](#hlsl-without-effects)
-   [Compilazione shader](#shader-compilation)
-   [Creazione di risorse shader](#creation-of-shader-resources)
-   [Interfaccia del livello Reflection dello shader](#shader-reflection-layer-interface)
-   [Layout assembler input-vertex shader/collegamento flusso di input](/windows)
-   [Effetti della rimozione del codice non recapitabile dello shader](#impact-of-shader-dead-code-removal)
-   [Esempio di struttura di input vertex shader](#vertex-shader-input-structure-example)
-   [Creazione di oggetti stato](#state-object-creation)

### <a name="resource-creation"></a>Creazione di risorse

L'API Direct3D 10 ha progettato le risorse come tipi di buffer generici che hanno flag di binding specifici in base all'utilizzo pianificato. Questo punto di progettazione è stato scelto per facilitare l'accesso onnipresente alle risorse nella pipeline per scenari quali il rendering in un buffer vertex, quindi il disegno immediato dei risultati senza interrompere la CPU. Nell'esempio seguente viene illustrata l'allocazione di buffer di vertici e index buffer in cui è possibile osservare che la descrizione della risorsa è diversa solo per i flag di associazione delle risorse GPU.

L'API Direct3D 10 ha fornito metodi helper di trama per creare in modo esplicito le risorse del tipo di trama, ma come si può immaginare, si tratta di funzioni di supporto molto utili.

-   CreateTexture2D()
-   CreateTextureCube()
-   CreateTexture3D()

Quando la destinazione è Direct3D 10, è probabile che si voglia allocare più elementi durante la creazione delle risorse rispetto a quanto si usa con Direct3D 9. Questa operazione diventerà più evidente con la creazione di buffer e trame della destinazione di rendering in cui è necessario creare anche una visualizzazione per accedere al buffer e impostare la risorsa nel dispositivo.

[Esercitazione 1: Nozioni fondamentali su Direct3D 10](https://msdn.microsoft.com/library/Ee416436(v=VS.85).aspx)

> [!Note]  
> Direct3D 10 e le versioni successive di Direct3D estendono il formato di file DDS per supportare i nuovi formati DXGI, le matrici di trama e le matrici della mappa cubo. Per ulteriori informazioni sull'estensione del formato di file DDS, vedere la [Guida alla programmazione per DDS](../direct3ddds/dx-graphics-dds-pguide.md).

 

### <a name="views"></a>Viste

Una vista è un'interfaccia tipizzata in modo specifico per i dati archiviati in un buffer pixel. Una risorsa può avere più visualizzazioni allocate contemporaneamente e questa funzionalità viene evidenziata nell'esempio di rendering del singolo passaggio a mappa cubi contenuto in questo SDK.

[Pagina della Guida per programmatori per l'accesso alle risorse](d3d10-graphics-programming-guide-resources-access-views.md)

[Esempio mappa cubi](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)

### <a name="static-versus-dynamic-resource-access"></a>Accesso a risorse statiche e dinamiche

Per ottenere prestazioni ottimali, le applicazioni devono partizionare l'utilizzo dei dati in termini di natura statica rispetto alla natura dinamica dei dati. Direct3D 10 è stato progettato per sfruttare i vantaggi di questo approccio e, di conseguenza, le regole di accesso per le risorse sono state notevolmente ristrette rispetto a Direct3D 9. Per le risorse statiche, è consigliabile popolare la risorsa con i relativi dati in fase di creazione. Se il motore è stato progettato intorno al punto di progettazione per la creazione, il blocco, il riempimento e lo sblocco di Direct3D 9, è possibile rinviare il popolamento dall'ora di creazione usando una risorsa di staging e il metodo UpdateSubResource sull'interfaccia della risorsa.

### <a name="direct3d-10-effects"></a>Effetti Direct3D 10

L'utilizzo del sistema di effetti Direct3D 10 esula dall'ambito di questo articolo. Il sistema è stato scritto per sfruttare appieno i vantaggi architettonici forniti da Direct3D 10. Per altri dettagli sull'uso, vedere la sezione [effetti (Direct3D 10)](d3d10-graphics-programming-guide-effects.md) .

### <a name="hlsl-without-effects"></a>HLSL senza effetti

La pipeline shader Direct3D 10 può essere gestita senza l'uso del sistema di effetti Direct3D 10. Si noti che in questo caso, tutti i buffer costanti, shader, sampler e trama devono essere gestiti dall'applicazione stessa. Per informazioni dettagliate, vedere il collegamento di esempio e le sezioni seguenti di questo documento:

[Esempio di HLSL senza effetti](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)

### <a name="shader-compilation"></a>Compilazione shader

Il compilatore Direct3D 10 HLSL introduce i miglioramenti alla definizione del linguaggio HLSL e quindi ha la possibilità di operare in due modalità. Per il supporto completo della semantica e delle funzioni intrinseche dello stile Direct3D 9, la compilazione deve essere richiamata usando il flag della modalità di compatibilità, che può essere specificato in base alla compilazione.

Il modello di Shader 4,0 specifica la semantica del linguaggio HLSL e le funzioni intrinseche per Direct3D 10 sono disponibili in [HLSL](../direct3dhlsl/dx-graphics-hlsl.md). Le principali modifiche apportate alla sintassi da Direct3D 9 HLSL per la maggior parte degli avvisi sono nell'area dell'accesso alla trama. La nuova sintassi è l'unico formato supportato dal compilatore al di fuori della modalità di compatibilità.

> [!Note]  
> Le API del tipo di compilatore Direct3D 10 ([**D3D10CompileShader**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10compileshader) e [**D3D10CompileEffectFromMemory**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10compileeffectfrommemory)) vengono fornite dai runtime Direct3D 10, 10,1 e 11 che vengono eseguiti in Windows Vista e versioni successive. Le API del tipo di compilatore Direct3D 10 hanno le stesse funzionalità del compilatore HLSL fornito in DirectX SDK (2006 dicembre). Questo compilatore HLSL non supporta i profili Direct3D 10,1 (vs \_ 4 1 \_ , PS \_ 4 \_ 1, GS \_ 4 \_ 1, FX \_ 4 \_ 1) e mancano numerose ottimizzazioni e miglioramenti. È possibile ottenere un compilatore HLSL che supporta i profili Direct3D 10,1 dall'ultima versione legacy di [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)). Per informazioni sul legacy DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md). È possibile ottenere la versione più recente di HLSL Fxc.exe il compilatore da riga di comando e le API [D3DCompiler](../direct3dhlsl/dx-graphics-d3dcompiler-reference.md) dall'Windows SDK.

 

### <a name="creation-of-shader-resources"></a>Creazione di risorse shader

La creazione di istanze dello shader compilate all'esterno del sistema Direct3D 10 Effects viene eseguita in modo molto simile a Direct3D 9. Tuttavia, in Direct3D 10, è importante proteggere la firma di input dello shader per un uso successivo. La firma viene restituita per impostazione predefinita come parte del BLOB dello shader, ma può essere estratta per ridurre i requisiti di memoria, se necessario. Per ulteriori informazioni, vedere [using shaders in Direct3D 10](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).

### <a name="shader-reflection-layer-interface"></a>Interfaccia del livello Reflection dello shader

Il livello di Reflection dello shader è l'interfaccia in base alla quale è possibile ottenere informazioni sui requisiti dello shader. Questa operazione è particolarmente utile durante la creazione di collegamenti di assembly di input (vedere di seguito), in cui potrebbe essere necessario attraversare i requisiti di input dello shader per assicurarsi di fornire la struttura di input corretta allo shader. È possibile creare un'istanza dell'interfaccia del livello Reflection contemporaneamente alla creazione di un'istanza di uno shader compilato.

Il livello Reflection dello shader sostituisce i metodi D3DX9 che forniscono funzionalità simili. Ad esempio, [**IsParameterUsed**](../direct3d9/id3dxeffect--isparameterused.md) viene sostituito dal metodo [**getdesc**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-id3d10shaderreflectionvariable-getdesc) .

### <a name="input-assembler-layouts---vertex-shader--input-stream-linkage"></a>Layout assembler input-vertex shader/collegamento flusso di input

L'assembler di input (IA) sostituisce la dichiarazione del flusso di vertici dello stile Direct3D 9 e la relativa struttura di descrizione è molto simile nel formato. La differenza principale che l'IA apporta è che l'oggetto layout IA creato deve essere mappato direttamente a un formato specifico della firma di input dello shader. L'oggetto di mapping creato per collegare il flusso di input allo shader può essere usato in qualsiasi numero di shader in cui la firma di input dello shader corrisponde a quella dello shader usato per creare il layout di input.

Per ottimizzare la pipeline con dati statici, è consigliabile prendere in considerazione le permutazioni del formato del flusso di input per le possibili firme di input dello shader e creare le istanze dell'oggetto di layout IA il prima possibile e riutilizzarle laddove possibile.

### <a name="impact-of-shader-dead-code-removal"></a>Effetti della rimozione del codice non recapitabile dello shader

Nella sezione seguente viene illustrata una differenza significativa tra Direct3D 9 e Direct3D 10 che è probabile che sia necessaria una gestione attenta nel codice del motore. Gli shader che contengono espressioni condizionali hanno spesso alcuni percorsi di codice rimossi come parte del processo di compilazione. In Direct3D 9 è possibile rimuovere due tipi di input (contrassegnati per la rimozione) quando non usati: input della firma, come nell'esempio riportato di seguito, e input costanti. Se la fine del buffer costante contiene voci inutilizzate, la dichiarazione di dimensioni nello shader rifletterà le dimensioni del buffer costante senza le voci inutilizzate alla fine. Entrambi questi tipi di input rimangono nelle firme o nei buffer costanti Direct3D 10 con un'eccezione speciale nel caso di input costanti non utilizzati alla fine di un buffer costante. Questo può avere un effetto sul motore quando si gestiscono shader di grandi dimensioni e si creano layout di input. Gli elementi rimossi dalle ottimizzazioni del codice inattivo nel compilatore devono comunque essere dichiarati nella struttura di input. Questo concetto è illustrato nell'esempio seguente:

### <a name="vertex-shader-input-structure-example"></a>Esempio di struttura di input vertex shader


```
struct VS_INPUT
{
float4 pos: SV_Position;
float2 uv1 : Texcoord1;
float2 uv2 : Texcoord2; *
};
```



\* La rimozione di codice non recapitabile di Direct3D 9 rimuoverebbe la dichiarazione nello shader a causa della rimozione del codice inattivo condizionale


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



In alternativa, è possibile rendere ancora più ovvio che la costante è una costante in fase di compilazione con la dichiarazione seguente:


```
#define LIGHT_MAPPED false
```



Nell'esempio precedente, in Direct3D 9, l'elemento UV2 verrebbe rimosso a causa di ottimizzazioni del codice inattivo nel compilatore. In Direct3D 10, il codice inattivo verrà comunque rimosso, ma il layout dell'assembler di input dello shader richiede la definizione dei dati di input. Il livello Reflection dello shader fornisce i mezzi per gestire questa situazione in modo generico, per cui è possibile attraversare i requisiti di input dello shader e assicurarsi di fornire una descrizione completa del flusso di input al mapping della firma dello shader.

Di seguito è riportato un esempio di funzione per rilevare l'esistenza di un nome/indice semantico in una firma della funzione:


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



### <a name="state-object-creation"></a>Creazione di oggetti stato

Quando si esegue il porting del codice del motore, potrebbe essere utile usare inizialmente un set predefinito di oggetti stato e disabilitare tutte le impostazioni dello stato di rendering del dispositivo Direct3D 9 o dello stato della trama. Questa operazione causerà il rendering degli artefatti, ma è il modo più rapido per iniziare a eseguire le operazioni. In un secondo momento è possibile costruire un sistema di gestione degli oggetti stato che può utilizzare una chiave composta per consentire il riutilizzo massimo del numero di oggetti di stato utilizzati.

## <a name="porting-textures"></a>Porting di trame

### <a name="file-formats-supported"></a>Formati di file supportati

Le funzioni **D3DXxxCreateXXX** e **D3DXxxSaveXXX** che creano o salvano una trama da o a un file di grafica (ad esempio, [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)) supportano un set di formati di file diverso in Direct3D 10 rispetto a quanto fatto in Direct3D 9:



| Formato file | Direct3D 9 | Direct3D 10 |
|-------------|------------|-------------|
| bmp        | x          | x           |
| jpg        | x          | x           |
| .tga        | x          |             |
| png        | x          | x           |
| .dds        | x          | x           |
| . ppm        | x          |             |
| dib        | x          |             |
| . HDR        | x          |             |
| . PFM        | x          |             |
| tiff       |            | x           |
| gif        |            | x           |
| tif        |            | x           |



 

Per informazioni dettagliate, confrontare le enumerazioni [**\_ FileFormat D3DXIMAGE**](../direct3d9/d3dximage-fileformat.md) di Direct3D 9 con le enumerazioni del [**\_ formato del \_ file \_ di immagine d3dx10**](d3dx10-image-file-format.md) per Direct3D 10.

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8. Per l'elaborazione dei file di trama, è consigliabile usare [DirectXTex](https://github.com/Microsoft/DirectXTex).

 

### <a name="mapping-texture-formats"></a>Mapping di formati di trama

La tabella seguente illustra il mapping dei formati di trama da Direct3D 9 a Direct3D 10. Eventuali contenuti in formati non disponibili in DXGI dovranno essere convertiti da routine di utilità.



| Formato Direct3D 9                   | Formato Direct3D 10                                                                                                                                                                                                                                   |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DFMT \_ sconosciuto                     | \_formato DXGI \_ sconosciuto                                                                                                                                                                                                                                |
| \_R8G8B8 D3DFMT                      | Non disponibile                                                                                                                                                                                                                                        |
| \_A8R8G8B8 D3DFMT                    | DXGI \_ Format \_ B8G8R8A8 \_ UNORM & DXGI \_ Format \_ B8G8R8A8 \_ UNORM \_ sRGB ¹                                                                                                                                                                                 |
| \_X8R8G8B8 D3DFMT                    | DXGI \_ Format \_ B8G8R8X8 \_ UNORM & DXGI \_ Format \_ B8G8R8X8 \_ UNORM \_ sRGB ¹                                                                                                                                                                                 |
| \_R5G6B5 D3DFMT                      | \_Formato DXGI \_ B5G6R5 \_ UNORM ²                                                                                                                                                                                                                         |
| \_X1R5G5B5 D3DFMT                    | Non disponibile                                                                                                                                                                                                                                        |
| \_A1R5G5B5 D3DFMT                    | \_Formato DXGI \_ B5G5R5A1 \_ UNORM ²                                                                                                                                                                                                                       |
| \_A4R4G4B4 D3DFMT                    | DXGI \_ Format \_ B4G4R4A4 \_ UNORM ³                                                                                                                                                                                                                       |
| \_R3G3B2 D3DFMT                      | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ a8                          | \_Formato DXGI \_ a8 \_ UNORM                                                                                                                                                                                                                              |
| \_A8R3G3B2 D3DFMT                    | Non disponibile                                                                                                                                                                                                                                        |
| \_X4R4G4B4 D3DFMT                    | Non disponibile                                                                                                                                                                                                                                        |
| \_A2B10G10R10 D3DFMT                 | \_Formato DXGI \_ R10G10B10A2                                                                                                                                                                                                                            |
| \_A8B8G8R8 D3DFMT                    | DXGI \_ Format \_ R8G8B8A8 \_ UNORM & DXGI \_ Format \_ R8G8B8A8 \_ UNORM \_ sRGB                                                                                                                                                                                  |
| \_X8B8G8R8 D3DFMT                    | Non disponibile                                                                                                                                                                                                                                        |
| \_G16R16 D3DFMT                      | \_Formato DXGI \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| \_A2R10G10B10 D3DFMT                 | Non disponibile                                                                                                                                                                                                                                        |
| \_A16B16G16R16 D3DFMT                | \_Formato DXGI \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| \_A8P8 D3DFMT                        | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ P8                          | Non disponibile                                                                                                                                                                                                                                        |
| \_L8 D3DFMT                          | DXGI \_ formato \_ R8 \_ UNORM Nota: usare. r swizzle in shader per duplicare il rosso con altri componenti per ottenere il comportamento di d3d9.                                                                                                                                    |
| \_A8L8 D3DFMT                        | DXGI \_ Format \_ R8G8 \_ UNORM Nota: usare Swizzle. rrrg in shader per duplicare il rosso e spostare il verde nei componenti alfa per ottenere il comportamento di d3d9.                                                                                                            |
| \_A4L4 D3DFMT                        | Non disponibile                                                                                                                                                                                                                                        |
| \_V8U8 D3DFMT                        | DXGI \_ Format \_ R8G8 \_ russar                                                                                                                                                                                                                            |
| \_L6V5U5 D3DFMT                      | Non disponibile                                                                                                                                                                                                                                        |
| \_X8L8V8U8 D3DFMT                    | Non disponibile                                                                                                                                                                                                                                        |
| \_Q8W8V8U8 D3DFMT                    | DXGI \_ Format \_ R8G8B8A8 \_ russar                                                                                                                                                                                                                        |
| \_V16U16 D3DFMT                      | DXGI \_ Format \_ R16G16 \_ russar                                                                                                                                                                                                                          |
| \_W11V11U10 D3DFMT                   | Non disponibile                                                                                                                                                                                                                                        |
| \_A2W10V10U10 D3DFMT                 | Non disponibile                                                                                                                                                                                                                                        |
| \_UYVY D3DFMT                        | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ R8G8 \_ B8G8                  | DXGI \_ Format \_ G8R8 \_ G8B8 \_ UNORM (in DX9 i dati sono stati ridimensionati da 255.0 f, ma questo può essere gestito nel codice dello shader).                                                                                                                                   |
| \_YUY2 D3DFMT                        | Non disponibile                                                                                                                                                                                                                                        |
| D3DFMT \_ G8R8 \_ G8B8                  | DXGI \_ Format \_ R8G8 \_ B8G8 \_ UNORM (in DX9 i dati sono stati ridimensionati da 255.0 f, ma questo può essere gestito nel codice dello shader).                                                                                                                                   |
| \_DXT1 D3DFMT                        | DXGI \_ Format \_ BC1 \_ UNORM & DXGI \_ Format \_ BC1 \_ UNORM \_ sRGB                                                                                                                                                                                            |
| \_DXT2 D3DFMT                        | DXGI \_ Format \_ BC1 \_ UNORM & DXGI \_ Format \_ BC1 \_ UNORM \_ sRGB Nota: DXT1 e DXT2 sono uguali dal punto di vista dell'API o dell'hardware... l'unica differenza è' premoltiplicated Alpha ', che può essere rilevata da un'applicazione e non necessita di un formato separato. |
| \_DXT3 D3DFMT                        | DXGI \_ Format \_ BC2 \_ UNORM & DXGI \_ Format \_ BC2 \_ UNORM \_ sRGB                                                                                                                                                                                            |
| \_DXT4 D3DFMT                        | DXGI \_ Format \_ BC2 \_ UNORM & DXGI \_ Format \_ BC2 \_ UNORM \_ sRGB Nota: DXT3 e DXT4 sono uguali dal punto di vista dell'API o dell'hardware... l'unica differenza è' premoltiplicated Alpha ', che può essere rilevata da un'applicazione e non necessita di un formato separato. |
| \_DXT5 D3DFMT                        | DXGI \_ Format \_ BC3 \_ UNORM & DXGI \_ Format \_ BC3 \_ UNORM \_ sRGB                                                                                                                                                                                            |
| D3DFMT \_ D16 & D3DFMT \_ D16 \_ lockable | \_Formato DXGI \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| \_D32 D3DFMT                         | Non disponibile                                                                                                                                                                                                                                        |
| \_D15S1 D3DFMT                       | Non disponibile                                                                                                                                                                                                                                        |
| \_D24S8 D3DFMT                       | Non disponibile                                                                                                                                                                                                                                        |
| \_D24X8 D3DFMT                       | Non disponibile                                                                                                                                                                                                                                        |
| \_D24X4S4 D3DFMT                     | Non disponibile                                                                                                                                                                                                                                        |
| \_D16 D3DFMT                         | \_Formato DXGI \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ D32F \_ lockable              | \_Formato DXGI \_ D32 \_ float                                                                                                                                                                                                                             |
| \_D24FS8 D3DFMT                      | Non disponibile                                                                                                                                                                                                                                        |
| \_S1D15 D3DFMT                       | Non disponibile                                                                                                                                                                                                                                        |
| \_S8D24 D3DFMT                       | DXGI \_ Format \_ D24 \_ UNORM \_ S8 \_ uint                                                                                                                                                                                                                   |
| \_X8D24 D3DFMT                       | Non disponibile                                                                                                                                                                                                                                        |
| \_X4S4D24 D3DFMT                     | Non disponibile                                                                                                                                                                                                                                        |
| \_L16 D3DFMT                         | DXGI \_ Format \_ R16 \_ UNORM Nota: usare. r swizzle in shader per duplicare il rosso degli altri componenti per ottenere il comportamento di d3d9.                                                                                                                                   |
| \_INDEX16 D3DFMT                     | \_Formato DXGI \_ R16 \_ uint                                                                                                                                                                                                                              |
| \_INDEX32 D3DFMT                     | \_Formato DXGI \_ R32 \_ uint                                                                                                                                                                                                                              |
| \_Q16W16V16U16 D3DFMT                | DXGI \_ Format \_ R16G16B16A16 \_ russar                                                                                                                                                                                                                    |
| D3DFMT \_ MULTi2 \_ ARGB8               | Non disponibile                                                                                                                                                                                                                                        |
| \_R16F D3DFMT                        | \_Formato DXGI \_ R16 \_ float                                                                                                                                                                                                                             |
| \_G16R16F D3DFMT                     | \_Formato DXGI \_ R16G16 \_ float                                                                                                                                                                                                                          |
| \_A16B16G16R16F D3DFMT               | \_Formato DXGI \_ R16G16B16A16 \_ float                                                                                                                                                                                                                    |
| \_R32F D3DFMT                        | \_Formato DXGI \_ R32 \_ float                                                                                                                                                                                                                             |
| \_G32R32F D3DFMT                     | \_Formato DXGI \_ R32G32 \_ float                                                                                                                                                                                                                          |
| \_A32B32G32R32F D3DFMT               | \_Formato DXGI \_ R32G32B32A32 \_ float                                                                                                                                                                                                                    |
| \_CXV8U8 D3DFMT                      | Non disponibile                                                                                                                                                                                                                                        |
| \_FLOAT1 D3DDECLTYPE                 | \_Formato DXGI \_ R32 \_ float                                                                                                                                                                                                                             |
| \_FLOAT2 D3DDECLTYPE                 | \_Formato DXGI \_ R32G32 \_ float                                                                                                                                                                                                                          |
| \_FLOAT3 D3DDECLTYPE                 | \_Formato DXGI \_ R32G32B32 \_ float                                                                                                                                                                                                                       |
| \_Float4 D3DDECLTYPE                 | \_Formato DXGI \_ R32G32B32A32 \_ float                                                                                                                                                                                                                    |
| D3DDECLTYPED3DCOLOR                 | Non disponibile                                                                                                                                                                                                                                        |
| \_UBYTE4 D3DDECLTYPE                 | DXGI \_ Format \_ R8G8B8A8 \_ uint Nota: shader ottiene i valori uint, ma se sono necessari i float integrali di tipo Direct3D 9 (0,0 f, 1.0 f... 255. f), UINT può essere semplicemente convertito in float32 in shader.                                                               |
| \_SHORT2 D3DDECLTYPE                 | DXGI \_ Format \_ R16G16 \_ Sint Nota: shader ottiene i valori Sint, ma se sono necessari i float integrali dello stile Direct3D 9, è possibile convertire Sint solo in float32 in shader.                                                                                       |
| \_SHORT4 D3DDECLTYPE                 | DXGI \_ Format \_ R16G16B16A16 \_ Sint Nota: shader ottiene i valori Sint, ma se sono necessari i float integrali dello stile Direct3D 9, è possibile convertire Sint solo in float32 in shader.                                                                                 |
| \_Dati UBYTE4N D3DDECLTYPE                | \_Formato DXGI \_ R8G8B8A8 \_ UNORM                                                                                                                                                                                                                        |
| \_SHORT2N D3DDECLTYPE                | DXGI \_ Format \_ R16G16 \_ russar                                                                                                                                                                                                                          |
| \_SHORT4N D3DDECLTYPE                | DXGI \_ Format \_ R16G16B16A16 \_ russar                                                                                                                                                                                                                    |
| \_USHORT2N D3DDECLTYPE               | \_Formato DXGI \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| \_USHORT4N D3DDECLTYPE               | \_Formato DXGI \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| \_UDEC3 D3DDECLTYPE                  | Non disponibile                                                                                                                                                                                                                                        |
| \_DEC3N D3DDECLTYPE                  | Non disponibile                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2             | \_Formato DXGI \_ R16G16 \_ float                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4             | \_Formato DXGI \_ R16G16B16A16 \_ float                                                                                                                                                                                                                    |
| FourCC 'ATI1'                       | \_Formato DXGI \_ BC4 \_ UNORM                                                                                                                                                                                                                             |
| FourCC 'ATI2'                       | \_Formato DXGI \_ BC5 \_ UNORM                                                                                                                                                                                                                             |



 

¹ DXGI 1,1, incluso nel runtime di Direct3D 11, include i formati BGRA. Tuttavia, il supporto per questi formati è facoltativo per i dispositivi Direct3D 10 e 10,1 con i driver implementati per Windows Display Driver Model (WDDM) per Windows Vista (WDDM 1,0). Prendere in considerazione l'uso di DXGI \_ Format \_ R8G8B8A8 \_ UNORM. In alternativa, è possibile creare il dispositivo con [**D3D10 \_ creare \_ il \_ \_ supporto di BGRA**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) per il dispositivo per assicurarsi di supportare solo i computer con il runtime Direct3D 11,0 e un driver WDDM 1,1 o versione successiva.

² DXGI 1,0 i formati 5:6:5 e 5:5:5:1 definiti, ma non sono supportati dal runtime Direct3D 10. x o Direct3D 11,0. Questi formati sono facoltativamente supportati con DXGI 1,2 nel runtime di DirectX 11,1, necessario per le schede video a livello di funzionalità 11,1 e WDDM 1,2 (visualizzazione del modello di driver a partire da Windows 8) e già supportati nei livelli di funzionalità di 10level9.

³ DXGI 1,2 ha introdotto il formato 4:4:4:4. Questo formato è facoltativamente supportato nel runtime di DirectX 11,1, necessario per le schede video a 11,1 livello di funzionalità e per i driver WDDM 1,2 e già supportato nei livelli di funzionalità di 10level9.

Per i formati non compressi, DXGI ha limitato il supporto per i modelli di formato pixel arbitrari; tutti i formati non compressi devono essere di tipo RGBA. Potrebbe essere necessario swizzling dei formati di pixel degli asset esistenti, che è consigliabile calcolare come passaggio pre-elaborazione offline, laddove possibile.

## <a name="porting-shaders"></a>Porting degli shader

### <a name="direct3d-10-shaders-are-authored-in-hlsl"></a>Gli shader Direct3D 10 sono stati creati in HLSL

Direct3D 10 limita l'uso del linguaggio assembly a quello solo a scopo di debug, pertanto è necessario convertire in HLSL gli shader assembly scritti in mano usati in Direct3D 9.

### <a name="shader-signatures-and-linkage"></a>Firme shader e collegamento

Sono stati discussi i requisiti per il collegamento degli assembly di input alle firme di input del vertex shader in precedenza in questo documento (vedere sopra). Si noti che il runtime di Direct3D 10 ha anche inasprito i requisiti per la fase di gestione del collegamento tra gli shader. Questa modifica influirà sulle origini dello shader in cui l'associazione tra fasi potrebbe non essere stata completamente descritta in Direct3D 9. Ad esempio:


```
VS_OUTPUT                       PS_INPUT
float4   pos : SV_POSITION;     float4 pos : SV_POSITION;
float4   uv1 : TEXCOORD1;       float4 uv1 : TEXCOORD1;
float4x3 tangentSp : TEXCOORD2; float4 tangent : TEXCOORD2; *
float4   Color : TEXCOORD6;     float4 color : TEXCOORD6;
```



\* Collegamento a VS-PS interruppe: anche se il pixel shader potrebbe non essere interessato alla matrice completa, il collegamento deve specificare il float4x3 completo.

Si noti che la semantica del collegamento tra le fasi deve corrispondere esattamente, tuttavia gli input delle fasi di destinazione possono essere un prefisso dei valori di output. Nell'esempio precedente, il pixel shader potrebbe avere position e texcoord1 come unici input, ma non può avere la posizione e texcoord2 come unici input a causa dei vincoli di ordinamento.

### <a name="hlsl-shader-stage-linkages"></a>Collegamenti alla fase HLSL shader

Il collegamento tra gli shader può essere eseguito in uno dei punti seguenti della pipeline:

-   Input assembler in vertex shader
-   Vertex shader al pixel shader
-   Vertex shader in Geometry shader
-   Vertex shader per eseguire il flusso dell'output
-   Geometry shader in pixel shader
-   Geometry shader per la trasmissione in streaming

### <a name="constant-buffers"></a>Buffer costanti

Per semplificare il trasferimento di contenuto da Direct3D 9, un approccio iniziale alla gestione costante all'esterno del sistema di effetti potrebbe implicare la creazione di un singolo buffer costante contenente tutte le costanti obbligatorie. È importante che le prestazioni ordinino le costanti nei buffer in base alla frequenza di aggiornamento prevista. Questa organizzazione ridurrà al minimo la quantità di set di costanti ridondanti.

### <a name="user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Piani di ritaglio utente in HLSL a livello di funzionalità 9 e superiore

A partire da Windows 8, è possibile usare l'attributo della funzione **clipplanes** in una [dichiarazione di funzione](../direct3dhlsl/dx-graphics-hlsl-function-syntax.md) HLSL anziché [SV \_ Clipdistance](../direct3dhlsl/dx-graphics-hlsl-semantics.md) per fare in modo che lo shader funzioni con il [livello di funzionalità](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x, nonché con il livello di funzionalità 10 e versioni successive. Per altre informazioni, vedere la pagina [relativa ai piani di ritaglio utente su hardware di livello funzionalità 9](../direct3dhlsl/user-clip-planes-on-10level9.md).

## <a name="additional-direct3d-10-differences-to-watch-for"></a>Altre differenze di Direct3D 10 da controllare

### <a name="integers-as-input"></a>Integer come input

In Direct3D 9 non era disponibile un supporto hardware reale per i tipi di dati Integer, tuttavia l'hardware Direct3D 10 supporta i tipi Integer espliciti. Se si dispone di dati a virgola mobile nel buffer del vertice, è necessario disporre di un input float. In caso contrario, un tipo integer sarà la rappresentazione dello schema di bit del valore a virgola mobile. Un tipo integer non è consentito per un input pixel shader a meno che il valore non sia contrassegnato per nessuna interpolazione (vedere [modificatori di interpolazione](../direct3dhlsl/dx-graphics-hlsl-struct.md)).

### <a name="mouse-cursors"></a>Cursori del mouse

Nelle versioni precedenti di Windows le routine del cursore del mouse GDI standard non funzionano correttamente in tutti i dispositivi esclusivi a schermo intero. Per gestire questi casi sono state aggiunte le API [**SetCursorProperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties), [**ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)e [**SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition) . Poiché la versione di GDI di Windows Vista comprende completamente le superfici [DXGI](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md) , non è necessario disporre di questa API del cursore del mouse specializzata, pertanto non esiste alcun equivalente Direct3D 10. Per le applicazioni Direct3D 10 è invece consigliabile utilizzare le [routine del cursore del mouse GDI](../menurc/cursors.md) standard per i cursori del mouse.

### <a name="mapping-texels-to-pixels-in-direct3d-10"></a>Mapping dei Texel ai pixel in Direct3D 10

In Direct3D 9, i centri di Texel e i pixel sono stati divisi a metà (vedere [mapping diretto dei Texel ai pixel (Direct3D 9)](../direct3d9/directly-mapping-texels-to-pixels.md)). In Direct3D 10, i centri Texel sono già a metà unità, pertanto non è necessario spostare le coordinate del vertice.

Il rendering di quad a schermo intero è più semplice con Direct3D 10. I quad a schermo intero devono essere definiti in clipspace (-1, 1) e passati semplicemente attraverso vertex shader senza alcuna modifica. In questo modo, non è necessario ricaricare il buffer di vertex ogni volta che la risoluzione dello schermo viene modificata e non è presente alcun lavoro aggiuntivo nel pixel shader per manipolare le coordinate di trama.

### <a name="reference-counting-behavior-changes"></a>Conteggio dei riferimenti modifiche del comportamento

Diversamente dalle versioni precedenti di Direct3D, le varie funzioni set non conterranno un riferimento agli oggetti Devices. Ciò significa che l'applicazione deve assicurarsi che contenga un riferimento all'oggetto per il periodo di tempo in cui si desidera associare tale oggetto alla pipeline. Quando il conteggio dei riferimenti dell'oggetto scende a zero, l'oggetto sarà disassociato dalla pipeline mentre viene eliminato definitivamente. Questo stile di riferimento è noto anche come tenuta a riferimento debole, quindi ogni percorso di associazione nell'oggetto dispositivo contiene un riferimento debole all'interfaccia/oggetto. Se non specificato diversamente in modo esplicito, questo comportamento deve essere presupposto per tutti i metodi set. Ogni volta che l'eliminazione di un oggetto comporta l'impostazione di un punto di associazione su **null** , il livello di debug emetterà un avviso. Si noti che le chiamate ai metodi Get del dispositivo, ad esempio [**OMGetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omgetrendertargets) , aumenteranno il conteggio dei riferimenti degli oggetti restituiti.

### <a name="test-cooperative-level"></a>Livello cooperativa di test

La funzionalità di [**TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel) dell'API Direct3D 9 è analoga all'impostazione [del \_ \_ test presente in DXGI](../direct3ddxgi/dxgi-present.md) quando si chiama [**present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present).

### <a name="stretchrect"></a>StretchRect

Una funzione simile al metodo Direct3D 9 [**IDirect3DDevice9:: StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) non è disponibile in Direct3D 10 e 10,1. Per copiare le superfici delle risorse, usare [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion). Per le operazioni di ridimensionamento, eseguire il rendering in una trama usando il filtro della trama. Per la conversione di superfici MSAA in superfici non MSAA, utilizzare [**ID3D10Device:: ResolveSubresource**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-resolvesubresource).

## <a name="additional-direct3d-101-differences"></a>Differenze aggiuntive con Direct3D 10,1

Windows Vista con Service Pack 1 (SP1) include un aggiornamento secondario a Direct3D 10 e Direct3D 10,1, che ha esposto le seguenti funzionalità hardware aggiuntive:

-   Shader per campione MSAA
-   Read-back profondità MSAA
-   Modalità di Blend indipendenti per destinazione di rendering
-   Matrici mappa cubo
-   Rendering in formati con compressione in blocchi (BC)

L'aggiornamento di Direct3D 10,1 ha aggiunto il supporto per le nuove interfacce seguenti, derivate dalle interfacce esistenti:

-   [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)
-   [**ID3D10BlendState1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)
-   [**ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1)

L'aggiornamento di Direct3D 10,1 include anche le strutture aggiuntive seguenti:

-   [**\_ \_ DESC1 Blend di destinazione di rendering D3D10 \_ \_**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_render_target_blend_desc1)
-   [**\_DESC1 Blend \_ D3D10**](/windows/desktop/api/D3D10_1/ns-d3d10_1-d3d10_blend_desc1)
-   [**\_ \_ Visualizzazione risorse shader D3D10 \_ \_ DESC1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_shader_resource_view_desc1)

L'API Direct3D 10,1 include un nuovo concetto denominato livello di funzionalità. Questo concetto significa che è possibile usare l'API Direct3D 10,1 per guidare l'hardware Direct3D 10,0 ([**\_ livello di funzionalità D3D10 \_ \_ 10 \_ 0**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)) o Direct3D 10,1 ([**D3D10 \_ funzionalità \_ livello \_ 10 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)). Poiché l'API Direct3D 10,1 è derivata dalle interfacce Direct3D 10, le applicazioni possono creare un dispositivo Direct3D 10,1, quindi usarlo come dispositivo Direct3D 10,0, tranne nel caso in cui siano necessarie nuove funzionalità specifiche di 10,1 (purché sia presente il livello di funzionalità di **\_ \_ \_ 10 \_ 1** a livello di funzionalità di D3D10 e supporti queste funzionalità).

> [!Note]  
> I dispositivi Direct3D 10,1 possono usare i profili shader 10,0 HLSL esistenti (vs \_ 4 \_ 0, PS \_ 4 \_ 0, GS \_ 4 \_ 0) e i nuovi profili 10,1 (vs \_ 4 \_ 1, PS \_ 4 \_ 1, GS \_ 4 \_ 1) con ulteriori istruzioni e funzionalità di HLSL.

 

Windows 7 conteneva un aggiornamento secondario all'API Direct3D 10,1 inclusa nel runtime di Direct3D 11. Questo aggiornamento aggiunge il supporto per i livelli di funzionalità seguenti:

-   [**\_Livello di funzionalità D3D10 \_ \_ 9 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**\_Livello di funzionalità D3D10 \_ \_ 9 \_ 2**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**\_Livello di funzionalità D3D10 \_ \_ 9 \_ 3**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)

Windows 7 ha aggiunto anche il supporto per Direct3D 10,1 per [Windows Advanced rasterizzation Platform (Warp)](../direct3darticles/directx-warp.md). È possibile specificare un driver WARP usando il [**\_ tipo di driver D3D10 \_ \_ Warp**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).

Per altre informazioni su Direct3D 10,1, vedere [funzionalità di direct3d 10,1](d3d10-graphics-programming-guide-10-1.md) e [**enumerazione \_ \_ Level1 della funzionalità D3D10**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di programmazione per Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
