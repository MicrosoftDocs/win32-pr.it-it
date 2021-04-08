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
# <a name="composing-and-registering-spns-for-scp-based-windows-sockets-service"></a><span data-ttu-id="6fc5b-105">Composizione e registrazione dei nomi SPN per il servizio Windows Sockets basato su SCP</span><span class="sxs-lookup"><span data-stu-id="6fc5b-105">Composing and registering SPNs for SCP-based Windows Sockets Service</span></span>

<span data-ttu-id="6fc5b-106">Nell'esempio di codice seguente viene illustrato come comporre e registrare i nomi SPN per un servizio.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-106">The following code example shows how to compose and register the SPNs for a service.</span></span> <span data-ttu-id="6fc5b-107">Chiamare questo codice dal programma di installazione del servizio dopo aver chiamato [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) e aver creato il punto di connessione del servizio (SCP) del servizio.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-107">Call this code from your service installer after calling [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) and creating the service's service connection point (SCP).</span></span>

<span data-ttu-id="6fc5b-108">Nell'esempio di codice seguente vengono chiamate le funzioni di esempio **SpnCompose** e **spnregister** che compongono e registrano il nome SPN.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-108">The following code example calls the **SpnCompose** and **SpnRegister** example functions that compose and register the SPN.</span></span> <span data-ttu-id="6fc5b-109">Per altre informazioni e per il codice sorgente **SpnCompose** , vedere [composizione dei nomi SPN per un servizio con SCP](composing-the-spns-for-a-service-with-an-scp.md).</span><span class="sxs-lookup"><span data-stu-id="6fc5b-109">For more information and the **SpnCompose** source code, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md).</span></span> <span data-ttu-id="6fc5b-110">Per altre informazioni e per il codice sorgente di **spnregister** , vedere la pagina relativa alla [registrazione dei nomi SPN per un servizio](registering-the-spns-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="6fc5b-110">For more information and the **SpnRegister** source code, see [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span>

<span data-ttu-id="6fc5b-111">Questo esempio usa il nome della classe del servizio e il nome distinto del relativo SCP per creare il nome dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-111">This example uses the service class name and the distinguished name of its SCP to create its service principal name.</span></span> <span data-ttu-id="6fc5b-112">Per ulteriori informazioni e un esempio di codice in cui viene illustrato il modo in cui il client esegue l'associazione al servizio SCP per recuperare le stringhe dei nomi, vedere [come i client trovano e usano un punto di connessione del servizio](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="6fc5b-112">For more information and a code example that shows how the client binds to the service SCP to retrieve these name strings, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span> <span data-ttu-id="6fc5b-113">Tenere presente che il codice per la composizione di un nome SPN varia a seconda del tipo di servizio e dei meccanismi utilizzati per pubblicare il servizio.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-113">Be aware that the code for composing an SPN varies depending on the type of service and the mechanisms used to publish the service.</span></span>

<span data-ttu-id="6fc5b-114">Il servizio registra il nome SPN archiviando l'oggetto nell'attributo **servicePrincipalName** dell'oggetto account del servizio nella directory.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-114">The service registers its SPN by storing it in the **servicePrincipalName** attribute of the service's account object in the directory.</span></span> <span data-ttu-id="6fc5b-115">Se il servizio viene eseguito con l'account LocalSystem anziché con un account del servizio, viene registrato il nome SPN nell'oggetto dell'account del computer locale nella directory.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-115">If the service runs under the LocalSystem account instead of under a service account, it registers its SPN under the local computer account's object in the directory.</span></span>


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



<span data-ttu-id="6fc5b-116">È possibile utilizzare codice simile per annullare la registrazione dei nomi SPN quando il servizio viene disinstallato.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-116">You can use similar code to unregister your SPNs when your service is uninstalled.</span></span> <span data-ttu-id="6fc5b-117">Specificare l' **operazione \_ op DS SPN \_ Delete \_ SPN \_** anziché **DS \_ SPN \_ Add \_ SPN \_ op**.</span><span class="sxs-lookup"><span data-stu-id="6fc5b-117">Specify the **DS\_SPN\_DELETE\_SPN\_OP** operation instead of **DS\_SPN\_ADD\_SPN\_OP**.</span></span>

 

 