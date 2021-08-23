---
description: Il metodo Invoke della classe CIM \_ Check valuta un controllo specifico.
ms.assetid: cf1adeb2-f8a2-4f84-978f-e801bce104ac
ms.tgt_platform: multiple
title: Richiamare il metodo della CIM_Check classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Check.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 68a6c03fbad6002d20f7ab84ac5aea3f7205183b613b66cd18d7cdf8b03678ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958970"
---
# <a name="invoke-method-of-the-cim_check-class"></a>Metodo Invoke della classe CIM \_ Check

Il **metodo Invoke** della classe [**CIM \_ Check**](cim-check.md) valuta un controllo specifico.

Per altre informazioni su come il metodo valuta un particolare controllo in un contesto CIM, vedere le sottoclassi [**CIM \_ Check**](cim-check.md) non astratte.

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

Restituisce il valore 0 (zero) in caso di esito positivo, 1 (uno) se il metodo non è supportato e qualsiasi altro numero per indicare un errore.

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

[**Controllo \_ CIM**](invoke-method-in-class-cim-check.md)
</dt> <dt>

[**Controllo \_ CIM**](cim-check.md)
</dt> </dl>

 

