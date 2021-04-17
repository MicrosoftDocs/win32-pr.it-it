---
title: Chiave AppID
description: Raggruppa le opzioni di configurazione per uno o più oggetti DCOM in una posizione centralizzata nel registro di sistema. Gli oggetti DCOM ospitati dallo stesso eseguibile sono raggruppati in un AppID per semplificare la gestione delle impostazioni di configurazione e della sicurezza comuni.
ms.assetid: 4e3d8c87-e6d7-4b4d-8f72-7180be1e51cf
keywords:
- Chiave del registro di sistema AppID COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b283a9cc47907cf418c2d7d6d613d151c7e5c5e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399794"
---
# <a name="appid-key"></a>Chiave AppID

Raggruppa le opzioni di configurazione per uno o più oggetti DCOM in una posizione centralizzata nel registro di sistema. Gli oggetti DCOM ospitati dallo stesso eseguibile sono raggruppati in un AppID per semplificare la gestione delle impostazioni di configurazione e della sicurezza comuni.

## <a name="registry-key"></a>Chiave del Registro di sistema

**HKEY \_ \_Classi software del computer locale \\ \\ \\ AppID** \\ *{* AppID \_ GUID *}*



| Valore del Registro di sistema                                           | Descrizione                                                                                                                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessPermission**](accesspermission.md)             | Descrive l'elenco di controllo di accesso (ACL) delle entità che possono accedere alle istanze di questa classe. Questo ACL viene usato solo da applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). |
| [**ActivateAtStorage**](activateatstorage.md)           | Configura il client per creare un'istanza degli oggetti nello stesso computer dello stato persistente utilizzato o da cui vengono inizializzati.                                                                    |
| [**AppID**](appid.md)                                   | Identifica il GUID AppID che corrisponde al file eseguibile denominato.                                                                                                                                             |
| [**AppIDFlags**](appidflags.md)                         | Configura il modo in cui un server COM configurato per l'esecuzione come "utente interattivo" verrà avviato o associato da un client in un desktop non predefinito.                                                              |
| [**AuthenticationLevel**](authenticationlevel.md)       | Imposta il livello di autenticazione per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o per le applicazioni che chiamano **CoInitializeSecurity** e specificano un AppID.               |
| [**DllSurrogate**](dllsurrogate.md)                     | Consente l'esecuzione di server DLL in un processo surrogato. Se viene specificata una stringa vuota, viene utilizzato il surrogato fornito dal sistema; in caso contrario, il valore specifica il percorso del surrogato da usare.                 |
| [**DllSurrogateExecutable**](dllsurrogateexecutable.md) | Consente l'esecuzione dei server DLL in un processo surrogato personalizzato, insieme al valore del registro di sistema [**DllSurrogate**](dllsurrogate.md) .                                                                          |
| [**Endpoint**](endpoints.md)                           | Configura un'applicazione COM per l'utilizzo di un numero di porta TCP specificato per le comunicazioni DCOM.                                                                                                                        |
| [**LaunchPermission**](launchpermission.md)             | Descrive l'elenco di controllo di accesso (ACL) delle entità che possono avviare nuovi server per questa classe.                                                                                                            |
| [**LoadUserSettings**](loadusersettings.md)             | Determina se COM caricherà il profilo utente per i server COM in esecuzione come identità dell'applicazione di avvio dell'utente.                                                                                           |
| [**LocalService**](localservice.md)                     | Installa un oggetto come applicazione di servizio.                                                                                                                                                                    |
| [**PreferredServerBitness**](preferredserverbitness.md) | Imposta l'architettura preferita, a 32 bit o a 64 bit, per questo server COM.                                                                                                                                         |
| [**RemoteServerName**](remoteservername.md)             | Configura il client per richiedere che l'oggetto venga eseguito in un determinato computer ogni volta che viene chiamata una funzione di attivazione per la quale non è specificata una struttura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) .              |
| [**ROTFlags**](rotflags.md)                             | Controlla la registrazione di un server COM nella tabella degli oggetti in esecuzione (ROT).                                                                                                                                    |
| [**RunAs**](runas.md)                                   | Configura una classe per l'esecuzione con un account utente specifico quando viene attivato da un client remoto senza essere scritto come applicazione di servizio.                                                                       |
| [**ServiceParameters**](serviceparameters.md)           | Specifica i parametri della riga di comando da passare a un oggetto installato per l'uso da parte di COM tramite il valore del registro di sistema [**LocalService**](localservice.md) .                                                       |
| [**SRPTrustLevel**](srptrustlevel.md)                   | Imposta il livello di attendibilità del criterio di restrizione software per le applicazioni.                                                                                                                                        |



 

## <a name="remarks"></a>Commenti

Per gli AppID viene eseguito il mapping a file eseguibili e classi utilizzando due meccanismi diversi:

-   Utilizzando un identificatore univoco globale (GUID) a 128 bit che identifica la chiave **AppID** . Una classe indica l'AppID corrispondente sotto la chiave [**CLSID**](clsid-key-hklm.md) in un valore denominato "AppID". Questo mapping viene utilizzato durante l'attivazione.
-   Utilizzando un valore denominato che indica un nome eseguibile, ad esempio "MYOLDAPP.EXE". Questo valore denominato è di tipo **reg \_ SZ** e contiene la rappresentazione di stringa dell'AppID associato al file eseguibile. Questo mapping viene usato per ottenere le autorizzazioni di accesso predefinite e il livello di autenticazione.

La chiave delle **\_ \_ \\ \\ classi software del computer locale HKEY** corrisponde alla chiave **\_ \_ radice delle classi HKEY** , che è stata mantenuta per la compatibilità con le versioni precedenti di com.

Per i server COM, il mapping viene in genere generato e scritto nel registro di sistema durante il processo di registrazione o durante l'esecuzione di dcomcnfg.exe. Tuttavia, i client COM che desiderano impostare la sicurezza tramite la chiave **AppID** devono creare chiavi del registro di sistema appropriate e specificare il mapping necessario chiamando le [funzioni del registro di sistema](/windows/desktop/SysInfo/registry-functions) o utilizzando Regedit.exe. È quindi possibile impostare valori come [**AccessPermission**](accesspermission.md) o [**AuthenticationLevel**](authenticationlevel.md) per il client. Si supponga, ad esempio, che il nome del file eseguibile per il processo client sia "YourClient.exe" e che si desideri impostare il livello di autenticazione su "None". Usare Guidgen.exe o Uuidgen.exe per creare il GUID che è l'AppID per il file eseguibile. Impostare quindi i valori nel registro di sistema, come illustrato nell'esempio seguente, in cui 00000001 rappresenta un livello di autenticazione "None":

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {MyGuid}
      AuthenticationLevel = 00000001
   MyClient.exe
      AppID = {MyGUID}
```

 

 