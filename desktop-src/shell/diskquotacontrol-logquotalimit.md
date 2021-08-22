---
description: Imposta o ottiene un valore booleano che indica se verrà effettuata una voce del registro eventi di sistema quando un utente supera il limite di quota assegnato.
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: DiskQuotaControl.LogQuotaLimit - proprietà
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
ms.openlocfilehash: 5f10710c5a16feb946caa78394d5e57e5d7d4884a50d45dc3e37291f40e7d283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455881"
---
# <a name="diskquotacontrollogquotalimit-property"></a>DiskQuotaControl.LogQuotaLimit - proprietà

Imposta o ottiene un valore booleano che indica se verrà effettuata una voce del registro eventi di sistema quando un utente supera il limite di quota assegnato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà è impostata su **TRUE se** viene effettuata una voce del registro eventi di sistema quando l'utente supera il limite di quota oppure FALSE in caso **contrario.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**Oggetto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> <dt>

[**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




