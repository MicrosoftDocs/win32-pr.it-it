---
description: Connette un servizio di bridging trasparente a una voce di inoltro dinamico (indirizzo MAC appreso).
ms.assetid: CA083F15-1E75-4EB9-BE56-95742181FDAC
title: Msvm_TransparentBridgingDynamicForwarding classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingDynamicForwarding
- Msvm_TransparentBridgingDynamicForwarding.Antecedent
- Msvm_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dd768b458ffed82f82b682b6f121baf67c6a909e142a9e9efdf7f63e29573671
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811761"
---
# <a name="msvm_transparentbridgingdynamicforwarding-class"></a>Classe Msvm \_ TransparentBridgingDynamicForwarding

Connette un servizio di bridging trasparente a una voce di inoltro dinamico (indirizzo MAC appreso).

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingDynamicForwarding : CIM_TransparentBridgingDynamicForwarding
{
  Msvm_TransparentBridgingService REF Antecedent;
  Msvm_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ TransparentBridgingDynamicForwarding** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ TransparentBridgingDynamicForwarding** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ TransparentBridgingService**](msvm-transparentbridgingservice.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) che rappresenta il servizio di bridging trasparente.

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

L'accesso alla **classe Msvm \_ TransparentBridgingDynamicForwarding** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ TransparentBridgingDynamicForwarding**](cim-transparentbridgingdynamicforwarding.md)
</dt> <dt>

[**CIM \_ TransparentBridgingDynamicForwarding**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingdynamicforwarding)
</dt> </dl>

 

