---
description: Il metodo Reset della classe CIM \_ ParallelController richiede la reimpostazione del dispositivo logico.
ms.assetid: 7cdd46b5-b054-4322-bb05-dd9fd6d54f13
ms.tgt_platform: multiple
title: Reimposta il metodo della classe CIM_ParallelController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParallelController.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83fed0b2df0c0470878ed560aedde6de74719184
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523698"
---
# <a name="reset-method-of-the-cim_parallelcontroller-class"></a>Metodo Reset della classe CIM \_ ParallelController

Il metodo **Reset** della classe CIM \_ ParallelController richiede la reimpostazione del dispositivo logico. Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_PARALLELCONTROLLER CIM](reset-method-in-class-cim-parallelcontroller.md)
</dt> <dt>

[**\_PARALLELCONTROLLER CIM**](cim-parallelcontroller.md)
</dt> </dl>

 

 




