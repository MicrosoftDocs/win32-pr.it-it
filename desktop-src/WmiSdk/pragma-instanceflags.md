---
description: Controlla la modalità di creazione o aggiornamento delle istanze a seconda dei flag specificati.
ms.assetid: 9932edf2-2e5f-4c5e-9889-f2be4af11bf2
ms.tgt_platform: multiple
title: pragma instanceflags
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
ms.openlocfilehash: 107325b329fcc51f474dd3ac9ea3a16e8882ff55114012d87a303ac73647bb37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817987"
---
# <a name="pragma-instanceflags"></a>pragma instanceflags

Il comando del preprocessore **pragma instanceflags** controlla la modalità di creazione o aggiornamento delle istanze a seconda dei flag specificati.

Di seguito viene descritta la sintassi:


```mof
#pragma instanceflags ([Flag])
```



*\[ Flag \]* deve essere uno degli argomenti seguenti.



| Flag       | Descrizione                                                                                                |
|------------|------------------------------------------------------------------------------------------------------------|
| createonly | Impedisce al compilatore di modificare le istanze esistenti nel file MOF.                                |
| updateonly | Impedisce al compilatore di creare nuove istanze se non esiste un'istanza specificata nel file MOF. |



 

## <a name="examples"></a>Esempio

L'esempio seguente illustra come usare questo comando.


```mof
#pragma instanceflags("createonly")
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

 

 




