---
description: La \_ notifica SPFILENOTIFY FILEOPDELAYED viene inviata da SetupInstallFileEx o SetupCommitFileQueue a una routine di callback quando un'operazione su file è stata posticipata perché il file è in uso. L'operazione verrà elaborata al successivo riavvio del sistema.
ms.assetid: a0b38e2b-2390-49e5-b288-77c31636e696
title: Messaggio SPFILENOTIFY_FILEOPDELAYED (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38975506ff998ec09c4549ec95d9ddb620466cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880837"
---
# <a name="spfilenotify_fileopdelayed-message"></a>\_Messaggio SPFILENOTIFY FILEOPDELAYED

La notifica **SPFILENOTIFY \_ FILEOPDELAYED** viene inviata da [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) o [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) a una routine di callback quando un'operazione su file è stata posticipata perché il file è in uso. L'operazione verrà elaborata al successivo riavvio del sistema.


```C++
SPFILENOTIFY_FILEOPDELAYED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Param1* 
</dt> <dd>

Puntatore a una struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

Se l'operazione ritardata è un'operazione di copia dei file, la struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) contiene le informazioni seguenti.



| Membro filePaths | Valore                                |
|------------------|--------------------------------------|
| **Win32Error**   | Nessun \_ errore                            |
| **Flag**        | copia di FILEOP \_                         |
| **Origine**       | Percorso completo del file temporaneo.     |
| **Destinazione**       | Percorso completo del file di destinazione effettivo. |



 

Il file temporaneo verrà copiato nella directory di destinazione al riavvio del sistema. Le funzioni di installazione generano automaticamente un percorso per il file temporaneo.

Se l'operazione ritardata è un'operazione di eliminazione di file, la struttura [**FILEpaths**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) contiene le informazioni seguenti.



| Membro filePaths | Valore                                |
|------------------|--------------------------------------|
| **Win32Error**   | Nessun \_ errore                            |
| **Flag**        | eliminazione di FILEOP \_                       |
| **Origine**       | NULL                                 |
| **Destinazione**       | Percorso completo del file da eliminare. |



 

</dd> <dt>

*Param2* 
</dt> <dd>

Non viene utilizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il valore restituito viene ignorato.

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

[**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




