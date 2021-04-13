---
description: In LSA sono disponibili diverse funzioni che possono essere chiamate dalle applicazioni per enumerare o impostare i privilegi per gli account di gruppo utente, gruppo e locale.
ms.assetid: c28c03f0-4638-42ed-8dad-1e934cf99273
title: Gestione delle autorizzazioni dell'account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4dc22a4088986abbdaa98d8cdde43415af84905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484588"
---
# <a name="managing-account-permissions"></a>Gestione delle autorizzazioni dell'account

In LSA sono disponibili diverse funzioni che possono essere chiamate dalle applicazioni per enumerare o impostare i [*privilegi*](/windows/desktop/SecGloss/p-gly) per gli account di gruppo utente, gruppo e locale.

Prima di poter gestire le informazioni sull'account, l'applicazione deve ottenere un handle per l'oggetto [**criteri**](policy-object.md) locale, come illustrato in [apertura di un handle di oggetto Criteri](opening-a-policy-object-handle.md). Per enumerare o modificare le autorizzazioni per un account, è inoltre necessario disporre dell' [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) per l'account. L'applicazione può individuare un SID dato il nome dell'account, come descritto in [traduzione tra nomi e SID](translating-between-names-and-sids.md).

Per accedere a tutti gli account che dispongono di un'autorizzazione specifica, chiamare [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright). Questa funzione popola una matrice con i SID di tutti gli account che dispongono dell'autorizzazione specificata.

Una volta ottenuto il SID di un account, è possibile modificarne le autorizzazioni. Chiamare [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) per aggiungere le autorizzazioni all'account. Se l'account specificato non esiste, **LsaAddAccountRights** lo crea. Per rimuovere le autorizzazioni da un account, chiamare [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights). Se si rimuovono tutte le autorizzazioni da un account, **LsaRemoveAccountRights** Elimina anche l'account.

L'applicazione può verificare le autorizzazioni attualmente assegnate a un account chiamando [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights). Questa funzione popola una matrice di strutture [**di \_ \_ stringhe Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . Ogni struttura contiene il nome di un privilegio utilizzato dall'account specificato.

Nell'esempio seguente viene aggiunta l'autorizzazione SeServiceLogonRight a un account. In questo esempio, la variabile AccountSID specifica il SID dell'account. Per ulteriori informazioni su come eseguire la ricerca di un SID di account, vedere la pagina relativa alla [conversione tra nomi e SID](translating-between-names-and-sids.md).


```C++
#include <windows.h>
#include <ntsecapi.h>

void AddPrivileges(PSID AccountSID, LSA_HANDLE PolicyHandle)
{
  LSA_UNICODE_STRING lucPrivilege;
  NTSTATUS ntsResult;

  // Create an LSA_UNICODE_STRING for the privilege names.
  if (!InitLsaString(&lucPrivilege, L"SeServiceLogonRight"))
  {
         wprintf(L"Failed InitLsaString\n");
         return;
  }

  ntsResult = LsaAddAccountRights(
    PolicyHandle,  // An open policy handle.
    AccountSID,    // The target SID.
    &lucPrivilege, // The privileges.
    1              // Number of privileges.
  );                
  if (ntsResult == STATUS_SUCCESS) 
  {
    wprintf(L"Privilege added.\n");
  }
  else
  {
    wprintf(L"Privilege was not added - %lu \n",
      LsaNtStatusToWinError(ntsResult));
  }
} 
```



Nell'esempio precedente la funzione InitLsaString converte una stringa [*Unicode*](/windows/desktop/SecGloss/u-gly) in una struttura di [**\_ \_ stringhe Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) . Il codice per questa funzione è illustrato in [uso di stringhe Unicode LSA](using-lsa-unicode-strings.md).

 

 
