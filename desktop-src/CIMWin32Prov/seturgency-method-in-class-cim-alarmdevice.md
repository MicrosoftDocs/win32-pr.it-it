---
description: Il metodo seurge imposta il livello di urgenza desiderato per un allarme.
ms.assetid: ac2e7fda-1317-440a-adbd-1ef0844d124c
ms.tgt_platform: multiple
title: Metodo seurgement della classe CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.SetUrgency
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35918677e210ac2fe7ac4798a04db9dc628f5fa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966136"
---
# <a name="seturgency-method-of-the-cim_alarmdevice-class"></a>Metodo seurgement della \_ classe CIM AlarmDevice

Il metodo **seurge** imposta il livello di urgenza desiderato per un allarme.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetUrgency(
  [in] uint16 RequestedUrgency
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RequestedUrgency* \[ in\]
</dt> <dd>

Frequenza relativa con cui l'allarme lampeggia, vibra o emette toni acustici. I valori seguenti sono dalla proprietà **urgenza** in [**CIM \_ AlarmDevice**](cim-alarmdevice.md).

<dt>

0
</dt> <dd>

Sconosciuto.

</dd> <dt>

1
</dt> <dd>

Altro.

</dd> <dt>

2
</dt> <dd>

Non supportata.

</dd> <dt>

3
</dt> <dd>

Si tratta di un messaggio informativo.

</dd> <dt>

4
</dt> <dd>

Non critico.

</dd> <dt>

5
</dt> <dd>

Critica.

</dd> <dt>

6
</dt> <dd>

Irreversibile.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) in caso di esito positivo, 1 (uno) se il livello di urgenza richiesto non è supportato e qualsiasi altro numero per indicare un errore.

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

[\_ALARMDEVICE CIM](seturgency-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[**\_ALARMDEVICE CIM**](cim-alarmdevice.md)
</dt> </dl>

 

