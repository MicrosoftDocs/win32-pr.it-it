---
description: Il metodo Reset della classe CIM \_ AlarmDevice richiede una reimpostazione del dispositivo logico. Questo metodo viene ereditato da CIM \_ LogicalDevice.
ms.assetid: e70718c5-2c80-4084-b233-b3e4d083e7b4
ms.tgt_platform: multiple
title: Metodo Reset della classe CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ac0cd1ded976ed4ba28ca89715d9ba72ea6c324b6eaaadc71eff8a38ca8f827e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816681"
---
# <a name="reset-method-of-the-cim_alarmdevice-class"></a>Metodo Reset della classe CIM \_ AlarmDevice

Il **metodo Reset** della classe [**CIM \_ AlarmDevice**](cim-alarmdevice.md) richiede una reimpostazione del dispositivo logico. Questo metodo viene ereditato da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Sintassi


```mof
uint32 Reset();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce 0 (zero) se la richiesta è stata eseguita correttamente, 1 (uno) se la richiesta non è supportata e un altro valore se si è verificato un errore.

## <a name="remarks"></a>Commenti

Questo metodo non è attualmente implementato da WMI. Per usare questo metodo, è necessario implementarlo nel proprio provider.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[CIM \_ AlarmDevice](reset-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[**CIM \_ AlarmDevice**](cim-alarmdevice.md)
</dt> </dl>

 

 




