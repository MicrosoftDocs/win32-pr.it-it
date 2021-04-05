---
description: Rappresenta il valore dell'istanza di una metrica definita da un'istanza della \_ classe MSVM AggregationMetricDefinition.
ms.assetid: 6dfcb711-6137-492a-aff4-82facbd11949
title: Classe Msvm_AggregationMetricValue
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
ms.openlocfilehash: f6842e5a23fbbf7cf1d639862cf5b9737bc1ff96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057981"
---
# <a name="msvm_aggregationmetricvalue-class"></a>\_Classe MSVM AggregationMetricValue

Rappresenta il valore dell'istanza di una metrica definita da un'istanza della classe [**MSVM \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) . Le proprietà ereditate da [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) forniscono il valore della metrica effettivo. Le proprietà definite da questa classe forniscono informazioni sull'intervallo in base al quale è stata applicata la funzione di aggregazione.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

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

La **classe \_ AggregationMetricValue di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ AggregationMetricValue di MSVM** dispone di queste proprietà.

<dl> <dt>

**AggregationDuration**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Rappresenta la durata dell'intervallo di tempo in cui è stata calcolata l'aggregazione. L'inizio di un intervallo di monitoraggio sul quale viene applicata la funzione di aggregazione viene determinato sottraendo **AggregationDuration** da **AggregationTimeStamp**. Questa proprietà viene ereditata da **CIM \_ AggregationMetricValue**.

</dd> <dt>

**AggregationTimeStamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica l'ora in cui è stata applicata la funzione di aggregazione per determinare il valore dell'istanza della metrica. Non corrisponde all'ora di creazione dell'istanza. Per un'istanza **di \_ AggregationMetricValue CIM** specificata, **AggregationTimeStamp** cambia ogni volta che viene applicata la funzione di aggregazione per calcolare il valore. Questa proprietà viene ereditata da **CIM \_ AggregationMetricValue**.

</dd> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica una dimensione di suddivisione dalla matrice **BreakdownDimensions** definita nel [**\_ BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md)associato. Si tratta della dimensione in base alla quale questo set di valori di metrica viene suddiviso. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**BreakdownValue**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Definisce un valore della proprietà **BreakdownDimension** definita per questa istanza del valore della metrica. Ad esempio, se **BreakdownDimension** è "transactionName", questa proprietà può assegnare un nome alla transazione effettiva a cui si applica questo particolare valore della metrica. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Duration**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica la durata del periodo di validità del valore della metrica. Questa proprietà non deve esistere per gli indicatori di tempo che si applicano solo a un punto nel tempo, ma deve essere specificata per i valori considerati validi per un determinato periodo di tempo, ad esempio il campionamento. Se la proprietà **Duration** esiste e non è **null**, la proprietà **timestamp** specifica la fine dell'intervallo. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Stringa che identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**MeasuredElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome descrittivo per l'elemento a cui appartiene il valore della metrica, ovvero l'elemento misurato. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Chiave dell'istanza di [**\_ BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md) per questo valore. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**MetricValue**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore della metrica rappresentata come stringa. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**TimeStamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'ora in cui il valore della metrica è stato acquisito o calcolato. Tenere presente che si tratta di una differenza rispetto all'ora di creazione dell'istanza. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Volatile**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**True** se il valore per il momento successivo utilizzerà la stessa istanza della classe e modificherà solo i valori delle proprietà, ad esempio il **valore** o il **timestamp**. Se **true**, l'istanza viene riutilizzata. Se **false**, le istanze esistenti rimangono invariate e viene creata una nuova istanza per il nuovo punto nel tempo. Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

