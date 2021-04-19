---
description: Le API DLP (Endpoint Data Loss Prevention) consentono alle applicazioni di inviare una notifica al sistema operativo prima e dopo determinate operazioni, ad esempio l'apertura o il salvataggio di un file.
title: Prevenzione della perdita di dati degli endpoint
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: 867e059e0accfc1208c96394c3065d69cf9f576c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495591"
---
# <a name="endpoint-data-loss-prevention"></a>Prevenzione della perdita di dati degli endpoint

Windows 10 implementa meccanismi che consentono di evitare la perdita di dati per i file sensibili. Le API DLP (Endpoint Data Loss Prevention) consentono alle applicazioni di inviare una notifica al sistema operativo prima e dopo determinate operazioni, ad esempio l'apertura o il salvataggio di un file. Queste notifiche fungono da "hint" che consentono al sistema di ottimizzare le operazioni di perdita dei dati.

## <a name="location-of-the-dlp-dll"></a>Percorso della DLL DLP

Poiché la DLL DLP dell'endpoint non è in bundle con il Windows SDK, le applicazioni dovranno caricare manualmente la DLL in fase di esecuzione. Il percorso della DLL viene archiviato nel Registro di sistema. Nella tabella seguente sono elencate le chiavi e i valori del Registro di sistema in cui sono archiviate queste informazioni. Questi percorsi sono definiti come costanti nell'elenco di codice endpointdlp.h di esempio fornito di seguito per praticità per gli sviluppatori.

| Costante | Valore | Descrizione   |
|----------|-------|---------------|
| ENDPOINTDLP_DLL_NAME | "EndpointDlp.dll" | Nome della DLL DLP dell'endpoint che fornisce l'API |
| ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY | "SOFTWARE \\ Microsoft \\ Windows Defender" | Windows Defender chiave del Registro di sistema in HKLM in cui sono archiviate alcune impostazioni DLP dell'endpoint |
| ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY | Valore di ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY |  Percorso del Registro di sistema nella chiave HKLM da cui è possibile EndpointDlp.dll percorso di installazione |
| ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE | "InstallLocation" | Valore del Registro di sistema in ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in cui è archiviato il EndpointDlp.dll di installazione |
| ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX | "x86" | Nelle piattaforme x64 concatenare questa directory per ottenere la versione x86 di EndpointDlp.dll |

## <a name="check-if-endpoint-dlp-is-enabled"></a>Controllare se la prevenzione della perdita dei dati dell'endpoint è abilitata

Per determinare se la prevenzione della perdita dei dati dell'endpoint è abilitata nel sistema, controllare il valore della chiave del Registro di sistema seguente. 

| Costante | Valore | Descrizione   |
|----------|-------|---------------|
| ENDPOINTDLP_ENABLED_FLAG_REGKEY |  \\"Funzionalità" | Percorso della chiave del flag abilitata per la prevenzione della perdita dei dati dell'endpoint in (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY |
| ENDPOINTDLP_ENABLED_FLAG_REGVALUE | "SenseDlpEnabled" | Valore del Registro di sistema in ENDPOINTDLP_ENABLED_FLAG_REGKEY contenente la chiave del Registro di sistema del flag DLP abilitato

## <a name="endpoint-dlp-apis"></a>API DLP degli endpoint

Le tabelle seguenti elencano le API fornite dalla DLL DLP dell'endpoint.

### <a name="initialization-and-versioning"></a>Inizializzazione e controllo delle versioni

| API | Descrizione |
|-----|-------------|
| [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md)                       | Notifica al sistema le modalità di imposizione desiderate per un set di operazioni dlp (Data Loss Prevention) dell'endpoint.                                  |
| [DlpGetEnforcementApiVersion](endpointdlp-dlpgetenforcementapiversion.md)                       | Recupera la versione dell'API prevenzione della perdita dei dati (DLP) dell'endpoint nel dispositivo corrente.                                  |


### <a name="document-operations"></a>Operazioni relative ai documenti

| API | Descrizione |
|-----|-------------|
| [DlpNotifyPreOpenDocument](endpointdlp-dlpnotifypreopendocument.md) | Fornisce al sistema informazioni su un documento prima dell'avvio dell'operazione di apertura. |
| [DlpNotifyPostOpenDocument](endpointdlp-dlpnotifypostopendocument.md) | Fornisce al sistema informazioni su un documento dopo il completamento dell'operazione di apertura.  |
| [DlpNotifyCloseDocument](endpointdlp-dlpnotifyclosedocument.md)                       | Fornisce al sistema informazioni su un documento prima che venga avviata l'operazione di chiusura del documento.                                  |
| [DlpNotifyPreOpenDocumentFile](endpointdlp-dlpnotifypreopendocumentfile.md)                         | Fornisce al sistema informazioni su un documento prima dell'avvio dell'operazione di apertura.  |
| [DlpNotifyPostOpenDocumentFile](endpointdlp-dlpnotifypostopendocumentfile.md)                       | Fornisce al sistema informazioni su un documento dopo il completamento dell'operazione di apertura.                                  |
| [DlpNotifyCloseDocumentFile](endpointdlp-dlpnotifyclosedocumentfile.md)                       | Fornisce al sistema informazioni su un documento prima che venga avviata l'operazione di chiusura del documento.                                  |

### <a name="save-as-operations"></a>Salvare come operazioni
| API | Descrizione |
|-----|-------------|
| [DlpNotifyPreSaveAsDocument](endpointdlp-dlpnotifypresaveasdocument.md)                       | Fornisce al sistema informazioni su un documento prima che venga avviata un'operazione di salvataggio con nome.                                  |
| [DlpNotifyPostSaveAsDocument](endpointdlp-dlpnotifypostsaveasdocument.md)                       | Fornisce al sistema informazioni su un documento dopo il completamento dell'operazione di salvataggio con nome.                                  |


### <a name="drag-and-drop-operations"></a>Operazioni di trascinamento della selezione

| API | Descrizione |
|-----|-------------|
| [DlpNotifyEnterDropTarget](endpointdlp-dlpnotifyenterdroptarget.md)                       | Fornisce al sistema informazioni su un documento quando viene immessa una destinazione di rilascio.                                  |
| [DlpNotifyLeaveDropTarget](endpointdlp-dlpnotifyleavedroptarget.md)                       | Fornisce al sistema informazioni su un documento quando un obiettivo di rilascio viene chiuso.                                  |
| [DlpNotifyPreDragDrop](endpointdlp-dlpnotifypredragdrop.md)                         | Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di trascinamento della selezione.  |
| [DlpNotifyPostDragDrop](endpointdlp-dlpnotifypostdragdrop.md)                         | Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione di trascinamento della selezione.  |


### <a name="clipboard-operations"></a>operazioni relative agli Appunti

| API | Descrizione |
|-----|-------------|
| [DlpNotifyPreCopyToClipboard](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di copia negli Appunti.  |
| [DlpNotifyPostCopyToClipboard](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione di copia negli Appunti.  |
| [DlpNotifyPrePasteFromClipboard](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | Fornisce al sistema informazioni su un documento prima che venga avviata un'operazione Incolla dagli Appunti.  |
| [DlpNotifyPostPasteFromClipboard](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione Incolla dagli Appunti.                                  |
| [DlpNotifyPostStashClipboard](endpointdlp-dlpnotifypoststashclipboard.md)                       | Fornisce al sistema informazioni sullo stato dopo il completamento di un'operazione di stash clipboard.                                  |
| [DlpNotifyPreStashClipboard](endpointdlp-dlpnotifyprestashclipboard.md)                       | Notifica al sistema prima che venga avviata un'operazione di stash clipboard.                                  |
| [DlpMustPasteFromSystemClipboard](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | Determina se l'app deve eseguire il pull dei dati dagli Appunti di sistema anziché dalla cache interna.                                  |

### <a name="print-operations"></a>Operazioni di stampa

| API | Descrizione |
|-----|-------------|
| [DlpNotifyPrePrint](endpointdlp-dlpnotifypreprint.md)                         | Fornisce al sistema informazioni su un documento prima che venga avviata un'operazione di stampa.  |
| [DlpNotifyPostStartPrint](endpointdlp-dlpnotifypoststartprint.md)                       | Fornisce al sistema informazioni su un documento dopo l'avvio di un'operazione di stampa.                                  |
| [DlpNotifyPostPrint](endpointdlp-dlpnotifypostprint.md)                       | Fornisce al sistema informazioni su un documento al termine di un'operazione di stampa.                                  |

## <a name="endpoint-dlp-example-header"></a>Intestazione di esempio DLP dell'endpoint

Poiché l'intestazione DLP dell'endpoint non è inclusa nel Windows SDK, è necessario creare manualmente il file di intestazione per ottenere le firme API da usare nell'implementazione. Per praticità, viene fornito codice di esempio che è possibile copiare e incollare nell'applicazione. Oltre alle dichiarazioni di funzione, questo elenco di codice definisce anche costanti utili come le informazioni sul controllo delle versioni e i percorsi delle chiavi del Registro di sistema.

```cpp
//
// EndpointDlp DLL name containing the Endpoint DLP API
//

#define ENDPOINTDLP_DLL_NAME L"EndpointDlp.dll"

//
// Windows Defender registry key under HKLM where some Endpoint DLP settings are stored
//

#define ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"SOFTWARE\\Microsoft\\Windows Defender"

//
// EndpointDlp.dll install location can be obtained from the registry under the following HKLM key
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY

//
// EndpointDlp.dll install location is stored under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in the following registry value
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE L"InstallLocation"

//
// On x64 platforms, concatanate the following directory to obtain the x86 version of EndpointDlp.dll
//

#define ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX L"x86"

//
// Endpoint DLP enabled flag can be found under the following HKLM key
//

#define ENDPOINTDLP_ENABLED_FLAG_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"\\Features"

//
// Endpoint DLP enabled flag can be found under ENDPOINTDLP_ENABLED_REGKEY in the following registry value
//

#define ENDPOINTDLP_ENABLED_FLAG_REGVALUE L"SenseDlpEnabled"


#define DLP_DOCUMENT_INFO_V_1 0x1     

#define DLP_DOCUMENT_INFO_V_LATEST DLP_DOCUMENT_INFO_V_1


//
//  Enlightened app enforcement capablities.
//

typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, // No enforcement, DLP enforces operation.
    DlpAppEnforceLevelNotify,   // App send notifications on operation, DLP enforces operation.
    DlpAppEnforceLevelPrevent,  // Currently not supported (App allows or blocks operation, DLP enforces warning, eventing and UI). 
    DlpAppEnforceLevelFull,     // Currently not supported (App handles all enforcement (blocks operation, enforces warning, UI), DLP will only handle auditing.)
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;

typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
    
//
//  The stucture describes the enforcement level for each operation.
//
    
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;


/*
Function description:
     The application calls this functio to declares the enforcement level for each operation.

Parameters:
    _In_ DWORD Count - Number of operations. 
    _In_reads_opt_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL* OperationEnforcement - Array indicating operations
    supported by the application and enforcement level:
        DlpAppEnforceLevelNone - No enforcement, DLP enforces operation.
        DlpAppEnforceLevelNotify -  App send notifications on operation, DLP enforces operation.

Return:
    S_OK - Function completed successfully.
    E_INVALIDARG - Invalid parameters passed to function.
    E_OUTOFMEMORY - Memory allocation failed.
    E_XXX - Varius error codes.
*/       
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);


/*
Function description:
    Returns the version of the enforcement API.
    MajorVersion indicates a new interfaces/API.
    MinorVersion indicates changes to existing interfaces/API-s.
   
Parameters:
    None.

Return:
    S_OK - Function completed successfully
    E_XXX - Varius error codes.
*/
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);


typedef struct _DLP_DOCUMENT_INFO {

    //
    //  Information version. Always set it to DLP_DOCUMENT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Original path of the document.
    //  
    
    LPCWSTR PersistentFileName;

    //
    //  Path to the real backing file.
    //
    
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;

//
//  Post operation status information.
//
    
#define DLP_POSTOP_STATUS_V_1 0x1     
        
#define DLP_POSTOP_STATUS_V_LATEST DLP_POSTOP_STATUS_V_1;
    
       
typedef struct _DLP_POSTOP_STATUS {

    //
    //  Information version. Always set it to DLP_POSTOP_STATUS_V_LATEST
    //
    
    DWORD Version;

    //
    //  Set to TRUE if app's operation succeeded, FALSE otherwise. 
    //
    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS;    


#define DLP_PRINT_INFO_V_1 0x1     
    
#define DLP_PRINT_INFO_V_LATEST DLP_PRINT_INFO_V_1;

typedef struct _DLP_PRINT_INFO {

    //
    //  Information version. Always set it to DLP_PRINT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Destination printer.
    //
    
    LPCWSTR PrinterName;

    //
    //  Print job name.
    //
    
    LPCWSTR JobName;

    //
    //  Output file, if printing to file.
    //

    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;

    
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreStashClipboard();
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
    
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 


```


