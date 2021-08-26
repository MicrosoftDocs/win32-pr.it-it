---
description: Elimina una classe esistente e le relative istanze dal repository.
ms.assetid: 6f96d14a-16ab-4e83-a75f-5dbf162d1692
ms.tgt_platform: multiple
title: pragma deleteclass
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
ms.openlocfilehash: 3cb62c9d90d5ac6346e25eaa3c254e0c6dd595805ec6901376ce9dccdf648289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996291"
---
# <a name="pragma-deleteclass"></a>pragma deleteclass

Il comando del preprocessore **pragma deleteclass** elimina una classe esistente e le relative istanze dal repository.

Di seguito viene descritta la sintassi:


```mof
#pragma deleteclass("ClassName", [Flag])
```



*ClassName* è il nome della classe che il compilatore MOF elimina dallo spazio dei nomi corrente.

*\[ Il \]* flag deve essere uno degli argomenti seguenti.



| Flag   | Descrizione                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| fail   | Causa la chiusura del compilatore MOF con un messaggio di errore se la classe non esiste già nel repository. |
| nofail | Fa sì che il compilatore MOF continui anche se la classe non esiste già.                                |



 

## <a name="examples"></a>Esempio

L'esempio seguente illustra come usare questo comando.


```mof
#pragma deleteclass("MyClass1",FAIL)
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

 

 




