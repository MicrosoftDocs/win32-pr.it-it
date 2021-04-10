---
title: AuthenticationLevel
description: Imposta il livello di autenticazione per le applicazioni che non chiamano CoInitializeSecurity o per le applicazioni che chiamano CoInitializeSecurity e specificano un AppID.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- Valore AuthenticationLevel del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b04bcf4992c8a6943bcb515fa0a4eae616fec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332636"
---
# <a name="authenticationlevel"></a><span data-ttu-id="b7a5e-104">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="b7a5e-104">AuthenticationLevel</span></span>

<span data-ttu-id="b7a5e-105">Imposta il livello di autenticazione per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o per le applicazioni che chiamano **CoInitializeSecurity** e specificano un AppID.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-105">Sets the authentication level for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or for applications that call **CoInitializeSecurity** and specify an AppID.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b7a5e-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="b7a5e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="b7a5e-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="b7a5e-107">Remarks</span></span>

<span data-ttu-id="b7a5e-108">Si tratta di un valore **reg \_ DWORD** equivalente alle \_ costanti del \_ livello auth C RPC \_ .</span><span class="sxs-lookup"><span data-stu-id="b7a5e-108">This is a **REG\_DWORD** value that is equivalent to the RPC\_C\_AUTHN\_LEVEL constants.</span></span>



| <span data-ttu-id="b7a5e-109">Valore</span><span class="sxs-lookup"><span data-stu-id="b7a5e-109">Value</span></span> | <span data-ttu-id="b7a5e-110">Costante</span><span class="sxs-lookup"><span data-stu-id="b7a5e-110">Constant</span></span>                             |
|-------|--------------------------------------|
| <span data-ttu-id="b7a5e-111">1</span><span class="sxs-lookup"><span data-stu-id="b7a5e-111">1</span></span>     | <span data-ttu-id="b7a5e-112">\_ \_ livello auth C \_ RPC \_</span><span class="sxs-lookup"><span data-stu-id="b7a5e-112">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           |
| <span data-ttu-id="b7a5e-113">2</span><span class="sxs-lookup"><span data-stu-id="b7a5e-113">2</span></span>     | <span data-ttu-id="b7a5e-114">\_connessione a \_ livello auth \_ C \_ RPC</span><span class="sxs-lookup"><span data-stu-id="b7a5e-114">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        |
| <span data-ttu-id="b7a5e-115">3</span><span class="sxs-lookup"><span data-stu-id="b7a5e-115">3</span></span>     | <span data-ttu-id="b7a5e-116">\_chiamata al \_ livello auth \_ C \_ RPC</span><span class="sxs-lookup"><span data-stu-id="b7a5e-116">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           |
| <span data-ttu-id="b7a5e-117">4</span><span class="sxs-lookup"><span data-stu-id="b7a5e-117">4</span></span>     | <span data-ttu-id="b7a5e-118">\_ \_ \_ PKT livello auth C RPC \_</span><span class="sxs-lookup"><span data-stu-id="b7a5e-118">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            |
| <span data-ttu-id="b7a5e-119">5</span><span class="sxs-lookup"><span data-stu-id="b7a5e-119">5</span></span>     | <span data-ttu-id="b7a5e-120">\_ \_ \_ integrità PKT del livello auth \_ C \_ RPC</span><span class="sxs-lookup"><span data-stu-id="b7a5e-120">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> |
| <span data-ttu-id="b7a5e-121">6</span><span class="sxs-lookup"><span data-stu-id="b7a5e-121">6</span></span>     | <span data-ttu-id="b7a5e-122">\_ \_ \_ privacy PKT a livello di autenticazione C \_ RPC \_</span><span class="sxs-lookup"><span data-stu-id="b7a5e-122">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   |



 

<span data-ttu-id="b7a5e-123">Il valore di **AuthenticationLevel** è simile al valore di [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) .</span><span class="sxs-lookup"><span data-stu-id="b7a5e-123">The **AuthenticationLevel** value is similar to the [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) value.</span></span> <span data-ttu-id="b7a5e-124">Se il valore **AuthenticationLevel** è presente, viene usato al posto del valore **LegacyAuthenticationLevel** per tale AppID.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-124">If the **AuthenticationLevel** value is present, it is used instead of the **LegacyAuthenticationLevel** value for that AppID.</span></span>

<span data-ttu-id="b7a5e-125">Se il valore **AuthenticationLevel** è di tipo errato o non è compreso nell'intervallo, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ha esito negativo, causando l'esito negativo del marshalling dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-125">If the **AuthenticationLevel** value is of the wrong type or out of range, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) fails, causing interface marshaling to fail.</span></span> <span data-ttu-id="b7a5e-126">In questo modo si impedisce all'applicazione di effettuare tutte le chiamate (Cross-Apartment, cross-thread, tra processi o tra computer).</span><span class="sxs-lookup"><span data-stu-id="b7a5e-126">This prevents the application from making any calls at all (cross-apartment, cross-thread, cross-process, or cross-computer).</span></span>

<span data-ttu-id="b7a5e-127">I valori **AuthenticationLevel** e [**AccessPermission**](accesspermission.md) sono indipendenti.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-127">The **AuthenticationLevel** and [**AccessPermission**](accesspermission.md) values are independent.</span></span> <span data-ttu-id="b7a5e-128">Se non è presente, viene usato il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b7a5e-128">If one is not present, the default is used.</span></span> <span data-ttu-id="b7a5e-129">Le regole seguenti elencano l'interazione tra il valore di **AuthenticationLevel** e il valore di **AccessPermission** :</span><span class="sxs-lookup"><span data-stu-id="b7a5e-129">The following rules list the interaction between the **AuthenticationLevel** value and the **AccessPermission** value:</span></span>

-   <span data-ttu-id="b7a5e-130">Se **AuthenticationLevel** è None, i valori [**AccessPermission**](accesspermission.md) e [**DefaultAccessPermission**](defaultaccesspermission.md) vengono ignorati (per tale applicazione).</span><span class="sxs-lookup"><span data-stu-id="b7a5e-130">If the **AuthenticationLevel** is NONE, the [**AccessPermission**](accesspermission.md) and [**DefaultAccessPermission**](defaultaccesspermission.md) values are ignored (for that application).</span></span>
-   <span data-ttu-id="b7a5e-131">Se **AuthenticationLevel** non è presente e [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) è None, i valori [**AccessPermission**](accesspermission.md) e [**DefaultAccessPermission**](defaultaccesspermission.md) vengono ignorati (per tale applicazione).</span><span class="sxs-lookup"><span data-stu-id="b7a5e-131">If the **AuthenticationLevel** is not present and the [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) is NONE, the [**AccessPermission**](accesspermission.md) and [**DefaultAccessPermission**](defaultaccesspermission.md) values are ignored (for that application).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7a5e-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b7a5e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7a5e-133">Costanti del livello di autenticazione</span><span class="sxs-lookup"><span data-stu-id="b7a5e-133">Authentication Level Constants</span></span>](com-authentication-level-constants.md)
</dt> <dt>

[<span data-ttu-id="b7a5e-134">**LegacyAuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="b7a5e-134">**LegacyAuthenticationLevel**</span></span>](legacyauthenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="b7a5e-135">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="b7a5e-135">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="b7a5e-136">Sicurezza in COM</span><span class="sxs-lookup"><span data-stu-id="b7a5e-136">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




