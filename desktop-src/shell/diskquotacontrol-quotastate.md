---
description: Imposta o ottiene lo stato delle quote disco del volume.
title: Proprietà DiskQuotaControl. QuotaState
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
ms.openlocfilehash: 460decc1068642ae797723b31f7350082f591d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485524"
---
# <a name="diskquotacontrolquotastate-property"></a>Proprietà DiskQuotaControl. QuotaState

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
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




