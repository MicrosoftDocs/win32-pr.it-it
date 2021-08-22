---
description: Contiene un riepilogo delle informazioni sul sistema di computer virtuale specificato.
ms.assetid: ab31d5db-a8d3-47bc-a024-0f4c4b93a34b
title: Msvm_ComputerSystemSummaryInformation classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystemSummaryInformation
- Msvm_ComputerSystemSummaryInformation.Antecedent
- Msvm_ComputerSystemSummaryInformation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 78ac2b89336a415bedd23e0ca4ecd6589abdefbf75a54900d716c78152d34d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531761"
---
# <a name="msvm_computersystemsummaryinformation-class"></a>Classe Msvm \_ ComputerSystemSummaryInformation

Contiene un riepilogo delle informazioni sul sistema di computer virtuale specificato.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Association, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ComputerSystemSummaryInformation : CIM_ElementView
{
  CIM_ComputerSystem          REF Antecedent;
  Msvm_SummaryInformationBase REF Dependent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ ComputerSystemSummaryInformation** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ ComputerSystemSummaryInformation** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Chiave**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Oggetto [**CiM \_ ComputerSystem**](cim-computersystem.md) che è un'istanza nella rappresentazione normalizzata della risorsa gestita.

> [!Note]
>
> Tipo di dati aggiornato da [**Msvm \_ ComputerSystem**](msvm-computersystem.md) in Windows 10 versione 1703.

 

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Msvm \_ SummaryInformationBase**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Istanza di [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) che rappresenta una visualizzazione de-normalizzata o aggregata della risorsa gestita rappresentata da [**Msvm \_ ComputerSystem**](msvm-computersystem.md) a cui fa riferimento la proprietà Antecedent.

> [!Note]
>
> Tipo di dati aggiornato [**da Msvm \_ SummaryInformation**](msvm-summaryinformation.md) in Windows 10 versione 1703.

 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ ElementView**](cim-elementview.md)
</dt> </dl>

 

