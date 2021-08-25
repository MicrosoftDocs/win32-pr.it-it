---
description: Rappresenta una definizione di metrica che contiene i metadati per un oggetto CIM \_ MetricInstance.
ms.assetid: 6abfb0dc-e80b-4ca6-89d9-2e43283d0abe
title: CIM_BaseMetricDefinition classe
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
ms.openlocfilehash: 0614b14f3033da5cf97dfb293f0e9cc130025dbb534331f8ec3386513d8796c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829721"
---
# <a name="cim_basemetricdefinition-class"></a>Classe CIM \_ BaseMetricDefinition

Rappresenta una definizione di metrica che contiene i metadati per un **oggetto CIM \_ MetricInstance.**

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

La **classe CIM \_ BaseMetricDefinition** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ BaseMetricDefinition** ha queste proprietà.

<dl> <dt>

**BreakdownDimensions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che contiene stringhe in formato libero che possono essere usate per suddividere le query [**di oggetti CIM \_ BaseMetricValue**](cim-basemetricvalue.md) lungo una determinata dimensione. Le stringhe devono essere significative per gli utenti finali dei dati delle metriche. Inoltre, le stringhe devono indicare le dimensioni di scomposimento supportate per la definizione della metrica, dalla strumentazione sottostante.

Un esempio è un nome di transazione che consente di suddividere il valore totale per tutte le transazioni in un set di valori, uno per ogni nome di transazione. Altri esempi sono un sistema di applicazioni o un nome di gruppo di utenti.

</dd> <dt>

**Calcolabile**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Caratteristiche della metrica usata per eseguire i calcoli.

<dt>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Non calcolo** (1)


</dt> <dd>

Stringa. L'aritmetica non ha senso.

</dd> <dt>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Sommabile** (2)


</dt> <dd>

È ragionevole sommare questo valore su molte istanze di , ad esempio UnitOfWork, ad esempio il numero di file elaborati in un processo di backup. Ad esempio, se ogni processo di backup è unitofwork e ogni processo esegue in media il backup di 27.000 file, è opportuno dire che 100 processi di backup hanno elaborato 2.700.000 file.

</dd> <dt>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Non sommabile** (3)


</dt> <dd>

Non ha senso sommare questo valore su molte istanze di UnitOfWork. Un esempio è una metrica che misura la lunghezza della coda quando un processo arriva a un server. Se ogni processo è unitOfWork e la lunghezza media della coda all'arrivo di ogni processo è 33, non ha senso dire che la lunghezza della coda per 100 processi è 3300. È opportuno dire che la media è 33.

</dd> </dl>

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BaseMetricDefinition**.**IsContinuous**")
</dt> </dl>

Indica il modo in cui il valore della metrica cambia usando attributi comuni, ad esempio la modifica della direzione, i valori minimo e massimo e la semantica di wrapping.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd>

La finestra di progettazione delle metriche non ha qualificato ChangeType.

</dd> <dt>

<span id="N_A"></span><span id="n_a"></span>

<span id="N_A"></span><span id="n_a"></span>**N/D** (2)


</dt> <dd>

Se la proprietà "IsContinuous" è "false", ChangeType non ha senso e MUST è impostato su "N/D".

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Contatore** (3)


</dt> <dd>

La metrica è una metrica contatore. Hanno valori interi non negativi che aumentano in modo monotono fino a raggiungere il numero massimo rappresentabile e quindi vengono incapsulati e iniziano ad aumentare da 0. Questi contatori, noti anche come contatori di rollover, possono essere usati ad esempio per contare il numero di errori di rete o il numero di transazioni elaborate. L'unico modo per un'applicazione client per tenere traccia del wrapping è recuperare il valore del contatore in intervalli opportunamente brevi.

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Misuratore** (4)


</dt> <dd>

La metrica è una metrica del misuratore. Hanno valori interi o float che possono aumentare e diminuire in modo arbitrario. Un misuratore NON DEVE eseguire il wrapping quando raggiunge il numero minimo o massimo rappresentabile, ma il valore "resta" in corrispondenza di tale numero. I valori minimi o massimi all'interno dell'intervallo di valori rappresentabili in corrispondenza del quale il valore della metrica "resta", possono o meno essere definiti.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF riservato** (5..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di dati della metrica.

<dt>

<span id="boolean"></span><span id="BOOLEAN"></span>

**booleano** (1)


</dt> <dd></dd> <dt>

<span id="char16"></span><span id="CHAR16"></span>

**char16** (2)


</dt> <dd></dd> <dt>

<span id="datetime"></span><span id="DATETIME"></span>

**datetime** (3)


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

**string** (10)


</dt> <dd></dd> <dt>

<span id="uint16"></span><span id="UINT16"></span>

**uint16** (11)


</dt> <dd></dd> <dt>

<span id="uint32"></span><span id="UINT32"></span>

**uint32** (12)


</dt> <dd></dd> <dt>

<span id="uint64"></span><span id="UINT64"></span>

**uint64** (13)


</dt> <dd></dd> <dt>

<span id="uint8"></span><span id="UINT8"></span>

**uint8** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**GatheringType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica come i valori delle metriche vengono raccolti dalla strumentazione sottostante.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd>

Indica che GatheringType non è noto.

</dd> <dt>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)


</dt> <dd>

Indica che i valori delle metriche CIM vengono aggiornati immediatamente quando i valori all'interno della risorsa misurata cambiano. I valori delle metriche OnChange riflettono effettivamente la situazione corrente all'interno della risorsa in qualsiasi momento. Un esempio è il numero di utenti connessi che vengono aggiornati immediatamente all'accesso e alla disconnessione degli utenti.

</dd> <dt>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periodico** (3)


</dt> <dd>

": indica che i valori delle metriche CIM vengono aggiornati periodicamente. Ad esempio, per un'applicazione client, un valore di metrica applicato all'ora corrente verrà visualizzato costante durante ogni intervallo di raccolta e quindi passa al nuovo valore alla fine di ogni intervallo di raccolta.

</dd> <dt>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)


</dt> <dd>

Indica che il valore della metrica CIM viene determinato ogni volta che viene letto da un'applicazione client. I valori delle metriche OnRequest restituiscono effettivamente la situazione corrente all'interno della risorsa se qualcuno la richiede. Tuttavia, non cambiano "non conservati" e pertanto la sottoscrizione per le modifiche di valore delle metriche OnRequest non è CONSIGLIATA.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF riservato** (5..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

ID univoco della definizione della metrica. Sono consigliati UUID/GUID di Open Software Foundation (OSF).

</dd> <dt>

**IsContinuous**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

True se il valore della metrica è continuo. in caso contrario, false.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della metrica. Questo nome non deve essere univoco, ma deve essere descrittivo e può contenere spazi vuoti.

</dd> <dt>

**ProgrammaticUnits**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Unità specifiche di un valore. Il valore di questa proprietà deve essere un valore valido del qualificatore Unità programmatiche come definito nell'appendice C.1 di DSP0004 V2.4 o versione successiva.

</dd> <dt>

**TimeScope**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**", "**CIM \_ BaseMetricValue**.**Duration**")
</dt> </dl>

Ambito temporale che si applica alla finestra di progettazione delle metriche.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd>

Indica che l'ambito temporale non è stato qualificato dalla finestra di progettazione delle metriche o è sconosciuto al provider.

</dd> <dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>**Punto** (2)


</dt> <dd>

Indica che la metrica si applica a un punto nel tempo. Nelle istanze BaseMetricValue corrispondenti TimeStamp specifica il punto nel tempo e Duration è sempre 0.

</dd> <dt>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Intervallo** (3)


</dt> <dd>

Indica che la metrica si applica a un intervallo di tempo. Nelle istanze BaseMetricValue corrispondenti TimeStamp specifica la fine dell'intervallo di tempo e Duration ne specifica la durata

</dd> <dt>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)


</dt> <dd>

Indica che la metrica si applica a un intervallo di tempo iniziato all'avvio della risorsa misurata,ad esempio l'elemento ManagedElement associato da MetricDefForMe. Nelle istanze BaseMetricValue corrispondenti TimeStamp specifica la fine dell'intervallo di tempo. Se Duration è 0, significa che il tempo di avvio della risorsa misurata è sconosciuto. In caso contrario, Duration specifica la durata tra l'avvio della risorsa e TimeStamp.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF riservato** (5..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Unità**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Unità della metrica. Ad esempio byte, pacchetti, processi, file, millisecondi e amp.

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

[**CIM \_ ManagedElement**](cim-managedelement.md)
</dt> </dl>

 

