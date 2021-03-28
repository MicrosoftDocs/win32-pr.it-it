---
description: Ottiene la soglia di quota predefinita come stringa di testo.
ms.assetid: 48b1cbd5-12dd-4c31-a14c-7904d29f6eb9
title: Proprietà DiskQuotaControl. DefaultQuotaThresholdText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b3b209c7c8e71b49fd3b9fce90b9ea30b584bd65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128439"
---
# <a name="diskquotacontroldefaultquotathresholdtext-property"></a>Proprietà DiskQuotaControl. DefaultQuotaThresholdText

Ottiene la soglia di quota predefinita come stringa di testo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
DefaultQuotaThresholdText = DiskQuotaControl.DefaultQuotaThresholdText
```



## <a name="property-value"></a>Valore proprietà

Valore stringa che contiene la soglia di quota predefinita per il volume.

## <a name="remarks"></a>Commenti

La soglia di quota predefinita viene applicata automaticamente ai nuovi utenti del volume. Se l'utilizzo del disco di un utente supera questo valore e la proprietà [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) è impostata su **true**, il sistema genera una voce del registro eventi. Se, ad esempio, la soglia predefinita è 10,0 MB, il valore della proprietà è "10,0 MB". Se il volume non dispone di una soglia predefinita, la proprietà viene impostata su "nessun limite" o sull'equivalente localizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




