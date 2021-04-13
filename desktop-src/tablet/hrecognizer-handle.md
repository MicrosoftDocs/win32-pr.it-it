---
description: Un handle HRECOGNIZER viene usato per creare un contesto di riconoscimento, recuperare gli attributi e le proprietà del riconoscimento e determinare le proprietà dei pacchetti richieste dal riconoscimento per eseguire il riconoscimento.
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: Handle HRECOGNIZER (riepilogo. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e78086ff86453ef8b0157bb3b274f3c47be0dc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343746"
---
# <a name="hrecognizer-handle"></a>Handle HRECOGNIZER

Un handle **HRECOGNIZER** viene usato per creare un contesto di riconoscimento, recuperare gli attributi e le proprietà del riconoscimento e determinare le proprietà dei pacchetti richieste dal riconoscimento per eseguire il riconoscimento.


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a>Commenti

Le funzioni seguenti usano un **HRECOGNIZER**.



| Funzione                                                               | Descrizione                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**CreateRecognizer**](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | Crea un riconoscitore.<br/>                                                                   |
| [**DestroyRecognizer**](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | Elimina definitivamente un riconoscimento.<br/>                                                                  |
| [**GetRecoAttributes**](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | Restituisce gli attributi del riconoscimento.<br/>                                               |
| [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | Crea un contesto del riconoscitore.<br/>                                                           |
| [**DestroyContext**](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | Elimina un contesto del riconoscitore.<br/>                                                          |
| [**GetAllRecognizers**](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | Ottiene tutti i riconoscitori.<br/>                                                                   |
| [**GetResultPropertyList**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | Recupera un elenco di proprietà che il riconoscimento può restituire per un intervallo di risultati.<br/>            |
| [**GetPreferredPacketDescription**](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | Recupera una descrizione del pacchetto che contiene le proprietà del pacchetto utilizzate dal riconoscimento.<br/> |
| [**GetUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | Recupera gli intervalli di punti Unicode supportati dal riconoscimento.<br/>                    |
| [**LoadCachedAttributes**](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | Carica gli attributi memorizzati nella cache di un riconoscimento.<br/>                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Riepilogo. h</dt> </dl> |



 

 




