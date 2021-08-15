---
title: Ripristino di un server Active Directory
description: I server Active Directory devono essere ripristinati offline.
ms.assetid: 91fbbdc1-0e84-4b89-8a38-4c8d0268992b
ms.tgt_platform: multiple
keywords:
- Ripristino di Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 865389b4ad80ad8c3009a86a881ff4cf291a4fc1b4606e78e8ecd01ceef7c893
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184294"
---
# <a name="restoring-an-active-directory-server"></a>Ripristino di un server Active Directory

I server Active Directory devono essere ripristinati offline. Il sistema deve essere riavviato in modalità ripristino servizi directory. In questa modalità, il sistema operativo viene eseguito senza Active Directory Domain Services e tutte le convalide degli utenti vengono eseguite tramite Gestione account di sicurezza (SAM) nel Registro di sistema. Per ripristinare Active Directory Domain Services, usare le credenziali di un amministratore locale nel controller di dominio ripristinato.

Il chiamante delle funzioni di ripristino deve avere il **edizione Standard di accesso RESTORE \_ \_ NAME.** Usare la [**funzione DsSetAuthIdentity**](dssetauthidentity.md) per impostare il contesto di sicurezza in cui vengono chiamate le funzioni di backup e ripristino della directory.

Tenere presente che quando si ripristina un Active Directory Domain Services, è necessario ripristinare anche gli altri componenti dello stato del sistema.

**Per ripristinare Active Directory Domain Services**

1.  Chiamare la [**funzione DsIsNTDSOnline**](dsisntdsonline.md) per determinare se Active Directory Domain Services sono in esecuzione.
2.  Se Active Directory Domain Services non sono in esecuzione, viene chiamata [**la funzione DsRestorePrepare**](dsrestoreprepare.md) per inizializzare l'operazione di ripristino e ottenere un handle del contesto di backup. Se Active Directory Domain Services in esecuzione, non può essere ripristinato e l'applicazione di ripristino deve non riuscire l'operazione di ripristino. La **funzione DsRestorePrepare** richiede che il token di scadenza sia ottenuto dalla [**funzione DsBackupPrepare**](dsbackupprepare.md) durante l'operazione di backup.
3.  Chiamare la [**funzione DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) per determinare le directory in cui devono essere ripristinati i file. Se questa funzione ha esito negativo, ripristinare i dati nella directory di origine del backup originale. ovvero la directory da cui è stato eseguito il backup dei dati.
4.  Chiamare la [**funzione DsRestoreRegister**](dsrestoreregister.md) per preparare il server Active Directory per l'operazione di ripristino e bloccare le directory di ripristino.
5.  Usare le funzioni Win32 standard per ripristinare i file. Eliminare prima di tutto tutti i file nella directory di destinazione. quindi copiare i file di backup nella directory di destinazione.
6.  Chiamare la [**funzione DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) per indicare che il ripristino è stato completato.
7.  Chiamare la [**funzione DsRestoreEnd**](dsrestoreend.md) per rilasciare tutte le risorse associate al contesto.

Dopo un ripristino in modalità ripristino servizi directory, il controller di dominio deve essere riavviato in modalità normale. All'avvio del servizio directory, il controller di dominio eseguirà la normale verifica coerenza e la directory ripristinata sarà online.

Tenere presente che il ripristino di un server Active Directory è sempre un'operazione in due parti. Ripristinare prima di tutto il database a un'ora in cui è stato eseguito il backup. In secondo luogo, replicare la directory , in cui l'account DSA appena ripristinato replica gli aggiornamenti post-backup da altri DSA nel dominio e nella foresta aziendale.

Un computer che esegue Windows 2000 o Windows Server 2003, che contiene una replica del servizio directory, è un controller di dominio.

La [**funzione DsRestoreRegister**](dsrestoreregister.md) aggiunge al Registro di sistema dati che devono superare il processo di ripristino del Registro di sistema per il corretto funzionamento del ripristino. Per assicurarsi che i dati del Registro di sistema siano mantenuti, ripristinare Active Directory Domain Services con le funzioni **DsRestore \** _ prima di riavviare il computer dopo la chiamata della funzione [_ *RegReplaceKey.* *](/windows/desktop/api/winreg/nf-winreg-regreplacekeya) Questo processo funziona perché **RegReplaceKey** non sostituisce effettivamente l'hive del Registro di sistema finché il computer non viene riavviato e i dati del Registro di sistema aggiunti dalla funzione **DsRestoreRegister** non vengono specificamente esclusi dalla sostituzione durante un'operazione di ripristino del Registro di sistema.

 

 