---
description: L'autorità di sicurezza locale (LSA) fornisce funzioni per la conversione tra i nomi di utenti, gruppi e gruppi locali e i relativi valori ID di sicurezza (SID) corrispondenti.
ms.assetid: 8845b709-a8f9-4d0f-a4a6-86d23d6b01d5
title: Conversione tra nomi e SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417034a99331c09f20546f2f352bc762a86f02e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306415"
---
# <a name="translating-between-names-and-sids"></a><span data-ttu-id="c598f-103">Conversione tra nomi e SID</span><span class="sxs-lookup"><span data-stu-id="c598f-103">Translating Between Names and SIDs</span></span>

<span data-ttu-id="c598f-104">L' [*autorità di sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA) fornisce funzioni per la conversione tra i nomi di utenti, gruppi e gruppi locali e i relativi valori [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="c598f-104">The [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) provides functions to translate between user, group, and local group names and their corresponding [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) values.</span></span> <span data-ttu-id="c598f-105">Per individuare i nomi di account, chiamare la funzione [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) .</span><span class="sxs-lookup"><span data-stu-id="c598f-105">To locate account names, call the [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) function.</span></span> <span data-ttu-id="c598f-106">Questa funzione restituisce il SID come coppia di indice RID/dominio.</span><span class="sxs-lookup"><span data-stu-id="c598f-106">This function returns the SID as a RID/Domain index pair.</span></span> <span data-ttu-id="c598f-107">Per ottenere il SID come singolo elemento, chiamare la funzione [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) .</span><span class="sxs-lookup"><span data-stu-id="c598f-107">To get the SID as a single element, call the [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) function.</span></span> <span data-ttu-id="c598f-108">Per individuare i SID, chiamare [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).</span><span class="sxs-lookup"><span data-stu-id="c598f-108">To locate SIDs, call [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).</span></span>

<span data-ttu-id="c598f-109">Queste funzioni possono tradurre le informazioni sul nome e sul SID da qualsiasi dominio ritenuto attendibile dal sistema locale.</span><span class="sxs-lookup"><span data-stu-id="c598f-109">These functions can translate name and SID information from any domain trusted by the local system.</span></span>

<span data-ttu-id="c598f-110">Prima di poter eseguire la conversione tra i nomi di account e i SID, l'applicazione deve ottenere un handle per l'oggetto [**criteri**](policy-object.md) locale, come illustrato in [apertura di un handle di oggetto Criteri](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="c598f-110">Before you can translate between account names and SIDs, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span>

<span data-ttu-id="c598f-111">Nell'esempio seguente viene ricercato il SID di un account, dato il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="c598f-111">The following example looks up the SID for an account, given the account name.</span></span>


```C++
void GetSIDInformation (LPWSTR AccountName,LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucName;
  PLSA_TRANSLATED_SID ltsTranslatedSID;
  PLSA_REFERENCED_DOMAIN_LIST lrdlDomainList;
  LSA_TRUST_INFORMATION myDomain;
  NTSTATUS ntsResult;
  PWCHAR DomainString = NULL;

  // Initialize an LSA_UNICODE_STRING with the name.
  if (!InitLsaString(&lucName, AccountName))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaLookupNames(
     PolicyHandle,     // handle to a Policy object
     1,                // number of names to look up
     &lucName,         // pointer to an array of names
     &lrdlDomainList,  // receives domain information
     &ltsTranslatedSID // receives relative SIDs
  );
  if (STATUS_SUCCESS != ntsResult) 
  {
    wprintf(L"Failed LsaLookupNames - %lu \n",
      LsaNtStatusToWinError(ntsResult));
    return;
  }

  // Get the domain the account resides in.
  myDomain = lrdlDomainList->Domains[ltsTranslatedSID->DomainIndex];
  DomainString = (PWCHAR) LocalAlloc(LPTR, myDomain.Name.Length + 1);
  wcsncpy_s(DomainString,
     myDomain.Name.Length + 1, 
     myDomain.Name.Buffer, 
     myDomain.Name.Length);

  // Display the relative Id. 
  wprintf(L"Relative Id is %lu in domain %ws.\n",
    ltsTranslatedSID->RelativeId,
    DomainString);

  LocalFree(DomainString);
  LsaFreeMemory(ltsTranslatedSID);
  LsaFreeMemory(lrdlDomainList);
}
```



<span data-ttu-id="c598f-112">Nell'esempio precedente la funzione **InitLsaString** converte una stringa Unicode in una struttura di [**\_ \_ stringhe Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="c598f-112">In the preceding example, the function **InitLsaString** converts a Unicode string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="c598f-113">Il codice per questa funzione è illustrato in [uso di stringhe Unicode LSA](using-lsa-unicode-strings.md).</span><span class="sxs-lookup"><span data-stu-id="c598f-113">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>

> [!Note]  
> <span data-ttu-id="c598f-114">Queste funzioni di conversione vengono fornite principalmente dagli editor di autorizzazioni per visualizzare le informazioni relative all' [*elenco di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL).</span><span class="sxs-lookup"><span data-stu-id="c598f-114">These translation functions are primarily provided for use by permissions editors to display [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) information.</span></span> <span data-ttu-id="c598f-115">Un editor di autorizzazioni deve sempre chiamare queste funzioni utilizzando l'oggetto [**criteri**](policy-object.md) per il sistema in cui si trova il nome o il SID dell' [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) .</span><span class="sxs-lookup"><span data-stu-id="c598f-115">A permission editor should always call these functions using the [**Policy**](policy-object.md) object for the system where the name or [*security identifier*](/windows/desktop/SecGloss/s-gly) SID is located.</span></span> <span data-ttu-id="c598f-116">Ciò garantisce che durante la traduzione venga fatto riferimento al set appropriato di domini trusted.</span><span class="sxs-lookup"><span data-stu-id="c598f-116">This ensures that the proper set of trusted domains is referenced during the translation.</span></span>

 

<span data-ttu-id="c598f-117">Controllo di accesso di Windows fornisce anche funzioni che eseguono traduzioni tra SID e nomi di account: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) e [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida).</span><span class="sxs-lookup"><span data-stu-id="c598f-117">Windows Access Control also provides functions that perform translations between SIDs and account names: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) and [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida).</span></span> <span data-ttu-id="c598f-118">Se l'applicazione deve cercare un nome di account o un SID e non usa funzionalità di criteri LSA aggiuntive, usare le funzioni di controllo di accesso di Windows invece delle funzioni dei criteri LSA.</span><span class="sxs-lookup"><span data-stu-id="c598f-118">If your application needs to look up an account name or SID and does not use additional LSA Policy functionality, use the Windows Access Control functions instead of the LSA Policy functions.</span></span> <span data-ttu-id="c598f-119">Per altre informazioni su queste funzioni, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="c598f-119">For more information about these functions, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

 

 
