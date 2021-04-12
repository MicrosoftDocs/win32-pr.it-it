---
description: Controlla il modo in cui le istanze vengono create o aggiornate a seconda dei flag specificati.
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
ms.openlocfilehash: acc05e201fcf153ab2156d4a360ce36b4539cd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233818"
---
# <a name="pragma-instanceflags"></a>pragma instanceflags

Il comando per il preprocessore **pragma instanceflags** controlla il modo in cui le istanze vengono create o aggiornate a seconda dei flag specificati.

Di seguito viene descritta la sintassi:


```mof
#pragma instanceflags ([Flag])
```



Il *\[ flag \]* deve essere uno degli argomenti seguenti.



| Flag       | Descrizione                                                                                                |
|------------|------------------------------------------------------------------------------------------------------------|
| createonly | Impedisce al compilatore di modificare le istanze esistenti nel file MOF.                                |
| UpdateOnly | Impedisce al compilatore di creare nuove istanze se non esiste un'istanza specificata nel file MOF. |



 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come utilizzare questo comando.


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

[Comandi del preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 




