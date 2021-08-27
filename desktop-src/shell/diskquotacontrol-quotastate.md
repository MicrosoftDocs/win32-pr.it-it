---
description: Imposta o ottiene lo stato delle quote disco del volume.
title: DiskQuotaControl.QuotaState - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaState
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b0766ecf-6e22-4481-a6a7-df873a277bc2
ms.openlocfilehash: cb2117237cd3072163447ee80895cbbb8bb854d7ad4424da83854b28ffa96196
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090631"
---
# <a name="diskquotacontrolquotastate-property"></a>DiskQuotaControl.QuotaState - proprietà

Imposta o ottiene lo stato delle quote disco del volume.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a>Valore proprietà

Questa proprietà può essere impostata su uno dei valori seguenti.



| State          | Valore | Descrizione               |
|----------------|-------|---------------------------|
| dqStateDisable | 0     | Le quote disco sono disabilitate. |
| dqStateTrack   | 1     | Le quote disco sono disabilitate. |
| dqStateEnforce | 2     | Applicare il limite di quota.      |



 

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

 

 




