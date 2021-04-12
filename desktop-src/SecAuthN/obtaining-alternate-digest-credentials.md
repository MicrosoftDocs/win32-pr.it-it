---
description: Per ottenere credenziali diverse da quelle associate alla sessione di accesso corrente, popolare una \_ struttura di identità di autenticazione WinNT sec con le \_ \_ informazioni per l'entità di sicurezza alternativa.
ms.assetid: f590ddb5-39a1-4d0c-a787-da938a63c206
title: Acquisizione di credenziali del digest alternative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ed7daa2a3179822929e8c2df8077ee55afaadb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232821"
---
# <a name="obtaining-alternate-digest-credentials"></a><span data-ttu-id="c02c7-103">Acquisizione di credenziali del digest alternative</span><span class="sxs-lookup"><span data-stu-id="c02c7-103">Obtaining Alternate Digest Credentials</span></span>

<span data-ttu-id="c02c7-104">Per ottenere [*credenziali*](../secgloss/c-gly.md) diverse da quelle associate alla [*sessione*](../secgloss/s-gly.md)di accesso corrente, popolare una struttura di [**\_ \_ \_ identità di autenticazione WinNT sec**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) con le informazioni per l' [*entità di sicurezza*](../secgloss/s-gly.md)alternativa.</span><span class="sxs-lookup"><span data-stu-id="c02c7-104">To obtain [*credentials*](../secgloss/c-gly.md) other than those associated with the current logon [*session*](../secgloss/s-gly.md), populate a [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure with information for the alternate [*security principal*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="c02c7-105">Passare la struttura alla funzione [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) utilizzando il parametro *pAuthData* .</span><span class="sxs-lookup"><span data-stu-id="c02c7-105">Pass the structure to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function using the *pAuthData* parameter.</span></span>

<span data-ttu-id="c02c7-106">Nella tabella seguente vengono descritti i membri della struttura di [**\_ \_ \_ identità dell'autenticazione WinNT del secondo**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) .</span><span class="sxs-lookup"><span data-stu-id="c02c7-106">The following table describes the members of the [**SEC\_WINNT\_AUTH\_IDENTITY**](/windows/win32/api/sspi/ns-sspi-sec_winnt_auth_identity_a) structure.</span></span>



| <span data-ttu-id="c02c7-107">Membro</span><span class="sxs-lookup"><span data-stu-id="c02c7-107">Member</span></span>             | <span data-ttu-id="c02c7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c02c7-108">Description</span></span>                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c02c7-109">**Utente**</span><span class="sxs-lookup"><span data-stu-id="c02c7-109">**User**</span></span>           | <span data-ttu-id="c02c7-110">Stringa con terminazione null che contiene il nome dell'entità di sicurezza le cui credenziali verranno utilizzate per stabilire un contesto di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c02c7-110">Null-terminated string containing the name of the security principal whose credentials will be used to establish a security context.</span></span> |
| <span data-ttu-id="c02c7-111">**UserLength**</span><span class="sxs-lookup"><span data-stu-id="c02c7-111">**UserLength**</span></span>     | <span data-ttu-id="c02c7-112">Lunghezza del membro **utente** , in caratteri.</span><span class="sxs-lookup"><span data-stu-id="c02c7-112">The length of the **User** member, in characters.</span></span> <span data-ttu-id="c02c7-113">Omettere il valore null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="c02c7-113">Omit the terminating null.</span></span>                                                         |
| <span data-ttu-id="c02c7-114">**Dominio**</span><span class="sxs-lookup"><span data-stu-id="c02c7-114">**Domain**</span></span>         | <span data-ttu-id="c02c7-115">Stringa con terminazione null che identifica il dominio contenente l'account dell'entità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c02c7-115">Null-terminated string that identifies the domain containing the account of the security principal.</span></span>                                  |
| <span data-ttu-id="c02c7-116">**DomainLength**</span><span class="sxs-lookup"><span data-stu-id="c02c7-116">**DomainLength**</span></span>   | <span data-ttu-id="c02c7-117">Lunghezza del membro del **dominio** , in caratteri.</span><span class="sxs-lookup"><span data-stu-id="c02c7-117">The length of the **Domain** member, in characters.</span></span> <span data-ttu-id="c02c7-118">Omettere il valore null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="c02c7-118">Omit the terminating null.</span></span>                                                       |
| <span data-ttu-id="c02c7-119">**Password**</span><span class="sxs-lookup"><span data-stu-id="c02c7-119">**Password**</span></span>       | <span data-ttu-id="c02c7-120">Stringa con terminazione null che contiene la password dell'entità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="c02c7-120">Null-terminated string containing the password of the security principal.</span></span>                                                            |
| <span data-ttu-id="c02c7-121">**PasswordLength**</span><span class="sxs-lookup"><span data-stu-id="c02c7-121">**PasswordLength**</span></span> | <span data-ttu-id="c02c7-122">Lunghezza del membro della **password** , in caratteri.</span><span class="sxs-lookup"><span data-stu-id="c02c7-122">The length of the **Password** member, in characters.</span></span> <span data-ttu-id="c02c7-123">Omettere il valore null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="c02c7-123">Omit the terminating null.</span></span>                                                     |
| <span data-ttu-id="c02c7-124">**Flag**</span><span class="sxs-lookup"><span data-stu-id="c02c7-124">**Flags**</span></span>          | <span data-ttu-id="c02c7-125">Indica se i membri della stringa sono in formato ANSI o [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c02c7-125">Indicates whether the string members are in ANSI or [*Unicode*](../secgloss/u-gly.md) format.</span></span>  |



 

<span data-ttu-id="c02c7-126">Nella tabella seguente sono elencati i valori validi per il membro dei **flag** della struttura.</span><span class="sxs-lookup"><span data-stu-id="c02c7-126">The following table lists the valid values for the **Flags** member of the structure.</span></span>



| <span data-ttu-id="c02c7-127">Costante</span><span class="sxs-lookup"><span data-stu-id="c02c7-127">Constant</span></span>                            | <span data-ttu-id="c02c7-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c02c7-128">Description</span></span>                                                                                                      |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c02c7-129">SEC \_ \_ identità auth \_ autenticazione \_ ANSI</span><span class="sxs-lookup"><span data-stu-id="c02c7-129">SEC\_WINNT\_AUTH\_IDENTITY\_ANSI</span></span>    | <span data-ttu-id="c02c7-130">Le stringhe in questa struttura sono in formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="c02c7-130">Strings in this structure are in ANSI format.</span></span>                                                                    |
| <span data-ttu-id="c02c7-131">SEC \_ identità di autenticazione WinNT ( \_ \_ \_ Unicode)</span><span class="sxs-lookup"><span data-stu-id="c02c7-131">SEC\_WINNT\_AUTH\_IDENTITY\_UNICODE</span></span> | <span data-ttu-id="c02c7-132">Le stringhe in questa struttura sono in formato [*Unicode*](../secgloss/u-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c02c7-132">Strings in this structure are in [*Unicode*](../secgloss/u-gly.md) format.</span></span> |



 

<span data-ttu-id="c02c7-133">La struttura e le costanti sono dichiarate nel file di intestazione rpcdce. h distribuito con Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="c02c7-133">The structure and constants are declared in the Rpcdce.h header file distributed with the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="c02c7-134">Nell'esempio seguente viene illustrata una chiamata sul lato client per ottenere le credenziali del digest per un account utente specifico.</span><span class="sxs-lookup"><span data-stu-id="c02c7-134">The following example demonstrates a client-side call to obtain Digest credentials for a specific user account.</span></span>


```C++
#include <windows.h>

#ifdef UNICODE
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;
#else
  ClientAuthID.Flags = SEC_WINNT_AUTH_IDENTITY_ANSI;
#endif

void main()
{
    SECURITY_STATUS SecStatus; 
    TimeStamp tsLifetime; 
    CredHandle hCred;
    SEC_WINNT_AUTH_IDENTITY ClientAuthID;
    LPTSTR UserName = TEXT("ASecurityPrinciple");
    LPTSTR DomainName = TEXT("AnAuthenticatingDomain");

    // Initialize the memory.
    ZeroMemory( &ClientAuthID, sizeof(ClientAuthID) );

    // Specify string format for the ClientAuthID structure.


    // Specify an alternate user, domain and password.
      ClientAuthID.User = (unsigned char *) UserName;
      ClientAuthID.UserLength = _tcslen(UserName);

      ClientAuthID.Domain = (unsigned char *) DomainName;
      ClientAuthID.DomainLength = _tcslen(DomainName);

    // Password is an application-defined LPTSTR variable
    // containing the user password.
      ClientAuthID.Password = Password;
      ClientAuthID.PasswordLength = _tcslen(Password);

    // Get the client side credential handle.
    SecStatus = AcquireCredentialsHandle (
      NULL,                  // Default principal.
      WDIGEST_SP_NAME,       // The Digest SSP. 
      SECPKG_CRED_OUTBOUND,  // Client will use the credentials.
      NULL,                  // Do not specify LOGON id.
      &ClientAuthID,         // User information.
      NULL,                  // Not used with Digest SSP.
      NULL,                  // Not used with Digest SSP.
      &hCred,                // Receives the credential handle.
      &tsLifetime            // Receives the credential time limit.
    );
}
```



<span data-ttu-id="c02c7-135">La funzione **\_ tcslen** restituisce la lunghezza della stringa in caratteri, escluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="c02c7-135">The **\_tcslen** function returns the string length in characters, not including the terminating null character.</span></span>

<span data-ttu-id="c02c7-136">Se l'applicazione può usare le credenziali stabilite all'accesso, vedere [recupero delle credenziali del digest predefinite](obtaining-default-digest-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="c02c7-136">If your application can use the credentials established at logon, see [Obtaining Default Digest Credentials](obtaining-default-digest-credentials.md).</span></span>

 

 
