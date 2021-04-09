---
description: Arresta il servizio Guest.
ms.assetid: 67FFA46C-0B61-4845-A617-BA10F4D42CBC
title: 'Metodo Msvm_GuestService:: StopService'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6c396078e2bd623a768f391a645091679694f453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879006"
---
# <a name="msvm_guestservicestopservice-method"></a>\_Metodo MSVM GuestService:: StopService

Arresta il servizio Guest.

## <a name="syntax"></a>Sintassi


```C++
uint32 StopService();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.



| Codice/valore restituito                                                                                                                                             | Descrizione         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**Completato senza errori**</dt> <dt>0</dt> </dl> | Esito positivo.<br/> |
| <dl> <dt>**Non supportato**</dt> <dt>1</dt> </dl>           |                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\\\\\Virtualizzazione radice \\ v2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_GuestService MSVM**](msvm-guestservice.md)
</dt> </dl>

 

 




