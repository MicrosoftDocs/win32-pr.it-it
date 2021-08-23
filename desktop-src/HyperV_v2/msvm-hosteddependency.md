---
description: Associa un'istanza di macchina virtuale all'oggetto di sistema del computer che rappresenta il sistema fisico di hosting.
ms.assetid: 755624D7-04D0-47EA-8623-DEDE6B1D5CBC
title: Msvm_HostedDependency classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedDependency
- Msvm_HostedDependency.Antecedent
- Msvm_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b0c67df565be0085d4579bf82b2a2d2e542f856e93321240821bc512be692c6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014519"
---
# <a name="msvm_hosteddependency-class"></a>Classe Msvm \_ HostedDependency

Associa un'istanza di macchina virtuale all'oggetto di sistema del computer che rappresenta il sistema fisico di hosting.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedDependency : CIM_HostedDependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ HostedDependency** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ HostedDependency** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al computer host. Questa proprietà viene ereditata da [**CIM \_ HostedDependency.**](/previous-versions//cc136861(v=vs.85))

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento alla macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ HostedDependency.**](/previous-versions//cc136861(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ HostedDependency** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ HostedDependency**](cim-hosteddependency.md)
</dt> <dt>

[**CIM \_ HostedDependency**](/previous-versions//cc136861(v=vs.85))
</dt> <dt>

[Classi di gestione del sistema virtuale](virtual-system-management-classes.md)
</dt> </dl>

 

