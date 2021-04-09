---
title: Esecuzione del backup di un server di Active Directory
description: Per un backup del server Active Directory è necessario eseguire il backup del database e dei log delle transazioni. Questo argomento fornisce una procedura dettagliata sul backup del servizio Active Directory directory da parte di un'applicazione di backup.
ms.assetid: 250b2f40-6d43-4aa5-a588-b0cd4839828d
ms.tgt_platform: multiple
keywords:
- backup Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5affde952ee543afe1bb9b794cce074a74382aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044015"
---
# <a name="backing-up-an-active-directory-server"></a>Esecuzione del backup di un server di Active Directory

Per un backup del server Active Directory è necessario eseguire il backup del database e dei log delle transazioni. Questo argomento fornisce una procedura dettagliata sul backup del servizio Active Directory directory da parte di un'applicazione di backup.

Il chiamante di queste funzioni di backup deve avere il privilegio **\_ \_ nome backup se** . È possibile utilizzare la funzione [**DsSetAuthIdentity**](dssetauthidentity.md) per impostare il contesto di sicurezza in cui vengono chiamate le funzioni di backup/ripristino della directory.

**Per eseguire il backup di un server di Active Directory, seguire questa procedura**

1.  Chiamare la funzione [**DsIsNTDSOnline**](dsisntdsonline.md) per determinare se Active Directory Domain Services sono in esecuzione.
2.  Se Active Directory Domain Services è in esecuzione, chiamare la funzione [**DsBackupPrepare**](dsbackupprepare.md) per inizializzare un handle del contesto di backup. Se Active Directory Domain Services non sono in esecuzione, non è possibile eseguirne il backup e l'applicazione di backup deve interrompere l'operazione di backup.
3.  Chiamare la funzione [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) per ottenere un elenco di file di cui eseguire il backup. Per rilasciare la memoria restituita da questa funzione, chiamare la funzione [**DsBackupFree**](dsbackupfree.md) .
4.  Per ogni nome nell'elenco di file restituito, chiamare la funzione [**DsBackupOpenFile**](dsbackupopenfile.md) seguita da chiamate ripetute alla funzione [**DsBackupRead**](dsbackupread.md) fino a quando non viene letto l'intero file. Al termine della lettura del file, chiamare la funzione [**DsBackupClose**](dsbackupclose.md) per chiuderla.
5.  Dopo aver eseguito il backup di tutti i file di database, chiamare la funzione [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) per ottenere un elenco dei log delle transazioni. Questo elenco viene gestito esattamente come l'elenco dei file di database.
6.  Al termine del backup del log delle transazioni, chiamare la funzione [**DsBackupTruncateLogs**](dsbackuptruncatelogs.md) per eliminare tutti i log delle transazioni di cui è stato eseguito il commit.
7.  Salvare il contenuto del token di scadenza fornito dalla funzione [**DsBackupPrepare**](dsbackupprepare.md) . Questa operazione può essere salvata in un file o in un'altra memoria persistente. Questo token deve essere passato alla funzione [**DsRestorePrepare**](dsrestoreprepare.md) per avviare un'operazione di ripristino.
8.  Liberare la memoria per il token di scadenza passando il puntatore del token alla funzione [**DsBackupFree**](dsbackupfree.md) .
9.  Infine, chiamare la funzione [**DsBackupEnd**](dsbackupend.md) per rilasciare tutte le risorse associate all'handle del contesto di backup.

 

 




