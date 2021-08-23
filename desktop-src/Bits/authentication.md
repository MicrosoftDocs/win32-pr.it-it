---
title: Autenticazione (BITS)
description: BITS supporta l'autenticazione di base, l'autenticazione Passport e diversi schemi di autenticazione challenge/response.
ms.assetid: cfd4aec3-79d0-4971-93f8-df797e5c0f75
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 9cb3d50f6689ed28889c68388969c1cb7d06ea912bc5d5ed4384f45a4e740f79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021289"
---
# <a name="authentication-bits"></a>Autenticazione (BITS)

BITS supporta l'autenticazione di base, l'autenticazione Passport e diversi schemi di autenticazione challenge/response. Se il server o il proxy richiede l'autenticazione utente, usare la funzione [**IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) per specificare le credenziali dell'utente. BITS usa [CryptoAPI](/windows/desktop/SecCrypto/cryptography-portal) per proteggere le credenziali.

Per impostare le credenziali per l'autenticazione di base, usare [**la funzione SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) per specificare il nome utente e la password. È consigliabile usare solo l'autenticazione di base https:// siti Web protetti. in caso contrario, il nome utente e la password saranno visibili agli utenti. 

È possibile incorporare il nome utente e la password nell'URL. Questa procedura non è considerata una buona procedura di sicurezza ed è deprecata in RFC 3986 (sezione 3.2.1).

Per [l'autenticazione Passport,](/windows/desktop/WinHttp/passport-authentication-in-winhttp) BITS supporta solo credenziali esplicite, non credenziali implicite legate all'account.

Per l'autenticazione di tipo challenge/response, BITS rappresenta l'utente e usa [Snego](../com/snego.md) per determinare l'autenticazione challenge/response da usare, ad esempio NTLM o il protocollo Kerberos. Per un elenco degli schemi di richiesta/risposta supportati da BITS, vedere [**BG \_ AUTH \_ SCHEME**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme).

I processi BITS possono avere esito negativo se nella directory virtuale nel server è abilitata l'autenticazione anonima e un altro schema di autenticazione e se gli ACL proteggono la directory virtuale o i file di download. Ad esempio, un processo ha esito negativo con "accesso negato" se nella directory virtuale è abilitata l'autenticazione anonima e integrata e il file contiene un ACL che consente solo a Ben di leggere il file. Ciò si verifica perché la directory virtuale consente l'accesso anonimo, quindi IIS non autentica in modo esplicito Ben (le credenziali di Ben non vengono usate per accedere al file e l'accesso viene negato).

## <a name="using-implicit-credentials"></a>Uso di credenziali implicite

Per usare le credenziali implicite (di accesso) dell'utente per l'autenticazione NTLM o Kerberos, chiamare il metodo [**IBackgroundCopyJob2::SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) e impostare i membri **UserName** e **Password** della struttura [**BG \_ BASIC \_ CREDENTIALS**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_basic_credentials) su **NULL.** Se si specificano credenziali implicite per un proxy, BITS userà anche le credenziali implicite per l'autenticazione del server, a meno che non si specificano credenziali esplicite del server.

Per altre informazioni sui servizi, vedere [Account del servizio e BITS.](service-accounts-and-bits.md)

È anche possibile modificare il valore del Registro di sistema **LMCompatibilityLevel** **o UseLMCompat.** Tuttavia, è consigliabile modificare questi valori solo se si dispone di un'applicazione esistente che non può essere modificata per chiamare il [**metodo SetCredentials.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials)

BITS userà credenziali implicite per l'autenticazione se il valore del Registro di sistema **LMCompatibilityLevel** è due o superiore e non è stato chiamato il [**metodo SetCredentials.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) Il percorso completo del valore del Registro di sistema **LMCompatibilityLevel** è **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **LSA** \\ **LmCompatibilityLevel**.

Si noti che la modifica del valore del Registro di sistema **LMCompatibilityLevel** può influire su altre applicazioni e servizi in esecuzione nel computer. Per altre informazioni sull'uso del valore del Registro di sistema **LMCompatibilityLevel,** [vedere KB147706](https://support.microsoft.com/kb/147706).

Se l'impostazione del valore del Registro di sistema **LMCompatibilityLevel** è un problema, è possibile creare il valore del Registro di sistema **UseLMCompat** in **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **BITS**. Il valore del Registro di sistema è un valore DWORD. Nella tabella seguente sono elencati i valori possibili **per UseLMCompat**:

|Valore|Descrizione|
|-|-|
| 0     | BITS invierà credenziali implicite ogni volta che il server richiede le credenziali NTLM o Kerberos.                                                                                           |
| 1     | BITS invierà credenziali implicite solo se il valore del Registro di sistema **LMCompatibilityLevel** del computer client è maggiore o uguale a 2.<br/>     |
| 2     | BITS invierà credenziali implicite solo se l'applicazione ha chiamato il [**metodo SetCredentials.**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials)<br/> |

BITS userà il valore predefinito "2" per il valore del Registro di sistema **UseLMCompat** se il valore del Registro di sistema non esiste.

## <a name="using-certificates-for-clientserver-authentication"></a>Uso di certificati per l'autenticazione client/server

Nelle comunicazioni client/server protette, i client e i server possono usare certificati digitali per l'autenticazione reciproca. BITS supporta automaticamente l'autenticazione server basata su certificati per i trasporti HTTP sicuri. Per fornire a BITS il certificato client necessario per l'autenticazione reciproca, chiamare il metodo [**IBackgroundCopyJobHttpOptions::SetClientCertificateByID**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid) o [**IBackgroundCopyJobHttpOptions::SetClientCertificateByName.**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname)

Quando un sito Web accetta ma non richiede un certificato client SSL e il processo BITS non specifica un certificato client, il processo avrà esito negativo con **ERRORE \_ WINHTTP \_ CLIENT \_ \_ AUTH CERT \_ NEEDED** (0x80072f0c).

## <a name="how-to-handle-authenticated-proxy-scenarios-that-require-user-specific-settings"></a>Come gestire scenari proxy autenticati che richiedono impostazioni specifiche dell'utente

Se si usa BITS in un ambiente che richiede l'autenticazione proxy durante l'esecuzione come account senza credenziali NTLM o Kerberos utilizzabili nel dominio di rete del computer, è necessario eseguire passaggi aggiuntivi per autenticarsi correttamente usando le credenziali di un altro account utente che dispone di credenziali nel dominio. Si tratta di uno scenario tipico quando il codice BITS viene eseguito come servizio di sistema, ad esempio LocalService, NetworkService o LocalSystem, perché tali account non hanno credenziali NTLM o Kerberos utilizzabili.

La logica di rilevamento proxy usata in BITS esegue le operazioni seguenti quando viene impostato un token helper di rete (BG \_ TOKEN \_ NETWORK):

-   Se [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) è stato chiamato con **BG \_ JOB PROXY USAGE \_ \_ \_ PRECONFIG,** leggere le impostazioni proxy IE locali usando la rappresentazione del contesto del token del proprietario del processo [**tramite WinHttpGetIEProxyConfigForCurrentUser.**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) A partire da Windows 10, versione 1809 (10.0; Build 17763), per questo passaggio viene usata l'identità del token helper.
-   Se [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) è stato chiamato con **BG \_ PROXY USAGE \_ \_ AUTODETECT** o se le impostazioni IE del caso **\_ BG JOB PROXY USAGE \_ \_ \_ PRECONFIG** specificano il rilevamento automatico o un URL di configurazione automatica, eseguire il rilevamento del proxy automatico o WPAD (Web Proxy Autodiscovery Protocol), usando la rappresentazione del token helper [**tramite WinHttpGetProxyForUrl.**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurl)

Successivamente, la rappresentazione del token helper viene usata per l'autenticazione del proxy o del server.

A partire da Windows 10, versione 1809 (10.0; Build 17763), lo scenario proxy autenticato con credenziali specifiche dell'utente è semplificato.

1.  Chiamare il metodo [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) del processo BITS con **BG \_ AUTH \_ SCHEME \_ NEGOTIATE,** *UserName* impostato su **NULL,** *Password* impostata su **NULL** e *Target* impostato su **BG \_ AUTH \_ TARGET \_ PROXY.** In questo modo le credenziali implicite dell'account utente vengono usate per l'autenticazione NTLM e Kerberos con il proxy e il server.
2.  Chiamare [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con **BG \_ JOB PROXY \_ \_ USAGE \_ PRECONFIG**.
3.  QueryInterface per [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions).
4.  Rappresentare l'account utente in uso per le credenziali NTLM/Kerberos.
5.  Chiamare [**SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken).
6. Chiamare [**SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) con **BG \_ TOKEN \_ NETWORK**.
7. Ripristinare la rappresentazione.
8. Continuare la configurazione del processo.
9. Chiamare [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) nel processo.

Prima Windows 10, versione 1809 (10.0; Build 17763), l'identità utente corretta (identità del token helper) viene usata per il rilevamento proxy basato sulla rete (WPAD) e per l'autenticazione proxy, ma il rilevamento effettivo delle impostazioni proxy locali (IE) viene sempre eseguito usando il token del proprietario del processo, anche quando è configurato un token helper. Per risolvere questo problema, è possibile seguire questa procedura.

1.  Rappresentare l'account utente in uso per le credenziali NTLM/Kerberos.
2.  Recuperare le impostazioni proxy IE dell'account utente chiamando [**WinHttpGetIEProxyConfigForCurrentUser.**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
3.  Ripristinare la rappresentazione.
4.  Chiamare il metodo [**SetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) del processo BITS con **BG \_ AUTH \_ SCHEME \_ NEGOTIATE,** *UserName* impostato su **NULL,** *Password* impostata su **NULL** e *Target* impostato su **BG \_ AUTH \_ TARGET \_ PROXY.** In questo modo le credenziali implicite dell'account utente vengono usate per l'autenticazione NTLM e Kerberos con il proxy e il server.
5.  Se il passaggio 2 ha restituito impostazioni proxy specifiche dell'utente (ad esempio *lpszProxy* o *lpszProxyBypass* non sono **NULL),** impostare manualmente le impostazioni del processo corrispondenti usando [**SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con l'impostazione **BG \_ JOB PROXY \_ USAGE \_ \_ OVERRIDE.**
6.  Se il passaggio 2 non ha prodotto impostazioni proxy specifiche dell'utente, chiamare [**SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con **BG \_ JOB USAGE \_ \_ PRECONFIG**.
7.  QueryInterface per [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions).
8.  Rappresentare nuovamente l'account utente.
9.  Chiamare [**SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken).
10. Chiamare [**SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) con **BG \_ TOKEN \_ NETWORK**.
11. Ripristinare la rappresentazione.
12. Continuare la configurazione del processo.
13. Chiamare [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) nel processo.
