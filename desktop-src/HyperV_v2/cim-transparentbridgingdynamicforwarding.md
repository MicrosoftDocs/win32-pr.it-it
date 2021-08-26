---
description: Associa un servizio di bridging trasparente a una voce del relativo database di inoltro.
ms.assetid: 6db93e71-c9b7-4710-a9ee-99a1055cfd82
title: CIM_TransparentBridgingDynamicForwarding classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingDynamicForwarding
- CIM_TransparentBridgingDynamicForwarding.Antecedent
- CIM_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 931b556cad32a7e83f82798c277e65995aa4318156a3f423a9fe2d7e057c252f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980791"
---
# <a name="cim_transparentbridgingdynamicforwarding-class"></a>Classe CIM \_ TransparentBridgingDynamicForwarding

Associa un servizio di bridging trasparente a una voce del relativo database di inoltro.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingDynamicForwarding : CIM_Dependency
{
  CIM_TransparentBridgingService REF Antecedent;
  CIM_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a>Members

La **classe CIM \_ TransparentBridgingDynamicForwarding** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ TransparentBridgingDynamicForwarding** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ TransparentBridgingService**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Riferimento [**CIM \_ TransparentBridgingService**](cim-transparentbridgingservice.md) al servizio di bridging trasparente.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ DynamicForwardingEntry**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento [**CIM \_ DynamicForwardingEntry**](cim-dynamicforwardingentry.md) alla voce del database di inoltro.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Dipendenza \_ CIM**](cim-dependency.md)
</dt> </dl>

 

