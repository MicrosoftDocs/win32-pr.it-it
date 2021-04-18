---
description: "\\_L'indicazione CIM è la classe base astratta per tutte le notifiche relative alle modifiche apportate agli oggetti dello schema e ai dati degli oggetti dello schema, eventi rilevati dai provider e dalla strumentazione. Le sottoclassi dell' \\_ indicazione CIM rappresentano tipi specifici di notifiche."
ms.assetid: 85a70425-7b32-449c-9fc0-1cfbf34d9187
title: Classe CIM_Indication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Indication
- CIM_Indication.IndicationIdentifier
- CIM_Indication.CorrelatedIndications
- CIM_Indication.IndicationTime
- CIM_Indication.PerceivedSeverity
- CIM_Indication.OtherSeverity
- CIM_Indication.IndicationFilterName
- CIM_Indication.SequenceContext
- CIM_Indication.SequenceNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 46b8d50f2e90d9a51c8ffa0b93de9ac16c889340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311143"
---
# <a name="cim_indication-class"></a>\_Classe di indicazione CIM

**CIM \_ Indica** la classe di base astratta per tutte le notifiche relative alle modifiche apportate agli oggetti dello schema e ai dati degli oggetti dello schema, eventi rilevati dai provider e dalla strumentazione. Le sottoclassi dell' **\_ indicazione CIM** rappresentano tipi specifici di notifiche.

## <a name="syntax"></a>Sintassi

``` syntax
[Indication, Version("2.24.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_Indication : __ExtrinsicEvent
{
  string   IndicationIdentifier;
  string   CorrelatedIndications[];
  datetime IndicationTime;
  uint16   PerceivedSeverity;
  string   OtherSeverity;
  string   IndicationFilterName;
  string   SequenceContext;
  sint64   SequenceNumber;
};
```

## <a name="members"></a>Members

La classe di **\_ indicazione CIM** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe di **\_ indicazione CIM** presenta queste proprietà.

<dl> <dt>

**CorrelatedIndications**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Notifiche correlate "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicazione CIM**.**IndicationIdentifier**")
</dt> </dl>

Matrice che contiene i valori **IndicationIdentifier** delle notifiche correlate a questo.

</dd> <dt>

**IndicationFilterName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ IndicationFilter.Name")
</dt> </dl>

Identificatore del filtro di indicazione che elabora l'indicazione. Il servizio di invio imposta questa proprietà. Questa proprietà è correlata alla proprietà **Name** dell'oggetto **\_ IndicationFilter CIM** . Il valore di **IndicationFilterName** deve usare il formato seguente:

-   *<OrgID>*:*<LocalID>*
-   *<OrgID>* deve includere un nome con copyright, marchio o univoco di proprietà dell'entità di business a cui appartiene l'oggetto.
-   *<OrgID>* non devono contenere i due punti (:)
-   *<LocalID>* Identificatore univoco scelto dall'entità di business a cui appartiene l'oggetto.

</dd> <dt>

**IndicationIdentifier**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Identificatore notifica ")
</dt> </dl>

Identificatore dell'indicazione. Questa proprietà può essere usata come valore chiave nella matrice di proprietà **CorrelatedIndications** . Pertanto, **IndicationIdentifier** deve essere un valore univoco all'interno dello spazio dei nomi di questa istanza della classe.

Per assicurarsi che **IndicationIdentifier** sia univoco, deve usare il formato seguente:

-   *<OrgID>*:*<LocalID>*
-   *<OrgID>* deve includere un nome con copyright, marchio o univoco di proprietà dell'entità di business a cui appartiene l'oggetto.
-   *<OrgID>* non devono contenere i due punti (:)
-   *<LocalID>* Identificatore univoco scelto dall'entità di business a cui appartiene l'oggetto.
-   Per le istanze definite da DMTF, *<OrgID>* deve essere impostato su "CIM".

</dd> <dt>

**IndicationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data e ora di creazione dell'indicazione. La proprietà può essere impostata su **null** se l'entità che ha creato l'indicazione non è in grado di determinare tali informazioni.

> [!Note]  
> Il valore **IndicationTime** può essere lo stesso per le indicazioni generate in rapida successione.

 

</dd> <dt>

**OtherSeverity**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")
</dt> </dl>

Gravità dell'indicazione dal punto di vista del notificatore quando **PerceivedSeverity** è impostato su "1" (other).

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation. ITU \| X733. Gravità percepita ")
</dt> </dl>

Gravità dell'indicazione dal punto di vista del notificatore.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd>

la gravità percepita dell'indicazione è sconosciuta o indeterminata.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd>

Indica che il valore della gravità è reperibile nella proprietà **OtherSeverity** .

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informazioni** (2)


</dt> <dd>

Quando si fornisce una risposta informativa, è necessario utilizzare le informazioni.

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Danneggiato/avviso** (3)


</dt> <dd>

Deve essere usato quando è appropriato per consentire all'utente di decidere se è necessaria un'azione.

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Secondario** (4)


</dt> <dd>

L'azione è necessaria, ma in questo momento la situazione non è grave.

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principale** (5)


</dt> <dd>

L'azione è ora necessaria.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (6)


</dt> <dd>

L'azione è ora necessaria e l'ambito è ampio (probabilmente verrà generata un'interruzione imminente a una risorsa critica).

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Irreversibile/irreversibile** (7)


</dt> <dd>

si è verificato un errore, ma è troppo tardi per intraprendere un'azione correttiva.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**SequenceContext**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicazione CIM**.**SequenceNumber**")
</dt> </dl>

Contesto di sequenza dell'identificatore di sequenza per l'indicazione. Se un servizio non supporta gli identificatori di sequenza per le indicazioni, questa proprietà deve essere impostata su **null**. Se l'indicazione viene recapitata, questa proprietà rimane invariata.

> [!Note]  
> L'identificatore di sequenza per l'indicazione consente a un listener di identificare le indicazioni duplicate quando il servizio tenta di recapitare le indicazioni, riordinare le indicazioni che non arrivano in ordine e rilevare le indicazioni perse.

 

Per assicurarsi che **SequenceContext** sia univoco, deve usare il formato seguente:

-   nome-servizio *-indicazione* \# *CIM-Service-Start-ID* \# *listener-destinazione-fase di creazione*
-   *indication-Service-Name* è il valore della proprietà **Name** dell'istanza **CIM \_ IndicationService** che fornisce l'indicazione.
-   *CIM-Service-Start-ID* è un identificatore che identifica in modo univoco l'operazione di avvio di un servizio. Ad esempio, potrebbe trattarsi di un timestamp dell'ora di inizio o di un contatore che aumenta per ogni avvio o riavvio del servizio.
-   *listener-Destination-Creation-Time* è un timestamp dell'ora di creazione dell'istanza **CIM \_ ListenerDestination** che rappresenta la destinazione del listener. nSince questo formato è solo una raccomandazione, i client CIM devono trattare il valore come un identificatore opaco per il contesto della sequenza e non deve basarsi su questo formato.

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicazione CIM**.**SequenceContext**")
</dt> </dl>

Numero di sequenza dell'identificatore di sequenza per l'indicazione.

> [!Note]  
> L'identificatore di sequenza per l'indicazione consente a un listener di identificare le indicazioni duplicate quando il servizio tenta di recapitare le indicazioni, riordinare le indicazioni che non arrivano in ordine e rilevare le indicazioni perse.

 

Il numero di sequenza presenta le caratteristiche seguenti:

-   Il numero di sequenza viene reimpostato su "0" ogni volta che viene modificato il valore di **SequenceContext** .
-   Ogni volta che la destinazione del listener riceve una nuova indicazione, il numero di sequenza viene aumentato di "1".
-   Il numero di sequenza viene eseguito a capo a "0" quando viene superato l'intervallo di valori.
-   Se l'indicazione viene recapitata, il **SequenceNumber** rimane invariato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

