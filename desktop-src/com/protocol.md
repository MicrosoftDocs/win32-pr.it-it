---
title: Protocollo
description: Indica che questa classe OLE 2 è inseribile nei contenitori OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Chiave del registro di sistema protocollo COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176cb3fce826a6416270fc35a902621521341e6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298611"
---
# <a name="protocol"></a><span data-ttu-id="be877-104">Protocollo</span><span class="sxs-lookup"><span data-stu-id="be877-104">Protocol</span></span>

<span data-ttu-id="be877-105">Indica che questa classe OLE 2 è inseribile nei contenitori OLE 1.</span><span class="sxs-lookup"><span data-stu-id="be877-105">Indicates that this OLE 2 class is insertable in OLE 1 containers.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="be877-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="be877-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Protocol
         StdFileEditing
            Server = path
            Verb
               0 = verb1
               1 = verb2
               ...
```

## <a name="remarks"></a><span data-ttu-id="be877-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="be877-107">Remarks</span></span>

<span data-ttu-id="be877-108">La voce **StdFileEditing** specifica le informazioni sulla compatibilità OLE 1.</span><span class="sxs-lookup"><span data-stu-id="be877-108">The **StdFileEditing** entry specifies OLE 1 compatibility information.</span></span> <span data-ttu-id="be877-109">Deve essere presente solo se gli oggetti di questa classe possono essere inseriti in contenitori OLE 1.</span><span class="sxs-lookup"><span data-stu-id="be877-109">It should be present only if objects of this class are insertable in OLE 1 containers.</span></span>

<span data-ttu-id="be877-110">**Server** specifica il percorso completo dell'applicazione server OLE 2 e il **verbo** specifica i verbi.</span><span class="sxs-lookup"><span data-stu-id="be877-110">**Server** specifies the full path to the OLE 2 server application and **Verb** specifies the verbs.</span></span> <span data-ttu-id="be877-111">Il verbo 0 è il verbo principale e i verbi aggiuntivi devono essere numerati consecutivamente.</span><span class="sxs-lookup"><span data-stu-id="be877-111">Verb 0 is the primary verb and additional verbs must be numbered consecutively.</span></span>

 

 




