---
description: 'Ulteriori informazioni su: utilizzo di output Protection Manager'
ms.assetid: 01edc17e-e71c-4772-a03c-09c9a2b8400f
title: Utilizzo di output Protection Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bf4def3b0575dd706ae5f0c62924b6f1375a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310174"
---
# <a name="using-output-protection-manager"></a>Utilizzo di output Protection Manager

Questo argomento descrive come usare output Protection Manager (OPM) per proteggere il contenuto video mentre passa su un connettore fisico a un dispositivo di visualizzazione. In questo argomento sono incluse le sezioni seguenti:

-   [Output video](#video-outputs)
-   [Inizializzazione di una sessione di OPM](#initializing-an-opm-session)
-   [Invio di richieste di stato di OPM](#sending-opm-status-requests)
-   [Invio di comandi OPM](#sending-opm-commands)
-   [Gestione di un output video disabilitato](#sending-opm-commands)
-   [Uso di HDCP per proteggere il contenuto](#using-hdcp-to-protect-content)

Il contenuto video Premium viene in genere crittografato per proteggerlo da duplicati non autorizzati. Naturalmente, il video deve essere decrittografato prima di essere visualizzato. I frame decrittografati e non compressi devono quindi passare attraverso un connettore fisico al dispositivo di visualizzazione. I provider di contenuti possono richiedere che i fotogrammi video siano protetti a questo punto, mentre si spostano sul connettore fisico.

A questo scopo esistono diversi meccanismi di protezione, tra cui High-Bandwidth Digital protezione del contenuto (HDCP) e DisplayPort protezione del contenuto (DPCP) per gli output digitali; e Copy Generation Management System-Analog (CGMS-A) per gli output analoghi. In genere, questi meccanismi comportano la crittografia o la rimescolanza del segnale prima che venga visualizzato.

OPM consente a un'applicazione di applicare meccanismi di protezione del contenuto nell'output del video. Con l'uso di OPM, l'applicazione invia comandi e richieste di stato al driver di grafica tramite un canale sicuro attendibile. OPM consente a un'applicazione di:

-   Verificare che un driver di grafica sia stato firmato da Microsoft.
-   Configurare un canale di comunicazione attendibile con il driver.
-   Applicare i meccanismi di protezione del contenuto nell'output fisico.

OPM sostituisce Certified Output Protection Protocol (COPP) e usa un'API simile. Per compatibilità con le versioni precedenti, l'interfaccia OPM può emulare l'interfaccia COPP. Di seguito sono riportate le differenze tra OPM e COPP:

-   OPM USA certificati X. 509, mentre COPP usa un formato di certificato proprietario.
-   OPM supporta i ripetitori HDCP.
-   Le applicazioni che usano OPM non devono analizzare i messaggi di rinnovabilità del sistema HDCP (SRM).
-   È possibile usare OPM quando la visualizzazione grafica usa la modalità di clonazione. COPP non supporta la modalità di clonazione.

Se l'applicazione usa il percorso multimediale protetto (PMP) per riprodurre contenuti video, non è necessario usare l'API di OPM, perché il PMP esegue tutte le chiamate OPM richieste. L'API OPM è disponibile per le applicazioni che non usano il PMP.

OPM è disponibile in Windows Vista e versioni successive, ma l'API non è stata resa pubblica fino a Windows 7. Per usare OPM in un'applicazione, è necessario avere le intestazioni e i file di libreria di Windows 7 SDK. Non è necessario ridistribuire le dll per l'uso di OPM in Windows Vista o Windows Server 2008.

## <a name="video-outputs"></a>Output video

Una scheda grafica può avere più di un output fisico, ognuno con le proprie funzionalità. Prima che un'applicazione riproduca contenuto protetto, deve impostare i meccanismi di protezione appropriati in ogni output video associato alla scheda grafica che visualizzerà il video. I meccanismi di protezione da applicare dipenderanno dalle regole di utilizzo per il contenuto.

Ogni output video è rappresentato da un'istanza dell'interfaccia [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) . Per ottenere gli output video, è possibile usare un dispositivo Direct3D o un handle di monitoraggio.

Uso di un dispositivo Direct3D:

1.  Ottenere il puntatore **IDirect3DDevice9** per il dispositivo Direct3D che l'applicazione userà per creare le superfici per i frame video.
2.  Chiamare la funzione [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) . Questa funzione alloca una matrice di puntatori [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) , uno per ogni output.

Utilizzo di handle di monitoraggio:

1.  Chiamare **EnumDisplayMonitors** per ottenere gli handle **HMONITOR** che corrispondono alla finestra del video. È possibile associare diversi monitoraggi alla stessa finestra, in modo che si possano ottenere diversi handle **HMONITOR** .
2.  Per ogni handle di monitoraggio, chiamare [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor). Questa funzione alloca una matrice di puntatori [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) , uno per ogni output.

## <a name="initializing-an-opm-session"></a>Inizializzazione di una sessione di OPM

Prima che l'applicazione invii comandi o richieste di stato OPM, è necessario verificare che l'output del video sia attendibile e stabilire una chiave di sessione. La chiave della sessione viene utilizzata per firmare i dati scambiati tra l'applicazione e il driver di grafica.

L'API OPM definisce un handshake che stabilisce l'attendibilità e imposta la chiave della sessione. È necessario eseguire questo handshake per ogni istanza dell'interfaccia [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) , come indicato di seguito:

1.  Chiamare [**IOPMVideoOutput:: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization). Questo metodo recupera due tipi di dati:
    -   Numero casuale generato dal driver. Questo numero verrà usato per completare l'handshake.
    -   Catena di certificati X. 509 del driver.
2.  Verificare che la catena di certificati sia stata firmata da Microsoft.
    > [!Note]  
    > La revoca dei certificati esula dall'ambito di OPM.

     

3.  Ottenere la chiave pubblica del driver dalla catena di certificati.
4.  Generare una chiave di sessione AES a 128 bit.
5.  Generare due numeri casuali a 32 bit:

    -   Numero di sequenza iniziale per le richieste di stato di OPM.
    -   Numero di sequenza iniziale per i comandi di OPM.

    Questi numeri devono essere generati usando un generatore di numeri pseudo-casuali sicuri crittograficamente, ad esempio **CryptGenRandom**.

6.  Copiare il numero casuale del driver (ottenuto nel passaggio 1), la chiave della sessione e i due numeri di sequenza in una struttura di [**\_ \_ \_ parametri di inizializzazione crittografata di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) , come descritto in [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization).
7.  Crittografare la struttura dei [**\_ \_ \_ parametri di inizializzazione crittografata di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) con RSAES-OAEP, utilizzando la chiave pubblica del driver, disponibile nel certificato del driver.
8.  Chiamare [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization).

## <a name="sending-opm-status-requests"></a>Invio di richieste di stato di OPM

Le richieste di stato di OPM restituiscono informazioni sull'output video, ad esempio il tipo di connettore fisico e il livello di protezione corrente. Per un elenco di tipi di richiesta, vedere [richieste di stato di OPM](opm-status-requests.md).

Per inviare una richiesta di stato, seguire questa procedura.

1.  Inizializzare una struttura del [**\_ \_ \_ parametro OPM Get Info**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) come illustrato nella tabella seguente.

    | Membro               | Descrizione                                                                                                                                                                                                                                                                                                                                                                 |
    |----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **OMAC**             | Ignorare questo campo per il momento.                                                                                                                                                                                                                                                                                                                                                    |
    | **rnRandomNumber**   | Numero casuale a 128 bit a crittografia sicura. Quando si effettua una richiesta di stato, generare sempre un nuovo numero casuale, anche se si esegue la stessa richiesta. Archiviare il numero in una variabile, perché sarà necessario farvi riferimento in un secondo momento.                                                                                                                             |
    | **guidInformation**  | GUID che identifica la richiesta di stato. Per un elenco delle richieste di stato, vedere [richieste di stato di OPM](opm-status-requests.md).                                                                                                                                                                                                                                               |
    | **ulSequenceNumber** | Numero di sequenza. Per la prima richiesta di stato, usare il numero di sequenza iniziale specificato nel metodo [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) (passaggio 5 dell' [inizializzazione di una sessione di OPM](#initializing-an-opm-session)). Ogni volta che si effettua un'altra richiesta di stato, incrementare il numero di 1. |
    | **abParameters**     | Matrice di byte che contiene dati di input aggiuntivi per la richiesta. Il formato dei dati di input è elencato nell'argomento di riferimento per ogni richiesta di stato.                                                                                                                                                                                                                    |
    | **cbParametersSize** | Dimensione dei dati validi nella matrice **abParameters** . Il contenuto del resto della matrice non è definito.                                                                                                                                                                                                                                                              |

    

     

2.  Calcolare l'elemento CBC MAC a una chiave (OMAC-1) per calcolare un hash per il blocco di dati visualizzato dopo il membro **OMAC** , quindi impostare il membro **OMAC** su questo valore. Vedere il [codice di esempio di OPM](opm-example-code.md).
3.  Chiamare il metodo [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) . Passare un puntatore alla struttura del [**\_ \_ \_ parametro OPM Get Info**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) e un puntatore a una struttura [**di \_ \_ informazioni richiesta da OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) . La risposta del driver viene scritta nella struttura **di \_ \_ informazioni richiesta da OPM** .
    -   Il membro **OMAC** di questa struttura contiene un OMAC calcolato per i dati che seguono questo membro.
    -   Il membro **abRequestedInformation** è una matrice di byte che contiene i dati di output per la risposta. Il formato dei dati di output è elencato nell'argomento di riferimento per ogni richiesta di stato.
4.  Calcolare un OMAC per la struttura delle [**\_ \_ informazioni richiesta da OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) , escluso il membro **OMAC** . Verificare che OMAC corrisponda al valore nel membro **OMAC** .
5.  Verificare che il membro **cbRequestedInformationSize** della struttura [**di \_ \_ informazioni richiesta da OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) fornisca la dimensione corretta per i dati di output. Ad esempio, i dati di output per la query del [**\_ \_ \_ tipo di connettore OPM Get**](opm-get-connector-type.md) sono una struttura di [**\_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) , quindi il valore di **cbRequestedInformationSize** deve essere `sizeof(OPM_STANDARD_INFORMATION)` .
6.  Eseguire il cast del membro **abRequestedInformation** della struttura di [**\_ \_ informazioni richiesta da OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) alla struttura dei dati di output corretta. Ad esempio, se la richiesta di stato è il [**\_ tipo di \_ connettore \_ OPM Get**](opm-get-connector-type.md), eseguire il cast di **abRequestedInformation** a una struttura di [**\_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .
7.  Verificare che il membro **rnRandomNumber** della struttura dei dati di output corrisponda al valore di **rnRandomNumber** del passaggio 1.
8.  Verificare il membro **ulStatusFlags** della struttura dei dati di output, come descritto in [gestione di un output video disabilitato](#handling-a-disabled-video-output).

Se uno dei controlli nei passaggi 5-8 ha esito negativo, l'applicazione deve interrompere la visualizzazione del contenuto protetto.

## <a name="sending-opm-commands"></a>Invio di comandi OPM

I comandi di OPM vengono usati per impostare il livello di protezione e altre impostazioni nell'output del video. L'invio di un comando OPM è simile all'invio di una richiesta di stato, ad eccezione del fatto che non sono presenti dati di risposta dal driver. Per un elenco di comandi, vedere [comandi di OPM](opm-commands.md).

Per inviare un comando OPM, seguire questa procedura.

1.  Compilare una struttura [**di \_ \_ parametri di configurazione di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) , come illustrato nella tabella seguente.

    | Membro                | Descrizione                                                                                                                                                                                                                                                                                                                                                   |
    |-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **OMAC**              | Ignorare questo campo per il momento.                                                                                                                                                                                                                                                                                                                                      |
    | **guidSetting**       | GUID che identifica il comando. Per un elenco di comandi, vedere [comandi di OPM](opm-commands.md).                                                                                                                                                                                                                                                             |
    | **ulSequenceNumber**  | Numero di sequenza. Per il primo comando, usare il numero di sequenza iniziale specificato nel metodo [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) (passaggio 5 dell' [inizializzazione di una sessione di OPM](#initializing-an-opm-session)). Ogni volta che si invia un altro comando, incrementare il numero di 1. |
    | **abParameters**      | Matrice di byte che contiene dati di input aggiuntivi per il comando. Il formato dei dati di input è elencato nell'argomento di riferimento per ogni comando.                                                                                                                                                                                                             |
    | **cbSettingDataSize** | Dimensione dei dati validi nella matrice **abParameters** . Il contenuto del resto della matrice non è definito.                                                                                                                                                                                                                                                |

    

     

2.  Calcolare un OMAC per il blocco di dati visualizzato dopo il membro **OMAC** , quindi impostare il membro **OMAC** su questo valore.
3.  Chiamare [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).

Per la maggior parte dei comandi, esiste una richiesta di stato corrispondente che restituisce lo stato del comando. Ad esempio, il comando [**OPM \_ set \_ Protection \_ Level**](opm-set-protection-level.md) imposta il livello di protezione e il comando [**OPM \_ get \_ virtual \_ Protection \_ Level**](opm-get-virtual-protection-level.md) ottiene il livello di protezione corrente.

## <a name="handling-a-disabled-video-output"></a>Gestione di un output video disabilitato

Un output video potrebbe disabilitare se stesso in qualsiasi momento per impedire l'uso non autorizzato del contenuto video. Questo problema può verificarsi perché un meccanismo di protezione smette di funzionare, perché il driver rileva la manomissione o perché la visualizzazione è stata disconnessa dal connettore fisico. Mentre un output video è disabilitato, non viene visualizzato alcun fotogramma video.

Quando la protezione del contenuto è abilitata, un'applicazione deve essere periodicamente (almeno una volta ogni 2 secondi) per eseguire i passaggi seguenti.

1.  Chiamare [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) per inviare la richiesta di stato del livello di [**\_ \_ protezione effettivo per il \_ \_ livello di protezione**](opm-get-actual-protection-level.md) o dell' [**OPM \_ get \_ virtual \_ Protection \_**](opm-get-virtual-protection-level.md) . I dati restituiti per entrambi i comandi sono una struttura di [**\_ \_ informazioni standard di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .
2.  Verificare il membro **ulInformation** della struttura [**di \_ \_ informazioni standard di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Questo membro contiene un flag che indica se la protezione del contenuto è ancora abilitata. Se la protezione del contenuto è disattivata, interrompere immediatamente la riproduzione del video.
3.  Se la protezione del contenuto è attiva, controllare il membro **ulStatusFlags** della struttura di [**\_ \_ informazioni standard di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Se non è impostato alcun flag, l'output del video funziona correttamente. In caso contrario, l'output del video è disabilitato.

I flag seguenti sono definiti per **ulStatusFlags**.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flag</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>OPM_STATUS_LINK_LOST</strong></td>
<td>La protezione dell'output ha smesso di funzionare per qualche motivo; ad esempio, il dispositivo di visualizzazione potrebbe essere scollegato da conntector. Arrestare la riproduzione e disattivare tutti i meccanismi di protezione dell'output.</td>
</tr>
<tr class="even">
<td><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></td>
<td>L'applicazione deve ristabilire la sessione di OPM. Rispondere come segue:
<ol>
<li>Arresta la riproduzione.</li>
<li>Disattivare tutti i meccanismi di protezione.</li>
<li>Rilasciare l'interfaccia <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput"><strong>IOPMVideoOutput</strong></a> .</li>
<li>Ricreare tutte le superfici video.</li>
<li>Creare un nuovo oggetto OPM e tentare di ristabilire la protezione del contenuto. Se l'operazione non riesce, visualizzare un messaggio di errore all'utente. Non riprodurre altri contenuti video.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></td>
<td>Questo flag si applica solo quando si usa HDCP e indica la presenza di un dispositivo HDCP revocato. Arrestare la riproduzione e disattivare tutti i meccanismi di protezione nell'output del video. Quando questo flag è impostato, viene impostato anche il flag <strong>OPM_STATUS_LINK_LOST</strong> .</td>
</tr>
<tr class="even">
<td><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></td>
<td>Il driver ha rilevato manomissioni. Arrestare la riproduzione e non riprodurre più video usando questo output video. È anche consigliabile interrompere l'uso di altri output video, perché il sistema potrebbe essere compromesso.</td>
</tr>
</tbody>
</table>



 

## <a name="using-hdcp-to-protect-content"></a>Uso di HDCP per proteggere il contenuto

Questa sezione descrive come abilitare la protezione dell'output HDCP con OPM. Ecco una descrizione generale dei passaggi che devono essere eseguiti dall'applicazione. I dettagli sono forniti più avanti in questa sezione.

1.  L'applicazione potrebbe dover fornire un SRM all'output del video. Il meccanismo per la ricezione di SRM non rientra nell'ambito dell'interfaccia OPM. Ad esempio, SRM potrebbe essere recapitato come parte di un flusso di broadcast.
2.  L'applicazione Abilita la protezione dell'output HDCP.
3.  L'applicazione riproduce il contenuto video. Periodicamente, l'applicazione esegue il polling del driver per verificare che HDCP sia attiva.
4.  Al termine della riproduzione, l'applicazione disattiva HDCP.

### <a name="setting-the-srm"></a>Impostazione di SRM

Per impostare SRM, seguire questa procedura.

1.  Inizializzare una struttura di [**\_ parametri del set di configurazione \_ HDCP \_ SRM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) con il numero di versione SRM.
2.  Archiviare SRM in una variabile.
3.  Inviare un comando [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) all'output del video. Usare la procedura descritta in [invio dei comandi di OPM](#sending-opm-commands).
    -   Il membro **abParameters** della struttura di [**configurazione dei \_ \_ parametri di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) contiene la struttura dei [**parametri di OPM \_ set \_ HDCP \_ MSR \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) .
    -   Il parametro *pbAdditionalParameters* del metodo [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) punta alla variabile che contiene SRM.
4.  Inviare una richiesta di stato della versione di un OPM per la [**\_ \_ \_ \_ \_ versione SRM corrente**](opm-get-current-hdcp-srm-version.md) all'output del video. Usare la procedura descritta in [invio di richieste di stato di OPM](#sending-opm-status-requests). Questa richiesta di stato non contiene dati di input, quindi il contenuto del membro **abParameters** della struttura del [**\_ parametro OPM Get \_ info \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) non è definito.
5.  Quando il metodo [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) restituisce, la matrice **abRequestedInformation** nella struttura [**di \_ \_ informazioni richiesta da OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) contiene una struttura di [**\_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Il membro **ulInformation** della struttura contiene il numero di versione dell'SRM corrente. Questo valore deve essere uguale al valore del passaggio 2.

### <a name="enabling-hdcp"></a>Abilitazione di HDCP

Per abilitare HDCP, seguire questa procedura.

1.  Inizializzare una struttura di [**\_ parametri del \_ \_ livello \_ di protezione set di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) con i valori seguenti:
    -   **ulProtectionType**  =  **OPM \_ tipo di protezione \_ \_ HDCP**
    -   **ulProtectionLevel**  =  **OPM \_ HDCP \_ su**
    -   **Riservato** = 0
    -   **Reserved2** = 0
2.  Inviare un comando per il [**\_ \_ \_ livello di protezione set di OPM**](opm-set-protection-level.md) . I dati di input nella matrice **abParameters** sono la struttura dei parametri del livello di protezione del set di [**OPM \_ \_ \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) .
3.  Inviare una richiesta di stato del [**\_ \_ \_ \_ livello di protezione virtuale OPM**](opm-get-virtual-protection-level.md) per verificare se la funzionalità HDCP è abilitata. I primi 4 byte del membro **abParameters** della struttura del [**\_ \_ \_ parametro OPM Get Info**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) contengono il valore di **protezione OPM del \_ tipo di protezione \_ \_ HDCP**.

Quando il metodo [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) restituisce, la matrice **abRequestedInformation** nella struttura [**di \_ \_ informazioni richiesta da OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) contiene una struttura di [**\_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Il membro **ulInformation** di questa struttura contiene un valore dell'enumerazione [**del \_ \_ \_ livello di protezione di OPM HDCP**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) . Se il valore è uguale **\_ a OPM HDCP \_ on**, significa che è abilitato HDCP. In caso contrario, ripetere i passaggi da 1 a 2 fino a quando non viene abilitato HDCP o si verifica un errore. (Ricordare di incrementare il numero di sequenza e generare ogni volta un nuovo numero casuale).

Per abilitare HDCP, in genere è necessario un numero di millisecondi compreso tra 100 e 200, ma l'esecuzione potrebbe richiedere più tempo. Non presupporre che la funzionalità HDCP sia abilitata fino a quando non è stata verificata.

Quando l'applicazione termina la riproduzione di contenuto protetto, disattivare HDCP. I passaggi sono identici a quelli per l'abilitazione di HDCP, ma nel passaggio 1, impostare **ulProtectionLevel** su **OPM \_ HDCP \_ disattivato**.

> [!Note]  
> Non abilitare HDCP se il tipo di connettore è **il \_ connettore OPM \_ tipo \_ DisplayPort \_ Embedded**. (Vedere i [**flag di tipo del connettore OPM**](opm-connector-type-flags.md).)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione protezione output](output-protection-manager.md)
</dt> </dl>

 

 



