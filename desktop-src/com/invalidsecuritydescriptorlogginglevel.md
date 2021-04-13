---
title: InvalidSecurityDescriptorLoggingLevel
description: Imposta il livello di dettaglio delle voci del registro eventi relative a descrittori di sicurezza non validi per le autorizzazioni di avvio e accesso dei componenti.
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- Valore InvalidSecurityDescriptorLoggingLevel del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ac333a7cb8b54f383f93a71131cbb0a9314466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328279"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a><span data-ttu-id="e9f48-104">InvalidSecurityDescriptorLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="e9f48-104">InvalidSecurityDescriptorLoggingLevel</span></span>

<span data-ttu-id="e9f48-105">Imposta il livello di dettaglio delle voci del registro eventi relative a descrittori di sicurezza non validi per le autorizzazioni di avvio e accesso dei componenti.</span><span class="sxs-lookup"><span data-stu-id="e9f48-105">Sets the verbosity of event log entries about invalid security descriptors for component launch and access permissions.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e9f48-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e9f48-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="e9f48-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9f48-107">Remarks</span></span>

<span data-ttu-id="e9f48-108">Si tratta di un valore **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e9f48-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="e9f48-109">Valore</span><span class="sxs-lookup"><span data-stu-id="e9f48-109">Value</span></span> | <span data-ttu-id="e9f48-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9f48-110">Description</span></span>                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f48-111">1</span><span class="sxs-lookup"><span data-stu-id="e9f48-111">1</span></span>     | <span data-ttu-id="e9f48-112">Registra sempre gli errori quando COM trova un descrittore di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="e9f48-112">Always log failures when COM finds an invalid security descriptor.</span></span> <span data-ttu-id="e9f48-113">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="e9f48-113">This is the default value.</span></span>                                                                                  |
| <span data-ttu-id="e9f48-114">2</span><span class="sxs-lookup"><span data-stu-id="e9f48-114">2</span></span>     | <span data-ttu-id="e9f48-115">Non registrare mai errori quando COM trova un descrittore di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="e9f48-115">Never log failures when COM finds an invalid security descriptor.</span></span> <span data-ttu-id="e9f48-116">Non è consigliabile disabilitare la registrazione degli eventi, in quanto può rendere più difficile la diagnosi dei problemi.</span><span class="sxs-lookup"><span data-stu-id="e9f48-116">It is not recommended that you disable event logging, as it can make it more difficult to diagnose problems.</span></span> |



 

<span data-ttu-id="e9f48-117">Se si impostano direttamente i descrittori di sicurezza per le autorizzazioni di avvio e di accesso, chiamati comunemente ACL, è possibile creare un descrittore di sicurezza il cui significato non può essere interpretato in modo non ambiguo.</span><span class="sxs-lookup"><span data-stu-id="e9f48-117">If you set launch and access permission security descriptors (commonly called ACLs) directly, it is possible to construct a security descriptor whose meaning cannot be interpreted unambiguously.</span></span> <span data-ttu-id="e9f48-118">COM crea una voce del registro eventi quando rileva un descrittore di sicurezza non valido.</span><span class="sxs-lookup"><span data-stu-id="e9f48-118">COM makes an event log entry when it encounters such an invalid security descriptor.</span></span>

<span data-ttu-id="e9f48-119">Si noti che [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) e [**CallFailureLoggingLevel**](callfailurelogginglevel.md) non sono in grado di controllare la registrazione di errori descrittori di sicurezza non validi</span><span class="sxs-lookup"><span data-stu-id="e9f48-119">Note that [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) and [**CallFailureLoggingLevel**](callfailurelogginglevel.md) have no control over logging invalid security descriptor errors.</span></span> <span data-ttu-id="e9f48-120">Usare **InvalidSecurityDescriptorLoggingLevel** per il controllo completo di questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e9f48-120">Use **InvalidSecurityDescriptorLoggingLevel** for full control over this functionality.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9f48-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e9f48-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9f48-122">Impostazione della sicurezza per le applicazioni COM</span><span class="sxs-lookup"><span data-stu-id="e9f48-122">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




