---
title: Control
description: Identifica un oggetto come controllo ActiveX.
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- Controllare la chiave del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3722d85b38399d7e95f226749bda45ccc82d1369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396866"
---
# <a name="control"></a><span data-ttu-id="4fbbf-104">Control</span><span class="sxs-lookup"><span data-stu-id="4fbbf-104">Control</span></span>

<span data-ttu-id="4fbbf-105">Identifica un oggetto come controllo ActiveX.</span><span class="sxs-lookup"><span data-stu-id="4fbbf-105">Identifies an object as an ActiveX Control.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4fbbf-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="4fbbf-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a><span data-ttu-id="4fbbf-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="4fbbf-107">Remarks</span></span>

<span data-ttu-id="4fbbf-108">Questa voce facoltativa viene usata dai contenitori per compilare le finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="4fbbf-108">This optional entry is used by containers to fill in dialog boxes.</span></span> <span data-ttu-id="4fbbf-109">Il contenitore utilizza questa sottochiave per determinare se includere un oggetto in una finestra di dialogo in cui sono visualizzati i controlli ActiveX.</span><span class="sxs-lookup"><span data-stu-id="4fbbf-109">The container uses this subkey to determine whether to include an object in a dialog box that displays ActiveX Controls.</span></span> <span data-ttu-id="4fbbf-110">Un controllo può omettere questa voce se è progettata per funzionare solo con un contenitore specifico e pertanto non è destinata all'inserimento in altri contenitori.</span><span class="sxs-lookup"><span data-stu-id="4fbbf-110">A control can omit this entry if it is designed to work only with a specific container and therefore does is not intended to be inserted in other containers.</span></span>

 

 




