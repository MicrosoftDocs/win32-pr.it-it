---
description: Imposta o ottiene un valore booleano che indica se verrà eseguita una voce del registro eventi di sistema quando un utente supera il limite di quota assegnato.
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: Proprietà DiskQuotaControl. LogQuotaLimit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3db64d7fb06ed8bfb7ba8c2483eb413f3f01a224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977170"
---
# <a name="diskquotacontrollogquotalimit-property"></a>Proprietà DiskQuotaControl. LogQuotaLimit

Imposta o ottiene un valore booleano che indica se verrà eseguita una voce del registro eventi di sistema quando un utente supera il limite di quota assegnato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è impostata su **true** se viene eseguita una voce del registro eventi di sistema quando l'utente supera il limite di quota o **false** in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**Oggetto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> <dt>

[**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




