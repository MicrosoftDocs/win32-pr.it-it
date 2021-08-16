---
description: Illustra come usare le funzioni di backup di Servizi certificati per ripristinare un database di Servizi certificati e i file associati.
ms.assetid: f4914f45-629d-4f24-8328-d7f27e8a0062
title: Ripristino di Servizi certificati dal backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665a1aed873cdf25f24dc5a7bc8b8466a5c3ae7a6c1aaf6bec07d2e8be336e9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900524"
---
# <a name="restoring-certificate-services-from-backup"></a>Ripristino di Servizi certificati dal backup

Lo scenario seguente illustra come usare le funzioni di backup di Servizi certificati per ripristinare e ripristinare un database di Servizi certificati e i file associati. Il processo di ripristino prevede la scrittura su disco dei file contenuti in un set di backup. È possibile ripristinare più set di backup (un backup completo più zero o più backup incrementali), ma tutti i ripristini devono essere completati prima di iniziare il processo di ripristino. Il processo di ripristino prevede che Servizi certificati riproduca i file di log per garantire la coerenza dei file di database e di log, garantendo in tal modo l'integrità del database. Lo scenario illustra le chiamate di funzione per ripristinare i set di backup e informare Servizi certificati dei parametri di ripristino.

Prima di implementare questo scenario, è necessario che esista un backup completo esistente del database di Servizi certificati.

1.  Caricare la Certadm.dll in memoria (chiamando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).
2.  Recuperare l'indirizzo di ognuna delle funzioni necessarie in Certadm.dll (tramite [**GetProcAddress).**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) Usare questi indirizzi quando si chiamano le funzioni nei passaggi rimanenti.
3.  Chiamare [**CertSrvIsServerOnline per**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) determinare se Servizi certificati è online. Se Servizi certificati è in esecuzione, arrestarlo prima di procedere. Per il corretto funzionamento delle operazioni di ripristino, Servizi certificati non deve essere online.
4.  Chiamare [**CertSrvRestorePrepare per**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestorepreparew) avviare una sessione di ripristino. L'handle del contesto di backup di Servizi certificati risultante verrà usato da molte delle altre funzioni.
5.  Determinare il percorso del database. Durante uno scenario di backup, questo valore sarebbe stato disponibile da una chiamata a [**CertSrvRestoreGetDatabaseLocations;**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) Questo valore deve essere stato archiviato come parte del backup.
6.  Creare una mappa di ripristino specificando il nome del database ripristinato. Per specificare una mappa di ripristino viene usata una struttura della mappa di ripristino del database di Servizi certificati (CSEDB \_ RSTMAPW). Impostare il membro \_ **pwszDatabaseName** di CSEDB RSTMAPW e il membro \_ **pwszNewDatabaseName** di CSEDB RSTMAPW sul percorso del database determinato nel passaggio 5. Facoltativamente, se il database ripristinato deve avere un nome diverso rispetto al database di backup, impostare il membro \_ **pwszNewDatabaseName** di CSEDB RSTMAPW sul nuovo nome del database.
7.  Se si desidera assicurarsi che le modifiche apportate al database dopo l'esecuzione del backup non siano riapplicate dopo il completamento del ripristino del database (come parte del ripristino del database eseguito al successivo avvio di Servizi certificati), eliminare i file dal database attivo e dalle directory di log del server di destinazione.
8.  Copiare i file contenuti nel backup completo nelle directory del database e del log attive del server di destinazione.
9.  Chiamare [**CertSrvRestoreRegister per**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw) registrare un'operazione di ripristino per il backup completo. **CertSrvRestoreRegister** usa la mappa di ripristino specificata nel passaggio 6. **CertSrvRestoreRegister** specifica anche il percorso del database di backup e dei log. La **chiamata a CertSrvRestoreRegister** forza Servizi certificati a tentare un'operazione di ripristino al successivo avvio. Impedisce inoltre a Servizi certificati di elaborare le richieste di certificati fino al completamento del ripristino.
10. Chiamare [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete), terminando così l'attività di registrazione avviata nel passaggio 8. Si noti che la registrazione di un'operazione di ripristino è un'istruzione che Servizi certificati deve seguire all'avvio; Il ripristino effettivo verrà avviato solo dopo l'avvio di Servizi certificati.
11. Per ogni backup incrementale da ripristinare, copiare i file contenuti nel backup incrementale nella directory dei log attivi del server di destinazione, quindi chiamare [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw), seguito da una chiamata a [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete). La registrazione dei backup incrementali per il ripristino può avvenire in qualsiasi ordine, ma solo il set di file per un backup incrementale deve essere copiato nel server prima di ogni chiamata a **CertSrvRestoreRegister.**
12. Copiare i file dinamici di Servizi certificati nel server di destinazione. I file dinamici sarebbero stati identificati durante il backup quando è stato chiamato [**CertSrvBackupGetDynamicFileList.**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) Potrebbe essere necessario arrestare il servizio di World Wide Web per consentire la sovrascrittura dei file dinamici.
13. Chiamare [**CertSrvRestoreEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreend) per terminare la sessione di ripristino.
14. Avviare manualmente l'applicazione Servizi certificati (o attendere il successivo riavvio per l'avvio automatico). All'avvio di Servizi certificati, determina se è stata registrata un'operazione di ripristino. Se è stata registrata un'operazione di ripristino, Servizi certificati inizierà il ripristino. Servizi certificati non eelaborare alcuna richiesta di certificato fino al completamento dell'operazione di ripristino.

> [!Note]  
> Al termine di un ripristino, è importante eseguire un nuovo backup completo del database di Servizi certificati. Questa operazione è necessaria per troncare i file di log ripristinati e per stabilire un set di backup di base per ripristini futuri. I backup eseguiti dopo un ripristino non possono essere misti con i backup (completi o incrementali) eseguiti prima del ripristino; in altre informazioni, dopo il ripristino di un database di Servizi certificati e il passaggio a uno stato successivo, non è possibile utilizzare i backup di pre-ripristino per ripristinare il database a tale stato successivo.

 

 

 
