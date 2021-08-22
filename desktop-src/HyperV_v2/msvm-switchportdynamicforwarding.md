---
description: Connette una porta del commutatore a una voce di inoltro dinamico (indirizzo MAC appreso).
ms.assetid: 70687D56-1282-46C7-AB4E-60E32B9DBA14
title: Msvm_SwitchPortDynamicForwarding classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SwitchPortDynamicForwarding
- Msvm_SwitchPortDynamicForwarding.Antecedent
- Msvm_SwitchPortDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d5deb326877e7af639c7bc18a73a8c968e75c26b64d690d4a4582085833fa23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950070"
---
# <a name="msvm_switchportdynamicforwarding-class"></a>Classe Msvm \_ SwitchPortDynamicForwarding

Connette una porta del commutatore a una voce di inoltro dinamico (indirizzo MAC appreso). Ciò è utile per trovare tutti gli indirizzi MAC appresi per una porta specificata.

La sintassi seguente è Managed Object Format codice MOF (Simplified Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SwitchPortDynamicForwarding : CIM_SwitchPortDynamicForwarding
{
  Msvm_EthernetSwitchPort     REF Antecedent;
  Msvm_DynamicForwardingEntry REF Dependent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ SwitchPortDynamicForwarding** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ SwitchPortDynamicForwarding** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) che rappresenta la porta del commutatore.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) che rappresenta la voce di inoltro dinamico del database di inoltro.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ SwitchPortDynamicForwarding** potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Esempio

Vedere [Esecuzione di query sugli oggetti di rete](querying-networking-objects.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ SwitchPortDynamicForwarding**](cim-switchportdynamicforwarding.md)
</dt> <dt>

[**CIM \_ SwitchPortDynamicForwarding**](/previous-versions//cc136921(v=vs.85))
</dt> </dl>

 

