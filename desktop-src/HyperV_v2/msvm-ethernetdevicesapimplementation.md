---
description: "Msvm_EthernetDeviceSAPImplementation classe : rappresenta un'associazione tra un punto di accesso del servizio e il dispositivo logico che lo implementa."
ms.assetid: C0DDB199-AD97-4DD7-8056-BD6BD0CECFA8
title: Msvm_EthernetDeviceSAPImplementation classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetDeviceSAPImplementation
- Msvm_EthernetDeviceSAPImplementation.Antecedent
- Msvm_EthernetDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0cabf80b7e55513fc5fc31b744db8cbc973ccd15bcda170804c754850d65dbfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524981"
---
# <a name="msvm_ethernetdevicesapimplementation-class"></a>Classe Msvm \_ EthernetDeviceSAPImplementation

Rappresenta un'associazione tra un punto di accesso del servizio e il dispositivo logico che lo implementa. La cardinalità di questa associazione è molti-a-molti. Un punto di accesso al servizio (SAP) può essere fornito da più di un dispositivo logico, operando in combinazione. Qualsiasi dispositivo può fornire più di un SAP. Quando molti dispositivi logici sono associati a un singolo SAP, si presuppone che questi elementi funzionino in combinazione per fornire il punto di accesso. Se esistono implementazioni diverse di sap, ognuna di queste implementazioni comporterebbe la creazione di singole istanze dell'oggetto SAP. Queste singole istanze hanno quindi associazioni alle implementazioni univoche.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_EthernetPort REF Antecedent;
  Msvm_LANEndpoint REF Dependent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ EthernetDeviceSAPImplementation** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ EthernetDeviceSAPImplementation** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Riferimento a una classe derivata da [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) che rappresenta il dispositivo logico.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Riferimento a un'istanza della [**classe MSvm \_ LANEndpoint**](msvm-lanendpoint.md) che rappresenta il sap che usa **l'attività precedente.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

