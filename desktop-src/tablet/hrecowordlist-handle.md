---
description: Un handle HRECOWORDLIST viene usato per gestire un elenco di parole collegato a un contesto di riconoscimento. Per migliorare i risultati del riconoscimento, usare un elenco di parole.
ms.assetid: 7333307b-1857-48a7-bb9f-bdbd8530f093
title: Handle HRECOWORDLIST (riepilogo. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e5d33862cacb7040a26edc23d7db04c57206c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526574"
---
# <a name="hrecowordlist-handle"></a>Handle HRECOWORDLIST

Un handle **HRECOWORDLIST** viene usato per gestire un elenco di parole collegato a un contesto di riconoscimento. Per migliorare i risultati del riconoscimento, usare un elenco di parole.


```C++
typedef HANDLE HRECOWORDLIST;
```



## <a name="remarks"></a>Commenti

La funzione seguente usa un **HRECOWORDLIST**.



| Funzione                                         | Descrizione                                         |
|--------------------------------------------------|-----------------------------------------------------|
| [**AddWordsToWordList**](/windows/desktop/api/recapis/nf-recapis-addwordstowordlist) | Aggiunge una o più parole all'elenco di parole.<br/> |
| [**DestroyWordList**](/windows/desktop/api/recapis/nf-recapis-destroywordlist)       | Elimina definitivamente l'elenco di parole corrente.<br/>          |
| [**MakeWordList**](/windows/desktop/api/recapis/nf-recapis-makewordlist)             | Crea un elenco di parole.<br/>                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Riepilogo. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzione WordList**](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 




