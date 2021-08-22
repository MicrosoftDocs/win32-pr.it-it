---
description: L'autorità di sicurezza locale (LSA) fornisce funzioni per la conversione tra i nomi di utenti, gruppi e gruppi locali e i valori corrispondenti dell'identificatore di sicurezza (SID).
ms.assetid: 8845b709-a8f9-4d0f-a4a6-86d23d6b01d5
title: Traduzione tra nomi e SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d5f67bd95e41a9813522d635e737f4fc528a61aebceeab205a2d40e1f44d7c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004809"
---
# <a name="translating-between-names-and-sids"></a>Traduzione tra nomi e SID

[*L'autorità di sicurezza*](/windows/desktop/SecGloss/l-gly) locale (LSA) fornisce funzioni per la conversione tra nomi di utenti, gruppi e gruppi locali e i valori corrispondenti [*dell'identificatore*](/windows/desktop/SecGloss/s-gly) di sicurezza (SID). Per individuare i nomi degli account, chiamare [**la funzione LsaLookupNames.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames) Questa funzione restituisce il SID come coppia di indici RID/dominio. Per ottenere il SID come singolo elemento, chiamare la [**funzione LsaLookupNames2.**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupnames2) Per individuare i SID, chiamare [**LsaLookupSids**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalookupsids).

Queste funzioni possono convertire le informazioni su nome e SID da qualsiasi dominio considerato attendibile dal sistema locale.

Prima di poter eseguire la conversione tra nomi di account e SID, l'applicazione deve ottenere un handle per l'oggetto [**Criteri**](policy-object.md) locale, come illustrato in Apertura di un handle [di oggetto criteri](opening-a-policy-object-handle.md).

L'esempio seguente cerca il SID per un account, dato il nome dell'account.


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



Nell'esempio precedente la funzione **InitLsaString** converte una stringa Unicode in una struttura [**LSA \_ UNICODE \_ STRING.**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) Il codice per questa funzione è illustrato in [Uso di stringhe Unicode LSA.](using-lsa-unicode-strings.md)

> [!Note]  
> Queste funzioni di conversione vengono fornite principalmente per l'uso da parte degli editor di autorizzazioni per [*visualizzare*](/windows/desktop/SecGloss/a-gly) informazioni sull'elenco di controllo di accesso (ACL). Un editor di autorizzazioni deve sempre chiamare queste funzioni usando [**l'oggetto Criteri**](policy-object.md) per il sistema in cui si trova il [*SID*](/windows/desktop/SecGloss/s-gly) del nome o dell'identificatore di sicurezza. Ciò garantisce che durante la conversione si fa riferimento al set appropriato di domini attendibili.

 

Windows Controllo di accesso fornisce anche funzioni che eseguono traduzioni tra SID e nomi di account: [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) e [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida). Se l'applicazione deve cercare un nome di account o un SID e non usa funzionalità aggiuntive dei criteri LSA, usare le funzioni di controllo di accesso Windows anziché le funzioni criteri LSA. Per altre informazioni su queste funzioni, vedere Controllo [di accesso](/windows/desktop/SecAuthZ/access-control).

 

 
