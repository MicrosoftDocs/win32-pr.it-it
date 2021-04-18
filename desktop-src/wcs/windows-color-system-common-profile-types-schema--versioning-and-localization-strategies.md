---
title: Schema dei tipi di profilo comuni di Windows Color System, strategia di controllo delle versioni e localizzazione
description: Schema dei tipi di profilo comuni di Windows Color System, strategia di controllo delle versioni e localizzazione
ms.assetid: 295522c6-7c53-47f6-9b98-aeee2b0e34fc
keywords:
- Windows Color System (WCS), tipi di profili comuni
- WCS (Windows Color System), tipi di profili comuni
- Gestione colori immagine, tipi di profili comuni
- gestione dei colori, tipi di profili comuni
- colori, tipi di profili comuni
- Windows Color System (WCS), profili
- WCS (Windows Color System), profili
- Gestione colori immagine, profili
- gestione dei colori, profili
- colori, profili
- Windows Color System (WCS), controllo delle versioni
- WCS (Windows Color System), controllo delle versioni
- Gestione colori immagine, controllo delle versioni
- gestione dei colori, controllo delle versioni
- colori, controllo delle versioni
- Windows Color System (WCS), localizzazione
- WCS (sistema di colori Windows), localizzazione
- Gestione colori immagine, localizzazione
- gestione dei colori, localizzazione
- colori, localizzazione
- Tipi di profilo comuni di WCS
- utenti del profilo
- tipi di profili comuni
- schemi, tipi di profili comuni
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814b652b654b6416b42a7a3484950273a93ea96
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "106321143"
---
# <a name="windows-color-system-common-profile-types-schema-versioning-and-localization-strategies"></a>Schema dei tipi di profilo comuni di Windows Color System, strategia di controllo delle versioni e localizzazione

-   [Schema di tipi di profilo comuni WCS V1](#wcs-common-profile-types-schema-v1)
-   [WCS Common profile types schema V2 aggiunte](#wcs-common-profile-types-schema-v2-additions)
-   [Controllo delle versioni dello schema del profilo WCS](#wcs-profile-schema-versioning)
-   [Localizzazione del profilo WCS](#wcs-profile-localization)
    -   [Espressione degli elementi localizzabili](#expressing-localizable-elements)
    -   [Supporto dello schema](#schema-support)
    -   [Selezione della lingua](#selecting-the-language)
    -   [Profili predefiniti](#built-in-profiles)
-   [Argomenti correlati](#related-topics)

## <a name="wcs-common-profile-types-schema-v1"></a>Schema di tipi di profilo comuni WCS V1

Di seguito è riportata la definizione dello schema v 1.0 per i tipi di profilo comuni WCS.


```XML
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:import namespace="http://www.w3.org/XML/1998/namespace" />

  <xs:annotation>
    <xs:documentation xml:lang="en">
      Common types used in WCS profile schemas.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:simpleType name="NonNegativeFloatType">
    <xs:restriction base="xs:float">
      <xs:minInclusive value="0"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="NonNegativeCIEXYZType">
    <xs:attribute name="X" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Y" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Z" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:simpleType name="GUIDType">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="LocalizedTextType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute ref="xml:lang" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="MultiLocalizedTextType">
    <xs:sequence>
      <xs:element name="Text" type="wcs:LocalizedTextType" minOccurs="1" />
    </xs:sequence>
  </xs:complexType>

</xs:schema>

```



Sono supportate solo le codifiche UTF-8 o UTF-16. Tutte le altre codifiche XML sono fortemente sconsigliate al fine di garantire un'interoperabilità ottimale.

## <a name="wcs-common-profile-types-schema-v2-additions"></a>WCS Common profile types schema V2 aggiunte

In Windows 7, lo schema dei tipi di profilo comuni WCS è stato aggiornato in modo da includere i tipi per supportare lo [schema di calibrazione WCS](wcs-calibration-schema.md).


```XML
  <xs:complexType name="ParameterizedCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="wcs:ParameterizedCurveType"/>
      <xs:element name="GreenTRC" type="wcs:ParameterizedCurveType"/>
      <xs:element name="BlueTRC" type="wcs:ParameterizedCurveType"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="ParameterizedCurveType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset1" type="xs:float" use="optional"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="optional"/>
    <xs:attribute name="Offset2" type="xs:float " use="optional"/>
    <xs:attribute name="TransitionPoint" type="wcs:NonNegativeFloatType" use="optional"/>
    <xs:attribute name="Offset3" type="xs:float" use="optional"/>
  </xs:complexType>

  <xs:simpleType name="FloatList">
    <xs:list itemType="xs:float"/>
  </xs:simpleType>

  <xs:complexType name="OneDimensionLutType">
    <xs:sequence>
      <xs:element name="Input" type="wcs:FloatList"/>
      <xs:element name="Output" type="wcs:FloatList"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="HDRToneResponseCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="wcs:OneDimensionLutType"/>
      <xs:element name="GreenTRC" type="wcs:OneDimensionLutType"/>
      <xs:element name="BlueTRC" type="wcs:OneDimensionLutType"/>
    </xs:sequence>
    <xs:attribute name="TRCLength" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:int">
          <xs:minInclusive value="2" />
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
```



## <a name="wcs-profile-schema-versioning"></a>Controllo delle versioni dello schema del profilo WCS

In questa appendice, il termine "consumer del profilo" si riferisce al software WCS o a un componente software di terze parti che utilizza i profili WCS.

Le versioni più recenti dei consumer di profili saranno in grado di utilizzare i profili WCS scritti in base alle versioni precedenti degli schemi. Per sfruttare appieno le funzionalità definite nella versione più recente degli schemi, in genere è richiesta la versione più recente di un consumer di profili. Tuttavia, gli utenti del profilo precedente possono utilizzare i profili scritti in base alle versioni più recenti degli schemi. Il consumer del profilo può ignorare gli elementi e gli attributi XML che non sono in grado di comprendere. I risultati saranno corretti, ma le prestazioni o la fedeltà potrebbero peggiorare rispetto ai risultati ottenuti con la versione più recente del consumer del profilo.

Di seguito sono riportate le linee guida per il controllo delle versioni dei consumer

-   Una determinata versione di un consumer del profilo deve riconoscere tutti gli elementi e gli attributi di uno spazio dei nomi della versione o nessuno di essi.
-   Se un consumer del profilo rileva un elemento o un attributo da uno spazio dei nomi che non è in grado di comprendere, deve considerarlo come una condizione di errore, a meno che il profilo non contenga istruzioni esplicite sull'elaborazione del fallback.
-   La [specifica Open Packaging](https://www.microsoft.com/whdc/xps/xpspkg.mspx) definisce un URI dello spazio dei nomi aggiuntivo, ovvero lo spazio dei nomi di compatibilità del markup, che definisce gli elementi e gli attributi che forniscono le linee guida per l'elaborazione
-   Tutte le versioni di tutti i consumer del profilo devono riconoscere e rispettare tutti gli elementi e gli attributi nello spazio dei nomi di compatibilità del markup.
-   I consumer del profilo basati su una nuova versione degli schemi del profilo devono supportare tutti gli spazi dei nomi della versione definiti in precedenza.

Nella versione 1.0 il WCS riconosce gli elementi e gli attributi degli spazi dei nomi seguenti:

-   https://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel
-   https://schemas.microsoft.com/windows/2005/02/color/GamutMapModel
-   https://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
-   https://schemas.microsoft.com/winfx/2005/06/markup-compatibility

Di seguito viene illustrato un esempio di compatibilità dei markup.


```XML
<?xml version="1.0" encoding="utf-8" ?>
<ColorAppearanceModel
  xmlns=http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
  xmlns:cam2=http://schemas.microsoft.com/windows/2007/08/color/ColorAppearanceModel
  xmlns:mc=http://schemas.microsoft.com/winfx/2005/02/markup-compatibility
  xs:schemaLocation="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel ColorAppearanceModel.xsd"
  xmlns:xs='http://www.w3.org/2001/XMLSchema-instance'
  mc:Ignorable="cam2">

  <ProfileName>Default profile for ICC viewing conditions</ProfileName>
  <mc:AlternateContent>
    <mc:Choice Requires="cam2">
      <cam2:AudioDescription source="ProfileExplanation.wav"/>
    </mc:Choice>
    <mc:Fallback>
      <Description>Appropriate for a print in a D50 viewing booth</Description>
        </mc:Fallback>
  </mc:AlternateContent>
  <Author>Microsoft</Author>

  <ViewingConditions>
    <WhitePointName>D50</WhitePointName>
    <Background X="19.3" Y="20.0" Z="16.5" />
    <Surround>Average</Surround>
    <LuminanceOfAdaptingField>31.8</LuminanceOfAdaptingField>
    <DegreeOfAdaptation>-1</DegreeOfAdaptation>
    <cam2:Humidity>30%</cam2:Humidity>
  </ViewingConditions>

</ColorAppearanceModel>
```



## <a name="wcs-profile-localization"></a>Localizzazione del profilo WCS

**Requisiti**

I profili WCS contengono determinati elementi, ad esempio ProfileName e Description, che contengono testo leggibile. Questo testo è localizzabile.

Di seguito sono riportate le linee guida per la creazione di profili:

-   Per i profili creati da terze parti, ad esempio i produttori di stampanti, l'autore del profilo deve incorporare testo descrittivo in più linguaggi.
-   Gli elementi seguenti devono essere localizzabili: 

    | Elemento     | CDMP | GMMP | CAMPO |
    |-------------|------|------|------|
    | ProfileName | x    | x    | x    |
    | Descrizione | x    | x    | x    |
    | Autore      | x    | x    | x    |

    

     

### <a name="expressing-localizable-elements"></a>Espressione degli elementi localizzabili

Anziché contenere direttamente il testo, ogni elemento localizzabile contiene uno o più elementi secondari WCS: text, ognuno dei quali deve specificare l'attributo XML: lang. Come descritto nella sezione 2,12 della [specifica XML](http://www.w3.org/TR/REC-xml/) ("identificazione della lingua"), il valore dell'attributo XML: lang deve essere un identificatore di lingua IETF RFC 3066, ad esempio "en-US", "en" o "FR-FR". Negli schemi WCS, il valore dell'attributo XML: lang non deve essere la stringa vuota "", anche se XML lo consente nel caso generale. Ad esempio:


```XML
<cdm:ColorDeviceModel ... />
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceeModel>
```



Due elementi WCS: text possono avere lo stesso attributo XML: lang. Ogni schema del profilo WCS deve applicare questo vincolo separatamente per ogni elemento localizzabile. Sono supportate solo le codifiche UTF-8 e UTF-16.

### <a name="schema-support"></a>Supporto dello schema

La progettazione si avvale dei tipi XSD WCS: LocalizedText e WCS: MultiLocalizedType definiti nello schema del tipo di profilo comune WCS:


```XML
    <xs:complexType name="LocalizedText">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="xml:lang" type="xs:string" use="required"/>
            <xs:extension/>
        <xs:simpleContent/>
    </xs:complexType/>

    <xs:complexType name="MultiLocalizedType">
        <xs:element name="Text" type="cam:LocalizedText" minOccurs="1"/>
    </xs:complexType>
```



Ogni schema del profilo WCS dichiara che ogni elemento localizzabile è di tipo MultiLocalizedType, ad esempio:


```XML
<xs:schema 
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
    xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
    targetNamespace=
        "http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
    version="1.0">
    <xs:import namespace=
        "http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"/>

    <xs:element name="cdm:Description" type="wcs:MultiLocalizableType" minOccurs="0"/>

    <xs:unique name="uniqueDescriptionLanguage">
      <xs:selector xpath="cdm:ColorDeviceModel/cdm:Description/wcs:Text"/>
      <xs:field xpath="@xml:lang"/>
    </unique>

    ...
</xs:schema>
```



Lo schema CDMP impone il vincolo che ogni WCS: Text Child dell'elemento CDM: Description deve avere un attributo XML: lang univoco. Viene applicato lo stesso vincolo per gli altri elementi localizzabili. Gli schemi CAMP e GMMP eseguono le stesse operazioni.

### <a name="selecting-the-language"></a>Selezione della lingua

Quando si decide quale versione della lingua di un elemento localizzabile visualizzare, il codice dell'applicazione deve selezionare la "versione più vicina" alla "lingua corrente". La "versione più vicina" e la "lingua corrente" significano effettivamente dipende dalla piattaforma; vedere di seguito. Se il profilo non contiene una versione della lingua corrispondente alla lingua corrente, l'applicazione deve selezionare la prima versione nel profilo, ovvero il primo elemento WCS: Text figlio dell'elemento localizzabile.

In Windows Vista, la selezione della lingua viene eseguita nel modo seguente: ogni thread ha un elenco associato di "lingue dell'interfaccia utente preferite", che è possibile ottenere chiamando [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages). L'elenco viene restituito in ordine di preferenza dell'utente. Ad esempio, in un sistema configurato per la lingua inglese (Stati Uniti), l'elenco restituito da **GetThreadPreferredUILanguages** è {"en-US", "en"}. Questo significa: 1) Inglese (Stati Uniti) se presente. 2) in caso contrario, utilizzare qualsiasi variante di lingua inglese, ad esempio "en-GB" o semplicemente "en".

Per ogni lingua nell'elenco, in ordine di elenco, il codice dell'interfaccia utente cerca un elemento WCS: text il cui attributo XML: lang è una corrispondenza esatta. Viene utilizzata la prima versione corrispondente. Se nessuna versione corrisponde, viene usato il primo elemento WCS: Text.

### <a name="built-in-profiles"></a>Profili predefiniti

I profili WCS standard forniti con Windows Vista, ad esempio sRGB. CDMP, hanno le stesse proprietà localizzabili di altri profili.

La soluzione Windows standard consiste nell'inserire le stringhe localizzate in una DLL MUI e farvi riferimento come segue:


```XML
<cdm:Description resourceId="mscms.dll,-101">
    <wcs:Text xml:lang="en-US">Hello, world!</wcs:Text>
<cdm:Description>
```



In un sistema Windows, il testo della descrizione verrebbe estratto dall'ID risorsa 101 nella versione localizzata appropriata delle risorse MUI per mscms.dll. I sistemi non Windows useranno i sottoelementi WCS: text come descritto in precedenza.

Viene introdotto un attributo ID univoco globale facoltativo sull'elemento radice di ogni schema del profilo WCS. Il profilo standard wcsRGB. CDMP potrebbe essere simile al seguente:


```XML
<cdm:ColorDeviceModel
    ID=http://schemas.microsoft.com/2005/02/color/profiles/wcsRGB.cdmp
    ... >
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello.</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour.</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceModel>
```



Per i profili dei colori WCS forniti con Windows, il colore CPL Visualizza le informazioni descrittive dalle risorse anziché dagli elementi WCS: text nei profili. In questo modo Windows può visualizzare le informazioni localizzate per questi profili in tutte le lingue supportate, senza richiedere che i profili themlselves contengano informazioni descrittive in tutte le lingue.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base sulla gestione dei colori](basic-color-management-concepts.md)
</dt> <dt>

[Schemi e algoritmi del sistema di colori Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 