---
description: Definisce una connessione attualmente attivata e configurata per fornire la comunicazione tra due \_ oggetti CIM ServiceAccessPoint.
ms.assetid: 03f8e43f-a77b-46e2-bb7d-c29758c65aee
title: Classe CIM_ActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActiveConnection
- CIM_ActiveConnection.Antecedent
- CIM_ActiveConnection.Dependent
- CIM_ActiveConnection.TrafficType
- CIM_ActiveConnection.OtherTrafficDescription
- CIM_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 644e8aaae1368e4164ceca7f7db29e343116c93c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308912"
---
# <a name="cim_activeconnection-class"></a>CIM \_ ActiveConnection (classe)

Definisce una connessione attualmente attivata e configurata per fornire la comunicazione tra due oggetti **CIM \_ serviceAccessPoint** . **CIM \_ ActiveConnection** viene usato quando la connessione non viene trattata come un oggetto **CIM \_ managementelement** . I punti di accesso al servizio connessi tramite una connessione attiva si trovano in genere nello stesso livello di rete o di applicazione.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ActiveConnection : CIM_SAPSAPDependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     TrafficType;
  string                     OtherTrafficDescription;
  boolean                    IsUnidirectional;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ActiveConnection** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ActiveConnection** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ serviceAccessPoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Il punto di accesso al servizio connesso all'altro punto di accesso al servizio tramite la connessione attiva. **CIM \_ Oggetto ServiceAccessPoint** . In una connessione unidirezionale, questo punto di accesso è quello che trasmette i dati.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ serviceAccessPoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Il punto di accesso al servizio configurato per comunicare o sta comunicando attivamente con il punto di accesso al servizio specificato nella proprietà **precedente** . In una connessione unidirezionale, questo punto di accesso è quello che riceve i dati.

</dd> <dt>

**IsUnidirectional**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

True se la connessione è unidirezionale. false se la connessione è bidirezionale. Quando la connessione è unidirezionale, la proprietà **antecedente** specifica il punto di accesso che trasmette i dati. In una connessione bidirezionale, l'attività **precedente** può specificare uno dei punti di accesso assegnati alla connessione.

</dd> <dt>

**OtherTrafficDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("nessun valore"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**TrafficType**")
</dt> </dl>

> [!Note]  
> Questa proprietà è deprecata. È invece consigliabile specificare queste informazioni nell'indirizzamento, nel protocollo e nella funzionalità di base degli endpoint.

 

Descrizione del tipo di traffico specificato quando la proprietà **TrafficType** è impostata su "1" (other).

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("nessun valore"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**OtherTrafficDescription**")
</dt> </dl>

> [!Note]  
> Questa proprietà è deprecata. È invece consigliabile specificare queste informazioni nell'indirizzamento, nel protocollo e nella funzionalità di base degli endpoint.

 

Tipo di traffico trasmesso sulla connessione.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Unicast"></span><span id="unicast"></span><span id="UNICAST"></span>

**Unicast** (2)


</dt> <dd></dd> <dt>

<span id="Broadcast"></span><span id="broadcast"></span><span id="BROADCAST"></span>

**Broadcast** (3)


</dt> <dd></dd> <dt>

<span id="Multicast"></span><span id="multicast"></span><span id="MULTICAST"></span>

**Multicast** (4)


</dt> <dd></dd> <dt>

<span id="Anycast"></span><span id="anycast"></span><span id="ANYCAST"></span>

**Anycast** (5)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SAPSAPDEPENDENCY CIM**](cim-sapsapdependency.md)
</dt> </dl>

 

