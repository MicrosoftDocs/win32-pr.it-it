---
description: Rappresenta una definizione di metrica che contiene i metadati per un \_ oggetto METRICINSTANCE CIM.
ms.assetid: 6abfb0dc-e80b-4ca6-89d9-2e43283d0abe
title: Classe CIM_BaseMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricDefinition
- CIM_BaseMetricDefinition.Id
- CIM_BaseMetricDefinition.Name
- CIM_BaseMetricDefinition.DataType
- CIM_BaseMetricDefinition.Calculable
- CIM_BaseMetricDefinition.Units
- CIM_BaseMetricDefinition.BreakdownDimensions
- CIM_BaseMetricDefinition.IsContinuous
- CIM_BaseMetricDefinition.ChangeType
- CIM_BaseMetricDefinition.TimeScope
- CIM_BaseMetricDefinition.GatheringType
- CIM_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cac965ed1eae59f1c269d897a12e9aa116183eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319528"
---
# <a name="cim_basemetricdefinition-class"></a>CIM \_ BaseMetricDefinition (classe)

Rappresenta una definizione di metrica che contiene i metadati per un **oggetto \_ MetricInstance CIM** .

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricDefinition : CIM_ManagedElement
{
  string  Id;
  string  Name;
  uint16  DataType;
  uint16  Calculable;
  string  Units;
  string  BreakdownDimensions[];
  boolean IsContinuous;
  uint16  ChangeType;
  uint16  TimeScope;
  uint16  GatheringType;
  string  ProgrammaticUnits;
};
```

## <a name="members"></a>Members

La classe **CIM \_ BaseMetricDefinition** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ BaseMetricDefinition** dispone di queste proprietà.

<dl> <dt>

**BreakdownDimensions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che contiene le stringhe di formato gratuite che possono essere utilizzate per suddividere le query di oggetti [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md) lungo una determinata dimensione. Le stringhe devono essere significative per gli utenti finali dei dati della metrica. Inoltre, le stringhe devono indicare quali dimensioni di suddivisione sono supportate per la definizione della metrica, dalla strumentazione sottostante.

Un esempio è un nome di transazione che consente di suddividere il valore totale di tutte le transazioni in un set di valori, uno per ogni nome di transazione. Altri esempi sono un sistema applicativo o un nome di gruppo di utenti.

</dd> <dt>

**Calcolabile**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Caratteristiche della metrica utilizzata per eseguire i calcoli.

<dt>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Non calcolabile** (1)


</dt> <dd>

Stringa. L'aritmetica non è sensata.

</dd> <dt>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Sommabile** (2)


</dt> <dd>

È ragionevole sommare questo valore in molte istanze di, ad esempio, UnitOfWork, ad esempio il numero di file elaborati in un processo di backup. Se, ad esempio, ogni processo di backup è un UnitOfWork e ogni processo esegue il backup di 27.000 file in media, è opportuno indicare che i processi di backup 100 hanno elaborato 2,7 milioni file.

</dd> <dt>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Non-sommabile** (3)


</dt> <dd>

Non ha senso sommare questo valore in molte istanze di UnitOfWork. Un esempio è una metrica che misura la lunghezza della coda quando un processo arriva a un server. Se ogni processo è un UnitOfWork e la lunghezza media della coda quando ogni processo arriva è 33, non è sensato dire che la lunghezza della coda per i processi 100 è 3300. È sensato dire che la media è 33.

</dd> </dl>

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BaseMetricDefinition**.**Uncontinuous**")
</dt> </dl>

Indica il modo in cui il valore della metrica cambia usando gli attributi comuni, ad esempio la modifica della direzione, i valori minimo e massimo e la semantica di wrapping.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd>

La finestra di progettazione metrica non ha qualificato l'oggetto ChangeType.

</dd> <dt>

<span id="N_A"></span><span id="n_a"></span>

<span id="N_A"></span><span id="n_a"></span>**N/** d (2)


</dt> <dd>

Se la proprietà "sacontinuous" è "false", ChangeType non ha senso e deve essere impostato su "N/A".

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Contatore** (3)


</dt> <dd>

La metrica è una metrica del contatore. Hanno valori interi non negativi che aumentano in modo progressivo fino a raggiungere il numero massimo rappresentabile, quindi eseguire il wrapping e iniziare ad aumentare da 0. Tali contatori, noti anche come contatori di rollover, possono essere usati ad esempio per conteggiare il numero di errori di rete o il numero di transazioni elaborate. L'unico modo in cui un'applicazione client tiene traccia degli incapsulamenti consiste nel recuperare il valore del contatore in intervalli opportunamente brevi.

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Misuratore** (4)


</dt> <dd>

La metrica è una metrica del misuratore. Hanno valori integer o float che possono aumentare e diminuire in modo arbitrario. NON è necessario eseguire il wrapping di un misuratore quando si raggiunge il numero minimo o massimo rappresentabile, invece, il valore "bastoni" a tale numero. Valori minimi o massimi all'interno dell'intervallo di valori rappresentabili in corrispondenza del quale il valore della metrica "bastoni", può o non essere definito.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di dati della metrica.

<dt>

<span id="boolean"></span><span id="BOOLEAN"></span>

**valore booleano** (1)


</dt> <dd></dd> <dt>

<span id="char16"></span><span id="CHAR16"></span>

**Char16** (2)


</dt> <dd></dd> <dt>

<span id="datetime"></span><span id="DATETIME"></span>

**DateTime** (3)


</dt> <dd></dd> <dt>

<span id="real32"></span><span id="REAL32"></span>

**real32** (4)


</dt> <dd></dd> <dt>

<span id="real64"></span><span id="REAL64"></span>

**real64** (5)


</dt> <dd></dd> <dt>

<span id="sint16"></span><span id="SINT16"></span>

**sint16** (6)


</dt> <dd></dd> <dt>

<span id="sint32"></span><span id="SINT32"></span>

**sint32** (7)


</dt> <dd></dd> <dt>

<span id="sint64"></span><span id="SINT64"></span>

**sint64** (8)


</dt> <dd></dd> <dt>

<span id="sint8"></span><span id="SINT8"></span>

**sint8** (9)


</dt> <dd></dd> <dt>

<span id="string"></span><span id="STRING"></span>

**stringa** (10)


</dt> <dd></dd> <dt>

<span id="uint16"></span><span id="UINT16"></span>

**UInt16** (11)


</dt> <dd></dd> <dt>

<span id="uint32"></span><span id="UINT32"></span>

**UInt32** (12)


</dt> <dd></dd> <dt>

<span id="uint64"></span><span id="UINT64"></span>

**UInt64** (13)


</dt> <dd></dd> <dt>

<span id="uint8"></span><span id="UINT8"></span>

**Uint8** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**GatheringType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il modo in cui i valori delle metriche vengono raccolti dalla strumentazione sottostante.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd>

Indica che GatheringType non è noto.

</dd> <dt>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)


</dt> <dd>

Indica che i valori della metrica CIM vengono aggiornati immediatamente quando i valori all'interno della risorsa misurata cambiano. I valori delle metriche OnChange riflettono effettivamente la situazione corrente all'interno della risorsa in qualsiasi momento. Un esempio è il numero di utenti connessi che vengono aggiornati immediatamente quando gli utenti accedono e si disconnettono.

</dd> <dt>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periodica** (3)


</dt> <dd>

": Indica che i valori della metrica CIM vengono aggiornati periodicamente. Ad esempio, per un'applicazione client, un valore della metrica che si applica all'ora corrente apparirà costante durante ogni intervallo di raccolta, quindi passa al nuovo valore alla fine di ogni intervallo di raccolta.

</dd> <dt>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)


</dt> <dd>

Indica che il valore della metrica CIM viene determinato ogni volta che viene letto da un'applicazione client. I valori delle metriche OnRequest restituiscono effettivamente la situazione corrente all'interno della risorsa, se richiesto. Tuttavia, non modificano "unosservato" e pertanto la sottoscrizione delle modifiche dei valori delle metriche OnRequest non è CONSIGLIata.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

ID univoco della definizione della metrica. Sono consigliati gli UUID/GUID Open Software Foundation (OSF).

</dd> <dt>

**IsContinuous**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

True se il valore della metrica è continuo. in caso contrario, false.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della metrica. Non è necessario che questo nome sia univoco, ma deve essere descrittivo e può contenere spazi vuoti.

</dd> <dt>

**ProgrammaticUnits**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Unità specifiche di un valore. Il valore di questa proprietà deve essere un valore valido del qualificatore unità programmatiche come definito nell'Appendice C. 1 di DSP0004 V 2.4 o versione successiva.

</dd> <dt>

**TimeScope**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**","**CIM \_ BaseMetricValue**.**Durata**")
</dt> </dl>

Ambito temporale che si applica alla finestra di progettazione della metrica.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd>

Indica che l'ambito di tempo non è stato qualificato dalla finestra di progettazione della metrica o è sconosciuto al provider.

</dd> <dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>**Punto** (2)


</dt> <dd>

Indica che la metrica si applica a un punto nel tempo. Nelle istanze BaseMetricValue corrispondenti, TimeStamp specifica il punto nel tempo e la durata è sempre 0.

</dd> <dt>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Intervallo** (3)


</dt> <dd>

Indica che la metrica si applica a un intervallo di tempo. Nelle istanze BaseMetricValue corrispondenti, TimeStamp specifica la fine dell'intervallo di tempo e Duration ne specifica la durata

</dd> <dt>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)


</dt> <dd>

Indica che la metrica si applica a un intervallo di tempo che inizia all'avvio della risorsa misurata, ovvero l'oggetto gestito associato da MetricDefForMe. Nelle istanze BaseMetricValue corrispondenti, TimeStamp specifica la fine dell'intervallo di tempo. Se Duration è 0, indica che il tempo di avvio della risorsa misurata è sconosciuto. Else, Duration specifica la durata tra l'avvio della risorsa e il TimeStamp.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Unità**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Unità della metrica. Esempi sono i byte, i pacchetti, i processi, i file, i millisecondi e gli ampere.

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

[**\_ManagementName CIM**](cim-managedelement.md)
</dt> </dl>

 

