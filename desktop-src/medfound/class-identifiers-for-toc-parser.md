---
description: Le classi seguenti sono dichiarate e associate a identificatori di classe (CLSID) in wmcodecdsp. h.
ms.assetid: f82d92dc-fbce-4274-a10f-72fa8dd776cc
title: Identificatori di classe per il parser della tabella dei contenuti (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5108855c687085e77ce36aa14b3424732e25572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305508"
---
# <a name="class-identifiers-for-table-of-contents-parser"></a>Identificatori di classe per il parser della tabella dei contenuti

Le classi seguenti sono dichiarate e associate a identificatori di classe (CLSID) in wmcodecdsp. h.



| Nome di classe       | Nome descrittivo dell'oggetto |
|------------------|----------------------|
| CTocEntry        | Voce Sommario            |
| CTocEntryList    | Elenco voci Sommario       |
| CToc             | Sommario                  |
| CTocCollection   | Raccolta TOC       |
| CTocParser       | Parser Sommario           |
| CTocGeneratorDmo | Generatore Sommario        |



 

La tabella precedente fornisce un nome descrittivo dell'oggetto per ogni classe. In questa documentazione vengono utilizzati i nomi descrittivi per fare riferimento alle istanze delle classi. La documentazione, ad esempio, fa riferimento a un'istanza della classe CTocEntry come oggetto voce del sommario.

Nel codice è possibile usare **\_ \_ uuidof** per fare riferimento ai CLSID. Ad esempio, è possibile usare il codice seguente per fare riferimento al CLSID per CTocGeneratorDmo.


```C++
__uuidof(CTocGeneratorDmo)
```



### <a name="clsid-constants-defined-in-wmcodecdsph"></a>Costanti CLSID definite in Wmcodecdsp. h

In alternativa all'utilizzo di **\_ \_ uuidof**, è possibile utilizzare le costanti per fare riferimento ai CLSID. Le costanti seguenti sono definite in wmcodecdsp. h



| Nome di classe     | Costante CLSID        |
|----------------|-----------------------|
| CTocEntry      | \_CTOCENTRY CLSID      |
| CTocEntryList  | \_CTOCENTRYLIST CLSID  |
| CToc           | \_CTOC CLSID           |
| CTocCollection | \_CTOCCOLLECTION CLSID |
| CTocParser     | \_CTOCPARSER CLSID     |



 

### <a name="clsid-constants-defined-in-wmcodecdspuuidlib"></a>Costanti CLSID definite in Wmcodecdspuuid. lib

La costante CLSID seguente è dichiarata, ma non definita, in wmcodecdsp. h. Per usarlo nel codice, è necessario eseguire il collegamento a wmcodecdspuuid. lib.



| Nome di classe       | Costante CLSID          |
|------------------|-------------------------|
| CTocGeneratorDmo | \_CTOCGENERATORDMO CLSID |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmvdspa.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti parser del sommario](toc-parser-objects.md)
</dt> </dl>

 

 




