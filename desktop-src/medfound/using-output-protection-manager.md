---
description: 'Altre informazioni su: Uso di Output Protection Manager'
ms.assetid: 01edc17e-e71c-4772-a03c-09c9a2b8400f
title: Uso di Output Protection Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e37dd548603a6f9d7769a9e724df3477e2fcde
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475517"
---
# <a name="using-output-protection-manager"></a>Uso di Output Protection Manager

Questo argomento descrive come usare Output Protection Manager (OPM) per proteggere il contenuto video durante il viaggio su un connettore fisico a un dispositivo di visualizzazione. In questo argomento sono incluse le sezioni seguenti:

-   [Output video](#video-outputs)
-   [Inizializzazione di una sessione OPM](#initializing-an-opm-session)
-   [Invio di richieste di stato OPM](#sending-opm-status-requests)
-   [Invio di comandi OPM](#sending-opm-commands)
-   [Gestione di un output video disabilitato](#sending-opm-commands)
-   [Uso di HDCP per proteggere il contenuto](#using-hdcp-to-protect-content)

Premium contenuto video viene in genere crittografato per proteggerlo da duplicazioni non autorizzate. Naturalmente, il video deve essere decrittografato prima di essere visualizzato. I fotogrammi decrittografati e non compressi devono quindi essere trasmessi attraverso un connettore fisico al dispositivo di visualizzazione. I provider di contenuti possono richiedere che i fotogrammi video siano protetti a questo punto, mentre attraversano il connettore fisico.

A questo scopo sono disponibili vari meccanismi di protezione, tra cui High-Bandwidth HdCP (Digital protezione del contenuto) e DisplayPort protezione del contenuto (DPCP) per gli output digitali; e Copy Generation Management System - Analog (CGMS-A) per output analoghi. In genere, questi meccanismi comportano la crittografia o l'assemblaggio del segnale prima che venga visualizzato.

OPM consente a un'applicazione di applicare meccanismi di protezione del contenuto nell'output video. Usando OPM, l'applicazione invia comandi e richieste di stato al driver di grafica tramite un canale sicuro attendibile. OPM consente a un'applicazione di:

-   Verificare che un driver di grafica sia stato firmato da Microsoft.
-   Configurare un canale di comunicazione attendibile con il driver.
-   Applicare meccanismi di protezione del contenuto all'output fisico.

OPM sostituisce Certified Output Protection Protcol (COPP) e usa un'API simile. Per compatibilità con le versioni precedenti, l'interfaccia OPM può emulare l'interfaccia COPP. Le differenze tra OPM e COPP includono quanto segue:

-   OPM usa certificati X.509, mentre COPP usa un formato di certificato proprietario.
-   OPM supporta i ripetitori HDCP.
-   Le applicazioni che usano OPM non devono analizzare i messaggi di rinnovo del sistema HDCP(SPM).
-   È possibile usare OPM quando la visualizzazione grafica usa la modalità di clonazione. COPP non supporta la modalità di clonazione.

Se l'applicazione usa il percorso multimediale protetto (PMP) per riprodurre il contenuto video, non è necessario usare l'API OPM, perché il PMP effettua tutte le chiamate OPM necessarie. L'API OPM è disponibile per le applicazioni che non usano il PMP.

OPM è disponibile in Windows Vista e versioni successive, ma l'API non è stata resa pubblica fino Windows 7. Per usare OPM in un'applicazione, è necessario disporre delle intestazioni e dei file di libreria di Windows 7 SDK. Non è necessario ridistribuire le DLL per usare OPM in Windows Vista o Windows Server 2008.

## <a name="video-outputs"></a>Output video

Una scheda grafica può avere più di un output fisico, ognuno con le proprie funzionalità. Prima di riprodurre contenuto protetto, un'applicazione deve impostare i meccanismi di protezione appropriati in ogni output video associato alla scheda grafica che visualizza il video. I meccanismi di protezione da applicare dipendono dalle regole di utilizzo per il contenuto.

Ogni output video è rappresentato da un'istanza [**dell'interfaccia IOPMVideoOutput.**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) È possibile usare un dispositivo Direct3D o handle di monitoraggio per ottenere gli output video.

Uso di un dispositivo Direct3D:

1.  Ottenere il **puntatore IDirect3DDevice9** per il dispositivo Direct3D che l'applicazione userà per creare superfici in cui contenere i fotogrammi video.
2.  Chiamare la [**funzione OPMGetVideoOutputsFromIDirect3DDevice9Object.**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) Questa funzione alloca una matrice di [**puntatori IOPMVideoOutput,**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) uno per ogni output.

Uso degli handle di monitoraggio:

1.  Chiamare **EnumDisplayMonitors** per ottenere gli handle **HMONITOR** che corrispondono alla finestra video. È possibile associare più monitor alla stessa finestra, pertanto è possibile ottenere diversi **handle HMONITOR.**
2.  Per ogni handle di monitoraggio, chiamare [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor). Questa funzione alloca una matrice di [**puntatori IOPMVideoOutput,**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) uno per ogni output.

## <a name="initializing-an-opm-session"></a>Inizializzazione di una sessione OPM

Prima che l'applicazione invii comandi OPM o richieste di stato, deve verificare che l'output video sia attendibile e stabilire una chiave di sessione. La chiave di sessione viene usata per firmare i dati s scambiati tra l'applicazione e il driver di grafica.

L'API OPM definisce un handshake che stabilisce l'attendibilità e imposta la chiave di sessione. È necessario eseguire questo handshake per ogni istanza [**dell'interfaccia IOPMVideoOutput,**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) come indicato di seguito:

1.  Chiamare [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization). Questo metodo recupera due parti di dati:
    -   Numero casuale generato dal driver. Questo numero verrà utilizzato per completare l'handshake.
    -   Catena di certificati X.509 del driver.
2.  Verificare che la catena di certificati sia stata firmata da Microsoft.
    > [!Note]  
    > La revoca del certificato non rientra nell'ambito di OPM.

     

3.  Ottenere la chiave pubblica del driver dalla catena di certificati.
4.  Generare una chiave di sessione AES a 128 bit.
5.  Generare due numeri casuali a 32 bit:

    -   Numero di sequenza iniziale per le richieste di stato OPM.
    -   Numero di sequenza iniziale per i comandi OPM.

    Questi numeri devono essere generati usando un generatore di numeri pseudocasuali sicuro dal punto di vista crittografico, ad esempio **CryptGenRandom.**

6.  Copiare il numero casuale del driver (ottenuto nel passaggio 1), la chiave di sessione e i due numeri di sequenza in una [**struttura OPM \_ ENCRYPTED \_ INITIALIZATION \_ PARAMETERS,**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) come descritto in [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization).
7.  Crittografare la struttura [**OPM \_ ENCRYPTED \_ INITIALIZATION \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) con RSAES-OAEP, usando la chiave pubblica del driver, disponibile nel certificato del driver.
8.  Chiamare [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization).

## <a name="sending-opm-status-requests"></a>Invio di richieste di stato OPM

Le richieste di stato OPM restituiscono informazioni sull'output video, ad esempio il tipo di connettore fisico e il livello di protezione corrente. Per un elenco dei tipi di richiesta, vedere [Richieste di stato OPM.](opm-status-requests.md)

Per inviare una richiesta di stato, seguire questa procedura.

1.  Inizializzare [**una struttura OPM GET INFO \_ \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) come illustrato nella tabella seguente.

    | Membro               | Descrizione                                                                                                                                                                                                                                                                                                                                                                 |
    |----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **Omac**             | Ignorare questo campo per il momento.                                                                                                                                                                                                                                                                                                                                                    |
    | **rnRandomNumber**   | Numero casuale a 128 bit sicuro dal punto di vista crittografico. Ogni volta che si effettua una richiesta di stato, generare sempre un nuovo numero casuale, anche se si effettua la stessa richiesta. Archiviare il numero in una variabile, perché sarà necessario fare riferimento a esso in un secondo momento.                                                                                                                             |
    | **guidInformation**  | GUID che identifica la richiesta di stato. Per un elenco delle richieste di stato, vedere [Richieste di stato OPM.](opm-status-requests.md)                                                                                                                                                                                                                                               |
    | **ulSequenceNumber** | Numero di sequenza. Per la prima richiesta di stato, usare il numero di sequenza iniziale specificato nel metodo [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) (passaggio 5 dell'inizializzazione di una sessione [OPM).](#initializing-an-opm-session) Ogni volta che si effettua un'altra richiesta di stato, incrementare questo numero di 1. |
    | **abParameters**     | Matrice di byte che contiene dati di input aggiuntivi per la richiesta. Il formato dei dati di input è elencato nell'argomento di riferimento per ogni richiesta di stato.                                                                                                                                                                                                                    |
    | **cbParametersSize** | Dimensione dei dati validi nella **matrice abParameters.** Il contenuto del resto della matrice non è definito.                                                                                                                                                                                                                                                              |

    

     

2.  Calcolare il codice MAC CBC a una chiave (OMAC-1) per calcolare un hash per il blocco di dati visualizzato dopo il membro **omac** e quindi impostare il membro **omac** su questo valore. Vedere [Il codice di esempio di OPM](opm-example-code.md).
3.  Chiamare il [**metodo IOPMVideoOutput::GetInformation.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) Passare un puntatore alla struttura [**OPM \_ GET INFO \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) e un puntatore a una [**struttura OPM REQUESTED \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) La risposta del driver viene scritta nella **struttura OPM \_ REQUESTED \_ INFORMATION.**
    -   Il **membro omac** di questa struttura contiene un OMAC calcolato per i dati che seguono questo membro.
    -   Il **membro abRequestedInformation** è una matrice di byte che contiene i dati di output per la risposta. Il formato dei dati di output è elencato nell'argomento di riferimento per ogni richiesta di stato.
4.  Calcolare un OMAC per la [**struttura OPM \_ REQUESTED \_ INFORMATION,**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) senza includere il **membro omac.** Verificare che OMAC corrisponda al valore nel **membro omac.**
5.  Assicurarsi che il **membro cbRequestedInformationSize** della [**struttura OPM REQUESTED \_ \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) dia le dimensioni corrette per i dati di output. Ad esempio, i dati di output per la query [**OPM \_ GET CONNECTOR \_ \_ TYPE**](opm-get-connector-type.md) sono una [**struttura OPM STANDARD \_ \_ INFORMATION,**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) quindi il valore di **cbRequestedInformationSize** deve essere `sizeof(OPM_STANDARD_INFORMATION)` .
6.  Eseguire il cast **del membro abRequestedInformation** della [**struttura OPM REQUESTED \_ \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) alla struttura dei dati di output corretta. Ad esempio, se la richiesta di stato è [**OPM \_ GET CONNECTOR \_ \_ TYPE,**](opm-get-connector-type.md)eseguire il cast di **abRequestedInformation** a [**una struttura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)
7.  Assicurarsi che il **membro rnRandomNumber** della struttura dei dati di output corrisponda al **valore di rnRandomNumber** del passaggio 1.
8.  Controllare il **membro ulStatusFlags della** struttura dei dati di output, come descritto in [Gestione di un output video disabilitato.](#handling-a-disabled-video-output)

Se uno dei controlli nei passaggi da 5 a 8 ha esito negativo, l'applicazione deve interrompere la visualizzazione del contenuto protetto.

## <a name="sending-opm-commands"></a>Invio di comandi OPM

I comandi OPM vengono usati per impostare il livello di protezione e altre impostazioni nell'output video. L'invio di un comando OPM è simile all'invio di una richiesta di stato, ad eccezione del fatto che non sono presenti dati di risposta dal driver. Per un elenco di comandi, vedere [Comandi OPM.](opm-commands.md)

Per inviare un comando OPM, seguire questa procedura.

1.  Compilare una [**struttura OPM \_ CONFIGURE \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) come illustrato nella tabella seguente.

    | Membro                | Descrizione                                                                                                                                                                                                                                                                                                                                                   |
    |-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **Omac**              | Ignorare questo campo per il momento.                                                                                                                                                                                                                                                                                                                                      |
    | **guidSetting**       | GUID che identifica il comando. Per un elenco di comandi, vedere [Comandi OPM.](opm-commands.md)                                                                                                                                                                                                                                                             |
    | **ulSequenceNumber**  | Numero di sequenza. Per il primo comando, usare il numero di sequenza iniziale specificato nel metodo [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) (passaggio 5 dell'inizializzazione di una sessione [OPM).](#initializing-an-opm-session) Ogni volta che si invia un altro comando, incrementare questo numero di 1. |
    | **abParameters**      | Matrice di byte che contiene dati di input aggiuntivi per il comando. Il formato dei dati di input è elencato nell'argomento di riferimento per ogni comando.                                                                                                                                                                                                             |
    | **cbSettingDataSize** | Dimensione dei dati validi nella **matrice abParameters.** Il contenuto del resto della matrice non è definito.                                                                                                                                                                                                                                                |

    

     

2.  Calcolare un OMAC per il blocco di dati visualizzato dopo il membro **omac** e quindi impostare il membro **omac** su questo valore.
3.  Chiamare [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).

Per la maggior parte dei comandi, esiste una richiesta di stato corrispondente che restituisce lo stato del comando. Ad esempio, il [**comando OPM \_ SET PROTECTION \_ \_ LEVEL**](opm-set-protection-level.md) imposta il livello di protezione e il comando [**OPM GET VIRTUAL PROTECTION \_ \_ \_ \_ LEVEL**](opm-get-virtual-protection-level.md) ottiene il livello di protezione corrente.

## <a name="handling-a-disabled-video-output"></a>Gestione di un output video disabilitato

Un output video potrebbe disabilitarsi in qualsiasi momento per impedire l'uso non autorizzato di contenuti video. Ciò può verificarsi perché un meccanismo di protezione smette di funzionare, perché il driver rileva manomissioni o perché lo schermo è stato disconnesso dal connettore fisico. Quando un output video è disabilitato, non viene visualizzato alcun fotogramma video.

Mentre la protezione del contenuto è abilitata, un'applicazione deve eseguire periodicamente (almeno una volta ogni 2 secondi) i passaggi seguenti.

1.  Chiamare [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) per inviare la richiesta di stato [**OPM \_ GET ACTUAL PROTECTION \_ \_ \_ LEVEL**](opm-get-actual-protection-level.md) o [**OPM GET VIRTUAL \_ PROTECTION \_ \_ \_ LEVEL.**](opm-get-virtual-protection-level.md) I dati restituiti per entrambi i comandi sono una [**struttura OPM \_ STANDARD \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)
2.  Controllare il **membro ulInformation** della [**struttura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Questo membro contiene un flag che indica se la protezione del contenuto è ancora abilitata. Se la protezione del contenuto è disattivata, interrompere immediatamente la riproduzione del video.
3.  Se la protezione del contenuto è impostata su on, controllare il **membro ulStatusFlags** della [**struttura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Se non è impostato alcun flag, l'output video funziona correttamente. In caso contrario, l'output video è disabilitato.

I flag seguenti sono definiti per **ulStatusFlags**.




| Flag | Descrizione | 
|------|-------------|
| <strong>OPM_STATUS_LINK_LOST</strong> | La protezione dell'output ha smesso di funzionare per qualche motivo. Ad esempio, il dispositivo di visualizzazione potrebbe essere scollegato dal conntector. Arrestare la riproduzione e disattivare tutti i meccanismi di protezione dell'output. | 
| <strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong> | L'applicazione deve ristabilire la sessione OPM. Rispondere come segue:<ol><li>Arrestare la riproduzione.</li><li>Disattivare tutti i meccanismi di protezione.</li><li>Rilasciare <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput"><strong>l'interfaccia IOPMVideoOutput.</strong></a></li><li>Ricreare tutte le superfici video.</li><li>Creare un nuovo oggetto OPM e tentare di ristabilire la protezione del contenuto. Se l'operazione non riesce, visualizzare un messaggio di errore all'utente. Non riprodurre altri contenuti video.</li></ol> | 
| <strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong> | Questo flag si applica solo quando si usa HDCP e indica la presenza di un dispositivo HDCP revocato. Arrestare la riproduzione e disattivare tutti i meccanismi di protezione nell'output video. Quando questo flag è impostato, <strong>viene OPM_STATUS_LINK_LOST</strong> anche il flag . | 
| <strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong> | Il driver ha rilevato manomissioni. Arrestare la riproduzione e non riprodurre altri video usando questo output video. È anche consigliabile interrompere l'uso di qualsiasi altro output video, perché il sistema potrebbe essere compromesso. | 




 

## <a name="using-hdcp-to-protect-content"></a>Uso di HDCP per proteggere il contenuto

Questa sezione descrive come abilitare la protezione dell'output HDCP tramite OPM. Ecco una descrizione generale dei passaggi che l'applicazione deve eseguire. I dettagli sono disponibili più avanti in questa sezione.

1.  L'applicazione potrebbe dover fornire un SRM all'output video. Il meccanismo per la ricezione di SPM non rientra nell'ambito dell'interfaccia OPM. Ad esempio, gli SPM possono essere recapitati come parte di un flusso di trasmissione.
2.  L'applicazione abilita la protezione dell'output HDCP.
3.  L'applicazione riproduce il contenuto video. Periodicamente, l'applicazione esegue il polling del driver per verificare che HDCP sia installato.
4.  Al termine della riproduzione, l'applicazione disattiva HDCP.

### <a name="setting-the-srm"></a>Impostazione di SRM

Per impostare SRM, seguire questa procedura.

1.  Inizializzare [**una struttura OPM SET \_ \_ HDCP \_ SRM \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) con il numero di versione SRM.
2.  Archiviare SRM in una variabile.
3.  Inviare [**un comando OPM SET \_ \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) all'output video. Usare la procedura descritta in [Invio di comandi OPM](#sending-opm-commands).
    -   Il **membro abParameters** della struttura [**OPM CONFIGURE \_ \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) contiene la [**struttura OPM SET \_ \_ HDCP \_ SRM \_ PARAMETERS.**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)
    -   Il *parametro pbAdditionalParameters* del metodo [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) punta alla variabile che contiene SRM.
4.  Inviare una [**richiesta di stato OPM GET \_ CURRENT \_ \_ HDCP \_ SRM \_ VERSION**](opm-get-current-hdcp-srm-version.md) all'output video. Usare la procedura descritta in [Invio di richieste di stato OPM](#sending-opm-status-requests). Questa richiesta di stato non contiene dati di input, quindi il contenuto del membro **abParameters** della [**struttura OPM \_ GET INFO \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) non è definito.
5.  Quando il [**metodo IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) viene restituito, la matrice **abRequestedInformation** nella struttura [**OPM REQUESTED \_ \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) contiene una [**struttura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Il **membro ulInformation** di questa struttura contiene il numero di versione dell'oggetto SRM corrente. Questo valore deve essere uguale al valore del passaggio 2.

### <a name="enabling-hdcp"></a>Abilitazione di HDCP

Per abilitare HDCP, seguire questa procedura.

1.  Inizializzare [**una struttura OPM SET PROTECTION \_ LEVEL \_ \_ \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) con i valori seguenti:
    -   **ulProtectionType**  =  **OPM \_ TIPO \_ DI \_ PROTEZIONE HDCP**
    -   **ulProtectionLevel**  =  **OPM \_ HDCP \_ ON**
    -   **Riservato** = 0
    -   **Reserved2** = 0
2.  Inviare un [**comando OPM \_ SET PROTECTION \_ \_ LEVEL.**](opm-set-protection-level.md) I dati di input nella **matrice abParameters** sono la [**struttura OPM SET PROTECTION LEVEL \_ \_ \_ \_ PARAMETERS.**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)
3.  Inviare una [**richiesta di stato OPM GET VIRTUAL \_ PROTECTION \_ \_ \_ LEVEL**](opm-get-virtual-protection-level.md) per verificare se HDCP è abilitato. I primi 4 byte del **membro abParameters** della struttura [**OPM \_ GET INFO \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) contengono il **valore OPM PROTECTION TYPE \_ \_ \_ HDCP**.

Quando il [**metodo GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) viene restituito, la matrice **abRequestedInformation** nella [**struttura OPM REQUESTED \_ \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) contiene una [**struttura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Il **membro ulInformation** di questa struttura contiene un valore dell'enumerazione [**OPM \_ HDCP PROTECTION \_ \_ LEVEL.**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) Se il valore è uguale a **OPM \_ HDCP \_ ON,** significa che HDCP è abilitato. In caso contrario, ripetere i passaggi da 1 a 2 fino a quando non viene abilitato HDCP o non si verifica un errore. Ricordarsi di incrementare il numero di sequenza e generare un nuovo numero casuale ogni volta.

In genere sono necessari da 100 a 200 millisecondi per abilitare HDCP, ma può richiedere più tempo. Non presupporre che HDCP sia abilitato fino a quando non è stato verificato.

Al termine della riproduzione del contenuto protetto da parte dell'applicazione, disattivare HDCP. I passaggi sono gli stessi per l'abilitazione di HDCP, ma nel passaggio 1 impostare **ulProtectionLevel** su **OPM \_ HDCP \_ OFF**.

> [!Note]  
> Non abilitare HDCP se il tipo di connettore è **OPM \_ CONNECTOR TYPE \_ \_ DISPLAYPORT \_ EMBEDDED**. Vedere Flag [**del tipo di connettore OPM.**](opm-connector-type-flags.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Output Protection Manager](output-protection-manager.md)
</dt> </dl>

 

 



