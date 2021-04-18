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
# <a name="translating-between-names-and-sids"></a>Conversione tra nomi e SID

L' [*autorità di sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA) fornisce funzioni per la conversione tra i nomi di utenti, gruppi e gruppi locali e i relativi valori [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) corrispondenti. Per individuare i nomi di account, chiamare la funzione [**LsaLookupNames**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) . Questa funzione restituisce il SID come coppia di indice RID/dominio. Per ottenere il SID come singolo elemento, chiamare la funzione [**LsaLookupNames2**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) . Per individuare i SID, chiamare [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).

Queste funzioni possono tradurre le informazioni sul nome e sul SID da qualsiasi dominio ritenuto attendibile dal sistema locale.

Prima di poter eseguire la conversione tra i nomi di account e i SID, l'applicazione deve ottenere un handle per l'oggetto [**criteri**](policy-object.md) locale, come illustrato in [apertura di un handle di oggetto Criteri](opening-a-policy-object-handle.md).

Nell'esempio seguente viene ricercato il SID di un account, dato il nome dell'account.


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



Nell'esempio precedente la funzione **InitLsaString** converte una stringa Unicode in una struttura di [**\_ \_ stringhe Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . Il codice per questa funzione è illustrato in [uso di stringhe Unicode LSA](using-lsa-unicode-strings.md).

> [!Note]  
> Queste funzioni di conversione vengono fornite principalmente dagli editor di autorizzazioni per visualizzare le informazioni relative all' [*elenco di controllo di accesso*](/windows/desktop/SecGloss/a-gly) (ACL). Un editor di autorizzazioni deve sempre chiamare queste funzioni utilizzando l'oggetto [**criteri**](policy-object.md) per il sistema in cui si trova il nome o il SID dell' [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) . Ciò garantisce che durante la traduzione venga fatto riferimento al set appropriato di domini trusted.

 

Controllo di accesso di Windows fornisce anche funzioni che eseguono traduzioni tra SID e nomi di account: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) e [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida). Se l'applicazione deve cercare un nome di account o un SID e non usa funzionalità di criteri LSA aggiuntive, usare le funzioni di controllo di accesso di Windows invece delle funzioni dei criteri LSA. Per altre informazioni su queste funzioni, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control).

 

 
