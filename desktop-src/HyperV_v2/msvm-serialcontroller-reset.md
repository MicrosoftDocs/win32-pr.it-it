---
description: Reimposta il dispositivo.
ms.assetid: 4ac8ee27-0629-45aa-80ee-f308c044d7fc
title: Reimposta il metodo della classe Msvm_SerialController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialController.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bf5fd2ff0218a4a4f39e64921e41fd497753d04e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312883"
---
# <a name="reset-method-of-the-msvm_serialcontroller-class"></a>Metodo Reset della \_ classe controller seriale di MSVM

Reimposta il dispositivo.

## <a name="syntax"></a>Sintassi


```mof
uint32 Reset();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1, versione 1703<br/>                                                                    |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Controller seriale MSVM**](msvm-serialcontroller.md)
</dt> </dl>

 

 




