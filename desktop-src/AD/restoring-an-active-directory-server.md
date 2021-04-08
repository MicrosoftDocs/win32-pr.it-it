---
title: Ripristino di un server di Active Directory
description: I server di Active Directory devono essere ripristinati offline.
ms.assetid: 91fbbdc1-0e84-4b89-8a38-4c8d0268992b
ms.tgt_platform: multiple
keywords:
- Ripristino di Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273d02fd50d6b3bd68a055a6a783566e4ebddcf7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872254"
---
# <a name="restoring-an-active-directory-server"></a>Ripristino di un server di Active Directory

I server di Active Directory devono essere ripristinati offline. Il sistema deve essere riavviato in modalità ripristino servizi directory. In questa modalità, il sistema operativo è in esecuzione senza Active Directory Domain Services e tutte le convalide degli utenti avvengono tramite Gestione account di sicurezza (SAM) nel registro di sistema. Per ripristinare Active Directory Domain Services, utilizzare le credenziali di un amministratore locale nel controller di dominio ripristinato.

Il chiamante delle funzioni di ripristino deve disporre del privilegio di accesso **se \_ Restore \_ Name** . Utilizzare la funzione [**DsSetAuthIdentity**](dssetauthidentity.md) per impostare il contesto di sicurezza in cui vengono chiamate le funzioni di backup e ripristino della directory.

Tenere presente che quando si esegue il ripristino di Active Directory Domain Services, è necessario ripristinare anche gli altri componenti dello stato del sistema.

**Per ripristinare Active Directory Domain Services**

1.  Chiamare la funzione [**DsIsNTDSOnline**](dsisntdsonline.md) per determinare se Active Directory Domain Services sono in esecuzione.
2.  Se Active Directory Domain Services non sono in esecuzione, viene chiamata la funzione [**DsRestorePrepare**](dsrestoreprepare.md) per inizializzare l'operazione di ripristino e ottenere un handle del contesto di backup. Se Active Directory Domain Services è in esecuzione, non può essere ripristinato e l'applicazione di ripristino deve avere esito negativo per l'operazione di ripristino. La funzione **DsRestorePrepare** richiede che il token di scadenza venga ottenuto dalla funzione [**DsBackupPrepare**](dsbackupprepare.md) durante l'operazione di backup.
3.  Chiamare la funzione [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) per determinare le directory in cui devono essere ripristinati i file. Se questa funzione ha esito negativo, ripristinare i dati nella directory di origine del backup originale; ovvero la directory da cui è stato eseguito il backup dei dati.
4.  Chiamare la funzione [**DsRestoreRegister**](dsrestoreregister.md) per preparare il server Active Directory per l'operazione di ripristino e bloccare le directory di ripristino.
5.  Per ripristinare i file, utilizzare le funzioni Win32 standard. Prima di tutto, eliminare tutti i file nella directory di destinazione; Copiare quindi i file di backup nella directory di destinazione.
6.  Chiamare la funzione [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) per indicare che il ripristino è stato completato.
7.  Chiamare la funzione [**DsRestoreEnd**](dsrestoreend.md) per rilasciare tutte le risorse associate al contesto.

Dopo un ripristino in modalità ripristino servizi directory, il controller di dominio deve essere riavviato in modalità normale. All'avvio del servizio directory, il controller di dominio eseguirà la normale verifica della coerenza e la directory ripristinata sarà in linea.

Tenere presente che il ripristino di un server Active Directory è sempre un'operazione in due parti. Per prima cosa, ripristinare il database fino a un momento in cui è stato effettuato il backup. In secondo luogo, replicare la directory, in cui la DSA appena ripristinata replica gli aggiornamenti post-backup da altri DSA nella foresta del dominio e dell'azienda.

Un computer che esegue Windows 2000 o Windows Server 2003, che contiene una replica del servizio directory, è un controller di dominio.

La funzione [**DsRestoreRegister**](dsrestoreregister.md) aggiunge dati al registro di sistema che devono rimanere inattivi nel processo di ripristino del registro di sistema affinché il ripristino funzioni correttamente. Per garantire la conservazione dei dati del registro di sistema, ripristinare Active Directory Domain Services con le funzioni **Impossibile \*** prima di riavviare il computer dopo la chiamata della funzione [**RegReplaceKey**](/windows/desktop/api/winreg/nf-winreg-regreplacekeya) . Questo processo funziona perché **RegReplaceKey** non sostituisce effettivamente l'hive del registro di sistema finché il computer non viene riavviato e i dati del registro di sistema aggiunti dalla funzione **DsRestoreRegister** sono esclusi in modo specifico dalla sostituzione durante un'operazione di ripristino del registro di sistema.

 

 