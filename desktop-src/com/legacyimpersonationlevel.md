---
title: LegacyImpersonationLevel
description: Imposta il livello predefinito di rappresentazione per le applicazioni che non chiamano CoInitializeSecurity.
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- Valore LegacyImpersonationLevel del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fa00494eb71e49c35bfa37b434afc5c999e73e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298367"
---
# <a name="legacyimpersonationlevel"></a><span data-ttu-id="b655c-104">LegacyImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="b655c-104">LegacyImpersonationLevel</span></span>

<span data-ttu-id="b655c-105">Imposta il livello predefinito di rappresentazione per le applicazioni che non chiamano [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="b655c-105">Sets the default level of impersonation for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

> [!Caution]  
> <span data-ttu-id="b655c-106">Non è consigliabile modificare questo valore, perché questo influirà su tutte le applicazioni server COM che non impostano la propria sicurezza a livello di processo e potrebbe impedire il corretto funzionamento.</span><span class="sxs-lookup"><span data-stu-id="b655c-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="b655c-107">Se si modifica questo valore in modo da influire sulle impostazioni di sicurezza di una particolare applicazione COM, è necessario modificare le impostazioni di sicurezza a livello di processo per quella particolare applicazione COM.</span><span class="sxs-lookup"><span data-stu-id="b655c-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="b655c-108">Per altre informazioni sull'impostazione della sicurezza a livello di processo, vedere [impostazione della sicurezza a livello di processo](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="b655c-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="b655c-109">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="b655c-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyImpersonationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="b655c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b655c-110">Remarks</span></span>

<span data-ttu-id="b655c-111">Si tratta di un valore **reg \_ Word** equivalente alle costanti a livello di RPC \_ C \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b655c-111">This is a **REG\_WORD** value that is equivalent to the RPC\_C\_IMP\_LEVEL constants.</span></span>



| <span data-ttu-id="b655c-112">Valore</span><span class="sxs-lookup"><span data-stu-id="b655c-112">Value</span></span> | <span data-ttu-id="b655c-113">Costante</span><span class="sxs-lookup"><span data-stu-id="b655c-113">Constant</span></span>                        |
|-------|---------------------------------|
| <span data-ttu-id="b655c-114">1</span><span class="sxs-lookup"><span data-stu-id="b655c-114">1</span></span>     | <span data-ttu-id="b655c-115">\_ \_ livello IMP C \_ RPC \_ Anonimo</span><span class="sxs-lookup"><span data-stu-id="b655c-115">RPC\_C\_IMP\_LEVEL\_ANONYMOUS</span></span>   |
| <span data-ttu-id="b655c-116">2</span><span class="sxs-lookup"><span data-stu-id="b655c-116">2</span></span>     | <span data-ttu-id="b655c-117">\_ \_ \_ Identificazione livello IMP C \_ RPC</span><span class="sxs-lookup"><span data-stu-id="b655c-117">RPC\_C\_IMP\_LEVEL\_IDENTIFY</span></span>    |
| <span data-ttu-id="b655c-118">3</span><span class="sxs-lookup"><span data-stu-id="b655c-118">3</span></span>     | <span data-ttu-id="b655c-119">RAPPRESENTAZIONE a livello di RPC \_ C \_ Imp \_ \_</span><span class="sxs-lookup"><span data-stu-id="b655c-119">RPC\_C\_IMP\_LEVEL\_IMPERSONATE</span></span> |
| <span data-ttu-id="b655c-120">4</span><span class="sxs-lookup"><span data-stu-id="b655c-120">4</span></span>     | <span data-ttu-id="b655c-121">\_ \_ \_ delegato livello IMP C \_ RPC</span><span class="sxs-lookup"><span data-stu-id="b655c-121">RPC\_C\_IMP\_LEVEL\_DELEGATE</span></span>    |



 

<span data-ttu-id="b655c-122">Se il valore del registro di sistema non è presente, il livello di rappresentazione predefinito stabilito dal sistema è 2 ( \_ Identificazione del livello di RPC C \_ \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="b655c-122">If this registry value is not present, the default impersonation level established by the system is 2 (RPC\_C\_IMP\_LEVEL\_IDENTIFY).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b655c-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b655c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b655c-124">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="b655c-124">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="b655c-125">Impostazione della sicurezza a livello di processo</span><span class="sxs-lookup"><span data-stu-id="b655c-125">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




