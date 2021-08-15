---
description: Ottiene il limite di quota predefinito come stringa di testo.
title: DiskQuotaControl.DefaultQuotaLimitText - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimitText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ea1b02e0-c480-4ef1-b6e0-1ec202d5f3c5
ms.openlocfilehash: 378d06286a0334cf6ca3056038f45be3a5919b4fd2aa88934957122bc751c141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094228"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a>DiskQuotaControl.DefaultQuotaLimitText - proprietà

Ottiene il limite di quota predefinito come stringa di testo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a>Valore proprietà

Valore stringa che contiene il limite di quota predefinito per i nuovi utenti del volume. Ad esempio, se la quota predefinita è 10,5 MB, il valore della proprietà è "10,5 MB". Se il volume non ha una quota predefinita, la proprietà viene impostata su "Nessun limite" o sull'equivalente localizzato.

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

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




