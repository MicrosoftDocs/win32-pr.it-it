---
title: Tipo semplice privilegeType
description: I privilegi determinano il tipo di operazioni di sistema che un account utente può eseguire. Un amministratore assegna privilegi agli account utente e di gruppo. I privilegi di ogni utente includono quelli concessi all'utente e ai gruppi a cui appartiene l'utente.
ms.assetid: 813b0886-ca76-4523-a1e6-42ca656851a7
keywords:
- Utilità di pianificazione di tipo semplice privilegeType
topic_type:
- apiref
api_name:
- privilegeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4864364a4752d72bd5305c5c2591b7d27391517f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301238"
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

Il tipo semplice **privilegeType** definisce i valori seguenti.



| Valore                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SeCreateTokenPrivilege          | Necessario per creare un token primario. Diritto utente: creare un oggetto token.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeAssignPrimaryTokenPrivilege   | Obbligatorio per assegnare il token primario di un processo. Diritto utente: sostituire un token a livello di processo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeLockMemoryPrivilege           | Obbligatorio per bloccare le pagine fisiche in memoria. Diritto utente: blocco di pagine in memoria. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| SeIncreaseQuotaPrivilege        | Obbligatorio per aumentare la quota assegnata a un processo. Diritto utente: modificare le quote di memoria per un processo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeUnsolicitedInputPrivilege     | Obbligatorio per leggere l'input non richiesto da un dispositivo terminal. Diritto utente: non applicabile. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SeMachineAccountPrivilege       | Necessario per creare un account computer. Diritto utente: aggiungere le workstation al dominio. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeTcbPrivilege                  | Questo privilegio identifica il proprio titolare come parte della base del computer attendibile. A alcuni sottosistemi protetti attendibili viene concesso questo privilegio. Diritto utente: agire come parte del sistema operativo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| SeSecurityPrivilege             | Obbligatorio per eseguire numerose funzioni correlate alla sicurezza, ad esempio il controllo e la visualizzazione dei messaggi di controllo. Questo privilegio identifica il proprio titolare come operatore di sicurezza. Diritto utente: gestire il controllo e il registro di sicurezza. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeTakeOwnershipPrivilege        | Obbligatorio per assumere la proprietà di un oggetto senza che venga concesso l'accesso discrezionale. Questo privilegio consente l'impostazione del valore proprietario solo per i valori che il titolare può assegnare legittimamente come proprietario di un oggetto. Diritto utente: assumere la proprietà di file o di altri oggetti. <br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| SeLoadDriverPrivilege           | Necessario per caricare o scaricare un driver di dispositivo. Diritto utente: caricare e scaricare i driver di dispositivo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemProfilePrivilege        | Obbligatorio per raccogliere le informazioni di profilatura per l'intero sistema. Diritto utente: profilare le prestazioni del sistema. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeSystemtimePrivilege           | Obbligatorio per modificare l'ora di sistema. Diritto utente: modificare l'ora di sistema. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeProfileSingleProcessPrivilege | Obbligatorio per raccogliere le informazioni di profilatura per un singolo processo. Diritto utente: profilo singolo processo. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseBasePriorityPrivilege | Obbligatorio per aumentare la priorità di base di un processo. Diritto utente: aumento della priorità di pianificazione. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeCreatePagefilePrivilege       | Obbligatorio per creare un file di paging. Diritto utente: creare un pagefile. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| SeCreatePermanentPrivilege      | Obbligatorio per creare un oggetto permanente. Diritto utente: creare oggetti condivisi permanenti. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| SeBackupPrivilege               | Obbligatorio per eseguire operazioni di backup. Questo privilegio fa in modo che il sistema conceda tutto il controllo di accesso in lettura a qualsiasi file, indipendentemente dall'elenco di controllo di accesso (ACL) specificato per il file. Qualsiasi richiesta di accesso diversa da Read viene comunque valutata con l'ACL. Questo privilegio è richiesto da RegSaveKey e RegSaveKeyExfunctions. Se questo privilegio viene mantenuto, vengono concessi i seguenti diritti di accesso: \_ controllo lettura, accesso \_ sicurezza del sistema \_ , file \_ lettura generica \_ , \_ attraversamento file. Diritto utente: backup di file e directory. <br/>                                                                                                                                     |
| SeRestorePrivilege              | Obbligatorio per eseguire operazioni di ripristino. Questo privilegio fa in modo che il sistema conceda tutti i controlli di accesso in scrittura a qualsiasi file, indipendentemente dall'ACL specificato per il file. Qualsiasi richiesta di accesso diversa da Write viene comunque valutata con l'ACL. Questo privilegio consente inoltre di impostare qualsiasi ID di sicurezza (SID) dell'utente o del gruppo valido come proprietario di un file. Questo privilegio è richiesto dalla funzione RegLoadKey. Se questo privilegio viene mantenuto, vengono concessi i seguenti diritti di accesso: scrittura \_ DAC, scrivi \_ proprietario, accesso \_ \_ sicurezza sistema, file \_ scrittura generica \_ , file \_ Aggiungi \_ file, \_ Aggiungi \_ sottodirectory file, Elimina. Diritto utente: ripristino di file e directory. <br/> |
| SeShutdownPrivilege             | Necessario per arrestare un sistema locale. Diritto utente: arrestare il sistema. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SeDebugPrivilege                | Necessario per eseguire il debug e la modifica della memoria di un processo di proprietà di un altro account. Diritto utente: debug di programmi. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeAuditPrivilege                | Obbligatorio per generare le voci del log di controllo. Assegnare questo privilegio ai server protetti. Diritto utente: genera controlli di sicurezza. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| SeSystemEnvironmentPrivilege    | Obbligatorio per modificare la RAM non volatile dei sistemi che usano questo tipo di memoria per archiviare le informazioni di configurazione. Diritto utente: modificare i valori dell'ambiente del firmware. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeChangeNotifyPrivilege         | Necessaria per ricevere notifiche delle modifiche apportate ai file o alle directory. Questo privilegio fa anche in modo che il sistema ignori tutti i controlli di accesso attraversati. È abilitata per impostazione predefinita per tutti gli utenti. Right utente: ignorare il controllo incrociato. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeRemoteShutdownPrivilege       | Necessario per arrestare un sistema utilizzando una richiesta di rete. Diritto utente: forza l'arresto da un sistema remoto. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| SeUndockPrivilege               | Obbligatorio per disancorare un portatile. Diritto utente: rimuovere il computer dalla stazione di ancoraggio. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| SeSyncAgentPrivilege            | Obbligatorio per l'utilizzo dei servizi di sincronizzazione delle directory LDAP da parte di un controller di dominio. Questo privilegio consente al titolare di leggere tutti gli oggetti e le proprietà nella directory, indipendentemente dalla protezione per gli oggetti e le proprietà. Per impostazione predefinita, viene assegnato agli account Administrator e LocalSystem nei controller di dominio. Diritto utente: sincronizzare i dati del servizio directory. <br/>                                                                                                                                                                                                                                                                                |
| SeEnableDelegationPrivilege     | Obbligatorio per contrassegnare gli account utente e computer come trusted per la delega. Diritto utente: consentire l'attendibilità degli account computer e utente per la delega. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeManageVolumePrivilege         | Necessario per abilitare i privilegi di gestione del volume. Diritto utente: gestire i file in un volume. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| SeImpersonatePrivilege          | Obbligatorio per la rappresentazione. Diritto utente: rappresenta un client dopo l'autenticazione. Windows XP/2000: questo privilegio non è supportato. <br/> Si noti che questo valore è supportato a partire da Windows Server 2003, Windows XP con SP2 e Windows 2000 con SP4.<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateGlobalPrivilege         | Obbligatorio per creare oggetti mapping di file denominati nello spazio dei nomi globale durante le sessioni di Servizi terminal. Questo privilegio è abilitato per impostazione predefinita per gli amministratori, i servizi e l'account di sistema locale. Diritto utente: creare oggetti globali. Windows XP/2000: questo privilegio non è supportato. <br/> Si noti che questo valore è supportato a partire da Windows Server 2003, Windows XP con SP2 e Windows 2000 con SP4.<br/>                                                                                                                                                                                                                                        |
| SeTrustedCredManAccessPrivilege | Obbligatorio per accedere a gestione credenziali come chiamante attendibile. Diritto utente: accedere a gestione credenziali come chiamante attendibile. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| SeRelabelPrivilege              | Obbligatorio per modificare il livello di integrità obbligatorio di un oggetto. Diritto utente: modificare l'etichetta di un oggetto. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| SeIncreaseWorkingSetPrivilege   | Obbligatorio per allocare ulteriore memoria per le applicazioni eseguite nel contesto degli utenti. Diritto utente: aumentare un processo working set. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| SeTimeZonePrivilege             | Obbligatorio per modificare il fuso orario associato al clock interno del computer. Diritto utente: modificare il fuso orario. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| SeCreateSymbolicLinkPrivilege   | Obbligatorio per creare un collegamento simbolico. Diritto utente: creare collegamenti simbolici. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



 

 





