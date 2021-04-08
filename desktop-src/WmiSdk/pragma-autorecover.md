---
description: Aggiunge un file MOF all'elenco di file compilati durante il ripristino del repository.
ms.assetid: 8901c04e-f8c1-45b0-b69d-e2ebc948f088
ms.tgt_platform: multiple
title: pragma autocover
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
ms.openlocfilehash: 9bb1cfca44e0bc5437d05d721ffcd57203e5aa9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968188"
---
# <a name="pragma-autorecover"></a>pragma autocover

Il comando **pragma autocover** preprocessore consente di aggiungere un file MOF all'elenco di file compilati durante il ripristino del repository. L'elenco dei file MOF di **autocover** è archiviato in questa chiave del registro di sistema:

**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **autocover file MOF**

WMI controlla l'integrità del repository WMI quando il sistema operativo avvia WMI. Se il repository è danneggiato, WMI ricompila automaticamente il repository e ricompila tutti i file MOF elencati in questa chiave nel registro di sistema.

Di seguito viene descritta la sintassi per il comando pragma autocover:


```mof
#pragma autorecover
```



Quando si usa questo comando, è tuttavia necessario osservare le restrizioni seguenti:

-   WMI non è in grado di ripristinare i file MOF presenti in un computer remoto.

    Pertanto, i file MOF elencati in questa chiave del registro di sistema devono trovarsi nel computer locale.

-   Non è possibile specificare le opzioni della riga di comando utilizzate dal compilatore MOF quando WMI recupera un file MOF.

    Pertanto, è necessario includere i comandi [pragma](-pragma.md) nel file MOF che rendono inutili le opzioni della riga di comando. Nell'esempio seguente viene descritta un'opzione della riga di comando comune che WMI non utilizza quando si recupera un file MOF da questa chiave del registro di sistema: **mofcomp-N:root \\ test mymof. mof**

    È tuttavia possibile specificare lo spazio dei nomi utilizzando un comando [pragma](-pragma.md) nel file MOF.

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

[Comandi del preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 




