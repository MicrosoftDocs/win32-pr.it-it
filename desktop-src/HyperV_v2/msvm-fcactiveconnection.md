---
description: Connette una porta di commutazione all'endpoint Fibre Channel a cui è connessa la porta.
ms.assetid: e2762e0c-2f78-4159-a67c-31213e311072
title: Classe Msvm_FcActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcActiveConnection
- Msvm_FcActiveConnection.Antecedent
- Msvm_FcActiveConnection.Dependent
- Msvm_FcActiveConnection.TrafficType
- Msvm_FcActiveConnection.OtherTrafficDescription
- Msvm_FcActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e29330e073266f2f2a8749ec3c70d9e26b35ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307923"
---
# <a name="msvm_fcactiveconnection-class"></a>\_Classe MSVM FcActiveConnection

Connette una porta di commutazione all'endpoint Fibre Channel a cui è connessa la porta. L'esistenza di questo oggetto significa che la porta di commutazione e l'endpoint Fibre Channel sono connessi attivamente e la porta Fibre Channel associata all'endpoint Fibre Channel può comunicare con la rete tramite la porta di commutazione.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcActiveConnection : CIM_ActiveConnection
{
  Msvm_FcEndpoint REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
  uint16              TrafficType;
  string              OtherTrafficDescription;
  boolean             IsUnidirectional;
};
```

## <a name="members"></a>Members

La **classe \_ FcActiveConnection di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ FcActiveConnection di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **MSVM \_ FcEndpoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Un riferimento a un'istanza della classe [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) che rappresenta il punto di accesso al servizio (SAP) configurato per comunicare o sta comunicando attivamente con SAP dipendente. In una connessione unidirezionale, questo SAP è quello che trasmette.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **MSVM \_ FcEndpoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Riferimento a un'istanza della classe [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) che rappresenta il SAP configurato per comunicare o sta comunicando attivamente con l'attività SAP precedente. In una connessione unidirezionale, questo SAP è quello che riceve.

</dd> <dt>

**IsUnidirectional**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se questa proprietà è **true**, la connessione è unidirezionale; in caso contrario, la connessione è bidirezionale. Quando una connessione è unidirezionale, è necessario definire il "relatore" come riferimento **antecedente** . In una connessione bidirezionale non è rilevante se il punto di accesso selezionato è l'attività **precedente** o **dipendente**. Questa proprietà viene ereditata da [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)).

</dd> <dt>

**OtherTrafficDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), ma non viene utilizzata.

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), ma non viene utilizzata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

