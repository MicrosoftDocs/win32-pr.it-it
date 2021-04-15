---
title: DoNotAddAllApplicationPackagesToRestrictions
description: Determina se RPCSS aggiunge automaticamente \_ \_ per impostazione predefinita un SID di tutti i pacchetti dell'applicazione a restrizioni com.
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800077c61e01cf0b3f76d5a92f8282c7ecca12e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395435"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a><span data-ttu-id="0c2ac-103">DoNotAddAllApplicationPackagesToRestrictions</span><span class="sxs-lookup"><span data-stu-id="0c2ac-103">DoNotAddAllApplicationPackagesToRestrictions</span></span>

<span data-ttu-id="0c2ac-104">Determina se RPCSS aggiunge automaticamente \_ \_ per impostazione predefinita un SID di tutti i pacchetti dell'applicazione a restrizioni com.</span><span class="sxs-lookup"><span data-stu-id="0c2ac-104">Determines whether RPCSS automatically appends an ALL\_APPLICATION\_PACKAGES SID to COM restrictions by default.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0c2ac-105">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="0c2ac-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a><span data-ttu-id="0c2ac-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c2ac-106">Remarks</span></span>

<span data-ttu-id="0c2ac-107">Si tratta di un valore **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="0c2ac-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="0c2ac-108">Valore</span><span class="sxs-lookup"><span data-stu-id="0c2ac-108">Value</span></span> | <span data-ttu-id="0c2ac-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c2ac-109">Description</span></span>                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c2ac-110">0</span><span class="sxs-lookup"><span data-stu-id="0c2ac-110">0</span></span>     | <span data-ttu-id="0c2ac-111">Disabilita le app di Windows Store durante la migrazione da Windows 7 a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0c2ac-111">Disables Windows Store apps upon migration from Windows 7 to Windows 8.</span></span>                   |
| <span data-ttu-id="0c2ac-112">1</span><span class="sxs-lookup"><span data-stu-id="0c2ac-112">1</span></span>     | <span data-ttu-id="0c2ac-113">Non aggiunge il SID tutti \_ i \_ pacchetti dell'applicazione alle restrizioni com.</span><span class="sxs-lookup"><span data-stu-id="0c2ac-113">Does not add the ALL\_APPLICATION\_PACKAGES SID to COM restrictions.</span></span> <span data-ttu-id="0c2ac-114">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="0c2ac-114">This is the default.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0c2ac-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0c2ac-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c2ac-116">Impostazione della sicurezza per le applicazioni COM</span><span class="sxs-lookup"><span data-stu-id="0c2ac-116">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




