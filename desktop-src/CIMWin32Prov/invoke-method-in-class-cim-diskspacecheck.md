---
description: Il metodo Invoke della classe CIM \_ DiskSpaceCheck valuta un controllo specifico. I dettagli del modo in cui il metodo valuta un particolare controllo in un contesto CIM sono descritti dalla sottoclasse CIM Check non \_ astratta.
ms.assetid: 1f06b0c4-3f39-4a6f-9205-2aa309fb06bb
ms.tgt_platform: multiple
title: Richiamare il metodo della CIM_DiskSpaceCheck classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DiskSpaceCheck.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: dbf8e976861c079fc79e70b3b9009b8948624e57e02870ad50c2630cd42aca7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118009897"
---
# <a name="invoke-method-of-the-cim_diskspacecheck-class"></a>Richiamare il metodo della classe \_ CIM DiskSpaceCheck

Il **metodo Invoke** della classe [**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md) valuta un controllo specifico. I dettagli del modo in cui il metodo valuta un particolare controllo in un contesto CIM sono descritti dalla sottoclasse [**CIM \_ Check**](cim-check.md) non astratta.

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

[CIM \_ DiskSpaceCheck](invoke-method-in-class-cim-diskspacecheck.md)
</dt> <dt>

[**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md)
</dt> </dl>

 

