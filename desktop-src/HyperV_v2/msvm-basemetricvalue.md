---
description: Rappresenta un valore di metrica definito da un'istanza della classe Msvm \_ BaseMetricDefinition.
ms.assetid: bd872f21-ab71-4ab7-88d3-b26dd2fbdbe5
title: Msvm_BaseMetricValue classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricValue
- Msvm_BaseMetricValue.InstanceID
- Msvm_BaseMetricValue.Caption
- Msvm_BaseMetricValue.Description
- Msvm_BaseMetricValue.ElementName
- Msvm_BaseMetricValue.MetricDefinitionId
- Msvm_BaseMetricValue.MeasuredElementName
- Msvm_BaseMetricValue.TimeStamp
- Msvm_BaseMetricValue.Duration
- Msvm_BaseMetricValue.MetricValue
- Msvm_BaseMetricValue.BreakdownDimension
- Msvm_BaseMetricValue.BreakdownValue
- Msvm_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24d61f6068cffc83f8556637bba30de57308b6a5bcefe5b015bc185ab7811108
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790221"
---
# <a name="msvm_basemetricvalue-class"></a>Classe Msvm \_ BaseMetricValue

Rappresenta un valore di metrica definito da un'istanza della [**classe Msvm \_ BaseMetricDefinition.**](msvm-basemetricdefinition.md)

La sintassi seguente è Managed Object Format codice MOF (Simplified Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricValue : CIM_BaseMetricValue
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ BaseMetricValue** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ BaseMetricValue** ha queste proprietà.

<dl> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica una dimensione di scomposizione dalla matrice **BreakdownDimensions** definita nell'oggetto [**Msvm \_ BaseMetricDefinition associato.**](msvm-basemetricdefinition.md) Si tratta della dimensione lungo la quale viene suddiviso questo set di valori di metrica. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**BreakdownValue**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Definisce un valore della proprietà **BreakdownDimension** definita per questa istanza del valore della metrica. Ad esempio, se **BreakdownDimension** è "TransactionName", questa proprietà potrebbe assegnare un nome alla transazione effettiva a cui si applica questo particolare valore della metrica. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Duration**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica la durata di validità del valore della metrica. Questa proprietà non deve esistere per i timestamp che si applicano solo a un punto nel tempo, ma deve essere specificata per i valori considerati validi per un determinato periodo di tempo ,ad esempio il campionamento. Se la **proprietà Duration** esiste e non è **Null,** la **proprietà TimeStamp** specifica la fine dell'intervallo. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Stringa che identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**MeasuredElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome descrittivo per l'elemento a cui appartiene il valore della metrica (elemento misurato). Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Chiave [**dell'istanza di Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) per questo valore. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**MetricValue**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore della metrica rappresentata come stringa. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'ora in cui il valore della metrica è stato acquisito o calcolato. Tenere presente che questo valore è diverso dal momento in cui è stata creata l'istanza. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Volatile**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**True** se il valore per il momento successivo userà la stessa istanza della classe e modificherà solo i valori delle proprietà , ad esempio **Value** o **TimeStamp**. Se **True,** l'istanza viene riutilizzata. Se **False**, le istanze esistenti rimangono invariate e viene creata una nuova istanza per il nuovo punto nel tempo. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

