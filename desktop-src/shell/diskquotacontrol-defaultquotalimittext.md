---
description: Ottiene il limite di quota predefinito come stringa di testo.
title: Proprietà DiskQuotaControl. DefaultQuotaLimitText
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
ms.openlocfilehash: 442e9094c62f22c3d990cf1112d145a1b2838e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128442"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a>Proprietà DiskQuotaControl. DefaultQuotaLimitText

Ottiene il limite di quota predefinito come stringa di testo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a>Valore proprietà

Valore stringa che contiene il limite di quota predefinito per i nuovi utenti del volume. Se, ad esempio, la quota predefinita è 10,5 MB, il valore della proprietà sarà "10,5 MB". Se il volume non dispone di una quota predefinita, la proprietà viene impostata su "nessun limite" o sull'equivalente localizzato.

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

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




