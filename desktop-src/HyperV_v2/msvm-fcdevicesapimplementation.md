---
description: "Msvm_FcDeviceSAPImplementation classe : rappresenta un'associazione tra un punto di accesso del servizio e il dispositivo logico che lo implementa."
ms.assetid: 5510c179-09e6-4762-b9b3-68ed49eafd66
title: Msvm_FcDeviceSAPImplementation classe
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
ms.openlocfilehash: 9aafe3bd029960a0b371c3a3d5ab54b66ad4849210189ab2946df2854656c500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523461"
---
# <a name="msvm_fcdevicesapimplementation-class"></a>Classe Msvm \_ FcDeviceSAPImplementation

Rappresenta un'associazione tra un punto di accesso del servizio e il dispositivo logico che lo implementa. La cardinalità di questa associazione è molti-a-molti. Un punto di accesso al servizio (SAP) può essere fornito da più dispositivi logici, operando in combinazione. Qualsiasi dispositivo può fornire più di un SAP. Quando molti dispositivi logici sono associati a un singolo SAP, si presuppone che questi elementi funzionino insieme per fornire il punto di accesso. Se esistono implementazioni diverse di un sap, ognuna di queste implementazioni comporterebbe la creazione di singole istanze dell'oggetto SAP. Queste singole istanze avrebbero quindi associazioni alle implementazioni univoche.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

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

La **classe Msvm \_ FcDeviceSAPImplementation** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ FcDeviceSAPImplementation** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ FCPort**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Riferimento a una classe derivata da **CIM \_ FCPort** che rappresenta il dispositivo logico.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Msvm \_ FcEndpoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ FcEndpoint**](msvm-fcendpoint.md) che rappresenta il sap che usa **antecedente**.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

