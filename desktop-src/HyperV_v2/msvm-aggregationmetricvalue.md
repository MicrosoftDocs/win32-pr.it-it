---
description: Rappresenta il valore dell'istanza di una metrica definita da un'istanza della classe Msvm \_ AggregationMetricDefinition.
ms.assetid: 6dfcb711-6137-492a-aff4-82facbd11949
title: Msvm_AggregationMetricValue classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricValue
- Msvm_AggregationMetricValue.InstanceID
- Msvm_AggregationMetricValue.Caption
- Msvm_AggregationMetricValue.Description
- Msvm_AggregationMetricValue.ElementName
- Msvm_AggregationMetricValue.MetricDefinitionId
- Msvm_AggregationMetricValue.MeasuredElementName
- Msvm_AggregationMetricValue.TimeStamp
- Msvm_AggregationMetricValue.Duration
- Msvm_AggregationMetricValue.MetricValue
- Msvm_AggregationMetricValue.BreakdownDimension
- Msvm_AggregationMetricValue.BreakdownValue
- Msvm_AggregationMetricValue.Volatile
- Msvm_AggregationMetricValue.AggregationTimeStamp
- Msvm_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 512ed39ea86bad6c1cb89bdf6ace7d528a6605b378a8c026b889be655f5c0a70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149311"
---
# <a name="msvm_aggregationmetricvalue-class"></a>Classe Msvm \_ AggregationMetricValue

Rappresenta il valore dell'istanza di una metrica definita da un'istanza della [**classe Msvm \_ AggregationMetricDefinition.**](msvm-aggregationmetricdefinition.md) Le proprietà ereditate da [**Msvm \_ BaseMetricValue forniscono**](msvm-basemetricvalue.md) il valore effettivo della metrica. Le proprietà definite da questa classe forniscono informazioni sull'intervallo in cui è stata applicata la funzione di aggregazione.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricValue : CIM_AggregationMetricValue
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
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ AggregationMetricValue** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ AggregationMetricValue** ha queste proprietà.

<dl> <dt>

**AggregationDuration**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Rappresenta la durata del calcolo dell'aggregazione. L'inizio di un intervallo di monitoraggio in cui viene applicata la funzione di aggregazione viene determinato sottraendo **AggregationDuration** da **AggregationTimeStamp.** Questa proprietà viene ereditata da **CIM \_ AggregationMetricValue**.

</dd> <dt>

**AggregationTimeStamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica l'ora in cui è stata applicata la funzione di aggregazione per determinare il valore dell'istanza della metrica. Non corrisponde all'ora di creazione dell'istanza. Per una determinata **istanza di \_ CIM AggregationMetricValue,** **AggregationTimeStamp** cambia ogni volta che viene applicata la funzione di aggregazione per calcolare il valore. Questa proprietà viene ereditata da **CIM \_ AggregationMetricValue**.

</dd> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica una dimensione scomposizione dalla **matrice BreakdownDimensions** definita nell'oggetto [**\_ BaseMetricDefinition msvm associato.**](msvm-basemetricdefinition.md) Si tratta della dimensione lungo la quale viene suddiviso questo set di valori delle metriche. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**BreakdownValue**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Definisce un valore della proprietà **BreakdownDimension** definito per questa istanza del valore della metrica. Ad esempio, se **BreakdownDimension** è "TransactionName", questa proprietà potrebbe assegnare un nome alla transazione effettiva a cui si applica questo particolare valore della metrica. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
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

Specifica la durata di validità del valore della metrica. Questa proprietà non deve esistere per i timestamp che si applicano solo a un punto nel tempo, ma deve essere specificata per i valori considerati validi per un determinato periodo di tempo (ad esempio, il campionamento). Se la **proprietà Duration** esiste e non è **Null,** la **proprietà TimeStamp** specifica la fine dell'intervallo. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Stringa che identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**MeasuredElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome descrittivo per l'elemento a cui appartiene il valore della metrica (l'elemento misurato). Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Chiave [**dell'istanza \_ BaseMetricDefinition msvm**](msvm-basemetricdefinition.md) per questo valore. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**MetricValue**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
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

**True** se il valore per il momento successivo userà la stessa istanza della classe e modificherà semplicemente i valori delle proprietà, ad esempio **Value** o **TimeStamp.** Se **True**, l'istanza viene riutilizzata. Se **False,** le istanze esistenti rimangono invariate e viene creata una nuova istanza per il nuovo punto nel tempo. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

