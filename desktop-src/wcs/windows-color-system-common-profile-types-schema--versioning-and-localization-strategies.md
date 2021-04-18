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
# <a name="windows-color-system-common-profile-types-schema-versioning-and-localization-strategies"></a><span data-ttu-id="056d6-127">Schema dei tipi di profilo comuni di Windows Color System, strategia di controllo delle versioni e localizzazione</span><span class="sxs-lookup"><span data-stu-id="056d6-127">Windows Color System Common Profile Types schema, Versioning and Localization Strategies</span></span>

-   [<span data-ttu-id="056d6-128">Schema di tipi di profilo comuni WCS V1</span><span class="sxs-lookup"><span data-stu-id="056d6-128">WCS Common Profile Types Schema V1</span></span>](#wcs-common-profile-types-schema-v1)
-   [<span data-ttu-id="056d6-129">WCS Common profile types schema V2 aggiunte</span><span class="sxs-lookup"><span data-stu-id="056d6-129">WCS Common Profile Types Schema V2 Additions</span></span>](#wcs-common-profile-types-schema-v2-additions)
-   [<span data-ttu-id="056d6-130">Controllo delle versioni dello schema del profilo WCS</span><span class="sxs-lookup"><span data-stu-id="056d6-130">WCS Profile Schema Versioning</span></span>](#wcs-profile-schema-versioning)
-   [<span data-ttu-id="056d6-131">Localizzazione del profilo WCS</span><span class="sxs-lookup"><span data-stu-id="056d6-131">WCS Profile Localization</span></span>](#wcs-profile-localization)
    -   [<span data-ttu-id="056d6-132">Espressione degli elementi localizzabili</span><span class="sxs-lookup"><span data-stu-id="056d6-132">Expressing localizable elements</span></span>](#expressing-localizable-elements)
    -   [<span data-ttu-id="056d6-133">Supporto dello schema</span><span class="sxs-lookup"><span data-stu-id="056d6-133">Schema Support</span></span>](#schema-support)
    -   [<span data-ttu-id="056d6-134">Selezione della lingua</span><span class="sxs-lookup"><span data-stu-id="056d6-134">Selecting the Language</span></span>](#selecting-the-language)
    -   [<span data-ttu-id="056d6-135">Profili predefiniti</span><span class="sxs-lookup"><span data-stu-id="056d6-135">Built-in profiles</span></span>](#built-in-profiles)
-   [<span data-ttu-id="056d6-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="056d6-136">Related topics</span></span>](#related-topics)

## <a name="wcs-common-profile-types-schema-v1"></a><span data-ttu-id="056d6-137">Schema di tipi di profilo comuni WCS V1</span><span class="sxs-lookup"><span data-stu-id="056d6-137">WCS Common Profile Types Schema V1</span></span>

<span data-ttu-id="056d6-138">Di seguito è riportata la definizione dello schema v 1.0 per i tipi di profilo comuni WCS.</span><span class="sxs-lookup"><span data-stu-id="056d6-138">The following provides the v1.0 schema definition for the WCS Common Profile Types.</span></span>


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



<span data-ttu-id="056d6-139">Sono supportate solo le codifiche UTF-8 o UTF-16.</span><span class="sxs-lookup"><span data-stu-id="056d6-139">Only UTF-8 or UTF-16 encodings are supported.</span></span> <span data-ttu-id="056d6-140">Tutte le altre codifiche XML sono fortemente sconsigliate al fine di garantire un'interoperabilità ottimale.</span><span class="sxs-lookup"><span data-stu-id="056d6-140">All other XML encodings are strongly discouraged in order to preserve optimum interoperability.</span></span>

## <a name="wcs-common-profile-types-schema-v2-additions"></a><span data-ttu-id="056d6-141">WCS Common profile types schema V2 aggiunte</span><span class="sxs-lookup"><span data-stu-id="056d6-141">WCS Common Profile Types Schema V2 Additions</span></span>

<span data-ttu-id="056d6-142">In Windows 7, lo schema dei tipi di profilo comuni WCS è stato aggiornato in modo da includere i tipi per supportare lo [schema di calibrazione WCS](wcs-calibration-schema.md).</span><span class="sxs-lookup"><span data-stu-id="056d6-142">In Windows 7, the WCS Common Profile Types schema has been updated to include types to support the [WCS Calibration schema](wcs-calibration-schema.md).</span></span>


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



## <a name="wcs-profile-schema-versioning"></a><span data-ttu-id="056d6-143">Controllo delle versioni dello schema del profilo WCS</span><span class="sxs-lookup"><span data-stu-id="056d6-143">WCS Profile Schema Versioning</span></span>

<span data-ttu-id="056d6-144">In questa appendice, il termine "consumer del profilo" si riferisce al software WCS o a un componente software di terze parti che utilizza i profili WCS.</span><span class="sxs-lookup"><span data-stu-id="056d6-144">In this Appendix, the term "profile consumer" refers to the WCS software, or to a third-party software component that consumes WCS profiles.</span></span>

<span data-ttu-id="056d6-145">Le versioni più recenti dei consumer di profili saranno in grado di utilizzare i profili WCS scritti in base alle versioni precedenti degli schemi.</span><span class="sxs-lookup"><span data-stu-id="056d6-145">Newer versions of profile consumers will be able to consume WCS profiles written according to older versions of the schemas.</span></span> <span data-ttu-id="056d6-146">Per sfruttare appieno le funzionalità definite nella versione più recente degli schemi, in genere è richiesta la versione più recente di un consumer di profili.</span><span class="sxs-lookup"><span data-stu-id="056d6-146">To take full advantage of features defined in the newest version of the schemas, the newest version of a profile consumer will generally be required.</span></span> <span data-ttu-id="056d6-147">Tuttavia, gli utenti del profilo precedente possono utilizzare i profili scritti in base alle versioni più recenti degli schemi.</span><span class="sxs-lookup"><span data-stu-id="056d6-147">However, older profile consumers can consume profiles written according to newer versions of the schemas.</span></span> <span data-ttu-id="056d6-148">Il consumer del profilo può ignorare gli elementi e gli attributi XML che non sono in grado di comprendere.</span><span class="sxs-lookup"><span data-stu-id="056d6-148">The profile consumer can ignore XML elements and attributes that it does not understand.</span></span> <span data-ttu-id="056d6-149">I risultati saranno corretti, ma le prestazioni o la fedeltà potrebbero peggiorare rispetto ai risultati ottenuti con la versione più recente del consumer del profilo.</span><span class="sxs-lookup"><span data-stu-id="056d6-149">The results will be correct, but performance or fidelity may degraded as compared to the results achieved with the newest version of the profile consumer.</span></span>

<span data-ttu-id="056d6-150">Di seguito sono riportate le linee guida per il controllo delle versioni dei consumer</span><span class="sxs-lookup"><span data-stu-id="056d6-150">The following are versioning guidelines for profile consumers:</span></span>

-   <span data-ttu-id="056d6-151">Una determinata versione di un consumer del profilo deve riconoscere tutti gli elementi e gli attributi di uno spazio dei nomi della versione o nessuno di essi.</span><span class="sxs-lookup"><span data-stu-id="056d6-151">A given version of a profile consumer must recognize either all of the elements and attributes from a version namespace, or none of them.</span></span>
-   <span data-ttu-id="056d6-152">Se un consumer del profilo rileva un elemento o un attributo da uno spazio dei nomi che non è in grado di comprendere, deve considerarlo come una condizione di errore, a meno che il profilo non contenga istruzioni esplicite sull'elaborazione del fallback.</span><span class="sxs-lookup"><span data-stu-id="056d6-152">If a profile consumer encounters an element or attribute from a namespace that it does not understand, it must treat this as an error condition, unless the profile contains explicit guidance on fallback processing.</span></span>
-   <span data-ttu-id="056d6-153">La [specifica Open Packaging](https://www.microsoft.com/whdc/xps/xpspkg.mspx) definisce un URI dello spazio dei nomi aggiuntivo, ovvero lo spazio dei nomi di compatibilità del markup, che definisce gli elementi e gli attributi che forniscono le linee guida per l'elaborazione</span><span class="sxs-lookup"><span data-stu-id="056d6-153">The [Open Packaging Specification](https://www.microsoft.com/whdc/xps/xpspkg.mspx) defines an additional namespace URI, the markup compatibility namespace, which defines elements and attributes that provide this fallback processing guidance.</span></span>
-   <span data-ttu-id="056d6-154">Tutte le versioni di tutti i consumer del profilo devono riconoscere e rispettare tutti gli elementi e gli attributi nello spazio dei nomi di compatibilità del markup.</span><span class="sxs-lookup"><span data-stu-id="056d6-154">All versions of all profile consumers must recognize and respect all the elements and attributes in the markup compatibility namespace.</span></span>
-   <span data-ttu-id="056d6-155">I consumer del profilo basati su una nuova versione degli schemi del profilo devono supportare tutti gli spazi dei nomi della versione definiti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="056d6-155">Profile consumers based on a new version of the profile schemas must support all previously defined version namespaces.</span></span>

<span data-ttu-id="056d6-156">Nella versione 1.0 il WCS riconosce gli elementi e gli attributi degli spazi dei nomi seguenti:</span><span class="sxs-lookup"><span data-stu-id="056d6-156">In the v1.0 release, WCS recognizes elements and attributes from the following namespaces:</span></span>

-   https://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel
-   https://schemas.microsoft.com/windows/2005/02/color/GamutMapModel
-   https://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
-   https://schemas.microsoft.com/winfx/2005/06/markup-compatibility

<span data-ttu-id="056d6-157">Di seguito viene illustrato un esempio di compatibilità dei markup.</span><span class="sxs-lookup"><span data-stu-id="056d6-157">The following demonstrates an example of markup compatibility.</span></span>


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



## <a name="wcs-profile-localization"></a><span data-ttu-id="056d6-158">Localizzazione del profilo WCS</span><span class="sxs-lookup"><span data-stu-id="056d6-158">WCS Profile Localization</span></span>

<span data-ttu-id="056d6-159">**Requisiti**</span><span class="sxs-lookup"><span data-stu-id="056d6-159">**Requirements**</span></span>

<span data-ttu-id="056d6-160">I profili WCS contengono determinati elementi, ad esempio ProfileName e Description, che contengono testo leggibile.</span><span class="sxs-lookup"><span data-stu-id="056d6-160">WCS profiles contain certain elements such as ProfileName and Description which contain human-readable text.</span></span> <span data-ttu-id="056d6-161">Questo testo è localizzabile.</span><span class="sxs-lookup"><span data-stu-id="056d6-161">This text is localizable.</span></span>

<span data-ttu-id="056d6-162">Di seguito sono riportate le linee guida per la creazione di profili:</span><span class="sxs-lookup"><span data-stu-id="056d6-162">The following are versioning guidelines for profile creators:</span></span>

-   <span data-ttu-id="056d6-163">Per i profili creati da terze parti, ad esempio i produttori di stampanti, l'autore del profilo deve incorporare testo descrittivo in più linguaggi.</span><span class="sxs-lookup"><span data-stu-id="056d6-163">For profiles created by 3rd parties such as printer manufacturers, the profile author should incorporate descriptive text in multiple languages.</span></span>
-   <span data-ttu-id="056d6-164">Gli elementi seguenti devono essere localizzabili:</span><span class="sxs-lookup"><span data-stu-id="056d6-164">The following elements should be localizable:</span></span> 

    | <span data-ttu-id="056d6-165">Elemento</span><span class="sxs-lookup"><span data-stu-id="056d6-165">Element</span></span>     | <span data-ttu-id="056d6-166">CDMP</span><span class="sxs-lookup"><span data-stu-id="056d6-166">CDMP</span></span> | <span data-ttu-id="056d6-167">GMMP</span><span class="sxs-lookup"><span data-stu-id="056d6-167">GMMP</span></span> | <span data-ttu-id="056d6-168">CAMPO</span><span class="sxs-lookup"><span data-stu-id="056d6-168">CAMP</span></span> |
    |-------------|------|------|------|
    | <span data-ttu-id="056d6-169">ProfileName</span><span class="sxs-lookup"><span data-stu-id="056d6-169">ProfileName</span></span> | <span data-ttu-id="056d6-170">x</span><span class="sxs-lookup"><span data-stu-id="056d6-170">x</span></span>    | <span data-ttu-id="056d6-171">x</span><span class="sxs-lookup"><span data-stu-id="056d6-171">x</span></span>    | <span data-ttu-id="056d6-172">x</span><span class="sxs-lookup"><span data-stu-id="056d6-172">x</span></span>    |
    | <span data-ttu-id="056d6-173">Descrizione</span><span class="sxs-lookup"><span data-stu-id="056d6-173">Description</span></span> | <span data-ttu-id="056d6-174">x</span><span class="sxs-lookup"><span data-stu-id="056d6-174">x</span></span>    | <span data-ttu-id="056d6-175">x</span><span class="sxs-lookup"><span data-stu-id="056d6-175">x</span></span>    | <span data-ttu-id="056d6-176">x</span><span class="sxs-lookup"><span data-stu-id="056d6-176">x</span></span>    |
    | <span data-ttu-id="056d6-177">Autore</span><span class="sxs-lookup"><span data-stu-id="056d6-177">Author</span></span>      | <span data-ttu-id="056d6-178">x</span><span class="sxs-lookup"><span data-stu-id="056d6-178">x</span></span>    | <span data-ttu-id="056d6-179">x</span><span class="sxs-lookup"><span data-stu-id="056d6-179">x</span></span>    | <span data-ttu-id="056d6-180">x</span><span class="sxs-lookup"><span data-stu-id="056d6-180">x</span></span>    |

    

     

### <a name="expressing-localizable-elements"></a><span data-ttu-id="056d6-181">Espressione degli elementi localizzabili</span><span class="sxs-lookup"><span data-stu-id="056d6-181">Expressing localizable elements</span></span>

<span data-ttu-id="056d6-182">Anziché contenere direttamente il testo, ogni elemento localizzabile contiene uno o più elementi secondari WCS: text, ognuno dei quali deve specificare l'attributo XML: lang.</span><span class="sxs-lookup"><span data-stu-id="056d6-182">Instead of directly containing text, each localizable element contains one or more wcs:Text sub-elements, each of which must specify the xml:lang attribute.</span></span> <span data-ttu-id="056d6-183">Come descritto nella sezione 2,12 della [specifica XML](http://www.w3.org/TR/REC-xml/) ("identificazione della lingua"), il valore dell'attributo XML: lang deve essere un identificatore di lingua IETF RFC 3066, ad esempio "en-US", "en" o "FR-FR".</span><span class="sxs-lookup"><span data-stu-id="056d6-183">As described in the [XML specification](http://www.w3.org/TR/REC-xml/) Section 2.12 ("Language Identification"), the value of the xml:lang attribute must be an IETF RFC 3066 language identifier such as "en-US", "en", or "fr-FR".</span></span> <span data-ttu-id="056d6-184">Negli schemi WCS, il valore dell'attributo XML: lang non deve essere la stringa vuota "", anche se XML lo consente nel caso generale.</span><span class="sxs-lookup"><span data-stu-id="056d6-184">In WCS schemas, the value of the xml:lang attribute must not be the empty string "", even though XML allows this in the general case.</span></span> <span data-ttu-id="056d6-185">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="056d6-185">For example:</span></span>


```XML
<cdm:ColorDeviceModel ... />
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceeModel>
```



<span data-ttu-id="056d6-186">Due elementi WCS: text possono avere lo stesso attributo XML: lang.</span><span class="sxs-lookup"><span data-stu-id="056d6-186">No two wcs:Text elements can have the same xml:lang attribute.</span></span> <span data-ttu-id="056d6-187">Ogni schema del profilo WCS deve applicare questo vincolo separatamente per ogni elemento localizzabile.</span><span class="sxs-lookup"><span data-stu-id="056d6-187">Each WCS profile schema must enforce this constraint separately for each localizable element.</span></span> <span data-ttu-id="056d6-188">Sono supportate solo le codifiche UTF-8 e UTF-16.</span><span class="sxs-lookup"><span data-stu-id="056d6-188">Only UTF-8 and UTF-16 encodings are supported.</span></span>

### <a name="schema-support"></a><span data-ttu-id="056d6-189">Supporto dello schema</span><span class="sxs-lookup"><span data-stu-id="056d6-189">Schema Support</span></span>

<span data-ttu-id="056d6-190">La progettazione si avvale dei tipi XSD WCS: LocalizedText e WCS: MultiLocalizedType definiti nello schema del tipo di profilo comune WCS:</span><span class="sxs-lookup"><span data-stu-id="056d6-190">The design makes use of the XSD types wcs:LocalizedText and wcs:MultiLocalizedType defined in the WCS Common Profile Type schema:</span></span>


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



<span data-ttu-id="056d6-191">Ogni schema del profilo WCS dichiara che ogni elemento localizzabile è di tipo MultiLocalizedType, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="056d6-191">Each WCS profile schema declares each localizable element to be of type MultiLocalizedType, for example:</span></span>


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



<span data-ttu-id="056d6-192">Lo schema CDMP impone il vincolo che ogni WCS: Text Child dell'elemento CDM: Description deve avere un attributo XML: lang univoco.</span><span class="sxs-lookup"><span data-stu-id="056d6-192">The CDMP schema enforces the constraint that each wcs:Text child of the cdm:Description element must have a unique xml:lang attribute.</span></span> <span data-ttu-id="056d6-193">Viene applicato lo stesso vincolo per gli altri elementi localizzabili.</span><span class="sxs-lookup"><span data-stu-id="056d6-193">It enforces the same constraint for the other localizable elements.</span></span> <span data-ttu-id="056d6-194">Gli schemi CAMP e GMMP eseguono le stesse operazioni.</span><span class="sxs-lookup"><span data-stu-id="056d6-194">The CAMP and GMMP schemas do the same.</span></span>

### <a name="selecting-the-language"></a><span data-ttu-id="056d6-195">Selezione della lingua</span><span class="sxs-lookup"><span data-stu-id="056d6-195">Selecting the Language</span></span>

<span data-ttu-id="056d6-196">Quando si decide quale versione della lingua di un elemento localizzabile visualizzare, il codice dell'applicazione deve selezionare la "versione più vicina" alla "lingua corrente".</span><span class="sxs-lookup"><span data-stu-id="056d6-196">When deciding which language version of a localizable element to display, application code should select the "closest version" to the "current language".</span></span> <span data-ttu-id="056d6-197">La "versione più vicina" e la "lingua corrente" significano effettivamente dipende dalla piattaforma; vedere di seguito.</span><span class="sxs-lookup"><span data-stu-id="056d6-197">What "closest version" and "current language" actually mean is platform-dependent; see below.</span></span> <span data-ttu-id="056d6-198">Se il profilo non contiene una versione della lingua corrispondente alla lingua corrente, l'applicazione deve selezionare la prima versione nel profilo, ovvero il primo elemento WCS: Text figlio dell'elemento localizzabile.</span><span class="sxs-lookup"><span data-stu-id="056d6-198">If the profile does not contain a language version that matches the current language, the application should select the first version in the profile (the first wcs:Text child element of the localizable element).</span></span>

<span data-ttu-id="056d6-199">In Windows Vista, la selezione della lingua viene eseguita nel modo seguente: ogni thread ha un elenco associato di "lingue dell'interfaccia utente preferite", che è possibile ottenere chiamando [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages).</span><span class="sxs-lookup"><span data-stu-id="056d6-199">On Windows Vista, the language selection is done as follows: Each thread has an associated list of "preferred UI languages", which can be obtained by calling [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages).</span></span> <span data-ttu-id="056d6-200">L'elenco viene restituito in ordine di preferenza dell'utente.</span><span class="sxs-lookup"><span data-stu-id="056d6-200">The list is returned in order of user preference.</span></span> <span data-ttu-id="056d6-201">Ad esempio, in un sistema configurato per la lingua inglese (Stati Uniti), l'elenco restituito da **GetThreadPreferredUILanguages** è {"en-US", "en"}.</span><span class="sxs-lookup"><span data-stu-id="056d6-201">For instance, on a system set up for US English, the list returned by **GetThreadPreferredUILanguages** is { "en-US", "en" }.</span></span> <span data-ttu-id="056d6-202">Questo significa: 1) Inglese (Stati Uniti) se presente.</span><span class="sxs-lookup"><span data-stu-id="056d6-202">This means: 1) US English if present.</span></span> <span data-ttu-id="056d6-203">2) in caso contrario, utilizzare qualsiasi variante di lingua inglese, ad esempio "en-GB" o semplicemente "en".</span><span class="sxs-lookup"><span data-stu-id="056d6-203">2) Otherwise, use any regional variant of English, such as "en-GB" or just plain "en".</span></span>

<span data-ttu-id="056d6-204">Per ogni lingua nell'elenco, in ordine di elenco, il codice dell'interfaccia utente cerca un elemento WCS: text il cui attributo XML: lang è una corrispondenza esatta.</span><span class="sxs-lookup"><span data-stu-id="056d6-204">For each language in that list, in list order, the UI code looks for a wcs:Text element whose xml:lang attribute is an exact match.</span></span> <span data-ttu-id="056d6-205">Viene utilizzata la prima versione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="056d6-205">The first matching version is used.</span></span> <span data-ttu-id="056d6-206">Se nessuna versione corrisponde, viene usato il primo elemento WCS: Text.</span><span class="sxs-lookup"><span data-stu-id="056d6-206">If no version matches, the first wcs:Text element is used.</span></span>

### <a name="built-in-profiles"></a><span data-ttu-id="056d6-207">Profili predefiniti</span><span class="sxs-lookup"><span data-stu-id="056d6-207">Built-in profiles</span></span>

<span data-ttu-id="056d6-208">I profili WCS standard forniti con Windows Vista, ad esempio sRGB. CDMP, hanno le stesse proprietà localizzabili di altri profili.</span><span class="sxs-lookup"><span data-stu-id="056d6-208">The standard WCS profiles shipped with Windows Vista, such as sRGB.cdmp, have the same localizable properties as other profiles.</span></span>

<span data-ttu-id="056d6-209">La soluzione Windows standard consiste nell'inserire le stringhe localizzate in una DLL MUI e farvi riferimento come segue:</span><span class="sxs-lookup"><span data-stu-id="056d6-209">The standard Windows solution would be to put the localized strings in a MUI DLL, and refer to them like this:</span></span>


```XML
<cdm:Description resourceId="mscms.dll,-101">
    <wcs:Text xml:lang="en-US">Hello, world!</wcs:Text>
<cdm:Description>
```



<span data-ttu-id="056d6-210">In un sistema Windows, il testo della descrizione verrebbe estratto dall'ID risorsa 101 nella versione localizzata appropriata delle risorse MUI per mscms.dll.</span><span class="sxs-lookup"><span data-stu-id="056d6-210">On a Windows system, the description text would be extracted from resource ID 101 in the appropriate localized version of the MUI resources for mscms.dll.</span></span> <span data-ttu-id="056d6-211">I sistemi non Windows useranno i sottoelementi WCS: text come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="056d6-211">Non-Windows systems would use the wcs:Text sub-elements as described above.</span></span>

<span data-ttu-id="056d6-212">Viene introdotto un attributo ID univoco globale facoltativo sull'elemento radice di ogni schema del profilo WCS.</span><span class="sxs-lookup"><span data-stu-id="056d6-212">We introduce an optional, globally unique ID attribute on the root element of each WCS profile schema.</span></span> <span data-ttu-id="056d6-213">Il profilo standard wcsRGB. CDMP potrebbe essere simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="056d6-213">The standard profile wcsRGB.cdmp might look like this:</span></span>


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



<span data-ttu-id="056d6-214">Per i profili dei colori WCS forniti con Windows, il colore CPL Visualizza le informazioni descrittive dalle risorse anziché dagli elementi WCS: text nei profili.</span><span class="sxs-lookup"><span data-stu-id="056d6-214">For the WCS color profiles shipped with windows, the Color CPL displays descriptive information from the resources, rather than from the wcs:Text elements in the profiles.</span></span> <span data-ttu-id="056d6-215">In questo modo Windows può visualizzare le informazioni localizzate per questi profili in tutte le lingue supportate, senza richiedere che i profili themlselves contengano informazioni descrittive in tutte le lingue.</span><span class="sxs-lookup"><span data-stu-id="056d6-215">This allows Windows to display localized information for these profiles in all supported languages, without requiring the profiles themlselves to contain descriptive information in all languages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="056d6-216">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="056d6-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="056d6-217">Concetti di base sulla gestione dei colori</span><span class="sxs-lookup"><span data-stu-id="056d6-217">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="056d6-218">Schemi e algoritmi del sistema di colori Windows</span><span class="sxs-lookup"><span data-stu-id="056d6-218">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 