---
title: Composizione e registrazione dei nomi SPN per il servizio Windows Sockets basato su SCP
description: Nell'esempio di codice seguente viene illustrato come comporre e registrare i nomi SPN per un servizio. Chiamare questo codice dal programma di installazione del servizio dopo aver chiamato CreateService e aver creato il punto di connessione del servizio (SCP) del servizio.
ms.assetid: 3957af10-974a-415f-b8fb-d9b52ac5a82d
ms.tgt_platform: multiple
keywords:
- nomi dell'entità servizio AD, composizione e registrazione di SPN per un servizio Windows Sockets basato su SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d754d51c0ad34b1623bdc84fc8178b04d33515ed
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724618"
---
# <a name="composing-and-registering-spns-for-scp-based-windows-sockets-service"></a>Composizione e registrazione dei nomi SPN per il servizio Windows Sockets basato su SCP

Nell'esempio di codice seguente viene illustrato come comporre e registrare i nomi SPN per un servizio. Chiamare questo codice dal programma di installazione del servizio dopo aver chiamato [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) e aver creato il punto di connessione del servizio (SCP) del servizio.

Nell'esempio di codice seguente vengono chiamate le funzioni di esempio **SpnCompose** e **spnregister** che compongono e registrano il nome SPN. Per altre informazioni e per il codice sorgente **SpnCompose** , vedere [composizione dei nomi SPN per un servizio con SCP](composing-the-spns-for-a-service-with-an-scp.md). Per altre informazioni e per il codice sorgente di **spnregister** , vedere la pagina relativa alla [registrazione dei nomi SPN per un servizio](registering-the-spns-for-a-service.md).

Questo esempio usa il nome della classe del servizio e il nome distinto del relativo SCP per creare il nome dell'entità servizio. Per ulteriori informazioni e un esempio di codice in cui viene illustrato il modo in cui il client esegue l'associazione al servizio SCP per recuperare le stringhe dei nomi, vedere [come i client trovano e usano un punto di connessione del servizio](how-clients-find-and-use-a-service-connection-point.md). Tenere presente che il codice per la composizione di un nome SPN varia a seconda del tipo di servizio e dei meccanismi utilizzati per pubblicare il servizio.

Il servizio registra il nome SPN archiviando l'oggetto nell'attributo **servicePrincipalName** dell'oggetto account del servizio nella directory. Se il servizio viene eseguito con l'account LocalSystem anziché con un account del servizio, viene registrato il nome SPN nell'oggetto dell'account del computer locale nella directory.


```C++
TCHAR szDNofSCP[MAX_PATH]; // DN of SCP. Initialize by querying SCP.
TCHAR szServiceClass[]=TEXT("ADSockAuth");
LPCTSTR szServiceAccountDN;   // DN of a service logon account. 
 
DWORD dwStatus;
TCHAR **pspn = NULL;
ULONG ulSpn = 1;
 
// Compose the SPNs.
dwStatus = SpnCompose(
        &pspn,              // Receives pointer to the SPN array.
        &ulSpn,             // Receives number of SPNs returned.
        szDNofSCP,          // Input: DN of the SCP.
        szServiceClass);    // Input: the service class string.
 
// Register the SPNs
if (dwStatus == NO_ERROR) 
    dwStatus = SpnRegister(
       szServiceAccountDN,  // Logon account to register SPNs on
       pspn,                // Array of SPNs
       ulSpn,               // Number of SPNs in array
       DS_SPN_ADD_SPN_OP);  // Add SPNs to the account
 
// Free the array of SPNs returned by SpnCompose.
DsFreeSpnArray(ulSpn, pspn); 
```



È possibile utilizzare codice simile per annullare la registrazione dei nomi SPN quando il servizio viene disinstallato. Specificare l' **operazione \_ op DS SPN \_ Delete \_ SPN \_** anziché **DS \_ SPN \_ Add \_ SPN \_ op**.

 

 