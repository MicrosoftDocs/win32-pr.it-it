---
title: Funzioni di gestione dei profili
description: Funzioni di gestione dei profili
ms.assetid: 185863b7-0b74-4c65-97c3-3c60b86d37fd
keywords:
- Windows Sistema di colori (WCS), funzioni
- WCS (Windows Color System), funzioni
- gestione del colore delle immagini, funzioni
- gestione dei colori, funzioni
- colori, funzioni
- Informazioni di riferimento su WCS, funzioni
- informazioni di riferimento per WCS, funzioni
- Windows Sistema a colori (WCS), profili
- WCS (Windows Color System), profili
- gestione dei colori delle immagini, profili
- gestione dei colori, profili
- colori, profili
- Informazioni di riferimento su WCS, profili
- informazioni di riferimento per WCS, profili
- gestione dei profili
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f047c2dee199800fad976dd7b959fbbb54d585fd252fb8b5390c3223415db4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587771"
---
# <a name="profile-management-functions"></a>Funzioni di gestione dei profili

## <a name="profile-management-functions"></a>Funzioni di gestione dei profili

Le funzioni API seguenti sono utili nella gestione dei profili.



| Funzione                                                                               | Descrizione                                                                                                                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssociateColorProfileWithDeviceW**](/windows/win32/api/icm/nf-icm-associatecolorprofilewithdevicew)             | Associa un profilo colori specificato a un dispositivo specificato.                                                              |
| [**CreateProfileFromLogColorSpaceW**] ((/windows/win32/api/icm/nf-icm-createprofilefromlogcolorspacew) | Converte uno spazio [colore logico in](c.md) un profilo di [dispositivo.](d.md) |
| [**DisassociateColorProfileFromDeviceW**](/windows/win32/api/icm/nf-icm-disassociatecolorprofilefromdevicew) | Dissocia un profilo colori specificato con un dispositivo specificato in un computer specificato. |
| [**EnumColorProfilesW**](/windows/win32/api/icm/nf-icm-enumcolorprofilesw) | Enumera tutti i profili che soddisfano i criteri di enumerazione specificati. |
| [**GetColorDirectoryW**](/windows/win32/api/icm/nf-icm-getcolordirectoryw) | Recupera il percorso della directory Windows COLOR in un computer specificato. |
| [**GetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicegammaramp)                                       | Ottiene la rampa gamma dalle schede di visualizzazione a colori diretta.                                                                                                |
| [**GetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) | Recupera il profilo colori registrato per lo spazio colori standard [specificato.](c.md) |
| [**InstallColorProfileW**](/windows/win32/api/icm/nf-icm-installcolorprofilew) | Installa un profilo specificato da usare in un computer specificato. Il profilo viene copiato anche nella directory COLOR. |
| [**RegisterCMMW**](/windows/win32/api/icm/nf-icm-registercmmw) | Associa un valore di identificazione specificato alla libreria a collegamento dinamico (DLL CMM) del modulo di gestione colori specificata. Quando questo ID viene visualizzato in un profilo colori, Windows possibile individuare il CMM corrispondente in modo da creare una trasformazione. |
| [**SetDeviceGammaRamp**](/windows/desktop/api/Wingdi/nf-wingdi-setdevicegammaramp)                                       | Imposta la rampa gamma sulle schede di visualizzazione a colori diretto.                                                                                                  |
| [**SetStandardColorSpaceProfileW**](/windows/win32/api/icm/nf-icm-setstandardcolorspaceprofilew) | Registra un profilo specificato per uno spazio colore standard [specificato.](c.md) È possibile eseguire query sul profilo usando [GetStandardColorSpaceProfileW.](/windows/win32/api/icm/nf-icm-getstandardcolorspaceprofilew) |
| [**UninstallColorProfileW**](/windows/win32/api/icm/nf-icm-uninstallcolorprofilew) | Rimuove un profilo colori specificato da un computer specificato. I file associati vengono eliminati facoltativamente dal sistema. |
| [**Annullare la registrazione diCMMW**](/windows/win32/api/icm/nf-icm-unregistercmmw) | Dissocia un valore ID specificato da una determinata libreria a collegamento dinamico del modulo di gestione colori (DLL CMM). |
| [**WcsAssociateColorProfileWithDevice**](/windows/win32/api/icm/nf-icm-wcsassociatecolorprofilewithdevice)       | Associa un profilo colori WCS specificato a un dispositivo specificato.                                                                                    |
| [**WcsCreateIccProfile**](/windows/win32/api/icm/nf-icm-wcscreateiccprofile)                                     | Converte un profilo WCS in un profilo ICC.                                                                                                          |
| [**WcsDisassociateColorProfileFromDevice**](/windows/win32/api/icm/nf-icm-wcsdisassociatecolorprofilefromdevice) | Dissocia un profilo colori WCS specificato con un dispositivo specificato in un computer specificato.                                                         |
| [**WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles)                                   | Enumera tutti i profili colori che soddisfano i criteri di enumerazione nell'ambito di gestione dei profili specificato.                                       |
| [**WcsEnumColorProfilesSize**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofilessize)                           | Restituisce le dimensioni, in byte, del buffer richiesto dalla [**funzione WcsEnumColorProfiles**](/windows/win32/api/icm/nf-icm-wcsenumcolorprofiles) per enumerare i profili colori. |
| [**WcsGetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofile)                         | Recupera il profilo colori predefinito per un dispositivo o l'impostazione predefinita indipendente dal dispositivo se il dispositivo non è specificato.                                  |
| [**WcsGetDefaultColorProfileSize**](/windows/win32/api/icm/nf-icm-wcsgetdefaultcolorprofilesize) | Restituisce le dimensioni, in byte, del nome del profilo colori predefinito per un dispositivo, incluso il terminatore **NULL.**                                       |
| [**WcsGetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Recupera la finalità di rendering predefinita nell'ambito di gestione del profilo specificato.                                                                    |
| [**WcsGetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcsgetdefaultrenderingintent) | Determina se l'utente ha scelto di usare un elenco di associazioni di profili per utente per il dispositivo specificato.                                          |
| [**WcsOpenColorProfileW**](/windows/win32/api/icm/nf-icm-wcsopencolorprofilew) | Crea un handle per un profilo colori specificato.                                                                                                       |
| [**WcsSetDefaultColorProfile**](/windows/win32/api/icm/nf-icm-wcssetdefaultcolorprofile) | Imposta il nome predefinito del profilo colori del tipo di profilo specificato nell'ambito di gestione del profilo specificato.                                         |
| [**WcsSetDefaultRenderingIntent**](/windows/win32/api/icm/nf-icm-wcssetdefaultrenderingintent) | Imposta la finalità di rendering predefinita nell'ambito di gestione del profilo specificato.                                                                         |
| [**WcsSetUsePerUserProfiles**](/windows/win32/api/icm/nf-icm-wcssetuseperuserprofiles)                           | Consente all'utente di specificare se usare un elenco di associazioni di profili per utente per il dispositivo specificato.                                              |



 

## <a name="profile-consumption-functions"></a>Funzioni di utilizzo del profilo

Le API di utilizzo del profilo sono le API in ICM2 che accettano profili XML ICC o WCS, handle di profilo o finalità di rendering come parametri e un set di nuove API per il supporto del profilo WCS per il codice di gestione dei colori dell'applicazione.

 

## <a name="profiles-and-profile-management-functions"></a>Profili e funzioni di gestione dei profili

Il flusso di lavoro di gestione dei profili si basa sulle API ICM2 esistenti che vengono aumentate per fornire funzionalità aggiuntive per la revisione del codice dell'applicazione.

I profili contengono informazioni usate dagli algoritmi di elaborazione dei colori per tradurre il colore tra spazi colori diversi. La gestione dei profili consente di eseguire query e specificare quali profili vengono usati in fasi diverse dal modello di elaborazione dei colori per gestire l'output dei colori di vari dispositivi periferici con caratteristiche di colore diverse.

La gestione dei profili offre il set di funzionalità seguente:

 

1. Installazione di profili colori da usare nel sistema.

 

2. Associazione di uno o più profili colori installati a qualsiasi dispositivo specifico.

 

3. Scelta di un profilo colori predefinito di un particolare tipo tra i profili disponibili per l'uso in una particolare fase di elaborazione del colore. Questo potrebbe essere per un dispositivo tra i profili associati o tra i profili installati nel sistema e non specifici del dispositivo.

 

4. Enumerazione dei profili colori che soddisfano criteri specifici tra i profili installati nel sistema.

Le estensioni del nome file del profilo WCS sono ".cdmp" per i DMP, ".camp" per i FILE DIP e ".gmmp" per IMMP.

 

**Gestione dei profili per utente e abilitazione dell'esecuzione nel contesto LUA**

L'obiettivo della progettazione descritta nel documento corrente è il seguente:

 

1. L'implementazione legacy di ICM2 non fornisce il supporto per la gestione dei profili per utente. Utenti diversi non possono avere le proprie impostazioni del profilo. In Vista l'infrastruttura di gestione dei profili WCS consente agli utenti di configurare le singole impostazioni del profilo per la maggior parte delle funzionalità.

 

2. Tutte le API di gestione dei profili ICM2 legacy modificano le impostazioni a livello di sistema e richiedono privilegi amministrativi. In Windows Vista tutti gli utenti vengono eseguiti nella maggior parte dei casi nelle impostazioni dell'account utente con privilegi minimi e gli amministratori possono elevare i privilegi in modo selettivo per eseguire applicazioni che modificano le impostazioni a livello di sistema. Nella gestione dei profili WCS tutte le impostazioni del profilo per utente sono configurabili nel contesto LUA. Le applicazioni di gestione dei profili possono essere eseguite come impostazioni LUA, aumentando l'ambito di utilizzo e garantendo che la sicurezza del sistema non venga compromessa.

La gestione dei profili in Vista offre i miglioramenti seguenti rispetto all'infrastruttura ICM2 legacy:

 

1. Abilita l'associazione dei profili ai dispositivi, le impostazioni predefinite del profilo e l'enumerazione dei profili sia nell'ambito per utente che a livello di sistema.

 

2. L'installazione di un profilo rimane a livello di sistema e richiede privilegi di amministratore. Questo è coerente con l'installazione del profilo durante l'installazione del dispositivo perché l'installazione del dispositivo è a livello di sistema e richiede privilegi amministrativi.

 

L'eventuale installazione di dispositivi dal contesto LUA è particolare rispetto a quanto supportato per tale classe di dispositivi. Ad esempio, in Vista è possibile eseguire l'installazione della stampante dal contesto LUA se all'utente sono stati concessi diritti per copiare file nell'archivio driver da un amministratore di dominio usando i criteri dell'archivio driver. L'infrastruttura di gestione dei profili colori non deve eseguire alcun tipo di operazione speciale a questo proposito, poiché l'installazione avviene nel contesto dello spooler.

 

3. La modifica delle impostazioni del profilo nell'ambito per utente può essere eseguita nel contesto LUA. Per le modifiche a livello di sistema sono necessari privilegi amministrativi. Le operazioni di gestione dei profili che richiedono la lettura delle informazioni di configurazione possono essere eseguite nel contesto LUA per le impostazioni per utente e a livello di sistema.

L'ambito di gestione dei profili indica l'ambito delle operazioni eseguite. per utente o a livello di sistema.

Per ogni operazione, viene indicato se può essere eseguita dal contesto LUA. Se non è possibile eseguire un'operazione nel contesto LUA, l'API di gestione dei profili corrispondente restituisce un errore con accesso negato. Le applicazioni che usano l'API, ad esempio Gestione colori Pannello di controllo, possono consentire all'utente di elevare al contesto amministrativo (usando OTS o l'interfaccia utente di consenso) e quindi chiamare l'API dal contesto con privilegi elevati in modo che l'operazione riesca.



Operazione

Ambito di gestione dei profili

Pre-condizione

Post-condizione

Eseguibile nel contesto LUA

${ROWSPAN2}$Install profilo${REMOVE}$  

A livello di sistema

Profilo copiato, installato nel sistema e disponibile per l'uso. Il profilo è enumerabile nell'ambito dell'utente corrente e a livello di sistema per tutti gli utenti.

Durante l'installazione del driver di dispositivo, regolato dai criteri di installazione dei driver. No, in caso contrario.

Utente corrente

Non supportato

${ROWSPAN2}$Uninstall profilo${REMOVE}$  

A livello di sistema

Il profilo è installato nel sistema

Profilo disinstallato dal sistema ed eventualmente eliminato dall'archivio profili. Il profilo non è più disponibile per l'uso e non è enumerabile in alcun ambito.

No

Utente corrente

Non supportato

${ROWSPAN2}$Associate profilo con device${REMOVE}$  

A livello di sistema

Il profilo è installato ed è di tipo ICC o CDMP

Il profilo è disponibile per l'uso con il dispositivo da parte di tutti gli utenti. È enumerabile, nell'ambito a livello di sistema e anche nell'ambito dell'utente corrente per tutti gli utenti, come associato al dispositivo.

No

Utente corrente

Il profilo è installato. Non è importante se il profilo è già associato al dispositivo nell'ambito a livello di sistema ed è di tipo ICC o CDMP.

Il profilo è disponibile per l'uso con il dispositivo da parte dell'utente corrente. È enumerabile solo nell'ambito dell'utente corrente (a meno che non vi sia anche un'associazione a livello di sistema) associata al dispositivo.

Sì

${ROWSPAN2}$Disassociate profilo dal dispositivo${REMOVE}$  

A livello di sistema

Il profilo è associato al dispositivo nell'ambito a livello di sistema ed è di tipo ICC o CDMP

Il profilo non è più disponibile per l'uso , ad eccezione degli utenti che hanno questa associazione anche nell'ambito dell'utente corrente. Non è enumerabile nell'ambito a livello di sistema. Potrebbe tuttavia essere enumerabile nell'ambito dell'utente corrente, per un utente che ha questa associazione nell'ambito.

No

Utente corrente

Il profilo è associato al dispositivo nell'ambito dell'utente corrente (indipendentemente dal fatto che sia associato nell'ambito a livello di sistema) e è di tipo ICC o CDMP.

Il profilo non è più disponibile per l'uso, o enumerabile come associato al dispositivo, dall'utente corrente (a meno che non sia associato anche nell'ambito a livello di sistema al dispositivo).

Sì

${ROWSPAN2}$Set per un tipo (DMP o ICC) come impostazione predefinita per un dispositivo${REMOVE}$  

A livello di sistema

Il profilo è di tipo ICC o CDMP

Il profilo viene usato per impostazione predefinita, per il tipo specifico con il dispositivo, per tutti gli utenti ad eccezione di quelli che hanno eseguito l'override di questa impostazione nell'ambito dell'utente corrente. Il profilo viene installato e associato a livello di sistema del dispositivo, se non è già così.

No

Utente corrente

Il profilo è di tipo ICC o CDMP

Il profilo viene usato per impostazione predefinita per il tipo specifico con il dispositivo nel caso dell'utente corrente, indipendentemente dall'impostazione predefinita a livello di sistema. Il profilo viene installato e associato al dispositivo per l'utente corrente, se questo non è già il caso.

Sì, se il profilo è già installato

${ROWSPAN2}$Set profilo per un tipo (ICC, DMP, CAMP, GMMP) e una combinazione di sottotipo come valore predefinito globale${REMOVE}$  

A livello di sistema

Ai dispositivi possono essere associati solo i profili ICC e CDMP.

Il profilo viene usato per impostazione predefinita per il tipo specifico. Gli utenti possono eseguire l'override di questa impostazione nell'ambito dell'utente corrente. Il profilo viene installato, se non è già così.

No

Utente corrente

Ai dispositivi possono essere associati solo i profili ICC e CDMP.

Il profilo viene usato per impostazione predefinita per il tipo specifico per l'utente corrente. Il profilo viene installato, se non è già così.

Sì, se il profilo è già installato.

${ROWSPAN2}$Erase l'override dell'utente corrente per una particolare impostazione del profilo predefinito, in modo che il valore predefinito del sistema venga sempre usato (come fallback) anche per l'ambito dell'utente corrente.${REMOVE}$  

A livello di sistema

Non applicabile

Utente corrente

Anche per le query dell'utente corrente sulle impostazioni predefinite del profilo, le impostazioni a livello di sistema vengono restituite per l'uso.

Sì

${ROWSPAN2}$Enumerate profili installati che soddisfano criteri specifici (ad esempio classe di dispositivo, classe di profilo e così via) ${REMOVE}$  

A livello di sistema

Solo i profili ICC e CDMP possono essere associati ed enumerati per i dispositivi.

Vengono enumerati i profili installati e che soddisfano i criteri specificati nell'ambito a livello di sistema.

Sì

Utente corrente

Solo i profili ICC e CDMP possono essere associati ai dispositivi e quindi enumerati per i dispositivi.

Vengono enumerati i profili installati e che soddisfano i criteri specificati nell'ambito a livello di sistema.

Sì

${ROWSPAN2}$Enumerate profili associati a un dispositivo specifico che soddisfano criteri specifici, ad esempio la classe del dispositivo e la classe di profilo${REMOVE}$  

A livello di sistema

Solo i profili ICC e CDMP possono essere associati ed enumerati per i dispositivi.

Vengono enumerati i profili associati al dispositivo nell'ambito a livello di sistema e soddisfano i criteri specificati nell'ambito a livello di sistema.

Sì

Utente corrente

Solo i profili ICC e CDMP possono essere associati ed enumerati per i dispositivi.

Vengono enumerati i profili disponibili come associati al dispositivo nell'ambito dell'utente corrente, che include le associazioni a livello di sistema e soddisfa i criteri specificati nell'ambito dell'utente corrente.

Sì



 

I tipi di profilo colori validi vengono forniti dall'enumerazione COLORPROFILETYPE.

I sottotipi di profilo colori validi vengono forniti dall'enumerazione COLORPROFILESUBTYPE.

Nella tabella seguente sono illustrate le combinazioni di tipo di profilo/sottotipo valide.



COLORPROFILETYPE

COLORPROFILESUBTYPE valido

Note

Impostazione predefinita dispositivo

Impostazione predefinita globale

Uso previsto

Uso previsto

CPT \_ ICC

CPST \_ NONE

Ottenere/impostare il profilo ICC predefinito associato a un dispositivo

CPST \_ RGBWorkingSpace o CPST \_ CustomWorkingSpace

Ottiene/imposta il profilo ICC come profilo RGB globale o spazio di lavoro personalizzato. Vedere la nota.

COLORPROFILETYPE CPT \_ ICC e CPT \_ DMP si escludono a vicenda. Il profilo colori predefinito impostato per un determinato spazio di lavoro (RGB o Personalizzato) può essere un profilo ICC o un profilo DMP, ma non entrambi.

CPT \_ DMP

CPST \_ NONE

Ottiene/imposta il profilo DMP predefinito associato a un dispositivo

CPST \_ RGBWorkingSpace o CPST \_ CustomWorkingSpace

Ottiene/imposta il profilo DMP come profilo RGB globale o spazio di lavoro personalizzato. Vedere la nota.

COLORPROFILETYPE CPT \_ ICC e CPT \_ DMP si escludono a vicenda. Il profilo colori predefinito impostato per un determinato spazio di lavoro (RGB o Personalizzato) può essere un profilo ICC o un profilo DMP, ma non entrambi.



 

> [!Note]  
> Quando viene chiamato WcsSetDefaultColorProfile per impostare un profilo DMP come profilo predefinito per lo spazio di lavoro RGB o uno spazio di lavoro personalizzato, è valido solo un profilo DMP di tipo RGBVirtualDevice, LCD o CRT.
>
>  
>
> Quando WcsSetDefaultColorProfile viene chiamato per impostare un profilo ICC come profilo predefinito per lo spazio di lavoro RGB o uno spazio di lavoro personalizzato, è valido solo un profilo ICC la cui classe è "spac" o "disp" e lo spazio colore è "RGB".

 

L'architettura è progettata in base ai requisiti delle operazioni, come indicato nelle enumerazioni e nelle tabelle precedenti.

### <a name="profile-management-public-api-layer"></a>Livello API pubblica di gestione dei profili

Poiché l'ambito di gestione dei profili non è supportato dalle API ICM2 legacy, è necessario un nuovo set di API di gestione dei profili WCS che definisce l'ambito di gestione dei profili come utente corrente o a livello di sistema. ? Le API ICM2 legacy continuano a essere supportate per la compatibilità con le versioni precedenti e funzionano nell'ambito di gestione del profilo implicito per la chiamata. o API ICM2 che funzionano nell'ambito dell'utente corrente? Questo è per le operazioni supportate per l'ambito dell'utente corrente e a livello di sistema nella gestione dei profili WCS. Le API ICM2 legacy chiamano le nuove API WCS con ambito di gestione del profilo come utente corrente. Questo approccio ha senso dal punto di vista dell'utente perché consente le impostazioni per utente da applicazioni legacy e anche l'esecuzione della maggior parte delle operazioni nel contesto LUA. o API ICM2 che funzionano nell'ambito a livello di sistema ? Si tratta di operazioni (profili di installazione e profili di disinstallazione) che supportano solo l'ambito a livello di sistema. Non vengono create nuove API di gestione dei profili WCS e le API esistenti possono essere modificate.

Le implementazioni sottostanti delle operazioni di gestione dei profili funzionano sulle entità di dati di configurazione seguenti per creare il contesto per gli algoritmi di elaborazione dei colori per fornire funzionalità di gestione dei colori. Si tratta di impostazioni specifiche del dispositivo o globali (indipendenti dal dispositivo). o Dati di configurazione specifici del dispositivo: ? Elenco di profili associati a un particolare dispositivo. ? Profilo predefinito per diversi tipi di profilo associati a un dispositivo. ? Modalità di corrispondenza dei profili utilizzati per l'enumerazione. o Dati di configurazione globali: ? Elenco dei profili installati nel sistema. ? Profilo predefinito globale per tipi di profilo diversi. ? Le implementazioni sottostanti dell'archiviazione dei dati di configurazione accettano l'ambito di archiviazione per i dati di configurazione (indipendenti dal dispositivo o specifici del dispositivo), che possono essere a livello di sistema o utente corrente. Questo è diverso dall'ambito di gestione dei profili. Un'operazione con ambito di gestione del profilo utente corrente può causare una lettura da un ambito di archiviazione a livello di sistema se l'impostazione dell'utente corrente per tale operazione non è presente. ? Il livello API ICM2/WCS chiama in questo livello di archiviazione per ottenere e impostare i dati con l'ambito di archiviazione appropriato. Il livello di archiviazione è trasparente per l'ambito di gestione dei profili. Logica per combinare i dati degli ambiti di archiviazione dell'utente corrente e a livello di sistema per creare o aggiornare una configurazione in base all'ambito di gestione dei profili specificato dal chiamante dell'API. Questa logica è presente nel livello API ICM2/WCS.

### <a name="device-specific-storage-layer"></a>Livello di archiviazione specifico del dispositivo

L'archiviazione per diverse classi di dispositivi, ad esempio stampa, acquisizione o visualizzazione, potrebbe essere diversa l'una dall'altra. Ad esempio, i dati di configurazione per un dispositivo di stampa devono essere archiviati usando API di stampa standard, ad esempio SetPrinterDataEx e GetPrinterDataEx, per consentire la copia dei profili e il trasferimento delle impostazioni in un computer client durante la connessione point-and-print. ? Questo livello esporta le funzionalità per aprire l'archivio, recuperare i dati, impostare i dati e chiudere l'archivio usando interfacce predefinite comuni in modo che il livello di archiviazione della configurazione di gestione dei profili possa chiamare in essi pur essendo trasparente per il modo in cui i dati vengono archiviati per tale dispositivo.

Nella figura seguente viene illustrata questa architettura.



Livello API pubblica di Gestione profili

${ROWSPAN2}$Legacy API ICM2 per operazioni che supportano solo l'ambito di gestione dei profili a livello di sistema in Vista (installazione, disinstallazione e ottenere la directory dei colori). Chiamano il livello di archiviazione della configurazione con l'ambito di archiviazione appropriato.${REMOVE}$  

API ICM2 legacy per operazioni che supportano l'ambito di gestione dei profili utente corrente e a livello di sistema in Vista (tutte le operazioni diverse da installazione, disinstallazione e ottenere la directory dei colori). Funzionano in modo implicito nell'ambito dell'utente corrente e chiamano una nuova API WCS con ambito di gestione dei profili come utente corrente.

Nuova API WCS con supporto dell'ambito di gestione dei profili utente corrente e a livello di sistema. Chiamano il livello di archiviazione della configurazione con l'ambito di archiviazione appropriato.



 



Configurazione della gestione dei profili Archiviazione livello

Routine di configurazione globale indipendenti dal dispositivo

Routine di configurazione specifiche del dispositivo

${ROWSPAN3}$Profile'installazione e gestione delle impostazioni predefinite del profilo indipendenti dal dispositivo, supportate nell'ambito di archiviazione a livello di sistema e utente corrente.${REMOVE}$  

Associazione dei dispositivi e gestione delle impostazioni del profilo predefinite specifiche del dispositivo, supportata nell'ambito di archiviazione a livello di sistema e utente corrente.

Device-Specific Archiviazione livello

Stampare risorse di archiviazione specifiche

Visualizzare risorse di archiviazione specifiche

Acquisire risorse di archiviazione specifiche



 

Le API ICM2 legacy per le operazioni che supportano solo l'ambito di gestione dei profili a livello di sistema in Vista non hanno modifiche nel comportamento. Le operazioni di installazione e disinstallazione rientrano in questa categoria.

Il comportamento delle API ICM2 legacy per le operazioni che supportano l'ambito di gestione del profilo utente corrente e a livello di sistema è stato modificato per eseguire query e configurare le impostazioni dell'utente corrente. Tutte le operazioni diverse da installazione e disinstallazione rientrano in questa categoria.

 

 




