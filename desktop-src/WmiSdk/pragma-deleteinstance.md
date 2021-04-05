---
description: Elimina un'istanza esistente di una classe dal repository.
ms.assetid: 4389f831-a60e-4198-a55a-79189d10a38a
ms.tgt_platform: multiple
title: pragma DeleteInstance
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
ms.openlocfilehash: 10d4c735f1e59533b57ae1814cfb8e36b2c1ad76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049645"
---
# <a name="pragma-deleteinstance"></a>pragma DeleteInstance

Il comando **pragma DeleteInstance** Elimina un'istanza esistente di una classe dal repository.

Di seguito viene descritta la sintassi per questo comando:


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



*InstanceID* è un identificatore univoco dell'istanza eliminata dal compilatore MOF dallo spazio dei nomi corrente.

Il *\[ flag \]* deve essere uno degli argomenti seguenti.



| Flag   | Descrizione                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| fail   | Causa la chiusura del compilatore MOF con un messaggio di errore se la classe non esiste già nel repository. |
| nofail | Determina la continuazione del compilatore MOF anche se la classe non esiste già.                                |



 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come utilizzare questo comando.


```mof
#pragma deleteinstance(
    "MSFT_RisingFallingTemplate.id='TestRisingFallingCorrId'",
    nofail)
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

 

 




