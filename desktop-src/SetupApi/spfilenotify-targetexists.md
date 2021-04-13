---
description: La \_ notifica TARGETEXISTS SPFILENOTIFY viene inviata alla routine di callback se il file da copiare è stato accodato con il \_ flag di copia sovrascrittura SP e il \_ file esiste già nella directory di destinazione.
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: Messaggio SPFILENOTIFY_TARGETEXISTS (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d0c1a1ffba520789113b0dc78246657a4fe324
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401756"
---
# <a name="spfilenotify_targetexists-message"></a>\_Messaggio SPFILENOTIFY TARGETEXISTS

La **notifica \_ TARGETEXISTS SPFILENOTIFY** viene inviata alla routine di callback se il file da copiare è stato accodato con il \_ flag di copia \_ sovrascrittura SP e il file esiste già nella directory di destinazione. Può essere inviato alla routine di callback da solo o combinato usando l'operatore OR con le notifiche [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) e/o [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md) .


```C++
SPFILENOTIFY_TARGETEXISTS
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) che contiene informazioni sui percorsi per i file di origine e di destinazione.

</dd> <dt>

*Param2* 
</dt> <dd>

Questo parametro non viene usato a meno che la notifica non venga combinata, usando l'operatore OR, con la notifica [**\_ LANGMISMATCH di SPFILENOTIFY**](spfilenotify-langmismatch.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback deve restituire uno dei valori seguenti.



| Codice restituito                                                                          | Descrizione                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**TRUE**</dt> </dl>  | Sovrascrivere il file nella directory di destinazione.<br/> |
| <dl> <dt>**FALSE**</dt> </dl> | Ignora l'operazione di copia corrente.<br/>            |



 

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

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
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

 

 




