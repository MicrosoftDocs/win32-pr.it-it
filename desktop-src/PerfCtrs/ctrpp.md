---
description: Lo strumento CTRPP è un pre-processore che analizza e convalida il manifesto dei contatori.
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
ms.openlocfilehash: dce12de641dda7b07871a4447190772533598748
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351856"
---
# <a name="ctrpp"></a>CTRPP

Lo strumento CTRPP è un pre-processore che analizza e convalida il manifesto per il provider v2. Lo strumento genera `.rc` risorse con le stringhe richieste dagli utenti del provider e genera un' `.h` intestazione con il codice usato per fornire i dati del contatore. Eseguire lo strumento CTRPP durante la compilazione del provider. È consigliabile usare il codice generato come punto di partenza quando si sviluppa il provider anziché provare a generare manualmente questo codice.

```syntax
ctrpp -o codeFile -rc rcFile [-legacy] [-MemoryRoutines] [-NotificationCallback] [-prefix prefix] [-ch symFile] [-backcompat] inputFile
```

## <a name="arguments"></a>Argomenti

|Opzione              |Descrizione
|--------------------|-----------
|*inputFile*         |**Obbligatorio:** Specifica il nome del `.man` file (manifesto XML) che definisce i contatori.
|**-o** *CodeFile*   |**Obbligatorio:** Specifica il nome del `.h` file di codice che deve essere generato da CTRPP. Questo file conterrà le funzioni di supporto inline C/C++ che semplificano l'inizializzazione e l'annullamento dell'inizializzazione del provider.
|**-RC** *rcFile*    |**Obbligatorio:** Specifica il nome del `.rc` file di risorse che deve essere generato da CTRPP. Questo file conterrà la tabella delle stringhe del provider.
|**-ch** *symFile*   |Specifica il nome del file di `.h` simboli facoltativo che deve essere generato da CTRPP. Questo file conterrà i simboli C/C++ per i nomi e i GUID di ogni contatore del provider.
|**-** *prefisso prefisso*|Specifica il prefisso da usare per le variabili e le funzioni definite nel file di intestazione generato.
|**-NotificationCallback**|Modifica la firma predefinita della funzione [**CounterInitialize**](counterinitialize.md) in modo da includere i parametri per specificare il nome delle funzioni di callback [*ControlCallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest), [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc)e [*freememory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) . Questo argomento ha lo stesso effetto dell'inclusione dell' `callback` attributo nell'elemento [**provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) .
|**-Esegui migrazione di** *outputfile*|Anziché generare `.h` file e `.rc` , aggiorna il manifesto *inputfile* alla versione più recente e lo salva in *outputfile*. Questa opzione non può essere usata con altre opzioni. Sintassi: `CTRPP -migrate NewFile.man OldFile.man`
|**-BackCompat**     |**Deprecato:** Il supporto per i provider in modalità kernel è stato aggiunto in Windows 7. Per impostazione predefinita, il codice generato da CTRPP per i provider in modalità kernel non sarà compatibile con le versioni precedenti di Windows (il driver non verrà caricato a causa di `Pcw***` API mancanti). Impostare `-BackCompat` per abilitare la compatibilità con le versioni precedenti di Windows. Il driver caricherà in modo dinamico le API necessarie e il codice generato Disabilita automaticamente il provider se le API non sono disponibili.
|**-MemoryRoutines** |**Deprecato:** Se usato con l' `-Legacy` opzione, include i modelli per le routine di memoria nel codice generato. In caso contrario, questo argomento avrà lo stesso effetto dell' `-NotificationCallback` opzione.
|**-Legacy**         |**Deprecato:** Genera `*.h` `*.c` `*.rc` i file,, e `*_r.h` utilizzando i modelli di codice di Windows Vista (genera PerfAutoInitialize e PerfAutoCleanup anziché CounterInitialize e CounterCleanup). Questa opzione può essere usata con **-MemoryRoutines** e **-NotificationCallback** ma non può essere usata con altre opzioni. Non usare le opzioni **-o** o **-RC** con questa opzione. I file generati verranno denominati in base al nome del manifesto e verranno scritti nella directory che contiene il manifesto. Sintassi: `CTRPP -legacy OldFile.man`

## <a name="remarks"></a>Commenti

Lo strumento CTRPP genera un file di `.h` codice, un `.rc` file di risorse e, facoltativamente, genera un `.h` file di simboli.

### <a name="using-the-generated-resource-file"></a>Uso del file di risorse generato

Lo strumento CTRPP genererà un `.rc` file di risorse che contiene le stringhe localizzabili necessarie per i consumer del CounterSet del provider.

> [!IMPORTANT]
> Le risorse di questo file devono essere incluse nel file binario del provider e il percorso completo del file binario del provider deve essere registrato durante l'installazione del manifesto del provider. I consumer che non sono in grado di individuare e caricare le risorse non saranno in grado di usare il CounterSet del provider.

Le risorse di stringa devono essere gestite come segue:

- Lo sviluppatore modifica il file del manifesto del provider ( `.man` ) per impostare l' `applicationIdentity` attributo del provider sul nome di un provider binario (. DLL,. SYS o. EXE) che conterrà le risorse di stringa per il provider e verrà installato come parte del componente provider.
- Lo strumento CTRPP legge il manifesto del provider e genera un `.rc` file.
- Lo strumento [RC (compilatore di risorse)](../menurc/resource-compiler.md) compila i dati dal file generato da CTRPP `.rc` per generare un `.res` file contenente le risorse binarie. Questa operazione può essere eseguita compilando direttamente il file generato da CTRPP `.rc` o compilando un altro `.rc` file che include il file generato da CTRPP `.rc` tramite una `#include` direttiva.
- Il linker incorpora i dati dal file generato da RC `.res` nel file binario del provider.
- Durante l'installazione, il file binario del provider viene copiato nel sistema dell'utente e il manifesto del provider viene registrato utilizzando lo [strumento lodctr](/windows-server/administration/windows-commands/lodctr). Lo strumento lodctr converte l' `applicationIdentity` attributo del manifesto del provider in un percorso completo e registra il percorso completo del file binario del provider nel registro di sistema.
  - Se il file binario del provider si trova nella stessa directory del manifesto, usare: `lodctr.exe /m:"C:\full\manifest\path\manifest.man"` . lodctr combinerà il percorso del manifesto specificato con l'attributo del manifesto `applicationIdentity` per formare il percorso completo.
  - In caso contrario, usare `lodctr.exe /m:"C:\full\manifest\path\manifest.man" "c:\full\binary\path"`. lodctr combinerà il percorso binario specificato con l'attributo del manifesto `applicationIdentity` per formare il percorso completo.
  - Ai fini della diagnostica, è possibile controllare il percorso completo registrato controllando il `ApplicationIdentity` valore della chiave del registro di sistema `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Perflib\_V2Providers\{<ProviderGuid>}` .
  - Se il file binario USA MUI per la localizzazione, assicurarsi di copiare il file MUI insieme al file binario.
- Durante la raccolta dei contatori, il consumer usa il percorso completo registrato al file binario del provider per individuare e caricare le stringhe necessarie dalle risorse del binario del provider.

### <a name="using-the-generated-code-file-in-a-user-mode-provider"></a>Uso del file di codice generato in un provider in modalità utente

Lo strumento CTRPP genererà un `.h` file di codice C/C++. Se l'attributo del manifesto del provider `providerType` è impostato su `userMode` , il file di codice generato conterrà le seguenti definizioni utili per la codifica di un provider in modalità utente:

- Funzione di inizializzazione del provider denominata [ * **Prefix * CounterInitialize**](counterinitialize.md).
- Funzione di pulizia del provider denominata [ * **Prefix * CounterCleanup**](countercleanup.md).
- Variabile globale ***provider** _ che archivia l'handle del provider aperto dalla funzione _ *_prefix_CounterInitialize**. Il nome della variabile è il valore dell' `symbol` attributo dell' `provider` elemento nel manifesto. Questa variabile deve essere usata nelle chiamate a `PerfCreateInstance` , `PerfDeleteInstance` e ad altre API per il controllo dei dati del provider.
- Per ogni contatore, una variabile di **GUID** * del contatore * globale con il GUID del contatore. Il nome della variabile è il valore dell' `counterSet` attributo dell'elemento `symbol` più il suffisso "GUID", ad esempio `MyCounterSetGUID` . Questa variabile deve essere usata nelle chiamate a `PerfCreateInstance` , `PerfDeleteInstance` e ad altre API per il controllo dei dati del provider.
- Per ogni contatore, una macro del ***contatore*** con il valore del contatore `id` . Il nome della macro corrisponde al valore dell' `counter` attributo dell'elemento `symbol` . Questa macro deve essere usata nelle chiamate a `PerfSetCounterRefValue` , `PerfSetULongLongCounterValue` e ad altre API per l'impostazione dei dati del provider.

Nei nomi di funzione, ***Prefix*** si riferisce al valore del `-prefix` parametro della riga di comando. Se il `-prefix` parametro non viene utilizzato, le funzioni verranno denominate `CounterInitialize` e `CounterCleanup` .

### <a name="using-the-generated-code-file-in-a-kernel-mode-provider"></a>Uso del file di codice generato in un provider in modalità kernel

Lo strumento CTRPP genererà un `.h` file di codice C/C++. Se l'attributo del manifesto del provider `providerType` è impostato su `kernelMode` , il file di codice generato conterrà le seguenti definizioni utili per la codifica di un CounterSet del provider in modalità kernel:

- Una funzione di inizializzazione del contatore denominata <b> *PREFIXE* registra il *contatore*</b>. Questa funzione compila una struttura [RegInfo](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) , quindi richiama [PcwRegister](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwregister), inserendo l'handle di registrazione del contatore risultante nella variabile globale del ***contatore*** .
- Una funzione di pulizia dei contatori denominata <b> *Prefix* Annulla la registrazione del *contatore*</b>. Questa funzione richiama [PcwUnregister](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwunregister) sull'handle di registrazione del contatore dei contatori nella variabile globale del ***contatore*** .
- Una funzione di creazione dell'istanza denominata <b> *Prefix* crea il *contatore*</b>. Questa funzione compila una matrice di strutture [PcwData](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) , quindi richiama [PcwCreateInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcreateinstance) usando l'handle di registrazione del contatore nella variabile globale del ***contatore*** .
- Una funzione di pulizia dell'istanza denominata <b> *Prefix* chiude il *contatore*</b>. Questa funzione richiama [PcwCloseInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwcloseinstance).
- Una funzione di creazione di report dell'istanza denominata <b> *Prefix* aggiungere il *contatore*</b> da usare dalla funzione di callback del contatore. Questa funzione compila una matrice di strutture [PcwData](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_data) , quindi richiama [PcwAddInstance](/windows-hardware/drivers/ddi/wdm/nf-wdm-pcwaddinstance).
- **Windows SDK 20H1 e versioni successive:** Funzione di inizializzazione RegInfo denominata <b> *Prefix* InitRegistrationInformation</b> per l'uso in scenari avanzati. Questa funzione compila una struttura [RegInfo](/windows-hardware/drivers/ddi/wdm/ns-wdm-_pcw_registration_information) . Questa funzione può essere usata nei casi in cui il <b>*contatore* dei registri di *prefisso*</b> generato non soddisfi le proprie esigenze, ad esempio quando si vuole personalizzare i valori nella struttura RegInfo o quando si vuole archiviare l'handle restituito in un'altra variabile.

Nei nomi di funzione, ***Prefix*** si riferisce al valore del `-prefix` parametro della riga di comando. Se il `-prefix` parametro non viene utilizzato, le funzioni non avranno alcun prefisso.

> [!NOTE]
> La funzione di <b>aggiunta del *contatore* di *prefisso*</b> generata viene utilizzata quando si dispone di un callback del contatore. Quando non si dispone di un callback del contatore, vengono utilizzate le funzioni del contatore create del <b> *prefisso*</b> generato e di chiusura del <b> *prefisso*</b> .

### <a name="using-the-generated-symbol-file"></a>Uso del file di simboli generato

Se il parametro **-ch** viene specificato nella riga di comando, lo strumento CTRPP genererà un `.h` file di simboli. Questo file contiene i simboli C/C++ per i nomi e i GUID di ogni contatore del provider. I simboli possono essere utilizzati per la scrittura di programmi hardcoded per utilizzare i dati di questo contatore usando le [funzioni consumer Perflib V2](using-the-perflib-functions-to-consume-counter-data.md).

## <a name="requirements"></a>Requisiti

|                         ||
|-------------------------|----
| Client minimo supportato| \[Solo app desktop di Windows Vista\]
| Server minimo supportato| \[Solo app desktop Windows Server 2008\]
