---
description: Utilizzato per proteggere le singole parti di un'applicazione in un ambiente bloccato. Può essere usato con l'installazione di file, chiavi del registro di sistema e cartelle create.
ms.assetid: 7c20e211-7704-49c2-a0c5-aaa695a09764
title: Tabella LockPermissions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c07402b80caec7beff68083567f2ff2fb9bf5eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311734"
---
# <a name="lockpermissions-table"></a>Tabella LockPermissions

La tabella LockPermissions viene utilizzata per proteggere le singole parti di un'applicazione in un ambiente bloccato. Può essere usato con l'installazione di file, chiavi del registro di sistema e cartelle create.

Un pacchetto progettato per l'installazione in Windows Server 2008 R2 o Windows 7 deve usare la [tabella MsiLockPermissionsEx](msilockpermissionsex-table.md) anziché la tabella LockPermissions. Windows Installer versioni precedenti alla Windows Installer 5,0 ignorano la tabella MsiLockPermissionsEx. Windows Installer 5,0 può installare un pacchetto che contiene la tabella LockPermissions. A partire da Windows Installer 5,0, l'installazione di un pacchetto che contiene sia la tabella MsiLockPermissionsEx che la tabella LockPermissions ha esito negativo e restituisce Windows Installer messaggio di errore 1941.

La tabella LockPermissions include le colonne seguenti.



| Colonna     | Tipo                               | Chiave | Nullable |
|------------|------------------------------------|-----|----------|
| LockObject | [Identificatore](identifier.md)       | S   | N        |
| Tabella      | [Text](text.md)                   | S   | N        |
| Dominio     | [Formattato](formatted.md)         | S   | S        |
| User       | [Formattato](formatted.md)         | S   | N        |
| Autorizzazione | [DoubleInteger](doubleinteger.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="LockObject"></span><span id="lockobject"></span><span id="LOCKOBJECT"></span>LockObject
</dt> <dd>

Questa colonna e la colonna della tabella specificano insieme il file, la directory o la chiave del registro di sistema da proteggere. La colonna LockObject è una chiave esterna che punta alla chiave primaria della tabella specificata dalla colonna della tabella.

</dd> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo
</dt> <dd>

Questa colonna e la colonna LockObject specificano il file, la directory o la chiave del registro di sistema da proteggere. Nella colonna della tabella immettere file, Registry o CreateFolder per specificare un LockObject elencato nella tabella [file](file-table.md), nella [tabella del registro di sistema](registry-table.md)o nella [tabella CreateFolder](createfolder-table.md).

</dd> <dt>

<span id="Domain"></span><span id="domain"></span><span id="DOMAIN"></span>Dominio
</dt> <dd>

Colonna che identifica il dominio dell'utente per il quale devono essere impostate le autorizzazioni. Si tratta del nome di un computer autonomo o di un nome di dominio. Il tipo di dati della colonna è [formattato](formatted.md)ed è possibile usare la stringa \[ % UserDomain \] in questo campo per ottenere il valore della variabile di ambiente UserDomain per il dominio corrente. Per ottenere qualsiasi altro dominio, è necessario usare [azioni personalizzate](custom-actions.md). Per ulteriori informazioni, vedere la tabella delle azioni personalizzata.

</dd> <dt>

<span id="User"></span><span id="user"></span><span id="USER"></span>Utente
</dt> <dd>

Colonna che identifica il nome localizzato dell'utente per il quale devono essere impostate le autorizzazioni. Questo nome deve trovarsi nel computer o nel dominio. L'installazione non riesce se il computer o il controller di dominio non riconosce la combinazione di dominio e utente o se non è possibile recuperare l'ID di sicurezza (SID) dell'utente. È possibile specificare più utenti per un singolo LockObject.

I nomi utente comuni "Everyone" e "Administrators" possono essere immessi in inglese e sono mappati a SID noti. Per LocalSystem viene fornito il controllo completo in tutti i descrittori di sicurezza creati tramite la tabella LockPermissions. È possibile usare la proprietà [**ComputerName**](computername.md), la proprietà [**LogonUser**](logonuser.md) o la [**proprietà UserName**](username.md) in questo campo per ottenere l'utente corrente. Per immettere il nome localizzato di un altro utente o gruppo, è necessaria un'azione personalizzata.

Per specificare gli elenchi di controllo di accesso per più utenti, è possibile usare più record con LockObject e voci di tabella identici (ma con voci utente diverse).

</dd> <dt>

<span id="Permission"></span><span id="permission"></span><span id="PERMISSION"></span>Autorizzazione
</dt> <dd>

Colonna che identifica la descrizione intera dei privilegi di sistema. Di seguito sono riportati i valori usati più di frequente (un elenco completo esiste in Winnt. h).



| Privilege                                                              | Descrizione                     |
|------------------------------------------------------------------------|---------------------------------|
| tutti GENERIci \_<br/> 0X10000000<br/> 268435456<br/>     | Accesso in lettura, scrittura ed esecuzione |
| esecuzione GENERIca \_<br/> 0X20000000<br/> 536870912<br/> | Esegui accesso                  |
| scrittura GENERIca \_<br/> 0X40000000<br/> 1073741824<br/>  | Accesso in scrittura                    |



 

Non è possibile specificare \_ la lettura generica nella colonna autorizzazione. Il tentativo di eseguire questa operazione avrà esito negativo. Al contrario, è necessario specificare un valore, ad esempio lettura chiave \_ o \_ lettura file generica \_ .

Il valore null immesso in questa colonna è riservato per un utilizzo futuro.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le azioni [InstallFiles](installfiles-action.md), [WriteRegistryValori consente](writeregistryvalues-action.md)e [CreateFolders](createfolders-action.md) nelle [*tabelle di sequenza*](s-gly.md) elaborano le informazioni contenute in questa tabella. Per informazioni sull'utilizzo di *tabelle di sequenza*, vedere [utilizzo di una tabella di sequenza](using-a-sequence-table.md).

L'autorizzazione può essere impostata solo nella tabella LockPermissions per gli utenti già presenti nel computer o nel dominio. Il tentativo di impostare le autorizzazioni per un utente sconosciuto comporta l'esito negativo dell'installazione, anche se tale account utente viene creato durante l'installazione mediante un'azione personalizzata posticipata.

Si consiglia di includere il gruppo locale dell'amministratore di sistema in tutti gli elenchi di controllo di accesso (ACL). Ciò garantisce che l'amministratore di sistema possa accedere e gestire gli oggetti.

Ogni file, chiave del registro di sistema o directory elencato nella tabella LockPermissions riceve un descrittore di sicurezza esplicito, indipendentemente dal fatto che venga sostituito o meno un oggetto esistente. Il Windows Installer tenta di mantenere la sicurezza per gli oggetti già presenti nel sistema. Se un oggetto non è elencato nella tabella LockPermissions e sostituisce un oggetto esistente, la sostituzione ottiene le impostazioni di sicurezza dell'oggetto che sostituisce.

Se un oggetto non è elencato nella tabella LockPermissions e non sostituisce un oggetto esistente, non riceve alcun descrittore di sicurezza esplicito. L'accesso al nuovo oggetto si basa sugli attributi del relativo oggetto padre o contenitore. Se un oggetto non è elencato nella tabella e sostituisce un oggetto senza descrittore di sicurezza esplicito, l'accesso al nuovo oggetto si basa sugli attributi del relativo oggetto padre o contenitore.

Il Windows Installer imposta la proprietà [**UserSID**](usersid.md) sull'ID di sicurezza (SID) o sull'utente che esegue l'installazione.

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE55](ice55.md)  
</dl>

 

 




