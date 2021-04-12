---
description: Le applicazioni client speciali potrebbero richiamare operazioni con privilegi.
ms.assetid: e09fcadc-282f-4f07-b69c-b15bfdb07a7d
ms.tgt_platform: multiple
title: Esecuzione di operazioni con privilegi con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc0468fef7531586020f55032bff94c977c4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344916"
---
# <a name="executing-privileged-operations-using-c"></a><span data-ttu-id="5da5e-103">Esecuzione di operazioni con privilegi con C++</span><span class="sxs-lookup"><span data-stu-id="5da5e-103">Executing Privileged Operations Using C++</span></span>

<span data-ttu-id="5da5e-104">Le applicazioni client speciali potrebbero richiamare operazioni con privilegi.</span><span class="sxs-lookup"><span data-stu-id="5da5e-104">Special client applications might invoke privileged operations.</span></span> <span data-ttu-id="5da5e-105">Ad esempio, un'applicazione potrebbe consentire a un responsabile di riavviare un computer Office che non risponde.</span><span class="sxs-lookup"><span data-stu-id="5da5e-105">For example, an application could allow a manager to reboot an unresponsive office computer.</span></span> <span data-ttu-id="5da5e-106">Utilizzando Strumentazione gestione Windows (WMI), è possibile eseguire un'operazione con privilegi chiamando il provider WMI per l'operazione con privilegi.</span><span class="sxs-lookup"><span data-stu-id="5da5e-106">By using Windows Management Instrumentation (WMI), you can execute a privileged operation by calling the WMI provider for the privileged operation.</span></span>

<span data-ttu-id="5da5e-107">Nella procedura riportata di seguito viene descritto come chiamare un provider per un'operazione con privilegi.</span><span class="sxs-lookup"><span data-stu-id="5da5e-107">The following procedure describes how to call a provider for a privileged operation.</span></span>

<span data-ttu-id="5da5e-108">**Per chiamare un provider per un'operazione con privilegi**</span><span class="sxs-lookup"><span data-stu-id="5da5e-108">**To call a provider for a privileged operation**</span></span>

1.  <span data-ttu-id="5da5e-109">Ottenere le autorizzazioni per il processo client per eseguire l'operazione con privilegi.</span><span class="sxs-lookup"><span data-stu-id="5da5e-109">Obtain permissions for the client process to execute the privileged operation.</span></span>

    <span data-ttu-id="5da5e-110">In genere, un amministratore imposta le autorizzazioni utilizzando gli strumenti di amministrazione del sistema, prima di eseguire il processo.</span><span class="sxs-lookup"><span data-stu-id="5da5e-110">Typically, an administrator sets the permissions using system administrative tools—prior to running the process.</span></span>

2.  <span data-ttu-id="5da5e-111">Ottenere l'autorizzazione per il processo del provider per abilitare l'operazione con privilegi.</span><span class="sxs-lookup"><span data-stu-id="5da5e-111">Obtain permission for the provider process to enable the privileged operation.</span></span>

    <span data-ttu-id="5da5e-112">In genere, è possibile impostare le autorizzazioni del provider con una chiamata alla funzione [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .</span><span class="sxs-lookup"><span data-stu-id="5da5e-112">Typically, you can set provider permissions with a call to the [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function.</span></span>

3.  <span data-ttu-id="5da5e-113">Ottenere l'autorizzazione per il processo client per abilitare l'operazione con privilegi.</span><span class="sxs-lookup"><span data-stu-id="5da5e-113">Obtain permission for the client process to enable the privileged operation.</span></span>

    <span data-ttu-id="5da5e-114">Questo passaggio è necessario solo se il provider è locale per il client.</span><span class="sxs-lookup"><span data-stu-id="5da5e-114">This step is necessary only if the provider is local to the client.</span></span> <span data-ttu-id="5da5e-115">Se il client e il provider sono presenti nello stesso computer, il client deve abilitare in modo specifico l'operazione con privilegi utilizzando una delle tecniche seguenti:</span><span class="sxs-lookup"><span data-stu-id="5da5e-115">If the client and provider exist on the same computer, the client must specifically enable the privileged operation by using one of the following techniques:</span></span>

    -   <span data-ttu-id="5da5e-116">Se il client è proprietario del processo, il client può utilizzare [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) per modificare il token di processo prima di chiamare WMI.</span><span class="sxs-lookup"><span data-stu-id="5da5e-116">If the client owns the process, the client can use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) to adjust the process token before calling WMI.</span></span> <span data-ttu-id="5da5e-117">In questo caso, non è necessario codificare ulteriormente.</span><span class="sxs-lookup"><span data-stu-id="5da5e-117">In this case, you do not need to code any further.</span></span>
    -   <span data-ttu-id="5da5e-118">Se il client non è in grado di accedere al token client, il client può utilizzare la procedura seguente per creare un token del thread e utilizzare [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) su tale token.</span><span class="sxs-lookup"><span data-stu-id="5da5e-118">If the client cannot access the client token, the client can use the following procedure to create a thread token and use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on that token.</span></span>

<span data-ttu-id="5da5e-119">Nella procedura seguente viene descritto come creare un token di thread e utilizzare [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) su tale token.</span><span class="sxs-lookup"><span data-stu-id="5da5e-119">The following procedure describes how to create a thread token and use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on that token.</span></span>

<span data-ttu-id="5da5e-120">**Per creare un token di thread e utilizzare AdjustTokenPrivileges su tale token**</span><span class="sxs-lookup"><span data-stu-id="5da5e-120">**To create a thread token and use AdjustTokenPrivileges on that token**</span></span>

1.  <span data-ttu-id="5da5e-121">Creare una copia del token di processo chiamando [**ImpersonateSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself).</span><span class="sxs-lookup"><span data-stu-id="5da5e-121">Create a copy of the process token by calling [**ImpersonateSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself).</span></span>
2.  <span data-ttu-id="5da5e-122">Recuperare il token del thread appena creato chiamando [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).</span><span class="sxs-lookup"><span data-stu-id="5da5e-122">Retrieve the newly created thread token by calling [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).</span></span>
3.  <span data-ttu-id="5da5e-123">Abilitare l'operazione Privileged con una chiamata a [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) sul nuovo token.</span><span class="sxs-lookup"><span data-stu-id="5da5e-123">Enable the privileged operation with a call to [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on the new token.</span></span>
4.  <span data-ttu-id="5da5e-124">Ottenere un puntatore a [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).</span><span class="sxs-lookup"><span data-stu-id="5da5e-124">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).</span></span>
5.  <span data-ttu-id="5da5e-125">Mascherare il puntatore a [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) con una chiamata a [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="5da5e-125">Cloak the pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) with a call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>
6.  <span data-ttu-id="5da5e-126">Ripetere i passaggi da 1 a 5 per ogni chiamata a WMI.</span><span class="sxs-lookup"><span data-stu-id="5da5e-126">Repeat steps 1 through 5 on each call to WMI.</span></span>

    > [!Note]  
    > <span data-ttu-id="5da5e-127">È necessario ripetere i passaggi perché COM memorizza nella cache i token in modo non corretto.</span><span class="sxs-lookup"><span data-stu-id="5da5e-127">You must repeat the steps because COM caches tokens incorrectly.</span></span>

     

<span data-ttu-id="5da5e-128">Per eseguire correttamente la compilazione, l'esempio di codice in questo argomento richiede la seguente \# istruzione include.</span><span class="sxs-lookup"><span data-stu-id="5da5e-128">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="5da5e-129">Nell'esempio di codice seguente viene illustrato come abilitare i privilegi in un computer locale.</span><span class="sxs-lookup"><span data-stu-id="5da5e-129">The following code example shows how to enable privileges on a local machine.</span></span>


```C++
// Get the privileges 
// The token has been obtained outside the scope of this code sample
// ================== 
DWORD dwLen;
bool bRes;
HANDLE hToken;

// obtain dwLen
bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  NULL, 
  0,
  &dwLen
); 

BYTE* pBuffer = new BYTE[dwLen];
if(pBuffer == NULL)
{
  CloseHandle(hToken);
  return WBEM_E_OUT_OF_MEMORY;
} 

bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  pBuffer,     
  dwLen,        
  &dwLen
);

if (!bRes)
{
  CloseHandle(hToken);
  delete [] pBuffer;
  return WBEM_E_ACCESS_DENIED;
} 

// Iterate through all the privileges and enable them all
// ====================================================== 
TOKEN_PRIVILEGES* pPrivs = (TOKEN_PRIVILEGES*)pBuffer;
for (DWORD i = 0; i < pPrivs->PrivilegeCount; i++)
{
  pPrivs->Privileges[i].Attributes |= SE_PRIVILEGE_ENABLED;
} 
// Store the information back in the token
// ========================================= 
bRes = AdjustTokenPrivileges(
  hToken, 
  FALSE, 
  pPrivs, 
  0, NULL, NULL
);

delete [] pBuffer;
CloseHandle(hToken); 

if (!bRes)
  return WBEM_E_ACCESS_DENIED;
else
  return WBEM_S_NO_ERROR;
```



 

 
