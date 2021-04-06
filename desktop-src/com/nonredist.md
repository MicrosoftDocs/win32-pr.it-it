---
title: NONREDIST
description: Aggiunge nomi all'elenco di file che non devono essere esportati quando le applicazioni COM+ sono assemblate per l'installazione in altri computer. Si noti che si tratta di una sottochiave, non di un valore.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- Valore del registro di sistema non REDIST COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d537208ecaf98cec46591966e4ae7d9c205850a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045405"
---
# <a name="nonredist"></a><span data-ttu-id="e5efc-105">NONREDIST</span><span class="sxs-lookup"><span data-stu-id="e5efc-105">NONREDIST</span></span>

<span data-ttu-id="e5efc-106">Aggiunge nomi all'elenco di file che non devono essere esportati quando le applicazioni COM+ sono assemblate per l'installazione in altri computer.</span><span class="sxs-lookup"><span data-stu-id="e5efc-106">Adds names to the list of files that should not be exported when COM+ applications are packaged for installation on other computers.</span></span> <span data-ttu-id="e5efc-107">Si noti che si tratta di una sottochiave, non di un valore.</span><span class="sxs-lookup"><span data-stu-id="e5efc-107">Note that this is a subkey, not a value.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e5efc-108">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e5efc-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a><span data-ttu-id="e5efc-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="e5efc-109">Remarks</span></span>

<span data-ttu-id="e5efc-110">I file aggiunti all'elenco sono rappresentati da coppie nome/valore archiviate in questa chiave.</span><span class="sxs-lookup"><span data-stu-id="e5efc-110">The files you add to the list are represented by name/value pairs stored under this key.</span></span> <span data-ttu-id="e5efc-111">In ogni coppia nome/valore il nome è il nome del file e il valore è riservato.</span><span class="sxs-lookup"><span data-stu-id="e5efc-111">In each name/value pair, the name is the file name and the value is reserved.</span></span>

 

 




