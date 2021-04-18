---
title: Enumerazione MPTHREAT_CATEGORY (MpClient. h)
description: Possibili categorie di minacce.
ms.assetid: 478ED59E-5D3C-43B3-A89D-44A649EDD086
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPTHREAT_CATEGORY
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPTHREAT_CATEGORY
topic_type:
- apiref
api_name:
- MPTHREAT_CATEGORY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a149ef6ce6ebadacbac6f0dd35247d793ca7000
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301406"
---
# <a name="mpthreat_category-enumeration"></a>\_Enumerazione categoria MPTHREAT

Possibili categorie di minacce.

## <a name="syntax"></a>Sintassi

```C++
typedef enum tagMPTHREAT_CATEGORY {
  MP_THREAT_CATEGORY_INVALID                    = 0,
  MP_THREAT_CATEGORY_ADWARE                     = 1,
  MP_THREAT_CATEGORY_SPYWARE                    = 2,
  MP_THREAT_CATEGORY_PASSWORDSTEALER            = 3,
  MP_THREAT_CATEGORY_TROJANDOWNLOADER           = 4,
  MP_THREAT_CATEGORY_WORM                       = 5,
  MP_THREAT_CATEGORY_BACKDOOR                   = 6,
  MP_THREAT_CATEGORY_REMOTEACCESSTROJAN         = 7,
  MP_THREAT_CATEGORY_TROJAN                     = 8,
  MP_THREAT_CATEGORY_EMAILFLOODER               = 9,
  MP_THREAT_CATEGORY_KEYLOGGER                  = 10,
  MP_THREAT_CATEGORY_DIALER                     = 11,
  MP_THREAT_CATEGORY_MONITORINGSOFTWARE         = 12,
  MP_THREAT_CATEGORY_BROWSERMODIFIER            = 13,
  MP_THREAT_CATEGORY_COOKIE                     = 14,
  MP_THREAT_CATEGORY_BROWSERPLUGIN              = 15,
  MP_THREAT_CATEGORY_AOLEXPLOIT                 = 16,
  MP_THREAT_CATEGORY_NUKER                      = 17,
  MP_THREAT_CATEGORY_SECURITYDISABLER           = 18,
  MP_THREAT_CATEGORY_JOKEPROGRAM                = 19,
  MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL      = 20,
  MP_THREAT_CATEGORY_SOFTWAREBUNDLER            = 21,
  MP_THREAT_CATEGORY_STEALTHNOTIFIER            = 22,
  MP_THREAT_CATEGORY_SETTINGSMODIFIER           = 23,
  MP_THREAT_CATEGORY_TOOLBAR                    = 24,
  MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE      = 25,
  MP_THREAT_CATEGORY_TROJANFTP                  = 26,
  MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE  = 27,
  MP_THREAT_CATEGORY_ICQEXPLOIT                 = 28,
  MP_THREAT_CATEGORY_TROJANTELNET               = 29,
  MP_THREAT_CATEGORY_EXPLOIT                    = 30,
  MP_THREAT_CATEGORY_FILESHARINGPROGRAM         = 31,
  MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL      = 32,
  MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE    = 33,
  MP_THREAT_CATEGORY_TOOL                       = 34,
  MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE     = 36,
  MP_THREAT_CATEGORY_TROJAN_DROPPER             = 37,
  MP_THREAT_CATEGORY_TROJAN_MASSMAILER          = 38,
  MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE  = 39,
  MP_THREAT_CATEGORY_TROJAN_PROXYSERVER         = 40,
  MP_THREAT_CATEGORY_VIRUS                      = 42,
  MP_THREAT_CATEGORY_KNOWN                      = 43,
  MP_THREAT_CATEGORY_UNKNOWN                    = 44,
  MP_THREAT_CATEGORY_SPP                        = 45,
  MP_THREAT_CATEGORY_BEHAVIOR                   = 46,
  MP_THREAT_CATEGORY_VULNERABILTIY              = 47,
  MP_THREAT_CATEGORY_POLICY                     = 48
} MPTHREAT_CATEGORY, *PMPTHREAT_CATEGORY;
```

## <a name="constants"></a>Costanti

Categoria minacce | Descrizione
-|-
<span id="MP_THREAT_CATEGORY_INVALID"></span><span id="mp_threat_category_invalid"></span>**MP \_ categoria di minacce \_ \_ non valida** | La categoria di minacce non esiste o è stata digitata in errore.
<span id="MP_THREAT_CATEGORY_ADWARE"></span><span id="mp_threat_category_adware"></span>**MP \_ categoria di minacce \_ \_ adware** | Applicazione potenzialmente indesiderata che Visualizza annunci.
<span id="MP_THREAT_CATEGORY_SPYWARE"></span><span id="mp_threat_category_spyware"></span>**MP \_ \_ \_ spyware categoria di minacce** | Malware che trasmette informazioni sul dispositivo o sull'utente, senza il consenso o la conoscenza dell'utente.
<span id="MP_THREAT_CATEGORY_PASSWORDSTEALER"></span><span id="mp_threat_category_passwordstealer"></span>**MP \_ categoria di minacce \_ \_ PASSWORDSTEALER** | Un'applicazione che raccoglie e/o trasmette una password a un utente malintenzionato.
<span id="MP_THREAT_CATEGORY_TROJANDOWNLOADER"></span><span id="mp_threat_category_trojandownloader"></span>**\_categoria di minacce MP \_ \_ TROJANDOWNLOADER** | Trojan che Scarica malware o applicazioni potenzialmente indesiderate in un dispositivo infetto.
<span id="MP_THREAT_CATEGORY_WORM"></span><span id="mp_threat_category_worm"></span>**MP \_ \_ \_ worm categoria minacce** | Software dannoso con propagazione automatica che può distribuirsi automaticamente tramite connessioni di rete.
<span id="MP_THREAT_CATEGORY_BACKDOOR"></span><span id="mp_threat_category_backdoor"></span>**\_ \_ backdoor categoria di minacce MP \_** | Malware che fornisce un mezzo per ignorare i normali protocolli di sicurezza e autenticazione in un dispositivo.
<span id="MP_THREAT_CATEGORY_REMOTEACCESSTROJAN"></span><span id="mp_threat_category_remoteaccesstrojan"></span>**MP \_ categoria di minacce \_ \_ REMOTEACCESSTROJAN** | Trojan che consente l'accesso remoto a un computer.
<span id="MP_THREAT_CATEGORY_TROJAN"></span><span id="mp_threat_category_trojan"></span>**\_ \_ Trojan categoria di minacce MP \_** | Software dannoso che si maschera come software legittimo.
<span id="MP_THREAT_CATEGORY_EMAILFLOODER"></span><span id="mp_threat_category_emailflooder"></span>**MP \_ categoria di minacce \_ \_ EMAILFLOODER** | Malware Invia un volume elevato di messaggi di posta elettronica a una destinazione.
<span id="MP_THREAT_CATEGORY_KEYLOGGER"></span><span id="mp_threat_category_keylogger"></span>**MP \_ categoria di minacce \_ \_ Keylogger** | Malware che registra le sequenze di tasti dell'utente, rubando potenzialmente le password e altri dati sensibili.
<span id="MP_THREAT_CATEGORY_DIALER"></span><span id="mp_threat_category_dialer"></span>**MP \_ \_ \_ dialer categoria di minacce** | Malware che effettua chiamate telefoniche non autorizzate, spesso a tariffe Premium.
<span id="MP_THREAT_CATEGORY_MONITORINGSOFTWARE"></span><span id="mp_threat_category_monitoringsoftware"></span>**MP \_ categoria di minacce \_ \_ MONITORINGSOFTWARE** | Applicazione potenzialmente indesiderata che monitora l'attività degli utenti, ad esempio il tipo di utente sulla tastiera o sulle visualizzazioni sullo schermo.
<span id="MP_THREAT_CATEGORY_BROWSERMODIFIER"></span><span id="mp_threat_category_browsermodifier"></span>**MP \_ categoria di minacce \_ \_ BROWSERMODIFIER** | Applicazione potenzialmente indesiderata che modifica le impostazioni del Web browser senza il consenso dell'utente.
<span id="MP_THREAT_CATEGORY_COOKIE"></span><span id="mp_threat_category_cookie"></span>**MP \_ \_ \_ cookie categoria minacce** | Dati inviati da un server Web a un browser, consentendo di salvare le informazioni sull'utente, ad esempio le impostazioni dell'applicazione Web, sulle visite ripetute.
<span id="MP_THREAT_CATEGORY_BROWSERPLUGIN"></span><span id="mp_threat_category_browserplugin"></span>**MP \_ categoria di minacce \_ \_ BROWSERPLUGIN** | Software che consente a un Web browser standard di visualizzare ed eseguire tipi di contenuto specifici, ad esempio file multimediali, immagini animate e moduli interattivi.
<span id="MP_THREAT_CATEGORY_AOLEXPLOIT"></span><span id="mp_threat_category_aolexploit"></span>**MP \_ categoria di minacce \_ \_ AOLEXPLOIT** | Malware che attacca gli utenti del servizio Internet AOL, spesso recuperando le password o modificando le impostazioni.
<span id="MP_THREAT_CATEGORY_NUKER"></span><span id="mp_threat_category_nuker"></span>**MP \_ \_ \_ Nuker categoria di minacce** | Malware progettato per l'arresto anomalo di un dispositivo o per renderlo meno stabile.
<span id="MP_THREAT_CATEGORY_SECURITYDISABLER"></span><span id="mp_threat_category_securitydisabler"></span>**MP \_ categoria di minacce \_ \_ SECURITYDISABLER** | Malware che disabilita le impostazioni di sicurezza o i prodotti.
<span id="MP_THREAT_CATEGORY_JOKEPROGRAM"></span><span id="mp_threat_category_jokeprogram"></span>**MP \_ categoria di minacce \_ \_ JOKEPROGRAM** | Un'applicazione progettata per divertire o spaventare un utente, senza danneggiare effettivamente il dispositivo.
<span id="MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL"></span><span id="mp_threat_category_hostileactivexcontrol"></span>**MP \_ categoria di minacce \_ \_ HOSTILEACTIVEXCONTROL** | Controllo ActiveX progettato da un utente malintenzionato per danneggiare un dispositivo. Un controllo ActiveX è un tipo di componente aggiuntivo del browser specifico di Internet Explorer.
<span id="MP_THREAT_CATEGORY_SOFTWAREBUNDLER"></span><span id="mp_threat_category_softwarebundler"></span>**MP \_ categoria di minacce \_ \_ SOFTWAREBUNDLER** | Software che installa altre applicazioni potenzialmente indesiderate, ad esempio adware o spyware. Il contratto di licenza del software per la creazione di bundle potrebbe richiedere tali componenti per funzionare.
<span id="MP_THREAT_CATEGORY_STEALTHNOTIFIER"></span><span id="mp_threat_category_stealthnotifier"></span>**MP \_ categoria di minacce \_ \_ STEALTHNOTIFIER** | Malware che si connette a un server remoto tramite una connessione Stealth per notificare a un utente malintenzionato l'installazione del malware.
<span id="MP_THREAT_CATEGORY_SETTINGSMODIFIER"></span><span id="mp_threat_category_settingsmodifier"></span>**MP \_ categoria di minacce \_ \_ malware SettingsModifier** | Applicazione potenzialmente indesiderata che modifica le impostazioni di un utente senza la conoscenza o il consenso dell'utente.
<span id="MP_THREAT_CATEGORY_TOOLBAR"></span><span id="mp_threat_category_toolbar"></span>**MP \_ \_ \_ barra degli strumenti categoria minaccia** | Un'applicazione potenzialmente indesiderata (PUA) che installa una barra degli strumenti nel Web browser dell'utente; spesso in bundle con PUA aggiuntivi, ad esempio adware.
<span id="MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE"></span><span id="mp_threat_category_remotecontrolsoftware"></span>**MP \_ categoria di minacce \_ \_ REMOTECONTROLSOFTWARE** | Applicazione potenzialmente indesiderata che consente l'accesso remoto a un dispositivo.
<span id="MP_THREAT_CATEGORY_TROJANFTP"></span><span id="mp_threat_category_trojanftp"></span>**MP \_ categoria di minacce \_ \_ TROJANFTP** | Trojan che usa un server FTP per consentire a un utente malintenzionato di caricare o scaricare file da un dispositivo.
<span id="MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE"></span><span id="mp_threat_category_potentialunwantedsoftware"></span>**MP \_ categoria di minacce \_ \_ POTENTIALUNWANTEDSOFTWARE** | Noto anche come *applicazione potenzialmente indesiderata* o *PUA*; software che può comportarsi in modo eccessivamente intrusivo, che è possibile che l'utente non sia stato previsto o completamente autorizzato.
<span id="MP_THREAT_CATEGORY_ICQEXPLOIT"></span><span id="mp_threat_category_icqexploit"></span>**MP \_ categoria di minacce \_ \_ ICQEXPLOIT** | Trojan che attacca il servizio di messaggistica ICQ, spesso recuperando le password o manomettendo le impostazioni.
<span id="MP_THREAT_CATEGORY_TROJANTELNET"></span><span id="mp_threat_category_trojantelnet"></span>**MP \_ categoria di minacce \_ \_ TROJANTELNET** | Trojan che installa un server Telnet sul computer di un utente senza la conoscenza o il consenso dell'utente.
<span id="MP_THREAT_CATEGORY_EXPLOIT"></span><span id="mp_threat_category_exploit"></span>**MP \_ \_ \_ exploit categoria di minacce** | Codice dannoso che sfrutta una vulnerabilità in un dispositivo o in un sistema.
<span id="MP_THREAT_CATEGORY_FILESHARINGPROGRAM"></span><span id="mp_threat_category_filesharingprogram"></span>**MP \_ categoria di minacce \_ \_ FILESHARINGPROGRAM** | Un'applicazione potenzialmente indesiderata che apre un dispositivo alla condivisione peer-to-peer dei file del dispositivo.
<span id="MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL"></span><span id="mp_threat_category_malware_creation_tool"></span>**MP \_ \_strumento di \_ \_ creazione malware \_ per categoria minacce** | Un'applicazione in grado di generare automaticamente file dannosi.
<span id="MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE"></span><span id="mp_threat_category_remote_control_software"></span>**MP \_ categoria di minacce \_ \_ \_ \_ software di controllo remoto** | Applicazione potenzialmente indesiderata che consente l'accesso remoto a un dispositivo.
<span id="MP_THREAT_CATEGORY_TOOL"></span><span id="mp_threat_category_tool"></span>**MP \_ \_ \_ strumento categoria minacce** | Utilità che consente a un utente malintenzionato di eseguire azioni dannose su un dispositivo.
<span id="MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE"></span><span id="mp_threat_category_trojan_denialofservice"></span>**MP \_ categoria di minacce \_ \_ Trojan \_ DENIALOFSERVICE** | Trojan progettato per inviare un volume elevato di richieste di rete a una destinazione come parte di un attacco Denial of Service (DoS).
<span id="MP_THREAT_CATEGORY_TROJAN_DROPPER"></span><span id="mp_threat_category_trojan_dropper"></span>**MP \_ categoria di minacce \_ \_ Trojan \_ Dropper** | Trojan che Scarica e installa malware o applicazioni potenzialmente indesiderate in una destinazione.
<span id="MP_THREAT_CATEGORY_TROJAN_MASSMAILER"></span><span id="mp_threat_category_trojan_massmailer"></span>**MP \_ categoria di minacce \_ \_ Trojan \_ MASSMAILER** | Trojan che invia un volume elevato di messaggi di posta elettronica a una destinazione, destinati a sovraccaricare la posta in arrivo della destinazione.
<span id="MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE"></span><span id="mp_threat_category_trojan_monitoringsoftware"></span>**MP \_ categoria di minacce \_ \_ Trojan \_ MONITORINGSOFTWARE** | Trojan che monitora l'attività degli utenti, ad esempio il tipo di utente sulla tastiera o sulle visualizzazioni sullo schermo.
<span id="MP_THREAT_CATEGORY_TROJAN_PROXYSERVER"></span><span id="mp_threat_category_trojan_proxyserver"></span>**MP \_ categoria di minacce \_ \_ Trojan \_ PROXYSERVER** | Un server proxy installato da un Trojan, che fornisce una connessione internet ininterrotta, consentendo al contempo l'accesso non autorizzato al dispositivo infetto.
<span id="MP_THREAT_CATEGORY_VIRUS"></span><span id="mp_threat_category_virus"></span>**MP \_ \_ \_ virus categoria minacce** | Malware che esegue la replica, in genere infettando altri file nel sistema, consentendo così l'esecuzione del codice malware e la relativa propagazione quando questi file sono attivati.
<span id="MP_THREAT_CATEGORY_KNOWN"></span><span id="mp_threat_category_known"></span>**MP \_ categoria di minacce \_ \_ Nota** | Minaccia malware non specificata.
<span id="MP_THREAT_CATEGORY_UNKNOWN"></span><span id="mp_threat_category_unknown"></span>**MP \_ \_categoria minaccia \_ sconosciuta** | Minaccia malware non specificata che non è stata ancora definita.
<span id="MP_THREAT_CATEGORY_SPP"></span><span id="mp_threat_category_spp"></span>**MP \_ categoria di minacce \_ \_ spp** | Tecnologia anti-pirateria che richiede l'attivazione di ogni installazione di un prodotto Windows con Microsoft.
<span id="MP_THREAT_CATEGORY_BEHAVIOR"></span><span id="mp_threat_category_behavior"></span>**MP \_ \_ \_ comportamento della categoria di minacce** | Tipo di rilevamento basato su azioni file spesso associate a attività dannose.
<span id="MP_THREAT_CATEGORY_VULNERABILTIY"></span><span id="mp_threat_category_vulnerabiltiy"></span>**MP \_ categoria di minacce \_ \_ VULNERABILTIY** | Qualsiasi debolezza, processo amministrativo o attività che rende un dispositivo suscettibile di sfruttare una minaccia.
<span id="MP_THREAT_CATEGORY_POLICY"></span><span id="mp_threat_category_policy"></span>**MP \_ \_ \_ criteri categoria minacce** | Set di regole definito da un amministratore che controlla le funzionalità nei dispositivi desktop e mobili, ad esempio gli aggiornamenti software.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato | Windows 8 (solo app desktop) |
| Server minimo supportato | Windows Server 2012 (solo app desktop) |
| Intestazione | MpClient. h |
