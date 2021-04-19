---
title: Funzioni di gestione del profilo
description: Funzioni di gestione del profilo
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- Windows Color System (WCS), funzioni
- WCS (Windows Color System), funzioni
- Gestione colori immagine, funzioni
- gestione dei colori, funzioni
- colori, funzioni
- Riferimento a WCS, funzioni
- informazioni di riferimento su WCS, funzioni
- Windows Color System (WCS), profili
- WCS (Windows Color System), profili
- Gestione colori immagine, profili
- gestione dei colori, profili
- colori, profili
- Riferimento a WCS, profili
- informazioni di riferimento su WCS, profili
- gestione dei profili
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a0e80e300532b20148eef6d9dc362438b6714a3
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "106320206"
---
# <a name="profile-management-functions"></a>Funzioni di gestione del profilo

## <a name="profile-management-functions"></a>Funzioni di gestione del profilo

Le funzioni API seguenti sono utili per la gestione dei profili.



| Funzione                                                                               | Descrizione                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssociateColorProfileWithDeviceW**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | Associa un profilo colori specificato a un dispositivo specificato.                                                              |
| [**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) | Converte uno [spazio di colore](c.md) logico in un [profilo di dispositivo](d.md). |
| [**DisassociateColorProfileFromDeviceW**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | Annulla l'associazione di un profilo colori specificato a un dispositivo specificato in un computer specificato. |
| [**EnumColorProfilesW**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | Enumera tutti i profili che soddisfano i criteri di enumerazione specificati. |
| [**GetColorDirectoryW**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | Recupera il percorso della directory dei colori di Windows in un computer specificato. |
| [**GetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | Ottiene la rampa gamma dalle lavagne di visualizzazione a colori diretti.                                                                                                |
| [**GetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | Recupera il profilo colori registrato per lo spazio dei [colori](c.md)standard specificato. |
| [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | Installa un determinato profilo da usare in un computer specificato. Il profilo viene anche copiato nella directory dei colori. |
| [**RegisterCMMW**](/windows/win32/api/icm/nf-icm-registercmmw) | Associa un valore di identificazione specificato al modulo di gestione dei colori specificato (libreria a collegamento dinamico). Quando questo ID viene visualizzato in un profilo colori, Windows può individuare il CMM corrispondente in modo da creare una trasformazione. |
| [**SetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | Imposta la rampa gamma sulle lavagne di visualizzazione a colori diretti.                                                                                                  |
| [**SetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | Registra un profilo specificato per un determinato [spazio dei colori](c.md)standard. È possibile eseguire query sul profilo utilizzando [GetStandardColorSpaceProfileW](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew). |
| [**UninstallColorProfileW**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | Rimuove un profilo colori specificato da un computer specificato. Facoltativamente, i file associati vengono eliminati dal sistema. |
| [**UnregisterCMMW**](/windows/win32/api/icm/nf-icm-unregistercmmw) | Annulla l'associazione di un valore ID specificato da una libreria di collegamento dinamico (DLL) del modulo di gestione colori specificata. |
| [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | Associa un profilo colori WCS specificato a un dispositivo specificato.                                                                                    |
| [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | Converte un profilo WCS in un profilo ICC.                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | Annulla l'associazione di un profilo colori WCS specificato a un dispositivo specifico in un computer specificato.                                                         |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | Enumera tutti i profili colori che soddisfano i criteri di enumerazione nell'ambito di gestione del profilo specificato.                                       |
| [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)                           | Restituisce la dimensione, in byte, del buffer richiesto dalla funzione [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) per enumerare i profili colori. |
| [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)                         | Recupera il profilo colori predefinito per un dispositivo o l'impostazione predefinita indipendente dal dispositivo se il dispositivo non è specificato.                                  |
| [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | Restituisce la dimensione, in byte, del nome del profilo colori predefinito per un dispositivo, incluso il carattere di terminazione **null** .                                       |
| [**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Recupera la finalità di rendering predefinita nell'ambito di gestione del profilo specificato.                                                                    |
| [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Determina se l'utente ha scelto di usare un elenco di associazioni del profilo per utente per il dispositivo specificato.                                          |
| [**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | Crea un handle per un profilo colori specificato.                                                                                                       |
| [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | Imposta il nome del profilo colori predefinito del tipo di profilo specificato nell'ambito di gestione del profilo specificato.                                         |
| [**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | Imposta la finalità di rendering predefinita nell'ambito di gestione del profilo specificato.                                                                         |
| [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | Consente all'utente di specificare se utilizzare un elenco di associazioni di profili per utente per il dispositivo specificato.                                              |



 

## <a name="profile-consumption-functions"></a>Funzioni di consumo del profilo

Le API di utilizzo del profilo sono le API in ICM2 che accettano profili XML ICC o WCS, handle del profilo o il rendering di Intent come parametri e un set di nuove API per il supporto del profilo WCS per il codice di gestione dei colori dell'applicazione.

 

## <a name="profiles-and-profile-management-functions"></a>Profili e funzioni di gestione del profilo

Il flusso di lavoro di gestione dei profili è basato sulle API ICM2 esistenti, che sono aumentate per fornire funzionalità aggiuntive per la revisione del codice dell'applicazione.

I profili contengono informazioni utilizzate dagli algoritmi di elaborazione dei colori per tradurre il colore tra spazi colore diversi. La gestione dei profili fornisce un modo per eseguire query e specificare quali profili vengono usati in fasi diverse dal modello di elaborazione dei colori per gestire l'output dei colori di varie periferiche con caratteristiche cromatiche diverse.

Gestione profili fornisce il set di funzionalità seguenti:

 

1. Installazione dei profili colori per l'utilizzo nel sistema.

 

2. Associazione di uno o più profili colori installati a qualsiasi dispositivo specifico.

 

3. Scelta di un profilo colori predefinito di un particolare tipo tra i profili disponibili per l'utilizzo in una determinata fase di elaborazione dei colori. Potrebbe trattarsi di un dispositivo tra i profili associati o tra i profili installati nel sistema e non specifici del dispositivo.

 

4. Enumerazione dei profili dei colori che soddisfano determinati criteri tra i profili installati nel sistema.

Le estensioni del nome file del profilo WCS sono ". CDMP" per DMPs, ". Camp" per i campi e ". gmmp" per GMMPs.

 

**Gestione dei profili per utente e abilitazione dell'esecuzione in un contesto LUA**

L'obiettivo della progettazione descritta nel documento corrente è il seguente:

 

1. L'implementazione di ICM2 legacy non fornisce supporto per la gestione dei profili per utente. Utenti diversi non possono avere impostazioni del proprio profilo. In vista, l'infrastruttura di gestione dei profili WCS consente agli utenti di configurare singole impostazioni del profilo per la maggior parte delle funzionalità.

 

2. Tutte le API legacy di gestione del profilo ICM2 modificano le impostazioni a livello di sistema e richiedono privilegi amministrativi. In Windows Vista tutti gli utenti eseguono la maggior parte delle impostazioni dell'account utente con privilegi minimi, mentre gli amministratori possono elevare i privilegi in modo selettivo per eseguire applicazioni che modificano le impostazioni a livello di sistema. Nella gestione dei profili WCS tutte le impostazioni del profilo per utente sono configurabili nel contesto LUA. Le applicazioni di gestione del profilo possono essere eseguite come impostazioni LUA, aumentando l'ambito di utilizzo e garantendo che la sicurezza del sistema non venga compromessa.

La gestione dei profili in vista offre i miglioramenti seguenti rispetto all'infrastruttura ICM2 legacy:

 

1. Consente l'associazione del profilo con i dispositivi, le impostazioni predefinite del profilo e l'enumerazione dei profili nell'ambito per utente e a livello di sistema.

 

2. L'installazione di un profilo rimane a livello di sistema e richiede privilegi di amministratore. Questo è coerente con l'installazione del profilo durante l'installazione del dispositivo perché l'installazione del dispositivo è a livello di sistema e richiede privilegi amministrativi.

 

Se i dispositivi possono essere installati dal contesto LUA sono specifici per ciò che è supportato per la classe del dispositivo. In vista, ad esempio, è possibile eseguire l'installazione della stampante dal contesto LUA se all'utente sono stati concessi i diritti per copiare i file nell'archivio driver da un amministratore di dominio usando i criteri di archivio driver. L'infrastruttura di gestione dei profili dei colori non deve eseguire alcuna operazione speciale in quanto l'installazione viene eseguita nel contesto dello spooler.

 

3. La modifica delle impostazioni del profilo nell'ambito per utente può essere eseguita nel contesto LUA. le modifiche a livello di sistema richiedono privilegi amministrativi. Le operazioni di gestione del profilo che richiedono la lettura delle informazioni di configurazione possono essere eseguite nel contesto LUA per le impostazioni per utente e a livello di sistema.

L'ambito di gestione dei profili indica l'ambito delle operazioni eseguite; per utente o a livello di sistema.

Per ogni operazione, viene indicato se può essere eseguita dal contesto LUA. Se un'operazione non può essere eseguita nel contesto LUA, l'API di gestione del profilo corrispondente restituisce un errore con accesso negato. Le applicazioni che usano l'API, ad esempio il pannello di controllo della gestione dei colori, possono consentire all'utente di elevare il contesto amministrativo (usando l'interfaccia utente OTS o di consenso), quindi chiamare l'API dal contesto con privilegi elevati in modo che l'operazione venga eseguita correttamente.



Operazione

Ambito di gestione del profilo

Pre-condizione

Post-condizione

Eseguibile nel contesto LUA

$ {ROWSPAN2} $Install profilo $ {REMOVE} $  

A livello di sistema

Profilo copiato, installato nel sistema e disponibile per l'utilizzo. Il profilo è enumerabile nell'ambito dell'utente corrente e a livello di sistema per tutti gli utenti.

Durante l'installazione del driver di dispositivo, governato dai criteri di installazione dei driver. No, in caso contrario.

Utente corrente

Non supportato

$ {ROWSPAN2} $Uninstall profilo $ {REMOVE} $  

A livello di sistema

Il profilo è installato nel sistema

Profilo disinstallato dal sistema ed eventualmente eliminato dall'archivio profili. Il profilo non è più disponibile per l'uso e non è enumerabile in alcun ambito.

No

Utente corrente

Non supportato

$ {ROWSPAN2} $Associate profilo con dispositivo $ {REMOVE} $  

A livello di sistema

Il profilo è installato ed è di tipo ICC o CDMP

Il profilo è disponibile per l'uso con il dispositivo da parte di tutti gli utenti. È enumerabile, nell'ambito a livello di sistema e anche nell'ambito dell'utente corrente per tutti gli utenti, come associato al dispositivo.

No

Utente corrente

Profilo installato. Non è importante se il profilo è già associato al dispositivo nell'ambito a livello di sistema ed è di tipo ICC o CDMP.

Il profilo è disponibile per l'uso con il dispositivo da parte dell'utente corrente. È enumerabile solo nell'ambito dell'utente corrente (a meno che non sia presente anche un'associazione a livello di sistema) come associato al dispositivo.

Sì

$ {ROWSPAN2} $Disassociate profilo dal dispositivo $ {REMOVE} $  

A livello di sistema

Il profilo è associato al dispositivo nell'ambito a livello di sistema ed è di tipo ICC o CDMP

Il profilo non è più disponibile per l'uso (ad eccezione degli utenti che hanno anche questa associazione nell'ambito dell'utente corrente). Non è enumerabile nell'ambito a livello di sistema. Potrebbe essere enumerabile nell'ambito dell'utente corrente, tuttavia, per un utente che dispone di questa associazione nell'ambito.

No

Utente corrente

Il profilo è associato al dispositivo nell'ambito dell'utente corrente (indipendentemente dal fatto che sia associato a un ambito a livello di sistema) ed è di tipo ICC o CDMP.

Il profilo non è più disponibile per l'uso, o enumerabile come associato al dispositivo, dall'utente corrente (a meno che non sia anche associato a un ambito a livello di sistema al dispositivo).

Sì

$ {ROWSPAN2} $Set profilo per un tipo (DMP o ICC) come impostazione predefinita per un dispositivo $ {REMOVE} $  

A livello di sistema

Il profilo è di tipo ICC o CDMP

Il profilo viene usato per impostazione predefinita, per il tipo specifico con il dispositivo, per tutti gli utenti ad eccezione di quelli che hanno eseguito l'override di questa impostazione nell'ambito dell'utente corrente. Il profilo viene installato e associato al sistema del dispositivo a livello di sistema, se non lo è già.

No

Utente corrente

Il profilo è di tipo ICC o CDMP

Il profilo viene usato per impostazione predefinita per il tipo specifico con il dispositivo in caso di utente corrente, indipendentemente dall'impostazione predefinita a livello di sistema. Il profilo viene installato e associato al dispositivo per l'utente corrente, se questa situazione non è già presente.

Sì, se il profilo è già installato

$ {ROWSPAN2} $Set profilo per un tipo (ICC, DMP, CAMP, GMMP) e una combinazione di sottotipo come valore predefinito globale $ {REMOVE} $  

A livello di sistema

È possibile associare solo i profili ICC e CDMP ai dispositivi.

Per impostazione predefinita, il profilo viene usato per il tipo specifico. Gli utenti possono eseguire l'override di questa impostazione nell'ambito dell'utente corrente. (Il profilo è installato, se questa situazione non è già presente).

No

Utente corrente

È possibile associare solo i profili ICC e CDMP ai dispositivi.

Per impostazione predefinita, il profilo viene usato per il tipo specifico per l'utente corrente. (Il profilo è installato, se questa situazione non è già presente).

Sì, se il profilo è già installato.

$ {ROWSPAN2} $Erase l'override dell'utente corrente per una particolare impostazione del profilo predefinito, in modo che l'impostazione predefinita del sistema venga sempre utilizzata (come fallback) anche per l'ambito dell'utente corrente. $ {REMOVE} $  

A livello di sistema

Non applicabile

Utente corrente

Anche per le query utente correnti sulle impostazioni predefinite del profilo, le impostazioni a livello di sistema vengono restituite per l'uso.

Sì

$ {ROWSPAN2} $Enumerate profili installati che soddisfano determinati criteri, ad esempio classe del dispositivo, classe del profilo e così via. $ {REMOVE} $  

A livello di sistema

È possibile associare ed enumerare solo i profili ICC e CDMP per i dispositivi.

I profili installati e che soddisfano i criteri specificati nell'ambito a livello di sistema vengono enumerati.

Sì

Utente corrente

Solo i profili ICC e CDMP possono essere associati ai dispositivi e quindi enumerati per i dispositivi.

I profili installati e che soddisfano i criteri specificati nell'ambito a livello di sistema vengono enumerati.

Sì

$ {ROWSPAN2} $Enumerate profili associati a un particolare dispositivo che soddisfa determinati criteri, ad esempio la classe Device e la classe profile $ {REMOVE} $  

A livello di sistema

È possibile associare ed enumerare solo i profili ICC e CDMP per i dispositivi.

I profili associati al dispositivo nell'ambito a livello di sistema e soddisfano i criteri specificati nell'ambito a livello di sistema vengono enumerati.

Sì

Utente corrente

È possibile associare ed enumerare solo i profili ICC e CDMP per i dispositivi.

I profili disponibili come associati al dispositivo nell'ambito dell'utente corrente, che include le associazioni a livello di sistema e soddisfa i criteri specificati nell'ambito dell'utente corrente, vengono enumerati.

Sì



 

I tipi di profilo colori validi sono forniti dall'enumerazione COLORPROFILETYPE.

I sottotipi di profilo colori validi vengono forniti dall'enumerazione COLORPROFILESUBTYPE.

Nella tabella seguente sono illustrate le combinazioni di tipi di profilo/sottotipi validi.



COLORPROFILETYPE

COLORPROFILESUBTYPE valido

Note

Impostazione predefinita dispositivo

Impostazioni predefinite globali

Uso previsto

Uso previsto

CPI del CPT \_

CPST \_ None

Ottenere/impostare il profilo ICC predefinito associato a un dispositivo

CPST \_ RGBWorkingSpace o CPST \_ CustomWorkingSpace

Ottenere/impostare il profilo ICC come profilo RGB globale o spazio di lavoro personalizzato. Vedere la nota.

COLORPROFILETYPE CPT \_ ICC e CPT dmp si escludono a \_ vicenda. Il profilo colori predefinito impostato per uno spazio di lavoro specificato (RGB o personalizzato) può essere un profilo ICC o un profilo DMP, ma non entrambi.

\_DMP CPT

CPST \_ None

Ottenere/impostare il profilo DMP predefinito associato a un dispositivo

CPST \_ RGBWorkingSpace o CPST \_ CustomWorkingSpace

Ottenere/impostare il profilo DMP come profilo RGB globale o spazio di lavoro personalizzato. Vedere la nota.

COLORPROFILETYPE CPT \_ ICC e CPT dmp si escludono a \_ vicenda. Il profilo colori predefinito impostato per uno spazio di lavoro specificato (RGB o personalizzato) può essere un profilo ICC o un profilo DMP, ma non entrambi.



 

> [!Note]  
> Quando WcsSetDefaultColorProfile viene chiamato per impostare un profilo DMP come profilo predefinito per lo spazio di lavoro RGB o uno spazio di lavoro personalizzato, solo un profilo DMP di tipo RGBVirtualDevice, LCD o CRT è valido.
>
>  
>
> Quando WcsSetDefaultColorProfile viene chiamato per impostare un profilo ICC come profilo predefinito per lo spazio di lavoro RGB o uno spazio di lavoro personalizzato, solo un profilo ICC la cui classe è "SPAC" o "disp" e il cui spazio colore è "RGB" è valido.

 

L'architettura è progettata in base ai requisiti delle operazioni come indicato nelle enumerazioni e nelle tabelle precedenti.

### <a name="profile-management-public-api-layer"></a>Livello API pubblico di gestione dei profili

Poiché l'ambito di gestione del profilo non è supportato dalle API ICM2 legacy, è necessario un nuovo set di API di gestione dei profili WCS che definisce l'ambito di gestione del profilo come utente corrente o a livello di sistema. ? Le API ICM2 legacy continuano a essere supportate per la compatibilità con le versioni precedenti e funzionano nell'ambito della gestione del profilo implicito per la chiamata. o ICM2 API che funzionano nell'ambito dell'utente corrente? Si tratta di operazioni supportate sia per l'ambito a livello di sistema che per l'utente corrente nella gestione dei profili WCS. Le API ICM2 legacy chiamano le nuove API WCS con ambito di gestione del profilo come utente corrente. Questa operazione è utile dal punto di vista dell'utente perché consente le impostazioni per utente dalle applicazioni legacy e anche l'esecuzione della maggior parte delle operazioni nel contesto LUA. o ICM2 API che funzionano nell'ambito a livello di sistema? Si tratta di operazioni (profili di installazione e profili di disinstallazione) che supportano solo l'ambito a livello di sistema. Non vengono create nuove API di gestione dei profili WCS ed è possibile modificare le API esistenti.

Le implementazioni sottostanti delle operazioni di gestione dei profili funzionano sulle seguenti entità di dati di configurazione per creare il contesto per gli algoritmi di elaborazione dei colori per fornire funzionalità di gestione dei colori. Si tratta di impostazioni specifiche del dispositivo o globali (indipendenti dal dispositivo). o dati di configurazione specifici del dispositivo:? Elenco di profili associati a un determinato dispositivo. ? Profilo predefinito per i diversi tipi di profilo associati a un dispositivo. ? Modalità di corrispondenza dei profili utilizzati per l'enumerazione. o dati di configurazione globali:? Elenco di profili installati nel sistema. ? Profilo predefinito globale per diversi tipi di profilo. ? Le implementazioni sottostanti dell'archiviazione dei dati di configurazione accettano l'ambito di archiviazione per i dati di configurazione (indipendente dal dispositivo o dispositivo specifico), che può essere l'utente corrente o a livello di sistema. Questa operazione è diversa dall'ambito di gestione del profilo. Un'operazione con ambito di gestione del profilo utente corrente può causare la lettura da un ambito di archiviazione a livello di sistema se l'impostazione dell'utente corrente per l'operazione non è presente. ? Il livello API ICM2/WCS chiama in questo livello di archiviazione per ottenere e impostare i dati con l'ambito di archiviazione appropriato. Il livello di archiviazione è trasparente per l'ambito di gestione del profilo. Logica per combinare i dati dagli ambiti di archiviazione dell'utente corrente e dell'intero sistema per creare o aggiornare una configurazione in base all'ambito di gestione del profilo specificato dal chiamante dell'API. Questa logica è presente nel livello API ICM2/WCS.

### <a name="device-specific-storage-layer"></a>Livello di archiviazione specifico del dispositivo

Lo spazio di archiviazione per classi diverse di dispositivi quali stampa, acquisizione o visualizzazione potrebbe essere diverso l'uno dall'altro. Ad esempio, i dati di configurazione per un dispositivo di stampa devono essere archiviati usando le API di stampa standard, ad esempio SetPrinterDataEx e GetPrinterDataEx, per consentire la copia dei profili e le impostazioni da trasferire in un computer client durante la connessione di tipo punto e stampa. ? Questo livello esporta la funzionalità per aprire lo Store, recuperare i dati, impostare i dati e chiudere l'archivio usando interfacce predefinite comuni, in modo che il livello di archiviazione della configurazione di gestione del profilo possa chiamarli mentre è trasparente per il modo in cui vengono archiviati i dati per tale dispositivo.

Nella figura seguente viene illustrata questa architettura.



Livello API pubblico di gestione dei profili

$ {ROWSPAN2} $Legacy API ICM2 per le operazioni che supportano solo l'ambito di gestione del profilo a livello di sistema in vista (installare, disinstallare e ottenere la directory dei colori). Chiamano il livello di archiviazione della configurazione con ambito di archiviazione appropriato. $ {REMOVE} $  

API ICM2 legacy per operazioni che supportano l'ambito di gestione dei profili utente e di sistema in vista (tutte le operazioni diverse da installazione, disinstallazione e ottenere la directory dei colori). Operano in modo implicito nell'ambito dell'utente corrente e chiamano la nuova API WCS con ambito di gestione del profilo come utente corrente.

Nuova API WCS con supporto dell'ambito di gestione dei profili utente corrente e a livello di sistema. Chiamano il livello di archiviazione della configurazione con ambito di archiviazione appropriato.



 



Livello di archiviazione della configurazione di gestione del profilo

Routine di configurazione globali indipendenti dal dispositivo

Routine di configurazione specifiche del dispositivo

$ {ROWSPAN3} $Profile l'installazione e la gestione delle impostazioni del profilo predefinite indipendenti dal dispositivo, supportata nell'ambito di archiviazione dell'utente corrente e a livello di sistema. $ {REMOVE} $  

Associazione del dispositivo e gestione delle impostazioni del profilo predefinito specifiche del dispositivo, supportata nell'ambito di archiviazione dell'utente corrente e a livello di sistema.

Livello di archiviazione Device-Specific

Archiviazione specifica di stampa

Visualizza archiviazione specifica

Acquisisci archiviazione specifica



 

Le API ICM2 legacy per le operazioni che supportano solo l'ambito di gestione dei profili a livello di sistema in vista non hanno alcuna modifica nel comportamento. Le operazioni di installazione e disinstallazione rientrino in questa categoria.

Le API legacy di ICM2 per le operazioni che supportano l'ambito di gestione dei profili utente corrente e a livello di sistema sono state modificate per eseguire query e configurare le impostazioni dell'utente corrente. Tutte le operazioni diverse da Install e Uninstall rientreranno in questa categoria.

 

 




