---
description: Ottiene un valore booleano che indica se il file di quota per il volume è attualmente in fase di ricompilazione.
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: Proprietà DiskQuotaControl. QuotaFileRebuilding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaFileRebuilding
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e06b73e53670a136e53721b4e6bc6b2f635d601b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977503"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a>Proprietà DiskQuotaControl. QuotaFileRebuilding

Ottiene un valore booleano che indica se il file di quota per il volume è attualmente in fase di ricompilazione.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è impostata su **true** se il file della quota viene ricompilato o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Il file di quote viene ricompilato automaticamente quando le quote sono abilitate nel sistema o quando una o più voci utente sono contrassegnate per l'eliminazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




