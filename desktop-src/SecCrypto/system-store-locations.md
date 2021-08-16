---
description: Un archivio di sistema è una raccolta costituita da uno o più archivi fisici di pari livello.
ms.assetid: 41fe9366-4c17-43bb-91d6-934c7aa87a2d
title: Percorsi dell'archivio di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d793d94bcb1c58bcc0d8c046b038df7e699d287b9ede3f14d6e2cb3c94ab781e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897433"
---
# <a name="system-store-locations"></a>Percorsi dell'archivio di sistema

Un archivio di sistema è una raccolta costituita da uno o più archivi fisici di pari livello. Per ogni archivio di sistema sono presenti archivi di pari livello fisici predefiniti. Dopo aver aperto un archivio di sistema come MY in CERT SYSTEM STORE CURRENT USER, il provider dell'archivio chiama \_ \_ \_ \_ [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) per aprire ognuno degli archivi fisici nella raccolta dell'archivio di sistema. Nel processo aperto, ognuno di questi archivi fisici viene aggiunto alla raccolta di archivi di sistema [**usando CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection). Tutti i certificati in tali archivi fisici sono disponibili tramite la raccolta dell'archivio di sistema logico.

Per ogni percorso dell'archivio di sistema, gli archivi di sistemi predefiniti sono:

-   MY
-   Radice
-   Attendibilità
-   CA

In CERT SYSTEM STORE CURRENT USER è presente anche un \_ \_ archivio \_ \_ UserDS predefinito. Per questa smart card è previsto un archivio di archiviazione.

Ecco gli archivi di sistema seguiti da altre osservazioni:

-   [UTENTE \_ CORRENTE \_ DELL'ARCHIVIO \_ DI \_ SISTEMA CERT](#cert_system_store_current_user)
-   [COMPUTER \_ LOCALE \_ DELL'ARCHIVIO DI \_ SISTEMA \_ CERT](#cert_system_store_local_machine)
-   [SERVIZIO CORRENTE \_ \_ DELL'ARCHIVIO DI \_ SISTEMA \_ CERT](#cert_system_store_current_service)
-   [CERT \_ SYSTEM \_ STORE \_ SERVICES](#cert_system_store_services)
-   [UTENTI \_ DELL'ARCHIVIO \_ DI SISTEMA CERT \_](#cert_system_store_users)
-   [CRITERI DI \_ GRUPPO UTENTE CORRENTI DEL SISTEMA \_ \_ \_ \_ CERT](#cert_system_current_user_group_policy)
-   [CRITERI DI \_ GRUPPO DEL COMPUTER LOCALE DEL \_ \_ \_ SISTEMA \_ CERT](#cert_system_local_machine_group_policy)
-   [CERT \_ SYSTEM \_ STORE \_ LOCAL \_ MACHINE \_ ENTERPRISE](#cert_system_store_local_machine_enterprise)
-   [Osservazioni:](#remarks)

### <a name="cert_system_store_current_user"></a>UTENTE \_ CORRENTE \_ DELL'ARCHIVIO \_ DI \_ SISTEMA CERT

Gli archivi di sistema CERT \_ SYSTEM STORE CURRENT USER sono nel percorso del Registro di sistema \_ \_ \_ seguente:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         SystemCertificates
```

Gli archivi fisici predefiniti associati a tali archivi di sistema sono i seguenti.



| Archivio di sistema | Archivio fisico                                           |
|--------------|----------------------------------------------------------|
| MY           | . Predefinito                                                 |
| Radice         | . Default.LocalMachine<br/> . Smartcard<br/>   |
| Attendibilità        | . Default.GroupPolicy<br/> . Localmachine<br/> |
| CA           | . Default.GroupPolicy<br/> . Localmachine<br/> |
| UserDS       | . Usercertificate                                         |



 

### <a name="cert_system_store_local_machine"></a>COMPUTER \_ LOCALE \_ DELL'ARCHIVIO DI \_ SISTEMA \_ CERT

Gli archivi di sistema CERT \_ SYSTEM STORE LOCAL MACHINE sono nel percorso del Registro di sistema \_ \_ \_ seguente:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         SystemCertificates
```

Gli archivi fisici predefiniti sono associati a tali archivi di sistema come indicato di seguito.



| Archivio di sistema | Archivio fisico                                                                                    |
|--------------|---------------------------------------------------------------------------------------------------|
| MY           | . Predefinito                                                                                          |
| Radice         | . Default.AuthRoot<br/> . Criteri di gruppo<br/> . Enterprise<br/> . Smartcard<br/> |
| Attendibilità        | . Default.GroupPolicy<br/> . Enterprise<br/>                                            |
| CA           | . Default.GroupPolicy<br/> . Enterprise <br/>                                           |



 

### <a name="cert_system_store_current_service"></a>SERVIZIO CORRENTE \_ \_ DELL'ARCHIVIO DI \_ SISTEMA \_ CERT

Gli archivi di sistema CERT \_ SYSTEM STORE CURRENT SERVICE sono nel percorso del Registro di sistema \_ \_ \_ seguente:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

Gli archivi fisici predefiniti associati a tali archivi di sistema sono i seguenti.



| Archivio di sistema | Archivio fisico                   |
|--------------|----------------------------------|
| MY           | . Predefinito                         |
| Radice         | . Default.LocalMachine<br/> |
| Attendibilità        | . Default.LocalMachine<br/> |
| CA           | . Default.LocalMachine<br/> |



 

### <a name="cert_system_store_services"></a>CERT \_ SYSTEM \_ STORE \_ SERVICES

Gli archivi di sistema CERT \_ SYSTEM STORE SERVICES sono nel percorso del Registro di sistema \_ \_ seguente:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

Gli archivi fisici predefiniti associati a tali archivi di sistema sono i seguenti.



| Archivio di sistema       | Archivio fisico                   |
|--------------------|----------------------------------|
| ServiceName \\ MY    | . Predefinito                         |
| Radice di \\ ServiceName  | . Default.LocalMachine<br/> |
| Attendibilità di \\ ServiceName | . Default.LocalMachine<br/> |
| ServiceName \\ CA    | . Default.LocalMachine<br/> |



 

### <a name="cert_system_store_users"></a>UTENTI \_ DELL'ARCHIVIO \_ DI SISTEMA CERT \_

Gli archivi di sistema CERT \_ SYSTEM STORE USERS sono nel percorso del Registro di sistema \_ \_ seguente:

```
HKEY_USERS
   UserName
      Software
         Microsoft
            SystemCertificates
```

Gli archivi fisici predefiniti associati a tali archivi di sistema sono i seguenti.



| Archivio di sistema  | Archivio fisico                   |
|---------------|----------------------------------|
| userid \\ MY    | . Default.LocalMachine<br/> |
| Userid \\ Root  | . Default.LocalMachine<br/> |
| userid \\ Trust | . Default.LocalMachine<br/> |
| USERID \\ CA    | . Default.LocalMachine<br/> |



 

### <a name="cert_system_current_user_group_policy"></a>CRITERI DI \_ GRUPPO UTENTE CORRENTI DEL SISTEMA \_ \_ \_ \_ CERT

Gli archivi di sistema CERT \_ SYSTEM CURRENT USER GROUP POLICY sono disponibili nel percorso del Registro di sistema \_ \_ \_ \_ seguente:

```
HKEY_CURRENT_USER
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_local_machine_group_policy"></a>CRITERI DI \_ GRUPPO DEL COMPUTER LOCALE DEL \_ \_ \_ SISTEMA \_ CERT

Gli archivi di sistema CERT \_ SYSTEM LOCAL MACHINE GROUP POLICY sono nel percorso del Registro di sistema \_ \_ \_ \_ seguente:

```
HKEY_LOCAL_MACHINE
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_store_local_machine_enterprise"></a>CERT \_ SYSTEM \_ STORE \_ LOCAL \_ MACHINE \_ ENTERPRISE

CERT SYSTEM STORE LOCAL MACHINE ENTERPRISE contiene certificati condivisi tra domini \_ \_ \_ \_ \_ dell'organizzazione e scaricati dalla directory aziendale globale. Per sincronizzare l'archivio aziendale del client, viene eseguito il polling della directory aziendale ogni otto ore e i certificati vengono scaricati automaticamente in background.

Gli archivi fisici predefiniti associati a questi archivi di sistema sono i seguenti.



| Archivio di sistema | Archivio fisico |
|--------------|----------------|
| MY           | . Predefinito       |
| Radice         | . Predefinito       |
| Attendibilità        | . Predefinito       |
| CA           | . Predefinito       |



 

### <a name="remarks"></a>Commenti

È possibile associare archivi fisici aggiuntivi a un archivio di sistema [**usando CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).

Gli archivi CERT SYSTEM STORE SERVICE e CERT SYSTEM STORE USERS vengono aperti antendo il nome dell'archivio nella stringa passata a \_ \_ \_ \_ \_ \_ *pvPara*  \\  **con il nome del servizio o dell'utente, ad esempio ServiceName Trust o . Impostazione** \\ **predefinita MY**. Il percorso CERT SYSTEM STORE SERVICES o CERT SYSTEM STORE USERS può aprire lo stesso archivio in CERT SYSTEM CURRENT SERVICE o CERT SYSTEM STORE CURRENT USER usando l'ID di sicurezza \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ testuale (SID) [](../secgloss/s-gly.md) del servizio o dell'utente corrente.

I criteri di gruppo CERT SYSTEM STORE USER GROUP POLICY e CERT SYSTEM LOCAL MACHINE GROUP POLICY in un'impostazione di rete vengono scaricati nel computer client dal modello \_ \_ Criteri di gruppo \_ \_ \_ \_ \_ \_ \_ \_ (GPT) durante l'avvio del computer o l'accesso utente. Questi archivi possono essere aggiornati nel computer client dopo l'avvio o l'accesso quando gpT viene modificato nel server di dominio da un amministratore. La [**funzione CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) consente a un'applicazione di ricevere una notifica quando gli archivi in una di queste posizioni sono stati modificati.

I percorsi dell'archivio di sistema seguenti possono essere aperti in modalità remota:

-   COMPUTER \_ LOCALE \_ DELL'ARCHIVIO DI \_ SISTEMA \_ CERT
-   CRITERI DI \_ GRUPPO CERT SYSTEM \_ STORE LOCAL \_ \_ MACHINE \_ \_
-   CERT \_ SYSTEM \_ STORE \_ SERVICES
-   UTENTI \_ DELL'ARCHIVIO \_ DI SISTEMA CERT \_

I percorsi dell'archivio di sistema vengono aperti in modalità remota antefissendo il nome dell'archivio nella stringa passata a *pvPara* con il nome del computer. Di seguito sono riportati alcuni esempi di nomi di archivi di sistema remoti:

-   *NomeComputer* \\ **CA**
-   \\\\*NomeComputer* \\ **CA**
-   *NomeComputer* \\ *ServiceName* \\ **Attendibilità**
-   \\\\*NomeComputer* \\ *ServiceName* \\ **Attendibilità**

 

 
