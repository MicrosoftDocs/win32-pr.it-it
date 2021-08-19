---
description: Imposta il servizio guest in uno stato avviato.
ms.assetid: 1DC6A5B3-0F91-4AC1-99D5-0E8CF5ED35A2
title: Msvm_GuestService::StartService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 52f3f05eef622940e0fb1a9645a66097a8930fac9a236f432d5471c4ee20c208
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050401"
---
# <a name="msvm_guestservicestartservice-method"></a>Metodo Msvm \_ GuestService::StartService

Imposta il servizio guest in uno stato avviato.

## <a name="syntax"></a>Sintassi


```C++
uint32 StartService();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.



| Codice/valore restituito                                                                                                                                             | Descrizione         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**Completata senza errori**</dt> <dt>0</dt> </dl> | Operazione completata.<br/> |
| <dl> <dt>**Non supportato**</dt> <dt>1</dt> </dl>           |                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\\\Root \\ Virtualization \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ GuestService**](msvm-guestservice.md)
</dt> </dl>

 

 




