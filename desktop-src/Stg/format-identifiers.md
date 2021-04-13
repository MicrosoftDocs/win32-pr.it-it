---
title: Identificatori di formato
description: I valori del set di proprietà vengono archiviati in una sezione contrassegnata con un FMTID univoco.
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- Identificatori di formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0202cd1287c3b4fef6e9e2b56e272541a03425b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329543"
---
# <a name="format-identifiers"></a><span data-ttu-id="22fab-104">Identificatori di formato</span><span class="sxs-lookup"><span data-stu-id="22fab-104">Format Identifiers</span></span>

<span data-ttu-id="22fab-105">I valori del set di proprietà vengono archiviati in una sezione contrassegnata con un FMTID univoco.</span><span class="sxs-lookup"><span data-stu-id="22fab-105">Property set values are stored in a section tagged with a unique FMTID.</span></span> <span data-ttu-id="22fab-106">Ad esempio, FMTID per il set di proprietà informazioni di riepilogo COM è **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.</span><span class="sxs-lookup"><span data-stu-id="22fab-106">For example, the FMTID for the COM Summary Information property set is **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.</span></span>

<span data-ttu-id="22fab-107">Per definire un FMTID per il set di proprietà informazioni di riepilogo, utilizzare la macro **\_ GUID Definisci** in un file di inclusione per il codice che modifica il set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="22fab-107">To define a FMTID for the Summary Information property set, use the **DEFINE\_GUID** macro in an include file for the code that manipulates the property set.</span></span>


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



<span data-ttu-id="22fab-108">Il codice che richiede FMTID per il set di proprietà informazioni di riepilogo può accedervi tramite la *variabile \_ SummaryInformation di fmtid* .</span><span class="sxs-lookup"><span data-stu-id="22fab-108">Any code that requires the FMTID for the Summary Information property set, can access it through the *FMTID\_SummaryInformation* variable.</span></span>

<span data-ttu-id="22fab-109">Quando si archiviano i set di proprietà nelle istanze di [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , convertire fmtid in un nome di stringa per l'oggetto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="22fab-109">When storing property sets in [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) instances, convert the FMTID to a string name for the storage object.</span></span>

 

 




