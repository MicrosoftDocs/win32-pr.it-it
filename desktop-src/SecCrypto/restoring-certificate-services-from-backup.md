---
description: Mostra come è possibile usare le funzioni di backup di Servizi certificati per ripristinare e recuperare un database di Servizi certificati e i file associati.
ms.assetid: f4914f45-629d-4f24-8328-d7f27e8a0062
title: Ripristino di Servizi certificati da backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f5adf46d802194909397a3b70483b3cf43bb409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317699"
---
# <a name="restoring-certificate-services-from-backup"></a>Ripristino di Servizi certificati da backup

Nello scenario seguente viene illustrato il modo in cui è possibile utilizzare le funzioni di backup di Servizi certificati per ripristinare e recuperare un database di Servizi certificati e i file associati. Il processo di ripristino prevede la scrittura dei file contenuti in un set di backup su disco. È possibile ripristinare più set di backup (un backup completo più zero o più backup incrementali), ma tutti i ripristini devono essere completati prima di iniziare il processo di ripristino. Il processo di ripristino prevede la riproduzione dei file di log da parte di Servizi certificati per garantire la coerenza del database e del file di registro, garantendo così l'integrità del database In questo scenario vengono illustrate le chiamate di funzione per ripristinare i set di backup e informare i servizi certificati dei parametri di ripristino.

Prima di implementare questo scenario, deve esistere un backup completo esistente del database di Servizi certificati.

1.  Caricare la libreria Certadm.dll in memoria (chiamando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).
2.  Recuperare l'indirizzo di ognuna delle funzioni necessarie in Certadm.dll (tramite [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)). Usare questi indirizzi quando si chiamano le funzioni nei passaggi rimanenti.
3.  Chiamare [**CertSrvIsServerOnline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) per determinare se Servizi certificati è online. Se Servizi certificati è in esecuzione, arrestarlo prima di procedere. Per il corretto funzionamento delle operazioni di ripristino, i servizi certificati non devono essere online.
4.  Chiamare [**CertSrvRestorePrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestorepreparew) per avviare una sessione di ripristino. L'handle del contesto di backup di Servizi certificati risultante verrà utilizzato da diverse altre funzioni.
5.  Determinare il percorso per il percorso del database. Durante uno scenario di backup, questo valore sarebbe stato disponibile da una chiamata a [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw); Questo valore deve essere stato archiviato come parte del backup.
6.  Creare una mappa di ripristino che specifichi il nome del database ripristinato. Una struttura della mappa di ripristino del database di Servizi certificati (CSEDB \_ RSTMAPW) viene utilizzata per specificare una mappa di ripristino. Impostare il \_ membro **pwszDatabaseName** di RSTMAPW di CSEDB e il \_ membro **RSTMAPW** di CSEDB pwszNewDatabaseName sul percorso del database determinato nel passaggio 5. Facoltativamente, se il database ripristinato ha un nome diverso da quello del database di backup, impostare il \_ membro **pwszNewDatabaseName** di RSTMAPW CSEDB sul nuovo nome del database.
7.  Se si desidera assicurarsi che le modifiche apportate al database dopo l'esecuzione del backup non vengano riapplicate dopo il completamento del ripristino del database (come parte del ripristino del database eseguito durante il successivo avvio dei servizi certificati), eliminare i file dal database attivo e dalle directory di log del server di destinazione.
8.  Copiare i file contenuti nel backup completo nel database attivo e nelle directory di log del server di destinazione.
9.  Chiamare [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw) per registrare un'operazione di ripristino per il backup completo. **CertSrvRestoreRegister** usa la mappa di ripristino specificata nel passaggio 6. **CertSrvRestoreRegister** specifica anche il percorso del database di backup e dei log. La chiamata di **CertSrvRestoreRegister** forza i servizi certificati a tentare un'operazione di ripristino al successivo avvio. Impedisce inoltre ai Servizi certificati di elaborare le richieste di certificato fino al completamento del ripristino.
10. Chiamare [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete), completando così l'attività di registrazione iniziata nel passaggio 8. Si noti che la registrazione di un'operazione di ripristino è un'istruzione per i servizi certificati da seguire all'avvio; il ripristino effettivo verrà eseguito solo dopo l'avvio di Servizi certificati.
11. Per eseguire il ripristino di ogni backup incrementale, copiare i file contenuti nel backup incrementale nella directory di log Active del server di destinazione, quindi chiamare [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw), seguito da una chiamata a [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete). La registrazione dei backup incrementali per il ripristino può essere eseguita in qualsiasi ordine, ma solo il set di file per un backup incrementale deve essere copiato nel server prima di ogni chiamata a **CertSrvRestoreRegister**.
12. Copiare i file dinamici di Servizi certificati nel server di destinazione. I file dinamici sono stati identificati durante il backup quando è stato chiamato [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) . Potrebbe essere necessario arrestare il servizio di pubblicazione World Wide Web per consentire la sovrascrittura dei file dinamici.
13. Chiamare [**CertSrvRestoreEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreend) per terminare la sessione di ripristino.
14. Avviare l'applicazione Servizi certificati manualmente (o attendere il riavvio successivo per avviarla automaticamente). All'avvio di Servizi certificati, verrà determinato se un'operazione di ripristino è stata registrata. Se un'operazione di ripristino è stata registrata, i servizi certificati inizieranno il ripristino. Servizi certificati non elaborerà alcuna richiesta di certificato fino al completamento dell'operazione di ripristino.

> [!Note]  
> Una volta completato il ripristino, è importante eseguire un nuovo backup completo del database di Servizi certificati. Questa operazione è necessaria per troncare i file di log ripristinati e per stabilire un set di backup di base per i ripristini futuri. I backup eseguiti dopo un'operazione di ripristino non possono essere combinati con i backup (completi o incrementali) eseguiti prima del ripristino. ovvero, dopo il ripristino di un database di Servizi certificati e l'avanzamento a uno stato successivo, non è possibile utilizzare i backup di pre-ripristino per ripristinare lo stato successivo del database.

 

 

 
