---
title: Firma radice versione 1.1
description: Lo scopo della versione 1.1 della firma radice è consentire alle applicazioni di indicare ai driver quando i descrittori in un heap dei descrittori non cambiano o i descrittori di dati puntano a non cambiano.
ms.assetid: 8FE42C1C-7F1D-4E70-A7EE-D5EC67237327
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a7a32576efa4d93a8d26aa57282f06e0d5a02f
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343666"
---
# <a name="root-signature-version-11"></a>Firma radice versione 1.1

Lo scopo della versione 1.1 della firma radice è consentire alle applicazioni di indicare ai driver quando i descrittori in un heap dei descrittori non cambiano o i descrittori di dati puntano a non cambiano. Ciò consente ai driver di eseguire ottimizzazioni che potrebbero essere possibili sapendo che un descrittore o la memoria a cui punta è statica per un certo periodo di tempo.

-   [Panoramica](#overview)
-   [Flag statici e volatili](#static-and-volatile-flags)
    -   [DESCRITTORI \_ VOLATILI](#descriptors_volatile)
    -   [DATA \_ VOLATILE](#data_volatile)
    -   [DATI \_ STATICI \_ DURANTE \_ L'ESECUZIONE \_ \_](#data_static_while_set_at_execute)
    -   [DATI \_ STATICI](#data_static)
    -   [Combinazione di flag](#combining-flags)
    -   [Riepilogo dei flag](#flag-summary)
-   [Riepilogo dell'API versione 1.1](#version-11-api-summary)
    -   [Enumerazioni](#enums)
    -   [Strutture](#helper-structures)
    -   [Funzioni](#functions)
    -   [Metodi](#methods)
    -   [Strutture helper](#helper-structures)
-   [Conseguenze della violazione dei flag statici](#consequences-of-violating-static-ness-flags)
-   [Gestione delle versioni](#version-management)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

La firma radice versione 1.0 consente che il contenuto degli heap dei descrittori e la memoria a cui puntano siano liberamente modificati dalle applicazioni ogni volta che gli elenchi di comandi o i bundle che vi fanno riferimento sono potenzialmente in esecuzione nella GPU. Molto spesso, tuttavia, le applicazioni non necessitano effettivamente della flessibilità necessaria per modificare i descrittori o la memoria dopo la registrazione dei comandi che vi fanno riferimento.

Le applicazioni sono spesso in grado di:

-   Configurare i descrittori (ed è possibile la memoria a cui puntano) prima di associare tabelle descrittori o descrittori radice in un elenco di comandi o in un bundle.
-   Assicurarsi che questi descrittori non cambino fino a quando l'elenco di comandi /bundle che vi fanno riferimento non avrà terminato l'esecuzione per l'ultima volta.
-   Assicurarsi che i dati a cui puntano i descrittori non cambino per la stessa durata completa.

In alternativa, un'applicazione può essere in grado di rispettare solo che i dati non cambiano per un periodo di tempo più breve. In particolare, i dati potrebbero essere statici per la finestra nel tempo durante l'esecuzione dell'elenco dei comandi che un'associazione di parametri radice (tabella descrittore o descrittore radice) punta attualmente ai dati. In altre parole, un'applicazione potrebbe voler eseguire l'esecuzione sulla sequenza temporale della GPU che aggiorna alcuni dati tra i periodi di tempo in cui è impostata tramite un parametro radice, sapendo che quando è impostata sarà statica.

Se i descrittori, o i descrittori di dati puntano a, non cambiano, i driver di ottimizzazione specifici potrebbero essere specifici del fornitore dell'hardware e, soprattutto, non cambiano comportamento oltre a migliorare eventualmente le prestazioni. Mantenere il maggior numero possibile di conoscenze sulla finalità dell'applicazione non grava sulle applicazioni.

Un'ottimizzazione è che molti driver possono produrre accessi alla memoria più efficienti tramite shader se conoscono le promesse che un'applicazione può fare sulla staticità dei descrittori e dei dati. Ad esempio, i driver potrebbero rimuovere un livello di riferimento indiretto per l'accesso a un descrittore in un heap converterlo in un descrittore radice se l'hardware specifico non è sensibile alle dimensioni dell'argomento radice.

L'attività aggiuntiva per gli sviluppatori che usano la versione 1.1 è quella di fare promesse sulla volatilità e sull'staticità dei dati laddove possibile, in modo che i driver possano eseguire le ottimizzazioni più sensato. Gli sviluppatori non devono fare promesse sulla staticità.

La versione 1.0 della firma radice continua a funzionare senza modifiche, anche se per le applicazioni che ricompilano le firme radice viene ora impostata la firma radice 1.1 (con un'opzione per forzare la versione 1.0 se lo si desidera).

## <a name="static-and-volatile-flags"></a>Flag statici e volatili

I flag seguenti fanno parte della firma radice per consentire ai driver di scegliere una strategia per gestire al meglio i singoli argomenti radice quando vengono impostati e incorporare gli stessi presupposti in oggetti di stato della pipeline (PSO) quando vengono compilati in origine, perché la firma radice fa parte di un pso.

I flag seguenti vengono impostati dall'app e si applicano ai descrittori o ai dati.

``` syntax
typedef enum D3D12_DESCRIPTOR_RANGE_FLAGS
{
    D3D12_DESCRIPTOR_RANGE_FLAG_NONE    = 0,
    D3D12_DESCRIPTOR_RANGE_FLAG_DESCRIPTORS_VOLATILE    = 0x1,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_VOLATILE   = 0x2,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE    = 0x4,
    D3D12_DESCRIPTOR_RANGE_FLAG_DATA_STATIC = 0x8
} D3D12_DESCRIPTOR_RANGE_FLAGS;

typedef enum D3D12_ROOT_DESCRIPTOR_FLAGS
{
    D3D12_ROOT_DESCRIPTOR_FLAG_NONE = 0,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_VOLATILE    = 0x2,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC_WHILE_SET_AT_EXECUTE = 0x4,
    D3D12_ROOT_DESCRIPTOR_FLAG_DATA_STATIC  = 0x8
} D3D12_ROOT_DESCRIPTOR_FLAGS;
```

### <a name="descriptors_volatile"></a>DESCRITTORI \_ VOLATILI

Con questo flag impostato, i descrittori in un heap dei descrittori a cui punta una tabella dei descrittori radice possono essere modificati dall'applicazione in qualsiasi momento, ad eccezione del fatto che l'elenco di comandi o i bundle che associano la tabella dei descrittori sono stati inviati e non hanno terminato l'esecuzione. Ad esempio, la registrazione di un elenco di comandi e  la successiva modifica dei descrittori in un heap descrittore a cui fa riferimento prima di inviare l'elenco di comandi per l'esecuzione è valida. Questo è l'unico comportamento supportato della firma radice versione 1.0.

Se il flag DESCRIPTORS \_ VOLATILE non *è* impostato, i descrittori sono statici. Non esiste alcun flag per questa modalità. I descrittori statici significano che i descrittori in un heap dei descrittori a cui punta una tabella di descrittori radice sono stati inizializzati al momento dell'impostazione della tabella dei descrittori in un elenco di comandi/bundle (durante la registrazione) e i descrittori non possono essere modificati fino al termine dell'esecuzione dell'elenco di comandi/bundle per l'ultima volta. *Per la firma radice versione 1.1,* i descrittori statici sono il presupposto predefinito e l'applicazione deve specificare il flag VOLATILE DESCRIPTORS \_ quando necessario.

Per i bundle che usano tabelle di descrittori con descrittori statici, i descrittori devono essere pronti a partire dal momento in cui viene registrato il bundle (anziché quando viene chiamato il bundle) e non cambiano fino al termine dell'esecuzione del bundle per l'ultima volta. Le tabelle dei descrittori che puntano a descrittori statici devono essere impostate durante la registrazione del bundle e non ereditate nel bundle. È valido per un elenco di comandi usare una tabella di descrittori con descrittori statici che sono stati impostati in un bundle e restituiti all'elenco di comandi.

Quando i descrittori sono statici, è presente un'altra modifica del comportamento che richiede l'impostazione del flag DESCRIPTORS \_ VOLATILE. Gli accessi non compresi nei limiti a qualsiasi vista buffer (a differenza delle viste Texture1D/2D/3D/Cube) non sono validi e producono risultati non definiti, inclusa la possibile reimpostazione del dispositivo, anziché restituire i valori predefiniti per le operazioni di lettura o eliminazione delle scritture. Lo scopo della rimozione della possibilità per le applicazioni di dipendere dall'hardware fuori dai limiti di controllo di accesso è consentire ai driver di scegliere di promuovere gli accessi ai descrittori statici agli accessi ai descrittori radice se lo ritengono più efficiente. I descrittori radice non supportano il controllo dei limiti.

Se le applicazioni dipendono dal comportamento di accesso alla memoria fuori dai limiti quando accedono ai descrittori, è necessario contrassegnare gli intervalli di descrittori che accedono a tali descrittori come \_ DESCRIPTORS VOLATILE.

### <a name="data_volatile"></a>DATA \_ VOLATILE

Con questo flag impostato, i dati a cui puntano i descrittori possono essere modificati dalla CPU in qualsiasi momento, ad eccezione del fatto che l'elenco di comandi/aggregazioni che associano la tabella dei descrittori è stato inviato e non ha completato l'esecuzione. Questo è l'unico comportamento supportato della firma radice versione 1.0.

Il flag è disponibile sia nei flag dell'intervallo di descrittori che nei flag del descrittore radice.

### <a name="data_static_while_set_at_execute"></a>DATI \_ STATICI \_ DURANTE \_ L'ESECUZIONE \_ \_

Con questo flag impostato, i dati a cui puntano i descrittori non possono cambiare a partire da quando la tabella del descrittore radice o del descrittore sottostante è impostata su un elenco di comandi/bundle durante l'esecuzione nella sequenza temporale della GPU e termina quando i successivi disegni/dispatch non fanno più riferimento ai dati.

Prima che un descrittore radice o una tabella descrittore  sia stata impostata nella GPU, questi dati possono essere modificati anche dallo stesso elenco di comandi/bundle. I dati possono anche essere modificati mentre un descrittore radice o una tabella di descrittori che vi punta è ancora impostato sull'elenco di comandi o sul bundle, purché le operazioni di disegno/invio che vi fanno riferimento siano state completate. In questo modo, tuttavia, è necessario che la tabella dei descrittori venga nuovamente associata all'elenco dei comandi prima della successiva dereferenziazione del descrittore radice o della tabella dei descrittori. Ciò consente al driver di sapere che i dati a cui punta un descrittore radice o una tabella di descrittori sono stati modificati.

La differenza essenziale tra DATA STATIC WHILE SET AT EXECUTE e DATA VOLATILE è data VOLATILE. Un driver non è in grado di stabilire se le copie dei dati in un elenco di comandi hanno modificato i dati a cui punta un descrittore, senza eseguire il rilevamento dello stato \_ \_ \_ \_ \_ \_ \_ aggiuntivo. Pertanto, se, ad esempio, un driver può inserire qualsiasi tipo di comandi di pre-recupero dei dati nel proprio elenco di comandi (per rendere più efficiente l'accesso dello shader ai dati noti, ad esempio), DATA STATIC WHILE SET AT EXECUTE consente al driver di sapere che è necessario solo eseguire il pre-recupero dei dati nel momento in cui viene impostato tramite \_ \_ \_ \_ \_ [**SetGraphicsRootDescriptorTable,**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) [**SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable) o uno dei metodi per impostare la visualizzazione costante del buffer, la visualizzazione delle risorse shader o la visualizzazione di accesso non ordinato.

Per i bundle, la promessa che i dati sono statici durante l'esecuzione viene applicata in modo univoco a ogni esecuzione del bundle.

Il flag è disponibile sia nei flag di intervallo dei descrittori che nei flag del descrittore radice.

### <a name="data_static"></a>DATI \_ STATICI

Se questo flag è impostato, i dati a cui puntano i descrittori sono stati inizializzati nel momento in cui un descrittore radice o una tabella di descrittori che fa riferimento alla memoria è stata impostata in un elenco di comandi/bundle durante la registrazione e i dati non possono essere modificati fino al termine dell'esecuzione dell'elenco di comandi o del bundle per l'ultima volta.

Per i bundle, la durata statica inizia in corrispondenza dell'impostazione del descrittore radice o della tabella dei descrittori durante la registrazione del bundle, anziché di un elenco di comandi chiamanti. Inoltre, una tabella descrittore che punta a dati statici deve essere impostata nel bundle e non ereditata. È valido per un elenco di comandi usare una tabella di descrittori che punta ai dati statici che sono stati impostati in un bundle e restituiti all'elenco di comandi.

Il flag è disponibile sia nei flag dell'intervallo di descrittori che nei flag del descrittore radice.

### <a name="combining-flags"></a>Combinazione di flag

È possibile specificare al massimo uno dei flag DATA alla volta, ad eccezione degli intervalli di descrittori sampler che non supportano affatto i flag DATA poiché i campionatori non puntano ai dati.

L'assenza di flag DATA per gli intervalli di descrittori SRV e CBV implica l'impostazione predefinita del comportamento DATA \_ STATIC WHILE SET AT \_ \_ \_ \_ EXECUTE. Il motivo per cui questa impostazione predefinita viene scelta invece di DATA STATIC è che DATA STATIC WHILE SET AT EXECUTE è molto più probabile che sia un'impostazione predefinita sicura per la maggior parte dei casi, pur continuando a produrre un'opportunità di ottimizzazione migliore rispetto all'impostazione predefinita \_ \_ di DATA \_ \_ \_ \_ \_ VOLATILE.

L'assenza di flag DATA per gli intervalli di descrittori UAV implica l'impostazione predefinita del comportamento DATA VOLATILE, dato che in genere vengono scritte \_ UAV.

DESCRIPTORS \_ VOLATILE non *può* essere combinato con DATA \_ STATIC, ma *può* essere combinato con gli altri flag DATA. Il motivo per cui DESCRIPTORS VOLATILE può essere combinato con DATA STATIC WHILE SET AT EXECUTE è che i descrittori volatili richiedono comunque che i descrittori siano pronti durante l'esecuzione dell'elenco di comandi/bundle e DATA STATIC WHILE SET AT EXECUTE sta solo facendo promesse sulla staticità all'interno di un subset di esecuzione dell'elenco di \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ comandi/bundle.

### <a name="flag-summary"></a>Riepilogo dei flag

Le tabelle seguenti riepilogano le combinazioni di flag che potrebbero essere utilizzate.



| Impostazioni valide di D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAGS                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nessun flag impostato                                                   | I descrittori sono statici (impostazione predefinita). Presupposti predefiniti per i dati: per SRV/CBV: DATA STATIC WHILE SET AT EXECUTE e \_ \_ per \_ \_ \_ UAV: DATA \_ VOLATILE. Queste impostazioni predefinite per SRV/CBV si adattano in modo sicuro ai modelli di utilizzo per la maggior parte delle firme radice.                                                                                              |
| DATI \_ STATICI                                                   | Sia i descrittori che i dati sono statici. In questo modo è possibile ottimizzare le potenzialità di ottimizzazione dei driver.                                                                                                                                                                                                                                                          |
| DATA \_ VOLATILE                                                 | I descrittori sono statici e i dati sono volatili.                                                                                                                                                                                                                                                                                                     |
| DATI \_ STATICI \_ DURANTE \_ L'IMPOSTAZIONE \_ IN FASE DI \_ ESECUZIONE                          | I descrittori sono statici e i dati sono statici durante l'esecuzione.                                                                                                                                                                                                                                                                                      |
| DESCRITTORI \_ VOLATILI                                          | I descrittori sono volatili e si presunzione predefinita sui dati: per SRV/CBV: DATA STATIC WHILE SET AT EXECUTE e \_ \_ per \_ \_ \_ UAV: DATA \_ VOLATILE.                                                                                                                                                                                              |
| DESCRITTORI DATI \_ VOLATILI \| \_ VOLATILE                        | Sia i descrittori che i dati sono volatili, equivalenti alla firma radice 1.0.                                                                                                                                                                                                                                                                            |
| DESCRITTORI DATI \_ VOLATILI \| \_ STATICI DURANTE \_ \_ L'IMPOSTAZIONE IN FASE DI \_ \_ ESECUZIONE | I descrittori sono volatili, ma si noti che non consentono comunque la modifica durante l'esecuzione dell'elenco dei comandi. È quindi valido combinare la dichiarazione aggiuntiva che i dati sono statici durante l'impostazione tramite la tabella dei descrittori radice durante l'esecuzione. I descrittori sottostanti sono effettivamente statici per più tempo di quanto si prometi che i dati siano statici. |



 



| Impostazioni valide di D3D12 \_ ROOT \_ DESCRIPTOR \_ FLAGS                                                  |  Descrizione                                                                                                                                                                                                                 |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nessun flag impostato                                      | Presupposti predefiniti per i dati: per SRV/CBV: DATA STATIC WHILE SET AT EXECUTE e \_ \_ per \_ \_ \_ UAV: DATA \_ VOLATILE. Queste impostazioni predefinite per SRV/CBV si adattano in modo sicuro ai modelli di utilizzo per la maggior parte delle firme radice. |
| DATI \_ STATICI                                      | I dati sono statici, il potenziale migliore per l'ottimizzazione del driver.                                                                                                                                                       |
| DATI \_ STATICI \_ DURANTE \_ L'ESECUZIONE \_ \_             | I dati sono statici durante l'esecuzione.                                                                                                                                                                              |
| DATA \_ VOLATILE                                    | Equivalente alla firma radice 1.0.                                                                                                                                                                                 |



 

## <a name="version-11-api-summary"></a>Riepilogo dell'API versione 1.1

Le chiamate API seguenti abilitano la versione 1.1.

### <a name="enums"></a>Enumerazioni

Queste enumerazioni contengono i flag di chiave per specificare il descrittore e la volatilità dei dati.

-   [**D3D \_ ROOT \_ SIGNATURE \_ VERSION:**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version) ID versione.
-   [**D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAGS:**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) intervallo di flag che determina se i descrittori o i dati sono volatili o statici.
-   [**D3D12 \_ ROOT \_ DESCRIPTOR \_ FLAGS:**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) un intervallo di flag simile a [**D3D12 \_ DESCRIPTOR \_ RANGE \_ FLAGS,**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags)ad eccezione del fatto che solo i flag di dati si applicano ai descrittori radice.

### <a name="structures"></a>Strutture

Le strutture aggiornate (dalla versione 1.0) contengono riferimenti ai flag di volatilità/statici.

-   [**D3D12 \_ FEATURE \_ DATA \_ ROOT \_ SIGNATURE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature) : passare questa struttura a [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) per verificare il supporto della firma radice versione 1.1.
-   [**D3D12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) può contenere qualsiasi versione di una descrizione della firma radice ed è progettato per essere usato con le funzioni di serializzazione/deserializzazione elencate di seguito.
-   Queste strutture sono equivalenti a quelle usate nella versione 1.0, con l'aggiunta di nuovi campi flag per intervalli di descrittori e descrittori radice:

    -   [**FIRMA RADICE D3D12 \_ \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1)
    -   [**D3D12 \_ DESCRIPTOR \_ RANGE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
    -   [**D3D12 \_ ROOT \_ DESCRIPTOR \_ TABLE1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
    -   [**D3D12 \_ ROOT \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
    -   [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

### <a name="functions"></a>Funzioni

I metodi elencati di seguito sostivano le funzioni [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) e [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) originali, perché sono progettate per funzionare su qualsiasi versione della firma radice. Il formato serializzato è ciò che viene passato all'API [**CreateRootSignature.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) Se uno shader è stato creato con una firma radice, lo shader compilato conterrà già una firma radice serializzata.

-   [**D3D12SerializeVersionedRootSignature:**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) se un'applicazione genera in modo procedurale la struttura dei dati [**D3D12 \_ VERSIONED \_ ROOT \_ SIGNATURE,**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) deve creare il modulo serializzato usando questa funzione.
-   [**D3D12CreateVersionedRootSignatureDeserializer:**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) genera un'interfaccia che può restituire la struttura dei dati deserializzati tramite [**GetUnconvertedRootSignatureDesc.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc)

### <a name="methods"></a>Metodi

[**L'interfaccia ID3D12VersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) viene creata per deserializzare la struttura dei dati della firma radice.

-   [**GetRootSignatureDescAtVersion:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getrootsignaturedescatversion) converte le strutture di descrizione della firma radice in una versione richiesta.
-   [**GetUnconvertedRootSignatureDesc:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc) restituisce un puntatore a una [**struttura DESC D3D12 \_ \_ VERSIONED ROOT \_ SIGNATURE. \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)

### <a name="helper-structures"></a>Strutture helper

Sono state aggiunte strutture helper per facilitare l'inizializzazione di alcune delle strutture della versione 1.1.

-   CD3DX12 \_ DESCRIPTOR \_ RANGE1
-   CD3DX12 \_ ROOT \_ PARAMETER1
-   CD3DX12 \_ STATIC \_ SAMPLER1
-   CD3DX12 \_ VERSIONED \_ ROOT \_ SIGNATURE \_ DESC

Vedere [Helper Structures and Functions for D3D12 (Strutture e funzioni helper per D3D12).](helper-structures-and-functions-for-d3d12.md)

## <a name="consequences-of-violating-static-ness-flags"></a>Conseguenze della violazione dei flag di associazione statica

Il descrittore e i flag di dati descritti in precedenza (nonché i valori predefiniti impliciti nell'assenza di flag specifici) definiscono una promessa da parte dell'applicazione al driver sul comportamento. Se un'applicazione viola la promessa, si tratta di un comportamento non valido: i risultati non sono definiti e potrebbero essere diversi tra driver e hardware diversi.

Il livello di debug include opzioni per convalidare che le applicazioni rispettano le promesse, incluse le promesse predefinite che vengono con la versione 1.1 della firma radice senza impostare alcun flag.

## <a name="version-management"></a>Gestione delle versioni

Quando si compilano firme radice associate agli shader, i compilatori HLSL più recente per impostazione predefinita compilano la firma radice alla versione 1.1, mentre i compilatori HLSL meno recente supportano solo la versione 1.0. Si noti che le firme radice 1.1 non funzioneranno nei sistema operativo che non supportano la firma radice 1.1.

La versione della firma radice compilata con uno shader può essere forzata a una versione specifica usando `/force_rootsig_ver <version>` . L'uso forzato della versione avrà esito positivo se il compilatore è in grado di mantenere il comportamento della firma radice da compilare nella versione forzata, ad esempio eliminando i flag non supportati nella firma radice che servono solo a scopo di ottimizzazione, ma non influiscono sul comportamento.

In questo modo un'applicazione può, ad esempio, compilare una firma radice 1.1 sia nella versione 1.0 che nella versione 1.1 quando si compila l'applicazione e selezionare la versione appropriata in fase di esecuzione a seconda del livello di supporto del sistema operativo. Sarebbe tuttavia più efficiente dello spazio per un'applicazione compilare le firme radice singolarmente (in particolare se sono necessarie più versioni), separatamente dagli shader. Anche se gli shader non vengono compilati inizialmente con una firma radice associata, il vantaggio della convalida della compatibilità della firma radice con uno shader può essere mantenuto usando l'opzione `/verifyrootsignature` del compilatore . In un secondo momento in fase di esecuzione, gli oggetti PSO possono essere creati usando shader che non dispongono di firme radice mentre passano la firma radice desiderata (ad esempio la versione appropriata supportata dal sistema operativo) come parametro separato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una firma radice](creating-a-root-signature.md)
</dt> <dt>

[Firme radice](root-signatures.md)
</dt> <dt>

[Specifica delle firme radice in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 




