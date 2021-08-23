---
description: La notifica SPFILENOTIFY TARGETEXISTS viene inviata alla routine di callback se il file da copiare è stato accodato con il \_ flag SP \_ COPY NOOVERWRITE e tale file esiste già nella \_ directory di destinazione.
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: SPFILENOTIFY_TARGETEXISTS messaggio (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51f845d7ccb41b330f6365eff269645d08e58597e7e6dd3e9acc7a7f0300c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664741"
---
# <a name="spfilenotify_targetexists-message"></a>SPFILENOTIFY \_ TARGETEXISTS MESSAGE

La **notifica SPFILENOTIFY \_ TARGETEXISTS** viene inviata alla routine di callback se il file da copiare è stato accodato con il flag SP \_ COPY NOOVERWRITE e tale file esiste già nella \_ directory di destinazione. Può essere inviato alla routine di callback da solo o in combinazione, usando l'operatore OR, con le notifiche [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) e/o [**SPFILENOTIFY \_ TARGETNEWER.**](spfilenotify-targetnewer.md)


```C++
SPFILENOTIFY_TARGETEXISTS
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a [**una struttura FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) che contiene informazioni sui percorsi dei file di origine e di destinazione.

</dd> <dt>

*Param2* 
</dt> <dd>

Questo parametro non viene utilizzato a meno che questa notifica non venga combinata, tramite l'operatore OR, con la notifica [**SPFILENOTIFY \_ LANGMISMATCH.**](spfilenotify-langmismatch.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback deve restituire uno dei valori seguenti.



| Codice restituito                                                                          | Descrizione                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**Vero**</dt> </dl>  | Sovrascrivere il file nella directory di destinazione.<br/> |
| <dl> <dt>**False**</dt> </dl> | Ignorare l'operazione di copia corrente.<br/>            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Overview](overview.md)
</dt> <dt>

[Notifications](notifications.md)
</dt> <dt>

[**Filepaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




