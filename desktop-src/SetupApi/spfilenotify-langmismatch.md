---
description: La \_ notifica SPFILENOTIFY LANGMISMATCH viene inviata alla routine di callback se la lingua del file da copiare non corrisponde alla lingua di un file di destinazione esistente.
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: Messaggio SPFILENOTIFY_LANGMISMATCH (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3d7828c90dd4dabb8e1cb73a8dcca7ae33ebd3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318213"
---
# <a name="spfilenotify_langmismatch-message"></a>\_Messaggio SPFILENOTIFY LANGMISMATCH

La notifica **SPFILENOTIFY \_ LANGMISMATCH** viene inviata alla routine di callback se la lingua del file da copiare non corrisponde alla lingua di un file di destinazione esistente. Può essere inviato alla routine di callback da solo o combinato usando l'operatore OR con [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md) e/o [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md).


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) che contiene informazioni sui percorsi dei file di origine e di destinazione.

</dd> <dt>

*Param2* 
</dt> <dd>

Identifica le lingue non corrispondenti. Questo membro ha l'identificatore di lingua del file di origine nella parola bassa e l'identificatore della lingua del file di destinazione esistente nella parola alta.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback deve restituire uno dei valori seguenti.



| Codice restituito                                                                          | Descrizione                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**TRUE**</dt> </dl>  | Copiare il file e sovrascrivere il file esistente.<br/>               |
| <dl> <dt>**FALSE**</dt> </dl> | Ignorare l'operazione di copia. Non sovrascrivere il file esistente.<br/> |



 

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

 

 




