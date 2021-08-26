---
description: Il metodo Invoke della classe CIM \_ OSVersionCheck valuta un controllo specifico. I dettagli del modo in cui il metodo valuta un particolare controllo in un contesto CIM sono descritti dalle sottoclassi CIM Check non \_ astratte. Questo metodo viene ereditato da CIM \_ Check.
ms.assetid: ff06772c-e40c-49c8-b334-5ee480926245
ms.tgt_platform: multiple
title: Richiamare il metodo della CIM_OSVersionCheck classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSVersionCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0fe5001de0f397be94e61ffa4118db0e9b6c76debedf84cc1f93cbfe468abc82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064881"
---
# <a name="invoke-method-of-the-cim_osversioncheck-class"></a>Richiamare il metodo della classe \_ CIM OSVersionCheck

Il **metodo Invoke** della classe [**CIM \_ OSVersionCheck**](cim-osversioncheck.md) valuta un controllo specifico. I dettagli del modo in cui il metodo valuta un particolare controllo in un contesto CIM sono descritti dalle sottoclassi [**CIM \_ Check**](cim-check.md) non astratte. Questo metodo viene ereditato da **CIM \_ Check**.

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

[CIM \_ OSVersionCheck](invoke-method-in-class-cim-osversioncheck.md)
</dt> <dt>

[**CIM \_ OSVersionCheck**](cim-osversioncheck.md)
</dt> </dl>

 

