---
description: Informazioni su come usare dispositivi NVMe ad alta velocità dall'applicazione Windows rete.
ms.assetid: 037AF841-C2C9-4551-9CCB-F2A2F199083A
title: Uso delle unità NVMe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 425516946d1e76e5c01f6ae5d11f104244f85ce0
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436276"
---
# <a name="working-with-nvme-drives"></a>Uso delle unità NVMe

**Si applica a:**

-   Windows 10
-   Windows Server 2016

Informazioni su come usare dispositivi NVMe ad alta velocità dall'applicazione Windows rete. L'accesso al dispositivo **viene abilitato tramiteStorNVMe.sys**, il driver in-box introdotto per la prima volta in Windows Server 2012 R2 e Windows 8.1. È anche disponibile per i dispositivi Windows 7 tramite una correzione rapida kb. In Windows 10 sono state introdotte diverse nuove funzionalità, tra cui un meccanismo pass-through per i comandi NVMe specifici del fornitore e gli aggiornamenti agli IOCTL esistenti.

Questo argomento offre una panoramica delle API di uso generale che è possibile usare per accedere alle unità NVMe in Windows 10. Descrive anche:

-   Come inviare un comando NVMe specifico del fornitore con [pass-through](#pass-through-mechanism)
-   Come [inviare un comando Identify, Get Features o Get Log Pages](#protocol-specific-queries) all'unità NVMe
-   Come ottenere [informazioni sulla temperatura da](#temperature-queries) un'unità NVMe
-   Come eseguire comandi di modifica del comportamento, ad esempio [l'impostazione delle soglie di temperatura](#behavior-changing-commands)

## <a name="apis-for-working-with-nvme-drives"></a>API per l'uso di unità NVMe

È possibile usare le API di uso generale seguenti per accedere alle unità NVMe in Windows 10. Queste API sono disponibili in **winioctl.h** per le applicazioni in modalità utente e **ntddstor.h** per i driver in modalità kernel. Per altre informazioni sui file di intestazione, vedere [File di intestazione.](#header-files)

-   [**IOCTL \_ STORAGE \_ PROTOCOL \_ COMMAND:**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) usare questo IOCTL con la struttura **STORAGE PROTOCOL \_ \_ COMMAND** per eseguire comandi NVMe. Questo ioCTL abilita il pass-through NVMe e supporta il log degli effetti dei comandi in NVMe. È possibile usarlo con comandi specifici del fornitore. Per altre informazioni, vedere [Meccanismo pass-through.](#pass-through-mechanism)

-   [**ARCHIVIAZIONE \_ PROTOCOL \_ COMMAND:**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) questa struttura del buffer di input include un **campo ReturnStatus** che può essere usato per segnalare i valori di stato seguenti.
    -   **STATO \_ DEL PROTOCOLLO DI ARCHIVIAZIONE IN \_ \_ SOSPESO**
    -   **STATO \_ DEL PROTOCOLLO DI ARCHIVIAZIONE \_ \_ RIUSCITO**
    -   **ERRORE DI \_ STATO DEL PROTOCOLLO DI \_ \_ ARCHIVIAZIONE**
    -   **RICHIESTA DI \_ STATO DEL PROTOCOLLO DI ARCHIVIAZIONE NON \_ \_ \_ VALIDA**
    -   **STATO \_ DEL PROTOCOLLO DI ARCHIVIAZIONE NESSUN \_ \_ \_ DISPOSITIVO**
    -   **STATO \_ DEL PROTOCOLLO DI ARCHIVIAZIONE \_ \_ OCCUPATO**
    -   **SOVRACCARICO \_ DEI DATI DI STATO DEL PROTOCOLLO DI \_ \_ \_ ARCHIVIAZIONE**
    -   **RISORSE \_ INSUFFICIENTI \_ PER LO STATO DEL PROTOCOLLO DI \_ \_ ARCHIVIAZIONE**
    -   **STATO \_ DEL PROTOCOLLO DI ARCHIVIAZIONE NON \_ \_ \_ SUPPORTATO**
-   [**IOCTL \_ STORAGE \_ QUERY \_ PROPERTY :**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) usare questo IOCTL con la struttura STORAGE PROPERTY **\_ \_ QUERY** per recuperare le informazioni sul dispositivo. Per altre informazioni, vedere [Query specifiche del protocollo e](#protocol-specific-queries) Query sulla [temperatura.](#temperature-queries)

-   [**ARCHIVIAZIONE \_ PROPERTY \_ QUERY:**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) questa struttura include i **campi PropertyId** **e AdditionalParameters** per specificare i dati su cui eseguire query. Nel **PropertyId** filed usare **l'enumerazione STORAGE PROPERTY \_ \_ ID** per specificare il tipo di dati. Usare il **campo AdditionalParameters** per specificare altri dettagli, a seconda del tipo di dati. Per i dati specifici del protocollo, usare la **struttura STORAGE PROTOCOL SPECIFIC \_ \_ \_ DATA** nel **campo AdditionalParameters.** Per i dati relativi alla temperatura, usare la struttura **\_ STORAGE TEMPERATURE \_ INFO** nel **campo AdditionalParameters.**
-   [**ARCHIVIAZIONE \_ PROPERTY \_ ID:**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) questa enumerazione include nuovi valori che consentono a **IOCTL \_ STORAGE QUERY \_ \_ PROPERTY** di recuperare informazioni specifiche del protocollo e sulla temperatura.

    -   **StorageAdapterProtocolSpecificProperty**
    -   **StorageDeviceProtocolSpecificProperty**

    Usare uno di questi ID proprietà specifici del protocollo in combinazione con **STORAGE \_ PROTOCOL SPECIFIC \_ \_ DATA** per recuperare i dati specifici del protocollo nella struttura DEL DESCRITTORE DI DATI DEL PROTOCOLLO [**\_ \_ \_ DI**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) ARCHIVIAZIONE.

    -   **StorageAdapterTemperatureProperty**
    -   **StorageDeviceTemperatureProperty**

    Usare uno di questi ID proprietà di temperatura per recuperare i dati relativi alla temperatura nella [**struttura STORAGE TEMPERATURE DATA \_ \_ \_ DESCRIPTOR.**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor)

-   [**ARCHIVIAZIONE \_ DATI \_ \_ SPECIFICI**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) DEL PROTOCOLLO: recuperare dati specifici di NVMe quando questa struttura viene usata per il campo **AdditionalParameters** di **STORAGE PROPERTY \_ \_ QUERY** e viene specificato un valore di enumerazione [**STORAGE PROTOCOL \_ \_ NVME \_ DATA \_ TYPE.**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) Usare uno dei valori **\_ \_ NVME \_ DATA \_ TYPE** del PROTOCOLLO DI ARCHIVIAZIONE seguenti nel campo **DataType** della struttura **STORAGE PROTOCOL \_ \_ SPECIFIC \_** DATA:

    -   Usare **NVMeDataTypeIdentify per** ottenere i dati del controller di identificazione o identificare i dati dello spazio dei nomi.
    -   Usare **NVMeDataTypeLogPage per** ottenere le pagine di log (inclusi i dati SMART/di integrità).
    -   Usare **NVMeDataTypeFeature** per ottenere le funzionalità dell'unità NVMe.

-   [**ARCHIVIAZIONE \_ INFORMAZIONI \_ SULLA TEMPERATURA:**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) questa struttura viene usata per contenere dati di temperatura specifici. Viene usato nel DESCRITTOre **STORAGE \_ TEMERATURE \_ DATA \_** per restituire i risultati di una query sulla temperatura.

-   [**IOCTL \_ STORAGE \_ SET \_ TEMPERATURE \_ THRESHOLD:**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) usare questo IOCTL con la struttura **STORAGE TEMPERATURE \_ \_ THRESHOLD** per impostare le soglie di temperatura. Per altre informazioni, vedere Comandi [di modifica del comportamento.](#behavior-changing-commands)

-   [**ARCHIVIAZIONE \_ TEMPERATURE \_ THRESHOLD:**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) questa struttura viene usata come buffer di input per specificare la soglia di temperatura. Il **campo OverThreshold** (booleano) specifica se il campo **Soglia** è il valore di soglia superiore o meno (in caso contrario, è il valore inferiore alla soglia).

## <a name="pass-through-mechanism"></a>Meccanismo pass-through

I comandi non definiti nella specifica NVMe sono i più difficili da gestire per il sistema operativo host: l'host non ha informazioni dettagliate sugli effetti che i comandi possono avere sul dispositivo di destinazione, sull'infrastruttura esposta (spazi dei nomi/dimensioni dei blocchi) e sul relativo comportamento.

Per eseguire in modo più semplice tali comandi specifici del dispositivo tramite lo stack di archiviazione Windows, un nuovo meccanismo pass-through consente il pipe dei comandi specifici del fornitore. Questa pipe pass-through consente anche lo sviluppo di strumenti di gestione e test. Tuttavia, questo meccanismo pass-through richiede l'uso del log degli effetti del comando. Inoltre, StoreNVMe.sys tutti i comandi, non solo i comandi pass-through, devono essere descritti nel log degli effetti dei comandi.

> [!IMPORTANT]
> StorNVMe.sys e Storport.sys bloccano qualsiasi comando per un dispositivo se non è descritto nel log degli effetti del comando.

 

### <a name="supporting-the-command-effects-log"></a>Supporto del log degli effetti del comando

Il log degli effetti dei comandi (come descritto in Comandi supportati ed effetti, sezione 5.10.1.5 della specifica [NVMe 1.2)](https://nvmexpress.org/specifications)consente di descrizione degli effetti dei comandi specifici del fornitore insieme ai comandi definiti dalla specifica. Ciò facilita sia la convalida del supporto dei comandi che l'ottimizzazione del comportamento dei comandi e pertanto deve essere implementato per l'intero set di comandi supportati dal dispositivo. Le condizioni seguenti descrivono il risultato della modalità di invio del comando in base alla relativa voce log degli effetti del comando.

Per qualsiasi comando specifico descritto nel log degli effetti del comando...

**Mentre**:

-   Command Supported (CSUPP) è impostato su "1", a significare che il comando è supportato dal controller (Bit 01)

    > [!Note]  
    > Quando CSUPP è impostato su "0", a significa che il comando non è supportato, il comando verrà bloccato

     

**E se** è impostata una delle opzioni seguenti:

-   La modifica delle funzionalità del controller (CCC) è impostata su "1", a significare che il comando può modificare le funzionalità del controller (Bit 04)

-   La modifica dell'inventario dello spazio dei nomi (NIC) è impostata su "1", a significare che il comando può modificare il numero o le funzionalità per più spazi dei nomi (Bit 03)

-   L'opzione NCC (Namespace Capability Change) è impostata su "1", a significare che il comando può modificare le funzionalità di un singolo spazio dei nomi (Bit 02)

-   L'invio e l'esecuzione del comando (CSE) è impostato su 001b o 010b, a significare che il comando può essere inviato quando non sono presenti altri comandi in sospeso per lo stesso o qualsiasi spazio dei nomi e che un altro comando non deve essere inviato allo stesso o a qualsiasi spazio dei nomi fino al completamento del comando (Bits 18:16)

**Il** comando verrà quindi inviato come unico comando in sospeso per l'adapter.

**In caso di altro tipo,** se :

-   L'invio e l'esecuzione dei comandi è impostato su 001b, a significare che il comando può essere inviato quando non sono presenti altri comandi in sospeso per lo stesso spazio dei nomi e che un altro comando non deve essere inviato allo stesso spazio dei nomi fino al completamento di questo comando (bit 18:16)

**Il** comando verrà quindi inviato come unico comando in attesa dell'oggetto numero di unità logica (LUN).

**In** caso contrario, il comando viene inviato con altri comandi in sospeso senza inibizione. Ad esempio, se al dispositivo viene inviato un comando specifico del fornitore per recuperare informazioni statistiche non definite in modo specifico, non dovrebbe esserci alcun rischio di modificare il comportamento o la capacità del dispositivo di eseguire i comandi di I/O. Tali richieste potrebbero essere inviate in parallelo all'I/O e non sarebbe necessario sospendere la ripresa.

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a>Uso di IOCTL \_ STORAGE PROTOCOL COMMAND per \_ \_ inviare comandi

Il pass-through può essere eseguito usando [**IOCTL \_ STORAGE \_ PROTOCOL \_ COMMAND,**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command)introdotto in Windows 10. Questo ioCTL è stato progettato per avere un comportamento simile a quello degli IOCTL pass-through SCSI e ATA esistenti, per inviare un comando incorporato al dispositivo di destinazione. Tramite questo IOCTL, il pass-through può essere inviato a un dispositivo di archiviazione, inclusa un'unità NVMe.

In NVMe, ad esempio, IOCTL consentirà l'invio dei codici di comando seguenti.

-   Comandi di amministrazione specifici del fornitore (C0h - FFh)
-   Comandi NVMe specifici del fornitore (80h - FFh)

Come per tutti gli altri IOCTL, usare [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) per inviare l'IOCTL pass-through. Il file IOCTL viene popolato usando la struttura del buffer di input [**\_ STORAGE PROTOCOL \_ COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) disponibile in **ntddstor.h.** Compilare il **campo Comando** con il comando specifico del fornitore.


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



Il comando specifico del fornitore che si desidera inviare deve essere popolato nel campo evidenziato sopra. Si noti ancora una volta che il log degli effetti del comando deve essere implementato per i comandi pass-through. In particolare, questi comandi devono essere segnalati come supportati nel log degli effetti dei comandi (vedere la sezione precedente per altre informazioni). Si noti anche che i campi PRP sono specifici del driver, pertanto le applicazioni che inviano comandi possono lasciarli come 0.

Infine, questo IOCTL pass-through è destinato all'invio di comandi specifici del fornitore. Per inviare altri comandi NVMe specifici dell'amministratore o non del fornitore, ad esempio Identify, questo IOCTL pass-through non deve essere usato. Ad esempio, **è necessario usare IOCTL \_ STORAGE QUERY \_ \_ PROPERTY** per Identificare o ottenere le pagine di log. Per altre informazioni, vedere la sezione successiva Query [specifiche del protocollo](/windows).

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a>Non aggiornare il firmware tramite il meccanismo pass-through

I comandi di download e attivazione del firmware non devono essere inviati tramite pass-through. **IOCTL \_ STORAGE \_ PROTOCOL \_ COMMAND deve** essere usato solo per i comandi specifici del fornitore.

Usare invece gli IOCL di archiviazione generali seguenti (introdotti in Windows 10) per evitare che le applicazioni usino direttamente la versione miniport SCSI del \_ firmware IOCTL. Archiviazione driver traslano ioCTL in un comando SCSI o nella versione miniport SCSI di \_ IOCTL nel miniport.

Questi IOCL sono consigliati per lo sviluppo di strumenti di aggiornamento del firmware in Windows 10 e Windows Server 2016:

-   [**INFORMAZIONI SUL \_ FIRMWARE DI \_ ARCHIVIAZIONE \_ IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [**DOWNLOAD DEL FIRMWARE DI ARCHIVIAZIONE IOCTL \_ \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [**ATTIVAZIONE DEL FIRMWARE DI ARCHIVIAZIONE IOCTL \_ \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

Per ottenere informazioni di archiviazione e aggiornare il firmware, Windows supporta anche i cmdlet di PowerShell per eseguire rapidamente questa operazione:

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> Per aggiornare il firmware in NVMe in Windows 8.1, usare IOCTL \_ SCSI \_ MINIPORT \_ FIRMWARE. Non è stato possibile eseguire il backport di questo IOCTL Windows 7. Per altre informazioni, vedere [Aggiornamento del firmware per un dispositivo NVMe in Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a>Restituzione di errori tramite il meccanismo pass-through

Analogamente agli IOCL pass-through SCSI e ATA, quando un comando/richiesta viene inviato al miniport o al dispositivo, ioCTL restituisce se ha avuto esito positivo o meno. Nella struttura [**STORAGE \_ PROTOCOL \_ COMMAND,**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) IOCTL restituisce lo stato tramite il **campo ReturnStatus.**

### <a name="example-sending-a-vendor-specific-command"></a>Esempio: invio di un comando specifico del fornitore

In questo esempio, un comando arbitrario specifico del fornitore (0xFF) viene inviato tramite pass-through a un'unità NVMe. Il codice seguente alloca un buffer, inizializza una query e quindi invia il comando al dispositivo tramite DeviceIoControl.


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



In questo esempio si prevede che `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` il comando sia riuscito al dispositivo.

## <a name="protocol-specific-queries"></a>Query specifiche del protocollo

Windows 8.1 introdotto [**IOCTL \_ STORAGE \_ QUERY PROPERTY \_ per**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) il recupero dei dati. In Windows 10, IOCTL è stato migliorato per supportare le funzionalità NVMe comunemente richieste, ad esempio **Get Log Pages,** **Get Features** e **Identify.** Ciò consente il recupero di informazioni specifiche di NVMe a scopo di monitoraggio e inventario.

Il buffer di input per IOCTL, [**STORAGE \_ PROPERTY \_ QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (da Windows 10) è visualizzato qui.


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



Quando si [**usa IOCTL \_ STORAGE QUERY \_ \_ PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) per recuperare informazioni specifiche del protocollo NVMe in [**STORAGE PROTOCOL DATA \_ \_ \_ DESCRIPTOR,**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor)configurare la struttura [**STORAGE PROPERTY \_ \_ QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) come segue:

-   Allocare un buffer che può contenere sia una [**query \_ DI PROPRIETÀ \_ DI ARCHIVIAZIONE**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) che una struttura DI DATI SPECIFICI DEL PROTOCOLLO [**\_ \_ \_ DI**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) ARCHIVIAZIONE.

-   Impostare il **campo PropertyID** su **StorageAdapterProtocolSpecificProperty** o **StorageDeviceProtocolSpecificProperty rispettivamente** per una richiesta di controller o dispositivo/spazio dei nomi.

-   Impostare il **campo QueryType** su **PropertyStandardQuery**.

-   Compilare [**la struttura STORAGE PROTOCOL SPECIFIC \_ \_ \_ DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) con i valori desiderati. L'inizio dei **DATI SPECIFICI DEL PROTOCOLLO DI \_ \_ \_ ARCHIVIAZIONE** è il **campo AdditionalParameters** di [**STORAGE PROPERTY \_ \_ QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).

La [**struttura DEI DATI \_ \_ SPECIFICI \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) DEL PROTOCOLLO DI ARCHIVIAZIONE (Windows 10) è illustrata qui.


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



Per specificare un tipo di informazioni specifiche del protocollo NVMe, configurare la struttura [**STORAGE \_ PROTOCOL SPECIFIC \_ \_ DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) come segue:

-   Impostare il **campo ProtocolType** su **ProtocolTypeNVMe**.

-   Impostare il **campo DataType** su un valore di enumerazione definito da [**STORAGE PROTOCOL \_ \_ NVME \_ DATA \_ TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):

    -   Usare **NVMeDataTypeIdentify** per ottenere i dati di Identificazione controller o Identificare i dati dello spazio dei nomi.
    -   Usare **NVMeDataTypeLogPage** per ottenere le pagine di log ,inclusi i dati SMART/health.
    -   Usare **NVMeDataTypeFeature per** ottenere le funzionalità dell'unità NVMe.

Quando **ProtocolTypeNVMe** viene usato come **ProtocolType**, le query per informazioni specifiche del protocollo possono essere recuperate in parallelo con altre operazioni di I/O nell'unità NVMe.

> [!IMPORTANT]
> Per un [**IOCTL_STORAGE_QUERY_PROPERTY**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property) che usa un **STORAGE_PROPERTY_ID** di [**StorageAdapterProtocolSpecificProperty**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id)e la cui struttura [**STORAGE_PROTOCOL_SPECIFIC_DATA**](/windows/win32/api/winioctl/ns-winioctl-storage_protocol_specific_data) o [**STORAGE_PROTOCOL_SPECIFIC_DATA_EXT**](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-storage_protocol_specific_data_ext) è impostata su e , impostare il membro ProtocolDataLength della stessa struttura su un valore minimo `ProtocolType=ProtocolTypeNvme` di `DataType=NVMeDataTypeLogPage` 512 (byte).


Gli esempi seguenti illustrano query specifiche del protocollo NVMe.

### <a name="example-nvme-identify-query"></a>Esempio: query NVMe Identify

In questo esempio la richiesta **Di** identificazione viene inviata a un'unità NVMe. Il codice seguente inizializza la struttura dei dati della query e quindi invia il comando al dispositivo tramite DeviceIoControl.


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
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: ***Identify Controller Data succeeded***.\n"));
        }
    }

  
```

> [!IMPORTANT]
> Per un [**IOCTL_STORAGE_QUERY_PROPERTY**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property) che usa un **STORAGE_PROPERTY_ID** di [**StorageAdapterProtocolSpecificProperty**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id)e la cui struttura [**STORAGE_PROTOCOL_SPECIFIC_DATA**](/windows/win32/api/winioctl/ns-winioctl-storage_protocol_specific_data) o [**STORAGE_PROTOCOL_SPECIFIC_DATA_EXT**](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-storage_protocol_specific_data_ext) è impostata su e , impostare il membro ProtocolDataLength della stessa struttura su un valore minimo `ProtocolType=ProtocolTypeNvme` di `DataType=NVMeDataTypeLogPage` 512 (byte).


Si noti che il chiamante deve allocare un singolo buffer contenente STORAGE \_ PROPERTY QUERY e le dimensioni di STORAGE PROTOCOL SPECIFIC \_ \_ \_ \_ DATA. In questo esempio viene utilizzato lo stesso buffer per l'input e l'output della query di proprietà. Ecco perché il buffer allocato ha una dimensione di "FIELD \_ OFFSET(STORAGE \_ PROPERTY \_ QUERY, AdditionalParameters) + sizeof(STORAGE \_ PROTOCOL SPECIFIC \_ \_ DATA) + NVME \_ MAX LOG \_ \_ SIZE". Anche se è possibile allocare buffer separati sia per l'input che per l'output, è consigliabile usare un singolo buffer per eseguire query sulle informazioni correlate a NVMe.

### <a name="example-nvme-get-log-pages-query"></a>Esempio: query NVMe Get Log Pages

In questo esempio, in base a quello precedente, la richiesta **Get Log Pages** viene inviata a un'unità NVMe. Il codice seguente prepara la struttura dei dati della query e quindi invia il comando al dispositivo tramite DeviceIoControl.


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

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: ***SMART/Health Information Log succeeded***.\n"));
    }

```



### <a name="example-nvme-get-features-query"></a>Esempio: query NVMe Get Features

In questo esempio, in base a quello precedente, la richiesta **Get Features** viene inviata a un'unità NVMe. Il codice seguente prepara la struttura dei dati della query e quindi invia il comando al dispositivo tramite DeviceIoControl.


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

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: ***Get Feature - Volatile Cache succeeded***.\n"));
    }
```
## <a name="protocol-specific-set"></a>Set specifico del protocollo

A partire Windows 10 19H1, il IOCTL_STORAGE_SET_PROPERTY è stato migliorato per supportare le funzionalità dei set NVMe.

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

} STORAGE_PROPERTY_SET, *PSTORAGE_PROPERTY_SET;
```

Quando si usa IOCTL_STORAGE_SET_PROPERTY per impostare la funzionalità NVMe, configurare la STORAGE_PROPERTY_SET struttura come indicato di seguito:

-   Allocare un buffer che può contenere sia un STORAGE_PROPERTY_SET che una STORAGE_PROTOCOL_SPECIFIC_DATA_EXT struttura .
-   Impostare il campo PropertyID su StorageAdapterProtocolSpecificProperty o StorageDeviceProtocolSpecificProperty rispettivamente per una richiesta di controller o dispositivo/spazio dei nomi.
-   Riempire la STORAGE_PROTOCOL_SPECIFIC_DATA_EXT con i valori desiderati. L'inizio del STORAGE_PROTOCOL_SPECIFIC_DATA_EXT è il campo AdditionalParameters STORAGE_PROPERTY_SET.

La STORAGE_PROTOCOL_SPECIFIC_DATA_EXT struttura è illustrata qui.

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

Per specificare un tipo di funzionalità NVMe da impostare, configurare la STORAGE_PROTOCOL_SPECIFIC_DATA_EXT struttura come indicato di seguito:
-   Impostare il campo ProtocolType su ProtocolTypeNvme;
-   Impostare il campo DataType sul valore di enumerazione NVMeDataTypeFeature definito da STORAGE_PROTOCOL_NVME_DATA_TYPE;

Gli esempi seguenti illustrano il set di funzionalità NVMe.

### <a name="example-nvme-set-features"></a>Esempio: Funzionalità del set di NVMe

In questo esempio la richiesta Imposta funzionalità viene inviata a un'unità NVMe. Il codice seguente prepara la struttura dei dati del set e quindi invia il comando al dispositivo tramite DeviceIoControl.

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

## <a name="temperature-queries"></a>Query sulla temperatura

In Windows 10, [**è anche possibile usare IOCTL STORAGE QUERY \_ \_ \_ PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) per eseguire query sui dati relativi alla temperatura dai dispositivi NVMe.

Per recuperare le informazioni sulla temperatura da un'unità NVMe in [**STORAGE \_ TEMPERATURE DATA \_ \_ DESCRIPTOR,**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor)configurare la struttura [**STORAGE PROPERTY \_ \_ QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) come segue:

-   Allocare un buffer che può contenere una [**struttura STORAGE \_ PROPERTY \_ QUERY.**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query)

-   Impostare il **campo PropertyID** su **StorageAdapterTemperatureProperty** o **StorageDeviceTemperatureProperty** rispettivamente per una richiesta di controller o dispositivo/spazio dei nomi.

-   Impostare il **campo QueryType** su **PropertyStandardQuery**.

La [**struttura STORAGE TEMPERATURE \_ \_ INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) (da Windows 10) è illustrata qui.


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

I comandi che modificano gli attributi del dispositivo o potenzialmente influiscono sul comportamento del dispositivo sono più difficili da gestire per il sistema operativo. Se gli attributi del dispositivo cambiano in fase di esecuzione durante l'elaborazione di I/O, possono verificarsi problemi di sincronizzazione o integrità dei dati se non gestiti correttamente.

Il comando NVMe **Set-Features** è un buon esempio di un comando di modifica del comportamento. Consente la modifica del meccanismo di arbitraggio e l'impostazione delle soglie di temperatura. Per garantire che i dati in fase di esecuzione non siano a rischio quando vengono inviati comandi set che influiscono sul comportamento, Windows sospende tutti gli I/O al dispositivo NVMe, le code di svuotamento e i buffer di scaricamento. Dopo che il comando set è stato eseguito correttamente, l'I/O viene ripreso (se possibile). Se non è possibile riprendere l'I/O, potrebbe essere necessaria una reimpostazione del dispositivo.

### <a name="setting-temperature-thresholds"></a>Impostazione delle soglie di temperatura

Windows 10 introdotto [**IOCTL \_ STORAGE \_ SET TEMPERATURE \_ \_ THRESHOLD,**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold)un IOCTL per ottenere e impostare le soglie di temperatura. È anche possibile usarlo per ottenere la temperatura corrente del dispositivo. Il buffer di input/output per questo IOCTL è la struttura [**STORAGE \_ TEMPERATURE \_ INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) della sezione di codice precedente.

### <a name="example-setting-over-threshold-temperature"></a>Esempio: Impostazione della temperatura oltre la soglia

In questo esempio viene impostata la temperatura oltre la soglia di un'unità NVMe. Il codice seguente prepara il comando e lo invia al dispositivo tramite DeviceIoControl.


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

Senza il log degli effetti dei comandi, il driver non è a conoscenza delle ramificazioni del comando. Per questo motivo è necessario il log degli effetti dei comandi. Consente al sistema operativo di determinare se un comando ha un impatto elevato e se può essere inviato in parallelo con altri comandi all'unità.

Il log degli effetti del comando non è ancora sufficientemente granulare da includere i comandi **Set-Features** specifici del fornitore. Per questo motivo, non è ancora possibile inviare comandi **Set-Features** specifici del fornitore. Tuttavia, è possibile usare il meccanismo pass-through, descritto in precedenza, per inviare comandi specifici del fornitore. Per altre informazioni, vedere [Meccanismo pass-through.](#pass-through-mechanism)

## <a name="header-files"></a>File di intestazione

I file seguenti sono rilevanti per lo sviluppo di NVMe. Questi file sono inclusi in [Microsoft Windows Software Development Kit (SDK).](https://developer.microsoft.com/windows/downloads)



| File di intestazione    | Descrizione                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| **ntddstor.h** | Definisce costanti e tipi per l'accesso ai driver della classe di archiviazione dalla modalità kernel.   |
| **nvme.h**     | Per altre strutture di dati correlate a NVMe.                                                 |
| **winioctl.h** | Per le definizioni IOCTL Win32 generali, incluse le API di archiviazione per le applicazioni in modalità utente. |



 

 

 
