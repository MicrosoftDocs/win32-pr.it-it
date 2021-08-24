---
description: Il metodo Reset della classe CIM \_ SerialController richiede una reimpostazione del dispositivo logico.
ms.assetid: b4d99f49-52ac-4f62-9573-c712d0cafdd0
ms.tgt_platform: multiple
title: Metodo Reset della classe CIM_SerialController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4fca63cfc772b4b91e77d126f0ff769a89417a11ed393d2c8e6d8cad17d10938
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701061"
---
# <a name="reset-method-of-the-cim_serialcontroller-class"></a>Metodo Reset della classe CIM \_ SerialController

Il **metodo Reset** della classe CIM \_ SerialController richiede una reimpostazione del dispositivo logico. Questo metodo viene ereditato da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

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

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

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

[CIM \_ SerialController](reset-method-in-class-cim-serialcontroller.md)
</dt> <dt>

[**CIM \_ SerialController**](cim-serialcontroller.md)
</dt> </dl>

 

 




