---
title: Identificatori di formato
description: I valori dei set di proprietà vengono archiviati in una sezione contrassegnata con un FMTID univoco.
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- Identificatori di formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ec9e9843b1dfe843e89ebf85eadbbcb5da8cb58dfc1b289eb88c844aae7456
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663151"
---
# <a name="format-identifiers"></a>Identificatori di formato

I valori dei set di proprietà vengono archiviati in una sezione contrassegnata con un FMTID univoco. Ad esempio, fmTID per il set di proprietà Informazioni di riepilogo COM è **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.

Per definire un FMTID per il set di proprietà Informazioni di riepilogo, usare la macro **DEFINE \_ GUID** in un file di inclusione per il codice che modifica il set di proprietà.


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



Qualsiasi codice che richiede FMTID per il set di proprietà Informazioni di riepilogo può accedervi tramite la *variabile \_ SummaryInformation fmTID.*

Quando si archiviano i set [**di proprietà nelle istanze di IStorage,**](/windows/desktop/api/Objidl/nn-objidl-istorage) convertire FMTID in un nome di stringa per l'oggetto di archiviazione.

 

 




