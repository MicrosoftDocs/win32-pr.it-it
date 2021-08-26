---
description: Il metodo Invoke della classe CIM \_ RebootAction esegue un'azione specifica. I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione. Questo metodo viene ereditato dall'azione \_ CIM.
ms.assetid: 27b6571e-94fe-423e-89ab-5ba2bc632882
ms.tgt_platform: multiple
title: Metodo Invoke della classe CIM_RebootAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RebootAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: eac69785beed5aa2b0865808bcca8bc5c3386506508acaebe177fc5008afaba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064851"
---
# <a name="invoke-method-of-the-cim_rebootaction-class"></a>Metodo Invoke della classe CIM \_ RebootAction

Il **metodo Invoke** della classe [**CIM \_ RebootAction**](cim-rebootaction.md) esegue un'azione specifica. I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione. Questo metodo viene ereditato [**dall'azione CIM \_**](cim-action.md).

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Invoke();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.

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

[CIM \_ RebootAction](invoke-method-in-class-cim-rebootaction.md)
</dt> <dt>

[**CIM \_ RebootAction**](cim-rebootaction.md)
</dt> </dl>

 

