---
title: LegacyAuthenticationLevel
description: Imposta il livello di autenticazione predefinito per le applicazioni che non chiamano CoInitializeSecurity.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- Valore LegacyAuthenticationLevel del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d87d808287418f635629e15324f2f517619be6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045364"
---
# <a name="legacyauthenticationlevel"></a><span data-ttu-id="53f16-104">LegacyAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="53f16-104">LegacyAuthenticationLevel</span></span>

<span data-ttu-id="53f16-105">Imposta il livello di autenticazione predefinito per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="53f16-105">Sets the default authentication level for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

> [!Caution]  
> <span data-ttu-id="53f16-106">Non è consigliabile modificare questo valore, perché questo influirà su tutte le applicazioni server COM che non impostano la propria sicurezza a livello di processo e potrebbe impedire il corretto funzionamento.</span><span class="sxs-lookup"><span data-stu-id="53f16-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="53f16-107">Se si modifica questo valore in modo da influire sulle impostazioni di sicurezza di una particolare applicazione COM, è necessario modificare le impostazioni di sicurezza a livello di processo per quella particolare applicazione COM.</span><span class="sxs-lookup"><span data-stu-id="53f16-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="53f16-108">Per altre informazioni sull'impostazione della sicurezza a livello di processo, vedere [impostazione della sicurezza a livello di processo](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="53f16-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="53f16-109">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="53f16-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="53f16-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="53f16-110">Remarks</span></span>

<span data-ttu-id="53f16-111">Si tratta di un valore **reg \_ Word** equivalente alle \_ costanti del \_ livello auth C RPC \_ .</span><span class="sxs-lookup"><span data-stu-id="53f16-111">This is a **REG\_WORD** value that is equivalent to the RPC\_C\_AUTHN\_LEVEL constants.</span></span>



| <span data-ttu-id="53f16-112">Valore</span><span class="sxs-lookup"><span data-stu-id="53f16-112">Value</span></span> | <span data-ttu-id="53f16-113">Costante</span><span class="sxs-lookup"><span data-stu-id="53f16-113">Constant</span></span>                             |
|-------|--------------------------------------|
| <span data-ttu-id="53f16-114">1</span><span class="sxs-lookup"><span data-stu-id="53f16-114">1</span></span>     | <span data-ttu-id="53f16-115">\_ \_ livello auth C \_ RPC \_</span><span class="sxs-lookup"><span data-stu-id="53f16-115">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           |
| <span data-ttu-id="53f16-116">2</span><span class="sxs-lookup"><span data-stu-id="53f16-116">2</span></span>     | <span data-ttu-id="53f16-117">\_connessione a \_ livello auth \_ C \_ RPC</span><span class="sxs-lookup"><span data-stu-id="53f16-117">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        |
| <span data-ttu-id="53f16-118">3</span><span class="sxs-lookup"><span data-stu-id="53f16-118">3</span></span>     | <span data-ttu-id="53f16-119">\_chiamata al \_ livello auth \_ C \_ RPC</span><span class="sxs-lookup"><span data-stu-id="53f16-119">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           |
| <span data-ttu-id="53f16-120">4</span><span class="sxs-lookup"><span data-stu-id="53f16-120">4</span></span>     | <span data-ttu-id="53f16-121">\_ \_ \_ PKT livello auth C RPC \_</span><span class="sxs-lookup"><span data-stu-id="53f16-121">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            |
| <span data-ttu-id="53f16-122">5</span><span class="sxs-lookup"><span data-stu-id="53f16-122">5</span></span>     | <span data-ttu-id="53f16-123">\_ \_ \_ integrità PKT del livello auth \_ C \_ RPC</span><span class="sxs-lookup"><span data-stu-id="53f16-123">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> |
| <span data-ttu-id="53f16-124">6</span><span class="sxs-lookup"><span data-stu-id="53f16-124">6</span></span>     | <span data-ttu-id="53f16-125">\_ \_ \_ privacy PKT a livello di autenticazione C \_ RPC \_</span><span class="sxs-lookup"><span data-stu-id="53f16-125">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   |



 

<span data-ttu-id="53f16-126">Se il valore del registro di sistema non è presente, il livello di autenticazione predefinito stabilito dal sistema è 2 ( \_ \_ connessione auth C RPC \_ ).</span><span class="sxs-lookup"><span data-stu-id="53f16-126">If this registry value is not present, the default authentication level established by the system is 2 (RPC\_C\_AUTHN\_CONNECT).</span></span>

## <a name="related-topics"></a><span data-ttu-id="53f16-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="53f16-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53f16-128">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="53f16-128">**AuthenticationLevel**</span></span>](authenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="53f16-129">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="53f16-129">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="53f16-130">Impostazione della sicurezza a livello di processo</span><span class="sxs-lookup"><span data-stu-id="53f16-130">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




