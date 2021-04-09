---
description: Il metodo Invoke della classe CIM \_ SettingCheck valuta un particolare controllo. I dettagli relativi al modo in cui il metodo valuta un particolare controllo in un contesto CIM sono descritti dalle sottoclassi di controllo CIM non astratte \_ . Questo metodo viene ereditato dal \_ controllo CIM.
ms.assetid: b2a9baea-cc5c-43d9-a93c-e3a77823d705
ms.tgt_platform: multiple
title: Metodo Invoke della classe CIM_SettingCheck
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a8c10246e841182aff1b49742694eeb3871d7862
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966056"
---
# <a name="invoke-method-of-the-cim_settingcheck-class"></a>Metodo Invoke della classe CIM \_ SettingCheck

Il metodo **Invoke** della classe [**CIM \_ SettingCheck**](cim-settingcheck.md) valuta un particolare controllo. I dettagli relativi al modo in cui il metodo valuta un particolare controllo in un contesto CIM sono descritti dalle sottoclassi [**di \_ controllo CIM**](cim-check.md) non astratte. Questo metodo viene ereditato dal **\_ controllo CIM**.

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

Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.

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

[\_SETTINGCHECK CIM](invoke-method-in-class-cim-settingcheck.md)
</dt> <dt>

[**\_SETTINGCHECK CIM**](cim-settingcheck.md)
</dt> </dl>

 

