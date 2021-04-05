---
title: Uso del servizio directory delle celle (CDS)
description: Se si dispone di CDS, è possibile usarlo anziché Microsoft Locator.
ms.assetid: df4b8db1-08f1-4ed8-895d-236199289e87
keywords:
- RPC (Remote Procedure Call), attività, uso del servizio directory delle celle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0029bf78308d6963d615daa04eaf87f3617ebbb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710582"
---
# <a name="using-the-cell-directory-service-cds"></a>Uso del servizio directory delle celle (CDS)

Se si dispone di CDS, è possibile usarlo anziché Microsoft Locator. Modificare le voci del registro di sistema come indicato di seguito:

``` syntax
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    NetworkAddress
 
HKEY_LOCAL_MACHINE
    Software
        Microsoft
            Rpc
                Name Service
                    Endpoint
```

La modifica di queste voci punterà a un computer gateway che esegue NSID. Verrà usato come localizzatore master. In caso di arresto anomalo, non verrà cercata alcuna sostituzione.

 

 




