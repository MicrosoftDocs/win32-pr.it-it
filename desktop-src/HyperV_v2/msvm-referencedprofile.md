---
description: Descrive un profilo a cui fa riferimento un altro profilo registrato.
ms.assetid: 36FC0161-C57F-488A-9B4A-C86C6EB481D7
title: Classe Msvm_ReferencedProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencedProfile
- Msvm_ReferencedProfile.Antecedent
- Msvm_ReferencedProfile.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbe95658556be8a15bed0e7e5b5b32dda23ff21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312900"
---
# <a name="msvm_referencedprofile-class"></a>\_Classe MSVM ReferencedProfile

Descrive un profilo a cui fa riferimento un altro profilo registrato.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class Msvm_ReferencedProfile : CIM_ReferencedProfile
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a>Members

La **classe \_ ReferencedProfile di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ReferencedProfile di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Profilo registrato a cui fa riferimento il profilo **dipendente** .

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Profilo registrato che fa riferimento ad altri profili.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                                                 |
| Spazio dei nomi<br/>                | \\Interoperabilità radice<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

