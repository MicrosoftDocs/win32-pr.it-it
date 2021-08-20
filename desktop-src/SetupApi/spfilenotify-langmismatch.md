---
description: La notifica SPFILENOTIFY LANGMISMATCH viene inviata alla routine di callback se la lingua del file da copiare non corrisponde alla lingua di un \_ file di destinazione esistente.
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: SPFILENOTIFY_LANGMISMATCH messaggio (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50cae8788e3ffac2de5cc7fc115b9363b8ad4591a0a4dd2447a3f86f735bec1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964469"
---
# <a name="spfilenotify_langmismatch-message"></a>MESSAGGIO SPFILENOTIFY \_ LANGMISMATCH

La **notifica SPFILENOTIFY \_ LANGMISMATCH** viene inviata alla routine di callback se la lingua del file da copiare non corrisponde alla lingua di un file di destinazione esistente. Può essere inviato alla routine di callback da solo o in combinazione, usando l'operatore OR, con [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md) e/o [**SPFILENOTIFY \_ TARGETNEWER.**](spfilenotify-targetnewer.md)


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a [**una struttura FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) che contiene informazioni sui percorsi dei file di origine e di destinazione.

</dd> <dt>

*Param2* 
</dt> <dd>

Identifica le lingue non corrispondenti. Questo membro ha l'identificatore di lingua del file di origine nella parola in basso e l'identificatore della lingua del file di destinazione esistente nella parola superiore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

La routine di callback deve restituire uno dei valori seguenti.



| Codice restituito                                                                          | Descrizione                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**Vero**</dt> </dl>  | Copiare il file e sovrascrivere il file esistente.<br/>               |
| <dl> <dt>**False**</dt> </dl> | Ignorare l'operazione di copia. Non sovrascrivere il file esistente.<br/> |



 

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

 

 




