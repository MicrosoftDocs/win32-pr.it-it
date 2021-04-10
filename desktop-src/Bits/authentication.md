---
title: Autenticazione (BITS)
description: BITS supporta l'autenticazione di base, l'autenticazione Passport e diversi schemi di autenticazione di richiesta/risposta.
ms.assetid: cfd4aec3-79d0-4971-93f8-df797e5c0f75
ms.topic: article
ms.date: 10/09/2018
ms.openlocfilehash: 5d970956676a3348dd4b8c4b420e044bd4714775
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103963660"
---
# <a name="authentication-bits"></a>Autenticazione (BITS)

BITS supporta l'autenticazione di base, l'autenticazione Passport e diversi schemi di autenticazione di richiesta/risposta. Se il server o il proxy richiede l'autenticazione utente, usare la funzione [**IBackgroundCopyJob2:: Secredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) per specificare le credenziali dell'utente. BITS USA [CryptoAPI](/windows/desktop/SecCrypto/cryptography-portal) per proteggere le credenziali.

Per impostare le credenziali per l'autenticazione di base, utilizzare la funzione [**Secredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) per specificare il nome utente e la password. È consigliabile usare l'autenticazione di base solo con i siti Web protetti con https://. in caso contrario, il nome utente e la password saranno visibili agli utenti. 

È possibile incorporare il nome utente e la password nell'URL. Questa operazione non è considerata una procedura di sicurezza efficace ed è deprecata in RFC 3986 (sezione 3.2.1).

Per l'autenticazione [Passport](/windows/desktop/WinHttp/passport-authentication-in-winhttp) , BITS supporta solo le credenziali esplicite e non le credenziali implicite associate all'account.

Per l'autenticazione di tipo richiesta/risposta, BITS rappresenta l'utente e utilizza [Snego](../com/snego.md) per determinare l'autenticazione di tipo richiesta/risposta da utilizzare, ad esempio NTLM o il protocollo Kerberos. Per un elenco di schemi di verifica/risposta supportati da BITS, [**vedere \_ \_ schema di autenticazione BG**](/windows/desktop/api/Bits1_5/ne-bits1_5-bg_auth_scheme).

I processi BITS possono avere esito negativo se la directory virtuale nel server dispone di autenticazione anonima e di un altro schema di autenticazione abilitato e se gli ACL proteggono la directory virtuale o scaricano i file. Ad esempio, un processo ha esito negativo con "accesso negato" se per la directory virtuale è abilitata l'autenticazione anonima e integrata e il file contiene un ACL che consente solo a ben di leggere il file. Questo problema si verifica perché la directory virtuale consente l'accesso anonimo, quindi IIS non autentica in modo esplicito il ben (le credenziali di ben non vengono usate per accedere al file e l'accesso viene negato).

## <a name="using-implicit-credentials"></a>Uso di credenziali implicite

Per usare le credenziali implicite (di accesso) dell'utente per l'autenticazione NTLM o Kerberos, chiamare il metodo [**IBackgroundCopyJob2:: Secredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) e impostare i membri **username** e **password** della struttura di [**credenziali di \_ base \_ di BG**](/windows/desktop/api/Bits1_5/ns-bits1_5-bg_basic_credentials) su **null**. Se si specificano credenziali implicite per un proxy, BITS utilizzerà anche le credenziali implicite per l'autenticazione server, a meno che non si specifichino le credenziali esplicite del server.

Per ulteriori informazioni sui servizi, vedere [account del servizio e BITS](service-accounts-and-bits.md).

È anche possibile modificare il valore del registro di sistema **LMCompatibilityLevel** o **UseLMCompat** . Tuttavia, è necessario modificare questi valori solo se si dispone di un'applicazione esistente che non può essere modificata in modo da chiamare il metodo [**Secredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) .

BITS utilizzerà le credenziali implicite per l'autenticazione se il valore del registro di sistema **LMCompatibilityLevel** è due o superiore e non è stato chiamato il metodo [**imcredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) . Il percorso completo del valore del registro di sistema **LMCompatibilityLevel** è **HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **LSA** \\ **LMCompatibilityLevel**.

Si noti che la modifica del valore del registro di sistema **LMCompatibilityLevel** può influire su altre applicazioni e servizi in esecuzione nel computer. Per ulteriori informazioni sull'utilizzo del valore del registro di sistema **LMCompatibilityLevel** , vedere [KB147706](https://support.microsoft.com/kb/147706).

Se l'impostazione del valore del registro di sistema **LMCompatibilityLevel** è un problema, è possibile creare il valore del registro di sistema **UseLMCompat** in **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **bits**. Il valore del registro di sistema è un valore DWORD. La tabella seguente elenca i valori possibili per **UseLMCompat**:

|Valore|Descrizione|
|-|-|
| 0     | BITS invierà le credenziali implicite ogni volta che il server richiede le credenziali NTLM o Kerberos.                                                                                           |
| 1     | BITS invierà le credenziali implicite solo se il valore del registro di sistema **LMCompatibilityLevel** del computer client è maggiore o uguale a 2.<br/>     |
| 2     | BITS invierà le credenziali implicite solo se l'applicazione ha chiamato il metodo [**Secredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) .<br/> |

BITS utilizzerà il valore predefinito "2" per il valore del registro di sistema **UseLMCompat** se il valore del registro di sistema non esiste.

## <a name="using-certificates-for-clientserver-authentication"></a>Uso dei certificati per l'autenticazione client/server

Nella comunicazione protetta tra client e server, i client e i server possono usare i certificati digitali per l'autenticazione reciproca. BITS supporta automaticamente l'autenticazione server basata sui certificati per i trasporti HTTP protetti. Per fornire BITS il certificato client necessario per l'autenticazione reciproca, chiamare il metodo [**IBackgroundCopyJobHttpOptions:: SetClientCertificateByID**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyid) o [**IBackgroundCopyJobHttpOptions:: SetClientCertificateByName**](/windows/desktop/api/Bits2_5/nf-bits2_5-ibackgroundcopyjobhttpoptions-setclientcertificatebyname) .

Quando un sito Web accetta ma non richiede un certificato client SSL e il processo BITS non specifica un certificato client, il processo avrà esito negativo e verrà eseguito l'errore con il certificato di **\_ \_ autenticazione client WinHTTP \_ \_ \_ necessario** (0x80072F0C).

## <a name="how-to-handle-authenticated-proxy-scenarios-that-require-user-specific-settings"></a>Come gestire scenari proxy autenticati che richiedono impostazioni specifiche dell'utente

Se si utilizzano BITS in un ambiente che richiede l'autenticazione proxy mentre è in esecuzione come account senza credenziali NTLM o Kerberos utilizzabili nel dominio di rete del computer, è necessario eseguire passaggi aggiuntivi per l'autenticazione corretta utilizzando le credenziali di un altro account utente che dispone di credenziali nel dominio. Si tratta di uno scenario tipico quando il codice BITS è in esecuzione come servizio di sistema, ad esempio LocalService, NetworkService o LocalSystem, in quanto questi account non dispongono di credenziali NTLM o Kerberos utilizzabili.

La logica di rilevamento del proxy utilizzata in BITS esegue le operazioni seguenti quando si imposta un token helper di rete ( \_ rete token BG \_ ):

-   Se [**Metodo ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) è stato chiamato con la **\_ \_ \_ \_ preconfigurazione di utilizzo del proxy del processo BG**, leggere le impostazioni del proxy di IE locale usando la rappresentazione del contesto del token del proprietario del processo tramite [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser). A partire da Windows 10, versione 1809 (10,0; Compilazione 17763), per questo passaggio viene usata l'identità del token di supporto.
-   Se [**Metodo ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) è stato chiamato con il rilevamento automatico dell' **\_ utilizzo del proxy \_ \_ BG** o se le impostazioni di IE del caso di **utilizzo del \_ proxy del processo \_ \_ \_ BG** specificano il rilevamento automatico o un URL di configurazione automatica, eseguono il rilevamento automatico del proxy o il protocollo WPAD (Web Proxy AutoDiscovery Protocol), usando la rappresentazione del token helper tramite [**WinHttpGetProxyForUrl**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetproxyforurl).

In seguito, la rappresentazione del token di supporto viene utilizzata per l'autenticazione del proxy o del server.

A partire da Windows 10, versione 1809 (10,0; Compilazione 17763), lo scenario proxy autenticato con credenziali specifiche dell'utente è semplificato.

1.  Chiamare il metodo [**GetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) del processo BITS con lo **\_ schema di autenticazione BG \_ \_ Negotiate**, *username* impostato su **null**, *password* impostata su **null** e *target* impostato su **BG \_ auth \_ target \_ proxy**. In questo modo, le credenziali implicite dell'account utente vengono utilizzate per l'autenticazione NTLM e Kerberos con il proxy e il server.
2.  Chiamare [**Metodo ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con **la \_ \_ \_ \_ preconfigurazione di utilizzo del proxy del processo BG**.
3.  QueryInterface per [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions).
4.  Rappresentare l'account utente in uso per le credenziali NTLM/Kerberos.
5.  Chiamare [**SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken).
6. Chiamare [**SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) con **la \_ \_ rete di token BG**.
7. Ripristinare la rappresentazione.
8. Continua l'installazione del processo.
9. Chiamare [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) per il processo.

Prima di Windows 10, versione 1809 (10,0; Build 17763), l'identità utente corretta (l'identità del token di supporto) viene usata per il rilevamento del proxy basato sulla rete (WPAD) e per l'autenticazione proxy, ma il rilevamento effettivo delle impostazioni proxy locali (IE) viene sempre eseguito usando il token del proprietario del processo, anche quando viene configurato un token helper. Per ovviare a questa lacuna, è possibile seguire questa procedura.

1.  Rappresentare l'account utente in uso per le credenziali NTLM/Kerberos.
2.  Recuperare le impostazioni del proxy IE dell'account utente chiamando [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).
3.  Ripristinare la rappresentazione.
4.  Chiamare il metodo [**GetCredentials**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials) del processo BITS con lo **\_ schema di autenticazione BG \_ \_ Negotiate**, *username* impostato su **null**, *password* impostata su **null** e *target* impostato su **BG \_ auth \_ target \_ proxy**. In questo modo, le credenziali implicite dell'account utente vengono utilizzate per l'autenticazione NTLM e Kerberos con il proxy e il server.
5.  Se il passaggio 2 ha restituito le impostazioni proxy specifiche dell'utente (ad esempio, *lpszProxy* o *LpszProxyBypass* non sono **null**), impostare manualmente le impostazioni del processo corrispondenti, usando [**SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con l'impostazione di sostituzione dell'utilizzo del **proxy del \_ processo \_ \_ \_ BG** .
6.  Se il passaggio 2 non produce impostazioni proxy specifiche per l'utente, chiamare [**SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) con **la \_ \_ \_ preconfigurazione di utilizzo del processo BG**.
7.  QueryInterface per [**IBitsTokenOptions**](/windows/desktop/api/Bits4_0/nn-bits4_0-ibitstokenoptions).
8.  Rappresenta nuovamente l'account utente.
9.  Chiamare [**SetHelperToken**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertoken).
10. Chiamare [**SetHelperTokenFlags**](/windows/desktop/api/Bits4_0/nf-bits4_0-ibitstokenoptions-sethelpertokenflags) con **la \_ \_ rete di token BG**.
11. Ripristinare la rappresentazione.
12. Continua l'installazione del processo.
13. Chiamare [**Resume**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume) per il processo.
