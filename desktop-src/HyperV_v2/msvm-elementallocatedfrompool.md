---
description: Associa un'istanza di una risorsa allocata al pool di risorse da cui è stata allocata.
ms.assetid: BA3168C7-E4F1-414B-827B-1A811069F223
title: Msvm_ElementAllocatedFromPool classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromPool
- Msvm_ElementAllocatedFromPool.Antecedent
- Msvm_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a68731bec7ae7ab8126fa6b76305257d4333f06012e619cd7a3c9a90bcc69283
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148533"
---
# <a name="msvm_elementallocatedfrompool-class"></a>Classe Msvm \_ ElementAllocatedFromPool

Associa un'istanza di una risorsa allocata al pool di risorse da cui è stata allocata.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromPool : CIM_ElementAllocatedFromPool
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ ElementAllocatedFromPool** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ ElementAllocatedFromPool** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CiM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Override**, **Max** (1)
</dt> </dl>

Pool di risorse. Questa proprietà viene ereditata da [**CIM \_ ElementAllocatedFromPool.**](/previous-versions//cc150668(v=vs.85))

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Risorsa allocata. Questa proprietà viene ereditata da [**CIM \_ ElementAllocatedFromPool.**](/previous-versions//cc150668(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ ElementAllocatedFromPool** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ ElementAllocatedFromPool**](cim-elementallocatedfrompool.md)
</dt> <dt>

[**CIM \_ ElementAllocatedFromPool**](/previous-versions//cc150668(v=vs.85))
</dt> <dt>

[**Msvm \_ ElementAllocatedFromPool (V1)**](/previous-versions/windows/desktop/virtual/msvm-elementallocatedfrompool)
</dt> <dt>

[Classi di gestione delle risorse](resource-management-classes.md)
</dt> </dl>

 

