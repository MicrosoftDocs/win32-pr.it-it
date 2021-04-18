---
description: Rappresenta un'associazione tra un punto di accesso al servizio e il dispositivo logico che lo implementa.
ms.assetid: 5510c179-09e6-4762-b9b3-68ed49eafd66
title: Classe Msvm_FcDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcDeviceSAPImplementation
- Msvm_FcDeviceSAPImplementation.Antecedent
- Msvm_FcDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bc40f25e3b288155e713415aa512d629b538d1cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307920"
---
# <a name="msvm_fcdevicesapimplementation-class"></a>\_Classe MSVM FcDeviceSAPImplementation

Rappresenta un'associazione tra un punto di accesso al servizio e il dispositivo logico che lo implementa. La cardinalità di questa associazione è molti-a-molti. Un punto di accesso al servizio (SAP) può essere fornito da più di un dispositivo logico, operando insieme. Qualsiasi dispositivo può fornire più di un SAP. Quando molti dispositivi logici sono associati a un singolo SAP, si presuppone che questi elementi funzionino insieme per fornire il punto di accesso. Se sono presenti implementazioni diverse di un SAP, ognuna di queste implementazioni genererà le singole creazioni di istanze dell'oggetto SAP. Queste singole creazioni di istanze avrebbero quindi le associazioni alle implementazioni univoche.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_FCPort      REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
};
```

## <a name="members"></a>Members

La **classe \_ FcDeviceSAPImplementation di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ FcDeviceSAPImplementation di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ FCPort**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Riferimento a una classe derivata da **CIM \_ FCPort** che rappresenta il dispositivo logico.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **MSVM \_ FcEndpoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Riferimento a un'istanza della classe [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) che rappresenta il SAP che sta utilizzando l'attività **precedente**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

