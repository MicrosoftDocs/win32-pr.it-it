---
title: Costanti di autenticazione (WSManDisp. h)
description: Specificare il metodo di autenticazione e la modalità di gestione dei server di certificati per il trasporto HTTPS delle richieste.
ms.assetid: adfefbc9-c386-48db-a0c2-145aa4f91bfa
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagCredUsernamePassword
- WSManFlagSkipCACheck
- WSManFlagSkipCNCheck
- WSManFlagUseNoAuthentication
- WSManFlagUseDigest
- WSManFlagUseNegotiate
- WSManFlagUseBasic
- WSManFlagUseKerberos
- WSManFlagNoEncryption
- WSManFlagUseClientCertificate
- WSManFlagUseCredSsp
- WSManFlagSkipRevocationCheck
- WSManFlagAllowNegotiateImplicitCredentials
- WSManFlagUseSsl
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce45d1474cf6c925149c05ae348231333c3356e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518772"
---
# <a name="authentication-constants"></a>Costanti di autenticazione

Le costanti di autenticazione sono costanti nell'enumerazione **\_ \_ WSManSessionFlags** che specificano il metodo di autenticazione e come gestire i server dei certificati per il trasporto HTTPS delle richieste.

Una o più costanti elencate nell'elenco seguente sono obbligatorie nel parametro *Flags* nelle chiamate a [**WSMan. CreateSession**](wsman-createsession.md) o in [**IWSMan:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) chiamate che si connettono a un computer remoto.

<dl> <dt>

<span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**
</dt> <dd> <dl> <dt>

4096 (0x1000)
</dt> <dt>



Usare il nome utente e la password come credenziali. Impostare questo flag quando si crea un oggetto [**ConnectionOptions**](connectionoptions.md) e si forniscono [**nome utente**](connectionoptions-username.md) e [**password**](connectionoptions-password.md). Le credenziali possono essere un account di dominio o un account nel computer locale. Per impostazione predefinita, l'account deve essere un membro del gruppo Administrators locale nel computer locale o remoto. Il servizio gestione remota Windows può tuttavia essere configurato in modo da consentire altri utenti. Per ulteriori informazioni, vedere [installazione e configurazione per gestione remota Windows](installation-and-configuration-for-windows-remote-management.md). È possibile impostare questo flag quando si specificano le credenziali per l'autenticazione Negotiate (nota anche come [*autenticazione integrata di Windows*](windows-remote-management-glossary.md)) o per [*l'autenticazione di base*](windows-remote-management-glossary.md).

Il metodo di scripting associato è [**WSMan. SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md)e il metodo C++ è [**IWSManEx. SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**
</dt> <dd> <dl> <dt>

8192 (0x2000)
</dt> <dt>



Quando si esegue la connessione tramite HTTPS, il client non convalida che il certificato del server sia firmato da un'autorità di certificazione (CA) attendibile. Usare questo valore solo quando il computer remoto è considerato attendibile da altri mezzi, ad esempio se il computer remoto fa parte di una rete fisicamente sicura e isolata oppure il computer remoto è elencato come host attendibile nella configurazione di WinRM.

Il metodo di scripting associato è [**WSMan. SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md)e il metodo C++ è [**IWSManEx. SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**
</dt> <dd> <dl> <dt>

16384 (0x4000)
</dt> <dt>



Quando si esegue la connessione tramite HTTPS, il client non convalida che il nome comune (CN) nel certificato del server corrisponda al nome del computer nella stringa di connessione. Usare solo quando il computer remoto è considerato attendibile da altri mezzi, ad esempio se il computer remoto fa parte di una rete fisicamente sicura e isolata oppure il computer remoto è elencato come host attendibile nella configurazione di WinRM.

Il metodo di scripting associato è [**WSMan. SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md)e il metodo C++ è [**IWSManEx. SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**
</dt> <dd> <dl> <dt>

32768 (0x8000)
</dt> <dt>



Non usare alcuna autenticazione. Specificare questa costante durante il test di una connessione a un computer remoto per determinare se un servizio che implementa il protocollo WS-Management è configurato per l'ascolto delle richieste di dati. Non è possibile combinare **WSManFlagUseNoAuthentication** con altre costanti di [**sessione**](session.md) . Il metodo di scripting associato è [**WSMan. SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md)e il metodo C++ è [**WSManEx. SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Usare l'autenticazione del digest. Solo il computer client può avviare una richiesta di autenticazione del digest. Il client invia una richiesta al server per l'autenticazione e la ricezione di una stringa di token dal server. Il client invia quindi la richiesta di risorse, inclusi il nome utente e un hash crittografico della password combinata con la stringa del token. L'autenticazione del digest è supportata per HTTP e HTTPS. Gli script client WinRM e le applicazioni possono specificare l'autenticazione del digest, ma non il servizio.

Il metodo di scripting associato è [**WSMan. SessionFlagUseDigest**](wsman-sessionflagusedigest.md)e il metodo C++ è [**IWSManEx. SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Usare l'autenticazione Negotiate. Il client invia una richiesta al server per l'autenticazione. Il server determina se utilizzare Kerberos o NTLM. Kerberos è selezionato per autenticare un account di dominio ed è selezionato NTLM per gli account computer locali. Il nome utente deve essere specificato nel formato dominio \\ nomeutente per un utente di dominio o nome utente nomeserver \\ per un utente locale in un computer server.

Il [controllo dell'account utente (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) influiscono sull'accesso al servizio WinRM. Quando si usa l'autenticazione Negotiate in un gruppo di lavoro o in un dominio, solo l'account Administrator predefinito può accedere al servizio. Per consentire a tutti gli account del gruppo Administrators di accedere al servizio, impostare la seguente chiave del registro di sistema su 1: **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \\ LocalAccountTokenFilterPolicy**.

Il metodo di scripting associato è [**WSMan. SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md)e il metodo C++ è [**IWSManEx. SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Usa l'autenticazione di base. Il client presenta le credenziali sotto forma di nome utente e password, trasmesse direttamente nel messaggio di richiesta. È possibile specificare solo le credenziali che identificano un account amministratore locale nel computer remoto.

Il metodo di scripting associato è [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md)e il metodo C++ è [**IWSManEx. SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Utilizzo dell'autenticazione Kerberos. Il client e il server eseguono l'autenticazione reciproca usando i ticket Kerberos.

Il metodo di scripting associato è [**WSMan. SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md)e il metodo C++ è [**IWSManEx. WSMan. SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Usare nessuna crittografia. Il traffico non crittografato non è consentito per impostazione predefinita e deve essere abilitato sia nel client che nel server.

Il metodo di scripting associato è [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md)e il metodo C++ è [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**
</dt> <dd> <dl> <dt>

2097152 (0x200000)
</dt> <dt>



Usare l'autenticazione basata sui certificati client.

Il metodo di scripting associato è [**WSMan. SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md)e il metodo C++ è [**IWSManEx2. SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**
</dt> <dd> <dl> <dt>

16777216 (0x1000000)
</dt> <dt>



Usare l'autenticazione Credential Security Support Provider (CredSSP).

Il metodo di scripting associato è [**WSMan. SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md)e il metodo C++ è [**IWSManEx3. SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**
</dt> <dd> <dl> <dt>

0x2000000
</dt> <dt>



Non controllare la revoca dei certificati durante l'autenticazione.


</dt> </dl> </dd> <dt>

<span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**
</dt> <dd> <dl> <dt>

0x4000000
</dt> <dt>



Consenti le credenziali implicite.


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**
</dt> <dd> <dl> <dt>

0x8000000
</dt> <dt>



USA Secure Socket Layer, Abilita HTTPS.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti di sessione](session-constants.md)
</dt> </dl>

 

 





