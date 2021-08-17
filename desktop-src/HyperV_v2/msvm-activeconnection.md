---
description: Connette una porta commutatore all'endpoint LAN a cui è connessa la porta.
ms.assetid: 963EC004-6A67-4F75-BD93-1BCD17F32490
title: Msvm_ActiveConnection classe
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
ms.openlocfilehash: 2f8326fe50d3fef4e7776fa865afdd730416cb38fccd6347b4b27f0079966501
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693611"
---
# <a name="msvm_activeconnection-class"></a>Classe Msvm \_ ActiveConnection

Connette una porta commutatore all'endpoint LAN a cui è connessa la porta. L'esistenza di questo oggetto significa che la porta del commutatore e l'endpoint LAN sono attivamente connesse e che la porta Ethernet associata all'endpoint LAN può comunicare con la rete tramite la porta del commutatore.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

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

La **classe Msvm \_ ActiveConnection** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ ActiveConnection** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ LANEndpoint**](msvm-lanendpoint.md) che rappresenta il punto di accesso del servizio (SAP) configurato per comunicare o che comunica attivamente con sap dipendente. In una connessione unidirezionale, questo SAP è quello che trasmette.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ LANEndpoint**](cim-lanendpoint.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Riferimento a un'istanza della [**classe Msvm \_ LANEndpoint**](cim-lanendpoint.md) che rappresenta il sap configurato per comunicare o sta comunicando attivamente con sap precedente. In una connessione unidirezionale, questo SAP è quello che riceve.

</dd> <dt>

**IsUnidirectional**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se questa proprietà è **True,** la connessione è unidirezionale. In caso contrario, questa connessione è bidirezionale. Quando una connessione è unidirezionale, il "parlante" deve essere definito come riferimento **antecedente.** In una connessione bidirezionale, non è importante se il punto di accesso selezionato è **antecedente** o **dipendente.** Questa proprietà viene ereditata da [**CIM \_ ActiveConnection.**](/previous-versions//cc136779(v=vs.85))

</dd> <dt>

**OtherTrafficDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ActiveConnection,**](/previous-versions//cc136779(v=vs.85))ma non viene usata.

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Questa proprietà viene ereditata da [**CIM \_ ActiveConnection,**](/previous-versions//cc136779(v=vs.85))ma non viene usata.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ ActiveConnection** potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ ActiveConnection**](cim-activeconnection.md)
</dt> <dt>

[**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))
</dt> </dl>

 

