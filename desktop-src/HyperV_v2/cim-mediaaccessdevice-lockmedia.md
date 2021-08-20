---
description: Blocca e sblocca i supporti in un dispositivo di accesso rimovibile.
ms.assetid: 357ee552-82d0-4201-bcc2-0acf208e16a0
title: Metodo LockMedia della classe CIM_MediaAccessDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0b5ad5319ef0b4a5dec3b910a8229ba5b9cae19b046c02195b8dcc22c6af9ce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995497"
---
# <a name="lockmedia-method-of-the-cim_mediaaccessdevice-class"></a>Metodo LockMedia della classe \_ MediaAccessDevice CIM

Blocca e sblocca i supporti in un dispositivo di accesso rimovibile.

## <a name="syntax"></a>Sintassi


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Blocco* \[ Pollici\]
</dt> <dd>

Se **TRUE,** blocca il supporto. Se **FALSE,** rilascia il supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 se l'operazione ha esito positivo. In caso contrario, restituisce un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)
</dt> </dl>

 

 




