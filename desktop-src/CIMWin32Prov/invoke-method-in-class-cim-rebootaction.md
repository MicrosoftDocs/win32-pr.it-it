---
description: Il metodo Invoke della classe CIM \_ rebootaction esegue una determinata azione. I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione. Questo metodo viene ereditato dall' \_ azione CIM.
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
ms.openlocfilehash: e68849a486cc6a5b61dc55cf86e259e2f58435e8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304671"
---
# <a name="invoke-method-of-the-cim_rebootaction-class"></a>Metodo Invoke della classe CIM \_ rebootaction

Il metodo **Invoke** della classe [**CIM \_ rebootaction**](cim-rebootaction.md) esegue una determinata azione. I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione. Questo metodo viene ereditato dall' [**\_ azione CIM**](cim-action.md).

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

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

[\_REBOOTACTION CIM](invoke-method-in-class-cim-rebootaction.md)
</dt> <dt>

[**\_REBOOTACTION CIM**](cim-rebootaction.md)
</dt> </dl>

 

