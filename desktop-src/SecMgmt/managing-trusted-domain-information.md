---
description: I criteri LSA forniscono diverse funzioni che è possibile utilizzare per creare, enumerare ed eliminare domini trusted e per impostare e recuperare informazioni sul dominio attendibile.
ms.assetid: 0c7534d7-3372-49c4-992c-9b519279982d
title: Gestione delle informazioni di dominio trusted
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7df297b8c83ebe9054ca6f04b657905c21fae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233120"
---
# <a name="managing-trusted-domain-information"></a><span data-ttu-id="a8118-103">Gestione delle informazioni di dominio trusted</span><span class="sxs-lookup"><span data-stu-id="a8118-103">Managing Trusted Domain Information</span></span>

<span data-ttu-id="a8118-104">I criteri LSA forniscono diverse funzioni che è possibile utilizzare per creare, enumerare ed eliminare domini trusted e per impostare e recuperare informazioni sul dominio attendibile.</span><span class="sxs-lookup"><span data-stu-id="a8118-104">LSA Policy provides several functions that you can use to create, enumerate, and delete trusted domains and to set and retrieve trusted domain information.</span></span>

<span data-ttu-id="a8118-105">Prima di poter gestire le informazioni sul dominio trusted, l'applicazione deve ottenere un handle per un oggetto [**criteri**](policy-object.md) , come illustrato in [apertura di un handle di oggetto Criteri](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="a8118-105">Before you can manage trusted domain information, your application must get a handle to a [**Policy**](policy-object.md) object, as explained in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="a8118-106">È possibile enumerare i domini trusted chiamando [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span><span class="sxs-lookup"><span data-stu-id="a8118-106">You can enumerate the trusted domains by calling [**LsaEnumerateTrustedDomainsEx**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex).</span></span>

<span data-ttu-id="a8118-107">Per recuperare informazioni su un dominio trusted, chiamare [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo) o [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname).</span><span class="sxs-lookup"><span data-stu-id="a8118-107">To retrieve information about a trusted domain, call either [**LsaQueryTrustedDomainInfo**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo) or [**LsaQueryTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfobyname).</span></span> <span data-ttu-id="a8118-108">Entrambe le funzioni restituiscono le stesse informazioni; Tuttavia, **LsaQueryTrustedDomainInfo** identifica il dominio trusted per SID e **LsaQueryTrustedDomainInfoByName** identifica il dominio trusted in base al nome.</span><span class="sxs-lookup"><span data-stu-id="a8118-108">Both functions return the same information; however, **LsaQueryTrustedDomainInfo** identifies the trusted domain by SID, and **LsaQueryTrustedDomainInfoByName** identifies the trusted domain by name.</span></span>

<span data-ttu-id="a8118-109">Per impostare informazioni per un dominio trusted, chiamare [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation) o [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname).</span><span class="sxs-lookup"><span data-stu-id="a8118-109">To set information for a trusted domain, call either [**LsaSetTrustedDomainInformation**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation) or [**LsaSetTrustedDomainInfoByName**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsasettrusteddomaininfobyname).</span></span> <span data-ttu-id="a8118-110">Come per le funzioni di query, **LsaSetTrustedDomainInformation** identifica il dominio trusted per SID, mentre **LsaSetTrustedDomainInfoByName** identifica il dominio trusted in base al nome.</span><span class="sxs-lookup"><span data-stu-id="a8118-110">As with the query functions, **LsaSetTrustedDomainInformation** identifies the trusted domain by SID, while **LsaSetTrustedDomainInfoByName** identifies the trusted domain by name.</span></span>

<span data-ttu-id="a8118-111">L'applicazione può revocare una relazione di trust per un dominio trusted chiamando [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain).</span><span class="sxs-lookup"><span data-stu-id="a8118-111">Your application can revoke a trust relationship for a trusted domain by calling [**LsaDeleteTrustedDomain**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsadeletetrusteddomain).</span></span>

<span data-ttu-id="a8118-112">Nell'esempio seguente vengono enumerati i domini trusted per il sistema locale.</span><span class="sxs-lookup"><span data-stu-id="a8118-112">The following example enumerates the trusted domains for the local system.</span></span>


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



 

 



