---
title: Installazione di un servizio in un computer host
description: Nell'esempio di codice seguente vengono illustrati i passaggi di base per l'installazione di un servizio abilitato per la directory in un computer host.
ms.assetid: 35a3b261-d499-4154-a022-1e33a9ef7ba8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d687bbbfadb4d1ccb789e9d5f1051ebfbb4484d7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472526"
---
# <a name="installing-a-service-on-a-host-computer"></a>Installazione di un servizio in un computer host

Nell'esempio di codice seguente vengono illustrati i passaggi di base per l'installazione di un servizio abilitato per la directory in un computer host. Esegue le operazioni seguenti:

1.  Chiama la funzione [**OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) per aprire un handle per Gestione controllo servizi (SCM) nel computer locale.
2.  Chiama la funzione [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) per installare il servizio nel database SCM. Questa chiamata specifica l'account e la password di accesso del servizio, nonché l'eseguibile del servizio e altre informazioni sul servizio. **CreateService** ha esito negativo se l'account di accesso specificato non è valido. Tuttavia, **CreateService** non controlla la validità della password. Non verifica inoltre che l'account disponga dell'accesso come servizio direttamente nel computer locale. Per ulteriori informazioni, vedere [concessione dell'accesso come servizio direttamente nel computer host](granting-logon-as-service-right-on-the-host-computer.md).
3.  Chiama la subroutine **ScpCreate** del servizio che crea un oggetto punto di connessione del servizio (SCP) nella directory per pubblicare il percorso dell'istanza del servizio. Per ulteriori informazioni, vedere [modalità di individuazione e utilizzo di un punto di connessione del servizio](how-clients-find-and-use-a-service-connection-point.md)da parte dei client. Questa routine archivia anche le informazioni di associazione del servizio nel SCP, imposta una voce ACE sull'SCP in modo che il servizio possa accedervi in fase di esecuzione, memorizza nella cache il nome distinto del SCP nel registro di sistema locale e restituisce il nome distinto del nuovo SCP.
4.  Chiama la subroutine **SpnCompose** del servizio che usa la stringa di classe del servizio e il nome distinto del SCP per comporre un nome dell'entità servizio (SPN). Per ulteriori informazioni, vedere [composizione dei nomi SPN per un servizio con SCP](composing-the-spns-for-a-service-with-an-scp.md). Il nome SPN identifica in modo univoco questa istanza del servizio.
5.  Chiama la subroutine **spnregister** del servizio che registra il nome SPN nell'oggetto account associato all'account di accesso del servizio. Per ulteriori informazioni, vedere [la pagina relativa alla registrazione dei nomi SPN per un servizio](registering-the-spns-for-a-service.md). La registrazione del nome SPN consente alle applicazioni client di autenticare il servizio.

Questo esempio di codice funziona correttamente indipendentemente dal fatto che l'account di accesso sia un account utente locale o di dominio o l'account LocalSystem. Per un account utente di dominio, il parametro *szServiceAccountSAM* contiene il nome ****\\*** utente di dominio* dell'account e il parametro *szServiceAccountDN* contiene il nome distinto dell'oggetto account utente nella directory. Per l'account LocalSystem, *szServiceAccountSAM* e *szPassword* sono **null** e *szServiceAccountSN* è il nome distinto dell'oggetto account del computer locale nella directory. Se *szServiceAccountSAM* specifica un account utente locale (il formato del nome è ". \\ *Nome utente*"), l'esempio di codice ignora la registrazione del nome SPN perché l'autenticazione reciproca non è supportata per gli account utente locali.

Tenere presente che la configurazione di sicurezza predefinita consente solo agli amministratori di dominio di eseguire questo codice.

Tenere inoltre presente che questo esempio di codice, come scritto, deve essere eseguito nel computer in cui viene installato il servizio. Di conseguenza, è in genere in un eseguibile di installazione separato dal codice di installazione del servizio, se presente, che estende lo schema, estende l'interfaccia utente o imposta criteri di gruppo. Tali operazioni installano i componenti del servizio per un'intera foresta, mentre questo codice installa il servizio in un singolo computer.


```C++
void InstallServiceOnLocalComputer(
            LPTSTR szServiceAccountDN,  // Distinguished name of logon account.
            LPTSTR szServiceAccountSAM, // SAM name of logon account.
            LPTSTR szPassword)          // Password of logon account.
{
SC_HANDLE   schService = NULL;
SC_HANDLE   schSCManager = NULL;
TCHAR szPath[512];
LPTSTR lpFilePart;
TCHAR szDNofSCP[MAX_PATH];
TCHAR szServiceClass[]=TEXT("ADSockAuth");
 
DWORD dwStatus;
TCHAR **pspn=NULL;
ULONG ulSpn=1;
 
// Get the full path of the service's executable.
// The code example assumes that the executable is in the current directory.
dwStatus = GetFullPathName(TEXT("service.exe"), 512, szPath, &lpFilePart);
if (dwStatus == 0) {
    _tprintf(TEXT("Unable to install %s - %s\n"), 
            TEXT(SZSERVICEDISPLAYNAME), GetLastErrorText(szErr, 256));
    return;
}
_tprintf(TEXT("path of service.exe: %s\n"), szPath);
 
// Open the Service Control Manager on the local computer.
schSCManager = OpenSCManager(
                NULL,                   // Computer (NULL == local)
                NULL,                   // Database (NULL == default)
                SC_MANAGER_ALL_ACCESS   // Access required
                );
if (! schSCManager) {
    _tprintf(TEXT("OpenSCManager failed - %s\n"), 
                   GetLastErrorText(szErr,256));
    goto cleanup;
}
        
// Install the service in the SCM database.
schService = CreateService(
            schSCManager,               // SCManager database
            TEXT(SZSERVICENAME),        // Name of service
            TEXT(SZSERVICEDISPLAYNAME), // Name to display
            SERVICE_ALL_ACCESS,         // Desired access
            SERVICE_WIN32_OWN_PROCESS,  // Service type
            SERVICE_DEMAND_START,       // Start type
            SERVICE_ERROR_NORMAL,       // Error control type
            szPath,                     // Service binary
            NULL,                       // No load ordering group
            NULL,                       // No tag identifier
            TEXT(SZDEPENDENCIES),       // Dependencies
            szServiceAccountSAM,        // Service account
            szPassword);                // Account password
if (! schService) {
    _tprintf(TEXT("CreateService failed - %s\n"), 
                   GetLastErrorText(szErr,256));
    goto cleanup;
}
 
_tprintf(TEXT("%s installed.\n"), TEXT(SZSERVICEDISPLAYNAME) );
 
// Create the service's Service Connection Point (SCP).
dwStatus = ScpCreate(
        2000,                 // Service default port number
        szServiceClass,       // Specifies the service class string
        szServiceAccountSAM,  // SAM name of logon account for ACE
        szDNofSCP             // Buffer returns the DN of the SCP
        );
if (dwStatus != 0) {
    _tprintf(TEXT("ScpCreate failed: %d\n"), dwStatus );
    DeleteService(schService);
    goto cleanup;
}
 
// Compose and register a service principal name for this service.
// This is performed on the install path because this requires elevated
// privileges for updating the directory.
// If a local account of the format ".\user name", skip the SPN.
if ( szServiceAccountSAM[0] == '.' ) 
{
    _tprintf(TEXT("Do not register SPN for a local account.\n"));
    goto cleanup;
}
 
dwStatus = SpnCompose(
        &pspn,            // Receives pointer to the SPN array.
        &ulSpn,           // Receives number of SPNs returned.
        szDNofSCP,        // Input: DN of the SCP.
        szServiceClass);  // Input: the service's class string.
 
if (dwStatus == NO_ERROR) 
    dwStatus = SpnRegister(
        szServiceAccountDN,  // Account on which SPNs are registered.
        pspn,                // Array of SPNs to register.
        ulSpn,               // Number of SPNs in array.
        DS_SPN_ADD_SPN_OP);  // Operation code: Add SPNs.
 
if (dwStatus != NO_ERROR) 
{
    _tprintf(TEXT("Failed to compose SPN: Error was %X\n"), 
                  dwStatus);
    DeleteService(schService);
    ScpDelete(szDNofSCP, szServiceClass, szServiceAccountDN);
    goto cleanup;
}
 
cleanup:
if (schSCManager)
    CloseServiceHandle(schSCManager);
if (schService)
    CloseServiceHandle(schService);
DsFreeSpnArray(ulSpn, pspn);
return;
}
```



Per ulteriori informazioni sull'esempio di codice precedente, vedere [composizione dei nomi SPN per un servizio con SCP](composing-the-spns-for-a-service-with-an-scp.md) e [registrazione dei nomi SPN per un servizio](registering-the-spns-for-a-service.md).

 

 