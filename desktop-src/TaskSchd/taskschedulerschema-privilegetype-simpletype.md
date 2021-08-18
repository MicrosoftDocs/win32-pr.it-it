---
title: Tipo semplice privilegeType
description: I privilegi determinano il tipo di operazioni di sistema che un account utente può eseguire. Un amministratore assegna privilegi agli account utente e di gruppo. I privilegi di ogni utente includono quelli concessi all'utente e ai gruppi a cui appartiene l'utente.
ms.assetid: 813b0886-ca76-4523-a1e6-42ca656851a7
keywords:
- privilegeType tipo semplice Utilità di pianificazione
topic_type:
- apiref
api_name:
- privilegeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4502c22e31ca131dabd6d776337c3693a4d4bf4d7753734cf0e6291cf234fbe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002289"
---
# <a name="privilegetype-simple-type"></a>Tipo semplice privilegeType

I privilegi determinano il tipo di operazioni di sistema che un account utente può eseguire. Un amministratore assegna privilegi agli account utente e di gruppo. I privilegi di ogni utente includono quelli concessi all'utente e ai gruppi a cui appartiene l'utente.

``` syntax
<xs:simpleType name="privilegeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="SeCreateTokenPrivilege"
         />
        <xs:enumeration
            value="SeAssignPrimaryTokenPrivilege"
         />
        <xs:enumeration
            value="SeLockMemoryPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseQuotaPrivilege"
         />
        <xs:enumeration
            value="SeUnsolicitedInputPrivilege"
         />
        <xs:enumeration
            value="SeMachineAccountPrivilege"
         />
        <xs:enumeration
            value="SeTcbPrivilege"
         />
        <xs:enumeration
            value="SeSecurityPrivilege"
         />
        <xs:enumeration
            value="SeTakeOwnershipPrivilege"
         />
        <xs:enumeration
            value="SeLoadDriverPrivilege"
         />
        <xs:enumeration
            value="SeSystemProfilePrivilege"
         />
        <xs:enumeration
            value="SeSystemtimePrivilege"
         />
        <xs:enumeration
            value="SeProfileSingleProcessPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseBasePriorityPrivilege"
         />
        <xs:enumeration
            value="SeCreatePagefilePrivilege"
         />
        <xs:enumeration
            value="SeCreatePermanentPrivilege"
         />
        <xs:enumeration
            value="SeBackupPrivilege"
         />
        <xs:enumeration
            value="SeRestorePrivilege"
         />
        <xs:enumeration
            value="SeShutdownPrivilege"
         />
        <xs:enumeration
            value="SeDebugPrivilege"
         />
        <xs:enumeration
            value="SeAuditPrivilege"
         />
        <xs:enumeration
            value="SeSystemEnvironmentPrivilege"
         />
        <xs:enumeration
            value="SeChangeNotifyPrivilege"
         />
        <xs:enumeration
            value="SeRemoteShutdownPrivilege"
         />
        <xs:enumeration
            value="SeUndockPrivilege"
         />
        <xs:enumeration
            value="SeSyncAgentPrivilege"
         />
        <xs:enumeration
            value="SeEnableDelegationPrivilege"
         />
        <xs:enumeration
            value="SeManageVolumePrivilege"
         />
        <xs:enumeration
            value="SeImpersonatePrivilege"
         />
        <xs:enumeration
            value="SeCreateGlobalPrivilege"
         />
        <xs:enumeration
            value="SeTrustedCredManAccessPrivilege"
         />
        <xs:enumeration
            value="SeRelabelPrivilege"
         />
        <xs:enumeration
            value="SeIncreaseWorkingSetPrivilege"
         />
        <xs:enumeration
            value="SeTimeZonePrivilege"
         />
        <xs:enumeration
            value="SeCreateSymbolicLinkPrivilege"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valori di enumerazione

Il **tipo semplice privilegeType** definisce i valori seguenti.



| Valore                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SeCreateTokenPrivilege          | Obbligatorio per creare un token primario. Diritto utente: creare un oggetto token.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeAssignPrimaryTokenPrivilege   | Obbligatorio per assegnare il token primario di un processo. Diritto utente: sostituire un token a livello di processo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeLockMemoryPrivilege           | Obbligatorio per bloccare le pagine fisiche in memoria. Diritto utente: bloccare le pagine in memoria. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeIncreaseQuotaPrivilege        | Obbligatorio per aumentare la quota assegnata a un processo. Diritto utente: regolare le quote di memoria per un processo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeUnsolicitedInputPrivilege     | Obbligatorio per leggere l'input non richiesto da un dispositivo terminale. Diritto utente: non applicabile. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SeMachineAccountPrivilege       | Obbligatorio per creare un account computer. Diritto utente: aggiungere workstation al dominio. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeTcbPrivilege                  | Questo privilegio identifica il titolare come parte della base di computer attendibili. Ad alcuni sottosistemi protetti attendibili viene concesso questo privilegio. Diritto utente: fungere da parte del sistema operativo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SeSecurityPrivilege             | Obbligatorio per eseguire una serie di funzioni correlate alla sicurezza, ad esempio il controllo e la visualizzazione dei messaggi di controllo. Questo privilegio identifica il titolare come operatore di sicurezza. Diritto utente: gestire il controllo e il log di sicurezza. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeTakeOwnershipPrivilege        | Obbligatorio per assumere la proprietà di un oggetto senza concedere l'accesso discrezionale. Questo privilegio consente di impostare il valore del proprietario solo su tali valori che il titolare può assegnare legittimamente come proprietario di un oggetto. Diritto utente: assumere la proprietà di file o altri oggetti. <br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| SeLoadDriverPrivilege           | Obbligatorio per caricare o scaricare un driver di dispositivo. Diritto utente: caricare e scaricare i driver di dispositivo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemProfilePrivilege        | Necessaria per raccogliere informazioni di profilatura per l'intero sistema. Diritto utente: profilare le prestazioni del sistema. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemtimePrivilege           | Obbligatorio per modificare l'ora di sistema. Diritto utente: modificare l'ora di sistema. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeProfileSingleProcessPrivilege | Obbligatorio per raccogliere informazioni di profilatura per un singolo processo. Diritto utente: profilare un singolo processo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseBasePriorityPrivilege | Obbligatorio per aumentare la priorità di base di un processo. Diritto utente: aumentare la priorità di pianificazione. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeCreatePagefilePrivilege       | Obbligatorio per creare un file di paging. Diritto utente: creare un file di paging. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| SeCreatePermanentPrivilege      | Obbligatorio per creare un oggetto permanente. Diritto utente: creare oggetti condivisi permanenti. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| SeBackupPrivilege               | Obbligatorio per eseguire operazioni di backup. Questo privilegio fa sì che il sistema concedi tutto il controllo di accesso in lettura a qualsiasi file, indipendentemente dall'elenco di controllo di accesso (ACL) specificato per il file. Qualsiasi richiesta di accesso diversa dalla lettura viene comunque valutata con l'ACL. Questo privilegio è richiesto dalle funzioni RegSaveKey e RegSaveKeyExfunctions. Se si dispone di questo privilegio, vengono concessi i diritti di accesso seguenti: READ \_ CONTROL, ACCESS \_ SYSTEM \_ SECURITY, FILE \_ GENERIC \_ READ, FILE \_ TRAVERSE. Diritto utente: eseguire il backup di file e directory. <br/>                                                                                                                                     |
| SeRestorePrivilege              | Obbligatorio per eseguire operazioni di ripristino. Questo privilegio fa sì che il sistema concedi tutto il controllo di accesso in scrittura a qualsiasi file, indipendentemente dall'ACL specificato per il file. Qualsiasi richiesta di accesso diversa dalla scrittura viene comunque valutata con l'ACL. Inoltre, questo privilegio consente di impostare qualsiasi ID di sicurezza (SID) di utenti o gruppi valido come proprietario di un file. Questo privilegio è richiesto dalla funzione RegLoadKey. Se si dispone di questo privilegio, vengono concessi i diritti di accesso seguenti: APPLICAZIONE LIVELLO DATI \_ WRITE, WRITE \_ OWNER, ACCESS \_ SYSTEM \_ SECURITY, FILE \_ GENERIC \_ WRITE, FILE ADD \_ \_ FILE, FILE ADD \_ \_ SUBDIRECTORY, DELETE. Diritto utente: ripristinare file e directory. <br/> |
| SeShutdownPrivilege             | Obbligatorio per arrestare un sistema locale. Diritto utente: arrestare il sistema. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeDebugPrivilege                | Necessario per eseguire il debug e modificare la memoria di un processo di proprietà di un altro account. Diritto utente: Eseguire il debug dei programmi. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeAuditPrivilege                | Obbligatorio per generare le voci del log di controllo. Concedere questo privilegio ai server protetti. Diritto utente: generare controlli di sicurezza. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| SeSystemEnvironmentPrivilege    | Necessario per modificare la RAM non volatile dei sistemi che usano questo tipo di memoria per archiviare le informazioni di configurazione. Diritto utente: modificare i valori dell'ambiente del firmware. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeChangeNotifyPrivilege         | Obbligatorio per ricevere notifiche di modifiche a file o directory. Questo privilegio fa anche in modo che il sistema salti tutti i controlli di accesso attraversamento. È abilitato per impostazione predefinita per tutti gli utenti. Diritto utente: ignora il controllo di attraversamento. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeRemoteShutdownPrivilege       | Necessario per arrestare un sistema usando una richiesta di rete. Diritto utente: forzare l'arresto da un sistema remoto. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SeUndockPrivilege               | Obbligatorio per disinserire un portatile. Diritto utente: rimuovere il computer dall'alloggiamento di espansione. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeSyncAgentPrivilege            | Obbligatorio per l'uso dei servizi di sincronizzazione della directory LDAP da parte di un controller di dominio. Questo privilegio consente al titolare di leggere tutti gli oggetti e le proprietà nella directory, indipendentemente dalla protezione per gli oggetti e le proprietà. Per impostazione predefinita, viene assegnato agli account Administrator e LocalSystem nei controller di dominio. Diritto utente: sincronizzare i dati del servizio directory. <br/>                                                                                                                                                                                                                                                                                |
| SeEnableDelegationPrivilege     | Obbligatorio per contrassegnare gli account utente e computer come attendibili per la delega. Diritto utente: abilitare gli account computer e utente come attendibili per la delega. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeManageVolumePrivilege         | Obbligatorio per abilitare i privilegi di gestione dei volumi. Diritto utente: gestire i file in un volume. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeImpersonatePrivilege          | Obbligatorio per la rappresentazione. Diritto utente: rappresenta un client dopo l'autenticazione. Windows XP/2000: questo privilegio non è supportato. <br/> Si noti che questo valore è supportato a partire da Windows Server 2003, Windows XP con SP2 e Windows 2000 con SP4.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateGlobalPrivilege         | Obbligatorio per creare oggetti di mapping di file denominati nello spazio dei nomi globale durante le sessioni di Servizi terminal. Questo privilegio è abilitato per impostazione predefinita per gli amministratori, i servizi e l'account di sistema locale. Diritto utente: creare oggetti globali. Windows XP/2000: questo privilegio non è supportato. <br/> Si noti che questo valore è supportato a partire da Windows Server 2003, Windows XP con SP2 e Windows 2000 con SP4.<br/>                                                                                                                                                                                                                                        |
| SeTrustedCredManAccessPrivilege | Obbligatorio per accedere Gestione credenziali come chiamante attendibile. Diritto utente: accesso Gestione credenziali come chiamante attendibile. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeRelabelPrivilege              | Obbligatorio per modificare il livello di integrità obbligatorio di un oggetto. Diritto utente: modificare l'etichetta di un oggetto. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseWorkingSetPrivilege   | Necessario per allocare più memoria per le applicazioni eseguite nel contesto degli utenti. Diritto utente: aumentare un processo working set. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| SeTimeZonePrivilege             | Obbligatorio per modificare il fuso orario associato all'orologio interno del computer. Diritto utente: modificare il fuso orario. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateSymbolicLinkPrivilege   | Obbligatorio per creare un collegamento simbolico. Diritto utente: creare collegamenti simbolici. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



 

 





