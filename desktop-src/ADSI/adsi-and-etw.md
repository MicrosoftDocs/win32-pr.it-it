---
title: Traccia eventi in ADSI
description: Windows Server 2008 e Windows Vista introducono Traccia eventi in Active Directory Service Interfaces (ADSI).
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- traccia eventi ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59b2db3775c8c578ad361667a2d89c36240caf4b3bbb4bcd5cdd2798011514b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023979"
---
# <a name="event-tracing-in-adsi"></a>Traccia eventi in ADSI

Windows Server 2008 e Windows Vista introducono [Traccia](/windows/desktop/ETW/event-tracing-portal) eventi in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI). Alcune aree del provider LDAP ADSI hanno un'implementazione sottostante complessa o che prevede una sequenza di passaggi che rende difficile diagnosticare i problemi. Per consentire agli sviluppatori di applicazioni di risolvere i problemi, Traccia eventi è stato aggiunto alle aree seguenti:

## <a name="schema-parsing-and-downloading"></a>Analisi e download dello schema

L'interfaccia IADs in ADSI richiede che lo schema LDAP venga memorizzato nella cache del client in modo che sia possibile effettuare correttamente il marshalling degli attributi ( come descritto nel modello [di schema ADSI](adsi-schema-model.md)). A tale scopo, ADSI carica lo schema per ogni processo (e per ogni server/dominio LDAP) in memoria da un file di schema (con estensione sch) salvato sul disco locale o scaricarlo dal server LDAP. Processi diversi nello stesso computer client usano lo schema memorizzato nella cache su disco, se disponibile e applicabile.

Se non è possibile ottenere lo schema dal disco o dal server, ADSI usa uno schema predefinito hardcoded. In questo caso, non è possibile effettuare il marshalling degli attributi che non fanno parte di questo schema predefinito e ADSI restituisce un errore durante il recupero di questi attributi. Questa operazione può essere causata da diversi fattori, tra cui problemi di analisi dello schema e privilegi insufficienti per scaricare lo schema. Spesso è difficile determinare il motivo per cui viene usato un determinato schema predefinito. L'uso di Traccia eventi in questa area consente di diagnosticare più rapidamente il problema e risolverlo.

## <a name="changing-and-setting-the-password"></a>Modifica e impostazione della password

[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) e [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) utilizzano più meccanismi per eseguire l'operazione richiesta in base alla configurazione disponibile , come descritto in Impostazione e modifica delle password utente [con il provider LDAP](setting-user-passwords-for-ldap-providers.md). Quando **ChangePassword** e **SetPassword** hanno esito negativo, può essere difficile determinare esattamente il motivo e Traccia eventi consente di risolvere i problemi con questi metodi.

## <a name="adsi-bind-cache"></a>Cache di binding ADSI

ADSI tenta internamente di riutilizzare le connessioni LDAP quando possibile (vedere [Connessione Caching](connection-caching.md)). Durante la risoluzione dei problemi, è utile verificare se è stata aperta una nuova connessione per la comunicazione con il server o se è stata usata una connessione esistente. Può anche essere utile tracciare il ciclo di vita della cache di connessione (talvolta definita cache di binding) e la relativa creazione o chiusura e se è stata verificata una segnalazione di connessione. Nel caso di un'associazione [serverless,](/windows/desktop/AD/serverless-binding-and-rootdse)ADSI chiama il localizzatore dc per selezionare un server per il dominio del contesto dell'utente. ADSI gestisce quindi una cache del mapping dominio-server per le connessioni successive. Traccia eventi consente di tracciare la selezione del controller di dominio ed è quindi utile per la risoluzione dei problemi relativi alla connessione.

## <a name="enabling-tracing-and-starting-a-tracing-session"></a>Abilitazione della traccia e avvio di una sessione di traccia

Per attivare la traccia ADSI, creare la chiave del Registro di sistema seguente:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **_ProcessName_**

*ProcessName* è il nome completo del processo che si vuole tracciare, inclusa l'estensione (ad esempio, "Svchost.exe"). È anche possibile inserire un valore facoltativo di tipo **DWORD** denominato PID in questa chiave. È consigliabile impostare questo valore e quindi tracciare solo un processo specifico. In caso contrario, verranno tracciate tutte le istanze dell'applicazione specificate da *ProcessName.*

Eseguire quindi il comando seguente:

**tracelog.exe -start** *sessionname* **-guid \#** provider _\_ guid_ **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*

*sessionname* è semplicemente un identificatore arbitrario usato per etichettare la sessione di traccia. Sarà necessario fare riferimento a questo nome di sessione in un secondo momento quando si arresta la sessione di traccia. Il GUID per il provider di rilevamento ADSI è "7288c9f8-d63c-4932-a345-89d6b060174d". *filename* specifica il file di log in cui verranno scritti gli eventi. *traceFlags* deve essere uno dei valori seguenti:



|         Flag                        |         valore              |
|---------------------------------|-----------------------|
| **SCHEMA DI \_ DEBUG**<br/>    | 0x00000001<br/> |
| **ESEGUIRE \_ IL DEBUG DI CHANGEPWD**<br/> | 0x00000002<br/> |
| **DEBUG \_ SETPWD**<br/>    | 0x00000004<br/> |
| **ESEGUIRE IL DEBUG \_ DI BINDCACHE**<br/> | 0x00000008<br/> |



 

Questi flag determinano [quali metodi ADSI](active-directory-service-interfaces-adsi.md) verranno tracciati, in base alla tabella seguente:



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
<li>CADsUser::ChangePassword</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><strong>DEBUG_SETPWD</strong><br/></td>
<td><ul>
<li>CADsUser::SetPassword</li>
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



 

È possibile combinare i flag combinando i bit appropriati *nell'argomento traceFlags.* Ad esempio, per specificare i **flag DEBUG \_ SCHEMA** e **DEBUG \_ BINDCACHE,** il valore *traceFlags* appropriato sarà 0x00000009.

Infine, il flag *traceLevel* deve essere uno dei valori seguenti:



|      Flag                                    |       valore                |
|------------------------------------------|-----------------------|
| **ERRORE \_ DEL LIVELLO DI \_ TRACCIA**<br/>       | 0x00000002<br/> |
| **INFORMAZIONI \_ SUL LIVELLO DI \_ TRACCIA**<br/> | 0x00000004<br/> |



 

**TRACE \_ LEVEL \_ INFORMATION fa** sì che il processo di traccia registri tutti gli eventi, mentre TRACE LEVEL **\_ \_ ERROR** fa sì che il processo di traccia registri solo gli eventi di errore.

Per terminare la traccia, eseguire il comando seguente:

**tracelog.exe -stop** *sessionname*

Nell'esempio precedente *sessionname* è lo stesso nome di quello fornito con il comando che ha avviato la sezione di traccia.

## <a name="remarks"></a>Commenti

È più efficace tracciare solo processi specifici specificando un PID specifico piuttosto che tracciare tutti i processi in un computer. Se è necessario tracciare più applicazioni nello stesso computer, potrebbe verificarsi un impatto sulle prestazioni. è disponibile un output di debug sostanziale nelle sezioni del codice orientate alle prestazioni. Inoltre, gli amministratori devono prestare attenzione a impostare correttamente le autorizzazioni dei file di log durante la traccia di più processi. In caso contrario, qualsiasi utente potrebbe essere in grado di leggere i log di traccia e altri utenti saranno in grado di tracciare i processi che contengono informazioni protette.

Si supponga, ad esempio, che l'amministratore configura la traccia per un'applicazione "Test.exe" e non specifica un PID nel Registro di sistema per tracciare più istanze del processo. Ora un altro utente vuole tracciare l'applicazione "Secure.exe". Se i file di log di traccia non sono limitati correttamente, l'utente deve solo rinominare "Secure.exe" in "Test.exe" e ne verrà tracciata la traccia. In generale, è meglio tracciare solo processi specifici durante la risoluzione dei problemi e rimuovere la chiave del Registro di sistema di traccia non appena viene eseguita la risoluzione dei problemi.

Poiché l'abilitazione di Traccia eventi produrrà file di log aggiuntivi, gli amministratori devono monitorare attentamente le dimensioni dei file di log. La mancanza di spazio su disco nel computer locale può causare una negazione del servizio.

## <a name="example-scenarios"></a>Scenari di esempio

Scenario 1: l'amministratore rileva un errore imprevisto in un'applicazione che imposta le password per gli account utente, quindi deve seguire questa procedura per risolvere il problema usando Traccia eventi.

1.  Scrivere uno script che riproduci il problema e creare la chiave del Registro di sistema

    **HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **cscript.exe**

2.  Avviare una sessione di traccia, impostando *traceFlags* su 0x2 (**DEBUG \_ CHANGEPASSWD**) e *traceLevel* su 0x4 (**TRACE LEVEL \_ \_ INFORMATION**), usando il comando seguente:

    **tracelog.exe -start scripttrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ adsi.etl -flag 0x2 -level 0x4**

3.  Eseguire cscript.exe con lo script di test per riprodurre il problema e quindi terminare la sessione di traccia:

    **tracelog.exe -stop scripttrace**

4.  Eliminare la chiave del Registro di sistema

    **HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **cscript.exe**

5.  Eseguire lo strumento ETW Tracerpt.exe analizzare le informazioni di traccia dal log:

    **tracelog.exe -start scripttrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ adsi.etl -flag 0x2 -level 0x4**

Scenario 2: l'amministratore vuole tracciare le operazioni di analisi e download dello schema in un'applicazione [ASP](https://msdn.microsoft.com/asp.net/default.aspx) denominata w3wp.exe che è già in esecuzione. A tale scopo, l'amministratore deve seguire questa procedura:

1.  Creare la chiave del Registro di sistema

    **HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **w3wp.exe**

    e all'interno di tale chiave, creare un valore di tipo DWORD denominato PID e impostarlo sull'ID processo dell'istanza di w3wp.exe attualmente in esecuzione nel computer locale.

2.  Creano quindi una sessione di traccia, impostando *traceFlags* su 0x1 (**DEBUG \_ SCHEMA**) e *traceLevel* su 0x4 (**TRACE LEVEL \_ \_ INFORMATION**):

    **tracelog.exe -start w3wptrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ w3wp.etl -flag 0x1 -level 0x4**

3.  Riprodurre l'operazione che richiede la risoluzione dei problemi.
4.  Terminare la sessione di traccia:

    **tracelog.exe -stop w3wptrace**

5.  Eliminare la chiave del Registro di **sistema HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **w3wp.exe**.
6.  Eseguire lo strumento ETW tracerpt.exe analizzare le informazioni di traccia dal log:

    **tracerpt.exe . \\ w3wp.etl -o -report**

 

