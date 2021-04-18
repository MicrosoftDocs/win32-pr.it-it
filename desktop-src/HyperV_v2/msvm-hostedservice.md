---
description: Associa un servizio al relativo computer di hosting.
ms.assetid: 888ABA71-6D67-4933-89E6-40F731AA7153
title: Classe Msvm_HostedService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedService
- Msvm_HostedService.Antecedent
- Msvm_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 284254d32e788e374d56b3822f5c00868552e1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307902"
---
# <a name="msvm_hostedservice-class"></a>\_Classe MSVM servizio ospitato

Associa un servizio al relativo computer di hosting. Le istanze di [**MSVM \_ VirtualizationManagementService**](msvm-virtualsystemmanagementservice.md) possono essere individuate tramite la relativa associazione a un host.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedService : CIM_HostedService
{
  CIM_ManagedElement REF Antecedent;
  CIM_Service        REF Dependent;
};
```

## <a name="members"></a>Members

La **classe \_ servizio ospitato di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ servizio ospitato di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al sistema del computer host. Questa proprietà viene ereditata da [**CIM \_ servizio ospitato**](/windows/desktop/CIMWin32Prov/cim-hostedservice).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **\_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al servizio ospitato. Questa proprietà viene ereditata da [**CIM \_ servizio ospitato**](/windows/desktop/CIMWin32Prov/cim-hostedservice).

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ servizio ospitato di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Esempio

Vedere [esecuzione di query sugli oggetti di rete](querying-networking-objects.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Servizio ospitato CIM**](cim-hostedservice.md)
</dt> <dt>

[**\_Servizio ospitato CIM**](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> <dt>

[Classi di gestione del sistema virtuale](virtual-system-management-classes.md)
</dt> </dl>

 

