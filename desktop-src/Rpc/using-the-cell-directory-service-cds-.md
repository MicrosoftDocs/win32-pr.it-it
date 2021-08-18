---
title: Uso del servizio directory cellulare (CDS)
description: Se si dispone di CDS, è possibile usarlo al posto di Microsoft Locator.
ms.assetid: df4b8db1-08f1-4ed8-895d-236199289e87
keywords:
- Chiamata di procedura remota RPC, attività, uso del servizio directory delle celle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df9058d917396a4e2e2dc3579768c3f3d5b46242b34c0fa5411c6d2204ed20b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010638"
---
# <a name="using-the-cell-directory-service-cds"></a>Uso del servizio directory cellulare (CDS)

Se si dispone di CDS, è possibile usarlo al posto di Microsoft Locator. Modificare le voci del Registro di sistema come illustrato:

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

La modifica di queste voci farà riferimento a un computer gateway che esegue l'NSID. Verrà usato come localizzatore master. In caso di arresto anomalo, non verrà cercata alcuna sostituzione.

 

 




