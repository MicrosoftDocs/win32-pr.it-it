---
description: I criteri LSA forniscono diverse funzioni che è possibile usare per creare, enumerare ed eliminare domini trusted e per impostare e recuperare informazioni sui domini trusted.
ms.assetid: 0c7534d7-3372-49c4-992c-9b519279982d
title: Gestione delle informazioni sui domini attendibili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a945705efaedf56920ee2170deeab9da0d01802259a57aca5cda2fac9d531aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894091"
---
# <a name="managing-trusted-domain-information"></a>Gestione delle informazioni sui domini attendibili

I criteri LSA forniscono diverse funzioni che è possibile usare per creare, enumerare ed eliminare domini trusted e per impostare e recuperare informazioni sui domini trusted.

Prima di poter gestire le informazioni sul dominio trusted, l'applicazione deve ottenere un handle per un oggetto [**Criteri,**](policy-object.md) come illustrato in Apertura di un handle [di oggetto criteri](opening-a-policy-object-handle.md).

È possibile enumerare i domini trusted chiamando [**LsaEnumerateTrustedDomainsEx.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex)

Per recuperare informazioni su un dominio trusted, chiamare [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo) o [**LsaQueryTrustedDomainInfoByName.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname) Entrambe le funzioni restituiscono le stesse informazioni. Tuttavia, **LsaQueryTrustedDomainInfo** identifica il dominio trusted in base al SID e **LsaQueryTrustedDomainInfoByName** identifica il dominio trusted in base al nome.

Per impostare le informazioni per un dominio trusted, chiamare [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation) o [**LsaSetTrustedDomainInfoByName.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname) Come per le funzioni di query, **LsaSetTrustedDomainInformation** identifica il dominio trusted in base al SID, mentre **LsaSetTrustedDomainInfoByName** identifica il dominio trusted in base al nome.

L'applicazione può revocare una relazione di trust per un dominio trusted chiamando [**LsaDeleteTrustedDomain.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain)

Nell'esempio seguente vengono enumerati i domini trusted per il sistema locale.


```C++
#include <windows.h>

void EnumerateTrusts(LSA_HANDLE PolicyHandle)
{
  LSA_ENUMERATION_HANDLE hEnum=0; 
  PLSA_TRUST_INFORMATION TrustInfo = NULL;
  ULONG ulReturned = 0;               
  NTSTATUS Status = 0;
  ULONG i;
  WCHAR StringBuffer[256];

  // Enumerate the trusted domains until there are no more to return.
  do 
  {
    Status = LsaEnumerateTrustedDomains(
       PolicyHandle,         // an open policy handle
       &hEnum,               // enumeration tracker
       (PVOID*)&TrustInfo,   // buffer to receive data
       32000,                // recommended buffer size
       &ulReturned           // number of items returned in TrustInfo
    );

    // Check the return status for errors.
    if((Status != STATUS_SUCCESS) &&
       (Status != STATUS_MORE_ENTRIES) &&
     (Status != STATUS_NO_MORE_ENTRIES))
      {
        // Handle the error.
        wprintf(L"Error occurred enumerating domains %lu\n",
        LsaNtStatusToWinError(Status));
        return;
      } 

      wprintf(L"Status %lu\n", LsaNtStatusToWinError(Status));
      // Process the trusted domain information.
      for (i=0;i<ulReturned; i++) 
      {
        // LSA_Unicode strings might not be null-terminated.
        if(TrustInfo[i].Name.Length < 256)
        {
            wcsncpy_s(StringBuffer,
                256,
                TrustInfo[i].Name.Buffer,
                TrustInfo[i].Name.Length
            );
            // Guarantee that StringBuffer is null-terminated.
            StringBuffer[TrustInfo[i].Name.Length] = NULL; 
        }
        else
        {
            fprintf(stderr, "Name too long for string buffer.\n");
            exit(1);
        }
        
        wprintf(L"Enum Trusted Domain - %ws ", StringBuffer);
      }
      // Free the buffer.
      if (TrustInfo != NULL) 
      {
        LsaFreeMemory(TrustInfo);
        TrustInfo = NULL;
      }
    } while (Status != STATUS_NO_MORE_ENTRIES);
    return;
}
```



 

 



