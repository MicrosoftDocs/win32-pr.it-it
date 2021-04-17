---
title: Traccia eventi in ADSI
description: Windows Server 2008 e Windows Vista introducono la traccia eventi in Active Directory Service Interfaces (ADSI).
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- ADSI di traccia eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f43c0d840cd1f3f70d293a0a4f5c299fd129efe
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300424"
---
# <a name="event-tracing-in-adsi"></a>Traccia eventi in ADSI

Windows Server 2008 e Windows Vista introducono la [traccia eventi](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI). Alcune aree del provider LDAP ADSI hanno un'implementazione sottostante complessa o che prevede una sequenza di passaggi che rendono difficile la diagnosi dei problemi. Per consentire agli sviluppatori di applicazioni di risolvere i problemi, è stata aggiunta la traccia eventi alle aree seguenti:

## <a name="schema-parsing-and-downloading"></a>Analisi dello schema e download

Per l'interfaccia IADs in ADSI è necessario che lo schema LDAP venga memorizzato nella cache del client in modo che sia possibile effettuare il marshalling degli attributi correttamente (come descritto nel [modello di schema ADSI](adsi-schema-model.md)). A tale scopo, ADSI carica lo schema per ogni processo (e per ogni server/dominio LDAP) in memoria da un file di schema (SCH) salvato nel disco locale o dal server LDAP. Diversi processi nello stesso computer client utilizzano lo schema memorizzato nella cache su disco, se disponibile e applicabile.

Se non è possibile ottenere lo schema dal disco o dal server, ADSI usa uno schema predefinito hardcoded. Quando si verifica questa situazione, non è possibile effettuare il marshalling degli attributi che non fanno parte di questo schema predefinito e ADSI restituisce un errore durante il recupero di questi attributi. Una serie di fattori può causare questa situazione, inclusi i problemi di analisi dello schema e privilegi insufficienti per scaricare lo schema. Spesso è difficile determinare il motivo per cui viene utilizzato un determinato schema predefinito. L'uso della traccia eventi in quest'area consente di diagnosticare più rapidamente il problema e risolverlo.

## <a name="changing-and-setting-the-password"></a>Modifica e impostazione della password

[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) e [**password**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) impiegano più di un meccanismo per eseguire l'operazione richiesta in base alla configurazione disponibile, come descritto in [impostazione e modifica delle password utente con il provider LDAP](setting-user-passwords-for-ldap-providers.md). Quando **ChangePassword** e **sepassword** hanno esito negativo, può essere difficile determinare esattamente il motivo per cui la traccia eventi aiuterà a risolvere i problemi con questi metodi.

## <a name="adsi-bind-cache"></a>Cache di binding ADSI

ADSI tenta internamente di riutilizzare le connessioni LDAP laddove possibile (vedere [caching della connessione](connection-caching.md)). Quando si esegue la risoluzione dei problemi, è utile tracciare se è stata aperta una nuova connessione per la comunicazione con il server o se è stata utilizzata una connessione esistente. Può anche essere utile per tenere traccia del ciclo di vita della cache di connessione (talvolta definita cache di binding) e della relativa creazione o chiusura e se è stato rilevato un riferimento alla connessione. Nel caso di un' [associazione senza server](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI chiama il localizzatore DC per selezionare un server per il dominio del contesto dell'utente. ADSI gestisce quindi una cache del mapping del server di dominio per le connessioni successive. La traccia eventi consente di tracciare la selezione del controller di dominio ed è quindi utile per la risoluzione dei problemi relativi alla connessione.

## <a name="enabling-tracing-and-starting-a-tracing-session"></a>Abilitazione della traccia e avvio di una sessione di traccia

Per attivare la traccia ADSI, creare la seguente chiave del registro di sistema:

**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Tracing** \\ ***ProcessName***

*ProcessName* è il nome completo del processo che si desidera tracciare, inclusa la relativa estensione, ad esempio "Svchost.exe". Inoltre, è possibile inserire un valore facoltativo di tipo **DWORD** denominato PID in questa chiave. È consigliabile impostare questo valore e quindi tracciare solo un processo specifico. In caso contrario, verranno tracciate tutte le istanze dell'applicazione specificata da *ProcessName* .

Eseguire quindi il comando seguente:

**tracelog.exe-avviare** *sessionname*  * *-GUID \# * * * \_ GUID del provider* **-f** *filename* **-flag** *flag* **-Level** *TraceLevel*

*sessionname* è semplicemente un identificatore arbitrario utilizzato per etichettare la sessione di traccia. quando si arresta la sessione di traccia, sarà necessario fare riferimento al nome della sessione in un secondo momento. Il GUID del provider di rilevamento ADSI è "7288c9f8-D63C-4932-A345-89d6b060174d". *filename* specifica il file di log in cui verranno scritti gli eventi. *flag* deve essere uno dei valori seguenti:



|                                 |                       |
|---------------------------------|-----------------------|
| **SCHEMA di DEBUG \_**<br/>    | 0x00000001<br/> |
| **CHANGEPWD di DEBUG \_**<br/> | 0x00000002<br/> |
| **Setpwd di DEBUG \_**<br/>    | 0x00000004<br/> |
| **BINDCACHE di DEBUG \_**<br/> | 0x00000008<br/> |



 

Questi flag determinano quali metodi [ADSI](active-directory-service-interfaces-adsi.md) verranno tracciati, in base alla tabella seguente:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>DEBUG_SCHEMA</strong><br/></td>
<td><ul>
<li>LdapGetSchema</li>
<li>GetSchemaInfoTime</li>
<li>LdapReadSchemaInfoFromServer</li>
<li>ProcessSchemaInfo</li>
<li>HelperReadLdapSchemaInfo</li>
<li>ProcessClassInfoArray</li>
<li>ReadSchemaInfoFromRegistry</li>
<li>StoreSchemaInfoFromRegistry</li>
<li>AttributeTypeDescription</li>
<li>ObjectClassDescription</li>
<li>DITContentRuleDescription</li>
<li>DirectoryString</li>
<li>DirectoryStrings</li>
<li>DITContentRuleDescription</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DEBUG_CHANGEPWD</strong><br/></td>
<td><ul>
<li>CADsUser:: ChangePassword</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><strong>DEBUG_SETPWD</strong><br/></td>
<td><ul>
<li>CADsUser:: password</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DEBUG_BINDCACHE</strong><br/></td>
<td><ul>
<li>GetServerBasedObject</li>
<li>GetServerLessBasedObject</li>
<li>GetGCDomainName</li>
<li>GetDefaultDomainName</li>
<li>GetUserDomainFlatName</li>
<li>BindCacheLookup</li>
<li>EquivalentPortNumbers</li>
<li>CanCredentialsBeReused</li>
<li>BindCacheAdd</li>
<li>BindCacheAddRef</li>
<li>AddReferralLink</li>
<li>CommonRemoveEntry</li>
<li>BindCacheDerefHelper</li>
<li>NotifyNewConnection</li>
<li>QueryForConnection</li>
<li>LdapOpenBindWithCredentials</li>
<li>LdapOpenBindWithDefaultCredentials</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

È possibile combinare i flag combinando i bit appropriati nell'argomento *flag* . Ad esempio, per specificare i flag **debug \_ schema** e **debug \_ BINDCACHE** , il valore *flag* appropriato sarà 0x00000009.

Infine, il flag *TraceLevel* deve essere uno dei valori seguenti:



|                                          |                       |
|------------------------------------------|-----------------------|
| **\_errore a livello di traccia \_**<br/>       | 0x00000002<br/> |
| **\_informazioni sul livello di traccia \_**<br/> | 0x00000004<br/> |



 

**Traccia \_ Le \_ informazioni sul livello** determinano la registrazione di tutti gli eventi da parte del processo di traccia, mentre l' **errore a \_ livello \_ di traccia** causa la registrazione solo degli eventi di errore.

Per terminare la traccia, eseguire il comando seguente:

**tracelog.exe-stop** *sessionname*

Nell'esempio precedente, *sessionname* ha lo stesso nome di quello fornito con il comando che ha avviato la sezione di traccia.

## <a name="remarks"></a>Commenti

È più efficace tracciare solo processi specifici specificando un determinato PID anziché tracciare tutti i processi in un computer. Se è necessario tracciare più applicazioni nello stesso computer, è possibile che si verifichi un effetto sulle prestazioni. è presente un output di debug sostanziale nelle sezioni orientate alle prestazioni del codice. Inoltre, gli amministratori devono prestare attenzione a impostare correttamente le autorizzazioni dei file di log durante la traccia di più processi. in caso contrario, qualsiasi utente potrebbe essere in grado di leggere i log di traccia e altri utenti saranno in grado di tracciare processi che contengono informazioni protette.

Si supponga, ad esempio, che l'amministratore imposti la traccia per un'applicazione "Test.exe" e non specifichi un PID nel registro di sistema per tracciare più istanze del processo. Un altro utente desidera quindi tracciare l'applicazione "Secure.exe". Se i file di log di traccia non sono limitati correttamente, è necessario che l'utente rinomi "Secure.exe" in "Test.exe" e verrà tracciato. In generale, è consigliabile tracciare solo processi specifici durante la risoluzione dei problemi e rimuovere la chiave del registro di sistema di traccia non appena viene eseguita la risoluzione dei problemi.

Poiché l'abilitazione della traccia eventi produrrà file di log aggiuntivi, gli amministratori dovrebbero monitorare attentamente le dimensioni dei file di registro; la mancanza di spazio su disco nel computer locale può causare un attacco Denial of Service.

## <a name="example-scenarios"></a>Scenari di esempio

Scenario 1: l'amministratore rileva un errore imprevisto in un'applicazione che imposta le password per gli account utente, in modo da eseguire la procedura seguente per risolvere il problema utilizzando la traccia eventi.

1.  Scrivere uno script per riprodurre il problema e creare la chiave del registro di sistema

    **HKEY \_ \_Computer locale** \\ **sistema** \\ **CurrentControlSet** \\ **Servizi** di \\  \\ **traccia** ADSI \\ **cscript.exe**

2.  Avviare una sessione di traccia, impostando *flag* su 0x2 (**debug \_ CHANGEPASSWD**) e *TraceLevel* su 0x4 (**\_ \_ informazioni sul livello di traccia**), usando il comando seguente:

    **tracelog.exe-Start scripttrace-GUID \# 7288c9f8-D63C-4932-A345-89d6b060174d-f. \\ ADSI. etl-flag 0x4 a livello di 0x2**

3.  Eseguire cscript.exe con lo script di test per riprodurre il problema e quindi terminare la sessione di traccia:

    **tracelog.exe arrestare scripttrace**

4.  Elimina la chiave del registro di sistema

    **HKEY \_ \_Computer locale** \\ **sistema** \\ **CurrentControlSet** \\ **Servizi** di \\  \\ **traccia** ADSI \\ **cscript.exe**

5.  Eseguire lo strumento ETW Tracerpt.exe per analizzare le informazioni di traccia dal log:

    **tracelog.exe-Start scripttrace-GUID \# 7288c9f8-D63C-4932-A345-89d6b060174d-f. \\ ADSI. etl-flag 0x4 a livello di 0x2**

Scenario 2: l'amministratore desidera tracciare le operazioni di analisi e download dello schema in un'applicazione [ASP](https://msdn.microsoft.com/asp.net/default.aspx) denominata w3wp.exe già in esecuzione. A tale scopo, l'amministratore deve eseguire le operazioni seguenti:

1.  Creazione della chiave del registro di sistema

    **HKEY \_ \_Computer locale** \\ **sistema** \\ **CurrentControlSet** \\ **Servizi** di \\  \\ **traccia** ADSI \\ **w3wp.exe**

    all'interno di tale chiave, creare un valore di tipo DWORD denominato PID e impostarlo sull'ID processo dell'istanza di w3wp.exe attualmente in esecuzione nel computer locale.

2.  Viene quindi creata una sessione di traccia, impostando *flag* su 0x1 (**\_ schema di debug**) e *TraceLevel* su 0x4 (**\_ \_ informazioni sul livello di traccia**):

    **tracelog.exe-Start w3wptrace-GUID \# 7288c9f8-D63C-4932-A345-89d6b060174d-f. \\ w3wp. etl-flag 0x4 a livello di 0x1**

3.  Riprodurre l'operazione che richiede la risoluzione dei problemi.
4.  Terminare la sessione di traccia:

    **tracelog.exe arrestare w3wptrace**

5.  Eliminare la chiave del registro di sistema **HKEY \_ Local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Tracing** \\ **w3wp.exe**.
6.  Eseguire lo strumento ETW tracerpt.exe per analizzare le informazioni di traccia dal log:

    **tracerpt.exe. \\ w3wp. etl-o-report**

 

