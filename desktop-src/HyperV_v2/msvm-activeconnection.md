---
description: Connette una porta di commutazione all'endpoint LAN a cui è connessa la porta.
ms.assetid: 963EC004-6A67-4F75-BD93-1BCD17F32490
title: Classe Msvm_ActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ActiveConnection
- Msvm_ActiveConnection.Antecedent
- Msvm_ActiveConnection.Dependent
- Msvm_ActiveConnection.TrafficType
- Msvm_ActiveConnection.OtherTrafficDescription
- Msvm_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf682fac419658785cfe7594aa6fc17e4b2dd28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883950"
---
# <a name="msvm_activeconnection-class"></a>\_Classe MSVM ActiveConnection

Connette una porta di commutazione all'endpoint LAN a cui è connessa la porta. L'esistenza di questo oggetto significa che la porta di commutazione e l'endpoint LAN sono connessi attivamente e che la porta Ethernet associata all'endpoint LAN può comunicare con la rete tramite la porta di commutazione.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ActiveConnection : CIM_ActiveConnection
{
  Msvm_LANEndpoint REF Antecedent;
  CIM_LANEndpoint  REF Dependent;
  uint16               TrafficType;
  string               OtherTrafficDescription;
  boolean              IsUnidirectional;
};
```

## <a name="members"></a>Members

La **classe \_ ActiveConnection di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ActiveConnection di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Un riferimento a un'istanza della classe [**MSVM \_ LANEndpoint**](msvm-lanendpoint.md) che rappresenta il punto di accesso al servizio (SAP) configurato per comunicare o sta comunicando attivamente con SAP dipendente. In una connessione unidirezionale, questo SAP è quello che trasmette.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ LANEndpoint**](cim-lanendpoint.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Riferimento a un'istanza della classe [**MSVM \_ LANEndpoint**](cim-lanendpoint.md) che rappresenta il SAP configurato per comunicare o sta comunicando attivamente con l'attività SAP precedente. In una connessione unidirezionale, questo SAP è quello che riceve.

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

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ ActiveConnection di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_ACTIVECONNECTION CIM**](cim-activeconnection.md)
</dt> <dt>

[**\_ACTIVECONNECTION CIM**](/previous-versions//cc136779(v=vs.85))
</dt> </dl>

 

