---
title: Attributi di sicurezza utente
description: Oltre alle proprietà di denominazione per gli oggetti utente, ad esempio objectGUID, objectSid, CN, Distinguishname e così via, sono disponibili altre proprietà di sicurezza per l'accesso, l'accesso alla rete e il controllo di accesso.
ms.assetid: eeb16938-4380-4622-804f-6b2ff19aa68d
ms.tgt_platform: multiple
keywords:
- Attributi di sicurezza, con AD
- Active Directory attributi di sicurezza utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51000aefdf9ec0f26406607bd781ac4d87b6106
ms.sourcegitcommit: 25bf66769c2087b1a87d6db5930b604cb57e0f98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/23/2020
ms.locfileid: "103963538"
---
# <a name="user-security-attributes"></a>Attributi di sicurezza utente

Oltre alle proprietà di denominazione per gli oggetti utente, ad esempio [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSID**](/windows/desktop/ADSchema/a-objectsid), [**CN**](/windows/desktop/ADSchema/a-cn), [**Distinguishname**](/windows/desktop/ADSchema/a-distinguishedname)e così via, sono disponibili altre proprietà di sicurezza per l'accesso, l'accesso alla rete e il controllo di accesso. Queste proprietà vengono usate dal sistema di sicurezza di Windows 2000. Queste proprietà possono essere visualizzate e gestite dallo snap-in Active Directory utente e computer.

<dl> <dt>

<span id="accountExpires"></span><span id="accountexpires"></span><span id="ACCOUNTEXPIRES"></span>[**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)
</dt> <dd>

L'attributo [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) specifica la scadenza di un account. Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601 (UTC). Il valore **TIMEQ \_ Forever** (definito in Lmaccess. h) indica che un account non scade mai.

</dd> <dt>

<span id="altSecurityIdentities"></span><span id="altsecurityidentities"></span><span id="ALTSECURITYIDENTITIES"></span>[**altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities)
</dt> <dd>

L'attributo [**altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities) è un attributo multivalore che contiene i mapping per i certificati X. 509 o gli account utente Kerberos esterni a questo utente ai fini dell'autenticazione. Diversi pacchetti di sicurezza, tra cui il pacchetto di autenticazione a chiave pubblica e Kerberos, utilizzano questi dati per autenticare gli utenti quando presentano la forma alternativa di identificazione, ad esempio certificato, ticket Kerberos UNIX e così via. Compilare un token Windows 2000 in base all'account utente corrispondente in modo che possano accedere alle risorse di sistema.

Per i certificati X. 509, i valori devono essere i nomi dell'emittente e del soggetto nei certificati 509v3, emessi da un'autorità di certificazione pubblica esterna, che eseguono il mapping all'account utente usato per trovare un account per l'autenticazione. Il pacchetto SSL (Schannel) usa la sintassi seguente: X509: <somecertinfotype> somecertinfo. Il valore seguente, ad esempio, specifica il DN dell'autorità emittente " \<I\> " con DN "c = US, O = InternetCA, CN = APublicCertificateAuthority" e il DN oggetto " \<S\> " con il DN "c = US, O = Fabrikam, OU = Sales, CN = Jeff Smith".


```C++
X509:<I>C=US,O=InternetCA,CN=APublicCertificateAuthority<S>C=US,O=Fabrikam,OU=Sales,CN=Jeff Smith
```



Tenere presente che \<S\> sono supportati "" o " \<I> " e " \<S\> ". La presenza di " \<I\> " non è supportata. Le applicazioni non devono modificare i valori in " \<I\> " o " \<S\> " perché la corrispondenza parziale del DN non è supportata.

Per gli account Kerberos esterni, i valori devono corrispondere al nome dell'account Kerberos. Il pacchetto Kerberos usa la sintassi seguente: "Kerberos: MITaccountname". Ad esempio, di seguito è riportato il valore per un account in Fabrikam.com:


```C++
Kerberos:Jeff.Smith@Fabrikam.com
```



</dd> <dt>

<span id="badPasswordTime"></span><span id="badpasswordtime"></span><span id="BADPASSWORDTIME"></span>[**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)
</dt> <dd>

Non replicato. L'attributo [**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime) specifica l'ultima volta che l'utente ha tentato di accedere all'account con una password non corretta. Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601 (UTC). Questo attributo viene mantenuto separatamente in ogni controller di dominio nel dominio. Un valore pari a zero indica che l'ora dell'ultima password non valida è sconosciuta. Per ottenere un valore accurato per l'ora dell'ultima password errata dell'utente nel dominio, è necessario eseguire una query su ogni controller di dominio nel dominio e usare il valore più grande.

</dd> <dt>

<span id="badPwdCount"></span><span id="badpwdcount"></span><span id="BADPWDCOUNT"></span>[**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)
</dt> <dd>

Non replicato. L'attributo [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount) specifica il numero di volte in cui l'utente ha tentato di accedere all'account con una password non corretta. Questo attributo viene mantenuto separatamente in ogni controller di dominio nel dominio. Il valore 0 indica che il valore è sconosciuto. Per ottenere un valore preciso per i tentativi di password non validi totali dell'utente nel dominio, è necessario eseguire una query su ogni controller di dominio nel dominio e utilizzare la somma dei valori.

</dd> <dt>

<span id="codePage"></span><span id="codepage"></span><span id="CODEPAGE"></span>[**codePage**](/windows/desktop/ADSchema/a-codepage)
</dt> <dd>

L'attributo [**codepage**](/windows/desktop/ADSchema/a-codepage) specifica la tabella codici per la lingua scelta dall'utente. Questo valore non viene utilizzato da Windows 2000.

</dd> <dt>

<span id="countryCode"></span><span id="countrycode"></span><span id="COUNTRYCODE"></span>[**countryCode**](/windows/desktop/ADSchema/a-countrycode)
</dt> <dd>

L'attributo [**CountryCode**](/windows/desktop/ADSchema/a-countrycode) specifica il codice paese/area geografica per la lingua dell'utente. Questo valore non viene utilizzato da Windows 2000.

</dd> <dt>

<span id="homeDirectory"></span><span id="homedirectory"></span><span id="HOMEDIRECTORY"></span>[**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)
</dt> <dd>

L'attributo [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) specifica il percorso della Home Directory per l'utente. La stringa può essere null.

Se [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) è impostato e specifica una lettera di unità, [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) deve essere un percorso UNC. Il percorso deve essere un percorso UNC di rete della directory di condivisione del server di form \\ \\ \\ \\ . Questo valore può essere una stringa null.

Se [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) non è impostato, [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) deve essere un percorso locale, ad esempio C: \\ mylocaldir.

</dd> <dt>

<span id="homeDrive"></span><span id="homedrive"></span><span id="HOMEDRIVE"></span>[**homeDrive**](/windows/desktop/ADSchema/a-homedrive)
</dt> <dd>

L'attributo [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) specifica la lettera di unità a cui eseguire il mapping del percorso UNC specificato da **HomeDirectory**. La lettera di unità deve essere specificata nel formato seguente:


```C++
<drive letter>:
```



dove " \<drive letter\> " è la lettera dell'unità da mappare. Ad esempio:


```C++
Z:
```



Se questo attributo non è impostato, [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) deve essere un percorso locale, ad esempio C: \\ mylocaldir.

</dd> <dt>

<span id="lastLogoff"></span><span id="lastlogoff"></span><span id="LASTLOGOFF"></span>[**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)
</dt> <dd>

Non replicato. L'attributo [**LastLogoff**](/windows/desktop/ADSchema/a-lastlogoff) specifica quando si è verificata l'ultima disconnessione. Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601 (UTC). La parte alta di questo Integer di grandi dimensioni corrisponde al membro **dwHighDateTime** della struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e la parte bassa corrisponde al membro **dwLowDateTime** della struttura **FILETIME** . Questo attributo viene mantenuto separatamente in ogni controller di dominio nel dominio. Un valore pari a zero indica che l'ora dell'ultimo disconnessione è sconosciuta. Per ottenere un valore accurato per l'ultima disconnessione dell'utente nel dominio, è necessario eseguire una query su ogni controller di dominio nel dominio e usare il valore più grande.

</dd> <dt>

<span id="lastLogon"></span><span id="lastlogon"></span><span id="LASTLOGON"></span>[**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)
</dt> <dd>

Non replicato. L'attributo [**LastLogon**](/windows/desktop/ADSchema/a-lastlogon) specifica quando si è verificato l'ultimo accesso. Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601 (UTC). La parte alta di questo Integer di grandi dimensioni corrisponde al membro **dwHighDateTime** della struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e la parte bassa corrisponde al membro **dwLowDateTime** della struttura **FILETIME** . Questo attributo viene mantenuto separatamente in ogni controller di dominio nel dominio. Un valore pari a zero indica che l'ora dell'ultimo accesso è sconosciuta. Per ottenere un valore accurato per l'ultimo accesso dell'utente nel dominio, è necessario eseguire una query su ogni controller di dominio nel dominio e usare il valore più grande.

</dd> <dt>

<span id="lmPwdHistory"></span><span id="lmpwdhistory"></span><span id="LMPWDHISTORY"></span>[**lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory)
</dt> <dd>

L'attributo [**lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory) è la cronologia delle password dell'utente nel formato unidirezionale di LAN Manager (lm) (OWF). La OWF LM viene utilizzata per la compatibilità con i client LAN Manager 2. x, Windows 95 e Windows 98. Questo attributo viene utilizzato solo dal sistema operativo. Tenere presente che non è possibile derivare la password in testo non crittografato dal formato OWF della password.

</dd> <dt>

<span id="logonCount"></span><span id="logoncount"></span><span id="LOGONCOUNT"></span>[**logonCount**](/windows/desktop/ADSchema/a-logoncount)
</dt> <dd>

Non replicato. L'attributo [**LogonCount**](/windows/desktop/ADSchema/a-logoncount) conta il numero di volte che l'utente ha tentato di accedere a questo account. Questo attributo viene mantenuto in ogni controller di dominio nel dominio. Il valore 0 indica che il valore è sconosciuto. Per ottenere un valore preciso per il numero totale di tentativi di accesso riusciti nel dominio, è necessario eseguire una query su ogni controller di dominio nel dominio e utilizzare la somma dei valori.

</dd> <dt>

<span id="mail"></span><span id="MAIL"></span>[**posta elettronica**](/windows/desktop/ADSchema/a-mail)
</dt> <dd>

L'attributo [**mail**](/windows/desktop/ADSchema/a-mail) è un attributo a valore singolo che contiene l'indirizzo SMTP dell'utente, ad esempio " jeff@Fabrikam.com ".

</dd> <dt>

<span id="maxStorage"></span><span id="maxstorage"></span><span id="MAXSTORAGE"></span>[**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)
</dt> <dd>

L'attributo [**maxStorage**](/windows/desktop/ADSchema/a-maxstorage) specifica la quantità massima di spazio su disco rigido che l'utente può utilizzare. Usare il valore **User \_ MAXSTORAGE \_ Unlimited** (definito in Lmaccess. h) per usare tutto lo spazio disponibile su disco.

</dd> <dt>

<span id="memberOf"></span><span id="memberof"></span><span id="MEMBEROF"></span>[**memberOf**](/windows/desktop/ADSchema/a-memberof)
</dt> <dd>

L'attributo [**membro**](/windows/desktop/ADSchema/a-memberof) è un attributo multivalore che contiene i gruppi di cui l'utente è membro diretto, ad eccezione del gruppo primario, rappresentato da [**primaryGroupID**](/windows/desktop/ADSchema/a-primarygroupid). L'appartenenza al gruppo dipende dal controller di dominio da cui viene recuperato questo attributo:

-   In un controller di dominio per il dominio che contiene l'utente, il [**membro**](/windows/desktop/ADSchema/a-memberof) per l'utente è completo per quanto riguarda l'appartenenza ai gruppi in tale dominio; Tuttavia, il **membro** non contiene l'appartenenza dell'utente ai gruppi globali e locali di dominio in altri domini.
-   In un server GC, il [**membro**](/windows/desktop/ADSchema/a-memberof) per l'utente è completo rispetto a tutte le appartenenze a gruppi universali.

Se entrambe le condizioni sono vere per il controller di dominio, entrambi i set di dati sono contenuti in [**member**](/windows/desktop/ADSchema/a-memberof).

Tenere presente che questo attributo elenca i gruppi che contengono l'utente nei rispettivi attributi membro, ma non contiene l'elenco ricorsivo di predecessori annidati. Se, ad esempio, l'utente O è un membro del gruppo C e del gruppo B e il gruppo B è annidato nel gruppo A, l'attributo [**membro**](/windows/desktop/ADSchema/a-memberof) dell'utente o elenca il gruppo c e il gruppo b, ma non il gruppo a.

Questo attributo non è archiviato: si tratta di un attributo di collegamento a ritroso calcolato.

</dd> <dt>

<span id="ntPwdHistory"></span><span id="ntpwdhistory"></span><span id="NTPWDHISTORY"></span>[**ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory)
</dt> <dd>

L'attributo [**ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory) è la cronologia delle password dell'utente in formato unidirezionale Windows NT (OWF). Windows 2000 usa Windows NT OWF. Questo attributo viene utilizzato solo dal sistema operativo. Tenere presente che non è possibile riportare la password in testo non crittografato dal formato OWF della password.

</dd> <dt>

<span id="otherMailbox"></span><span id="othermailbox"></span><span id="OTHERMAILBOX"></span>[**otherMailbox**](/windows/desktop/ADSchema/a-othermailbox)
</dt> <dd>

L'attributo [**otherMailbox**](/windows/desktop/ADSchema/a-othermailbox) è un attributo multivalore che contiene altri indirizzi di posta elettronica aggiuntivi in un modulo, ad esempio, "CCMAIL: SergioMelchiori".

</dd> <dt>

<span id="PasswordExpirationDate"></span><span id="passwordexpirationdate"></span><span id="PASSWORDEXPIRATIONDATE"></span>[**PasswordExpirationDate**](/windows/desktop/ADSI/iadsuser-property-methods)
</dt> <dd>

La data di scadenza della password non è un attributo dell'oggetto utente. Si tratta di un valore calcolato in base alla somma di [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) per l'utente e il [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) del dominio dell'utente. Per ottenere la data di scadenza della password, ottenere la proprietà [**IADsUser. PasswordExpirationDate**](/windows/desktop/ADSI/iadsuser-property-methods) . Non è possibile modificare questo attributo per un utente; in alternativa, impostare la proprietà [**IADsDomain. MaxPasswordAge**](/windows/desktop/ADSI/iadsdomain-property-methods) per modificare l'impostazione per il dominio.

</dd> <dt>

<span id="primaryGroupID"></span><span id="primarygroupid"></span><span id="PRIMARYGROUPID"></span>[**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid)
</dt> <dd>

L'attributo [**primaryGroupID**](/windows/desktop/ADSchema/a-primarygroupid) è un attributo a valore singolo che contiene il [**PrimaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) del gruppo che rappresenta il gruppo primario dell'oggetto. Il gruppo primario dell'oggetto non è incluso nell'attributo [**membro**](/windows/desktop/ADSchema/a-memberof) . Per impostazione predefinita, ad esempio, il gruppo primario di un oggetto utente è il **PrimaryGroupToken** del gruppo Domain Users, ma il gruppo Domain Users non fa parte dell'attributo **member** dell'oggetto utente.

</dd> <dt>

<span id="profilePath"></span><span id="profilepath"></span><span id="PROFILEPATH"></span>[**PercorsoProfilo**](/windows/desktop/ADSchema/a-profilepath)
</dt> <dd>

L'attributo [**filePath**](/windows/desktop/ADSchema/a-profilepath) specifica un percorso per il profilo dell'utente. Questo valore può essere una stringa null, un percorso assoluto locale o un percorso UNC.

</dd> <dt>

<span id="pwdLastSet"></span><span id="pwdlastset"></span><span id="PWDLASTSET"></span>[**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)
</dt> <dd>

L'attributo [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) specifica la data dell'Ultima modifica della password. Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100-nanosecondi a partire dal 1 ° gennaio 1601 (UTC).

Il sistema usa il valore di questo attributo e l'attributo [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) del dominio che contiene l'oggetto utente per calcolare la data di scadenza della password. Ovvero la somma di [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) per l'utente e il **maxPwdAge** del dominio dell'utente.

Questo attributo controlla se l'utente deve modificare la password quando l'utente accede successivamente. Se [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) è zero, l'impostazione predefinita è che l'utente deve modificare la password all'accesso successivo. Il valore-1 indica che l'utente non deve modificare la password all'accesso successivo. Il sistema imposta questo valore su-1 dopo che l'utente ha impostato la password.

</dd> <dt>

<span id="sAMAccountType"></span><span id="samaccounttype"></span><span id="SAMACCOUNTTYPE"></span>[**sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype)
</dt> <dd>

L'attributo [**sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype) specifica un numero intero che rappresenta il tipo di conto. Questa impostazione viene impostata dal sistema operativo quando viene creato l'oggetto.

</dd> <dt>

<span id="scriptPath"></span><span id="scriptpath"></span><span id="SCRIPTPATH"></span>[**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)
</dt> <dd>

L'attributo [**ScriptPath**](/windows/desktop/ADSchema/a-scriptpath) specifica il percorso dello script di accesso dell'utente, con estensione cmd, exe o bat. La stringa può essere null.

</dd> <dt>

<span id="unicodePwd"></span><span id="unicodepwd"></span><span id="UNICODEPWD"></span>[**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd)
</dt> <dd>

L'attributo [**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd) è la password dell'utente.

Per impostare la password utente, utilizzare il metodo [**IADsUser. ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) , se lo script o l'applicazione consente all'utente di modificare la propria password o il metodo [**IADsUser. sepassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) , se lo script o l'applicazione consente a un amministratore di reimpostare una password.

Password dell'utente in formato unidirezionale Windows NT (OWF). Windows 2000 usa Windows NT OWF. Questo attributo viene utilizzato solo dal sistema operativo. Tenere presente che non è possibile riportare la password in testo non crittografato dal formato OWF della password.

</dd> <dt>

<span id="userAccountControl"></span><span id="useraccountcontrol"></span><span id="USERACCOUNTCONTROL"></span>[**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)
</dt> <dd>

L'attributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) specifica i flag che controllano la password, il blocco, la disabilitazione, l'abilitazione, lo script e il comportamento della Home Directory per l'utente. Questo attributo contiene anche un flag che indica il tipo di account dell'oggetto. L'oggetto utente ha in genere il \_ set di account UF Normal \_ .

I flag seguenti sono definiti in Lmaccess. h.



| Flag                     | Descrizione                                                                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_script UF               | Script di accesso eseguito. Questo valore deve essere impostato per LAN Manager 2,0 o Windows NT.                                                                             |
| \_ACCOUNTDISABLE UF       | L'account utente è disabilitato.                                                                                                                                    |
| \_homedir UF \_ obbligatorio    | La home directory è obbligatoria. Questo valore viene ignorato in Windows NT e Windows 2000.                                                                            |
| UF \_ passwd \_ NOTREQD      | Non è necessaria alcuna password.                                                                                                                                         |
| \_modifica del \_ cant della passwd di UF \_ | L'utente non può modificare la password.                                                                                                                             |
| \_blocco UF              | L'account è attualmente bloccato. Questo valore può essere cancellato per sbloccare un account bloccato in precedenza. Questo valore non può essere utilizzato per bloccare un account bloccato in precedenza. |
| \_password UF dont \_ expire \_ | Rappresenta la password, che non deve mai scadere nell'account.                                                                                               |



 

I flag seguenti descrivono il tipo di account. È possibile impostare solo un valore. Non è possibile modificare il tipo di account.



| Flag                            | Descrizione                                                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_account UF Normal \_             | Si tratta di un tipo di account predefinito che rappresenta un utente tipico.                                                                                                                                                                                  |
| \_account con \_ duplicazione temporanea UF \_    | Si tratta di un account per gli utenti il cui account primario si trova in un altro dominio. Questo account fornisce l'accesso utente al dominio, ma non a un dominio che considera attendibile il dominio. Il gestore utenti fa riferimento a questo tipo di account come account utente locale. |
| \_ \_ account attendibilità UF workstation \_ | Si tratta di un account computer per un server Windows NT Workstation/Windows 2000 Professional o Windows NT Server/Windows 2000 che è membro di questo dominio.                                                                                     |
| \_ \_ account trust server \_ UF      | Si tratta di un account computer di un controller di dominio di backup di Windows NT che è membro di questo dominio.                                                                                                                                           |
| \_ \_ account trust tra domini \_ UF | Questo è un permesso per considerare attendibile un dominio di Windows NT che considera attendibili altri domini.                                                                                                                                                            |



 

</dd> <dt>

<span id="userCertificate"></span><span id="usercertificate"></span><span id="USERCERTIFICATE"></span>[**userCertificate**](/windows/desktop/ADSchema/a-usercertificate)
</dt> <dd>

L'attributo [**userCertificate**](/windows/desktop/ADSchema/a-usercertificate) è un attributo multivalore che contiene i certificati X509v3 con codifica der rilasciati all'utente. Tenere presente che questo attributo contiene i certificati di chiave pubblica rilasciati all'utente dal servizio certificati Microsoft.

</dd> <dt>

<span id="userSharedFolder"></span><span id="usersharedfolder"></span><span id="USERSHAREDFOLDER"></span>[**userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder)
</dt> <dd>

L'attributo [**userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder) specifica un percorso UNC della cartella documenti condivisi dell'utente. Il percorso deve essere un percorso UNC di rete della directory di condivisione del server di form \\ \\ \\ \\ . Questo valore può essere una stringa null.

</dd> <dt>

<span id="userWorkstations"></span><span id="userworkstations"></span><span id="USERWORKSTATIONS"></span>[**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)
</dt> <dd>

L'attributo [**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations) è un attributo a valore singolo che contiene i nomi NetBIOS delle workstation da cui l'utente può accedere. Ogni nome NetBIOS è separato da una virgola.

Se non è impostato alcun valore, indica che non è presente alcuna restrizione. Per disabilitare gli accessi da tutte le workstation a questo account, impostare il \_ valore UF ACCOUNTDISABLE (definito in Lmaccess. h) nell'attributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) .

</dd> </dl>

 

 
