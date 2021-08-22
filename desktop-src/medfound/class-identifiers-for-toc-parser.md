---
description: Le classi seguenti sono dichiarate e associate agli identificatori di classe (CLSID) in wmcodecdsp.h.
ms.assetid: f82d92dc-fbce-4274-a10f-72fa8dd776cc
title: Identificatori di classe per il parser sommario (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c340ec32b8de4ce42619d57f6e44da9d77d0eead4940dc94d90baec4d349ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664691"
---
# <a name="class-identifiers-for-table-of-contents-parser"></a>Identificatori di classe per il parser sommario

Le classi seguenti sono dichiarate e associate agli identificatori di classe (CLSID) in wmcodecdsp.h.



| Nome di classe       | Nome descrittivo dell'oggetto |
|------------------|----------------------|
| CTocEntry        | Voce del sommario            |
| CTocEntryList    | Elenco voci sommario       |
| CToc             | Sommario                  |
| CTocCollection   | Raccolta sommario       |
| CTocParser       | Parser sommario           |
| CTocGeneratorDmo | Generatore di sommario        |



 

La tabella precedente fornisce un nome descrittivo per ogni classe. Questa documentazione usa questi nomi descrittivi per fare riferimento alle istanze delle classi. Ad esempio, la documentazione fa riferimento a un'istanza della classe CTocEntry come oggetto TOC Entry.

Nel codice è possibile usare **\_ \_ uuidof** per fare riferimento ai CLSID. Ad esempio, è possibile usare il codice seguente per fare riferimento al CLSID per CTocGeneratorDmo.


```C++
__uuidof(CTocGeneratorDmo)
```



### <a name="clsid-constants-defined-in-wmcodecdsph"></a>Costanti CLSID definite in Wmcodecdsp.h

In alternativa all'uso **\_ \_ di uuidof**, è possibile usare costanti per fare riferimento ai CLSID. Le costanti seguenti sono definite in wmcodecdsp.h



| Nome di classe     | Costante CLSID        |
|----------------|-----------------------|
| CTocEntry      | CLSID \_ CTocEntry      |
| CTocEntryList  | CLSID \_ CTocEntryList  |
| CToc           | CLSID \_ CToc           |
| CTocCollection | CLSID \_ CTocCollection |
| CTocParser     | CLSID \_ CTocParser     |



 

### <a name="clsid-constants-defined-in-wmcodecdspuuidlib"></a>Costanti CLSID definite in Wmcodecdspuuid.lib

La costante CLSID seguente viene dichiarata, ma non definita, in wmcodecdsp.h. Per usarlo nel codice, è necessario collegarsi a wmcodecdspuuid.lib.



| Nome di classe       | Costante CLSID          |
|------------------|-------------------------|
| CTocGeneratorDmo | CLSID \_ CTocGeneratorDmo |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmvdspa.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti del parser sommario](toc-parser-objects.md)
</dt> </dl>

 

 




