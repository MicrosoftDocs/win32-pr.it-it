---
title: Attributi di sicurezza utente
description: Oltre a denominare le proprietà per gli oggetti utente, ad esempio objectGUID, objectSid, cn, distinguishedName e così via, sono disponibili altre proprietà di sicurezza usate per l'accesso, l'accesso alla rete e il controllo di accesso.
ms.assetid: eeb16938-4380-4622-804f-6b2ff19aa68d
ms.tgt_platform: multiple
keywords:
- Attributi di sicurezza, uso di AD
- Attributi di sicurezza utente AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dfe23252002f2ffbbba3f8e8a8faf5a2d36ce348bdbd7503c0d99a816a81902
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024889"
---
# <a name="user-security-attributes"></a>Attributi di sicurezza utente

Oltre a denominare le proprietà per gli oggetti utente, ad esempio [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSid**](/windows/desktop/ADSchema/a-objectsid), [**cn**](/windows/desktop/ADSchema/a-cn), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname)e così via, sono disponibili altre proprietà di sicurezza usate per l'accesso, l'accesso alla rete e il controllo di accesso. Queste proprietà vengono usate dal sistema di Windows 2000. Queste proprietà possono essere visualizzate e gestite dallo snap-in Utenti e computer di Active Directory.

<dl> <dt>

<span id="accountExpires"></span><span id="accountexpires"></span><span id="ACCOUNTEXPIRES"></span>[**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)
</dt> <dd>

[**L'attributo accountExpires**](/windows/desktop/ADSchema/a-accountexpires) specifica la scadenza di un account. Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100 nanosecondi dal 1° gennaio 1601 (UTC). Il valore **TIMEQ \_ FOREVER** (definito in Lmaccess.h) indica che un account non scade mai.

</dd> <dt>

<span id="altSecurityIdentities"></span><span id="altsecurityidentities"></span><span id="ALTSECURITYIDENTITIES"></span>[**altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities)
</dt> <dd>

[**L'attributo altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities) è un attributo multivalore che contiene i mapping per i certificati X.509 o gli account utente Kerberos esterni a questo utente ai fini dell'autenticazione. Diversi pacchetti di sicurezza, tra cui il pacchetto di autenticazione a chiave pubblica e Kerberos, usano questi dati per autenticare gli utenti quando presentano la forma alternativa di identificazione, ad esempio certificato, ticket Kerberos UNIX e così via. Creare un token Windows 2000 basato sull'account utente corrispondente in modo che possa accedere alle risorse di sistema.

Per i certificati X.509, i valori devono essere i nomi dell'autorità di certificazione e del soggetto nei certificati 509v3, emessi da un'autorità di certificazione pubblica esterna, che esevranno essere mappati all'account utente usato per trovare un account per l'autenticazione. Il pacchetto SSL (Schannel) usa la sintassi seguente: X509: <somecertinfotype> somecertinfo. Ad esempio, il valore seguente specifica il DN dell'autorità emittente " " con il \<I\> DN "C=US,O=InternetCA,CN=APublicCertificateAuthority" e il DN dell'oggetto " " con il \<S\> DN "C=US,O=Fabrikam,OU=Sales,CN=Jeff Smith".


```C++
X509:<I>C=US,O=InternetCA,CN=APublicCertificateAuthority<S>C=US,O=Fabrikam,OU=Sales,CN=Jeff Smith
```



Tenere presente che \<S\> " " o " " e " " sono \<I> \<S\> supportati. La presenza solo \<I\> di " " non è supportata. Le applicazioni non devono modificare i valori all'interno di " \<I\> " o " " perché la corrispondenza \<S\> DN parziale non è supportata.

Per gli account Kerberos esterni, i valori devono essere il nome dell'account Kerberos. Il pacchetto Kerberos usa la sintassi seguente: "Kerberos:MITaccountname". Ad esempio, di seguito è riportato il valore per un account in Fabrikam.com:


```C++
Kerberos:Jeff.Smith@Fabrikam.com
```



</dd> <dt>

<span id="badPasswordTime"></span><span id="badpasswordtime"></span><span id="BADPASSWORDTIME"></span>[**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)
</dt> <dd>

Non replicata. [**L'attributo badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime) specifica l'ultimo tentativo di accesso dell'utente all'account usando una password non corretta. Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100 nanosecondi dal 1° gennaio 1601 (UTC). Questo attributo viene mantenuto separatamente in ogni controller di dominio nel dominio. Il valore zero indica che l'ora dell'ultima password non valida è sconosciuta. Per ottenere un valore accurato per l'ora dell'ultima password non valida dell'utente nel dominio, è necessario eseguire query su ogni controller di dominio nel dominio e usare il valore più grande.

</dd> <dt>

<span id="badPwdCount"></span><span id="badpwdcount"></span><span id="BADPWDCOUNT"></span>[**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)
</dt> <dd>

Non replicata. [**L'attributo badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount) specifica il numero di tentativi di accesso dell'utente all'account usando una password non corretta. Questo attributo viene mantenuto separatamente in ogni controller di dominio nel dominio. Il valore 0 indica che il valore è sconosciuto. Per ottenere un valore accurato per i tentativi di password non validi totali dell'utente nel dominio, è necessario eseguire query su ogni controller di dominio nel dominio e usare la somma dei valori.

</dd> <dt>

<span id="codePage"></span><span id="codepage"></span><span id="CODEPAGE"></span>[**Codepage**](/windows/desktop/ADSchema/a-codepage)
</dt> <dd>

[**L'attributo codePage**](/windows/desktop/ADSchema/a-codepage) specifica la tabella codici per la lingua scelta dall'utente. Questo valore non viene usato da Windows 2000.

</dd> <dt>

<span id="countryCode"></span><span id="countrycode"></span><span id="COUNTRYCODE"></span>[**Countrycode**](/windows/desktop/ADSchema/a-countrycode)
</dt> <dd>

[**L'attributo countryCode**](/windows/desktop/ADSchema/a-countrycode) specifica il codice paese/area geografica per la lingua dell'utente. Questo valore non viene usato da Windows 2000.

</dd> <dt>

<span id="homeDirectory"></span><span id="homedirectory"></span><span id="HOMEDIRECTORY"></span>[**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)
</dt> <dd>

[**L'attributo homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) specifica il percorso della home directory per l'utente. La stringa può essere Null.

Se [**homeDrive è**](/windows/desktop/ADSchema/a-homedrive) impostato e specifica una lettera di unità, [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) deve essere un percorso UNC. Il percorso deve essere un percorso UNC di rete della directory della \\ \\ condivisione del server \\ \\ form. Questo valore può essere una stringa Null.

Se [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) non è impostato, [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) deve essere un percorso locale, ad esempio C: \\ mylocaldir.

</dd> <dt>

<span id="homeDrive"></span><span id="homedrive"></span><span id="HOMEDRIVE"></span>[**Homedrive**](/windows/desktop/ADSchema/a-homedrive)
</dt> <dd>

[**L'attributo homeDrive**](/windows/desktop/ADSchema/a-homedrive) specifica la lettera di unità a cui eseguire il mapping del percorso UNC specificato da **homeDirectory**. La lettera di unità deve essere specificata nel formato seguente:


```C++
<drive letter>:
```



dove " \<drive letter\> " è la lettera dell'unità di cui eseguire il mapping. Esempio:


```C++
Z:
```



Se questo attributo non è impostato, [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) deve essere un percorso locale, ad esempio C: \\ mylocaldir.

</dd> <dt>

<span id="lastLogoff"></span><span id="lastlogoff"></span><span id="LASTLOGOFF"></span>[**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)
</dt> <dd>

Non replicata. [**L'attributo lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff) specifica quando si è verificata l'ultima disconnessione. Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100 nanosecondi dal 1° gennaio 1601 (UTC). La parte alta di questo intero di grandi dimensioni corrisponde al membro **dwHighDateTime** della struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e la parte inferiore corrisponde al membro **dwLowDateTime** della struttura **FILETIME.** Questo attributo viene mantenuto separatamente in ogni controller di dominio nel dominio. Il valore zero indica che l'ora dell'ultima disconnessione è sconosciuta. Per ottenere un valore accurato per l'ultima disconnessione dell'utente nel dominio, è necessario eseguire query su ogni controller di dominio nel dominio e usare il valore più grande.

</dd> <dt>

<span id="lastLogon"></span><span id="lastlogon"></span><span id="LASTLOGON"></span>[**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)
</dt> <dd>

Non replicata. [**L'attributo lastLogon**](/windows/desktop/ADSchema/a-lastlogon) specifica quando si è verificato l'ultimo accesso. Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100 nanosecondi dal 1° gennaio 1601 (UTC). La parte alta di questo intero di grandi dimensioni corrisponde al membro **dwHighDateTime** della struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e la parte inferiore corrisponde al membro **dwLowDateTime** della struttura **FILETIME.** Questo attributo viene mantenuto separatamente in ogni controller di dominio nel dominio. Il valore zero indica che l'ora dell'ultimo accesso è sconosciuta. Per ottenere un valore accurato per l'ultimo accesso dell'utente nel dominio, è necessario eseguire query su ogni controller di dominio nel dominio e usare il valore più grande.

</dd> <dt>

<span id="lmPwdHistory"></span><span id="lmpwdhistory"></span><span id="LMPWDHISTORY"></span>[**lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory)
</dt> <dd>

[**L'attributo lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory) è la cronologia delle password dell'utente in formato unidiredirezione LAN Manager (LM). L'OWF LM viene usato per la compatibilità con i client DIN Manager 2.x, Windows 95 e Windows 98. Questo attributo viene usato solo dal sistema operativo. Tenere presente che non è possibile derivare la password in testo non crittografato dal formato OWF della password.

</dd> <dt>

<span id="logonCount"></span><span id="logoncount"></span><span id="LOGONCOUNT"></span>[**logonCount**](/windows/desktop/ADSchema/a-logoncount)
</dt> <dd>

Non replicata. [**L'attributo logonCount**](/windows/desktop/ADSchema/a-logoncount) conta il numero di volte in cui l'utente ha tentato di accedere a questo account. Questo attributo viene mantenuto in ogni controller di dominio nel dominio. Il valore 0 indica che il valore è sconosciuto. Per ottenere un valore accurato per il numero totale di tentativi di accesso riusciti dell'utente nel dominio, è necessario eseguire query su ogni controller di dominio nel dominio e usare la somma dei valori.

</dd> <dt>

<span id="mail"></span><span id="MAIL"></span>[**Posta**](/windows/desktop/ADSchema/a-mail)
</dt> <dd>

[**L'attributo mail**](/windows/desktop/ADSchema/a-mail) è un attributo a valore singolo che contiene l'indirizzo SMTP per l'utente, ad esempio " jeff@Fabrikam.com ".

</dd> <dt>

<span id="maxStorage"></span><span id="maxstorage"></span><span id="MAXSTORAGE"></span>[**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)
</dt> <dd>

[**L'attributo maxStorage**](/windows/desktop/ADSchema/a-maxstorage) specifica la quantità massima di spazio su disco rigido che l'utente può usare. Usare il **valore USER \_ MAXSTORAGE \_ UNLIMITED** (definito in Lmaccess.h) per usare tutto lo spazio disponibile su disco.

</dd> <dt>

<span id="memberOf"></span><span id="memberof"></span><span id="MEMBEROF"></span>[**Memberof**](/windows/desktop/ADSchema/a-memberof)
</dt> <dd>

[**L'attributo memberOf**](/windows/desktop/ADSchema/a-memberof) è un attributo multivalore che contiene gruppi di cui l'utente è un membro diretto, ad eccezione del gruppo primario, rappresentato da [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid). L'appartenenza al gruppo dipende dal controller di dominio (DC) da cui viene recuperato questo attributo:

-   In un controller di dominio per il dominio che contiene l'utente, [**memberOf**](/windows/desktop/ADSchema/a-memberof) per l'utente è completo rispetto all'appartenenza per i gruppi in tale dominio; tuttavia, **memberOf** non contiene l'appartenenza dell'utente ai gruppi locali e globali del dominio in altri domini.
-   In un server GC, [**memberOf**](/windows/desktop/ADSchema/a-memberof) per l'utente è completo rispetto a tutte le appartenenze a gruppi universali.

Se entrambe le condizioni sono vere per il controller di dominio, entrambi i set di dati sono contenuti in [**memberOf.**](/windows/desktop/ADSchema/a-memberof)

Tenere presente che questo attributo elenca i gruppi che contengono l'utente nell'attributo membro, non contiene l'elenco ricorsivo di predecessori annidati. Ad esempio, se l'utente O è un membro del gruppo C e il gruppo B e il gruppo B sono annidati nel gruppo A, l'attributo [**memberOf**](/windows/desktop/ADSchema/a-memberof) dell'utente O elenca il gruppo C e il gruppo B, ma non il gruppo A.

Questo attributo non viene archiviato, ma è un attributo di back link calcolato.

</dd> <dt>

<span id="ntPwdHistory"></span><span id="ntpwdhistory"></span><span id="NTPWDHISTORY"></span>[**ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory)
</dt> <dd>

[**L'attributo ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory) è la cronologia delle password dell'utente in Windows NT unidirezione (OWF). Windows 2000 usa il Windows NT OWF. Questo attributo viene usato solo dal sistema operativo. Tenere presente che non è possibile ricavare la password in testo non crittografato dal formato OWF della password.

</dd> <dt>

<span id="otherMailbox"></span><span id="othermailbox"></span><span id="OTHERMAILBOX"></span>[**Other(Altro)**](/windows/desktop/ADSchema/a-othermailbox)
</dt> <dd>

[**L'attributo otherAttribute**](/windows/desktop/ADSchema/a-othermailbox) è un attributo multivalore che contiene altri indirizzi di posta elettronica aggiuntivi in un modulo, ad esempio "CCMAIL: JeffSmith".

</dd> <dt>

<span id="PasswordExpirationDate"></span><span id="passwordexpirationdate"></span><span id="PASSWORDEXPIRATIONDATE"></span>[**PasswordExpirationDate**](/windows/desktop/ADSI/iadsuser-property-methods)
</dt> <dd>

La data di scadenza della password non è un attributo dell'oggetto utente. Si tratta di un valore calcolato basato sulla somma di [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) per l'utente e [**di maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) del dominio dell'utente. Per ottenere la data di scadenza della password, ottenere la [**proprietà IADsUser.PasswordExpirationDate.**](/windows/desktop/ADSI/iadsuser-property-methods) Non è possibile modificare questo attributo per un utente. impostare invece la [**proprietà IADsDomain.MaxPasswordAge**](/windows/desktop/ADSI/iadsdomain-property-methods) per modificare l'impostazione per il dominio.

</dd> <dt>

<span id="primaryGroupID"></span><span id="primarygroupid"></span><span id="PRIMARYGROUPID"></span>[**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid)
</dt> <dd>

[**L'attributo primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) è un attributo a valore singolo che contiene [**il primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) del gruppo che è il gruppo primario dell'oggetto. Il gruppo primario dell'oggetto non è incluso [**nell'attributo memberOf.**](/windows/desktop/ADSchema/a-memberof) Ad esempio, per impostazione predefinita, il gruppo primario di un oggetto utente è **primaryGroupToken** del gruppo Domain Users, ma il gruppo Domain Users non fa parte dell'attributo **memberOf dell'oggetto** utente.

</dd> <dt>

<span id="profilePath"></span><span id="profilepath"></span><span id="PROFILEPATH"></span>[**profilePath**](/windows/desktop/ADSchema/a-profilepath)
</dt> <dd>

[**L'attributo profilePath**](/windows/desktop/ADSchema/a-profilepath) specifica un percorso al profilo dell'utente. Questo valore può essere una stringa Null, un percorso assoluto locale o un percorso UNC.

</dd> <dt>

<span id="pwdLastSet"></span><span id="pwdlastset"></span><span id="PWDLASTSET"></span>[**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)
</dt> <dd>

[**L'attributo pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) specifica l'ultima modifica della password. Questo valore viene archiviato come intero grande che rappresenta il numero di intervalli di 100 nanosecondi dal 1° gennaio 1601 (UTC).

Il sistema usa il valore di questo attributo e l'attributo [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) del dominio che contiene l'oggetto utente per calcolare la data di scadenza della password. Ciò significa che la somma di [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) per l'utente e **maxPwdAge** del dominio dell'utente.

Questo attributo controlla se l'utente deve modificare la password al successivo accesso dell'utente. Se [**pwdLastSet è**](/windows/desktop/ADSchema/a-pwdlastset) zero, il valore predefinito, l'utente deve modificare la password all'accesso successivo. Il valore -1 indica che l'utente non deve modificare la password all'accesso successivo. Il sistema imposta questo valore su -1 dopo che l'utente ha impostato la password.

</dd> <dt>

<span id="sAMAccountType"></span><span id="samaccounttype"></span><span id="SAMACCOUNTTYPE"></span>[**sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype)
</dt> <dd>

[**L'attributo sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype) specifica un numero intero che rappresenta il tipo di conto. Questa proprietà viene impostata dal sistema operativo quando viene creato l'oggetto .

</dd> <dt>

<span id="scriptPath"></span><span id="scriptpath"></span><span id="SCRIPTPATH"></span>[**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)
</dt> <dd>

[**L'attributo scriptPath**](/windows/desktop/ADSchema/a-scriptpath) specifica il percorso dello script di accesso dell'utente, con estensione cmd, .exe o .bat file. La stringa può essere Null.

</dd> <dt>

<span id="unicodePwd"></span><span id="unicodepwd"></span><span id="UNICODEPWD"></span>[**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd)
</dt> <dd>

[**L'attributo unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd) è la password utente.

Per impostare la password utente, usare il metodo [**IADsUser.ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) se lo script o l'applicazione consente all'utente di modificare la propria password oppure il metodo [**IADsUser.SetPassword,**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) se lo script o l'applicazione consente a un amministratore di reimpostare una password.

Password dell'utente in Windows NT unidirezione (OWF). Windows 2000 usa il Windows NT OWF. Questo attributo viene usato solo dal sistema operativo. Tenere presente che non è possibile ricavare la password in testo non crittografato dal formato OWF della password.

</dd> <dt>

<span id="userAccountControl"></span><span id="useraccountcontrol"></span><span id="USERACCOUNTCONTROL"></span>[**Useraccountcontrol**](/windows/desktop/ADSchema/a-useraccountcontrol)
</dt> <dd>

[**L'attributo userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) specifica i flag che controllano il comportamento di password, blocco, disabilitazione/abilitazione, script e home directory per l'utente. Questo attributo contiene anche un flag che indica il tipo di account dell'oggetto. Per l'oggetto utente è in genere impostato \_ l'account UF \_ NORMAL.

I flag seguenti sono definiti in Lmaccess.h.



| Flag                     | Descrizione                                                                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UF \_ SCRIPT               | Script di accesso eseguito. Questo valore deve essere impostato per LAN Manager 2.0 o Windows NT.                                                                             |
| UF \_ ACCOUNTDISABLE       | L'account utente è disabilitato.                                                                                                                                    |
| UF \_ HOMEDIR \_ OBBLIGATORIO    | La home directory è obbligatoria. Questo valore viene ignorato in Windows NT e Windows 2000.                                                                            |
| UF \_ PASSWD \_ NOTREQD      | Non è necessaria alcuna password.                                                                                                                                         |
| UF \_ PASSWD \_ CANT \_ CHANGE | L'utente non può modificare la password.                                                                                                                             |
| BLOCCO \_ UF              | L'account è attualmente bloccato. Questo valore può essere cancellato per sbloccare un account bloccato in precedenza. Questo valore non può essere usato per bloccare un account bloccato in precedenza. |
| UF \_ DONT \_ EXPIRE \_ PASSWD | Rappresenta la password, che non deve mai scadere nell'account.                                                                                               |



 

I flag seguenti descrivono il tipo di account. È possibile impostare un solo valore. Non è possibile modificare il tipo di account.



| Flag                            | Descrizione                                                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ACCOUNT \_ NORMALE UF \_             | Si tratta di un tipo di account predefinito che rappresenta un utente tipico.                                                                                                                                                                                  |
| UF \_ TEMP \_ DUPLICATE \_ ACCOUNT    | Si tratta di un account per gli utenti il cui account primario si trova in un altro dominio. Questo account fornisce l'accesso utente a questo dominio, ma non a qualsiasi dominio che considera attendibile questo dominio. User Manager fa riferimento a questo tipo di account come account utente locale. |
| ACCOUNT DI \_ ATTENDIBILITÀ WORKSTATION UF \_ \_ | Si tratta di un account computer per una workstation Windows NT/Windows 2000 Professional o Windows NT Server/Windows 2000 Server membro di questo dominio.                                                                                     |
| ACCOUNT TRUST DEL SERVER UF \_ \_ \_      | Si tratta di un account computer per un controller Windows NT backup di backup che è membro di questo dominio.                                                                                                                                           |
| ACCOUNT TRUST TRA DOMINI UF \_ \_ \_ | Si tratta di un account di attendibilità per un Windows NT che considera attendibile altri domini.                                                                                                                                                            |



 

</dd> <dt>

<span id="userCertificate"></span><span id="usercertificate"></span><span id="USERCERTIFICATE"></span>[**Usercertificate**](/windows/desktop/ADSchema/a-usercertificate)
</dt> <dd>

[**L'attributo userCertificate**](/windows/desktop/ADSchema/a-usercertificate) è un attributo multivalore che contiene i certificati X509v3 con codifica DER rilasciati all'utente. Tenere presente che questo attributo contiene i certificati a chiave pubblica rilasciati a questo utente dal Servizio certificati Microsoft.

</dd> <dt>

<span id="userSharedFolder"></span><span id="usersharedfolder"></span><span id="USERSHAREDFOLDER"></span>[**userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder)
</dt> <dd>

[**L'attributo userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder) specifica un percorso UNC della cartella documenti condivisi dell'utente. Il percorso deve essere un percorso UNC di rete della directory della \\ \\ condivisione del server \\ \\ form. Questo valore può essere una stringa Null.

</dd> <dt>

<span id="userWorkstations"></span><span id="userworkstations"></span><span id="USERWORKSTATIONS"></span>[**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)
</dt> <dd>

[**L'attributo userWorkstations**](/windows/desktop/ADSchema/a-userworkstations) è un attributo a valore singolo che contiene i nomi NetBIOS delle workstation da cui l'utente può accedere. Ogni nome NetBIOS è separato da una virgola.

Se non è impostato alcun valore, significa che non è presente alcuna restrizione. Per disabilitare gli accessi da tutte le workstation a questo account, impostare il valore UF \_ ACCOUNTDISABLE (definito in Lmaccess.h) [**nell'attributo userAccountControl.**](/windows/desktop/ADSchema/a-useraccountcontrol)

</dd> </dl>

 

 
