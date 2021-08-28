---
description: L'indicazione CIM è la classe di base astratta per tutte le notifiche relative alle modifiche negli oggetti dello schema e ai dati degli oggetti dello schema, agli eventi rilevati \_ dai provider e dalla strumentazione. Le sottoclassi di CIM \_ Indication rappresentano tipi specifici di notifiche.
ms.assetid: 85a70425-7b32-449c-9fc0-1cfbf34d9187
title: CIM_Indication classe
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
ms.openlocfilehash: e859e7834a051bad0a5ea402e8bd6c3685b5ad54
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883525"
---
# <a name="cim_indication-class"></a>Classe di indicazione CIM \_

**CIM \_ L'indicazione** è la classe di base astratta per tutte le notifiche relative alle modifiche negli oggetti dello schema e ai dati degli oggetti dello schema, agli eventi rilevati dai provider e dalla strumentazione. Le sottoclassi di **CIM \_ Indication** rappresentano tipi specifici di notifiche.

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

La **classe CIM \_ Indication** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ Indication** ha queste proprietà.

<dl> <dt>

**CorrelatedIndications**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Notifiche correlate"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**INDICAZIONE CIM \_**.**IndicationIdentifier**")
</dt> </dl>

Matrice che contiene i **valori di IndicationIdentifier** delle notifiche correlate a questa.

</dd> <dt>

**IndicationFilterName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ IndicationFilter.Name")
</dt> </dl>

Identificatore del filtro di indicazione che elabora l'indicazione. Il servizio mittente imposta questa proprietà. Questa proprietà è correlata alla **proprietà Name** dell'oggetto **CIM \_ IndicationFilter.** Il valore di **IndicationFilterName** deve usare il formato seguente:

-   *&lt; OrgID: &gt;**&lt; LocalID &gt;*
-   *&lt; OrgID &gt;* deve includere un nome protetto da copyright, con marchio o univoco di proprietà dell'entità aziendale proprietaria dell'oggetto.
-   *&lt; OrgID &gt; non* deve contenere i due punti (:)
-   *&lt; LocalID &gt;* un identificatore univoco scelto dall'entità aziendale proprietaria dell'oggetto.

</dd> <dt>

**IndicationIdentifier**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Identificatore di notifica")
</dt> </dl>

Identificatore dell'indicazione. Questa proprietà può essere usata come valore chiave nella matrice di proprietà **CorrelatedIndications.** Pertanto, **IndicationIdentifier** deve essere un valore univoco all'interno dello spazio dei nomi di questa istanza della classe.

Per assicurarsi che **IndicationIdentifier** sia univoco, deve usare il formato seguente:

-   *&lt; OrgID: &gt;**&lt; LocalID &gt;*
-   *&lt; OrgID &gt;* deve includere un nome protetto da copyright, con marchio o univoco di proprietà dell'entità aziendale proprietaria dell'oggetto.
-   *&lt; OrgID &gt; non* deve contenere i due punti (:)
-   *&lt; LocalID &gt;* un identificatore univoco scelto dall'entità aziendale proprietaria dell'oggetto.
-   Per le istanze definite da DMTF, *&lt; OrgID &gt;* deve essere impostato su "CIM".

</dd> <dt>

**IndicationTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora e data di creazione dell'indicazione. La proprietà può essere impostata su **NULL** se l'entità che ha creato l'indicazione non è in grado di determinare queste informazioni.

> [!Note]  
> Il **valore IndicationTime** può essere lo stesso per le indicazioni generate in rapida successione.

 

</dd> <dt>

**OtherSeverity**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")
</dt> </dl>

Gravità dell'indicazione dal punto di vista del notificatore quando **PerceivedSeverity** è impostato su "1" (Altro).

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Gravità percepita")
</dt> </dl>

Gravità dell'indicazione dal punto di vista del notificatore.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)


</dt> <dd>

La gravità percepita dell'indicazione è sconosciuta o indeterminata.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)


</dt> <dd>

Indica che il valore della gravità è disponibile nella **proprietà OtherSeverity.**

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informazioni** (2)


</dt> <dd>

Le informazioni devono essere usate quando si fornisce una risposta informativa.

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Danneggiato/Avviso** (3)


</dt> <dd>

Deve essere usato quando appropriato per consentire all'utente di decidere se è necessaria un'azione.

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Secondario** (4)


</dt> <dd>

È necessaria un'azione, ma la situazione non è grave in questo momento.

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principale** (5)


</dt> <dd>

L'azione è necessaria ORA.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critico** (6)


</dt> <dd>

L'azione è necessaria ORA e l'ambito è ampio (potrebbe verificarsi un'imminente interruzione di una risorsa critica).

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Irreversibile/Non irreversibile** (7)


</dt> <dd>

si è verificato un errore, ma è troppo tardi per eseguire un'azione correttiva.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**SequenceContext**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**INDICAZIONE CIM \_**.**SequenceNumber**")
</dt> </dl>

Contesto di sequenza dell'identificatore di sequenza per l'indicazione. Se un servizio non supporta gli identificatori di sequenza per le indicazioni, questa proprietà deve essere impostata su **NULL.** Se l'indicazione viene rieliverata, questa proprietà rimane invariata.

> [!Note]  
> L'identificatore di sequenza per l'indicazione consente a un listener di identificare le indicazioni duplicate quando il servizio tenta di ridenoverare le indicazioni, riordinare le indicazioni che arrivano non in ordine e rilevare le indicazioni perse.

 

Per assicurarsi che **SequenceContext** sia univoco, deve usare il formato seguente:

-   *indication-service-name* \# *cim-service-start-id* \# *listener-destination-creation-time*
-   *indication-service-name* è il valore della proprietà **Name** dell'istanza **cim \_ IndicationService** che recapita l'indicazione.
-   *cim-service-start-id* è un identificatore che identifica in modo univoco l'operazione di avvio di un servizio. Ad esempio, potrebbe trattarsi di un timestamp dell'ora di inizio o di un contatore che aumenta per ogni avvio o riavvio del servizio.
-   *listener-destination-creation-time* è un timestamp dell'ora di creazione dell'istanza **CIM \_ ListenerDestination** che rappresenta la destinazione del listener.nSince che questo formato è solo una raccomandazione, i client CIM trattano il valore come identificatore opaco per il contesto della sequenza e non si basano su questo formato.

</dd> <dt>

**Sequencenumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **sint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**INDICAZIONE CIM \_**.**SequenceContext**")
</dt> </dl>

Numero di sequenza dell'identificatore di sequenza per l'indicazione.

> [!Note]  
> L'identificatore di sequenza per l'indicazione consente a un listener di identificare le indicazioni duplicate quando il servizio tenta di ridenoverare le indicazioni, riordinare le indicazioni che arrivano non in ordine e rilevare le indicazioni perse.

 

Il numero di sequenza presenta le caratteristiche seguenti:

-   Il numero di sequenza viene reimpostato su "0" ogni volta che cambia il **valore sequenceContext.**
-   Ogni volta che la destinazione del listener riceve una nuova indicazione, il numero di sequenza viene aumentato di "1".
-   Il numero di sequenza esegue il wrapping su "0" quando viene superato l'intervallo di valori.
-   Se l'indicazione viene rieliverata, **SequenceNumber** rimane invariato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

