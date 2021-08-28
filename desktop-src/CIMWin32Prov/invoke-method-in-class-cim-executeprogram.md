---
description: Il metodo Invoke della classe CIM \_ ExecuteProgram esegue un'azione specifica. I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione. Questo metodo viene ereditato dall'azione \_ CIM.
ms.assetid: 14a12fae-14a6-412a-a778-8dd34a5843d1
ms.tgt_platform: multiple
title: Metodo Invoke della classe CIM_ExecuteProgram
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ExecuteProgram.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e2945b3083060dfb4a3211771d53b770d3c4f574a0465003cf83a174a9d5c0f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065101"
---
# <a name="invoke-method-of-the-cim_executeprogram-class"></a>Metodo Invoke della classe \_ CIM ExecuteProgram

Il **metodo Invoke** della classe [**CIM \_ ExecuteProgram**](cim-executeprogram.md) esegue un'azione specifica. I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione. Questo metodo viene ereditato [**dall'azione CIM \_**](cim-action.md).

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene Managed Object Format sintassi MOF (Managed Object Format). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Invoke();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.

## <a name="remarks"></a>Commenti

WMI non implementa questa classe.

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

[CIM \_ ExecuteProgram](invoke-method-in-class-cim-executeprogram.md)
</dt> <dt>

[**CIM \_ ExecuteProgram**](cim-executeprogram.md)
</dt> </dl>

 

