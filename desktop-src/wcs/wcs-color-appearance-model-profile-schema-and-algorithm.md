---
title: Schema e algoritmo del profilo del modello di aspetto del colore WCS
description: Schema e algoritmo del profilo del modello di aspetto del colore WCS
ms.assetid: 017588fe-cec9-4178-a912-7950cefc036c
keywords:
- Sistema di colori Windows (WCS), profilo colore aspetto modello (CAMP)
- WCS (sistema di colori Windows), profilo colore aspetto modello (CAMP)
- Gestione colori immagine, profilo colore aspetto modello (CAMP)
- gestione dei colori, profilo del modello di aspetto colore (CAMP)
- colori, profilo del modello di aspetto colore (CAMP)
- Windows Color System (WCS), profili
- WCS (Windows Color System), profili
- Gestione colori immagine, profili
- gestione dei colori, profili
- colori, profili
- profilo del modello di aspetto colore (CAMP)
- CAMP (Profilo modello aspetto colore)
- schemi, profilo del modello di aspetto colore (CAMP)
- algoritmi, profilo del modello di aspetto colore (CAMP)
- Profilo modello aspetto colore WCS
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a928aebcfe02f1db39de2452a0b49e5c888bccc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "106320212"
---
# <a name="wcs-color-appearance-model-profile-schema-and-algorithm"></a><span data-ttu-id="26aec-118">Schema e algoritmo del profilo del modello di aspetto del colore WCS</span><span class="sxs-lookup"><span data-stu-id="26aec-118">WCS Color Appearance Model Profile Schema and Algorithm</span></span>

[<span data-ttu-id="26aec-119">Overview</span><span class="sxs-lookup"><span data-stu-id="26aec-119">Overview</span></span>](#overview)

[<span data-ttu-id="26aec-120">Architettura del profilo del modello di aspetto colore (CAMP)</span><span class="sxs-lookup"><span data-stu-id="26aec-120">Color Appearance Model Profile (CAMP) Architecture</span></span>](#color-appearance-model-profile-architecture)

[<span data-ttu-id="26aec-121">Schema del campo</span><span class="sxs-lookup"><span data-stu-id="26aec-121">The CAMP Schema</span></span>](#the-camp-schema)

[<span data-ttu-id="26aec-122">Elementi dello schema del campo</span><span class="sxs-lookup"><span data-stu-id="26aec-122">The CAMP Schema Elements</span></span>](#the-camp-schema-elements)

[<span data-ttu-id="26aec-123">Algoritmo di CAMP</span><span class="sxs-lookup"><span data-stu-id="26aec-123">The CAMP Algorithm</span></span>](#the-camp-algorithm)

### <a name="overview"></a><span data-ttu-id="26aec-124">Panoramica</span><span class="sxs-lookup"><span data-stu-id="26aec-124">Overview</span></span>

<span data-ttu-id="26aec-125">Questo schema viene usato per specificare il contenuto di un profilo del modello di aspetto colore (CAMP).</span><span class="sxs-lookup"><span data-stu-id="26aec-125">This schema is used to specify the content of a color appearance model profile (CAMP).</span></span> <span data-ttu-id="26aec-126">Gli algoritmi di base associati sono descritti nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="26aec-126">The associated baseline algorithms are described in the following sections.</span></span>

<span data-ttu-id="26aec-127">Il campo è costituito da tag XML che forniscono valori parametrici alle variabili del modello di aspetto dei colori della linea di base CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="26aec-127">The CAMP is composed of XML tags that provide parametric values to the CIECAM02 baseline color appearance model variables.</span></span> <span data-ttu-id="26aec-128">I dettagli sugli intervalli per i parametri sono disponibili nella specifica del modello di aspetto dei colori di base e nella raccomandazione CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="26aec-128">Details on the ranges for parameters are provided in the baseline color appearance model specification and CIECAM02 recommendation.</span></span>

### <a name="color-appearance-model-profile-architecture"></a><span data-ttu-id="26aec-129">Architettura del profilo del modello aspetto colore</span><span class="sxs-lookup"><span data-stu-id="26aec-129">Color Appearance Model Profile Architecture</span></span>

![Diagramma che illustra l'architettura del profilo dei campi costituita da tag X M.](images/camp-image002new.png)

### <a name="the-camp-schema"></a><span data-ttu-id="26aec-131">Schema del campo</span><span class="sxs-lookup"><span data-stu-id="26aec-131">The CAMP Schema</span></span>


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema
  xmlns:cam="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Appearance Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:annotation>
    <xs:documentation>
      ColorAppearanceModel element contains viewing conditions
      parameters based on CIECAM02.
    </xs:documentation>
  </xs:annotation>
  <xs:element name="ColorAppearanceModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="ViewingConditions">
          <xs:complexType>
            <xs:sequence>
              <xs:choice>
                <xs:element name="WhitePoint" type="wcs:NonNegativeCIEXYZType"/>
                <xs:element name="WhitePointName">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="D50"/>
                      <xs:enumeration value="D65"/>
                      <xs:enumeration value="A"/>
                      <xs:enumeration value="F2"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:element>
              </xs:choice>
              <xs:element name="Background" type="wcs:NonNegativeCIEXYZType"/>
              <xs:choice>
                <xs:element name="ImpactOfSurround" type="xs:float"/>
                <xs:element name="Surround">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="Average"/>
                      <xs:enumeration value="Dim"/>
                      <xs:enumeration value="Dark"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:element>
              </xs:choice>
              <xs:element name="LuminanceOfAdaptingField" type="xs:float"/>
              <xs:element name="DegreeOfAdaptation" type="xs:float"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
        <xs:element name="NormalizeToMediaWhitePoint" minOccurs="0">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="True"/>
              <xs:enumeration value="False"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>
```



## <a name="the-camp-schema-elements"></a><span data-ttu-id="26aec-132">Elementi dello schema del campo</span><span class="sxs-lookup"><span data-stu-id="26aec-132">The CAMP Schema Elements</span></span>

## <a name="colorappearancemodel"></a><span data-ttu-id="26aec-133">ColorAppearanceModel</span><span class="sxs-lookup"><span data-stu-id="26aec-133">ColorAppearanceModel</span></span>

<span data-ttu-id="26aec-134">Questo elemento è una sequenza di:</span><span class="sxs-lookup"><span data-stu-id="26aec-134">This element is a sequence of:</span></span>

1.  <span data-ttu-id="26aec-135">Stringa ProfileName,</span><span class="sxs-lookup"><span data-stu-id="26aec-135">ProfileName string,</span></span>
2.  <span data-ttu-id="26aec-136">stringa di descrizione facoltativa,</span><span class="sxs-lookup"><span data-stu-id="26aec-136">optional Description string,</span></span>
3.  <span data-ttu-id="26aec-137">stringa autore facoltativa,</span><span class="sxs-lookup"><span data-stu-id="26aec-137">optional Author string,</span></span>
4.  <span data-ttu-id="26aec-138">Elemento ViewingConditions.</span><span class="sxs-lookup"><span data-stu-id="26aec-138">ViewingConditions element.</span></span>

<span data-ttu-id="26aec-139">**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.</span><span class="sxs-lookup"><span data-stu-id="26aec-139">**Validation conditions:** Each sub-element is validated by its own type.</span></span> <span data-ttu-id="26aec-140">Le lunghezze di stringa sono limitate a 10.000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="26aec-140">String lengths are limited to 10,000 characters.</span></span>

## <a name="namespace"></a><span data-ttu-id="26aec-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="26aec-141">Namespace</span></span>

<span data-ttu-id="26aec-142">xmlns: Cam = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "</span><span class="sxs-lookup"><span data-stu-id="26aec-142">xmlns:cam="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"</span></span>

<span data-ttu-id="26aec-143">targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "</span><span class="sxs-lookup"><span data-stu-id="26aec-143">targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"</span></span>

## <a name="version"></a><span data-ttu-id="26aec-144">Versione</span><span class="sxs-lookup"><span data-stu-id="26aec-144">Version</span></span>

<span data-ttu-id="26aec-145">Versione &gt; 0,1 o &lt; = "1,0" con la prima versione di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="26aec-145">Version &gt;0.1 or &lt;= "1.0" with the first release of Windows Vista.</span></span>

<span data-ttu-id="26aec-146">**Condizioni di convalida:** Qualsiasi valore di versione &lt; = 2,0 è valido anche per supportare le modifiche non di rilievo nel formato.</span><span class="sxs-lookup"><span data-stu-id="26aec-146">**Validation conditions:** Any version value &lt;=2.0 is also valid to support non-breaking changes to the format.</span></span>

## <a name="documentation"></a><span data-ttu-id="26aec-147">Documentazione</span><span class="sxs-lookup"><span data-stu-id="26aec-147">Documentation</span></span>

<span data-ttu-id="26aec-148">Schema del profilo del modello di aspetto colore.</span><span class="sxs-lookup"><span data-stu-id="26aec-148">Color Appearance Model Profile Schema.</span></span>

<span data-ttu-id="26aec-149">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="26aec-149">Copyright (C) Microsoft.</span></span> <span data-ttu-id="26aec-150">Tutti i diritti sono riservati.</span><span class="sxs-lookup"><span data-stu-id="26aec-150">All rights reserved.</span></span>

<span data-ttu-id="26aec-151">**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.</span><span class="sxs-lookup"><span data-stu-id="26aec-151">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

## <a name="surroundtype"></a><span data-ttu-id="26aec-152">SurroundType</span><span class="sxs-lookup"><span data-stu-id="26aec-152">SurroundType</span></span>

<span data-ttu-id="26aec-153">Questo elemento è un'enumerazione dei parametri CIECAM02 "Average", "Dim" o "Dark" oppure i parametri quantitativi effettivi dalla raccomandazione CIECAM02 c, che determina l'effetto della Racchiudi.</span><span class="sxs-lookup"><span data-stu-id="26aec-153">This element is a either an enumeration of "Average," "Dim," or "Dark" CIECAM02 parameters or the actual quantitative parameters from the CIECAM02 recommendation c, impact of the surround.</span></span>

<span data-ttu-id="26aec-154">**Condizioni di convalida:** Il parametro c può essere compreso tra 0,525 e 0,69.</span><span class="sxs-lookup"><span data-stu-id="26aec-154">**Validation conditions:** The c parameter can range from 0.525 to 0.69.</span></span>

## <a name="viewingconditions"></a><span data-ttu-id="26aec-155">ViewingConditions</span><span class="sxs-lookup"><span data-stu-id="26aec-155">ViewingConditions</span></span>

<span data-ttu-id="26aec-156">Questo elemento è costituito dai sottoelementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="26aec-156">This element consists of the following sub-elements:</span></span>



| <span data-ttu-id="26aec-157">Elemento</span><span class="sxs-lookup"><span data-stu-id="26aec-157">Element</span></span>                    | <span data-ttu-id="26aec-158">Tipo</span><span class="sxs-lookup"><span data-stu-id="26aec-158">Type</span></span>           |
|----------------------------|----------------|
| <span data-ttu-id="26aec-159">WhitePoint</span><span class="sxs-lookup"><span data-stu-id="26aec-159">WhitePoint</span></span>                 | <span data-ttu-id="26aec-160">WhitePointType</span><span class="sxs-lookup"><span data-stu-id="26aec-160">WhitePointType</span></span> |
| <span data-ttu-id="26aec-161">Sfondo</span><span class="sxs-lookup"><span data-stu-id="26aec-161">Background</span></span>                 | <span data-ttu-id="26aec-162">CIE XYZ</span><span class="sxs-lookup"><span data-stu-id="26aec-162">CIEXYZ</span></span>         |
| <span data-ttu-id="26aec-163">Surround</span><span class="sxs-lookup"><span data-stu-id="26aec-163">Surround</span></span>                   | <span data-ttu-id="26aec-164">SurroundType</span><span class="sxs-lookup"><span data-stu-id="26aec-164">SurroundType</span></span>   |
| <span data-ttu-id="26aec-165">LuminanceOfAdaptingField</span><span class="sxs-lookup"><span data-stu-id="26aec-165">LuminanceOfAdaptingField</span></span>   | <span data-ttu-id="26aec-166">float</span><span class="sxs-lookup"><span data-stu-id="26aec-166">float</span></span>          |
| <span data-ttu-id="26aec-167">DegreeOfAdaptation</span><span class="sxs-lookup"><span data-stu-id="26aec-167">DegreeOfAdaptation</span></span>         | <span data-ttu-id="26aec-168">float</span><span class="sxs-lookup"><span data-stu-id="26aec-168">float</span></span>          |
| <span data-ttu-id="26aec-169">NormalizeToMediaWhitePoint</span><span class="sxs-lookup"><span data-stu-id="26aec-169">NormalizeToMediaWhitePoint</span></span> | <span data-ttu-id="26aec-170">Boolean</span><span class="sxs-lookup"><span data-stu-id="26aec-170">Boolean</span></span>        |



 

<span data-ttu-id="26aec-171">**Condizioni di convalida:** Gli elementi secondari CIE XYZ vengono convalidati da NonNegativeXYZType.</span><span class="sxs-lookup"><span data-stu-id="26aec-171">**Validation conditions:** CIEXYZ sub-elements are validated by NonNegativeXYZType.</span></span> <span data-ttu-id="26aec-172">LuminanceOfAdaptingField è un massimo di 10, 000cd/m ^ 2.</span><span class="sxs-lookup"><span data-stu-id="26aec-172">The LuminanceOfAdaptingField is a maximum of 10,000cd/m^2.</span></span> <span data-ttu-id="26aec-173">DegreeOfAdaptation può essere compreso tra 0,0 e 1,0.</span><span class="sxs-lookup"><span data-stu-id="26aec-173">The DegreeOfAdaptation can range from 0.0 to 1.0.</span></span> <span data-ttu-id="26aec-174">Il valore di NormalizeToMediaWhitePoint può essere "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="26aec-174">The NormalizeToMediaWhitePoint value can be either "true" or "false."</span></span> <span data-ttu-id="26aec-175">Se il sottoelemento NormalizeToMediaWhitePoint è assente, il valore predefinito è "true".</span><span class="sxs-lookup"><span data-stu-id="26aec-175">If the NormalizeToMediaWhitePoint sub-element is absent, it effectively defaults to "true."</span></span> <span data-ttu-id="26aec-176">Vedere la sezione algoritmo del campo seguente.</span><span class="sxs-lookup"><span data-stu-id="26aec-176">See the following CAMP algorithm section.</span></span>

## <a name="whitepointtype"></a><span data-ttu-id="26aec-177">WhitePointType</span><span class="sxs-lookup"><span data-stu-id="26aec-177">WhitePointType</span></span>

<span data-ttu-id="26aec-178">Questo elemento è un'enumerazione del valore di origine di luce CIE ("D50", "D65", "A" o "F2") o un sottoelemento CIE XYZ.</span><span class="sxs-lookup"><span data-stu-id="26aec-178">This element is a either an enumeration of CIE light source value ("D50," "D65," "A," or "F2") or a CIEXYZ sub-element.</span></span>

<span data-ttu-id="26aec-179">**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.</span><span class="sxs-lookup"><span data-stu-id="26aec-179">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

## <a name="ciexyztype"></a><span data-ttu-id="26aec-180">CIEXYZType</span><span class="sxs-lookup"><span data-stu-id="26aec-180">CIEXYZType</span></span>

<span data-ttu-id="26aec-181">L'elemento CIEXYZType è costituito da tre elementi a virgola mobile IEEE a precisione singola NonNegativeFloatType, denominati "X", "Y" e "Z".</span><span class="sxs-lookup"><span data-stu-id="26aec-181">The CIEXYZType element is composed of three NonNegativeFloatType single-precision IEEE floating-point elements, named "X," "Y," and "Z."</span></span> <span data-ttu-id="26aec-182">Queste misurazioni possono essere di tipo assoluto (non relativo) CIE XYZ 1931 o assoluti (non relativi) CIE XYZ 1931 Direct (transmissal) in candele per metro unità quadrate.</span><span class="sxs-lookup"><span data-stu-id="26aec-182">These measurements can be either absolute (not relative) CIEXYZ 1931 reflective values or absolute (not relative) CIEXYZ 1931 direct (transmissive) values in candelas per meter squared units.</span></span>

<span data-ttu-id="26aec-183">**Condizioni di convalida:** Ciò significa che solo i valori reali sono validi e i valori di misurazione CIE XYZ negativi non sono validi.</span><span class="sxs-lookup"><span data-stu-id="26aec-183">**Validation conditions:** This means that only real-world values are valid, and negative CIEXYZ measurement values are invalid.</span></span> <span data-ttu-id="26aec-184">Poiché si tratta di valori assoluti, i valori possono avere un intervallo ben superiore a 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="26aec-184">Since these are absolute values, values can range well beyond 1.0f.</span></span> <span data-ttu-id="26aec-185">Un limite ragionevole per qualsiasi valore X, Y o Z verrà impostato arbitrariamente su 10000.0 f.</span><span class="sxs-lookup"><span data-stu-id="26aec-185">A reasonable limit for any X, Y, or Z value will be arbitrarily set to 10000.0f.</span></span>

 

### <a name="the-camp-algorithm"></a><span data-ttu-id="26aec-186">Algoritmo di CAMP</span><span class="sxs-lookup"><span data-stu-id="26aec-186">The CAMP Algorithm</span></span>

<span data-ttu-id="26aec-187">Il modello di aspetto dei colori (camma) si basa sulle equazioni del modello di aspetto dei colori di CIECAM02 CIE.</span><span class="sxs-lookup"><span data-stu-id="26aec-187">The color appearance model (CAM) is based on the CIE CIECAM02 color appearance model equations.</span></span>

<span data-ttu-id="26aec-188">Questa classe implementa la modellazione dell'aspetto dei colori.</span><span class="sxs-lookup"><span data-stu-id="26aec-188">This class implements the color appearance modeling.</span></span> <span data-ttu-id="26aec-189">Si noti che la camma WCS *non* è sostituibile, ad esempio con un plug-in.</span><span class="sxs-lookup"><span data-stu-id="26aec-189">Note that the WCS CAM is *not* replaceable, for example, using a plug-in.</span></span> <span data-ttu-id="26aec-190">Si tratta di un obiettivo di progettazione per avere un solo modello di aspetto colore.</span><span class="sxs-lookup"><span data-stu-id="26aec-190">It is a design goal to have only one color appearance model.</span></span> <span data-ttu-id="26aec-191">La camma è basata sulle raccomandazioni CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="26aec-191">The CAM is based on CIECAM02 recommendations.</span></span>

<span data-ttu-id="26aec-192">CIECAM02 può essere usato in due modi.</span><span class="sxs-lookup"><span data-stu-id="26aec-192">CIECAM02 can be used in two ways.</span></span> <span data-ttu-id="26aec-193">Nella direzione da colorimetrico a aspetto, fornisce un mapping dallo spazio CIE XYZ allo spazio di aspetto dei colori.</span><span class="sxs-lookup"><span data-stu-id="26aec-193">In the colorimetric-to-appearance direction, it provides a mapping from CIE XYZ space to color appearance space.</span></span> <span data-ttu-id="26aec-194">Nella direzione appearance-to-colorimetrico, viene eseguito il mapping dallo spazio di aspetto dei colori allo spazio XYZ.</span><span class="sxs-lookup"><span data-stu-id="26aec-194">In the appearance-to-colorimetric direction, it maps from color appearance space back to XYZ space.</span></span> <span data-ttu-id="26aec-195">L'aspetto dei colori è correlato alla luminosità, J, Chroma, C e Hue, h.</span><span class="sxs-lookup"><span data-stu-id="26aec-195">The color appearance correlates lightness, J, chroma, C, and hue, h.</span></span> <span data-ttu-id="26aec-196">Questi tre valori formano un sistema di coordinate cilindrico.</span><span class="sxs-lookup"><span data-stu-id="26aec-196">These three values form a cylindrical coordinate system.</span></span> <span data-ttu-id="26aec-197">Spesso, risulta più facile lavorare in un sistema di coordinate rettangolare, quindi calcolare a = C cos h e b = C sin h, per dare CIECAM02 jab.</span><span class="sxs-lookup"><span data-stu-id="26aec-197">Frequently, it turns out to be more convenient to work in a rectangular coordinate system, so compute a = C cos h and b = C sin h, to give CIECAM02 Jab.</span></span>

<span data-ttu-id="26aec-198">È possibile utilizzare i valori di luminosità della camma maggiori di 100.</span><span class="sxs-lookup"><span data-stu-id="26aec-198">You can use CAM lightness values greater than 100.</span></span> <span data-ttu-id="26aec-199">Il Comitato CIE che ha formulato CIECAM02 non ha indirizzato il comportamento dell'asse della luminosità per i valori di input con una luminanza maggiore del punto bianco adottato. ovvero per i valori Y di input maggiori del valore Y del punto bianco adottato.</span><span class="sxs-lookup"><span data-stu-id="26aec-199">The CIE committee that formulated CIECAM02 did not address the behavior of the lightness axis for input values with a luminance greater than the adopted white point; that is, for input Y values greater than the adopted white point Y value.</span></span> <span data-ttu-id="26aec-200">La sperimentazione ha dimostrato che le equazioni di luminanza in CIECAM02 si comportano ragionevolmente per tali valori.</span><span class="sxs-lookup"><span data-stu-id="26aec-200">Experimentation has shown that the luminance equations in CIECAM02 behave reasonably for such values.</span></span> <span data-ttu-id="26aec-201">La luminosità aumenta in modo esponenziale e segue lo stesso esponente (approssimativamente 1/3).</span><span class="sxs-lookup"><span data-stu-id="26aec-201">The lightness increases exponentially and follows the same exponent (roughly 1/3).</span></span>

<span data-ttu-id="26aec-202">A volte gli utenti desiderano modificare il modo in cui viene calcolato il grado di adattamento (D).</span><span class="sxs-lookup"><span data-stu-id="26aec-202">Users sometimes want to change the way that the degree of adaptation (D) is calculated.</span></span> <span data-ttu-id="26aec-203">La progettazione WCS consente agli utenti di controllare questo calcolo modificando il valore degreeOfadaptation nei parametri di visualizzazione delle condizioni.</span><span class="sxs-lookup"><span data-stu-id="26aec-203">The WCS design enables users to control this calculation by changing the degreeOfadaptation value in the viewing conditions parameters.</span></span>

<span data-ttu-id="26aec-204">Per garantire una corrispondenza più coerente con le aspettative influenze degli utenti, il degreeOfAdaptation nei campi predefiniti è 1,0.</span><span class="sxs-lookup"><span data-stu-id="26aec-204">To provide a more consistent match to users' ICC-influenced expectations, the degreeOfAdaptation in the default CAMPS is 1.0.</span></span> <span data-ttu-id="26aec-205">Ciò produce risultati migliori in tutti i casi diversi dall'assoluto tritato, in cui potrebbe essere necessario consentire a WCS di calcolare il degreeOfAdaptation (tramite degreeOfAdaptation =-1).</span><span class="sxs-lookup"><span data-stu-id="26aec-205">This produces better results in all cases other than MinCD Absolute, where one might want to let WCS compute the degreeOfAdaptation (via degreeOfAdaptation = -1).</span></span>

<span data-ttu-id="26aec-206">Invece di usare un valore surround pari a "Average", "Dim" e "Dark", viene fornito un valore surround continuo, calcolato dal valore c.</span><span class="sxs-lookup"><span data-stu-id="26aec-206">Instead of using a surround value of "Average," "Dim," and "Dark," a continuous surround value, computed from the value c, is provided.</span></span> <span data-ttu-id="26aec-207">Il valore di c deve essere un valore float compreso tra 0,525 e 0,69.</span><span class="sxs-lookup"><span data-stu-id="26aec-207">The value of c must be a float between 0.525 and 0.69.</span></span>

<span data-ttu-id="26aec-208">Da *c*, *NC* e *F* possono essere calcolati, usando l'interpolazione lineare a tratti tra i valori già specificati per "Average", "Dim" e "Dark".</span><span class="sxs-lookup"><span data-stu-id="26aec-208">From *c*, *Nc* and *F* can be computed, using piecewise linear interpolation between the values already provided for "Average," "Dim," and "Dark."</span></span> <span data-ttu-id="26aec-209">Questo modello è illustrato nella figura 1 di CIE 159:2004, la specifica CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="26aec-209">This models what is shown in Figure 1 of CIE 159:2004, the CIECAM02 specification.</span></span>



| <span data-ttu-id="26aec-210">degreeOfAdaption</span><span class="sxs-lookup"><span data-stu-id="26aec-210">degreeOfAdaption</span></span>                     | <span data-ttu-id="26aec-211">Comportamento</span><span class="sxs-lookup"><span data-stu-id="26aec-211">Behavior</span></span>                                                                       |
|--------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="26aec-212">-1.0</span><span class="sxs-lookup"><span data-stu-id="26aec-212">-1.0</span></span>                                 | ![Mostra una formula per il comportamento predefinito C I E C A M 02.](images/camp-image006.png)<span data-ttu-id="26aec-214">Questo è il comportamento predefinito di CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="26aec-214">This is the default CIECAM02 behavior.</span></span><br/> |
| <span data-ttu-id="26aec-215">0,0 &lt; = degreeOfAdaption &lt; = 1,0</span><span class="sxs-lookup"><span data-stu-id="26aec-215">0.0 &lt;= degreeOfAdaption &lt;= 1.0</span></span> | <span data-ttu-id="26aec-216">*D* = degreeOfAdaptation (valore fornito dall'utente)</span><span class="sxs-lookup"><span data-stu-id="26aec-216">*D* = degreeOfAdaptation (the value supplied by the user)</span></span>                      |



 

<span data-ttu-id="26aec-217">All'implementazione è stata aggiunta anche una certa quantità di controllo degli errori.</span><span class="sxs-lookup"><span data-stu-id="26aec-217">A certain amount of error checking has also been added to the implementation.</span></span> <span data-ttu-id="26aec-218">I numeri di equazione seguenti sono quelli usati nella definizione CIE 159:2004 di CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="26aec-218">The following equation numbers are those used in the CIE 159:2004 definition of CIECAM02.</span></span>

<span data-ttu-id="26aec-219">**ColorimetricToAppearanceColors**</span><span class="sxs-lookup"><span data-stu-id="26aec-219">**ColorimetricToAppearanceColors**</span></span>

<span data-ttu-id="26aec-220">I valori di input vengono controllati per verificarne la ragionevolezza: se X o Z &lt; 0,0 o Y &lt; -1,0, HRESULT è E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="26aec-220">The input values are checked for reasonableness: If X or Z &lt; 0.0, or if Y &lt; -1.0, then the HRESULT is E\_INVALIDARG.</span></span> <span data-ttu-id="26aec-221">Se-1,0 &lt; = Y &lt; 0,0, J, C e h sono tutti impostati su 0,0.</span><span class="sxs-lookup"><span data-stu-id="26aec-221">If -1.0 &lt;= Y &lt; 0.0, then J, C, and h are all set to 0.0.</span></span>

<span data-ttu-id="26aec-222">Esistono determinate condizioni interne che possono produrre risultati di errore.</span><span class="sxs-lookup"><span data-stu-id="26aec-222">There are certain internal conditions that can produce error results.</span></span> <span data-ttu-id="26aec-223">Anziché produrre tali risultati, i risultati interni vengono ritagliati per produrre valori compresi nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="26aec-223">Instead of producing such results, the internal results are clipped to produce in-range values.</span></span> <span data-ttu-id="26aec-224">Ciò si verifica per le specifiche dei colori che sarebbero scure e probabilmente cromatiche: nell'equazione 7,23, se è &lt; 0, a = 0.</span><span class="sxs-lookup"><span data-stu-id="26aec-224">This happens for specifications of colors that would be dark and impossibly chromatic: In equation 7.23, if A &lt; 0, A = 0.</span></span> <span data-ttu-id="26aec-225">Nell'equazione 7,26, se t &lt; 0, t = 0.</span><span class="sxs-lookup"><span data-stu-id="26aec-225">In equation 7.26, if t &lt; 0, t = 0.</span></span>

<span data-ttu-id="26aec-226">**AppearanceToColorimetricColors**</span><span class="sxs-lookup"><span data-stu-id="26aec-226">**AppearanceToColorimetricColors**</span></span>

<span data-ttu-id="26aec-227">Verifica della ragionevolezza dei valori di input.</span><span class="sxs-lookup"><span data-stu-id="26aec-227">The input values are checked for reasonableness.</span></span> <span data-ttu-id="26aec-228">Se C &lt; 0, c &gt; 300 o J &gt; 500, HRESULT è E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="26aec-228">If C &lt; 0 , C &gt; 300, or J &gt; 500, then the HRESULT is E\_INVALIDARG.</span></span>

<span data-ttu-id="26aec-229">*R '<sub>a;</sub>*, *G '<sub>a;</sub>* e *B '<sub>a;</sub>*, (equazioni 8,19-8,21) vengono ritagliati nell'intervallo 399,9.</span><span class="sxs-lookup"><span data-stu-id="26aec-229">*R'<sub>a;</sub>*, *G'<sub>a;</sub>*, and *B'<sub>a;</sub>*, (equations 8.19 - 8.21) are clipped to the range   399.9 .</span></span>

<span data-ttu-id="26aec-230">Per tutti i profili dei modelli di aspetto dei colori (Camp), il motore WCS esaminerà il punto bianco adottato.</span><span class="sxs-lookup"><span data-stu-id="26aec-230">For all Color Appearance Model Profiles (CAMPs), the WCS engine will examine the adopted white point.</span></span> <span data-ttu-id="26aec-231">Se Y non è 100,0, il punto bianco adottato verrà ridimensionato in modo che Y sia uguale a 100,0.</span><span class="sxs-lookup"><span data-stu-id="26aec-231">If Y is not 100.0, then the adopted white point will be scaled so that Y does equal 100.0.</span></span> <span data-ttu-id="26aec-232">Lo stesso ridimensionamento verrà applicato al valore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="26aec-232">The same scaling will be applied to the background value.</span></span> <span data-ttu-id="26aec-233">Il fattore di scala è 100.0/adoptedWhitePoint. Y.</span><span class="sxs-lookup"><span data-stu-id="26aec-233">The scaling factor is 100.0/adoptedWhitePoint.Y.</span></span> <span data-ttu-id="26aec-234">Lo stesso fattore di scala viene applicato a ogni X, Y e Z. Se il campo NormalizeToMediaWhitePoint è impostato su "true" o se è assente dal campo, il motore ridimensiona anche tutti i colori del dispositivo in input in DeviceToColorimetric, in modo che il valore Y del punto bianco del supporto del dispositivo sia uguale a 100,0.</span><span class="sxs-lookup"><span data-stu-id="26aec-234">The same scaling factor is applied to each of X, Y, and Z. If the NormalizeToMediaWhitePoint field is set to "True," or if it is absent from the CAMP, the engine also scales all device colors input to DeviceToColorimetric so that the Y value of the device media white point equals 100.0.</span></span> <span data-ttu-id="26aec-235">I colori del dispositivo provenienti da ColorimetricToDevice verranno ridimensionati in base all'inverso moltiplicativo del fattore di scala.</span><span class="sxs-lookup"><span data-stu-id="26aec-235">Device colors coming from ColorimetricToDevice will be scaled by the multiplicative inverse of that scaling factor.</span></span> <span data-ttu-id="26aec-236">Se il flag NormalizeToMediaWhitePoint è impostato su "false", i dati colorimetrico non vengono ridimensionati.</span><span class="sxs-lookup"><span data-stu-id="26aec-236">If the NormalizeToMediaWhitePoint flag is set to "False," then the colorimetric data is not scaled.</span></span>

<span data-ttu-id="26aec-237">Per alcune attività è opportuno ridimensionare i valori colorimetrico provenienti da DeviceToColorimetric.</span><span class="sxs-lookup"><span data-stu-id="26aec-237">For some tasks, it makes sense to scale the colorimetric values coming from DeviceToColorimetric.</span></span> <span data-ttu-id="26aec-238">Le equazioni di luminosità iperbolica nella camma sono progettate per la luminanza di un punto bianco di 100,0.</span><span class="sxs-lookup"><span data-stu-id="26aec-238">The hyperbolic lightness equations in the CAM are really designed for a white point luminance of 100.0.</span></span> <span data-ttu-id="26aec-239">L'unica posizione in cui entra in gioco una differenza nella luminanza assoluta (o nell'illuminazione) si trova nella luminosità del campo di adattamento.</span><span class="sxs-lookup"><span data-stu-id="26aec-239">The only place where a difference in the absolute luminance (or illuminance) comes into play is in the luminance of the adapting field.</span></span> <span data-ttu-id="26aec-240">Quindi, la camma deve essere inizializzata con un punto bianco Y di 100,0.</span><span class="sxs-lookup"><span data-stu-id="26aec-240">So the CAM must be initialized with a white point Y of 100.0.</span></span> <span data-ttu-id="26aec-241">Tuttavia, se viene usato il punto bianco medio del modello di dispositivo come punto bianco adottato, tutti i colori provenienti dal dispositivo devono essere ridimensionati di conseguenza oppure il bianco del dispositivo non verrà distribuito con un valore J pari a 100,0.</span><span class="sxs-lookup"><span data-stu-id="26aec-241">But if the device model's medium white point is being used as the adopted white point, then all colors coming from the device must be scaled accordingly, or device white will not come out with a J value of 100.0.</span></span> <span data-ttu-id="26aec-242">Pertanto, è necessario ridimensionare i valori Y nelle misurazioni.</span><span class="sxs-lookup"><span data-stu-id="26aec-242">So the Y values have to be scaled in the measurements.</span></span> <span data-ttu-id="26aec-243">È possibile ridimensionare i valori di misurazione prima di inizializzare il modello di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="26aec-243">The measurement values could be scaled before initializing the device model.</span></span> <span data-ttu-id="26aec-244">I risultati saranno già nell'intervallo appropriato.</span><span class="sxs-lookup"><span data-stu-id="26aec-244">Then results would already be in the proper range.</span></span> <span data-ttu-id="26aec-245">Tuttavia, ciò renderebbe più difficile il test del modello di dispositivo, perché i valori in uscita richiederebbero la scalabilità.</span><span class="sxs-lookup"><span data-stu-id="26aec-245">But that would make testing the device model more difficult, because the values coming out would require scaling.</span></span> <span data-ttu-id="26aec-246">Per le attività in cui il punto bianco medio del dispositivo viene percepito come un vero bianco, è auspicabile normalizzare il punto di supporto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="26aec-246">For tasks in which the device medium white point is perceived to be a true white, normalizing by the device media white point is desirable.</span></span>

<span data-ttu-id="26aec-247">La camma viene inizializzata direttamente dal campo.</span><span class="sxs-lookup"><span data-stu-id="26aec-247">The CAM is initialized directly from the CAMP.</span></span> <span data-ttu-id="26aec-248">Questo consente agli sviluppatori una certa flessibilità nell'inizializzazione della camma, in base all'attività che desidera eseguire.</span><span class="sxs-lookup"><span data-stu-id="26aec-248">This allows developers some flexibility in initializing the CAM, based upon the task they want to perform.</span></span> <span data-ttu-id="26aec-249">In alcune attività, gli osservatori ignoreranno qualsiasi Chroma nei puntini bianchi dei supporti, perché cognitivamente "sanno" che i supporti di origine e di destinazione sono "bianchi".</span><span class="sxs-lookup"><span data-stu-id="26aec-249">In some tasks, observers will ignore any chroma in the media white points, because they cognitively "know" that the source and destination media are "white."</span></span> <span data-ttu-id="26aec-250">In questi casi, gli sviluppatori vorranno inizializzare le camme in diretta e inversa con i rispettivi punti di supporto.</span><span class="sxs-lookup"><span data-stu-id="26aec-250">In such cases, developers will want to initialize the forward and inverse CAMs with their respective media white points.</span></span> <span data-ttu-id="26aec-251">In alcuni casi, gli osservatori possono confrontare il colore degli sfondi dei supporti.</span><span class="sxs-lookup"><span data-stu-id="26aec-251">In some cases, observers may be comparing the color of the media backgrounds.</span></span> <span data-ttu-id="26aec-252">In questi casi, è consigliabile usare una camma per entrambi i dispositivi e potrebbe essere auspicabile non ridimensionare i valori colorimetrico di ogni dispositivo in base al punto bianco medio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="26aec-252">In these cases, it is advisable to use one CAM for both devices, and it may be desirable not to scale each device's colorimetric values by that device's medium white point.</span></span> <span data-ttu-id="26aec-253">Quindi, i diversi valori tristimolo del supporto determineranno valori di aspetto diversi in CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="26aec-253">Then the different tristimulus values of the media will lead to different appearance values in CIECAM02.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26aec-254">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26aec-254">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26aec-255">Concetti di base sulla gestione dei colori</span><span class="sxs-lookup"><span data-stu-id="26aec-255">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="26aec-256">Schemi e algoritmi del sistema di colori Windows</span><span class="sxs-lookup"><span data-stu-id="26aec-256">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





