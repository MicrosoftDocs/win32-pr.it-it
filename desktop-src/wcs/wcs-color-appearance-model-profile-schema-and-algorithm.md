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
# <a name="wcs-color-appearance-model-profile-schema-and-algorithm"></a>Schema e algoritmo del profilo del modello di aspetto del colore WCS

[Overview](#overview)

[Architettura del profilo del modello di aspetto colore (CAMP)](#color-appearance-model-profile-architecture)

[Schema del campo](#the-camp-schema)

[Elementi dello schema del campo](#the-camp-schema-elements)

[Algoritmo di CAMP](#the-camp-algorithm)

### <a name="overview"></a>Panoramica

Questo schema viene usato per specificare il contenuto di un profilo del modello di aspetto colore (CAMP). Gli algoritmi di base associati sono descritti nelle sezioni seguenti.

Il campo è costituito da tag XML che forniscono valori parametrici alle variabili del modello di aspetto dei colori della linea di base CIECAM02. I dettagli sugli intervalli per i parametri sono disponibili nella specifica del modello di aspetto dei colori di base e nella raccomandazione CIECAM02.

### <a name="color-appearance-model-profile-architecture"></a>Architettura del profilo del modello aspetto colore

![Diagramma che illustra l'architettura del profilo dei campi costituita da tag X M.](images/camp-image002new.png)

### <a name="the-camp-schema"></a>Schema del campo


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



## <a name="the-camp-schema-elements"></a>Elementi dello schema del campo

## <a name="colorappearancemodel"></a>ColorAppearanceModel

Questo elemento è una sequenza di:

1.  Stringa ProfileName,
2.  stringa di descrizione facoltativa,
3.  stringa autore facoltativa,
4.  Elemento ViewingConditions.

**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo. Le lunghezze di stringa sono limitate a 10.000 caratteri.

## <a name="namespace"></a>Spazio dei nomi

xmlns: Cam = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

## <a name="version"></a>Versione

Versione &gt; 0,1 o &lt; = "1,0" con la prima versione di Windows Vista.

**Condizioni di convalida:** Qualsiasi valore di versione &lt; = 2,0 è valido anche per supportare le modifiche non di rilievo nel formato.

## <a name="documentation"></a>Documentazione

Schema del profilo del modello di aspetto colore.

Copyright (C) Microsoft. Tutti i diritti sono riservati.

**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.

## <a name="surroundtype"></a>SurroundType

Questo elemento è un'enumerazione dei parametri CIECAM02 "Average", "Dim" o "Dark" oppure i parametri quantitativi effettivi dalla raccomandazione CIECAM02 c, che determina l'effetto della Racchiudi.

**Condizioni di convalida:** Il parametro c può essere compreso tra 0,525 e 0,69.

## <a name="viewingconditions"></a>ViewingConditions

Questo elemento è costituito dai sottoelementi seguenti:



| Elemento                    | Tipo           |
|----------------------------|----------------|
| WhitePoint                 | WhitePointType |
| Sfondo                 | CIE XYZ         |
| Surround                   | SurroundType   |
| LuminanceOfAdaptingField   | float          |
| DegreeOfAdaptation         | float          |
| NormalizeToMediaWhitePoint | Boolean        |



 

**Condizioni di convalida:** Gli elementi secondari CIE XYZ vengono convalidati da NonNegativeXYZType. LuminanceOfAdaptingField è un massimo di 10, 000cd/m ^ 2. DegreeOfAdaptation può essere compreso tra 0,0 e 1,0. Il valore di NormalizeToMediaWhitePoint può essere "true" o "false". Se il sottoelemento NormalizeToMediaWhitePoint è assente, il valore predefinito è "true". Vedere la sezione algoritmo del campo seguente.

## <a name="whitepointtype"></a>WhitePointType

Questo elemento è un'enumerazione del valore di origine di luce CIE ("D50", "D65", "A" o "F2") o un sottoelemento CIE XYZ.

**Condizioni di convalida:** Ogni sottoelemento viene convalidato in base al relativo tipo.

## <a name="ciexyztype"></a>CIEXYZType

L'elemento CIEXYZType è costituito da tre elementi a virgola mobile IEEE a precisione singola NonNegativeFloatType, denominati "X", "Y" e "Z". Queste misurazioni possono essere di tipo assoluto (non relativo) CIE XYZ 1931 o assoluti (non relativi) CIE XYZ 1931 Direct (transmissal) in candele per metro unità quadrate.

**Condizioni di convalida:** Ciò significa che solo i valori reali sono validi e i valori di misurazione CIE XYZ negativi non sono validi. Poiché si tratta di valori assoluti, i valori possono avere un intervallo ben superiore a 1,0 f. Un limite ragionevole per qualsiasi valore X, Y o Z verrà impostato arbitrariamente su 10000.0 f.

 

### <a name="the-camp-algorithm"></a>Algoritmo di CAMP

Il modello di aspetto dei colori (camma) si basa sulle equazioni del modello di aspetto dei colori di CIECAM02 CIE.

Questa classe implementa la modellazione dell'aspetto dei colori. Si noti che la camma WCS *non* è sostituibile, ad esempio con un plug-in. Si tratta di un obiettivo di progettazione per avere un solo modello di aspetto colore. La camma è basata sulle raccomandazioni CIECAM02.

CIECAM02 può essere usato in due modi. Nella direzione da colorimetrico a aspetto, fornisce un mapping dallo spazio CIE XYZ allo spazio di aspetto dei colori. Nella direzione appearance-to-colorimetrico, viene eseguito il mapping dallo spazio di aspetto dei colori allo spazio XYZ. L'aspetto dei colori è correlato alla luminosità, J, Chroma, C e Hue, h. Questi tre valori formano un sistema di coordinate cilindrico. Spesso, risulta più facile lavorare in un sistema di coordinate rettangolare, quindi calcolare a = C cos h e b = C sin h, per dare CIECAM02 jab.

È possibile utilizzare i valori di luminosità della camma maggiori di 100. Il Comitato CIE che ha formulato CIECAM02 non ha indirizzato il comportamento dell'asse della luminosità per i valori di input con una luminanza maggiore del punto bianco adottato. ovvero per i valori Y di input maggiori del valore Y del punto bianco adottato. La sperimentazione ha dimostrato che le equazioni di luminanza in CIECAM02 si comportano ragionevolmente per tali valori. La luminosità aumenta in modo esponenziale e segue lo stesso esponente (approssimativamente 1/3).

A volte gli utenti desiderano modificare il modo in cui viene calcolato il grado di adattamento (D). La progettazione WCS consente agli utenti di controllare questo calcolo modificando il valore degreeOfadaptation nei parametri di visualizzazione delle condizioni.

Per garantire una corrispondenza più coerente con le aspettative influenze degli utenti, il degreeOfAdaptation nei campi predefiniti è 1,0. Ciò produce risultati migliori in tutti i casi diversi dall'assoluto tritato, in cui potrebbe essere necessario consentire a WCS di calcolare il degreeOfAdaptation (tramite degreeOfAdaptation =-1).

Invece di usare un valore surround pari a "Average", "Dim" e "Dark", viene fornito un valore surround continuo, calcolato dal valore c. Il valore di c deve essere un valore float compreso tra 0,525 e 0,69.

Da *c*, *NC* e *F* possono essere calcolati, usando l'interpolazione lineare a tratti tra i valori già specificati per "Average", "Dim" e "Dark". Questo modello è illustrato nella figura 1 di CIE 159:2004, la specifica CIECAM02.



| degreeOfAdaption                     | Comportamento                                                                       |
|--------------------------------------|--------------------------------------------------------------------------------|
| -1.0                                 | ![Mostra una formula per il comportamento predefinito C I E C A M 02.](images/camp-image006.png)Questo è il comportamento predefinito di CIECAM02.<br/> |
| 0,0 &lt; = degreeOfAdaption &lt; = 1,0 | *D* = degreeOfAdaptation (valore fornito dall'utente)                      |



 

All'implementazione è stata aggiunta anche una certa quantità di controllo degli errori. I numeri di equazione seguenti sono quelli usati nella definizione CIE 159:2004 di CIECAM02.

**ColorimetricToAppearanceColors**

I valori di input vengono controllati per verificarne la ragionevolezza: se X o Z &lt; 0,0 o Y &lt; -1,0, HRESULT è E \_ INVALIDARG. Se-1,0 &lt; = Y &lt; 0,0, J, C e h sono tutti impostati su 0,0.

Esistono determinate condizioni interne che possono produrre risultati di errore. Anziché produrre tali risultati, i risultati interni vengono ritagliati per produrre valori compresi nell'intervallo. Ciò si verifica per le specifiche dei colori che sarebbero scure e probabilmente cromatiche: nell'equazione 7,23, se è &lt; 0, a = 0. Nell'equazione 7,26, se t &lt; 0, t = 0.

**AppearanceToColorimetricColors**

Verifica della ragionevolezza dei valori di input. Se C &lt; 0, c &gt; 300 o J &gt; 500, HRESULT è E \_ INVALIDARG.

*R '<sub>a;</sub>*, *G '<sub>a;</sub>* e *B '<sub>a;</sub>*, (equazioni 8,19-8,21) vengono ritagliati nell'intervallo 399,9.

Per tutti i profili dei modelli di aspetto dei colori (Camp), il motore WCS esaminerà il punto bianco adottato. Se Y non è 100,0, il punto bianco adottato verrà ridimensionato in modo che Y sia uguale a 100,0. Lo stesso ridimensionamento verrà applicato al valore di sfondo. Il fattore di scala è 100.0/adoptedWhitePoint. Y. Lo stesso fattore di scala viene applicato a ogni X, Y e Z. Se il campo NormalizeToMediaWhitePoint è impostato su "true" o se è assente dal campo, il motore ridimensiona anche tutti i colori del dispositivo in input in DeviceToColorimetric, in modo che il valore Y del punto bianco del supporto del dispositivo sia uguale a 100,0. I colori del dispositivo provenienti da ColorimetricToDevice verranno ridimensionati in base all'inverso moltiplicativo del fattore di scala. Se il flag NormalizeToMediaWhitePoint è impostato su "false", i dati colorimetrico non vengono ridimensionati.

Per alcune attività è opportuno ridimensionare i valori colorimetrico provenienti da DeviceToColorimetric. Le equazioni di luminosità iperbolica nella camma sono progettate per la luminanza di un punto bianco di 100,0. L'unica posizione in cui entra in gioco una differenza nella luminanza assoluta (o nell'illuminazione) si trova nella luminosità del campo di adattamento. Quindi, la camma deve essere inizializzata con un punto bianco Y di 100,0. Tuttavia, se viene usato il punto bianco medio del modello di dispositivo come punto bianco adottato, tutti i colori provenienti dal dispositivo devono essere ridimensionati di conseguenza oppure il bianco del dispositivo non verrà distribuito con un valore J pari a 100,0. Pertanto, è necessario ridimensionare i valori Y nelle misurazioni. È possibile ridimensionare i valori di misurazione prima di inizializzare il modello di dispositivo. I risultati saranno già nell'intervallo appropriato. Tuttavia, ciò renderebbe più difficile il test del modello di dispositivo, perché i valori in uscita richiederebbero la scalabilità. Per le attività in cui il punto bianco medio del dispositivo viene percepito come un vero bianco, è auspicabile normalizzare il punto di supporto del dispositivo.

La camma viene inizializzata direttamente dal campo. Questo consente agli sviluppatori una certa flessibilità nell'inizializzazione della camma, in base all'attività che desidera eseguire. In alcune attività, gli osservatori ignoreranno qualsiasi Chroma nei puntini bianchi dei supporti, perché cognitivamente "sanno" che i supporti di origine e di destinazione sono "bianchi". In questi casi, gli sviluppatori vorranno inizializzare le camme in diretta e inversa con i rispettivi punti di supporto. In alcuni casi, gli osservatori possono confrontare il colore degli sfondi dei supporti. In questi casi, è consigliabile usare una camma per entrambi i dispositivi e potrebbe essere auspicabile non ridimensionare i valori colorimetrico di ogni dispositivo in base al punto bianco medio del dispositivo. Quindi, i diversi valori tristimolo del supporto determineranno valori di aspetto diversi in CIECAM02.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base sulla gestione dei colori](basic-color-management-concepts.md)
</dt> <dt>

[Schemi e algoritmi del sistema di colori Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





