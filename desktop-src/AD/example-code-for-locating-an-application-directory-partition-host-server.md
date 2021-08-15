---
title: Codice di esempio per l'individuazione di un server host della partizione di directory applicativa
description: Questo argomento include un esempio di codice che individua un server host della partizione di directory applicativa.
ms.assetid: c161323b-13ce-4986-8b24-b459009ff53c
ms.tgt_platform: multiple
keywords:
- Codice di esempio per l'individuazione di un server host della partizione di directory applicativa AD
- Partizione di directory applicativa AD , codice di esempio per l'individuazione di un server host della partizione di directory applicativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d7a218acf3608c18587b7d9b9c82779f17fd6eb251608a86d99d8acb3b7bd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118693600"
---
# <a name="example-code-for-locating-an-application-directory-partition-host-server"></a>Codice di esempio per l'individuazione di un server host della partizione di directory applicativa

Questo argomento include un esempio di codice che individua un server host della partizione di directory applicativa.

L'esempio di codice C/C++ seguente illustra come usare la funzione [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea) per individuare un controller di dominio che ospita una replica di una partizione di directory applicativa. Questo esempio di codice illustra anche come usare la [**funzione DsCrackNames**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dscracknamesa) per convertire il nome distinto di una partizione di directory applicativa in un nome DNS.


```C++
/***************************************************************************

    AppPartitionDNToDNS()

    Converts the distinguished name of an application directory partition to 
    a DNS name for the partition.

    The caller must free the memory allocated to ppszDNS by calling 
    FreeADsMem when it is no longer required.

***************************************************************************/

DWORD AppPartitionDNToDNS(LPCTSTR pszDN, LPTSTR *ppszDNS)
{   
    DWORD dwRet;
    LPCTSTR rgpszNames[] = {pszDN};
    PDS_NAME_RESULT pResults;

    /*
    Convert the distinguished name to a DNS name using only syntactic 
    mapping. The DS_NAME_FLAG_SYNTACTICAL_ONLY flag allows DsCrackNames to 
    be called without binding.
    */
    dwRet = DsCrackNames(NULL, 
        DS_NAME_FLAG_SYNTACTICAL_ONLY,
        DS_FQDN_1779_NAME,
        DS_CANONICAL_NAME,
        1,
        rgpszNames,
        &pResults);

    if(NO_ERROR == dwRet)
    {
        /*
        Allocate the memory and copy the DNS name of the partition.
        */
        DWORD dwBytes = (lstrlen(pResults->rItems[0].pDomain) + 1) * sizeof(TCHAR);
        *ppszDNS = (LPTSTR)AllocADsMem(dwBytes);
        if(*ppszDNS)
        {
            wcsncpy_s(*ppszDNS, pResults->rItems[0].pDomain, dwBytes);

            dwRet = NO_ERROR;
        }
        else
        {
            dwRet = ERROR_NOT_ENOUGH_MEMORY;
        }
        
        // Free the result set.
        DsFreeNameResult(pResults);
    }
    
    return dwRet;
}

/***************************************************************************

    PrintDCFromAppPartition()

    Given the distinguished name of an application directory partition, 
    prints to the console the DNS name of a domain controller that hosts a 
    replica of the application directory partition.

***************************************************************************/

DWORD PrintDCFromAppPartition(LPCTSTR pszAppPartitionDN)
{
    DWORD dwRet;

    /*
    Convert the distinguished name of the partition to a DNS name so that 
    the DNS name can be passed to DsGetDcName.
    */
    LPTSTR pszDNS;
    dwRet = AppPartitionDNToDNS(pszAppPartitionDN, &pszDNS);
    if(NO_ERROR == dwRet)
    {
        PDOMAIN_CONTROLLER_INFO pdci;

        /*
        Get the name of a domain controller that hosts a replica of the 
        application directory partition.
        */
        dwRet = DsGetDcName(NULL, 
            pszDNS, 
            NULL, 
            NULL, 
            DS_ONLY_LDAP_NEEDED, 
            &pdci);

        if(NO_ERROR == dwRet)
        {
            // Print the DNS name of the domain controller.
            _tprintf(pdci->DomainControllerName);
            
            NetApiBufferFree(pdci);
        }

        FreeADsMem(pszDNS);
    }

    return dwRet;
}
```



 

 




