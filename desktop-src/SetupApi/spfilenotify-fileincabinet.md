---
description: La \_ notifica SPFILENOTIFY FILEINCABINET viene inviata a una routine di callback da SetupIterateCabinet per ogni file trovato nell'archivio. La routine di callback deve restituire un valore che indica se estrarre il file.
ms.assetid: c6d89759-c0d4-4741-b992-43eaa0dc4f01
title: Messaggio SPFILENOTIFY_FILEINCABINET (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496db3cef814f2bf366f4cb6f91132efe01a2406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318614"
---
# <a name="spfilenotify_fileincabinet-message"></a>\_Messaggio SPFILENOTIFY FILEINCABINET

La notifica **SPFILENOTIFY \_ FILEINCABINET** viene inviata a una routine di callback da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) per ogni file trovato nell'archivio. La routine di callback deve restituire un valore che indica se estrarre il file.


```C++
SPFILENOTIFY_FILEINCABINET
  Param1 = (UINT) FileInCabinetInfo;
  Param2 = (UINT) CabinetFile;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a un [**file \_ nella struttura di \_ \_ informazioni sul cabinet**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) che contiene informazioni sul file nell'archivio.

</dd> <dt>

*Param2* 
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il nome file del file CAB.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback deve restituire uno dei seguenti elementi.



| Codice restituito                                                                                 | Descrizione                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_Ignora FILEOP**</dt> </dl> | Non estrarre il file, ignorarlo.<br/> |
| <dl> <dt>**\_doit FILEOP**</dt> </dl> | Estrai il file.<br/>                 |



 

Se la routine di callback restituisce FILEOP \_ doit, il nome da usare per il file estratto deve essere specificato nel membro **FullTargetName** del [**file nella struttura di \_ \_ \_ informazioni del cabinet**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) passato alla routine in *param1*.

> [!Note]  
> Non esiste alcuna routine di callback predefinita del cabinet. L'applicazione di installazione deve fornire una routine di callback per gestire le notifiche inviate da [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Overview](overview.md)
</dt> <dt>

[Notifications](notifications.md)
</dt> <dt>

[**\_informazioni su file in \_ cabinet \_**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a)
</dt> <dt>

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

 




