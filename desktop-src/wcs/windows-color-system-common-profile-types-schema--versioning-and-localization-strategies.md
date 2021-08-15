---
title: Windows Schema dei tipi di profilo comuni del sistema colori, strategie di controllo delle versioni e localizzazione
description: Windows Schema dei tipi di profilo comuni del sistema colori, strategie di controllo delle versioni e localizzazione
ms.assetid: 295522c6-7c53-47f6-9b98-aeee2b0e34fc
keywords:
- Windows Sistema colori (WCS), tipi di profilo comuni
- WCS (Windows Color System),tipi di profilo comuni
- gestione dei colori delle immagini, tipi di profilo comuni
- gestione dei colori, tipi di profilo comuni
- colori, tipi di profilo comuni
- Windows Sistema colori (WCS), profili
- WCS (Windows Color System),profiles
- gestione dei colori delle immagini, profili
- gestione dei colori, profili
- colori, profili
- Windows Sistema colori (WCS), controllo delle versioni
- WCS (Windows Color System),controllo delle versioni
- gestione dei colori delle immagini, controllo delle versioni
- gestione dei colori, controllo delle versioni
- colori, controllo delle versioni
- Windows sistema di colori (WCS), localizzazione
- WCS (Windows Color System),localizzazione
- gestione dei colori delle immagini, localizzazione
- gestione dei colori, localizzazione
- colori, localizzazione
- Tipi di profilo comuni WCS
- consumer di profili
- tipi di profilo comuni
- schemi, tipi di profilo comuni
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c9df44fa7095d8cbcd3df6de00c92ba2d4ab2ddb7ef7d3565a820e925265ea0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442291"
---
# <a name="windows-color-system-common-profile-types-schema-versioning-and-localization-strategies"></a>Windows Schema dei tipi di profilo comuni del sistema colori, strategie di controllo delle versioni e localizzazione

-   [Schema dei tipi di profilo comuni WCS V1](#wcs-common-profile-types-schema-v1)
-   [Aggiunte dello schema V2 dei tipi di profilo comuni WCS](#wcs-common-profile-types-schema-v2-additions)
-   [Controllo delle versioni dello schema del profilo WCS](#wcs-profile-schema-versioning)
-   [Localizzazione dei profili WCS](#wcs-profile-localization)
    -   [Espressione di elementi localizzabili](#expressing-localizable-elements)
    -   [Supporto dello schema](#schema-support)
    -   [Selezione della lingua](#selecting-the-language)
    -   [Profili predefiniti](#built-in-profiles)
-   [Argomenti correlati](#related-topics)

## <a name="wcs-common-profile-types-schema-v1"></a>Schema dei tipi di profilo comuni WCS V1

Di seguito viene fornita la definizione dello schema v1.0 per i tipi di profilo comuni WCS.


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



Sono supportate solo codifiche UTF-8 o UTF-16. Tutte le altre codifiche XML sono fortemente sconsigliate per mantenere un'interoperabilità ottimale.

## <a name="wcs-common-profile-types-schema-v2-additions"></a>Aggiunte dello schema V2 dei tipi di profilo comuni WCS

In Windows 7 lo schema WCS Common Profile Types è stato aggiornato per includere i tipi per supportare lo [schema di calibrazione WCS](wcs-calibration-schema.md).


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

In questa Appendice il termine "consumer di profili" si riferisce al software WCS o a un componente software di terze parti che utilizza profili WCS.

Le versioni più recenti dei consumer di profili saranno in grado di utilizzare i profili WCS scritti in base alle versioni precedenti degli schemi. Per sfruttare al meglio le funzionalità definite nella versione più recente degli schemi, sarà in genere necessaria la versione più recente di un consumer di profili. Tuttavia, i consumer di profili meno recenti possono utilizzare i profili scritti in base alle versioni più recenti degli schemi. Il consumer del profilo può ignorare gli elementi e gli attributi XML che non è in grado di comprendere. I risultati saranno corretti, ma le prestazioni o la fedeltà potrebbero peggiorare rispetto ai risultati ottenuti con la versione più recente del consumer del profilo.

Di seguito sono riportate le linee guida per il controllo delle versioni per i consumer del profilo:

-   Una determinata versione di un consumer del profilo deve riconoscere tutti gli elementi e gli attributi di uno spazio dei nomi della versione o nessuno di essi.
-   Se un consumer del profilo rileva un elemento o un attributo da uno spazio dei nomi non compreso, deve considerarlo come una condizione di errore, a meno che il profilo non contenga indicazioni esplicite sull'elaborazione del fallback.
-   Open [Packaging Specification definisce un](https://www.microsoft.com/whdc/xps/xpspkg.mspx) URI dello spazio dei nomi aggiuntivo, lo spazio dei nomi di compatibilità del markup, che definisce gli elementi e gli attributi che forniscono queste linee guida per l'elaborazione del fallback.
-   Tutte le versioni di tutti i consumer di profili devono riconoscere e rispettare tutti gli elementi e gli attributi nello spazio dei nomi di compatibilità del markup.
-   I consumer di profili basati su una nuova versione degli schemi del profilo devono supportare tutti gli spazi dei nomi delle versioni definiti in precedenza.

Nella versione 1.0 WCS riconosce gli elementi e gli attributi dagli spazi dei nomi seguenti:

-   https://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel
-   https://schemas.microsoft.com/windows/2005/02/color/GamutMapModel
-   https://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
-   https://schemas.microsoft.com/winfx/2005/06/markup-compatibility

Di seguito viene illustrato un esempio di compatibilità del markup.


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



## <a name="wcs-profile-localization"></a>Localizzazione dei profili WCS

**Requisiti**

I profili WCS contengono determinati elementi, ad esempio ProfileName e Description, che contengono testo leggibile. Questo testo è localizzabile.

Di seguito sono riportate le linee guida per il controllo delle versioni per gli autori di profili:

-   Per i profili creati da terze parti, ad esempio i produttori di stampanti, l'autore del profilo deve incorporare testo descrittivo in più lingue.
-   Gli elementi seguenti devono essere localizzabili: 

    | Elemento     | CDMP | GMMP | Campo |
    |-------------|------|------|------|
    | ProfileName | x    | x    | x    |
    | Descrizione | x    | x    | x    |
    | Autore      | x    | x    | x    |

    

     

### <a name="expressing-localizable-elements"></a>Espressione di elementi localizzabili

Anziché contenere direttamente testo, ogni elemento localizzabile contiene uno o più sotto-elementi wcs:Text, ognuno dei quali deve specificare l'attributo xml:lang. Come descritto nella sezione 2.12 della specifica [XML](http://www.w3.org/TR/REC-xml/) ("Identificazione della lingua"), il valore dell'attributo xml:lang deve essere un identificatore di lingua IETF RFC 3066, ad esempio "en-US", "en" o "fr-FR". Negli schemi WCS, il valore dell'attributo xml:lang non deve essere la stringa vuota "", anche se XML lo consente in generale. Esempio:


```XML
<cdm:ColorDeviceModel ... />
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceeModel>
```



Due elementi wcs:Text non possono avere lo stesso attributo xml:lang. Ogni schema del profilo WCS deve applicare questo vincolo separatamente per ogni elemento localizzabile. Sono supportate solo le codifiche UTF-8 e UTF-16.

### <a name="schema-support"></a>Supporto dello schema

La progettazione usa i tipi XSD wcs:LocalizedText e wcs:MultiLocalizedType definiti nello schema WCS Common Profile Type:


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



Ogni schema del profilo WCS dichiara ogni elemento localizzabile come di tipo MultiLocalizedType, ad esempio:


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



Lo schema CDMP applica il vincolo che ogni elemento figlio wcs:Text dell'elemento cdm:Description deve avere un attributo xml:lang univoco. Applica lo stesso vincolo per gli altri elementi localizzabili. Gli schemiCAMP e GMMP esempiano la stessa operazione.

### <a name="selecting-the-language"></a>Selezione della lingua

Quando si decide quale versione della lingua di un elemento localizzabile visualizzare, il codice dell'applicazione deve selezionare la "versione più vicina" alla "lingua corrente". Il significato di "versione più vicina" e "lingua corrente" dipende dalla piattaforma; vedere di seguito. Se il profilo non contiene una versione della lingua corrispondente alla lingua corrente, l'applicazione deve selezionare la prima versione nel profilo (il primo elemento figlio wcs:Text dell'elemento localizzabile).

In Windows Vista la selezione della lingua viene eseguita nel modo seguente: ogni thread ha un elenco associato di "lingue preferite dell'interfaccia utente", che possono essere ottenute chiamando [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages). L'elenco viene restituito in ordine di preferenza dell'utente. Ad esempio, in un sistema configurato per l'inglese degli Stati Uniti, l'elenco restituito da **GetThreadPreferredUILanguages** è { "en-US", "en" }. Ciò significa: 1) Inglese Stati Uniti, se presente. 2) In caso contrario, usare qualsiasi variante regionale dell'inglese, ad esempio "en-GB" o semplicemente "en".

Per ogni lingua nell'elenco, in ordine di elenco, il codice dell'interfaccia utente cerca un elemento wcs:Text il cui attributo xml:lang è una corrispondenza esatta. Viene usata la prima versione corrispondente. Se nessuna versione corrisponde, viene usato il primo elemento wcs:Text.

### <a name="built-in-profiles"></a>Profili predefiniti

I profili WCS standard forniti con Windows Vista, ad esempio sRGB.cdmp, hanno le stesse proprietà localizzabili di altri profili.

La soluzione Windows standard consiste nell'inserire le stringhe localizzate in una DLL MUI e fare riferimento a tali stringhe in questo modo:The standard Windows solution would be to put the localized strings in a MUI DLL, and refer to them like this:


```XML
<cdm:Description resourceId="mscms.dll,-101">
    <wcs:Text xml:lang="en-US">Hello, world!</wcs:Text>
<cdm:Description>
```



In un Windows, il testo della descrizione viene estratto dall'ID risorsa 101 nella versione localizzata appropriata delle risorse MUI per mscms.dll. I sistemi Windows usano i sotto-elementi wcs:Text come descritto in precedenza.

Viene introdotto un attributo ID univoco globale facoltativo nell'elemento radice di ogni schema del profilo WCS. Il profilo standard wcsRGB.cdmp potrebbe essere simile al seguente:


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



Per i profili colori WCS forniti con le finestre, color CPL visualizza informazioni descrittive dalle risorse, anziché dagli elementi wcs:Text nei profili. Ciò consente Windows informazioni localizzate per questi profili in tutte le lingue supportate, senza richiedere che i profili contengano informazioni descrittive in tutte le lingue.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base sulla gestione dei colori](basic-color-management-concepts.md)
</dt> <dt>

[Windows Schemi e algoritmi del sistema di colori](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 