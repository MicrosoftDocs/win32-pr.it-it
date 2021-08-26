---
title: Schema e algoritmo del profilo del modello WCS Color Appearance
description: Schema e algoritmo del profilo del modello WCS Color Appearance
ms.assetid: 017588fe-cec9-4178-a912-7950cefc036c
keywords:
- Windows Sistema colori (WCS), profilo del modello di aspetto dei colori (CAMP)
- WCS (Windows Color System), profilo del modello di aspetto dei colori (CAMP)
- gestione del colore delle immagini, profilo del modello di aspetto del colore (CAMP)
- gestione dei colori, profilo del modello di aspetto dei colori (CAMP)
- colors,color appearance model profile (CAMP)
- Windows Sistema colori (WCS), profili
- WCS (Windows Color System), profili
- gestione dei colori delle immagini, profili
- gestione dei colori, profili
- colori, profili
- Profilo del modello di aspetto dei colori (CAMP)
- CAMP (profilo del modello con aspetto a colori)
- schemi, profilo del modello di aspetto dei colori (CAMP)
- algoritmi, profilo del modello di aspetto del colore (CAMP)
- Profilo del modello di aspetto del colore WCS
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042cf74d264a7b5d40fdc30fec44784680a67b95363b579d0c7bebc7ececcedb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090101"
---
# <a name="wcs-color-appearance-model-profile-schema-and-algorithm"></a>Schema e algoritmo del profilo del modello WCS Color Appearance

[Overview](#overview)

[Architettura del profilo del modello di aspetto del colore (CAMP)](#color-appearance-model-profile-architecture)

[Schema DI CAMPI](#the-camp-schema)

[Elementi dello schema CAMP](#the-camp-schema-elements)

[Algoritmo CAMP](#the-camp-algorithm)

### <a name="overview"></a>Panoramica

Questo schema viene usato per specificare il contenuto di un profilo del modello di aspetto a colori (CAMP). Gli algoritmi di base associati sono descritti nelle sezioni seguenti.

L'elemento CAMP è costituito da tag XML che forniscono valori parametrici alle variabili del modello per l'aspetto dei colori della linea di base DIM02. I dettagli sugli intervalli per i parametri sono disponibili nella specifica del modello di aspetto del colore di base e nella raccomandazione DIM02.

### <a name="color-appearance-model-profile-architecture"></a>Architettura del profilo del modello di aspetto colore

![Diagramma che illustra l'architettura del profilo CAMP in base ai tag X M L.](images/camp-image002new.png)

### <a name="the-camp-schema"></a>Schema DI CAMPI


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



## <a name="the-camp-schema-elements"></a>Elementi dello schema CAMP

## <a name="colorappearancemodel"></a>ColorAppearanceModel

Questo elemento è una sequenza di:

1.  Stringa ProfileName,
2.  stringa di descrizione facoltativa,
3.  stringa di creazione facoltativa,
4.  Elemento ViewingConditions.

**Condizioni di convalida:** Ogni sotto-elemento viene convalidato in base al proprio tipo. La lunghezza delle stringhe è limitata a 10.000 caratteri.

## <a name="namespace"></a>Spazio dei nomi

xmlns:cam=" http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

targetNamespace=" http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

## <a name="version"></a>Versione

Versione &gt; 0.1 o &lt; = "1.0" con la prima versione di Windows Vista.

**Condizioni di convalida:** Qualsiasi valore di versione =2.0 è valido anche per &lt; supportare modifiche non di rilievo al formato.

## <a name="documentation"></a>Documentazione

Schema del profilo del modello di aspetto colore.

Copyright (C) Microsoft. Tutti i diritti sono riservati.

**Condizioni di convalida:** Ogni sotto-elemento viene convalidato in base al proprio tipo.

## <a name="surroundtype"></a>SurroundType

Questo elemento è un'enumerazione di parametri "Average", "Dim" o "Dark" CIECAM02 o i parametri quantitativi effettivi della raccomandazione DIM02 c, impatto del surround.

**Condizioni di convalida:** Il parametro c può essere compreso tra 0,525 e 0,69.

## <a name="viewingconditions"></a>Visualizzazione di condizioni

Questo elemento è costituito dai sotto-elementi seguenti:



| Elemento                    | Tipo           |
|----------------------------|----------------|
| WhitePoint                 | WhitePointType |
| Sfondo                 | CIEXYZ         |
| Surround                   | SurroundType   |
| LuminanceOfAdaptingField   | float          |
| DegreeOfAdaptation         | float          |
| NormalizeToMediaWhitePoint | Boolean        |



 

**Condizioni di convalida:** Gli elementi secondari CIEXYZ vengono convalidati da NonNegativeXYZType. LuminanceOfAdaptingField è un massimo di 10.000cd/m^2. DegreeOfAdaptation può essere compreso tra 0,0 e 1,0. Il valore NormalizeToMediaWhitePoint può essere "true" o "false". Se il sotto-elemento NormalizeToMediaWhitePoint è assente, il valore predefinito è "true". Vedere la sezione seguente relativa all'algoritmo CAMP.

## <a name="whitepointtype"></a>WhitePointType

Questo elemento è un'enumerazione di valori di origine luce CIE ("D50", "D65", "A" o "F2") o un sotto-elemento CIEXYZ.

**Condizioni di convalida:** Ogni sotto-elemento viene convalidato in base al proprio tipo.

## <a name="ciexyztype"></a>CIEXYZType

L'elemento CIEXYZType è costituito da tre elementi A virgola mobile IEEE a precisione singola NonNegativeFloatType, denominati "X", "Y" e "Z". Queste misurazioni possono essere valori assoluti (non relativi) CIEXYZ 1931 riflettenti o valori assoluti (non relativi) CIEXYZ 1931 diretti (trasmissivi) in candela per unità quadrate del contatore.

**Condizioni di convalida:** Ciò significa che sono validi solo i valori reali e i valori di misura CIEXYZ negativi non sono validi. Poiché si tratta di valori assoluti, i valori possono essere ben oltre 1,0f. Un limite ragionevole per qualsiasi valore X, Y o Z verrà impostato arbitrariamente su 10000,0f.

 

### <a name="the-camp-algorithm"></a>Algoritmo CAMP

Il modello DIM (Color Appearance Model) è basato sulle equazioni del modello CIE EMEM02.

Questa classe implementa la modellazione dell'aspetto dei colori. Si noti che WCS CAM non *è* sostituibile, ad esempio usando un plug-in. È un obiettivo di progettazione avere un solo modello di aspetto a colori. La CAM è basata su raccomandazioni DIM02.

SIDM02 può essere usato in due modi. Nella direzione colorimetrica-aspetto, fornisce un mapping dallo spazio CIE XYZ allo spazio dell'aspetto del colore. Nella direzione da aspetto a colorimetrico, viene eseguito il mapping dallo spazio dell'aspetto del colore allo spazio XYZ. L'aspetto del colore correla la luminosità, J, chroma, C e hue, h. Questi tre valori formano un sistema di coordinate cilindrico. Spesso, risulta più comodo lavorare in un sistema di coordinate rettangolare, quindi calcolare un = C cos h e b = C sin h, per dare UNM02 Jab.

È possibile usare valori di luminosità CAM maggiori di 100. Il comitato CIE che ha formulato ILM02 non ha seguito il comportamento dell'asse di leggerezza per i valori di input con una luminanza maggiore del punto bianco adottato; cio, per i valori Y di input maggiori del valore Y del punto bianco adottato. La sperimentazione ha dimostrato che le equazioni di luminanza in CIECAM02 si comportano ragionevolmente per tali valori. La leggerezza aumenta in modo esponenziale e segue lo stesso esponente (circa 1/3).

A volte gli utenti vogliono modificare il modo in cui viene calcolato il grado di adattamento (D). La progettazione WCS consente agli utenti di controllare questo calcolo modificando il valore degreeOfadaptation nei parametri delle condizioni di visualizzazione.

Per fornire una corrispondenza più coerente con le aspettative degli utenti influenzate da ICC, degreeOfAdaptation nel valore predefinito DICAMPS è 1.0. Ciò produce risultati migliori in tutti i casi diversi da MinCD Absolute, in cui è possibile consentire a WCS di calcolare degreeOfAdaptation (tramite degreeOfAdaptation = -1).

Invece di usare un valore di surround "Average", "Dim" e "Dark", viene fornito un valore di surround continuo, calcolato dal valore c. Il valore di c deve essere un valore float compreso tra 0,525 e 0,69.

Da *c* è possibile calcolare *Nc* e *F,* usando l'interpolazione lineare a pezzetti tra i valori già specificati per "Average", "Dim" e "Dark". In questo modo viene modellata la figura 1 della specifica CIE 159:2004, la specifica DIM02.



| degreeOfAdaption                     | Comportamento                                                                       |
|--------------------------------------|--------------------------------------------------------------------------------|
| -1.0                                 | ![Mostra una formula per il comportamento C I E C A M 02 predefinito.](images/camp-image006.png)Si tratta del comportamento predefinito DIM02.<br/> |
| 0,0 &lt; = degreeOfAdaption &lt; = 1,0 | *D* = degreeOfAdaptation (valore fornito dall'utente)                      |



 

All'implementazione è stata aggiunta anche una certa quantità di controllo degli errori. I numeri di equazione seguenti sono quelli usati nella definizione CIE 159:2004 di PIÙM02.

**ColorimetricToAppearanceColors**

Viene verificata la ragionevolezza dei valori di input: se X o Z &lt; 0.0 o Y &lt; -1.0, il valore HRESULT è E \_ INVALIDARG. Se -1.0 &lt; = Y &lt; 0.0, J, C e h sono tutti impostati su 0,0.

Alcune condizioni interne possono produrre risultati di errore. Invece di produrre tali risultati, i risultati interni vengono ritagliati per produrre valori nell'intervallo. Ciò si verifica per le specifiche di colori che sarebbero scuri e impossibilmente cromatici: nell'equazione 7.23, se A &lt; 0, A = 0. Nell'equazione 7.26, se t &lt; 0, t = 0.

**AppearanceToColorimetricColors**

Viene verificata la ragionevolezza dei valori di input. Se C &lt; 0 , C &gt; 300 o J &gt; 500, HRESULT è E \_ INVALIDARG.

*R'<sub>a;</sub>*, *G'<sub>a;</sub>* e *B'<sub>a;</sub>*, (equazioni 8.19 - 8.21) vengono ritagliati nell'intervallo 399,9 .

Per tutti i profili DELP (Color Appearance Model), il motore WCS esaminerà il punto bianco adottato. Se Y non è 100,0, il punto bianco adottato verrà ridimensionato in modo che Y sia uguale a 100,0. Lo stesso ridimensionamento verrà applicato al valore dello sfondo. Il fattore di scala è 100.0/adoptedWhitePoint.Y. Lo stesso fattore di scala viene applicato a ogni X, Y e Z. Se il campo NormalizeToMediaWhitePoint è impostato su "True" o se è assente dal CAMPO, il motore ridimensiona anche tutti i colori del dispositivo immessi in DeviceToColorimetric in modo che il valore Y del punto bianco multimediale del dispositivo sia uguale a 100,0. I colori del dispositivo provenienti da ColorimetricToDevice verranno ridimensionati in base all'inverso moltiplicativo di tale fattore di scala. Se il flag NormalizeToMediaWhitePoint è impostato su "False", i dati colorimetrici non vengono ridimensionati.

Per alcune attività, è opportuno ridimensionare i valori colorimetrici provenienti da DeviceToColorimetric. Le equazioni di leggerezza iperbolica nella CAM sono progettate per una luminenza a punti bianca di 100,0. L'unico punto in cui entra in gioco una differenza nella luminenza assoluta (o illuminazione) è la luminazione del campo di adattamento. La camma deve quindi essere inizializzata con un punto bianco Y di 100,0. Tuttavia, se il punto bianco medio del modello di dispositivo viene usato come punto bianco adottato, tutti i colori provenienti dal dispositivo devono essere ridimensionati di conseguenza o il bianco del dispositivo non verrà visualizzato con un valore J di 100,0. I valori Y devono quindi essere ridimensionati nelle misurazioni. I valori di misurazione possono essere ridimensionati prima di inizializzare il modello di dispositivo. I risultati saranno già nell'intervallo corretto. Ma questo renderebbe più difficile testare il modello di dispositivo, perché i valori in uscita richiederebbero il ridimensionamento. Per le attività in cui il punto bianco medio del dispositivo viene percepito come un vero bianco, è consigliabile normalizzare in base al punto bianco multimediale del dispositivo.

L'istanza di CAM viene inizializzata direttamente da CAMP. Ciò consente agli sviluppatori una certa flessibilità nell'inizializzazione della camma, in base all'attività che vogliono eseguire. In alcune attività, gli osservatori ignoreranno qualsiasi chroma nei punti vuoti multimediali, perché "sanno" che i supporti di origine e di destinazione sono "bianchi". In questi casi, gli sviluppatori vorranno inizializzare i CAM in avanti e inversa con i rispettivi punti vuoti multimediali. In alcuni casi, gli osservatori potrebbero confrontare il colore degli sfondi multimediali. In questi casi, è consigliabile usare una REGISTRAZIONE per entrambi i dispositivi e potrebbe essere preferibile non ridimensionare i valori colorimetrici di ogni dispositivo in base al punto bianco medio del dispositivo. I diversi valori tristimuli dei supporti porteranno quindi a valori di aspetto diversi in PIÙM02.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base sulla gestione dei colori](basic-color-management-concepts.md)
</dt> <dt>

[Windows Schemi e algoritmi del sistema di colori](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





