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
ms.openlocfilehash: 0d3b5b1fa209be7fd472a87aec25a5e590d93c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885234"
---
# <a name="pragma-deleteclass"></a>pragma deleteclass

Il comando per il preprocessore **pragma deleteclass** Elimina una classe esistente e le relative istanze dal repository.

Di seguito viene descritta la sintassi:


```mof
#pragma deleteclass("ClassName", [Flag])
```



*NomeClasse* è il nome della classe che il compilatore MOF Elimina dallo spazio dei nomi corrente.

Il *\[ flag \]* deve essere uno degli argomenti seguenti.



| Flag   | Descrizione                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| fail   | Causa la chiusura del compilatore MOF con un messaggio di errore se la classe non esiste già nel repository. |
| nofail | Determina la continuazione del compilatore MOF anche se la classe non esiste già.                                |



 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come utilizzare questo comando.


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

 

 




