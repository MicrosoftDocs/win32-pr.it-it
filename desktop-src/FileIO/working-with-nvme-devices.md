---
description: Informazioni su come usare dispositivi NVMe ad alta velocità dall'applicazione Windows.
ms.assetid: 037AF841-C2C9-4551-9CCB-F2A2F199083A
title: Utilizzo delle unità NVMe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be94adf8355940bd93de137d122d91e468c2173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309524"
---
# <a name="working-with-nvme-drives"></a>Utilizzo delle unità NVMe

**Si applica a:**

-   Windows 10
-   Windows Server 2016

Informazioni su come usare dispositivi NVMe ad alta velocità dall'applicazione Windows. L'accesso al dispositivo viene abilitato tramite **StorNVMe.sys**, il driver interno introdotto per la prima volta in Windows Server 2012 R2 e Windows 8.1. È anche disponibile per i dispositivi Windows 7 tramite una correzione a caldo KB. In Windows 10 sono state introdotte diverse nuove funzionalità, incluso un meccanismo pass-through per i comandi NVMe specifici del fornitore e gli aggiornamenti a IOCTL esistenti.

Questo argomento fornisce una panoramica delle API di uso generale che è possibile usare per accedere alle unità NVMe in Windows 10. Vengono inoltre descritte le operazioni seguenti:

-   Come inviare un comando NVMe specifico del fornitore con [pass-through](#pass-through-mechanism)
-   Come [inviare un comando identifica, Ottieni funzionalità o Ottieni pagine di log](#protocol-specific-queries) all'unità NVMe
-   Come [ottenere informazioni sulla temperatura](#temperature-queries) da un'unità NVMe
-   Come eseguire i comandi di modifica del comportamento, ad esempio l' [impostazione delle soglie di temperatura](#behavior-changing-commands)

## <a name="apis-for-working-with-nvme-drives"></a>API per l'uso di unità NVMe

È possibile usare le API generali seguenti per accedere alle unità NVMe in Windows 10. Queste API si trovano in **winioctl. h** per le applicazioni in modalità utente e **ntddstor. h** per i driver in modalità kernel. Per ulteriori informazioni sui file di intestazione, vedere [file di intestazione](#header-files).

-   [**IOCTL \_ \_ \_ Comando del protocollo di archiviazione**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : usare questo IOCTL con la struttura dei comandi del **\_ protocollo \_ di archiviazione** per emettere i comandi NVMe. Questo IOCTL Abilita NVMe pass-through e supporta il log degli effetti del comando in NVMe. È possibile usarlo con comandi specifici del fornitore. Per altre informazioni, vedere [meccanismo pass-through](#pass-through-mechanism).

-   [**Archiviazione \_ \_Comando protocollo**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : questa struttura del buffer di input include un campo **ReturnStatus** che può essere usato per segnalare i valori di stato seguenti.
    -   **stato del protocollo di archiviazione \_ \_ \_ in sospeso**
    -   **stato del protocollo di archiviazione \_ \_ \_ riuscito**
    -   **\_errore di \_ stato del protocollo di archiviazione \_**
    -   **\_ \_ \_ richiesta non valida per lo stato del protocollo di archiviazione \_**
    -   **stato del protocollo di archiviazione \_ \_ \_ senza \_ dispositivo**
    -   **stato del protocollo di archiviazione \_ \_ \_ occupato**
    -   **\_ \_ \_ sovraccarico dei dati sullo stato del protocollo di archiviazione \_**
    -   **\_risorse stato protocollo di archiviazione \_ \_ insufficiente \_**
    -   **\_lo stato del protocollo di archiviazione \_ non è \_ \_ supportato**
-   [**IOCTL \_ \_ \_ Proprietà query di archiviazione**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : usare questo IOCTL con la struttura della **\_ \_ query della proprietà di archiviazione** per recuperare le informazioni sul dispositivo. Per altre informazioni, vedere [query specifiche del protocollo](#protocol-specific-queries) e [query di temperatura](#temperature-queries).

-   [**Archiviazione \_ PROPERTY \_ query**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : questa struttura include i campi **PropertyId** e **AdditionalParameters** per specificare i dati su cui eseguire la query. Nel file **PropertyId** , usare l'enumerazione **\_ \_ ID proprietà di archiviazione** per specificare il tipo di dati. Usare il campo **AdditionalParameters** per specificare ulteriori dettagli, a seconda del tipo di dati. Per i dati specifici del protocollo, usare la struttura **\_ \_ \_ dei dati specifica del protocollo di archiviazione** nel campo **AdditionalParameters** . Per i dati relativi alla temperatura, usare la struttura **\_ \_ info temperature di archiviazione** nel campo **AdditionalParameters** .
-   [**Archiviazione \_ \_ID proprietà**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : questa enumerazione include nuovi valori che consentono **alla \_ \_ \_ proprietà di query di archiviazione IOCTL** di recuperare informazioni sulla temperatura e sul protocollo.

    -   **StorageAdapterProtocolSpecificProperty**
    -   **StorageDeviceProtocolSpecificProperty**

    Usare uno di questi ID proprietà specifici del protocollo in combinazione con **\_ \_ \_ i dati specifici del protocollo di archiviazione** per recuperare i dati specifici del protocollo nella struttura del [**\_ \_ \_ descrittore dei dati del protocollo di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) .

    -   **StorageAdapterTemperatureProperty**
    -   **StorageDeviceTemperatureProperty**

    Usare uno di questi ID di proprietà della temperatura per recuperare i dati sulla temperatura nella struttura del [**\_ \_ \_ descrittore dei dati della temperatura di archiviazione**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) .

-   [**Archiviazione \_ \_ \_ Dati specifici del protocollo**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : recuperare i dati specifici del NVMe quando questa struttura viene usata per il campo **AdditionalParameters** della **\_ \_ query della proprietà di archiviazione** e viene specificato un valore di enumerazione del [**\_ \_ \_ \_ tipo di dati NVMe del protocollo di archiviazione**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) . Usare uno dei valori del **\_ tipo di \_ \_ dati NVME \_ del protocollo di archiviazione** seguenti nel campo **DataType** della struttura di **\_ \_ \_ dati specifica del protocollo di archiviazione** :

    -   Usare **NVMeDataTypeIdentify** per ottenere identifica dati del controller o identificare i dati dello spazio dei nomi.
    -   Usare **NVMeDataTypeLogPage** per ottenere le pagine di log (inclusi i dati intelligenti/di integrità).
    -   Usare **NVMeDataTypeFeature** per ottenere le funzionalità dell'unità NVMe.

-   [**Archiviazione \_ \_Informazioni sulla temperatura**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : questa struttura viene utilizzata per conservare dati di temperatura specifici. Viene usato nel **\_ \_ \_ descrittore di dati TEMERATURE di archiviazione** per restituire i risultati di una query di temperatura.

-   [**IOCTL \_ \_Soglia di \_ temperatura \_ del set di archiviazione**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : usare questo IOCTL con la struttura della **\_ \_ soglia di temperatura di archiviazione** per impostare le soglie di temperatura. Per altre informazioni, vedere [comandi di modifica del comportamento](#behavior-changing-commands).

-   [**Archiviazione \_ \_Soglia temperatura**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : questa struttura viene utilizzata come buffer di input per specificare la soglia di temperatura. Il campo di **sovrasoglia** (booleano) specifica se il campo della **soglia** è il valore della soglia superiore o meno. in caso contrario, è il valore di soglia sotto.

## <a name="pass-through-mechanism"></a>Meccanismo pass-through

I comandi che non sono definiti nella specifica NVMe sono i più difficili da gestire per il sistema operativo host. l'host non è in grado di comprendere gli effetti che i comandi possono avere sul dispositivo di destinazione, l'infrastruttura esposta (dimensioni di spazi dei nomi/blocchi) e il relativo comportamento.

Per portare a termine tali comandi specifici del dispositivo tramite lo stack di archiviazione di Windows, un nuovo meccanismo pass-through consente di inviare tramite pipe i comandi specifici del fornitore. Questa pipe pass-through facilita anche lo sviluppo di strumenti di gestione e test. Tuttavia, questo meccanismo pass-through richiede l'uso del log degli effetti del comando. Inoltre, StoreNVMe.sys richiede che tutti i comandi, non solo i comandi pass-through, siano descritti nel log degli effetti dei comandi.

> [!IMPORTANT]
> StorNVMe.sys e Storport.sys bloccherà qualsiasi comando in un dispositivo, se non è descritto nel log degli effetti dei comandi.

 

### <a name="supporting-the-command-effects-log"></a>Supporto del log degli effetti del comando

Il log degli effetti del comando (come descritto in comandi supportati ed effetti, sezione 5.10.1.5 della [specifica NVMe 1,2](https://nvmexpress.org/specifications)) consente di descrivere gli effetti dei comandi specifici del fornitore insieme ai comandi definiti dalla specifica. Ciò facilita la convalida del supporto del comando e l'ottimizzazione del comportamento del comando e pertanto deve essere implementato per l'intero set di comandi supportati dal dispositivo. Le condizioni seguenti descrivono il risultato della modalità di invio del comando in base alla voce del log degli effetti dei comandi.

Per qualsiasi comando specifico descritto nel log degli effetti del comando...

**Durante** le operazioni seguenti:

-   Il comando supportato (CSUPP) è impostato su' 1', a indicare che il comando è supportato dal controller (bit 01)

    > [!Note]  
    > Quando CSUPP è impostato su' 0' (a indicare che il comando non è supportato) il comando verrà bloccato

     

**E se** viene impostata una delle seguenti opzioni:

-   La modifica della funzionalità del controller (CCC) è impostata su' 1' a indicare che il comando può modificare le funzionalità del controller (bit 04)

-   La modifica dell'inventario dello spazio dei nomi (NIC) è impostata su' 1', a indicare che il comando può modificare il numero o le funzionalità per più spazi dei nomi (bit 03)

-   La modifica della funzionalità dello spazio dei nomi (NCC) è impostata su' 1', a indicare che il comando può modificare le funzionalità di un singolo spazio dei nomi (bit 02)

-   L'invio e l'esecuzione del comando (CSE) è impostato su 001B o 010B, a indicare che il comando può essere inviato quando non vi sono altri comandi in attesa dello stesso o di uno spazio dei nomi e che un altro comando non deve essere inviato allo stesso o a uno spazio dei nomi fino al completamento del comando (BITS 18:16)

Il comando verrà **quindi** inviato come unico comando in attesa per l'adapter.

**Else if**:

-   L'invio e l'esecuzione del comando (CSE) è impostato su 001B, a indicare che il comando può essere inviato quando non vi sono altri comandi in attesa per lo stesso spazio dei nomi e che un altro comando non deve essere inviato allo stesso spazio dei nomi fino al completamento del comando (BITS 18:16)

Il comando verrà **quindi** inviato come unico comando in attesa all'oggetto numero di unità logica (lun).

**In caso contrario**, il comando viene inviato con altri comandi in attesa senza inibizione. Ad esempio, se un comando specifico del fornitore viene inviato al dispositivo per recuperare informazioni statistiche che non sono definite da specifiche, non è necessario alcun rischio per modificare il comportamento o la funzionalità del dispositivo per eseguire I comandi di I/O. Tali richieste possono essere gestite in parallelo all'I/O e non è necessario sospendere la ripresa.

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a>Uso del \_ comando IOCTL storage \_ Protocol \_ per inviare comandi

Il pass-through può essere eseguito tramite [**il \_ \_ \_ comando IOCTL Storage Protocol**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), introdotto in Windows 10. Questo IOCTL è stato progettato per avere un comportamento simile a quello delle IOCTL di pass-through SCSI e ATA esistenti, per inviare un comando incorporato al dispositivo di destinazione. Tramite questo IOCTL è possibile inviare il pass-through a un dispositivo di archiviazione, inclusa un'unità NVMe.

Ad esempio, in NVMe, IOCTL consentirà l'invio dei seguenti codici di comando.

-   Comandi amministrativi specifici del fornitore (C0h – FFh)
-   Comandi NVMe specifici del fornitore (80H – FFh)

Come per tutti gli altri IOCTL, usare [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) per inviare il comando IOCTL pass-through. IOCTL viene popolato usando la struttura del buffer di input del [**\_ \_ comando del protocollo di archiviazione**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) disponibile in **ntddstor. h**. Popolare il campo di **comando** con il comando specifico del fornitore.


```C++
typedef struct _STORAGE_PROTOCOL_COMMAND {

    ULONG   Version;                        // STORAGE_PROTOCOL_STRUCTURE_VERSION
    ULONG   Length;                         // sizeof(STORAGE_PROTOCOL_COMMAND)

    STORAGE_PROTOCOL_TYPE  ProtocolType;
    ULONG   Flags;                          // Flags for the request

    ULONG   ReturnStatus;                   // return value
    ULONG   ErrorCode;                      // return value, optional

    ULONG   CommandLength;                  // non-zero value should be set by caller
    ULONG   ErrorInfoLength;                // optional, can be zero
    ULONG   DataToDeviceTransferLength;     // optional, can be zero. Used by WRITE type of request.
    ULONG   DataFromDeviceTransferLength;   // optional, can be zero. Used by READ type of request.

    ULONG   TimeOutValue;                   // in unit of seconds

    ULONG   ErrorInfoOffset;                // offsets need to be pointer aligned
    ULONG   DataToDeviceBufferOffset;       // offsets need to be pointer aligned
    ULONG   DataFromDeviceBufferOffset;     // offsets need to be pointer aligned

    ULONG   CommandSpecific;                // optional information passed along with Command.
    ULONG   Reserved0;

    ULONG   FixedProtocolReturnData;        // return data, optional. Some protocol, such as NVMe, may return a small amount data (DWORD0 from completion queue entry) without the need of separate device data transfer.
    ULONG   Reserved1[3];

    _Field_size_bytes_full_(CommandLength) UCHAR Command[ANYSIZE_ARRAY];

} STORAGE_PROTOCOL_COMMAND, *PSTORAGE_PROTOCOL_COMMAND;
```



Il comando specifico del fornitore da inviare deve essere popolato nel campo evidenziato sopra. Si noti che il log degli effetti del comando deve essere implementato per i comandi pass-through. In particolare, questi comandi devono essere segnalati come supportati nel log degli effetti del comando. per ulteriori informazioni, vedere la sezione precedente. Si noti inoltre che i campi PRP sono specifici del driver, pertanto le applicazioni che inviano comandi possono lasciarle come 0.

Infine, questo IOCTL pass-through viene utilizzato per l'invio di comandi specifici del fornitore. Per inviare altri comandi NVMe amministrativi o non specifici del fornitore, ad esempio l'identificazione, questo IOCTL pass-through non deve essere usato. Ad esempio, è necessario usare la **\_ \_ \_ proprietà query di archiviazione IOCTL** per identificare o ottenere le pagine del log. Per altre informazioni, vedere la sezione successiva, [query specifiche del protocollo](/windows).

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a>Non aggiornare il firmware tramite il meccanismo pass-through

I comandi per il download e l'attivazione del firmware non devono essere inviati tramite il pass-through. **IOCTL \_ Il \_ \_ comando del protocollo di archiviazione** deve essere usato solo per i comandi specifici del fornitore.

Usare invece le IOCTL di archiviazione generali seguenti (introdotte in Windows 10) per evitare che le applicazioni usino direttamente la \_ versione SCSI miniport del firmware IOCTL. I driver di archiviazione convertiranno il IOCTL in un comando SCSI o nella \_ versione miniport SCSI di IOCTL per il miniport.

Queste IOCTL sono consigliate per lo sviluppo di strumenti di aggiornamento del firmware in Windows 10 e Windows Server 2016:

-   [**\_informazioni sul \_ firmware di archiviazione \_ IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [**\_download del \_ firmware di archiviazione IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [**\_attivazione del \_ firmware di archiviazione IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

Per ottenere informazioni sull'archiviazione e aggiornare il firmware, Windows supporta anche i cmdlet di PowerShell per eseguire questa operazione rapidamente:

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> Per aggiornare il firmware in NVMe in Windows 8.1, usare \_ il \_ firmware miniport SCSI IOCTL \_ . Questo IOCTL non è stato sottoportato a Windows 7. Per ulteriori informazioni, vedere [aggiornamento del firmware per un dispositivo NVMe in Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a>Restituzione di errori tramite il meccanismo pass-through

Analogamente alle IOCTL pass-through SCSI e ATA, quando un comando/richiesta viene inviato al miniport o al dispositivo, l'IOCTL restituisce se l'operazione ha avuto esito positivo o negativo. Nella struttura [**dei \_ \_ comandi del protocollo di archiviazione**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) , IOCTL restituisce lo stato tramite il campo **ReturnStatus** .

### <a name="example-sending-a-vendor-specific-command"></a>Esempio: invio di un comando specifico del fornitore

In questo esempio, un comando arbitrario specifico del fornitore viene inviato tramite pass-through a un'unità NVMe. Il codice seguente alloca un buffer, Inizializza una query e quindi invia il comando al dispositivo tramite DeviceIoControl.


```C++
    ZeroMemory(buffer, bufferLength);  
    protocolCommand = (PSTORAGE_PROTOCOL_COMMAND)buffer;  

    protocolCommand->Version = STORAGE_PROTOCOL_STRUCTURE_VERSION;  
    protocolCommand->Length = sizeof(STORAGE_PROTOCOL_COMMAND);  
    protocolCommand->ProtocolType = ProtocolTypeNvme;  
    protocolCommand->Flags = STORAGE_PROTOCOL_COMMAND_FLAG_ADAPTER_REQUEST;  
    protocolCommand->CommandLength = STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->ErrorInfoLength = sizeof(NVME_ERROR_INFO_LOG);  
    protocolCommand->DataFromDeviceTransferLength = 4096;  
    protocolCommand->TimeOutValue = 10;  
    protocolCommand->ErrorInfoOffset = FIELD_OFFSET(STORAGE_PROTOCOL_COMMAND, Command) + STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->DataFromDeviceBufferOffset = protocolCommand->ErrorInfoOffset + protocolCommand->ErrorInfoLength;  
    protocolCommand->CommandSpecific = STORAGE_PROTOCOL_SPECIFIC_NVME_ADMIN_COMMAND;  

    command = (PNVME_COMMAND)protocolCommand->Command;  

    command->CDW0.OPC = 0xFF;  
    command->u.GENERAL.CDW10 = 0xto_fill_in;  
    command->u.GENERAL.CDW12 = 0xto_fill_in;  
    command->u.GENERAL.CDW13 = 0xto_fill_in;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_PROTOCOL_COMMAND,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL 
                             );  
```



In questo esempio, si prevede `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` se il comando è riuscito al dispositivo.

## <a name="protocol-specific-queries"></a>Query specifiche del protocollo

Windows 8.1 introdotta la [**\_ proprietà di \_ query \_ di archiviazione IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) per il recupero dei dati. In Windows 10, il IOCTL è stato migliorato per supportare le funzionalità di NVMe richieste comunemente, ad esempio **ottenere le pagine del log**, ottenere le **funzionalità** e **identificare**. In questo modo è possibile recuperare informazioni specifiche di NVMe a scopo di monitoraggio e inventario.

Di seguito è riportato il buffer di input per IOCTL, la [**\_ \_ query della proprietà di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (da Windows 10).


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



Quando si usa la [**\_ \_ \_ proprietà query di archiviazione IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) per recuperare le informazioni specifiche del protocollo NVMe nel [**\_ \_ \_ descrittore di dati del protocollo di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor), configurare la struttura della [**\_ \_ query della proprietà di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) come segue:

-   Allocare un buffer che può contenere sia [**una \_ \_ query della proprietà di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) che una struttura di [**\_ \_ \_ dati specifica del protocollo di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) .

-   Impostare il campo **PropertyId** su **StorageAdapterProtocolSpecificProperty** o **StorageDeviceProtocolSpecificProperty** rispettivamente per una richiesta controller o dispositivo/spazio dei nomi.

-   Impostare il campo **QueryType** su **PropertyStandardQuery**.

-   Riempire la [**struttura \_ \_ \_ dei dati specifica del protocollo di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) con i valori desiderati. L'inizio dei **\_ \_ \_ dati specifici del protocollo di archiviazione** è il campo **AdditionalParameters** della [**\_ \_ query della proprietà di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).

Di seguito è illustrata la struttura [**\_ \_ \_ dei dati specifica del protocollo di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) (da Windows 10).


```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                 

    ULONG   ProtocolDataRequestValue;
    ULONG   ProtocolDataRequestSubValue;

    ULONG   ProtocolDataOffset;         
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;   
    ULONG   Reserved[3];

} STORAGE_PROTOCOL_SPECIFIC_DATA, *PSTORAGE_PROTOCOL_SPECIFIC_DATA;
```



Per specificare un tipo di informazioni specifiche del protocollo NVMe, configurare la struttura dei [**\_ \_ \_ dati specifica del protocollo di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) come segue:

-   Impostare il campo **ProtocolType** su **ProtocolTypeNVMe**.

-   Impostare il campo **DataType** su un valore di enumerazione definito [**dal \_ \_ tipo di \_ dati \_ NVME del protocollo di archiviazione**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):

    -   Usare **NVMeDataTypeIdentify** per ottenere identifica dati del controller o identificare i dati dello spazio dei nomi.
    -   Usare **NVMeDataTypeLogPage** per ottenere le pagine di log (inclusi i dati intelligenti/di integrità).
    -   Usare **NVMeDataTypeFeature** per ottenere le funzionalità dell'unità NVMe.

Quando **ProtocolTypeNVMe** viene usato come **ProtocolType**, è possibile recuperare le query per le informazioni specifiche del protocollo in parallelo con altre i/O sull'unità NVMe.

Negli esempi seguenti vengono illustrate le query specifiche del protocollo NVMe.

### <a name="example-nvme-identify-query"></a>Esempio: NVMe identificare la query

In questo esempio la richiesta di **Identificazione** viene inviata a un'unità NVMe. Il codice seguente inizializza la struttura dei dati della query e quindi invia il comando al dispositivo tramite DeviceIoControl.


```C++
    BOOL    result;
    PVOID   buffer = NULL;
    ULONG   bufferLength = 0;
    ULONG   returnedLength = 0;

    PSTORAGE_PROPERTY_QUERY query = NULL;
    PSTORAGE_PROTOCOL_SPECIFIC_DATA protocolData = NULL;
    PSTORAGE_PROTOCOL_DATA_DESCRIPTOR protocolDataDescr = NULL;

    //
    // Allocate buffer for use.
    //
    bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_QUERY, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA) + NVME_MAX_LOG_SIZE;
    buffer = malloc(bufferLength);

    if (buffer == NULL) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: allocate buffer failed, exit.\n"));
        goto exit;
    }

    //
    // Initialize query data structure to get Identify Controller Data.
    //
    ZeroMemory(buffer, bufferLength);

    query = (PSTORAGE_PROPERTY_QUERY)buffer;
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;

    query->PropertyId = StorageAdapterProtocolSpecificProperty;
    query->QueryType = PropertyStandardQuery;

    protocolData->ProtocolType = ProtocolTypeNvme;
    protocolData->DataType = NVMeDataTypeIdentify;
    protocolData->ProtocolDataRequestValue = NVME_IDENTIFY_CNS_CONTROLLER;
    protocolData->ProtocolDataRequestSubValue = 0;
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);
    protocolData->ProtocolDataLength = NVME_MAX_LOG_SIZE;

    //
    // Send request down.
    //
    result = DeviceIoControl(DeviceList[Index].Handle,
                             IOCTL_STORAGE_QUERY_PROPERTY,
                             buffer,
                             bufferLength,
                             buffer,
                             bufferLength,
                             &returnedLength,
                             NULL
                             );

    ZeroMemory(buffer, bufferLength);
    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < NVME_MAX_LOG_SIZE)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // Identify Controller Data 
    //
    {
        PNVME_IDENTIFY_CONTROLLER_DATA identifyControllerData = (PNVME_IDENTIFY_CONTROLLER_DATA)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        if ((identifyControllerData->VID == 0) ||
            (identifyControllerData->NN == 0)) {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Identify Controller Data not valid.\n"));
            goto exit;
        } else {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Identify Controller Data succeeded_*_.\n"));
        }
    }

  
```



Si noti che il chiamante deve allocare un singolo buffer contenente \_ \_ la query della proprietà di archiviazione e le dimensioni dei \_ dati specifici del protocollo di archiviazione \_ \_ . In questo esempio viene usato lo stesso buffer per l'input e l'output della query della proprietà. Questo è il motivo per cui il buffer allocato ha una dimensione di "offset del campo \_ ( \_ query della proprietà \_ di archiviazione, AdditionalParameters) + sizeof ( \_ dati specifici del protocollo di archiviazione \_ \_ ) + \_ dimensioni massime del \_ log NVME \_ ". Sebbene sia possibile allocare buffer distinti sia per l'input che per l'output, è consigliabile usare un singolo buffer per eseguire query sulle informazioni correlate a NVMe.

### <a name="example-nvme-get-log-pages-query"></a>Esempio: NVMe get log Pages query

In questo esempio, in base a quello precedente, la richiesta _ *get log Pages** viene inviata a un'unità NVMe. Il codice seguente prepara la struttura dei dati della query e quindi invia il comando al dispositivo tramite DeviceIoControl.


```C++
    ZeroMemory(buffer, bufferLength);  

    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  // This will be passed as the lower 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue2 = 0; // This will be passed as the higher 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue3 = 0; // This will be passed as Log Specific Identifier in CDW11.
    protocolData->ProtocolDataRequestSubValue4 = 0; // This will map to STORAGE_PROTOCOL_DATA_SUBVALUE_GET_LOG_PAGE definition, then user can pass Retain Asynchronous Event, Log Specific Field.

    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log failed. Error Code %d.\n"), GetLastError());
        goto exit;
    }

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < sizeof(NVME_HEALTH_INFO_LOG))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // SMART/Health Information Log Data 
    //
    {
        PNVME_HEALTH_INFO_LOG smartInfo = (PNVME_HEALTH_INFO_LOG)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log Data - Temperature %d.\n"), ((ULONG)smartInfo->Temperature[1] << 8 | smartInfo->Temperature[0]) - 273);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_SMART/Health Information Log succeeded_*_.\n"));
    }

```



### <a name="example-nvme-get-features-query"></a>Esempio: NVMe Get features query

In questo esempio, in base a quello precedente, la richiesta _ *Get features** viene inviata a un'unità NVMe. Il codice seguente prepara la struttura dei dati della query e quindi invia il comando al dispositivo tramite DeviceIoControl.


```C++
    //  
    // Initialize query data structure to Volatile Cache feature.  
    //  

    ZeroMemory(buffer, bufferLength);  


    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeFeature;  
    protocolData->ProtocolDataRequestValue = NVME_FEATURE_VOLATILE_WRITE_CACHE;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = 0;  
    protocolData->ProtocolDataLength = 0;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache failed. Error Code %d.\n"), GetLastError());  
        goto exit;  
    }  

    //  
    // Validate the returned data.  
    //  

    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||  
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache  - data descriptor header not valid.\n"));  
        return;                                           
    }  

    //
    // Volatile Cache 
    //
    {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache - %x.\n"), protocolDataDescr->ProtocolSpecificData.FixedProtocolReturnData);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Get Feature - Volatile Cache succeeded_*_.\n"));
    }
```
## <a name="protocol-specific-set"></a>Set specifico del protocollo

Da Windows 10 19H1, il IOCTL_STORAGE_SET_PROPERTY è stato migliorato per supportare le funzionalità di NVMe set.

Il buffer di input per il IOCTL_STORAGE_SET_PROPERTY è illustrato di seguito:

```C++
typedef struct _STORAGE_PROPERTY_SET {

    //
    // ID of the property being retrieved
    //

    STORAGE_PROPERTY_ID PropertyId;

    //
    // Flags indicating the type of set property being performed
    //

    STORAGE_SET_TYPE SetType;

    //
    // Space for additional parameters if necessary
    //

    UCHAR AdditionalParameters[1];

} STORAGE_PROPERTY_SET, _PSTORAGE_PROPERTY_SET;
```

Quando si usa IOCTL_STORAGE_SET_PROPERTY per impostare la funzionalità NVMe, configurare la struttura di STORAGE_PROPERTY_SET come segue:

-   Allocare un buffer che può contenere sia un STORAGE_PROPERTY_SET che una struttura STORAGE_PROTOCOL_SPECIFIC_DATA_EXT;
-   Impostare il campo PropertyID su StorageAdapterProtocolSpecificProperty o StorageDeviceProtocolSpecificProperty rispettivamente per una richiesta controller o dispositivo/spazio dei nomi.
-   Riempire la struttura STORAGE_PROTOCOL_SPECIFIC_DATA_EXT con i valori desiderati. L'inizio del STORAGE_PROTOCOL_SPECIFIC_DATA_EXT è il campo AdditionalParameters di STORAGE_PROPERTY_SET.

Di seguito è illustrata la struttura del STORAGE_PROTOCOL_SPECIFIC_DATA_EXT.

```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA_EXT {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                   // The value will be protocol specific, as defined in STORAGE_PROTOCOL_NVME_DATA_TYPE or STORAGE_PROTOCOL_ATA_DATA_TYPE.

    ULONG   ProtocolDataValue;
    ULONG   ProtocolDataSubValue;      // Data sub request value

    ULONG   ProtocolDataOffset;         // The offset of data buffer is from beginning of this data structure.
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;
    ULONG   ProtocolDataSubValue2;     // First additional data sub request value

    ULONG   ProtocolDataSubValue3;     // Second additional data sub request value
    ULONG   ProtocolDataSubValue4;     // Third additional data sub request value

    ULONG   ProtocolDataSubValue5;     // Fourth additional data sub request value
    ULONG   Reserved[5];
} STORAGE_PROTOCOL_SPECIFIC_DATA_EXT, *PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT;
```

Per specificare un tipo di funzionalità NVMe da impostare, configurare la struttura STORAGE_PROTOCOL_SPECIFIC_DATA_EXT come indicato di seguito:
-   Impostare il campo ProtocolType su ProtocolTypeNvme;
-   Impostare il campo DataType sul valore di enumerazione NVMeDataTypeFeature definito da STORAGE_PROTOCOL_NVME_DATA_TYPE;

Gli esempi seguenti illustrano il set di funzionalità NVMe.

### <a name="example-nvme-set-features"></a>Esempio: NVMe set features

In questo esempio la richiesta set features viene inviata a un'unità NVMe. Il codice seguente prepara la struttura dei dati del set e quindi invia il comando al dispositivo tramite DeviceIoControl.

```C++
            PSTORAGE_PROPERTY_SET                   setProperty = NULL;
            PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT     protocolData = NULL;
            PSTORAGE_PROTOCOL_DATA_DESCRIPTOR_EXT   protocolDataDescr = NULL;

            //
            // Allocate buffer for use.
            //
            bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_SET, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA_EXT);
            bufferLength += NVME_MAX_LOG_SIZE;

            buffer = new UCHAR[bufferLength];

            //
            // Initialize query data structure to get the desired log page.
            //
            ZeroMemory(buffer, bufferLength);

            setProperty = (PSTORAGE_PROPERTY_SET)buffer;

            setProperty->PropertyId = StorageAdapterProtocolSpecificProperty;
            setProperty->SetType = PropertyStandardSet;

            protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT)setProperty->AdditionalParameters;

            protocolData->ProtocolType = ProtocolTypeNvme;
            protocolData->DataType = NVMeDataTypeFeature;
            protocolData->ProtocolDataValue = NVME_FEATURE_HOST_CONTROLLED_THERMAL_MANAGEMENT;

            protocolData->ProtocolDataSubValue = 0; // This will pass to CDW11.
            protocolData->ProtocolDataSubValue2 = 0; // This will pass to CDW12.
            protocolData->ProtocolDataSubValue3 = 0; // This will pass to CDW13.
            protocolData->ProtocolDataSubValue4 = 0; // This will pass to CDW14.
            protocolData->ProtocolDataSubValue5 = 0; // This will pass to CDW15.

            protocolData->ProtocolDataOffset = 0;
            protocolData->ProtocolDataLength = 0;

            //
            // Send request down.
            //
            result = DeviceIoControl(m_deviceHandle,
                                     IOCTL_STORAGE_SET_PROPERTY,
                                     buffer,
                                     bufferLength,
                                     buffer,
                                     bufferLength,
                                     &returnedLength,
                                     NULL
            );
```

## <a name="temperature-queries"></a>Query di temperatura

In Windows 10, [**la \_ \_ \_ proprietà query di archiviazione IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) può essere usata anche per eseguire query sui dati di temperatura dai dispositivi NVMe.

Per recuperare le informazioni sulla temperatura da un'unità NVMe [**nel \_ \_ \_ descrittore di dati della temperatura di archiviazione**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), configurare la struttura della [**\_ \_ query della proprietà di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) come segue:

-   Allocare un buffer che può contenere una struttura di [**\_ \_ query della proprietà di archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) .

-   Impostare il campo **PropertyId** su **StorageAdapterTemperatureProperty** o **StorageDeviceTemperatureProperty** rispettivamente per una richiesta controller o dispositivo/spazio dei nomi.

-   Impostare il campo **QueryType** su **PropertyStandardQuery**.

Di seguito è riportata la struttura delle [**\_ \_ informazioni sulla temperatura di archiviazione**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) (da Windows 10).


```C++
typedef struct _STORAGE_TEMPERATURE_INFO {

    USHORT  Index;                      // Starts from 0. Index 0 may indicate a composite value.
    SHORT   Temperature;                // Signed value; in Celsius.
    SHORT   OverThreshold;              // Signed value; in Celsius.
    SHORT   UnderThreshold;             // Signed value; in Celsius.

    BOOLEAN OverThresholdChangable;     // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN UnderThresholdChangable;    // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN EventGenerated;             // Indicates that notification will be generated when temperature cross threshold.
    UCHAR   Reserved0;
    ULONG   Reserved1;

} STORAGE_TEMPERATURE_INFO, *PSTORAGE_TEMPERATURE_INFO;
```



## <a name="behavior-changing-commands"></a>Comandi di modifica del comportamento

I comandi che modificano gli attributi dei dispositivi o potenzialmente influire sul comportamento del dispositivo sono più difficili da gestire con il sistema operativo. Se gli attributi del dispositivo cambiano in fase di esecuzione durante l'elaborazione dell'I/O, possono verificarsi problemi di sincronizzazione o integrità dei dati se non vengono gestiti correttamente.

Il comando **set-features** di NVMe è un valido esempio di un comando di modifica del comportamento. Consente la modifica del meccanismo di arbitraggio e l'impostazione delle soglie di temperatura. Per assicurarsi che i dati in corso non siano a rischio quando i comandi set che influiscono sul comportamento vengono inviati, verranno sospese tutte le operazioni di I/O nel dispositivo NVMe, le code di svuotamento e i buffer di svuotamento. Una volta eseguito correttamente il comando set, l'I/O viene ripreso (se possibile). Se non è possibile riprendere l'I/O, potrebbe essere necessaria la reimpostazione del dispositivo.

### <a name="setting-temperature-thresholds"></a>Impostazione delle soglie di temperatura

Windows 10 ha introdotto la [**soglia di temperatura del \_ set di archiviazione \_ \_ \_ IOCTL**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold), un IOCTL per ottenere e impostare le soglie di temperatura. È anche possibile usarlo per ottenere la temperatura corrente del dispositivo. Il buffer di input/output per questo IOCTL è la struttura delle [**\_ \_ informazioni sulla temperatura di archiviazione**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) , dalla sezione di codice precedente.

### <a name="example-setting-over-threshold-temperature"></a>Esempio: impostazione della temperatura eccessiva della soglia

In questo esempio viene impostata la temperatura eccessiva di soglia di un'unità NVMe. Il codice seguente prepara il comando e quindi lo invia al dispositivo tramite DeviceIoControl.


```C++
    BOOL    result;  
    ULONG   returnedLength = 0;  
    
    STORAGE_TEMPERATURE_THRESHOLD setThreshold = {0};  

    setThreshold.Version = sizeof(STORAGE_TEMPERATURE_THRESHOLD); 
    setThreshold.Size = sizeof(STORAGE_TEMPERATURE_THRESHOLD);  
    setThreshold.Flags = STORAGE_TEMPERATURE_THRESHOLD_FLAG_ADAPTER_REQUEST;  
    setThreshold.Index = SensorIndex;  
    setThreshold.Threshold = Threshold;  
    setThreshold.OverThreshold = UpdateOverThreshold; 

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD,  
                             &setThreshold,  
                             sizeof(STORAGE_TEMPERATURE_THRESHOLD),  
                             NULL,  
                             0,  
                             &returnedLength,  
                             NULL  
                             ); 

```



### <a name="setting-vendor-specific-features"></a>Impostazione delle funzionalità specifiche del fornitore

Senza il log degli effetti del comando, il driver non conosce le ramificazioni del comando. Questo è il motivo per cui il log degli effetti del comando è obbligatorio. Consente al sistema operativo di determinare se un comando ha un effetto elevato e se può essere inviato in parallelo con altri comandi all'unità.

Il log degli effetti del comando non è ancora sufficientemente granulare per includere i comandi **Set-Feature** specifici del fornitore. Per questo motivo, non è ancora possibile inviare comandi **Set-Feature** specifici del fornitore. Tuttavia, è possibile usare il meccanismo pass-through, descritto in precedenza, per inviare comandi specifici del fornitore. Per altre informazioni, vedere [meccanismo pass-through](#pass-through-mechanism).

## <a name="header-files"></a>File di intestazione

I file seguenti sono rilevanti per lo sviluppo di NVMe. Questi file sono inclusi in [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads).



| File di intestazione    | Descrizione                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| **ntddstor. h** | Definisce costanti e tipi per l'accesso ai driver della classe di archiviazione dalla modalità kernel.   |
| **nVMe. h**     | Per altre strutture di dati correlate a NVMe.                                                 |
| **winioctl. h** | Per le definizioni globali del comando IOCTL Win32, incluse le API di archiviazione per le applicazioni in modalità utente. |



 

 

 
