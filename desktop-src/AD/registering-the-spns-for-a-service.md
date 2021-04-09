---
title: Registrazione dei nomi SPN per un servizio
description: Nell'esempio di codice seguente viene registrato o annullata la registrazione di uno o più nomi di entità servizio (SPN) per un'istanza del servizio.
ms.assetid: 60c252c7-76d2-4683-bf90-0f3483e6e8e0
ms.tgt_platform: multiple
keywords:
- Registrazione dei nomi SPN per un servizio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f51e6e40113a76c4a85603aa88fbb2683945330
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956305"
---
# <a name="registering-the-spns-for-a-service"></a><span data-ttu-id="655c4-104">Registrazione dei nomi SPN per un servizio</span><span class="sxs-lookup"><span data-stu-id="655c4-104">Registering the SPNs for a Service</span></span>

<span data-ttu-id="655c4-105">Nell'esempio di codice seguente viene registrato o annullata la registrazione di uno o più nomi di entità servizio (SPN) per un'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="655c4-105">The following code example registers or unregisters one or more service principal names (SPNs) for a service instance.</span></span>

<span data-ttu-id="655c4-106">Nell'esempio viene chiamata la funzione [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) , in cui vengono archiviati i nomi spn in Active Directory Domain Services sotto l'attributo [**servicePrincipalName**](/windows/desktop/ADSchema/a-serviceprincipalname) dell'oggetto account specificato dal parametro *pszServiceAcctDN* .</span><span class="sxs-lookup"><span data-stu-id="655c4-106">The example calls the [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) function, which stores the SPNs in Active Directory Domain Services under the [**servicePrincipalName**](/windows/desktop/ADSchema/a-serviceprincipalname) attribute of the account object specified by the *pszServiceAcctDN* parameter.</span></span> <span data-ttu-id="655c4-107">L'oggetto account corrisponde all'account di accesso specificato nella chiamata [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) per l'istanza del servizio.</span><span class="sxs-lookup"><span data-stu-id="655c4-107">The account object corresponds to the logon account specified in the [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) call for this service instance.</span></span> <span data-ttu-id="655c4-108">Se l'account di accesso è un account utente di dominio, *pszServiceAcctDN* deve essere il nome distinto dell'oggetto account in dominio di Active Directory Server per l'account utente.</span><span class="sxs-lookup"><span data-stu-id="655c4-108">If the logon account is a domain user account, *pszServiceAcctDN* must be the distinguished name of the account object in Active Directory Domain Servers for that user account.</span></span> <span data-ttu-id="655c4-109">Se l'account di accesso del servizio è l'account LocalSystem, *pszServiceAcctDN* deve essere il nome distinto dell'oggetto account computer per il computer host in cui è installato il servizio.</span><span class="sxs-lookup"><span data-stu-id="655c4-109">If the service's logon account is the LocalSystem account, *pszServiceAcctDN* must be the distinguished name of the computer account object for the host computer on which the service is installed.</span></span>


```C++
/***************************************************************************

    SpnRegister()

    Register or unregister the SPNs under the service's account.

    If the service runs in LocalSystem account, pszServiceAcctDN is the 
    distinguished name of the local computer account.

    Parameters:

    pszServiceAcctDN - Contains the distinguished name of the logon 
    account for this instance of the service.

    pspn - Contains an array of SPNs to register.

    ulSpn - Contains the number of SPNs in the array.

    Operation - Contains one of the DS_SPN_WRITE_OP values that determines 
    the type of operation to perform on the SPNs.

***************************************************************************/

DWORD SpnRegister(TCHAR *pszServiceAcctDN,
                  TCHAR **pspn,
                  unsigned long ulSpn,
                  DS_SPN_WRITE_OP Operation)
{
    DWORD dwStatus;
    HANDLE hDs;
    TCHAR szSamName[512];
    DWORD dwSize = sizeof(szSamName) / sizeof(szSamName[0]);
    PDOMAIN_CONTROLLER_INFO pDcInfo;

    // Bind to a domain controller. 
    // Get the domain for the current user.
    if(GetUserNameEx(NameSamCompatible, szSamName, &dwSize))
    {
        TCHAR *pWhack = _tcschr(szSamName, '\\');
        if(pWhack)
        {
            *pWhack = '\0';
        }
    } 
    else 
    {
        return GetLastError();
    }
     
    // Get the name of a domain controller in that domain.
    dwStatus = DsGetDcName(NULL,
        szSamName,
        NULL,
        NULL,
        DS_IS_FLAT_NAME |
            DS_RETURN_DNS_NAME |
            DS_DIRECTORY_SERVICE_REQUIRED,
        &pDcInfo);
    if(dwStatus != 0) 
    {
        return dwStatus;
    }
     
    // Bind to the domain controller.
    dwStatus = DsBind(pDcInfo->DomainControllerName, NULL, &hDs);
     
    // Free the DOMAIN_CONTROLLER_INFO buffer.
    NetApiBufferFree(pDcInfo);
    if(dwStatus != 0) 
    {
        return dwStatus;
    }
     
    // Write the SPNs to the service account or computer account.
    dwStatus = DsWriteAccountSpn(
            hDs,                    // Handle to the directory.
            Operation,              // Add or remove SPN from account's existing SPNs.
            pszServiceAcctDN,       // DN of service account or computer account.
            ulSpn,                  // Number of SPNs to add.
            (const TCHAR **)pspn);  // Array of SPNs.

    // Unbind the DS in any case.
    DsUnBind(&hDs);
     
    return dwStatus;
}
```



 

 