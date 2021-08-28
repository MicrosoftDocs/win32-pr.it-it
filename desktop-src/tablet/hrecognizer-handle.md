---
description: Un handle HRECOGNIZER viene usato per creare un contesto di riconoscimento, recuperare gli attributi e le proprietà del riconoscitore e determinare le proprietà del pacchetto necessarie al riconoscimento per eseguire il riconoscimento.
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: Handle HRECOGNIZER (Recapis.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 192890991dcb7e8b0a0086bbca68a6ccbc2af790d9c7d78e76fe963d268c8240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092451"
---
# <a name="hrecognizer-handle"></a>HRECOGNIZER Handle

Un handle **HRECOGNIZER** viene usato per creare un contesto di riconoscimento, recuperare gli attributi e le proprietà del riconoscitore e determinare le proprietà del pacchetto necessarie al riconoscimento per eseguire il riconoscimento.


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a>Commenti

Le funzioni seguenti usano **HRECOGNIZER.**



| Funzione                                                               | Descrizione                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**CreateRecognizer**](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | Crea un sistema di riconoscimento.<br/>                                                                   |
| [**DestroyRecognizer**](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | Elimina un sistema di riconoscimento.<br/>                                                                  |
| [**GetRecoAttributes**](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | Restituisce gli attributi del riconoscitore.<br/>                                               |
| [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | Crea un contesto di riconoscimento.<br/>                                                           |
| [**DestroyContext**](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | Elimina un contesto di riconoscimento.<br/>                                                          |
| [**GetAllRecognizers**](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | Ottiene tutti i riconoscitori.<br/>                                                                   |
| [**GetResultPropertyList**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | Recupera un elenco di proprietà che il riconoscimento può restituire per un intervallo di risultati.<br/>            |
| [**GetPreferredPacketDescription**](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | Recupera una descrizione del pacchetto che contiene le proprietà del pacchetto utilizzate dal riconoscimento.<br/> |
| [**GetUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | Recupera gli intervalli di punti Unicode supportati dal riconoscimento.<br/>                    |
| [**LoadCachedAttributes**](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | Carica gli attributi memorizzati nella cache di un riconoscitore.<br/>                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                        |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Intestazione<br/>                   | <dl> <dt>Recapis.h</dt> </dl> |



 

 




