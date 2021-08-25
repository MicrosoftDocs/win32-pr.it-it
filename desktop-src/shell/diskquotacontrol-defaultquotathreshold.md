---
description: Imposta o ottiene la soglia di quota predefinita.
ms.assetid: d3f23e52-586f-4cb8-b91c-44a71f8f94b2
title: DiskQuotaControl.DefaultQuotaThreshold - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 46d44f2e2df24c5ee1cbf646643810e09d007eb15ba6c9a352eb492dfb104752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943111"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a>DiskQuotaControl.DefaultQuotaThreshold - proprietà

Imposta o ottiene la soglia di quota predefinita.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a>Valore proprietà

Valore **intero** impostato sulla soglia di avviso predefinita per i nuovi utenti, in byte.

## <a name="remarks"></a>Commenti

La soglia di quota predefinita viene applicata automaticamente ai nuovi utenti del volume. Se l'utilizzo del disco di un utente supera questo valore e la proprietà [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) è impostata su **TRUE,** il sistema genera una voce del registro eventi. Ad esempio, se la soglia predefinita è 10,0 MB, il valore della proprietà è "10,0 MB". Se il volume non ha una soglia predefinita, la proprietà viene impostata su "Nessun limite" o sull'equivalente localizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




