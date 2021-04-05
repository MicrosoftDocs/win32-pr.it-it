---
description: Un archivio di sistema è una raccolta costituita da uno o più archivi di pari livello fisici.
ms.assetid: 41fe9366-4c17-43bb-91d6-934c7aa87a2d
title: Percorsi di archivio di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0863ffde8be5db67459908b1ec26ec73da029744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967619"
---
# <a name="system-store-locations"></a>Percorsi di archivio di sistema

Un archivio di sistema è una raccolta costituita da uno o più archivi di pari livello fisici. Per ogni archivio di sistema sono presenti archivi di pari livello fisici predefiniti. Dopo l'apertura di un archivio di sistema come MY at CERT \_ System \_ Store \_ Current \_ User, il provider dell'archivio chiama [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) per aprire tutti gli archivi fisici nella raccolta di archivi di sistema. Nel processo aperto ognuno di questi archivi fisici viene aggiunto alla raccolta di archivi di sistema tramite [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection). Tutti i certificati in tali archivi fisici sono disponibili tramite la raccolta di archivi di sistema logici.

Per ogni percorso di archivio di sistema, gli archivi di sistemi predefiniti sono:

-   MY
-   Radice
-   Trust
-   CA

Nell' \_ \_ \_ utente corrente dell'archivio CERT System \_ è presente anche un archivio UserDS predefinito. Un archivio di smart card è pianificato per questo percorso.

Ecco gli archivi di sistema seguiti da ulteriori osservazioni:

-   [\_ \_ \_ utente corrente archivio certificati di sistema \_](#cert_system_store_current_user)
-   [\_ \_ \_ computer locale archivio certificati di sistema \_](#cert_system_store_local_machine)
-   [\_ \_ \_ servizio corrente archivio certificati di sistema \_](#cert_system_store_current_service)
-   [\_servizi di \_ Archivio di sistema CERT \_](#cert_system_store_services)
-   [\_utenti di \_ Archivio di sistema CERT \_](#cert_system_store_users)
-   [\_criteri di \_ \_ gruppo dell'utente corrente \_ del \_ sistema CERT](#cert_system_current_user_group_policy)
-   [\_criteri di \_ \_ gruppo del computer locale \_ di sistema CERT \_](#cert_system_local_machine_group_policy)
-   [\_Archivio di sistema CERT \_ \_ \_ computer locale \_ Enterprise](#cert_system_store_local_machine_enterprise)
-   [Osservazioni:](#remarks)

### <a name="cert_system_store_current_user"></a>\_ \_ \_ utente corrente archivio certificati di sistema \_

\_ \_ \_ \_ Gli archivi di sistema degli utenti correnti del sistema di certificati si trovano nel seguente percorso del registro di sistema:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         SystemCertificates
```

Gli archivi fisici predefiniti associati a tali archivi di sistema sono i seguenti.



| Archivio di sistema | Archivio fisico                                           |
|--------------|----------------------------------------------------------|
| MY           | . Predefinita                                                 |
| Radice         | . Default. LocalMachine<br/> . Smart Card<br/>   |
| Trust        | . Default. GroupPolicy<br/> . LocalMachine<br/> |
| CA           | . Default. GroupPolicy<br/> . LocalMachine<br/> |
| UserDS       | . UserCertificate                                         |



 

### <a name="cert_system_store_local_machine"></a>\_ \_ \_ computer locale archivio certificati di sistema \_

\_ \_ \_ \_ Gli archivi di sistema del computer locale dell'archivio del sistema CERT si trovano nel seguente percorso del registro di sistema:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         SystemCertificates
```

Gli archivi fisici predefiniti sono associati a tali archivi di sistema, come indicato di seguito.



| Archivio di sistema | Archivio fisico                                                                                    |
|--------------|---------------------------------------------------------------------------------------------------|
| MY           | . Predefinita                                                                                          |
| Radice         | . Default. AuthRoot<br/> . GroupPolicy<br/> . Enterprise<br/> . Smart Card<br/> |
| Trust        | . Default. GroupPolicy<br/> . Enterprise<br/>                                            |
| CA           | . Default. GroupPolicy<br/> . Enterprise <br/>                                           |



 

### <a name="cert_system_store_current_service"></a>\_ \_ \_ servizio corrente archivio certificati di sistema \_

\_ \_ \_ \_ Gli archivi del sistema del servizio di archiviazione del sistema CERT correnti si trovano nel seguente percorso del registro di sistema:

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
| MY           | . Predefinita                         |
| Radice         | . Default. LocalMachine<br/> |
| Trust        | . Default. LocalMachine<br/> |
| CA           | . Default. LocalMachine<br/> |



 

### <a name="cert_system_store_services"></a>\_servizi di \_ Archivio di sistema CERT \_

\_ \_ \_ Gli archivi di sistema di CERT System Store Services si trovano nel seguente percorso del registro di sistema:

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
| ServiceName \\ My    | . Predefinita                         |
| Radice ServiceName \\  | . Default. LocalMachine<br/> |
| Trust di ServiceName \\ | . Default. LocalMachine<br/> |
| CA ServiceName \\    | . Default. LocalMachine<br/> |



 

### <a name="cert_system_store_users"></a>\_utenti di \_ Archivio di sistema CERT \_

\_ \_ \_ Gli archivi di sistema CERT System Store Users si trovano nel seguente percorso del registro di sistema:

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
| ID \\ utente    | . Default. LocalMachine<br/> |
| \\radice UserID  | . Default. LocalMachine<br/> |
| \\attendibilità UserID | . Default. LocalMachine<br/> |
| \\CA UserID    | . Default. LocalMachine<br/> |



 

### <a name="cert_system_current_user_group_policy"></a>\_criteri di \_ \_ gruppo dell'utente corrente \_ del \_ sistema CERT

\_ \_ \_ \_ \_ Gli archivi di sistema di criteri di gruppo dell'utente corrente del sistema CERT sono nel seguente percorso del registro di sistema:

```
HKEY_CURRENT_USER
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_local_machine_group_policy"></a>\_criteri di \_ \_ gruppo del computer locale \_ di sistema CERT \_

\_ \_ \_ \_ \_ Gli archivi di sistema di criteri di gruppo del computer locale di sistema CERT sono nel seguente percorso del registro di sistema:

```
HKEY_LOCAL_MACHINE
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_store_local_machine_enterprise"></a>\_Archivio di sistema CERT \_ \_ \_ computer locale \_ Enterprise

Il \_ \_ computer locale dell'archivio del sistema CERT \_ contiene i \_ \_ certificati condivisi tra domini nell'azienda e scaricati dalla directory globale dell'organizzazione. Per sincronizzare l'archivio aziendale del client, viene eseguito il polling della directory aziendale ogni otto ore e i certificati vengono scaricati automaticamente in background.

Gli archivi fisici predefiniti associati a questi archivi di sistema sono i seguenti.



| Archivio di sistema | Archivio fisico |
|--------------|----------------|
| MY           | . Predefinita       |
| Radice         | . Predefinita       |
| Trust        | . Predefinita       |
| CA           | . Predefinita       |



 

### <a name="remarks"></a>Commenti

Gli archivi fisici aggiuntivi possono essere associati a un archivio di sistema tramite [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).

Gli \_ archivi CERT System \_ Store \_ Service e CERT \_ System \_ Store \_ Users vengono aperti anteponendo il nome dell'archivio nella stringa passata a *pvPara* con il nome del servizio o dell'utente, ad esempio *ServiceName* \\ **trust** o **. Predefinito** \\ **My**. Il percorso CERT System \_ \_ Store \_ Services o CERT \_ System \_ Store \_ Users può aprire lo stesso archivio in cert \_ System \_ Current \_ Service o CERT \_ System \_ Store \_ utente corrente \_ usando l'ID di [*sicurezza*](../secgloss/s-gly.md) testuale (SID) del servizio o dell'utente corrente.

Gli archivi nei criteri di \_ \_ \_ gruppo dell'utente dell'archivio di sistema CERT \_ \_ e \_ dei criteri di gruppo del computer \_ locale del sistema CERT \_ \_ \_ in un'impostazione di rete vengono scaricati nel computer client dal modello di criteri di gruppo (GPT) durante l'avvio del computer o l'accesso dell'utente. Questi archivi possono essere aggiornati nel computer client dopo l'avvio o l'accesso quando il GPT viene modificato nel server di dominio da un amministratore. La funzione [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) consente a un'applicazione di ricevere una notifica quando vengono modificati i negozi in una di queste posizioni.

È possibile aprire in remoto i percorsi di archivio di sistema seguenti:

-   \_ \_ \_ computer locale archivio certificati di sistema \_
-   \_criteri di \_ \_ gruppo del \_ computer \_ locale \_ dell'archivio di sistema CERT
-   \_servizi di \_ Archivio di sistema CERT \_
-   \_utenti di \_ Archivio di sistema CERT \_

I percorsi dell'archivio di sistema vengono aperti in modalità remota anteponendo il nome dell'archivio nella stringa passata a *pvPara* con il nome del computer. Esempi di nomi di archivio di sistema remoto sono:

-   *Nomecomputer* \\ **CA**
-   \\\\*Nomecomputer* \\ **CA**
-   *Nomecomputer* \\ *ServiceName* \\ **Attendibilità**
-   \\\\*Nomecomputer* \\ *ServiceName* \\ **Attendibilità**

 

 
