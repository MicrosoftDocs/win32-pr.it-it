---
description: Lo strumento CTRPP è un preprocessore che analizza e convalida il manifesto dei contatori.
ms.assetid: 3939f6a1-0a94-429d-a71e-b37f045fea13
title: CTRPP
ms.topic: reference
ms.date: 08/17/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- CTRPP
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8c55e9f3b95d99feabac92574a4be59dacb8ffd7f3b55be07c2bd8fec576da86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033931"
---
# <a name="ctrpp"></a>CTRPP

Lo strumento CTRPP è un preprocessore che analizza e convalida il manifesto per il provider V2. Lo strumento genera risorse con le stringhe necessarie per i consumer del provider e genera un'intestazione con il codice utilizzato per `.rc` fornire i dati del `.h` contatore. È consigliabile eseguire lo strumento CTRPP durante la compilazione del provider. È consigliabile usare il codice generato come punto di partenza quando si sviluppa il provider anziché tentare di generare il codice manualmente.

```syntax
ctrpp -o codeFile -rc rcFile [-legacy] [-MemoryRoutines] [-NotificationCallback] [-prefix prefix] [-ch symFile] [-backcompat] inputFile
```

## <a name="arguments"></a>Argomenti

|Opzione              |Descrizione
|--------------------|-----------
|*inputFile*         |**Obbligatorio:** Specifica il nome del `.man` file (manifesto XML) che definisce i contatori.
|**-o** *codeFile*   |**Obbligatorio:** Specifica il nome del `.h` file di codice che deve essere generato da CTRPP. Questo file conterrà funzioni helper inline C/C++ che semplificano l'inizializzazione e l'annullamento dell'inizializzazione del provider.
|**-rc** *rcFile*    |**Obbligatorio:** Specifica il nome `.rc` dell'oggetto (file di risorse) che deve essere generato da CTRPP. Questo file conterrà la tabella delle stringhe del provider.
|**-ch** *symFile*   |Specifica il nome del file di `.h` simboli facoltativo che deve essere generato da CTRPP. Questo file conterrà simboli C/C++ per i nomi e i GUID di ogni counterset nel provider.
|**Prefisso -prefix** |Specifica il prefisso da utilizzare per le variabili e le funzioni definite nel file di intestazione generato.
|**-NotificationCallback**|Modifica la firma predefinita della funzione [**CounterInitialize**](counterinitialize.md) in modo da includere i parametri per specificare il nome delle funzioni di callback [*ControlCallback,*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)e [*FreeMemory.*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) Questo argomento ha lo stesso effetto dell'inclusione `callback` dell'attributo [**nell'elemento provider.**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element)
|**-migrate** *outputFile*|Invece di generare file e , aggiorna il manifesto inputFile alla versione `.h` più recente e lo salva in `.rc` *outputFile*  . Questa opzione non può essere usata con altre opzioni. Sintassi: `CTRPP -migrate NewFile.man OldFile.man`
|**-BackCompat**     |**Deprecato:** Il supporto per i provider in modalità kernel è stato aggiunto in Windows 7. Per impostazione predefinita, il codice generato da CTRPP per i provider in modalità kernel non sarà compatibile con le versioni precedenti di Windows (il caricamento del driver non riuscirà a causa di `Pcw***` API mancanti). Impostare `-BackCompat` per abilitare la compatibilità con le versioni precedenti di Windows. Il driver carica dinamicamente le API necessarie e il codice generato disabilita automaticamente il provider se le API non sono disponibili.
|**-MemoryRoutines** |**Deprecato:** Se usato con `-Legacy` l'opzione , include i modelli per le routine di memoria nel codice generato. In caso contrario, questo argomento ha lo stesso effetto `-NotificationCallback` dell'opzione .
|**-Legacy**         |**Deprecato:** Genera file , , e usando i modelli di codice `*.h` `*.c` Windows Vista `*.rc` `*_r.h` (genera PerfAutoInitialize e PerfAutoCleanup anziché CounterInitialize e CounterCleanup). Questa opzione può essere usata con **-MemoryRoutines** e **-NotificationCallback,** ma non con altre opzioni. Non usare le **opzioni -o** **o -rc** con questa opzione. I file generati verranno denominati in base al nome del manifesto e verranno scritti nella directory che contiene il manifesto. Sintassi: `CTRPP -legacy OldFile.man`

## <a name="remarks"></a>Commenti

Lo strumento CTRPP genera un `.h` file di codice, un `.rc` file di risorse e facoltativamente genera un `.h` file di simboli.

### <a name="using-the-generated-resource-file"></a>Uso del file di risorse generato

Lo strumento CTRPP genererà un file di risorse che contiene le stringhe localizzabili necessarie per i consumer dei `.rc` counterset del provider.

> [!IMPORTANT]
> Le risorse di questo file devono essere incluse nel file binario del provider e il percorso completo del file binario del provider deve essere registrato durante l'installazione del manifesto del provider. I consumer che non sono in grado di individuare e caricare le risorse non potranno usare i contatori del provider.

Le risorse stringa devono essere gestite nel modo seguente:

- Lo sviluppatore modifica il file manifesto del provider ( ) per impostare l'attributo del provider sul nome di un file binario del `.man` provider (.DLL, .SYS o .EXE) che conterrà le risorse stringa per il provider e verrà installato come parte del `applicationIdentity` componente del provider.
- Lo strumento CTRPP legge il manifesto del provider e genera un `.rc` file.
- Lo [strumento RC (compilatore di risorse)](../menurc/resource-compiler.md) compila i dati dal file generato da CTRPP per generare un `.rc` file contenente le risorse `.res` binarie. Questa operazione può essere eseguita compilando direttamente il file generato da CTRPP oppure compilando un altro file che include il file generato da `.rc` `.rc` CTRPP `.rc` tramite una direttiva `#include` .
- Il linker incorpora i dati del file generato da RC `.res` nel file binario del provider.
- Durante l'installazione, il file binario del provider viene copiato nel sistema dell'utente e il manifesto del provider viene registrato tramite [lo strumento lodctr](/windows-server/administration/windows-commands/lodctr). Lo strumento lodctr converte l'attributo del manifesto del provider in un percorso completo e registra il percorso completo del file binario `applicationIdentity` del provider nel Registro di sistema.
  - Se il file binario del provider si trova nella stessa directory del manifesto, usare: `lodctr.exe /m:"C:\full\manifest\path\manifest.man"` . lodctr combinerà il percorso del manifesto specificato con l'attributo del manifesto `applicationIdentity` per formare il percorso completo.
  - In caso contrario, usare `lodctr.exe /m:"C:\full\manifest\path\manifest.man" "c:\full\binary\path"`. lodctr combinerà il percorso binario specificato con l'attributo del manifesto `applicationIdentity` per formare il percorso completo.
  - A scopo diagnostico, è possibile esaminare il percorso completo registrato controllando il `ApplicationIdentity` valore della chiave del Registro di sistema `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Perflib\_V2Providers\{<ProviderGuid>}` .
  - Se il file binario usa MUI per la localizzazione, assicurarsi di copiare il file MUI insieme al file binario.
- Durante la raccolta di counterset, il consumer usa il percorso completo registrato del file binario del provider per individuare e caricare le stringhe necessarie dalle risorse del file binario del provider.

### <a name="using-the-generated-code-file-in-a-user-mode-provider"></a>Uso del file di codice generato in un provider in modalità utente

Lo strumento CTRPP genererà un `.h` file di codice C/C++. Se l'attributo del manifesto del provider è impostato su , il file di codice generato conterrà le definizioni seguenti utili per codificare un `providerType` `userMode` provider in modalità utente:

- Una funzione di inizializzazione del provider [ * **denominata prefix*CounterInitialize**](counterinitialize.md).
- Una funzione di pulizia del provider [ * **denominata prefix*CounterCleanup**](countercleanup.md).
- Variabile ***provider** _ globale che archivia l'handle del provider aperto dalla funzione _ *_prefix_CounterInitialize** . Il nome della variabile è il valore `symbol` dell'attributo `provider` dell'elemento nel manifesto. Questa variabile deve essere usata nelle chiamate `PerfCreateInstance` a , e altre API per controllare i dati del `PerfDeleteInstance` provider.
- Per ogni insieme di contatori, una variabile globale ***counterset*GUID** con il GUID dell'insieme di contatori. Il nome della variabile è il valore `counterSet` dell'attributo dell'elemento più `symbol` il suffisso "GUID", ad esempio `MyCounterSetGUID` . Questa variabile deve essere usata nelle chiamate `PerfCreateInstance` a , e altre API per controllare i dati del `PerfDeleteInstance` provider.
- Per ogni contatore, una macro ***del*** contatore con il valore del `id` contatore. Il nome della macro è il valore `counter` dell'attributo `symbol` dell'elemento. Questa macro deve essere usata nelle chiamate `PerfSetCounterRefValue` a , e altre API per impostare i dati del `PerfSetULongLongCounterValue` provider.

Nei nomi delle funzioni il ***prefisso*** fa riferimento al valore del parametro `-prefix` della riga di comando. Se il `-prefix` parametro non viene usato, le funzioni verranno denominate `CounterInitialize` e `CounterCleanup` .

### <a name="using-the-generated-code-file-in-a-kernel-mode-provider"></a>Uso del file di codice generato in un provider in modalità kernel

Lo strumento CTRPP genererà un `.h` file di codice C/C++. Se l'attributo del manifesto del provider è impostato su , il file di codice generato conterrà le definizioni seguenti utili per codificare i contatori di un provider in modalità `providerType` `kernelMode` kernel:

- Funzione di inizializzazione counterset denominata <b> *prefisso* Register *Counterset*</b>. Questa funzione compila una struttura [RegInfo](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) e quindi richiama [PcwRegister,](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwregister)inserendo l'handle di registrazione del contatore risultante nella variabile ***Counterset*** globale.
- Una funzione di pulizia dell'insieme di contatori <b> *denominata prefix* Unregister *Counterset*</b>. Questa funzione richiama [PcwUnregister sull'handle](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwunregister) di registrazione del contatore nella variabile ***Counterset*** globale.
- Una funzione di creazione dell'istanza <b> *denominata prefisso* Create *Counterset*</b>. Questa funzione riempie una matrice di [strutture PcwData](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) e quindi richiama [PcwCreateInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcreateinstance) usando l'handle di registrazione del contatore nella variabile ***Counterset*** globale.
- Una funzione di pulizia dell'istanza <b> *denominata prefisso* Close *Counterset*</b>. Questa funzione richiama [PcwCloseInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcloseinstance).
- Funzione di creazione report dell'istanza <b> *denominata prefisso* Add *Counterset*</b> da usare dalla funzione di callback counterset. Questa funzione riempie una matrice di [strutture PcwData](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) e quindi richiama [PcwAddInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwaddinstance).
- **Windows SDK 20H1 e versioni successive:** Funzione di inizializzazione RegInfo denominata <b> *prefisso* InitRegistrationInformation *Counterset*</b> da usare in scenari avanzati. Questa funzione riempie una [struttura RegInfo.](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) Questa funzione può essere usata nei casi in cui il prefisso generato <b> Register *Counterset*</b> non soddisfa le proprie esigenze, ad esempio quando si vogliono personalizzare i valori nella struttura RegInfo o quando si vuole archiviare l'handle restituito in un'altra variabile.

Nei nomi delle funzioni il ***prefisso*** fa riferimento al valore del parametro `-prefix` della riga di comando. Se il `-prefix` parametro non viene usato, le funzioni non avranno alcun prefisso.

> [!NOTE]
> La funzione <b> *Add**Counterset*</b> del prefisso generato viene usata quando si dispone di un callback di counterset. Le funzioni <b> *create**counterset e*</b> <b> *close**counterset*</b> generate vengono usate quando non è disponibile un callback di counterset.

### <a name="using-the-generated-symbol-file"></a>Uso del file di simboli generato

Se il **parametro -ch** viene specificato nella riga di comando, lo strumento CTRPP genererà un `.h` file di simboli. Questo file contiene i simboli C/C++ per i nomi e i GUID di ogni counterset nel provider. I simboli possono essere usati durante la scrittura di programmi hard-coded per l'utilizzo dei dati di questo counterset usando le funzioni [consumer PerfLib V2](using-the-perflib-functions-to-consume-counter-data.md).

## <a name="requirements"></a>Requisiti

| Requisito             | Valore |
|-------------------------|-------|
| Client minimo supportato| Windows Solo \[ app desktop Vista\]
| Server minimo supportato| Windows Solo app desktop di Server 2008 \[\]
