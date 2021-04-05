---
title: Versione (COM)
description: Specifica il numero di versione del controllo.
ms.assetid: 69ad4647-d39c-4bfd-b027-0a2db8fb3881
keywords:
- Chiave del registro di sistema versione COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcfe909113dad3b0d84ac692463661e82750aaa0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103873233"
---
# <a name="version-com"></a><span data-ttu-id="e89ef-104">Versione (COM)</span><span class="sxs-lookup"><span data-stu-id="e89ef-104">Version (COM)</span></span>

<span data-ttu-id="e89ef-105">Specifica il numero di versione del controllo.</span><span class="sxs-lookup"><span data-stu-id="e89ef-105">Specifies the version number of the control.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e89ef-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e89ef-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Version = value
```

## <a name="remarks"></a><span data-ttu-id="e89ef-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="e89ef-107">Remarks</span></span>

<span data-ttu-id="e89ef-108">Si tratta di un valore **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="e89ef-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="e89ef-109">Il numero di versione deve corrispondere alla versione della libreria dei tipi associata al controllo.</span><span class="sxs-lookup"><span data-stu-id="e89ef-109">The version number should match the version of the type library associated with the control.</span></span>

 

 




