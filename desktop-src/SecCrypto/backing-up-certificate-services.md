---
description: Come usare le funzioni di backup di Servizi certificati per eseguire il backup di un database di Servizi certificati e dei file associati.
ms.assetid: f5c9c9f9-5211-4151-b8e0-3351d462c71b
title: Backup di Servizi certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeeb0881d517de538971d7eafb835ec48f3f33328e3a026b450e6719bfb23ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773087"
---
# <a name="backing-up-certificate-services"></a>Backup di Servizi certificati

Di seguito è riportato uno scenario che illustra come usare le funzioni di backup di Servizi certificati per eseguire il backup di un database di Servizi certificati e dei file associati.

1.  Caricare la Certadm.dll in memoria (chiamando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).
2.  Recuperare l'indirizzo di ognuna delle funzioni necessarie in Certadm.dll (tramite [**GetProcAddress).**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) Usare questi indirizzi quando si chiamano le funzioni nei passaggi rimanenti.
3.  Chiamare [**CertSrvIsServerOnline per**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew) determinare se Servizi certificati è online. Per il corretto funzionamento delle operazioni di backup, è necessario che Servizi certificati sia online.
4.  Chiamare [**CertSrvBackupPrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew) per avviare una sessione di backup. L'handle del contesto di backup di Servizi certificati risultante verrà usato da molte delle altre funzioni di backup.
5.  Chiamare [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) per determinare la mappa di ripristino. La mappa di ripristino contiene i percorsi da utilizzare durante il ripristino del backup. Salvare le informazioni recuperate **da CertSrvRestoreGetDatabaseLocations** in un percorso specifico dell'applicazione.
6.  Chiamare [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) per determinare i nomi dei file di database di cui eseguire il backup. Per ognuno di questi file, eseguire i passaggi da 7 a 9.
7.  Chiamare [**CertSrvBackupOpenFile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew) per aprire il file per il backup.
8.  Chiamare [**CertSrvBackupRead**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread) per leggere una parte di byte dal file, quindi chiamare una routine specifica dell'applicazione per archiviare i byte in un supporto di backup. Ripetere questo passaggio fino a quando non viene eseguito il backup di tutti i byte nel file.
9.  Chiamare [**CertSrvBackupClose**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose) per chiudere il file.
10. Chiamare [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) per determinare i nomi dei file di log di cui eseguire il backup. Per ognuno di questi file, eseguire i passaggi da 7 a 9.
11. Chiamare [**CertSrvBackupTruncateLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs) per troncare i file di log di cui è stato eseguito il backup nei passaggi 6 e 10. Questo passaggio è facoltativo. Tuttavia, chiamare **CertSrvBackupTruncateLogs** solo se è stato eseguito il backup di tutti i file restituiti da [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw) e [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) . In caso contrario, l'operazione di ripristino avrà esito negativo. Per informazioni dettagliate, vedere la pagina di riferimento **di CertSrvBackupTruncateLogs.**
12. Chiamare [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) per determinare i nomi dei file non di database di cui eseguire il backup. Questi file sono identificati solo dalla funzione e devono essere sottoposti a backup in altri mezzi.
13. Eseguire il backup dei file dinamici identificati nel passaggio 12 usando routine separate da Certadm.dll.
14. Chiamare [**CertSrvBackupEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend) per terminare la sessione di backup.
15. Chiamare [**CertSrvBackupFree**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree) in base alle esigenze per rilasciare i buffer allocati da determinate funzioni di backup di Servizi certificati. Le chiamate a [**CertSrvBackupGetBackupLogs,**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw) [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)e [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw) allocano buffer che possono essere liberati da una chiamata a **CertSrvBackupFree.**
16. Rilasciare le Certadm.dll chiamando [**FreeLibrary.**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)

Per informazioni sui privilegi necessari per eseguire il backup del database di Servizi certificati e dei file [associati,](setting-the-backup-and-restore-privileges.md)vedere Impostazione dei privilegi di backup e ripristino .

 

 
