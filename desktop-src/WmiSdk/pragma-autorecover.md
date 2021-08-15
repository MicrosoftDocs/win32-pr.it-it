---
description: Aggiunge un file MOF all'elenco di file compilati durante il ripristino del repository.
ms.assetid: 8901c04e-f8c1-45b0-b69d-e2ebc948f088
ms.tgt_platform: multiple
title: pragma autorecover
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: cc36191482731e77d0f82c4e3734350da2f6ed2fbd3faad7b2972dca4e0e6bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992701"
---
# <a name="pragma-autorecover"></a>pragma autorecover

Il **comando del preprocessore pragma autorecover** aggiunge un file MOF all'elenco di file compilati durante il ripristino del repository. L'elenco dei file MOF **di salvataggio automatico** è archiviato in questa chiave del Registro di sistema:

**HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **autorecover mofs**

WMI controlla l'integrità del repository WMI quando il sistema operativo avvia WMI. Se il repository è danneggiato, WMI ricompila automaticamente il repository e ricompila tutti i file MOF elencati in questa chiave nel Registro di sistema.

Di seguito viene descritta la sintassi per il comando pragma autorecover:


```mof
#pragma autorecover
```



Tuttavia, è necessario osservare le restrizioni seguenti quando si usa questo comando:

-   WMI non è in grado di ripristinare i file MOF che si trovano in un computer remoto.

    Pertanto, i file MOF elencati in questa chiave del Registro di sistema devono risiedere nel computer locale.

-   Non è possibile specificare le opzioni della riga di comando utilizzate dal compilatore MOF quando WMI recupera un file MOF.

    Pertanto, è necessario includere nel file MOF comandi [pragma](-pragma.md) che rendono non necessarie le opzioni della riga di comando. L'esempio seguente descrive un'opzione della riga di comando comune che WMI non usa durante il ripristino di un file MOF da questa chiave del Registro di sistema: **mofcomp -N:Root \\ Test mymof.mof**

    Tuttavia, è possibile specificare lo spazio dei nomi usando un [comando pragma](-pragma.md) nel file MOF.

    ```mof
    #pragma namespace ("\\\\.\\Root\\test")
    ```

    

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Comandi per il preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 




