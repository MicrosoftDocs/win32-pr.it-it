---
title: Firma radice versione 1,1
description: Lo scopo della firma radice versione 1,1 è quello di consentire alle applicazioni di indicare ai driver quando i descrittori in un heap descrittore non cambiano o i descrittori di dati che puntano a non cambiano.
ms.assetid: 8FE42C1C-7F1D-4E70-A7EE-D5EC67237327
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d0a107b4186f164e60a6225f55c5ba3f4f06b2
ms.sourcegitcommit: f5a319899176e2df564bdb4d9eaffc32140452a2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2020
ms.locfileid: "104548852"
---
# <a name="root-signature-version-11"></a>Firma radice versione 1,1

Lo scopo della firma radice versione 1,1 è quello di consentire alle applicazioni di indicare ai driver quando i descrittori in un heap descrittore non cambiano o i descrittori di dati che puntano a non cambiano. Ciò consente all'opzione per i driver di eseguire ottimizzazioni che potrebbero essere possibili sapendo che un descrittore o la memoria a cui fa riferimento è statico per un determinato periodo di tempo.

-   [Overview](#overview)
-   [Flag statici e volatili](#static-and-volatile-flags)
    -   [descrittori \_ volatili](#descriptors_volatile)
    -   [DATI \_ volatili](#data_volatile)
    -   [DATI \_ statici \_ durante il \_ set \_ in fase di \_ esecuzione](#data_static_while_set_at_execute)
    -   [DATI \_ statici](#data_static)
    -   [Combinazione di flag](#combining-flags)
    -   [Riepilogo flag](#flag-summary)
-   [Riepilogo API versione 1,1](#version-11-api-summary)
    -   [Enumerazioni](#enums)
    -   [Strutture](#helper-structures)
    -   [Funzioni](#functions)
    -   [Metodi](#methods)
    -   [Strutture Helper](#helper-structures)
-   [Conseguenze della violazione dei flag di nesso statico](#consequences-of-violating-static-ness-flags)
-   [Gestione delle versioni](#version-management)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

La firma radice versione 1,0 consente il contenuto degli heap dei descrittori e la memoria a cui puntano per essere liberamente modificati dalle applicazioni ogni volta che gli elenchi di comandi/bundle che vi fanno riferimento sono potenzialmente in fase di volo sulla GPU. Molto spesso, tuttavia, le applicazioni non necessitano effettivamente della flessibilità necessaria per modificare i descrittori o la memoria dopo la registrazione dei comandi che vi fanno riferimento.

Spesso le applicazioni sono in grado di:

-   Impostare i descrittori (e la memoria a cui puntano) prima di associare le tabelle dei descrittori o i descrittori radice in un elenco di comandi o in un bundle.
-   Assicurarsi che questi descrittori non cambino fino a quando l'elenco di comandi/Bundles che vi fa riferimento non hanno terminato l'esecuzione per l'ultima volta.
-   Assicurarsi che i dati a cui puntano i descrittori non cambino per la stessa durata completa.

In alternativa, un'applicazione può solo essere in grado di rispettare i dati che non cambiano per un periodo di tempo più breve. In particolare, i dati potrebbero essere statici per la finestra nel tempo durante l'esecuzione dell'elenco di comandi, che attualmente puntano ai dati in un'associazione di parametri radice (tabella descrittore o descrittore radice). In altre parole, un'applicazione può voler eseguire l'esecuzione sulla sequenza temporale GPU che aggiorna alcuni dati tra i periodi di tempo in cui viene impostata tramite un parametro radice, sapendo che quando viene impostata, sarà statica.

Se i descrittori o i descrittori di dati puntano a, non cambieranno, quindi i driver specifici per le ottimizzazioni potrebbero essere specifici del fornitore dell'hardware e, di fatto, non modificano il comportamento ad eccezione del miglioramento delle prestazioni. Il mantenimento di tutte le informazioni sulle finalità dell'applicazione possibili non comporta un sovraccarico sulle applicazioni.

Una ottimizzazione è che molti driver possono produrre accessi di memoria più efficienti da shader se conoscono le promesse che un'applicazione può apportare sulla staticità dei descrittori e dei dati. I driver, ad esempio, potrebbero rimuovere un livello di riferimento indiretto per l'accesso a un descrittore in un heap convertendo questo oggetto in un descrittore radice se l'hardware specifico non è sensibile alle dimensioni dell'argomento radice.

L'attività aggiuntiva per gli sviluppatori che usano la versione 1,1 consiste nel creare promesse sulla volatilità e sul nesso statico dei dati laddove possibile, in modo che i driver possano apportare le ottimizzazioni che hanno senso. Gli sviluppatori non devono effettuare alcuna promesse sul nesso statico.

La firma radice versione 1,0 continua a funzionare senza modifiche, anche se le applicazioni che ricompilano firme radice utilizzeranno per impostazione predefinita la firma radice 1,1 ora (con un'opzione per forzare la versione 1,0, se necessario).

## <a name="static-and-volatile-flags"></a>Flag statici e volatili

I flag seguenti fanno parte della firma radice per consentire ai driver di scegliere una strategia per gestire al meglio gli argomenti radice singoli quando sono impostati e incorporare le stesse ipotesi negli oggetti di stato della pipeline (PSO) quando vengono compilati in origine, perché la firma radice fa parte di un oggetto PSO.

I flag seguenti sono impostati dall'app e si applicano ai descrittori o ai dati.

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

### <a name="descriptors_volatile"></a>descrittori \_ volatili

Con questo flag impostato, i descrittori in un heap descrittore a cui punta una tabella del descrittore radice possono essere modificati dall'applicazione in qualsiasi momento tranne quando l'elenco dei comandi o i bundle che associano la tabella descrittore sono stati inviati e l'esecuzione non è terminata. È ad esempio possibile registrare un elenco di comandi e successivamente modificare i descrittori in un heap del descrittore a cui fa riferimento *prima* di inviare l'elenco di comandi per l'esecuzione è valido. Si tratta dell'unico comportamento supportato della firma radice versione 1,0.

Se il flag volatile descrittori \_ *non* è impostato, i descrittori sono statici. Nessun flag per questa modalità. I descrittori statici indicano che i descrittori in un heap del descrittore a cui punta una tabella del descrittore radice sono stati inizializzati nel momento in cui la tabella descrittore è impostata su un elenco di comandi/Bundle (durante la registrazione) e i descrittori non possono essere modificati fino al completamento dell'esecuzione dell'elenco dei comandi o del bundle. *Per la firma radice versione 1,1, i descrittori statici rappresentano il presupposto predefinito* e l'applicazione deve specificare il flag volatile descrittori \_ quando necessario.

Per i bundle che usano tabelle descrittore con descrittori statici, i descrittori devono essere pronti a partire dal momento in cui viene registrato il bundle (in contrapposizione al momento in cui viene chiamato il bundle) e non cambiano fino a quando l'esecuzione del bundle non è terminata per l'ultima volta. Le tabelle dei descrittori che puntano a descrittori statici devono essere impostate durante la registrazione del bundle e non ereditate nel bundle. È valido per un elenco di comandi usare una tabella descrittore con descrittori statici impostati in un bundle e restituiti all'elenco dei comandi.

Quando i descrittori sono statici, esiste un'altra modifica del comportamento che richiede l'impostazione del flag volatile dei descrittori \_ . Al di fuori dei limiti gli accessi alle viste del buffer (a differenza delle viste Texture1D/2D/3D/Cube) non sono validi e producono risultati non definiti, inclusa la possibile reimpostazione del dispositivo, anziché restituire i valori predefiniti per le operazioni di lettura o eliminazione delle Scritture. Lo scopo di rimuovere la possibilità per le applicazioni di dipendere dal controllo dell'accesso all'hardware al di fuori dei limiti consiste nel consentire ai driver di scegliere di innalzare di livello gli accessi descrittori statici agli accessi descrittori radice se ritengono che risulti più efficiente. I descrittori radice non supportano il controllo fuori limite.

Se le applicazioni dipendono dal comportamento di accesso alla memoria al di fuori del limite durante l'accesso ai descrittori, è necessario contrassegnare gli intervalli di descrittori che accedono a tali descrittori come descrittori \_ volatili.

### <a name="data_volatile"></a>DATI \_ volatili

Con questo flag impostato, i dati a cui puntano i descrittori possono essere modificati dalla CPU in qualsiasi momento, tranne nel caso in cui l'elenco dei comandi o i bundle che associano la tabella dei descrittori siano stati inviati e non siano stati completati. Si tratta dell'unico comportamento supportato della firma radice versione 1,0.

Il flag è disponibile sia nei flag di intervallo dei descrittori che nei flag del descrittore radice.

### <a name="data_static_while_set_at_execute"></a>DATI \_ statici \_ durante il \_ set \_ in fase di \_ esecuzione

Se questo flag è impostato, i dati a cui fanno riferimento i descrittori non possono essere modificati a partire da quando il descrittore radice sottostante o la tabella descrittore viene impostata in un elenco di comandi o in un bundle durante l'esecuzione sulla sequenza temporale della GPU e termina quando i dati di disegno/invio successivi non faranno più riferimento ai dati.

Prima che sia stato impostato un descrittore radice o una tabella descrittore sulla GPU, questi dati *possono* essere modificati anche dallo stesso elenco di comandi/bundle. I dati possono anche essere modificati mentre un descrittore radice o una tabella del descrittore che lo puntano è ancora impostato sull'elenco dei comandi o sul bundle, purché il progetto o le recapito siano stati completati. In questo modo, tuttavia, è necessario riassociare la tabella del descrittore all'elenco di comandi prima della successiva dereferenziazione del descrittore radice o della tabella descrittore. In questo modo, il driver sa che i dati a cui punta un descrittore radice o una tabella descrittore sono stati modificati.

La differenza essenziale tra i dati \_ statici \_ durante l' \_ \_ \_ esecuzione e i dati \_ volatili è con dati \_ volatili. un driver non è in grado di stabilire se le copie dei dati in un elenco di comandi hanno modificato i dati a cui punta un descrittore, senza eseguire un rilevamento dello stato aggiuntivo. Quindi, se, ad esempio, un driver può inserire qualsiasi tipo di comando di recupero preliminare dei dati nel proprio elenco di comandi (per rendere più efficiente l'accesso allo shader ai dati noti, ad esempio), \_ i dati statici \_ durante l' \_ \_ \_ esecuzione consentono al driver di capire che è necessario eseguire il recupero dei dati solo nel momento in cui viene impostato tramite [**SetGraphicsRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable), [**SetComputeRootDescriptorTable**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable) o uno dei metodi per impostare la visualizzazione del buffer costante, la visualizzazione delle risorse dello shader o la visualizzazione di accesso non ordinato.

Per i bundle, il suggerimento che i dati sono statici durante l'esecuzione viene applicato in modo univoco a ogni esecuzione del bundle.

Il flag è disponibile sia nei flag di intervallo dei descrittori che nei flag del descrittore radice.

### <a name="data_static"></a>DATI \_ statici

Se questo flag è impostato, i dati a cui puntano i descrittori sono stati inizializzati dal momento in cui è stato impostato un descrittore radice o una tabella descrittore che fa riferimento alla memoria in un elenco di comandi/bundle durante la registrazione e i dati non possono essere modificati fino al completamento dell'esecuzione dell'elenco dei comandi o del bundle per l'ultima volta.

Per i bundle, la durata statica inizia in corrispondenza del descrittore radice o dell'impostazione della tabella del descrittore durante la registrazione del bundle, anziché registrare un elenco di comandi chiamante. Inoltre, una tabella descrittore che punta ai dati statici deve essere impostata nel bundle e non ereditata. È valido per un elenco di comandi usare una tabella del descrittore che punta a dati statici impostati in un bundle e restituiti all'elenco dei comandi.

Il flag è disponibile sia nei flag di intervallo dei descrittori che nei flag del descrittore radice.

### <a name="combining-flags"></a>Combinazione di flag

È possibile specificare al massimo uno dei flag di dati alla volta, ad eccezione degli intervalli descrittori del campionatore che non supportano i flag di dati perché i sampler non puntano ai dati.

L'assenza di flag di dati per gli intervalli di descrittori SRV e CBV indica il presupposto di un valore predefinito di dati \_ statici \_ durante l'impostazione del \_ comportamento di \_ \_ esecuzione. Il motivo per cui viene scelta questa impostazione predefinita anziché i dati \_ statici è che i dati \_ statici \_ durante l' \_ \_ \_ esecuzione sono molto più probabilmente un valore predefinito sicuro per la maggior parte dei casi, garantendo allo stesso tempo un'opportunità di ottimizzazione migliore rispetto all'impostazione predefinita per i dati \_ volatili.

L'assenza di flag di dati per gli intervalli di descrittori UAV indica \_ che viene presupposto un comportamento predefinito dei dati volatili, dato che in genere vengono scritti UAV.

I descrittori \_ volatili *non possono* essere combinati con \_ i dati statici, ma *possono* essere combinati con gli altri flag di dati. Il motivo per cui i descrittori \_ volatili possono essere combinati con i dati \_ statici \_ mentre \_ \_ è impostato in fase di esecuzione è che i descrittori \_ volatili richiedono che i descrittori siano pronti durante l'esecuzione dell'elenco dei comandi o del bundle e che i dati \_ statici durante l'esecuzione \_ \_ \_ \_ siano solo le promesse per l'esecuzione statica all'interno di un subset dell'esecuzione dell'elenco dei comandi/bundle

### <a name="flag-summary"></a>Riepilogo flag

Nelle tabelle seguenti vengono riepilogate le combinazioni di flag che potrebbero essere utilizzate.



|                                                                |                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Impostazioni valide per i \_ flag di intervallo del descrittore D3D12 \_ \_**             | **Descrizione**                                                                                                                                                                                                                                                                                                                                      |
| Nessun flag impostato                                                   | I descrittori sono statici (impostazione predefinita). Presupposti predefiniti per i dati: per SRV/CBV: dati \_ statici \_ durante il \_ set \_ in fase di \_ esecuzione e per UAV: dati \_ volatili. Queste impostazioni predefinite per SRV/CBV si adatteranno in modo sicuro ai modelli di utilizzo per la maggior parte delle firme radice.                                                                                              |
| DATI \_ statici                                                   | I descrittori e i dati sono statici. Questa operazione massimizza il rischio di ottimizzazione del driver.                                                                                                                                                                                                                                                          |
| DATI \_ volatili                                                 | I descrittori sono statici e i dati sono volatili.                                                                                                                                                                                                                                                                                                     |
| DATI \_ statici \_ durante il \_ set \_ in fase di \_ esecuzione                          | I descrittori sono statici e i dati sono statici mentre vengono impostati in fase di esecuzione.                                                                                                                                                                                                                                                                                      |
| descrittori \_ volatili                                          | I descrittori sono volatili e i presupposti predefiniti vengono creati sui dati: per SRV/CBV: dati \_ statici \_ durante l' \_ \_ \_ esecuzione e per UAV: dati \_ volatili.                                                                                                                                                                                              |
| descrittori \_ \| dati volatili \_ volatili                        | I descrittori e i dati sono volatili, equivalenti alla firma radice 1,0.                                                                                                                                                                                                                                                                            |
| descrittori \_ \| dati volatili \_ statici \_ durante il \_ set \_ in fase di \_ esecuzione | I descrittori sono volatili, ma si noti che non è ancora possibile modificarli durante l'esecuzione dell'elenco dei comandi. Pertanto, è possibile combinare la dichiarazione aggiuntiva che i dati sono statici durante l'impostazione tramite la tabella del descrittore radice durante l'esecuzione. i descrittori sottostanti sono effettivamente statici per un periodo più lungo rispetto alla promessa che i dati sono statici. |



 



|                                                   |                                                                                                                                                                                                                   |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Impostazioni valide per i \_ \_ flag del descrittore radice D3D12 \_** | **Descrizione**                                                                                                                                                                                                   |
| Nessun flag impostato                                      | Presupposti predefiniti per i dati: per SRV/CBV: dati \_ statici \_ durante il \_ set \_ in fase di \_ esecuzione e per UAV: dati \_ volatili. Queste impostazioni predefinite per SRV/CBV si adatteranno in modo sicuro ai modelli di utilizzo per la maggior parte delle firme radice. |
| DATI \_ statici                                      | I dati sono statici, il miglior potenziale per l'ottimizzazione del driver.                                                                                                                                                       |
| DATI \_ statici \_ durante il \_ set \_ in fase di \_ esecuzione             | I dati sono statici mentre vengono impostati in fase di esecuzione.                                                                                                                                                                              |
| DATI \_ volatili                                    | Equivalente alla firma radice 1,0.                                                                                                                                                                                 |



 

## <a name="version-11-api-summary"></a>Riepilogo API versione 1,1

Le chiamate API seguenti consentono di abilitare la versione 1,1.

### <a name="enums"></a>Enumerazioni

Queste enumerazioni contengono i flag chiave per specificare il descrittore e la volatilità dei dati.

-   [**D3D \_ \_ \_ Versione della firma radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version) : ID versione.
-   [**D3D12 \_ \_ \_ Flag di intervallo descrittori**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags) : intervallo di flag che determina se i descrittori o i dati sono volatili o statici.
-   [**D3D12 \_ \_ \_ Flag di descrittore radice**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) : un intervallo simile di flag ai [**\_ \_ \_ flag di intervallo descrittore D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags), con la differenza che solo i flag di dati si applicano ai descrittori radice

### <a name="structures"></a>Strutture

Le strutture aggiornate (dalla versione 1,0) contengono riferimenti ai flag di volatilità/static.

-   [**D3D12 \_ \_ \_ \_ Firma radice dati funzionalità**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_root_signature) : passare questa struttura a [**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) per verificare il supporto della firma radice versione 1,1.
-   [**D3D12 \_ VERSIONE della \_ \_ firma radice \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) : può contenere qualsiasi versione di una descrizione della firma radice ed è progettata per essere usata con le funzioni di serializzazione/deserializzazione elencate di seguito.
-   Queste strutture sono equivalenti a quelle usate nella versione 1,0, con l'aggiunta di nuovi campi dei flag per gli intervalli di descrittori e i descrittori radice:

    -   [**\_Firma radice \_ D3D12 \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1)
    -   [**\_Descrittore D3D12 \_ nell'intervallo 1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1)
    -   [**\_Descrittore radice D3D12 \_ \_ Tabella1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor_table1)
    -   [**\_DESCRIPTOR1 radice \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
    -   [**\_Parametro1 radice \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)

### <a name="functions"></a>Funzioni

I metodi elencati di seguito sostituiscono le funzioni [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) e [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) originali, perché sono progettate per funzionare con qualsiasi versione della firma radice. Il formato serializzato è quello passato nell'API [**CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature) . Se uno shader è stato creato con una firma radice, lo shader compilato conterrà già una firma radice serializzata.

-   [**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) : se un'applicazione genera in modo procedurale la struttura dei dati della [**\_ \_ \_ firma radice con versione D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) , deve creare il form serializzato usando questa funzione.
-   [**D3D12CreateVersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) : genera un'interfaccia che può restituire la struttura dei dati deserializzata tramite [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc).

### <a name="methods"></a>Metodi

L'interfaccia [**ID3D12VersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) viene creata per deserializzare la struttura dei dati della firma radice.

-   [**GetRootSignatureDescAtVersion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getrootsignaturedescatversion) : converte le strutture della descrizione della firma radice in una versione richiesta.
-   [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc) : restituisce un puntatore a una [**struttura \_ \_ \_ \_ desc della firma radice con versione D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) .

### <a name="helper-structures"></a>Strutture Helper

Sono state aggiunte strutture helper per facilitare l'inizializzazione di alcune delle strutture della versione 1,1.

-   \_Descrittore CD3DX12 \_ nell'intervallo 1
-   \_Parametro1 radice \_ CD3DX12
-   \_SAMPLER1 statico \_ CD3DX12
-   \_ \_ Descrizione della firma radice \_ con versione CD3DX12 \_

Vedere [le strutture e le funzioni di supporto per D3D12](helper-structures-and-functions-for-d3d12.md).

## <a name="consequences-of-violating-static-ness-flags"></a>Conseguenze della violazione dei flag di nesso statico

Il descrittore e i flag di dati descritti in precedenza, nonché i valori predefiniti impliciti in assenza di flag particolari, definiscono una promessa da parte dell'applicazione al driver sulla relativa modalità di comportamento. Se un'applicazione viola il suggerimento, questo comportamento non è valido: i risultati non sono definiti e potrebbero essere diversi tra driver e hardware diversi.

Il livello di debug include opzioni per la convalida delle promesse rispettate dalle applicazioni, incluse le promesse predefinite disponibili con l'uso della firma radice versione 1,1 senza impostare alcun flag.

## <a name="version-management"></a>Gestione delle versioni

Quando si compilano le firme radice collegate agli shader, per impostazione predefinita i compilatori HLSL più recenti compilano la firma radice alla versione 1,1, mentre i compilatori HLSL precedenti supportano solo 1,0. Si noti che 1,1 firme radice non funzioneranno in sistemi operativi che non supportano la firma radice 1,1.

La versione della firma radice compilata con uno shader può essere forzata a una determinata versione utilizzando `/force_rootsig_ver <version>` . La forzatura della versione avrà esito positivo se il compilatore è in grado di mantenere il comportamento della firma radice compilata nella versione forzata, ad esempio eliminando flag non supportati nella firma radice che servono solo a scopo di ottimizzazione, ma non influiscono sul comportamento.

In questo modo un'applicazione può, ad esempio, compilare una firma radice 1,1 in 1,0 e 1,1 durante la compilazione dell'applicazione e selezionare la versione appropriata in fase di esecuzione a seconda del livello di supporto del sistema operativo. Per la compilazione di firme radice singolarmente (in particolare se sono necessarie più versioni), tuttavia, la maggior parte dello spazio è efficiente, separatamente dagli shader. Anche se gli shader non vengono inizialmente compilati con una firma radice collegata, il vantaggio della convalida del compilatore della compatibilità della firma radice con uno shader può essere mantenuto usando l' `/verifyrootsignature` opzione del compilatore. In un secondo momento in fase di esecuzione, è possibile creare PSO usando gli shader che non dispongono di firme radice, passando la firma radice desiderata (probabilmente la versione appropriata supportata dal sistema operativo) come parametro separato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una firma radice](creating-a-root-signature.md)
</dt> <dt>

[Firme radice](root-signatures.md)
</dt> <dt>

[Specifica delle firme radice in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 




