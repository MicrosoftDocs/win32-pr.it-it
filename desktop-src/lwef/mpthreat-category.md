---
title: MPTHREAT_CATEGORY enumerazione (MpClient.h)
description: Possibili categorie di minacce.
ms.assetid: 478ED59E-5D3C-43B3-A89D-44A649EDD086
keywords:
- MPTHREAT_CATEGORY funzionalità dell'ambiente Windows legacy
- PMPTHREAT_CATEGORY puntatore di enumerazione Legacy Windows Environment Features
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
ms.openlocfilehash: 70cfd95de751d51be3ab4b61bc361687738422a6d31c234576e812efcd57bd4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975971"
---
# <a name="mpthreat_category-enumeration"></a>Enumerazione MPTHREAT \_ CATEGORY

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

Categoria di minaccia | Descrizione
-|-
<span id="MP_THREAT_CATEGORY_INVALID"></span><span id="mp_threat_category_invalid"></span>**Mp \_ CATEGORIA DI \_ MINACCIA \_ NON VALIDA** | La categoria di minaccia non esiste o è stata digitata in modo errato.
<span id="MP_THREAT_CATEGORY_ADWARE"></span><span id="mp_threat_category_adware"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCE ADWARE** | Un'applicazione potenzialmente indesiderata che visualizza annunci pubblicitari.
<span id="MP_THREAT_CATEGORY_SPYWARE"></span><span id="mp_threat_category_spyware"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCE SPYWARE** | Malware che trasmette informazioni sul dispositivo o sull'utente, senza il consenso o le conoscenze dell'utente.
<span id="MP_THREAT_CATEGORY_PASSWORDSTEALER"></span><span id="mp_threat_category_passwordstealer"></span>**Mp \_ PASSWORD \_ DELLE CATEGORIE DI \_ MINACCETEALER** | Applicazione che raccoglie e/o trasmette una password a un utente malintenzionato.
<span id="MP_THREAT_CATEGORY_TROJANDOWNLOADER"></span><span id="mp_threat_category_trojandownloader"></span>**MP \_ THREAT \_ CATEGORY \_ TROJANDOWNLOADER** | Un trojan che scarica malware o applicazioni potenzialmente indesiderate in un dispositivo infetto.
<span id="MP_THREAT_CATEGORY_WORM"></span><span id="mp_threat_category_worm"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCE WORM** | Software dannoso auto-propagato in grado di distribuirsi automaticamente tramite connessioni di rete.
<span id="MP_THREAT_CATEGORY_BACKDOOR"></span><span id="mp_threat_category_backdoor"></span>**MP \_ THREAT \_ CATEGORY \_ BACKDOOR** | Malware che consente di ignorare i normali protocolli di sicurezza e autenticazione in un dispositivo.
<span id="MP_THREAT_CATEGORY_REMOTEACCESSTROJAN"></span><span id="mp_threat_category_remoteaccesstrojan"></span>**Mp \_ CATEGORIA \_ DI MINACCIA \_ REMOTEACCESSTROJAN** | Un trojan che fornisce l'accesso remoto a un computer.
<span id="MP_THREAT_CATEGORY_TROJAN"></span><span id="mp_threat_category_trojan"></span>**MP \_ THREAT \_ CATEGORY \_ TROJAN** | Software dannoso che si nasconde come software legittimo.
<span id="MP_THREAT_CATEGORY_EMAILFLOODER"></span><span id="mp_threat_category_emailflooder"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCE EMAILFLOODER** | Il malware invia un volume elevato di messaggi di posta elettronica a una destinazione.
<span id="MP_THREAT_CATEGORY_KEYLOGGER"></span><span id="mp_threat_category_keylogger"></span>**Mp \_ KEYLOGGER \_ DELLA \_ CATEGORIA DI MINACCE** | Malware che registra le sequenze di tasti dell'utente, potenzialmente rubando password e altri dati sensibili.
<span id="MP_THREAT_CATEGORY_DIALER"></span><span id="mp_threat_category_dialer"></span>**Mp \_ DIALER \_ DELLA \_ CATEGORIA DI MINACCE** | Malware che effettua chiamate telefoniche non autorizzate, spesso a tariffe Premium.
<span id="MP_THREAT_CATEGORY_MONITORINGSOFTWARE"></span><span id="mp_threat_category_monitoringsoftware"></span>**Mp \_ MONITORAGGIO \_ DELLE CATEGORIE DI \_ MINACCESOFTWARE** | Un'applicazione potenzialmente indesiderata che monitora l'attività dell'utente, ad esempio ciò che l'utente dise imposta sulla tastiera o sulle visualizzazioni sullo schermo.
<span id="MP_THREAT_CATEGORY_BROWSERMODIFIER"></span><span id="mp_threat_category_browsermodifier"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCE BROWSERMODIFIER** | Applicazione potenzialmente indesiderata che modifica le impostazioni del Web browser senza il consenso dell'utente.
<span id="MP_THREAT_CATEGORY_COOKIE"></span><span id="mp_threat_category_cookie"></span>**Mp \_ COOKIE DELLA \_ CATEGORIA \_ DI MINACCE** | Dati inviati da un server Web a un browser, consentendo di salvare le informazioni sull'utente, ad esempio le impostazioni dell'applicazione Web, in visite ripetute.
<span id="MP_THREAT_CATEGORY_BROWSERPLUGIN"></span><span id="mp_threat_category_browserplugin"></span>**Mp \_ BROWSER \_ CATEGORIA \_ DI MINACCEPLUGIN** | Software che consente a un Web browser standard di visualizzare ed eseguire tipi specifici di contenuto, ad esempio file multimediali, immagini animate e moduli interattivi.
<span id="MP_THREAT_CATEGORY_AOLEXPLOIT"></span><span id="mp_threat_category_aolexploit"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCIA AOLEXPLOIT** | Malware che attacchi gli utenti del servizio Internet AOL, spesso recuperando le password o modificando le impostazioni.
<span id="MP_THREAT_CATEGORY_NUKER"></span><span id="mp_threat_category_nuker"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCE NUKER** | Malware progettato per l'arresto anomalo di un dispositivo o per renderlo meno stabile.
<span id="MP_THREAT_CATEGORY_SECURITYDISABLER"></span><span id="mp_threat_category_securitydisabler"></span>**Mp \_ SICUREZZA \_ DELLA CATEGORIA DI \_ MINACCEDISABLER** | Malware che disabilita le impostazioni di sicurezza o i prodotti.
<span id="MP_THREAT_CATEGORY_JOKEPROGRAM"></span><span id="mp_threat_category_jokeprogram"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCIAPROGRAMMA** | Un'applicazione progettata per l'uso o la spavento di un utente, senza danneggiare effettivamente il dispositivo.
<span id="MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL"></span><span id="mp_threat_category_hostileactivexcontrol"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCIA EREMITAACTIVEXCONTROL** | Controllo ActiveX progettato da un utente malintenzionato per danneggiare un dispositivo. Un ActiveX è un tipo di componente aggiuntivo del browser specifico per Internet Explorer.
<span id="MP_THREAT_CATEGORY_SOFTWAREBUNDLER"></span><span id="mp_threat_category_softwarebundler"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCE SOFTWAREBUNDLER** | Software che installa altre applicazioni potenzialmente indesiderate, ad esempio adware o spyware. Il contratto di licenza del software di creazione di aggregazione può richiedere questi altri componenti per funzionare.
<span id="MP_THREAT_CATEGORY_STEALTHNOTIFIER"></span><span id="mp_threat_category_stealthnotifier"></span>**Mp \_ MASCHERATORE \_ CATEGORIA \_ DI MINACCENOTIFIER** | Malware che si connette a un server remoto tramite una connessione maschera per notificare a un utente malintenzionato che il malware è stato installato.
<span id="MP_THREAT_CATEGORY_SETTINGSMODIFIER"></span><span id="mp_threat_category_settingsmodifier"></span>**Mp \_ IMPOSTAZIONI \_ DELLE CATEGORIE DI \_ MINACCEMODIFICATORE** | Un'applicazione potenzialmente indesiderata che modifica le impostazioni di un utente senza che l'utente ne sia a conoscenza o consenziente.
<span id="MP_THREAT_CATEGORY_TOOLBAR"></span><span id="mp_threat_category_toolbar"></span>**Mp \_ BARRA DEGLI \_ STRUMENTI DELLE CATEGORIE DI \_ MINACCE** | Un'applicazione potenzialmente indesiderata (PUA) che installa una barra degli strumenti nel Web browser dell'utente; spesso in bundle con puA aggiuntive, ad esempio adware.
<span id="MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE"></span><span id="mp_threat_category_remotecontrolsoftware"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCE REMOTECONTROLSOFTWARE** | Un'applicazione potenzialmente indesiderata che fornisce l'accesso remoto a un dispositivo.
<span id="MP_THREAT_CATEGORY_TROJANFTP"></span><span id="mp_threat_category_trojanftp"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCE TROJANFTP** | Un trojan che usa un server FTP per consentire a un utente malintenzionato di caricare o scaricare file da un dispositivo.
<span id="MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE"></span><span id="mp_threat_category_potentialunwantedsoftware"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCIA POTENTIALUNWANTEDSOFTWARE** | Noto anche come *applicazione potenzialmente indesiderata o* *PUA.* software che può comportarsi in modo esente da intrusive, che l'utente potrebbe non avere previsto o a cui l'utente ha dato il consenso completo.
<span id="MP_THREAT_CATEGORY_ICQEXPLOIT"></span><span id="mp_threat_category_icqexploit"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCE ICQEXPLOIT** | Un trojan che attacchi il servizio di messaggistica ICQ, spesso recuperando password o manomissioni delle impostazioni.
<span id="MP_THREAT_CATEGORY_TROJANTELNET"></span><span id="mp_threat_category_trojantelnet"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCIA TROJANTELNET** | Un trojan che installa un server telnet nel computer di un utente senza che l'utente ne sia a conoscenza o consenziente.
<span id="MP_THREAT_CATEGORY_EXPLOIT"></span><span id="mp_threat_category_exploit"></span>**Mp \_ EXPLOIT \_ DELLA CATEGORIA DI \_ MINACCE** | Codice dannoso che sfrutta una vulnerabilità in un dispositivo o in un sistema.
<span id="MP_THREAT_CATEGORY_FILESHARINGPROGRAM"></span><span id="mp_threat_category_filesharingprogram"></span>**Mp \_ FILE \_ DELLE CATEGORIE DI \_ MINACCEHARINGPROGRAM** | Un'applicazione potenzialmente indesiderata che apre un dispositivo alla condivisione peer-to-peer dei file del dispositivo.
<span id="MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL"></span><span id="mp_threat_category_malware_creation_tool"></span>**Mp \_ STRUMENTO DI \_ CREAZIONE MALWARE PER CATEGORIA DI \_ \_ \_ MINACCE** | Un'applicazione in grado di generare automaticamente file dannosi.
<span id="MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE"></span><span id="mp_threat_category_remote_control_software"></span>**Mp \_ CATEGORIA \_ DI MINACCE SOFTWARE DI CONTROLLO \_ \_ \_ REMOTO** | Un'applicazione potenzialmente indesiderata che consente l'accesso remoto a un dispositivo.
<span id="MP_THREAT_CATEGORY_TOOL"></span><span id="mp_threat_category_tool"></span>**Mp \_ STRUMENTO CATEGORIA \_ \_ DI MINACCE** | Utilità che consente a un utente malintenzionato di eseguire azioni dannose su un dispositivo.
<span id="MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE"></span><span id="mp_threat_category_trojan_denialofservice"></span>**Mp \_ CATEGORIA DI \_ \_ MINACCIA TROJAN \_ DENIALOFSERVICE** | Un trojan progettato per inviare un volume elevato di richieste di rete a una destinazione come parte di un attacco Denial of Service (DoS).
<span id="MP_THREAT_CATEGORY_TROJAN_DROPPER"></span><span id="mp_threat_category_trojan_dropper"></span>**Mp \_ THREAT \_ CATEGORY \_ TROJAN \_ DROPPER** | Un trojan che scarica e installa malware o applicazioni potenzialmente indesiderate in una destinazione.
<span id="MP_THREAT_CATEGORY_TROJAN_MASSMAILER"></span><span id="mp_threat_category_trojan_massmailer"></span>**Mp \_ CATEGORIA DI \_ \_ MINACCIA TROJAN \_ MASSMAILER** | Un trojan che invia un volume elevato di messaggi di posta elettronica a una destinazione, destinato a sovraccaricare la posta in arrivo della destinazione.
<span id="MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE"></span><span id="mp_threat_category_trojan_monitoringsoftware"></span>**Mp \_ CATEGORIA \_ DI MINACCE TROJAN \_ \_ MONITORINGSOFTWARE** | Un trojan che monitora l'attività dell'utente, ad esempio ciò che l'utente ha sulla tastiera o le visualizzazioni sullo schermo.
<span id="MP_THREAT_CATEGORY_TROJAN_PROXYSERVER"></span><span id="mp_threat_category_trojan_proxyserver"></span>**Mp \_ CATEGORIA DI \_ \_ MINACCE TROJAN \_ PROXYSERVER** | Un server proxy installato da un trojan, che fornisce una connessione Internet senza interruzioni, consentendo l'accesso non autorizzato al dispositivo infetto.
<span id="MP_THREAT_CATEGORY_VIRUS"></span><span id="mp_threat_category_virus"></span>**Mp \_ VIRUS \_ DELLA CATEGORIA DI \_ MINACCE** | Malware che viene replicato, comunemente infettando altri file nel sistema, consentendo così l'esecuzione del codice malware e la sua propagazione quando tali file vengono attivati.
<span id="MP_THREAT_CATEGORY_KNOWN"></span><span id="mp_threat_category_known"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCIA NOTA** | Minaccia malware non specificata.
<span id="MP_THREAT_CATEGORY_UNKNOWN"></span><span id="mp_threat_category_unknown"></span>**Mp \_ CATEGORIA DI \_ MINACCIA \_ SCONOSCIUTA** | Minaccia malware non specificata che non è ancora stata definita.
<span id="MP_THREAT_CATEGORY_SPP"></span><span id="mp_threat_category_spp"></span>**Mp \_ CATEGORIA \_ DI \_ MINACCE SPP** | Tecnologia anti-piracy che richiede che ogni installazione di un Windows prodotto sia attivata con Microsoft.
<span id="MP_THREAT_CATEGORY_BEHAVIOR"></span><span id="mp_threat_category_behavior"></span>**Mp \_ COMPORTAMENTO \_ DELLE CATEGORIE DI \_ MINACCE** | Tipo di rilevamento basato su azioni di file spesso associate ad attività dannose.
<span id="MP_THREAT_CATEGORY_VULNERABILTIY"></span><span id="mp_threat_category_vulnerabiltiy"></span>**Mp \_ CATEGORIA \_ \_ DI MINACCIA VULNERABILTIY** | Qualsiasi punto debole, processo amministrativo o attività che rende un dispositivo soggetto a exploit da una minaccia.
<span id="MP_THREAT_CATEGORY_POLICY"></span><span id="mp_threat_category_policy"></span>**Mp \_ CRITERI DI \_ CATEGORIA \_ DI MINACCE** | Set di regole definite da un amministratore che controllano le funzionalità nei dispositivi desktop e mobili, ad esempio gli aggiornamenti software.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato | Windows 8 (solo app desktop) |
| Server minimo supportato | Windows Server 2012 (solo app desktop) |
| Intestazione | MpClient.h |
