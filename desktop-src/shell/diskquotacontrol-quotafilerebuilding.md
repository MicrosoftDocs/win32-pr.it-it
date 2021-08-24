---
description: Ottiene un valore booleano che indica se il file di quota per il volume è attualmente in fase di ricompilato.
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: DiskQuotaControl.QuotaFileRebuilding - proprietà
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
ms.openlocfilehash: 8e90d5d920392b9b518fed619aeb4f8c7b99d830fad9f6f901c59fe6128ca94b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710521"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a>DiskQuotaControl.QuotaFileRebuilding - proprietà

Ottiene un valore booleano che indica se il file di quota per il volume è attualmente in fase di ricompilato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è impostata su **TRUE** se il file di quota viene ricompilato oppure **SU FALSE in caso** contrario.

## <a name="remarks"></a>Commenti

Il file di quota viene ricompilato automaticamente quando le quote sono abilitate nel sistema o quando una o più voci utente sono contrassegnate per l'eliminazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




