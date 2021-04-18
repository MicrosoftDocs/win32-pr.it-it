---
description: Associazione tra un punto di accesso al servizio (SAP) e la relativa modalità di implementazione.
ms.assetid: 36108521-A699-4498-A962-DC0801D9EE81
title: Classe Msvm_DeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DeviceSAPImplementation
- Msvm_DeviceSAPImplementation.Antecedent
- Msvm_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9551d4409edfdfca18b66e3a3b86d6adcb28b19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314332"
---
# <a name="msvm_devicesapimplementation-class"></a>\_Classe MSVM DeviceSAPImplementation

Associazione tra un punto di accesso al servizio (SAP) e la relativa modalità di implementazione. La cardinalità di questa associazione è molti-a-molti. Un SAP può essere fornito da più di un dispositivo logico, operando insieme. Qualsiasi dispositivo può fornire più di un SAP. Quando molti dispositivi logici sono associati a un singolo SAP, si presuppone che questi elementi funzionino insieme per fornire il punto di accesso. Se sono presenti implementazioni diverse di un SAP, ognuna di queste implementazioni genererà le singole creazioni di istanze dell'oggetto SAP. Queste singole creazioni di istanze avrebbero quindi le associazioni alle implementazioni univoche.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Members

La **classe \_ DeviceSAPImplementation di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ DeviceSAPImplementation di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ serviceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il punto di accesso al servizio implementato usando il dispositivo logico. Questa proprietà viene ereditata da [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ DeviceSAPImplementation di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_DEVICESAPIMPLEMENTATION CIM**](cim-devicesapimplementation.md)
</dt> <dt>

[**\_DEVICESAPIMPLEMENTATION CIM**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 

