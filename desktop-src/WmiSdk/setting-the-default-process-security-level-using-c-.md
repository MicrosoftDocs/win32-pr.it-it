---
description: Quando un'applicazione client accede per la prima volta a Strumentazione gestione Windows (WMI), deve impostare il livello di sicurezza del processo predefinito con una chiamata a CoInitializeSecurity.
ms.assetid: 4248fd1b-0867-40d8-8c9c-541156212df8
ms.tgt_platform: multiple
title: Impostazione del livello di sicurezza del processo predefinito mediante C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33bb51deb2c228f0958209c774e7526b4eeed958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530133"
---
# <a name="setting-the-default-process-security-level-using-c"></a><span data-ttu-id="87f8b-103">Impostazione del livello di sicurezza del processo predefinito mediante C++</span><span class="sxs-lookup"><span data-stu-id="87f8b-103">Setting the Default Process Security Level Using C++</span></span>

<span data-ttu-id="87f8b-104">Quando un'applicazione client accede per la prima volta a Strumentazione gestione Windows (WMI), deve impostare il livello di sicurezza del processo predefinito con una chiamata a [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="87f8b-104">When a client application logs on to Windows Management Instrumentation (WMI) for the first time, it must set the default process security level with a call to [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="87f8b-105">COM utilizza le informazioni della chiamata per determinare la sicurezza che un altro processo deve avere per accedere al processo dell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="87f8b-105">COM uses the information in the call to determine how much security another process must have to access the client application process.</span></span>

<span data-ttu-id="87f8b-106">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="87f8b-106">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="87f8b-107">Modifica delle credenziali di autenticazione predefinite con C++</span><span class="sxs-lookup"><span data-stu-id="87f8b-107">Changing the Default Authentication Credentials Using C++</span></span>](#changing-the-default-authentication-credentials-using-c)
-   [<span data-ttu-id="87f8b-108">Modifica dei livelli di rappresentazione predefiniti con C++</span><span class="sxs-lookup"><span data-stu-id="87f8b-108">Changing the Default Impersonation Levels Using C++</span></span>](#changing-the-default-impersonation-levels-using-c)

<span data-ttu-id="87f8b-109">Per la maggior parte delle applicazioni client, gli argomenti illustrati nell'esempio seguente impostano la sicurezza predefinita per WMI.</span><span class="sxs-lookup"><span data-stu-id="87f8b-109">For most client applications the arguments shown in the following example set the default security for WMI.</span></span>


```C++
HRESULT hr = NULL;
hr = CoInitializeSecurity(
        NULL,                       // security descriptor
       -1,                          // use this simple setting
       NULL,                        // use this simple setting
       NULL,                        // reserved
       RPC_C_AUTHN_LEVEL_DEFAULT,   // authentication level  
       RPC_C_IMP_LEVEL_IMPERSONATE, // impersonation level
       NULL,                        // use this simple setting
       EOAC_NONE,                   // no special capabilities
       NULL);                          // reserved

if (FAILED(hr))
{
  CoUninitialize();
  cout << "Failed to initialize security. Error code = 0x"
       << hex << hr << endl;
  return;
}
```



<span data-ttu-id="87f8b-110">Il codice richiede i riferimenti seguenti e le \# istruzioni include per la compilazione corretta.</span><span class="sxs-lookup"><span data-stu-id="87f8b-110">The code requires the following references and \#include statements to compile correctly.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")
```



<span data-ttu-id="87f8b-111">L'impostazione del livello di autenticazione sul **\_ \_ \_ \_ valore predefinito del livello di autenticazione RPC C** consente a DCOM di negoziare il livello di autenticazione in modo che corrisponda alle richieste di sicurezza del computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="87f8b-111">Setting the authentication level to **RPC\_C\_AUTHN\_LEVEL\_DEFAULT** allows DCOM to negotiate the authentication level to match the security demands of the target computer.</span></span> <span data-ttu-id="87f8b-112">Per altre informazioni, vedere [modifica delle credenziali di autenticazione predefinite con c++](#changing-the-default-authentication-credentials-using-c) e [modifica delle impostazioni di rappresentazione predefinite con c++](#changing-the-default-impersonation-levels-using-c).</span><span class="sxs-lookup"><span data-stu-id="87f8b-112">For more information, see [Changing the Default Authentication Credentials Using C++](#changing-the-default-authentication-credentials-using-c) and [Changing the Default Impersonation Settings Using C++](#changing-the-default-impersonation-levels-using-c).</span></span>

## <a name="changing-the-default-authentication-credentials-using-c"></a><span data-ttu-id="87f8b-113">Modifica delle credenziali di autenticazione predefinite con C++</span><span class="sxs-lookup"><span data-stu-id="87f8b-113">Changing the Default Authentication Credentials Using C++</span></span>

<span data-ttu-id="87f8b-114">Le credenziali di autenticazione predefinite funzionano per la maggior parte delle situazioni, ma potrebbe essere necessario usare credenziali di autenticazione diverse in situazioni diverse.</span><span class="sxs-lookup"><span data-stu-id="87f8b-114">The default authentication credentials work for most situations, but you might need to use different authentication credentials in different situations.</span></span> <span data-ttu-id="87f8b-115">Ad esempio, potrebbe essere necessario aggiungere la crittografia alle procedure di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="87f8b-115">For example, you might want to add encryption to the authentication procedures.</span></span>

<span data-ttu-id="87f8b-116">Nella tabella seguente sono elencati e descritti i diversi livelli di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="87f8b-116">The following table lists and describes the different levels of authentication.</span></span>



| <span data-ttu-id="87f8b-117">Livello di autenticazione</span><span class="sxs-lookup"><span data-stu-id="87f8b-117">Authentication level</span></span>                 | <span data-ttu-id="87f8b-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87f8b-118">Description</span></span>                                                                           |
|--------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="87f8b-119">\_ \_ \_ valore predefinito del livello auth C RPC \_</span><span class="sxs-lookup"><span data-stu-id="87f8b-119">RPC\_C\_AUTHN\_LEVEL\_DEFAULT</span></span>        | <span data-ttu-id="87f8b-120">Autenticazione di sicurezza predefinita.</span><span class="sxs-lookup"><span data-stu-id="87f8b-120">Default security authentication.</span></span>                                                      |
| <span data-ttu-id="87f8b-121">\_ \_ livello auth C \_ RPC \_</span><span class="sxs-lookup"><span data-stu-id="87f8b-121">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           | <span data-ttu-id="87f8b-122">Nessuna autenticazione.</span><span class="sxs-lookup"><span data-stu-id="87f8b-122">No authentication.</span></span>                                                                    |
| <span data-ttu-id="87f8b-123">\_connessione a \_ livello auth \_ C \_ RPC</span><span class="sxs-lookup"><span data-stu-id="87f8b-123">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        | <span data-ttu-id="87f8b-124">Autenticazione solo quando il client crea una relazione con il server.</span><span class="sxs-lookup"><span data-stu-id="87f8b-124">Authentication only when the client creates a relationship with the server.</span></span>           |
| <span data-ttu-id="87f8b-125">\_chiamata al \_ livello auth \_ C \_ RPC</span><span class="sxs-lookup"><span data-stu-id="87f8b-125">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           | <span data-ttu-id="87f8b-126">Autenticazione ogni volta che il server riceve una chiamata RPC.</span><span class="sxs-lookup"><span data-stu-id="87f8b-126">Authentication each time the server receives an RPC.</span></span>                                  |
| <span data-ttu-id="87f8b-127">\_ \_ \_ PKT livello auth C RPC \_</span><span class="sxs-lookup"><span data-stu-id="87f8b-127">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            | <span data-ttu-id="87f8b-128">Autenticazione ogni volta che il server riceve i dati da un client.</span><span class="sxs-lookup"><span data-stu-id="87f8b-128">Authentication each time the server receives data from a client.</span></span>                      |
| <span data-ttu-id="87f8b-129">\_ \_ \_ integrità PKT del livello auth \_ C \_ RPC</span><span class="sxs-lookup"><span data-stu-id="87f8b-129">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> | <span data-ttu-id="87f8b-130">Autenticazione che non sono stati modificati dati dal pacchetto.</span><span class="sxs-lookup"><span data-stu-id="87f8b-130">Authentication that no data from the packet has been modified.</span></span>                        |
| <span data-ttu-id="87f8b-131">\_ \_ \_ privacy PKT a livello di autenticazione C \_ RPC \_</span><span class="sxs-lookup"><span data-stu-id="87f8b-131">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   | <span data-ttu-id="87f8b-132">Include tutti i livelli di autenticazione precedenti e consente di crittografare il valore di ogni chiamata RPC.</span><span class="sxs-lookup"><span data-stu-id="87f8b-132">Includes all previous authentication levels, and encrypts the value of each RPC call.</span></span> |



 

<span data-ttu-id="87f8b-133">È possibile specificare le credenziali di autenticazione predefinite per più utenti usando una **sola struttura dell' \_ \_ elenco di autenticazione** nel parametro *pAuthList* di [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="87f8b-133">You can specify the default authentication credentials for multiple users by using a **SOLE\_AUTHENTICATION\_LIST** structure in the *pAuthList* parameter of [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

<span data-ttu-id="87f8b-134">Nell'esempio di codice riportato di seguito viene illustrato come modificare le credenziali di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="87f8b-134">The following code example shows how to change the authentication credentials.</span></span>


```C++
// Auth Identity structure
SEC_WINNT_AUTH_IDENTITY_W        authidentity;
SecureZeroMemory( &authidentity, sizeof(authidentity) );

authidentity.User = L"MyUser";
authidentity.UserLength = wcslen( authidentity.User );
authidentity.Domain = L"MyDomain ";
authidentity.DomainLength = wcslen( authidentity.Domain );
authidentity.Password = L"";
authidentity.PasswordLength = wcslen( authidentity.Password );
authidentity.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

SecureZeroMemory( authninfo, sizeof(SOLE_AUTHENTICATION_INFO)*2 );

// NTLM Settings
authninfo[0].dwAuthnSvc = RPC_C_AUTHN_WINNT;
authninfo[0].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[0].pAuthInfo = &authidentity;

// Kerberos Settings
authninfo[1].dwAuthnSvc = RPC_C_AUTHN_GSS_KERBEROS ;
authninfo[1].dwAuthzSvc = RPC_C_AUTHZ_NONE;
authninfo[1].pAuthInfo = &authidentity;

SOLE_AUTHENTICATION_LIST    authentlist;

authentlist.cAuthInfo = 2;
authentlist.aAuthInfo = authninfo;

CoInitializeSecurity( 
  NULL, 
  -1, 
  NULL, 
  NULL, 
  RPC_C_AUTHN_LEVEL_CALL, 
  RPC_C_IMP_LEVEL_IMPERSONATE,
  &authentlist, 
  EOAC_NONE,
  NULL);
```



## <a name="changing-the-default-impersonation-levels-using-c"></a><span data-ttu-id="87f8b-135">Modifica dei livelli di rappresentazione predefiniti con C++</span><span class="sxs-lookup"><span data-stu-id="87f8b-135">Changing the Default Impersonation Levels Using C++</span></span>

<span data-ttu-id="87f8b-136">COM fornisce livelli di sicurezza predefiniti letti dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="87f8b-136">COM provides default security levels read from the system registry.</span></span> <span data-ttu-id="87f8b-137">Tuttavia, a meno che non sia stato modificato specificamente, le impostazioni del registro di sistema impostano il livello di rappresentazione troppo basso per il funzionamento di WMI.</span><span class="sxs-lookup"><span data-stu-id="87f8b-137">However, unless specifically modified, the registry settings set the impersonation level too low for WMI to function.</span></span> <span data-ttu-id="87f8b-138">In genere, il livello di rappresentazione predefinito è **l' \_ \_ Identificazione del \_ livello \_ Imp c di RPC**, ma WMI richiede almeno la rappresentazione a **\_ \_ livello di \_ entità \_ RPC c** per funzionare con la maggior parte dei provider e potrebbe verificarsi una situazione in cui è necessario impostare un livello di rappresentazione superiore.</span><span class="sxs-lookup"><span data-stu-id="87f8b-138">Typically, the default impersonation level is **RPC\_C\_IMP\_LEVEL\_IDENTIFY**, but WMI needs at least **RPC\_C\_IMP\_LEVEL\_IMPERSONATE** to function with most providers, and you might encounter a situation where you need to set a higher level of impersonation.</span></span> <span data-ttu-id="87f8b-139">Per ulteriori informazioni, vedere [connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="87f8b-139">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="87f8b-140">Nella tabella seguente sono elencati i diversi livelli di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="87f8b-140">The following table lists the different levels of impersonation.</span></span>



| <span data-ttu-id="87f8b-141">Level</span><span class="sxs-lookup"><span data-stu-id="87f8b-141">Level</span></span>                           | <span data-ttu-id="87f8b-142">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87f8b-142">Description</span></span>                                                                                                   |
|---------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87f8b-143">\_ \_ \_ impostazione predefinita livello IMP C RPC \_</span><span class="sxs-lookup"><span data-stu-id="87f8b-143">RPC\_C\_IMP\_LEVEL\_DEFAULT</span></span>     | <span data-ttu-id="87f8b-144">Il sistema operativo sceglie il livello di rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="87f8b-144">The operating system chooses the level of impersonation.</span></span>                                                      |
| <span data-ttu-id="87f8b-145">\_ \_ livello IMP C \_ RPC \_ Anonimo</span><span class="sxs-lookup"><span data-stu-id="87f8b-145">RPC\_C\_IMP\_LEVEL\_ANONYMOUS</span></span>   | <span data-ttu-id="87f8b-146">Il server può rappresentare il client, ma il token di rappresentazione non può essere utilizzato per nulla.</span><span class="sxs-lookup"><span data-stu-id="87f8b-146">The server can impersonate the client, but the impersonation token cannot be used for anything.</span></span>               |
| <span data-ttu-id="87f8b-147">\_ \_ \_ Identificazione livello IMP C \_ RPC</span><span class="sxs-lookup"><span data-stu-id="87f8b-147">RPC\_C\_IMP\_LEVEL\_IDENTIFY</span></span>    | <span data-ttu-id="87f8b-148">Il server può ottenere l'identità del client e rappresentare il client per il controllo ACL.</span><span class="sxs-lookup"><span data-stu-id="87f8b-148">The server can obtain the identity of the client and impersonate the client for ACL checking.</span></span>                 |
| <span data-ttu-id="87f8b-149">RAPPRESENTAZIONE a livello di RPC \_ C \_ Imp \_ \_</span><span class="sxs-lookup"><span data-stu-id="87f8b-149">RPC\_C\_IMP\_LEVEL\_IMPERSONATE</span></span> | <span data-ttu-id="87f8b-150">Il server può rappresentare il client in un limite di computer.</span><span class="sxs-lookup"><span data-stu-id="87f8b-150">The server can impersonate the client across one computer boundary.</span></span>                                           |
| <span data-ttu-id="87f8b-151">\_ \_ \_ delegato livello IMP C \_ RPC</span><span class="sxs-lookup"><span data-stu-id="87f8b-151">RPC\_C\_IMP\_LEVEL\_DELEGATE</span></span>    | <span data-ttu-id="87f8b-152">Il server può rappresentare il client tra più limiti e può effettuare chiamate per conto del client.</span><span class="sxs-lookup"><span data-stu-id="87f8b-152">The server can impersonate the client across multiple boundaries, and can make calls on behalf of the client.</span></span> |



 

 

 
