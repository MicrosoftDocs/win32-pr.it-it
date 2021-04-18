---
title: LegacySecureReferences
description: Determina se le chiamate AddRef/release sono protette per le applicazioni che non chiamano CoInitializeSecurity.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- Valore LegacySecureReferences del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2776bf3661013f1e622bbc2e1c553f2551c62808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298368"
---
# <a name="legacysecurereferences"></a><span data-ttu-id="53aff-104">LegacySecureReferences</span><span class="sxs-lookup"><span data-stu-id="53aff-104">LegacySecureReferences</span></span>

<span data-ttu-id="53aff-105">Determina se  / le chiamate di **rilascio** AddRef sono protette per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="53aff-105">Determines whether **AddRef**/**Release** invocations are secured for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="53aff-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="53aff-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a><span data-ttu-id="53aff-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="53aff-107">Remarks</span></span>

<span data-ttu-id="53aff-108">Si tratta di un valore **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="53aff-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="53aff-109">Il valore ' Y ' o ' y ' indica che **AddRef** e **Release** sono protette.</span><span class="sxs-lookup"><span data-stu-id="53aff-109">A value of 'Y' or 'y' indicate that **AddRef** and **Release** are secured.</span></span> <span data-ttu-id="53aff-110">Se il valore del registro di sistema non è presente o è impostato su un valore diverso da' Y ' o ' y ', **AddRef** e **Release** non sono protetti.</span><span class="sxs-lookup"><span data-stu-id="53aff-110">If this registry value is not present or is set to a value other than 'Y' or 'y', **AddRef** and **Release** are not secured.</span></span> <span data-ttu-id="53aff-111">L'abilitazione di riferimenti protetti rallenta le chiamate remote.</span><span class="sxs-lookup"><span data-stu-id="53aff-111">Enabling secure references slows remote calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53aff-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="53aff-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53aff-113">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="53aff-113">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="53aff-114">Impostazione della sicurezza a livello di processo</span><span class="sxs-lookup"><span data-stu-id="53aff-114">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




