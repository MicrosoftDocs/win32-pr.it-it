---
description: Definisce una connessione attualmente attivata e configurata per fornire la comunicazione tra due oggetti \_ ServiceAccessPoint CIM.
ms.assetid: 03f8e43f-a77b-46e2-bb7d-c29758c65aee
title: CIM_ActiveConnection classe
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
ms.openlocfilehash: a2961779744e90d0e4281e53c3d78c92081993027deb6c435846abbffb41b110
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041761"
---
# <a name="cim_activeconnection-class"></a>Classe \_ CIM ActiveConnection

Definisce una connessione attualmente attivata e configurata per fornire la comunicazione tra due **oggetti \_ ServiceAccessPoint CIM.** **CIM \_ ActiveConnection** viene usato quando la connessione non viene considerata come **un oggetto CIM \_ ManagedElement.** I punti di accesso del servizio connessi da una connessione attiva si trovano in genere allo stesso livello di rete o applicazione.

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

La **classe \_ CIM ActiveConnection** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CIM ActiveConnection** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Punto di accesso del servizio connesso all'altro punto di accesso del servizio tramite la connessione attiva. **CIM \_ Oggetto ServiceAccessPoint.** In una connessione unidirezionale, questo punto di accesso è quello che trasmette i dati.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dipendente")
</dt> </dl>

Punto di accesso al servizio configurato per comunicare o che comunica attivamente con il punto di accesso del servizio specificato nella **proprietà Antecedent.** In una connessione unidirezionale, questo punto di accesso è quello che riceve i dati.

</dd> <dt>

**IsUnidirectional**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

True se la connessione è unidirezionale. false se la connessione è bidirezionale. Quando la connessione è unidirezionale, la **proprietà Antecedent** specifica il punto di accesso che trasmette i dati. In una connessione bidirezionale, **Antecedent** può specificare uno dei due punti di accesso assegnati alla connessione.

</dd> <dt>

**OtherTrafficDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Nessun valore"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**TrafficType**")
</dt> </dl>

> [!Note]  
> Questa proprietà è deprecata. È invece consigliabile specificare queste informazioni nell'indirizzamento, nel protocollo e nella funzionalità di base degli endpoint.

 

Descrizione del tipo di traffico specificato quando la **proprietà TrafficType** è impostata su "1" (Altro).

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Nessun valore"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**OtherTrafficDescription**")
</dt> </dl>

> [!Note]  
> Questa proprietà è deprecata. È invece consigliabile specificare queste informazioni nell'indirizzamento, nel protocollo e nella funzionalità di base degli endpoint.

 

Tipo di traffico trasmesso tramite questa connessione.

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

**Trasmissione** (3)


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
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ SAPSAPDependency**](cim-sapsapdependency.md)
</dt> </dl>

 

