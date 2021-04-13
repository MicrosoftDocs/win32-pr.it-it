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
# <a name="managing-account-permissions"></a><span data-ttu-id="ebf49-103">Gestione delle autorizzazioni dell'account</span><span class="sxs-lookup"><span data-stu-id="ebf49-103">Managing Account Permissions</span></span>

<span data-ttu-id="ebf49-104">In LSA sono disponibili diverse funzioni che possono essere chiamate dalle applicazioni per enumerare o impostare i [*privilegi*](/windows/desktop/SecGloss/p-gly) per gli account di gruppo utente, gruppo e locale.</span><span class="sxs-lookup"><span data-stu-id="ebf49-104">The LSA provides several functions that applications can call to enumerate or set [*privileges*](/windows/desktop/SecGloss/p-gly) for user, group, and local group accounts.</span></span>

<span data-ttu-id="ebf49-105">Prima di poter gestire le informazioni sull'account, l'applicazione deve ottenere un handle per l'oggetto [**criteri**](policy-object.md) locale, come illustrato in [apertura di un handle di oggetto Criteri](opening-a-policy-object-handle.md).</span><span class="sxs-lookup"><span data-stu-id="ebf49-105">Before you can manage account information, your application must get a handle to the local [**Policy**](policy-object.md) object, as demonstrated in [Opening a Policy Object Handle](opening-a-policy-object-handle.md).</span></span> <span data-ttu-id="ebf49-106">Per enumerare o modificare le autorizzazioni per un account, è inoltre necessario disporre dell' [*ID di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) per l'account.</span><span class="sxs-lookup"><span data-stu-id="ebf49-106">In addition, to enumerate or edit permissions for an account, you must have the [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) for that account.</span></span> <span data-ttu-id="ebf49-107">L'applicazione può individuare un SID dato il nome dell'account, come descritto in [traduzione tra nomi e SID](translating-between-names-and-sids.md).</span><span class="sxs-lookup"><span data-stu-id="ebf49-107">Your application can locate a SID given the account name, as described in [Translating Between Names and SIDs](translating-between-names-and-sids.md).</span></span>

<span data-ttu-id="ebf49-108">Per accedere a tutti gli account che dispongono di un'autorizzazione specifica, chiamare [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright).</span><span class="sxs-lookup"><span data-stu-id="ebf49-108">To access all accounts that have a particular permission, call [**LsaEnumerateAccountsWithUserRight**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright).</span></span> <span data-ttu-id="ebf49-109">Questa funzione popola una matrice con i SID di tutti gli account che dispongono dell'autorizzazione specificata.</span><span class="sxs-lookup"><span data-stu-id="ebf49-109">This function populates an array with the SIDs of all accounts that have the specified permission.</span></span>

<span data-ttu-id="ebf49-110">Una volta ottenuto il SID di un account, è possibile modificarne le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="ebf49-110">After you have obtained the SID of an account, you can modify its permissions.</span></span> <span data-ttu-id="ebf49-111">Chiamare [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) per aggiungere le autorizzazioni all'account.</span><span class="sxs-lookup"><span data-stu-id="ebf49-111">Call [**LsaAddAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaaddaccountrights) to add permissions to the account.</span></span> <span data-ttu-id="ebf49-112">Se l'account specificato non esiste, **LsaAddAccountRights** lo crea.</span><span class="sxs-lookup"><span data-stu-id="ebf49-112">If the specified account does not exist, **LsaAddAccountRights** creates it.</span></span> <span data-ttu-id="ebf49-113">Per rimuovere le autorizzazioni da un account, chiamare [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights).</span><span class="sxs-lookup"><span data-stu-id="ebf49-113">To remove permissions from an account, call [**LsaRemoveAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaremoveaccountrights).</span></span> <span data-ttu-id="ebf49-114">Se si rimuovono tutte le autorizzazioni da un account, **LsaRemoveAccountRights** Elimina anche l'account.</span><span class="sxs-lookup"><span data-stu-id="ebf49-114">If you remove all permissions from an account, **LsaRemoveAccountRights** also deletes the account.</span></span>

<span data-ttu-id="ebf49-115">L'applicazione può verificare le autorizzazioni attualmente assegnate a un account chiamando [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights).</span><span class="sxs-lookup"><span data-stu-id="ebf49-115">Your application can check the permissions currently assigned to an account by calling [**LsaEnumerateAccountRights**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsaenumerateaccountrights).</span></span> <span data-ttu-id="ebf49-116">Questa funzione popola una matrice di strutture [**di \_ \_ stringhe Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="ebf49-116">This function populates an array of [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structures.</span></span> <span data-ttu-id="ebf49-117">Ogni struttura contiene il nome di un privilegio utilizzato dall'account specificato.</span><span class="sxs-lookup"><span data-stu-id="ebf49-117">Each structure contains the name of a privilege held by the specified account.</span></span>

<span data-ttu-id="ebf49-118">Nell'esempio seguente viene aggiunta l'autorizzazione SeServiceLogonRight a un account.</span><span class="sxs-lookup"><span data-stu-id="ebf49-118">The following example adds the SeServiceLogonRight permission to an account.</span></span> <span data-ttu-id="ebf49-119">In questo esempio, la variabile AccountSID specifica il SID dell'account.</span><span class="sxs-lookup"><span data-stu-id="ebf49-119">In this example, the AccountSID variable specifies the SID of the account.</span></span> <span data-ttu-id="ebf49-120">Per ulteriori informazioni su come eseguire la ricerca di un SID di account, vedere la pagina relativa alla [conversione tra nomi e SID](translating-between-names-and-sids.md).</span><span class="sxs-lookup"><span data-stu-id="ebf49-120">For more information about how to lookup an account SID, see [Translating Between Names and SIDs](translating-between-names-and-sids.md).</span></span>


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



<span data-ttu-id="ebf49-121">Nell'esempio precedente la funzione InitLsaString converte una stringa [*Unicode*](/windows/desktop/SecGloss/u-gly) in una struttura di [**\_ \_ stringhe Unicode LSA**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) .</span><span class="sxs-lookup"><span data-stu-id="ebf49-121">In the preceding example, the function InitLsaString converts a [*Unicode*](/windows/desktop/SecGloss/u-gly) string to an [**LSA\_UNICODE\_STRING**](/windows/desktop/api/lsalookup/ns-lsalookup-lsa_unicode_string) structure.</span></span> <span data-ttu-id="ebf49-122">Il codice per questa funzione è illustrato in [uso di stringhe Unicode LSA](using-lsa-unicode-strings.md).</span><span class="sxs-lookup"><span data-stu-id="ebf49-122">The code for this function is shown in [Using LSA Unicode Strings](using-lsa-unicode-strings.md).</span></span>

 

 
