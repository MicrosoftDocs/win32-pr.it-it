---
description: Il metodo Reset della classe CIM \_ ParallelController richiede una reimpostazione del dispositivo logico.
ms.assetid: 7cdd46b5-b054-4322-bb05-dd9fd6d54f13
ms.tgt_platform: multiple
title: Metodo Reset della classe CIM_ParallelController
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
ms.openlocfilehash: 512164337a6cdeb68dc1370c1f7c7540ffe6eb8242c75c4904d90c41cd267e55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118418572"
---
# <a name="reset-method-of-the-cim_parallelcontroller-class"></a>Metodo Reset della classe CIM \_ ParallelController

Il **metodo Reset** della classe CIM \_ ParallelController richiede una reimpostazione del dispositivo logico. Questo metodo viene ereditato da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

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

[CIM \_ ParallelController](reset-method-in-class-cim-parallelcontroller.md)
</dt> <dt>

[**CIM \_ ParallelController**](cim-parallelcontroller.md)
</dt> </dl>

 

 




