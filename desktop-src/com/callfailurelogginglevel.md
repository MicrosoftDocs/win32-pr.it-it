---
title: CallFailureLoggingLevel
description: Imposta il livello di dettaglio delle voci del registro eventi sulle chiamate non riuscite ai componenti.
ms.assetid: 68a7210c-f2a0-4db6-9759-08ff9132a563
keywords:
- Valore CallFailureLoggingLevel del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4432f21f333d5aa5f8b3cebbd6f0fa339cf0f13a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855886"
---
# <a name="callfailurelogginglevel"></a><span data-ttu-id="d97d6-104">CallFailureLoggingLevel</span><span class="sxs-lookup"><span data-stu-id="d97d6-104">CallFailureLoggingLevel</span></span>

<span data-ttu-id="d97d6-105">Imposta il livello di dettaglio delle voci del registro eventi sulle chiamate non riuscite ai componenti.</span><span class="sxs-lookup"><span data-stu-id="d97d6-105">Sets the verbosity of event log entries about failed calls to components.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d97d6-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="d97d6-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   CallFailureLoggingLevel = value
```

## <a name="remarks"></a><span data-ttu-id="d97d6-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="d97d6-107">Remarks</span></span>

<span data-ttu-id="d97d6-108">Si tratta di un valore **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="d97d6-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="d97d6-109">Valore</span><span class="sxs-lookup"><span data-stu-id="d97d6-109">Value</span></span> | <span data-ttu-id="d97d6-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d97d6-110">Description</span></span>                                                                            |
|-------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d97d6-111">1</span><span class="sxs-lookup"><span data-stu-id="d97d6-111">1</span></span>     | <span data-ttu-id="d97d6-112">Registrare sempre gli errori durante una chiamata nel processo del server COM.</span><span class="sxs-lookup"><span data-stu-id="d97d6-112">Always log failures during a call in the COM Server process.</span></span>                           |
| <span data-ttu-id="d97d6-113">2</span><span class="sxs-lookup"><span data-stu-id="d97d6-113">2</span></span>     | <span data-ttu-id="d97d6-114">Non registrare mai errori durante una chiamata nel processo del server COM.</span><span class="sxs-lookup"><span data-stu-id="d97d6-114">Never log failures during a call in the COM Server process.</span></span> <span data-ttu-id="d97d6-115">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="d97d6-115">This is the default value.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d97d6-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d97d6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d97d6-117">Impostazione della sicurezza per le applicazioni COM</span><span class="sxs-lookup"><span data-stu-id="d97d6-117">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




