---
description: Associazione tra un punto di accesso al servizio (SAP) e la relativa modalità di implementazione.
ms.assetid: d1d99299-f2d9-4025-a48d-cf8180f2f7af
title: Classe Msvm_WiFiDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiDeviceSAPImplementation
- Msvm_WiFiDeviceSAPImplementation.Antecedent
- Msvm_WiFiDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8debec96efb93e60ec18d75b62ffa0d13b0e0a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879106"
---
# <a name="msvm_wifidevicesapimplementation-class"></a>\_Classe MSVM WiFiDeviceSAPImplementation

Associazione tra un punto di accesso al servizio (SAP) e la relativa modalità di implementazione. La cardinalità di questa associazione è molti-a-molti. Un SAP può essere fornito da più di un dispositivo logico, operando insieme. Qualsiasi dispositivo può fornire più di un SAP. Quando molti dispositivi logici sono associati a un singolo SAP, si presuppone che questi elementi funzionino insieme per fornire il punto di accesso. Se sono presenti implementazioni diverse di un SAP, ognuna di queste implementazioni genererà le singole creazioni di istanze dell'oggetto SAP. Queste singole creazioni di istanze avrebbero quindi le associazioni alle implementazioni univoche.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  Msvm_WiFiPort     REF Antecedent;
  Msvm_WiFiEndpoint REF Dependent;
};
```

## <a name="members"></a>Members

La **classe \_ WiFiDeviceSAPImplementation di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ WiFiDeviceSAPImplementation di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ WiFiPort**](msvm-wifiport.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Istanza della classe [**MSVM \_ WiFiPort**](msvm-wifiport.md) che rappresenta il dispositivo logico.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ WiFiEndpoint**](msvm-wifiendpoint.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Istanza della classe [**MSVM \_ WiFiEndpoint**](msvm-wifiendpoint.md) che rappresenta il punto di accesso al servizio implementato utilizzando il dispositivo logico.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

