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
# <a name="registering-the-spns-for-a-service"></a>Registrazione dei nomi SPN per un servizio

Nell'esempio di codice seguente viene registrato o annullata la registrazione di uno o più nomi di entità servizio (SPN) per un'istanza del servizio.

Nell'esempio viene chiamata la funzione [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) , in cui vengono archiviati i nomi spn in Active Directory Domain Services sotto l'attributo [**servicePrincipalName**](/windows/desktop/ADSchema/a-serviceprincipalname) dell'oggetto account specificato dal parametro *pszServiceAcctDN* . L'oggetto account corrisponde all'account di accesso specificato nella chiamata [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) per l'istanza del servizio. Se l'account di accesso è un account utente di dominio, *pszServiceAcctDN* deve essere il nome distinto dell'oggetto account in dominio di Active Directory Server per l'account utente. Se l'account di accesso del servizio è l'account LocalSystem, *pszServiceAcctDN* deve essere il nome distinto dell'oggetto account computer per il computer host in cui è installato il servizio.


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



 

 