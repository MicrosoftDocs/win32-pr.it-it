---
description: Elimina un'istanza esistente di una classe dal repository.
ms.assetid: 4389f831-a60e-4198-a55a-79189d10a38a
ms.tgt_platform: multiple
title: pragma deleteinstance
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
ms.openlocfilehash: 29739f1d95cf5c8352c2b7822dbc3da7777f41f69fc5086631e0069c3b832623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316846"
---
# <a name="pragma-deleteinstance"></a>pragma deleteinstance

Il **comando pragma deleteinstance** elimina un'istanza esistente di una classe dal repository.

Di seguito viene descritta la sintassi per questo comando:


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



*InstanceId* è un identificatore univoco dell'istanza che il compilatore MOF elimina dallo spazio dei nomi corrente.

*\[ Flag \]* deve essere uno degli argomenti seguenti.



| Flag   | Descrizione                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| fail   | Causa la chiusura del compilatore MOF con un messaggio di errore se la classe non esiste già nel repository. |
| nofail | Fa sì che il compilatore MOF continui anche se la classe non esiste già.                                |



 

## <a name="examples"></a>Esempio

L'esempio seguente illustra come usare questo comando.


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

[Comandi per il preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 




