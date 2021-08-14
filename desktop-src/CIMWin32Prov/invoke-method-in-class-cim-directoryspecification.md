---
description: Il metodo Invoke della classe CIM \_ DirectorySpecification valuta un controllo specifico.
ms.assetid: 63289f94-f134-4159-898c-404cdd8f2a5c
ms.tgt_platform: multiple
title: Richiamare il metodo della CIM_DirectorySpecification classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecification.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8dd080d2bf28bbddf047b4712d5e5688f16be460749df4f5fc28f023697dbf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118419305"
---
# <a name="invoke-method-of-the-cim_directoryspecification-class"></a>Metodo Invoke della classe \_ CiM DirectorySpecification

Il **metodo Invoke** della classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) valuta un controllo specifico. Informazioni dettagliate sul modo in cui il metodo valuta un particolare controllo in un contesto CIM sono descritte dalle sottoclassi [**CIM \_ Check**](cim-check.md) non astratte. Questo metodo viene ereditato da **CIM \_ Check**.

> [!IMPORTANT]
> Le classi CIM DMTF (Distributed Management Task Force) (Common Information Model) sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Invoke();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, 1 se il metodo non è supportato e qualsiasi altro valore indica un errore.

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

[Directory \_ CIMSpecification](invoke-method-in-class-cim-directoryspecification.md)
</dt> <dt>

[**Directory \_ CIMSpecification**](cim-directoryspecification.md)
</dt> </dl>

 

