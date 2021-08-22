---
description: Associa due elementi gestiti che rappresentano aspetti diversi della stessa entità sottostante.
ms.assetid: 107A2B15-09F2-490A-8AB2-F9FE5F6FEE60
title: Msvm_LogicalIdentity classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalIdentity
- Msvm_LogicalIdentity.SameElement
- Msvm_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 12ee48b85ae11b10a24bab35001baa45c8382105158050d110eb7448a8e883e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148364"
---
# <a name="msvm_logicalidentity-class"></a>Classe \_ Msvm LogicalIdentity

Associa due elementi gestiti che rappresentano aspetti diversi della stessa entità sottostante. Questa classe deriva da [**CIM \_ LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalIdentity : CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ LogicalIdentity** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ LogicalIdentity** ha queste proprietà.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un aspetto alternativo dell'entità di sistema.

</dd> <dt>

**SystemElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un aspetto dell'elemento logico.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo app desktop R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ LogicalIdentity**](cim-logicalidentity.md)
</dt> <dt>

[**CIM \_ LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity)
</dt> </dl>

 

