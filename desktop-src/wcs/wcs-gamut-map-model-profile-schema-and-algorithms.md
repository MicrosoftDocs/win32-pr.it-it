---
title: Schema e algoritmi del profilo del modello mappa WCS Gamut
description: Schema e algoritmi del profilo del modello mappa WCS Gamut
ms.assetid: 64b9871a-1b4f-4e9a-be4d-4c25b3198b91
keywords:
- Windows Sistema colori (WCS), profilo del modello mappa gamut (GMMP)
- WCS (Windows Color System), profilo del modello mappa gamut (GMMP)
- gestione del colore delle immagini, profilo del modello mappa gamut (GMMP)
- gestione dei colori, profilo del modello mappa gamut (GMMP)
- colors,gamut map model profile (GMMP)
- Windows Sistema a colori (WCS), profili
- WCS (Windows Color System), profili
- gestione dei colori delle immagini, profili
- gestione dei colori, profili
- colori, profili
- Profilo del modello mappa gamut (GMMP)
- GMMP (profilo modello mappa gamut)
- Profilo del modello mappa gamut WCS
- schemi, profilo del modello mappa gamut (GMMP)
- algoritmi, profilo del modello mappa gamut (GMMP)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7db5b7a26fe5832fe33095c5785e90ad0a6938649878ff279e101a7e5817cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118037291"
---
# <a name="wcs-gamut-map-model-profile-schema-and-algorithms"></a>Schema e algoritmi del profilo del modello mappa WCS Gamut

-   [Overview](#overview)
-   [Architettura del profilo del modello mappa Gamut](#gamut-map-model-profile-architecture)
-   [Generazione del limite Gamut](#generation-of-the-gamut-boundary)
-   [The GMMP Schema](#the-gmmp-schema)
-   [Elementi dello schema GMMP](#the-gmmp-schema-elements)
-   [GamutMapModel](#defaultbaselinegamutmapmodel-type)
    -   [Namespace](#namespace)
    -   [Version](#version)
    -   [Documentazione](#documentation)
    -   [Tipo DefaultBaselineGamutMapModel](#defaultbaselinegamutmapmodel-type)
    -   [PlugInGamutMapType](#plugingamutmaptype)
    -   [Extensiontype](#extensiontype)
-   [Algoritmi di base GMMP](#the-gmmp-baseline-algorithms)
-   [Allineamento degli assi neutri](#aligning-the-neutral-axes)
    -   [Differenza di colore minima (MinCD)](#minimum-color-difference-mincd)
    -   [BasicPhoto](#basicphoto)
    -   [Overview](#overview)
    -   [Caso di shell a gamut singolo](#the-case-of-single-gamut-shell)
    -   [Miglioramento del nero](#black-enhancement)
    -   [Caso di shell a doppio gamut](#the-case-of-dual-gamut-shells)
    -   [Motivi per le modifiche apportate alle raccomandazioni CIE TC8-03](#reasons-for-changes-from-the-cie-tc8-03-recommendations)
    -   [Mapping delle tonalità](#hue-mapping)
-   [Descrizione dei limiti gamut e algoritmi della shell Gamut](#gamut-boundary-description-and-gamut-shell-algorithms)
    -   [Triangolazione del limite gamut](#triangulation-of-the-gamut-boundary)
    -   [Elementi linea limite](#boundary-line-elements)
    -   [Operazione Gamut: CheckGamut](#gamut-operation-checkgamut)
    -   [Piano tinta completa: Interseca](#full-hue-plane-intersect)
    -   [Operazione Gamut: CheckGamut (continua)](#gamut-operation-checkgamut-continued)
    -   [Mapping gamut differenza colore minima](#minimum-color-difference-gamut-mapping)
    -   [Smussamento della tonalità](#hue-smoothing)
    -   [Impostazione di primarie e secondarie nella descrizione dei limiti gamut](#setting-primaries-and-secondaries-in-the-gamut-boundary-description)
    -   [Impostazione dell'asse neutro nella descrizione del limite gamut](#setting-the-neutral-axis-in-the-gamut-boundary-description)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Questo schema viene usato per specificare il contenuto di un profilo del modello mappa gamut (GMMP). Gli algoritmi di base associati sono descritti nell'argomento seguente.

Lo schema GMMP di base è costituito da informazioni di intestazione comuni, un riferimento facoltativo a un plug-in gamut map model preferito e tag di estensione.

Il GMMP fornisce inoltre informazioni esplicite sul modello mappa Gamut di destinazione e fornisce criteri sul modello mappa Gamut di fallback di base da usare se il modello di destinazione non è disponibile. Lo schema può includere informazioni di estensione private, ma non include altre informazioni estranee.

## <a name="gamut-map-model-profile-architecture"></a>Architettura del profilo del modello mappa Gamut

![Diagramma che mostra il profilo del modello mappa Gamut.](images/gmmp-image002.png)

Il campionamento dello spazio colorante del dispositivo di output viene eseguito tramite l'iterazione delle coloranti da 0.0 a 1.0 con un passaggio frazionario, accumulando tutte le combinazioni di ogni colorante in ogni passaggio e quindi convertendole dallo spazio colorante del dispositivo allo spazio dell'aspetto del colore usando il metodo DM::D eviceToColorimetricColors seguito dal metodo CAM::ColorimetricToAppearanceColors. Di seguito è riportato un esempio di come viene eseguita questa operazione per RGB.


```C++
For (red= 0.0; red <= 1.0; red += redStep) {

     For (green = 0.0; green <= 1.0; green += greenStep) {

          For (blue = 0.0; blue <= 1.0; blue += blueStep) {

               Colorants[0] = red; colorants[1] = green; colorants[2] = blue;

               pRGBDM->DeviceToColorimetricColors(1, colorants, &amp;XYZ);

               pCAM->ColorimetricToAppearanceColors(1, &amp;XYZ, &amp;JCh);

          }

     }

}

```



## <a name="generation-of-the-gamut-boundary"></a>Generazione del limite Gamut

Esistono tre componenti al limite della gamma: le primarie, i campioni neutri e le shell. Le primarie vengono generate prendendo le primarie del dispositivo e applicando la trasformazione DeviceToColorimetric/ColorimetricToAppearance. I campioni neutri vengono generati tramite il campionamento dello spazio colorante del dispositivo nell'area neutra e l'applicazione della stessa trasformazione. Per tre dispositivi coloranti (RGB o CMY), i campioni neutri sono definiti come con tutte le coloranti uguali, ad esempio R == G == B. Per CMYK, gli esempi neutri sono definiti come C == M == Y == 0.

I fattori che influenzano i dati usati per creare il limite di gamut sono i campioni di dati (solo dispositivi di base) e le condizioni di visualizzazione. La dimensione del passaggio usata per eseguire il campionamento completo dello spazio colorante (per i monitoraggi e per la shell plausibile) è una costante interna e non è disponibile per la manipolazione esterna. La modifica delle condizioni di visualizzazione modifica il comportamento del modello di aspetto colore (CAM) e modifica la forma del limite di gamut, quindi è necessario generare un limite di gamut associato al profilo delle condizioni di visualizzazione. Se vengono usati dati di esempio, come nel caso delle stampanti di base e dei dispositivi di acquisizione, gli esempi avranno un notevole impatto sulla forma della gamma di riferimento e influiranno sul comportamento del modello stesso.

Per i dispositivi di input, ad esempio fotocamere e scanner, vengono usati campionamenti diversi per generare la shell di riferimento e la shell plausibile. La shell di riferimento viene generata dalle misurazioni usate per inizializzare il modello di dispositivo. La shell plausibile viene generata in modo simile alla figura precedente per i dispositivi di output. La differenza è che quando si input una destinazione tipica, non si ottengono valori completamente saturi (dove R, G o B = 255). È necessario eseguire l'estrapolazione usando il modello di dispositivo per stimare tali valori.

## <a name="the-gmmp-schema"></a>The GMMP Schema


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema 
  xmlns:gmm="http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Gamut Map Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:element name="GamutMapModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="DefaultBaselineGamutMapModel">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="HPMinCD_Absolute"/>
              <xs:enumeration value="HPMinCD_Relative"/>
              <xs:enumeration value="SGCK"/>
              <xs:enumeration value="HueMap"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
        <xs:element name="PlugInGamutMapModel" minOccurs="0">
          <xs:complexType>
            <xs:sequence>
              <xs:any namespace="##other" processContents="skip"
                minOccurs="0" maxOccurs="unbounded" />
            </xs:sequence>
            <xs:attribute name="GUID" type="wcs:GUIDType" use="required"/>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>
```



## <a name="the-gmmp-schema-elements"></a>Elementi dello schema GMMP

## <a name="gamutmapmodel"></a>GamutMapModel

Questo elemento è una sequenza dei sotto-elementi seguenti:

1.  Stringa ProfileName,
2.  DefaultBaselineGamutMapModel,
3.  Stringa di descrizione facoltativa,
4.  Stringa di creazione facoltativa,
5.  PlugInGamutMap facoltativo e
6.  ExtensionType facoltativo.

**Condizioni di** convalida: ogni sotto-elemento viene convalidato in base al proprio tipo.

### <a name="namespace"></a>Spazio dei nomi

xmlns:gmm=" http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel "

targetNamespace=" http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel "

### <a name="version"></a>Versione

Versione "1.0" con la prima versione di Windows Vista.

**Condizioni di** convalida: 1.0 in Windows Vista. Le &lt; versioni 2.0 sono valide anche per supportare modifiche non di rilievo al formato.

### <a name="documentation"></a>Documentazione

Schema del profilo del modello mappa Gamut.

Copyright (C) Microsoft. Tutti i diritti sono riservati.

**Condizioni di** convalida: ogni sotto-elemento viene convalidato in base al proprio tipo.

### <a name="defaultbaselinegamutmapmodel-type"></a>Tipo DefaultBaselineGamutMapModel

Tipo UINT

Valori di enumerazione:

<dl> "MinCD \_ Absolute"  
"MinCD \_ Relative"  
"SIG \_ KNEE"  
"HueMap"  
</dl>

**Condizioni di convalida:** i valori devono corrispondere a una delle enumerazioni precedenti.

### <a name="plugingamutmaptype"></a>PlugInGamutMapType

Questo elemento è una sequenza di GUID GUIDType ed eventuali elementi secondari.

**Condizioni di** convalida: il GUID viene usato per corrispondere al GUID della DLL plug-in GMM. Esistono un massimo di 100.000 elementi secondari personalizzati.

### <a name="extensiontype"></a>Extensiontype

Questo elemento è una sequenza facoltativa di tutti gli elementi secondari.

**Condizioni di** convalida: possono essere presenti al massimo 100.000 elementi secondari.

## <a name="the-gmmp-baseline-algorithms"></a>Algoritmi di base GMMP

## <a name="aligning-the-neutral-axes"></a>Allineamento degli assi neutri

La maggior parte degli algoritmi di mapping a gamut ha l'obiettivo di eseguire il mapping dell'asse neutro del dispositivo di origine all'asse neutro del dispositivo di destinazione: il bianco passa al bianco, dal nero al nero e dal grigio al grigio. Questa operazione viene affrontata in parte ridimensionando la leggerezza dei colori di origine in modo che corrisponda alla gamma di luminosità del dispositivo di destinazione. Ma questo non consente di risolvere completamente il problema.

È una proprietà fisica della maggior parte dei dispositivi di creazione di immagini che la cromaticità del bianco del dispositivo non corrisponde esattamente alla cromaticità del dispositivo nero. Ad esempio, il monitoraggio del bianco dipende dalla somma delle cromatiche e delle luminanze relative delle tre primarie, mentre il nero di monitoraggio dipende dalla riflettenza della superficie di visualizzazione. Il bianco della stampante dipende dalla cromaticità della carta, mentre il nero della stampante dipende dall'input penna o dal toner usato. Un modello di aspetto che esegue il mapping del bianco del dispositivo esattamente all'asse neutro dello spazio dell'aspetto (chroma esattamente uguale a zero) non esegue il mapping del dispositivo nero all'asse neutro. Poiché l'occhio è più sensibile alle differenze di croma con l'aumentare della luminosità, i grigi medi saranno rappresentati come ancora più cromatici rispetto al nero del dispositivo. La figura 1 illustra la curvatura degli assi neutri in due dimensioni. In realtà, gli assi neutri formano una curva più complessa in tre dimensioni.

Mentre la CAM stima che questi colori neutri del dispositivo verranno visualizzati cromatici, gli osservatori effettivi sembrano compensare questo problema. La maggior parte delle persone non considera questi valori neutri del dispositivo come cromatici. Per la maggior parte dei modelli di mapping a gamut, è quindi consigliabile continuare a eseguire il mapping dei neutri di origine ai neutri del dispositivo.

Per eseguire il mapping dei neutri di origine ai neutri del dispositivo, regolare i limiti di gamut di origine e di destinazione e ogni pixel quando si applica l'algoritmo di mapping della gamma. Prima di tutto, regolare ogni valore nel colore di origine in modo che l'asse neutro del dispositivo di origine in corrispondenza della luminosità del colore di origine cada direttamente sull'asse neutro dello spazio dell'aspetto. Vedere il lato sinistro della figura 1. Modificare quindi la descrizione del limite della gamma del dispositivo di destinazione in modo che ogni colore sull'asse neutro del dispositivo di destinazione in corrispondenza della luce del colore del limite della gamma del dispositivo di destinazione ricada direttamente sull'asse neutro dello spazio dell'aspetto. Vedere il lato destro della figura 1.

![Diagramma che mostra il grafo limite gamut di origine a sinistra e il limite gamut di destinazione a destra.](images/gmmp-image004.png)

**Figura 1:** Allineamento degli assi neutri illustrati. A sinistra: regolazione dei punti di origine rispetto all'asse neutro del dispositivo di origine. A destra: modifica della descrizione del limite della gamma di destinazione rispetto alla descrizione del limite della gamma di destinazione.

Si noti che si regola ogni valore di pixel di origine rispetto all'asse neutro in corrispondenza di tale valore di leggerezza. Ciò garantisce che i neutri del dispositivo di origine cadranno sull'asse neutro del modello di aspetto. Si spostano anche tutti gli altri colori con tale luminosità della stessa quantità, in modo che non siano presenti discontinuità nella rappresentazione della gamma di origine. È necessario spostare di quantità diverse a livelli di luminosità diversi, perché i neutri del dispositivo di origine non sono rappresentati come ugualmente cromatici ai diversi livelli di luminosità. Chiaramente, non si tratta di una trasformazione semplice.

La gestione dei valori del dispositivo di destinazione è un po' più difficile. Inizialmente, si regola l'intero limite della gamma di destinazione in modo simile, ma rispetto all'asse neutro del dispositivo di destinazione. Questa operazione è illustrata nella figura 1 sul lato destro. Questa regolazione assicura che i valori grigi di origine verranno mappati ai valori grigi di destinazione. Questo è lo spazio in cui operano gli algoritmi di mapping della gamma.

Tuttavia, questo spazio non descrive in modo accurato il vero comportamento del dispositivo di destinazione. È necessario invertire il mapping prima che i colori mappati a gamut siano consegnati al modello di aspetto e al modello di dispositivo di destinazione. Tutti i valori mappati vengono compensati dall'opposto dell'offset applicato in precedenza all'asse neutro del dispositivo di destinazione. In questo modo viene eseguito il mapping dell'asse neutro di destinazione al valore rappresentato originariamente dalla CAM. Lo stesso vale per il limite di gamut e per tutti i valori intermedi.

![Diagramma che mostra un grafico per annullare l'allineamento dell'asse neutro del dispositivo di destinazione.](images/gmmp-image008.png)

**Figura 2:** Annullamento dell'allineamento dell'asse neutro del dispositivo di destinazione

### <a name="minimum-color-difference-mincd"></a>Differenza di colore minima (MinCD)

Differenza di colore minima (MinCD) Versioni relative e assolute, equivalenti alla finalità colorimetrica ICC.

> [!Note]  
> MinCD GMM è adatto per il mapping di grafica e line art contenenti colori "logo" (tinte piatte), sfumature di colore del logo con alcuni colori fuori gamma e per la fase finale delle trasformazioni di prova. Anche se minCD GMM può essere usato per immagini fotografiche interamente all'interno della gamma di destinazione, non è consigliabile per il rendering generale delle immagini fotografiche. Il mapping dei colori out-of-gamut ai colori sulla superficie della gamma di destinazione può causare artefatti indesiderati, ad esempio irregolarità del tono o della croma in sfumature lisce che attraversano il limite della gamma. BasicPhoto è consigliato per le immagini fotografiche. Se un'immagine di tipo fotografia o contone richiede un mapping di gamut diverso da BasicPhoto, l'alternativa consiste nel creare un GMM plug-in che implementa tale mapping, anziché usare MinCD.

 

I colori in gamut rimangono invariati. Per i colori out-of-gamut, la luminosità e la croma vengono regolate individuando il punto nella gamma di destinazione con la distanza minima del colore dai punti di input fuori gamma. La distanza dei colori viene calcolata nello spazio JCh. Tuttavia, si pondera la distanza in leggerezza (J) e la distanza in chroma (C) o tonalità (h) in modo diverso. Una funzione di peso dipendente dalla croma viene usata per la distanza in leggerezza in modo che il peso sia più piccolo per la croma piccola e più grande per la croma di grandi dimensioni fino a quando non viene raggiunta una chroma soglia, dopo la quale il peso rimane a 1, ovvero lo stesso peso della distanza in chroma o tonalità. Ciò segue l'utilizzo consigliato per CMC e CIEDE2000. Esistono due varianti: colorimetrica relativa e colorimetrica assoluta.

**Colorimetrica relativa:** Allineare prima di tutto gli assi neutri di origine e di destinazione, come descritto in precedenza. Ritagliare quindi il colore di origine regolato al limite della gamma di destinazione regolata. Vedere la figura 4. Mapping di chroma con una leggerezza costante. Regolare i valori del dispositivo di destinazione come descritto in precedenza. Nel caso di un limite gamut di destinazione monocromatico, il ritaglio della chroma indica che il valore della croma (C) è impostato su zero (0,0).

**Colorimetrica assoluta:** È simile alla colorimetrica relativa, ma senza l'allineamento dell'asse neutro di origine e di destinazione. Il valore di origine viene ritagliato direttamente sull'asse neutro di destinazione. Si noti che se i limiti della gamma di origine e di destinazione sono monocromatici, il comportamento è identico alla variante colorimetrica relativa. in altri, viene eseguito l'allineamento degli assi neutri e quindi la croma viene ritagliata a zero. In questo modo si garantisce che si osti un output ragionevole anche se i supporti e le coloranti sono significativamente diversi.

![Diagramma che mostra un grafico per il ritaglio MinCD alla gamma regolata.](images/gmmp-image010.png)

**Figura 3:** Ritaglio minCD alla gamma regolata

### <a name="basicphoto"></a>BasicPhoto

### <a name="overview"></a>Panoramica

BasicPhoto: equivalente alla finalità preferita, di tipo grafico o percettivo ICC.

Questo algoritmo è una variante del mapping della leggerezza sigmoidale dipendente dalla croma e del ridimensionamento del ginocchio cuspide (SGCK) descritto da CIE TC8-03 in CIE156:2004. Questo algoritmo variant supporta i descrittori di limite gamut (GBD) con shell a doppio gamut. cio, GBD con una shell di riferimento e una shell plausibile. L'algoritmo SGCK, che originariamente presuppone una sola shell gamut nel GBD, si basa sull'algoritmo SIG KNEE (Braun 1999), che incorpora il mapping della leggerezza sigmoidale e il ridimensionamento delle funzioni del ginocchio proposto da Braun e Fairchild (1999), combinato con la dipendenza \_ della chroma da GCUSP (Morovic, 1998). Mantiene costante la tonalità percepita, ad esempio, l'angolo della tonalità in Un oggetto con correzione della tonalità e usa un ridimensionamento di luminosità sigmoida generico (indipendente dall'immagine) applicato in modo dipendente dalla croma e una croma della funzione del ginocchio del 90%. La variante viene ridimensionata lungo linee di leggerezza costante.

### <a name="the-case-of-single-gamut-shell"></a>Caso di shell a gamut singolo

È utile esaminare l'algoritmo nel caso in cui i GBD di origine e di destinazione hanno una sola shell gamut. In questo caso, l'algoritmo è costituito dai calcoli seguenti.

Per prima cosa, eseguire il mapping iniziale della leggerezza usando la formula seguente:

![Mostra la formula per il mapping iniziale della leggerezza.](images/gmmp-image012.png) (1)

dove *Jₒ* è la leggerezza originale e *J <sub>R</sub>* è la leggerezza della riproduzione.

![Mostra la seconda formula di mapping della leggerezza.](images/gmmp-image014.png) (2)

Quando il limite della gamma di origine è monocromatico, il valore della croma sarà zero per il limite monocromatico a causa dell'allineamento dell'asse neutro. Ciò comporta il caso degenerato in cui C è uguale a zero. In questo caso, *p <sub>C</sub>* è impostato su 1.

*p <sub>C</sub>* è un fattore di ponderazione dipendente dalla croma (Morovic, 1998) che dipende dalla croma del colore originale, C e *J <sub>S</sub>* sono il risultato del mapping della luminosità originale usando una funzione sigmoidal.

 

Per calcolare *J <sub>S</sub>* (Braun e Fairchild, 1999), viene prima impostata una tabella di ricerca unidimensionale (LUT) tra i valori di luminosità originale e di riproduzione sulla base di una funzione normale cumulativa discreta (S).

![Mostra una formula per calcolare J s.](images/gmmp-image016.png) (3)

dove x ₀ e S sono rispettivamente la deviazione media e standard della distribuzione normale e *i* = 0,1,2... *m*,*m* è il numero di punti usati nell'LUT. *S <sub>i</sub>* è il valore della funzione normale cumulativa per *i*  / *m* percent. I parametri dipendono dalla leggerezza del punto nero della gamma di riproduzione e possono essere interpolati dalla tabella 1. Per informazioni dettagliate sul calcolo di questi parametri, vedere Braun e Fairchild (1999, p. 391).

:::row:::
    :::column:::
        J <sub>minOut</sub>
    :::column-end:::
    :::column:::
       5.0
    :::column-end:::
    :::column:::
        10,0
    :::column-end:::
    :::column:::
        15.0
    :::column-end:::
    :::column:::
        20,0
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        x ₀
    :::column-end:::
    :::column:::
       53.7
    :::column-end:::
    :::column:::
        56.8
    :::column-end:::
    :::column:::
        58.2
    :::column-end:::
    :::column:::
        60.6
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        S
    :::column-end:::
    :::column:::
       43,0
    :::column-end:::
    :::column:::
        40,0
    :::column-end:::
    :::column:::
        35.0
    :::column-end:::
    :::column:::
        34.5
    :::column-end:::
:::row-end:::


**Tabella 1:** Calcolo del parametro di compressione della leggerezza BasicPhoto

Per usare S come mapping di leggerezza LUT (S <sub>LUT),</sub> deve prima essere normalizzato nell'intervallo di leggerezza \[ di 0.100 \] . I dati normalizzati vengono quindi ridimensionati nell'intervallo dinamico del dispositivo di destinazione, come illustrato nell'equazione 4, dove *J*<sub>min\ *Out*</sub> e *J*<sub>max\ *Out*</sub> sono rispettivamente i valori di leggerezza del punto nero e del punto bianco del supporto di riproduzione.

![Mostra la formula per S come mapping di leggerezza LUT.](images/gmmp-image018.png) (4)

A questo punto, i valori *J S* possono essere ottenuti dalla S <sub>LUT</sub> interpolando tra i punti *m* dei valori *J O'* e *J S* corrispondenti contenuti e usando l'equazione seguente come input.

![Mostra la formula per ottenere i valori J S.](images/gmmp-image020.png) (5)

J <sub>minIn</sub> è il valore di leggerezza del punto nero del supporto originale, J <sub>maxIn</sub> è il valore di leggerezza del punto bianco del supporto originale e J <sub>O</sub> è la luminosità originale. Per informazioni di riferimento successive, è possibile indicare da *S* la funzione sigmoidal definita nel modo appena descritto, come illustrato nella figura 4 seguente.

![Diagramma che mostra il grafico per il mapping della croma con una leggerezza costante.](images/gmmp-image024.png)

**Figura 4:** Mapping di Chroma con una leggerezza costante

In secondo piano, se il limite della gamma di destinazione è cromatico, comprimere la chroma lungo linee di leggerezza costante (l) ed eseguire la compressione come indicato di seguito.

![Mostra la formula per eseguire la compressione della croma.](images/gmmp-image026.png)  (6)

dove *d* rappresenta la distanza da *E* su *l*; *g* rappresenta il limite medio della gamma; *r* rappresenta la riproduzione; e *o* la figura 5 originale.

![Diagramma che mostra il grafico per la compressione della croma e della leggerezza in BasicPhoto.](images/gmmp-image028.png)

**Figura 5:** Compressione di chroma e leggerezza in BasicPhoto

Se il limite della gamma di destinazione è monocromatico, il valore di chroma viene ritagliato a zero.

In terzo piano, usare un clip MinCD (descritto in precedenza) per eliminare eventuali errori residui.

### <a name="black-enhancement"></a>Miglioramento del nero

L'algoritmo precedente può essere modificato per migliorare il nero quando la destinazione è un dispositivo di stampa. Il problema riguarda la scelta di *J <sub>minOut</sub>*, che in genere non corrisponde al colore più scuro che una stampante può produrre.

In particolare, il colore con la massima densità, ottenuto inserendo il 100% di inks (o la copertura massima possibile, se è in vigore la limitazione GCR/input penna), in genere non è "neutro" nello spazio dell'aspetto del colore. Vedere la figura 6. In altre parole, se per il dispositivo di destinazione viene usata la luminosità minima neutra, il ridimensionatore di leggerezza costruito verrà mappato a una luminosità minima che non è la massima densità che può essere ottenuta dalla stampante. Si consideri l'ulteriore caso d'uso del monitoraggio da stampante a stampante. Il monitor nero, R=G=B=0, verrà quindi stampato come non con la massima densità. L'impatto sulla qualità dell'immagine è la mancanza di profondità e contrasto.

![Diagramma che mostra come il punto nero del dispositivo potrebbe essere più scuro della luminosità minima neutra.](images/gmmp-seqfigure01.png)

**Figura 6:** il punto nero del dispositivo può essere più scuro della luminosità minima neutra.

Si supponga che il "punto nero del dispositivo" di destinazione sia Jkakbk/JkCkh k. Se C k non è zero, il punto nero del dispositivo non è neutro rispetto a CAM02. Se si usa J k per la destinazione "luminosità minima neutra" nella costruzione del ridimensionatore di leggerezza; cio, impostazione

*J <sub>minOut</sub> = Jₖ*

e applicarlo alla shell di gamut di origine, si ottiene la configurazione illustrata nella figura 7. Nella figura, il piano di tonalità corrisponde a h k.

![Diagramma che mostra il ridimensionatore di leggerezza modificato con il punto nero del dispositivo di destinazione.](images/gmmp-seqfigure02.png)

**Figura 7:** Geometria che usa il ridimensionatore di leggerezza modificato con il punto nero del dispositivo di destinazione

Per consentire l'esecuzione dell'algoritmo di compressione chroma successivo, è necessario allineare le leggerezze massima e minima nelle shell di origine e di destinazione. Questa operazione può essere ottenuta regolando la shell di destinazione tra J <sub>neutralMin</sub> e J k spostando i punti a sinistra. Inoltre, questa trasformazione deve essere applicata all'intero spazio di Jab, non solo al piano di tonalità corrispondente a h k.

La trasformazione è

![Mostra la formula per la trasformazione.](images/gmmp-seqfigure03.png)

La figura 8 illustra l'effetto della trasformazione.

![Diagramma che mostra l'effetto del ridimensionatore di luminosità modificato con il punto nero del dispositivo di destinazione.](images/gmmp-seqfigure04.png)

**Figura 8:** Geometria che usa il ridimensionatore di leggerezza modificato con il punto nero del dispositivo di destinazione

Dopo aver applicato il consueto algoritmo di compressione chroma, il punto deve quindi essere "spostato indietro". In altri termini, è necessario applicare la trasformazione inversa per ottenere il colore mappato finale.

![Mostra la formula per la trasformazione inversa per ottenere il colore mappato finale.](images/gmmp-seqfigure05.png)

### <a name="the-case-of-dual-gamut-shells"></a>Caso di shell a doppio gamut

L'obiettivo è generalizzare SIG KNEE per la shell a gamut singolo nel caso in cui il dispositivo di origine GBD o il dispositivo di destinazione \_ GBD abbia una struttura a due shell. La shell interna sarà denominata Shell di riferimento, mentre la shell esterna sarà denominata Shell plausibile. Si vogliono considerare i casi seguenti.

(a) Sia gbD di origine che GBD di destinazione hanno una struttura a due shell.

(b) L'origine GBD ha una struttura a due shell; il GBD di destinazione ha una sola shell.

(c) L'unità GBD di origine ha una sola shell; la struttura GBD di destinazione ha una struttura a due shell.

(d) Sia gbD di origine che GBD di destinazione hanno una sola shell.

Il caso (d) è il caso della shell a gamut singola descritta in precedenza. Per i casi (a), (b) e (c), è possibile generalizzare la scalabilità della leggerezza per usare le informazioni aggiuntive della struttura a doppio shell. Nei casi (b) e (c) in cui l'origine o la destinazione ha una sola shell, si introduce una "shell di riferimento indotta" che verrà discussa in una sezione successiva, "Shell di riferimento indotta". L'algoritmo generale per due shell verrà descritto per caso (a). Dopo aver spiegato la costruzione della shell di riferimento indotta, l'algoritmo può essere applicato anche ai case (b) e (c). Come per la compressione chroma, il rapporto di compressione sarà determinato dalle shell più grandi disponibili. In altre parole, se sono disponibili sia Plausible Shell che Reference Shell, verrà usata plausible Shell. In caso contrario, verrà usata la shell di riferimento.

*Scalabilità della leggerezza generalizzata*

L'esistenza di due shell per GBD di origine e di destinazione significa che è necessario eseguire il mapping di un set di quattro punti dal GBD di origine a un set corrispondente nel GBD di destinazione.

![Illustra come eseguire il mapping di un set di quattro punti a un set corrispondente.](images/gmmp-image030.png)

I pedice hanno i significati seguenti.

o o r: "originale" (origine) o "riproduzione" (destinazione)

min o max: luminosità neutra minima o luminosità massima neutra

pla o ref: Plausible Shell o Reference Shell

L'ordinamento in ogni quadruplo è anche la grandezza relativa prevista di questi punti.

La mappa Lightness Rescaling usa le stesse prime due equazioni della singola shell, ma *J S* è definito in modo a parte, come indicato di seguito.

![Mostra la formula per J S in modo a pezzettino.](images/gmmp-image032.png) (7)

In altre parole, è sigmoidal all'interno della shell di riferimento e lineare all'esterno. Vedere Figura 9.

![Diagramma che mostra un grafico per la funzione di scalabilità della leggerezza per i GBD a due shell.](images/gmmp-image033.png)

**Figura 9:** Funzione di scalabilità leggera per GBD a due shell

**SHELL DI RIFERIMENTO INDOTTA**

Se un GBD ha una shell e l'altro GBD ha due shell, è necessario creare una "shell di riferimento" per il GBD con una sola shell. La shell esistente, denominata shell di riferimento, verrà modificata in "Shell plausibile". In realtà, non è necessario creare una shell nello spazio vuoto completo. Poiché la scalabilità leggera usa solo *J max* e *J min*, è necessario solo creare questi valori per la shell di riferimento indotta. Esistono due casi, a seconda di quale GBD ha due shell.

Caso 1: gbd di origine ha due shell; GBD di destinazione ha una shell.

Determinare la shell di riferimento indotta dalla destinazione sull'asse neutro; ad esempio J <sub>r,\ min,\ ref</sub> e J <sub>r,\ max,\ ref</sub> della shell. Questa operazione viene eseguita usando l'algoritmo seguente.

![Mostra l'algoritmo per determinare la shell di riferimento indotta dalla destinazione.](images/gmmp-induced01.png)

I fattori ? <sub>low</sub> e ? <sub>controllo</sub> elevato della separazione tra la shell plausibile e la shell di riferimento. Un valore pari a 1 indica che i valori <sub>minimi</sub> J o J mₐₓ coincidono. I valori vengono "indotti" dalla shell di riferimento di origine e dalla shell plausible di origine.

![Mostra la formula per i valori della shell di riferimento di origine e della shell plausibile di origine.](images/gmmp-induced02.png)

I "fattori di fudge" F  <sub>basso</sub> e F <sub>alto</sub> sono parametri regolabili che devono essere compresi tra 0 e 1. Se il valore è 0, le mₐₓ J <sub>min</sub> o J vengono indotte direttamente dalle shell di origine. In questo caso, scegliere F <sub>basso</sub> = 0,95 e F <sub>alto</sub> = 0,1.

Caso 2: gbd di origine ha una shell; gbd di destinazione ha due shell.

Determinare la shell di riferimento indotta dall'origine sull'asse neutro; ad esempio J <sub>o,\ min,\ ref</sub> e J <sub>o,\ max,\ ref</sub> della shell. Questa operazione viene eseguita usando l'algoritmo seguente.

![Mostra l'algoritmo per determinare la shell di riferimento indotta dalla destinazione sull'asse neutro.](images/gmmp-induced03.png)

Anche in questo caso, i fattori ? <sub>low</sub> e ? <sub>controllo</sub> elevato della separazione tra la shell plausibile e la shell di riferimento. Un valore pari a 1 indica che i valori <sub>minimi</sub> J o mₐₓ coincidono. I relativi valori sono "indotta" dalla shell di riferimento di origine e dalla shell plausible di origine:

![Mostra l'algoritmo per controllare la separazione tra la shell di riferimento e la shell plausibile di origine.](images/gmmp-induced04.png)

### <a name="reasons-for-changes-from-the-cie-tc8-03-recommendations"></a>Motivi delle modifiche apportate alle raccomandazioni CIE TC8-03

BasicPhoto differisce dalle raccomandazioni CIE TC8-03 nei modi seguenti.

1.  Chroma non viene compresso verso la cusp ma lungo le linee di leggerezza costante.
2.  L'intervallo di leggerezza usa la leggerezza del colore più scuro della gamma anziché il punto in cui il limite di gamut attraversa l'asse neutro.
3.  BasicPhoto supporta sia una shell gamut di riferimento che una shell gamut plausibile, se uno dei limiti gamut nella trasformazione ha due shell.
4.  BasicPhoto usa ILM02; invece di usare ILM97s per eseguire la conversione in D65 a 400 cd/m2 e quindi usare lo spazio colore RIT IPT.

La prima modifica è stata apportata per evitare problemi di inversione del tono che possono verificarsi quando si usa la compressione verso un cusp. Come illustrato nella figura 10, la compressione cusp può causare inversioni del tono. Ciò può verificarsi quando i colori della croma alta sono più chiari dei colori della croma inferiore. Poiché SGCK comprime ogni pixel in modo indipendente sia nella leggerezza che nella croma, non è garantito mantenere la relazione di leggerezza tra i valori dei pixel dopo la compressione. Lo svantaggio noto di questa decisione di compressione su linee di leggerezza costante è che è possibile subire perdite di chroma, in particolare nelle aree in cui il limite della gamma di destinazione è molto piana, come accade con i gialli luminosi.

![Diagramma che mostra l'inversione del tono causata da SGCK.](images/gmmp-toneinversion.png)

**Figura 10:** Inversione del tono causata da SGCK

![Mostra un'immagine originale di una teiera.](images/originalteapot.jpg)![Mostra il risultato SGCK dell'immagine della teiera.](images/badteapot.jpg)![Mostra il risultato BasicPhoto dell'immagine della teiera.](images/betterteapot.jpg)

**Figura 11:** Immagine originale, risultato SGCK e risultato BasicPhoto

La figura 11 illustra questa inversione del tono. A sinistra è disponibile un'immagine originale acquisita da una fotocamera digitale. al centro, l'immagine riprodotta da SGCK; e a destra, l'immagine riprodotta da BasicPhoto. L'immagine a sinistra si trova nello spazio colori della fotocamera digitale, le immagini al centro e a destra si trova nello spazio colore di un display video LCD. Nell'immagine originale, la parte superiore della teiera è più scura della parte inferiore, perché la parte inferiore riflette la tovaglia su cui si trova. Nell'immagine SGCK la parte superiore è effettivamente più leggera rispetto alla parte inferiore, a causa dell'inversione del tono. Inoltre, è difficile vedere gli elementi riflessi nella parte inferiore della teiera. A destra BasicPhoto ha corretto l'inversione del tono e gli articoli riflessi sono più chiaramente distinguibili.

La seconda modifica è stata apportata per migliorare la riproduzione di colori quasi neri sulle stampanti in cui il nero più nero non cade direttamente sull'asse neutro DELLAM02. La figura 12 seguente mostra un'immagine convertita in sRGB. riprodotto per una stampante ink inkgb con SGCK; e riprodotti per la stessa stampante usando BasicPhoto. L'immagine al centro non usa il dispositivo completo nero e quindi non ha il contrasto visualizzato nell'originale. Il contrasto viene ripristinato con BasicPhoto.

![Mostra l'immagine originale di un playset.](images/playstructure.jpg)![Mostra l'immagine del playset riprodotta per una stampante ink ink di R G B tramite SGCK.](images/playstructurebad.jpg)![Mostra l'immagine del playset riprodotta per una stampante ink ink di R G B usando BasicPhoto.](images/betterplaystructure.jpg)

**Figura 12:** Nero avanzato

La terza modifica è stata apportata per migliorare la riproduzione dei colori per le fotocamere digitali. In particolare nei casi in cui la fotocamera digitale è stata profilata usando una destinazione di riferimento, una descrizione del limite gamut creata da colori misurati potrebbe non includere tutti i colori che potrebbero essere acquisiti in una scena reale. Invece di ritagliare tutti i colori fino alla gamma della destinazione di colore misurata, è possibile consentire l'estrapolazione per produrre un limite di gamut plausibile. L'algoritmo BasicPhoto è progettato per supportare tale limite di gamut estrapolato.

La quarta modifica è stata apportata perché il mapping di gamut funziona bene. Il processo consigliato da TC8-03 per la conversione dei colori del dispositivo in D65 a 400 cd/m2 e quindi l'uso dello spazio colori RIT IPT richiede molto tempo e a elevato utilizzo di calcolo.

### <a name="hue-mapping"></a>Mapping delle tonalità

HueMap è l'equivalente della finalità Saturazione ICC.

Se il limite di gamut di origine o quello di gamut di destinazione non contiene valori primari, questo modello ripristina il modello MinCD (relativo) descritto in una sezione precedente. ad esempio i dispositivi per cui non è possibile determinare le primarie (profili ICC con più di quattro canali) o profili ICC monocromatici.

Questo algoritmo regola innanzitutto la tonalità del valore del colore di input. Regola quindi contemporaneamente la leggerezza e la chroma, usando un mapping di traslatura. Infine, il valore del colore viene ritagliato per assicurarsi che sia compreso nell'ambito di gamut.

Il primo passaggio consiste nel determinare "Hue Wheels". Trovare i valori JCh per i colori primario e secondario sia per il dispositivo di origine che per quello di destinazione. Si stanno prendendo in considerazione solo i componenti hue. Il risultato è una ruota della tonalità primaria o secondaria con sei punti colore per ogni dispositivo. Vedere la figura 13.

![Diagramma che mostra le rotelle di tonalità con sei punti colore.](images/gmmp-figure12.png)

**Figura 13:** Ruota hue

È possibile ottenere risultati migliori se il database primario blu di origine non viene ruotato nella replica primaria blu di destinazione. Al contrario, l'angolo della tonalità primaria blu di origine viene usato come angolo della tonalità primaria blu di destinazione.

Eseguire quindi le rotazioni della tonalità per ogni colore di input dall'immagine di origine,

a)Usando l'angolo di tonalità del colore di input, determinare la posizione del colore sulla rotellina della tonalità di origine rispetto ai due colori primari o secondari adiacenti. La posizione può essere pensata come una percentuale della distanza tra le primarie. Ad esempio, la tonalità di colore di input è il 40% del percorso dal valore della tonalità di Magenta al valore di tonalità rosso.

b)Nella ruota della tonalità di destinazione trovare l'angolo di tonalità associato, ad esempio il 40% da Magenta al rosso. Questo valore sarà l'angolo della tonalità di destinazione.

In generale, i database primari e secondari di origine non avranno gli stessi angoli di tonalità dei database primari e secondari di destinazione. ciò significa che l'angolo della tonalità di destinazione sarà in genere diverso dall'angolo di tonalità di origine.

Si supponga, ad esempio, che le ruote hue produca i valori seguenti:

Source M = 295 gradi, Source R = 355 degrees.

Destination M = 290 gradi, Destination R = 346 degrees.

Se l'angolo di tonalità del colore di input è di 319 gradi, è il 40% dell'angolo (24 gradi) dall'origine M alla R di origine. L'angolo da M a R è di 60 gradi e l'angolo da M alla tonalità di input è di 24 gradi. Calcolare l'angolo nella destinazione che è del 40% dalla destinazione M alla destinazione R (22 gradi), in modo che l'angolo di tonalità del colore di destinazione sia di 312 gradi.

Calcolare quindi i punti di riferimento della tonalità per la tonalità di origine e la tonalità di destinazione. Per calcolare il punto di riferimento della tonalità per un particolare valore h (tonalità), si vogliono trovare il valore J (leggerezza) e il valore C (chroma).

-   Trovare il valore J del punto di riferimento della tonalità interpolando tra i valori J per i punti primari o secondari adiacenti, usando la posizione relativa della tonalità; ad esempio il 40% in questo esempio.
-   Trovare il valore C massimo in questo valore J e in questo valore h. È ora disponibile il JCh del punto di riferimento della tonalità per tale tonalità.

![Diagramma che mostra una foglia di tonalità.](images/gmmp-figure13.png)

**Figura 14:** Foglia di tonalità (visualizzazione di una sezione limite gamut a una tonalità specifica)

Il passaggio successivo consiste nel calcolare il mapping della sezione per ogni pixel. In primo luogo, visualizzare una foglia di tonalità dalla gamma di origine per l'angolo della tonalità di colore di origine e una foglia di tonalità dalla gamut di destinazione per l'angolo della tonalità di destinazione calcolato durante la rotazione della tonalità. Le fette di tonalità vengono create prendendo una "sezione" dalla superficie limite del gamut JCh con un angolo di tonalità specifico (vedere la figura 14).

NOTA: per motivi di ottimizzazione delle prestazioni, le foglia di tonalità non vengono effettivamente create. vengono descritte e mostrate qui solo a scopo di visualizzazione. Le operazioni vengono eseguite direttamente sulla superficie limite della gamma alla tonalità specificata. Si calcolano quindi i punti di riferimento della tonalità per determinare il mapping della setra.

-   Eseguire una scalabilità leggera per eseguire il mapping dei punti bianco e nero della foglia di origine alla foglia di destinazione (vedere la figura 15). I punti nero e bianco della foglia di tonalità di origine vengono mappati in modo lineare ai punti nero e bianco della foglia di tonalità di destinazione, ridimensionando tutte le coordinate J del limite di origine. Il valore del colore di input mappato alla tonalità viene ridimensionato nello stesso modo.

![Diagramma che mostra il mapping della leggerezza.](images/gmmp-figure14.png)

**Figura 15:** Mapping della leggerezza

-   Determinare i punti di riferimento della tonalità per ogni foglia di tonalità. Applicare un mapping di sezione alla foglia di origine in modo che i punti di riferimento di origine e di destinazione coincidano (vedere la figura 16). Il punto di riferimento per una gamma in corrispondenza di una tonalità specifica è il punto di riferimento della tonalità interpolata tra le primarie adiacenti. Il punto di riferimento della foglia di tonalità di origine viene mappato in modo lineare al punto di riferimento della foglia di tonalità di destinazione, usando un'operazione di "sezione" che blocca l'asse J, mantenendo i punti neri e i punti bianchi stazionari. I punti neri, i punti bianchi e i punti di riferimento delle tonalità di origine e di destinazione devono coincidere.
-   Applicare il mapping di semaforo al valore del colore di input regolato per la leggerezza. Le coordinate J e C del valore del colore di origine vengono ridimensionate in modo proporzionale rispetto alla distanza dall'asse J.
-   Successivamente, viene eseguita una leggera compressione della leggerezza dipendente dalla croma verso il valore J del punto di riferimento della tonalità sul punto di colore mappato a scaglie. La compressione verso il riferimento alla tonalità J viene eseguita in modo simile a gamma, in cui il bianco, il nero, i grigi e i punti sul riferimento della tonalità J non sono interessati. Tutti gli altri punti tendono verso il riferimento alla tonalità J in modo uniforme, leggermente in prossimità del riferimento della tonalità J, con la costante della chroma rimanente. La dipendenza chroma garantisce che i colori neutri non siano interessati e l'effetto viene aumentato sui colori con una chroma superiore.

Di seguito è riportata una descrizione matematica della compressione della leggerezza verso il riferimento della tonalità J o della regolazione del valore J del punto di destinazione. Viene chiamato punto di destinazione perché è stato eseguito il mapping alla gamma di destinazione.

In primo luogo, calcolare "factorC" (fattore di dipendenza chroma) per il punto di destinazione, che determina l'effetto della compressione della leggerezza. I punti vicini o sull'asse J avranno una compressione piccola o nessuna compressione. i punti più distorsi dall'asse J (alta chroma) avranno una compressione maggiore. Moltiplicare per 0,5 per assicurarsi che factorC sia minore di 1, perché è possibile che sourceC sia leggermente maggiore di referenceC, ma non il doppio del doppio.

factorC = (destinationC/referenceC) ? 0,5

dove:

destinationC è il valore C del punto di destinazione.

referenceC è il valore C del punto di riferimento Hue.

Determinare quindi se il punto di destinazione J si trova sopra o sotto il riferimento di tonalità J. Se è sopra, eseguire le operazioni seguenti:

1.  Calcolare "factorJ" per il punto di destinazione relativo al referenceJ. Questo valore factorJ sarà compreso tra 0 e 1 (0 se per referenceJ; 1 se in maxJ).
2.  factorJ = (destinationJ - referenceJ) / (maxJ - referenceJ)

    dove:

    destinationJ è il valore J del punto di destinazione.

    referenceJ è il valore J del punto di riferimento della tonalità.

    maxJ è il valore J massimo della gamma.

3.  Applicare una funzione di potenza simile a gamma a factorJ, che ridurrà factorJ di una determinata quantità. Questo esempio usa la potenza di 2 (il quadrato). Sottrarre il fattore ridottoJ dal fattore originaleJ e moltiplicare il risultato per l'intervallo J totale sopra il riferimento principaleJ per trovare il "deltaJ", che rappresenta la modifica in J dopo la compressione della leggerezza, ma senza includere la dipendenza chroma.
4.  deltaJ = (factorJ - (factorJ ? factorJ)) ? (maxJ - referenceJ)

5.  Applicare factorC alla deltaJ (maggiore è la chroma, maggiore è l'effetto) e calcolare il nuovo valore J per il punto di destinazione.
6.  destinationJ = destinationJ - (deltaJ ? factorC)

Se il valore J per il punto di destinazione è sotto referenceJ, viene eseguito un calcolo simile ai passaggi precedenti A-C, usando minJ anziché maxJ per trovare l'intervallo in J per calcolare il factorJ e tenendo conto della polarità delle operazioni "sotto" il referenceJ.

factorJ = (referenceJ - destinationJ) / (referenceJ - minJ)

deltaJ = (factorJ - (factorJ ? factorJ)) ? (referenceJ - minJ)

destinationJ = destinationJ + (deltaJ ? factorC)

dove:

minJ è il valore J minimo della gamma.

La chroma per i punti di colore di input viene espansa in modo lineare (quando possibile) lungo una luce costante proporzionale al valore chroma massimo delle gamut di origine e destinazione in base a tale tonalità e leggerezza. In combinazione con la compressione della leggerezza dipendente dalla chroma precedente, ciò consente di mantenere la saturazione perché il mapping della sega con i punti di riferimento talvolta causa l'overcomprimere il punto di origine nella chroma (vedere la figura 16).

![Diagramma che mostra il mapping della cande in modo che corrisponda ai punti di riferimento della tonalità, prima della barra a sinistra, dopo la barra a destra.](images/gmmp-shearmapping.png)

**Figura 16:** Mapping della sega, compressione della leggerezza verso il riferimento della tonalità J e espansione della chroma

Di seguito è riportata una descrizione matematica del processo di espansione della chroma o la modifica del valore C del punto di destinazione. Viene chiamato punto di destinazione perché è stato mappato e la leggerezza è stata compressa nella gamma di destinazione.

1.  Prima del mapping di sega, determinare sourceExtentC (l'extent chroma alla leggerezza e alla tonalità del punto di origine).
2.  Dopo il mapping di estendibilità e la compressione della leggerezza che trasforma il punto di origine nel punto di destinazione, determinare destExtentC (l'extent chroma alla luce e alla tonalità del punto di destinazione).
3.  Se sourceExtentC è maggiore di destExtentC, non è necessaria alcuna regolazione della chroma al punto di destinazione ed è possibile ignorare il passaggio successivo.
4.  Regolare destinationC (la chroma del punto di destinazione) in modo che si adatti all'estensione della chroma di destinazione con questa luminosità e tonalità.
5.  destinationC = destinationC ? (destExtentC/sourceExtentC)

    dove:

    destinationC è il valore C del punto di destinazione.

    sourceExtentC è il valore C massimo della gamma di sorgenti alla leggerezza e alla tonalità del punto di origine.

    destExtentC è il valore C massimo della gamma di destinazione alla leggerezza e alla tonalità del punto di destinazione.

Infine, eseguire il ritaglio della distanza mimimum. Se il colore di input con rotazione della tonalità, regolato con leggerezza e mappato a taglio è ancora leggermente esterno al gamut di destinazione, ritagliarlo (spostarlo) nel punto più vicino al limite di gamut di destinazione (vedere la figura 17).

![Diagramma che mostra il ritaglio della distanza minima.](images/gmmp-figure15.png)

**Figura 17:** Ritaglio della distanza minima

## <a name="gamut-boundary-description-and-gamut-shell-algorithms"></a>Descrizione dei limiti di Gamut e algoritmi della shell Gamut

La funzione limite di gamut del dispositivo usa il motore del modello di dispositivo e i parametri analitici per derivare un limite di gamut del dispositivo a colori, descritto come un elenco di vertici indicizzati della carena della gamut del dispositivo. La carena viene calcolata in modo diverso a seconda che si lavori con dispositivi additivi, ad esempio monitor e proiettori o dispositivi sottrattivi. L'elenco di vertici indicizzati viene archiviato in CIEJab. La struttura dell'elenco di vertici indicizzati è ottimizzata per l'accelerazione hardware da DirectX.

Questo approccio ha molte soluzioni note. Se si cerca "Convex hull DirectX" sul Web, si ottengono più di 100 riscontri. Ad esempio, è disponibile un riferimento del 1983 su questo argomento specifico (Teoria della grafica computer e applicazione, "Shiphulls, superfici b-spline e cadcam", pp. 34-49) con riferimenti a partire dal 1970 al 1982 sull'argomento.

La raccolta di punti può essere determinata dalle informazioni disponibili esternamente, come indicato di seguito:

-   I punti per la shell di riferimento per i monitoraggi vengono generati usando un campionamento del cubo dei colori nello spazio colorato del dispositivo.
-   I punti per la shell di riferimento per stampanti e dispositivi di acquisizione vengono ottenuti dai dati di esempio usati per inizializzare il modello.
-   I punti per la shell di riferimento per scRGB e sRGB vengono generati usando un campionamento del cubo dei colori per sRGB.
-   I punti per la shell plausibile per i dispositivi di acquisizione vengono generati usando un campionamento del cubo dei colori nello spazio colorato del dispositivo.
-   I punti per la shell di riferimento per i proiettori vengono generati usando un campionamento di un poliedro nel cubo dei colori nello spazio colorato del dispositivo.
-   I punti per la possibile shell per spazi colori a intervalli dinamici ampi vengono generati usando un campionamento del cubo dei colori nello spazio stesso.

È possibile creare un elenco di vertici che descriva in modo efficiente la gamma dei dispositivi a colori, in base a un profilo di dispositivo e ai servizi di supporto del sistema.

Per i dispositivi di output, il limite di gamut descrive la gamma di colori che possono essere visualizzati dal dispositivo. Viene generato un limite di gamut dagli stessi dati usati per modellare il comportamento del dispositivo. Concettualmente, si genera un campionamento dell'intervallo di colori che il dispositivo può produrre, si misurano i colori, si convertono le misurazioni nello spazio dell'aspetto e quindi si usano i risultati per creare il limite di gamut.

I dispositivi di input sono più difficili. Ogni pixel in un'immagine di input deve avere un valore. Ogni pixel deve essere in grado di rappresentare qualsiasi colore trovato nel mondo reale in qualche modo. In questo senso, nessun colore è "fuori gamma" per un dispositivo di input, perché possono essere sempre rappresentati.

Tutti i formati di immagine digitale hanno un intervallo dinamico fisso. A causa di questa limitazione, esistono sempre alcuni smuli distinti mappati allo stesso valore digitale. Non è quindi possibile stabilire un mapping uno-a-uno tra i colori reali e i valori della fotocamera digitale. Il limite di gamut viene invece formato stimando una gamma di colori reali in grado di produrre le risposte digitali della fotocamera. L'intervallo stimato viene utilizzato come intervallo per il dispositivo di input.

Sono incluse le primarie per fornire il mapping di gamut di tipo finalità grafica aziendale.

In un vero stile orientato a oggetti si astrae la rappresentazione sottostante del limite di gamut. In questo modo è possibile modificare la rappresentazione in futuro. Per comprendere il descrittore di limite di gamut (GBD) usato nella nuova CTE, è necessario prima di tutto comprendere il funzionamento degli algoritmi di mapping gamut. Tradizionalmente, gli GVA sono stati progettati per soddisfare le esigenze della community di grafica grafica; ovvero riprodurre immagini di cui è già stato eseguito correttamente il rendering per il dispositivo in cui è stata creata l'immagine di input. L'obiettivo degli gmA di grafica grafica è quello di ottenere la migliore riproduzione possibile dell'immagine di input nel dispositivo di output. La nuova CTE GBD è progettata per risolvere quattro problemi chiave.

Poiché viene eseguito il rendering dell'immagine di input per il dispositivo di input, tutti i colori rientrano nell'intervallo tra il punto bianco del supporto e il punto nero. Si supponga che l'immagine sia una fotografia di una scena in cui è presente un bianco diffuso, ad esempio una persona con una ty shirt bianca, e un'evidenziazione speculare, ad esempio una luce che si riflette da una finestra o da un paraurti di colore. Il rendering della scena verrà eseguito sul supporto di input in modo che l'evidenziazione speculare sia mappata al punto bianco del supporto e che il bianco diffuso sia mappato a un colore neutro più scuro rispetto al punto bianco del supporto. La scelta di come eseguire il mapping dei colori dalla scena al supporto di input è sia una decisione dipendente dalla scena che una decisione di tipo fisico. Se l'evidenziazione speculare non è presente nella scena originale, è probabile che il bianco diffuso sia mappato al punto bianco del supporto. In una scena con molti dettagli evidenziati, verrebbe lasciato un intervallo maggiore tra il bianco speculare e il bianco diffuso. In una scena in cui l'evidenziazione non è significativa, potrebbe essere lasciato un intervallo molto piccolo.

Per le immagini con rendering preliminare, il mapping di gamut è relativamente semplice. Fondamentalmente, il punto bianco del supporto originale viene mappato al punto bianco del supporto di riproduzione, il punto nero di origine viene mappato al punto nero di destinazione e la maggior parte del mapping è completo. I diversi gmA esistenti offrono variazioni per il mapping di altri punti sulla scala del tono del supporto di origine e diversi modi per gestire i valori chroma out-of-gamut. Tuttavia, il mapping tra bianco e bianco e nero è coerente in tutte queste varianti. Questa implementazione richiede che il bianco sia sopra una J \* di 50 e il nero sotto una J di \* 50.

Non tutte le codifiche dei colori limitano gli intervalli di colori per le immagini di input. La codifica colori standard IEC scRGB (IEC 61966-2-2) fornisce 16 bit per ognuno dei tre canali di colore rosso, verde e blu (RGB). In tale codifica, il nero di riferimento non viene codificato come triplo RGB (0, 0, 0), ma come (4096, 4096, 4096). Il bianco di riferimento è codificato come (12288, 12288, 12288). La codifica scRGB può essere usata per rappresentare evidenziazioni speculari e dettagli dell'ombreggiatura. Include tripli RGB che non sono fisicamente possibili perché richiedono quantità negative di luce e codifiche esterne al locus spulare CIE. Ovviamente, nessun dispositivo può produrre tutti i colori nella gamma scRGB. In realtà, nessun dispositivo può produrre tutti i colori che un essere umano può vedere. Pertanto, i dispositivi non possono riempire la gamma scRGB e sarebbe utile essere in grado di rappresentare la parte della gamma che riempiono. Ogni dispositivo ha un intervallo di valori nello spazio scRGB che può produrre. Questi sono i colori "previsti" per il dispositivo. Sarebbe sorprendente che il dispositivo produca colori al di fuori di questa gamma. Esiste una trasformazione definita dallo spazio scRGB allo spazio dell'aspetto, quindi ogni dispositivo ha anche una gamma di valori di aspetto che si prevede di riprodurre.

Sia in scRGB che nell'input dei dispositivi di acquisizione caratterizzati da una destinazione fissa, è possibile ottenere un valore non compreso nell'intervallo di valori previsti. Se qualcuno calibra una fotocamera in una destinazione di test; e quindi acquisisce una scena con evidenziazioni speculari. Potrebbero essere presenti pixel più luminosi del punto bianco della destinazione. La stessa cosa può verificarsi se un rosso naturale è più cromatico del rosso di destinazione. Se un utente accetta un'immagine scRGB da un dispositivo e quindi modifica manualmente i colori nell'immagine, è possibile creare pixel che non rientrano nell'intervallo previsto della gamma del dispositivo, anche se si trova all'interno della gamma scRGB completa.

Un secondo problema potrebbe non sembrare all'inizio correlato a questo problema. Si verifica quando si usa una destinazione colore per caratterizzare un dispositivo di input, ad esempio una fotocamera o uno scanner. Le destinazioni riflettenti vengono in genere prodotte su carta e contengono una serie di patch colorate. Le funzionalità forniscono file di dati con misurazioni dei colori adottate in una condizione di visualizzazione fissa per ogni patch di colore. Gli strumenti di profilatura dei colori creano un mapping tra questi valori misurati e i valori restituiti dai sensori di colore nei dispositivi. Il problema è che spesso queste destinazioni di colore non coprono l'intera gamma di valori del dispositivo. Ad esempio, lo scanner o la fotocamera potrebbe restituire un valore (253, 253, 253) per il punto bianco di riferimento e una patch rossa di riferimento potrebbe avere un valore RGB pari a (254, 12, 4). Rappresentano l'intervallo di valori previsti per il dispositivo di input, in base ai valori di destinazione. Se si caratterizza il dispositivo di input in base alle risposte alla destinazione, ci si aspetta solo i colori all'interno di questo intervallo ristretto. Questo intervallo non solo è inferiore all'intervallo di colori che possono essere visualizzati dagli esseri umani, ma è inferiore alla gamma di colori che il dispositivo può produrre.

In entrambi i casi, è difficile stimare la gamma del dispositivo o dell'immagine di input, nonostante l'esistenza di una gamma di riferimento o misurazioni. Nel primo problema, la gamut plausibile del dispositivo di input è inferiore alla gamma completa di scRGB. Nel secondo problema, la gamma di riferimento della destinazione è inferiore alla gamma possibile completa del dispositivo di input.

Il terzo problema riguarda il mapping dei toni. Sono stati proposti molti modelli di limiti di gamut che possono rappresentare in modo adeguato le immagini pre-sottoposte a rendering usate nel disegno grafico, ad esempio, braun e Fairchild Mountain range GBD (Braun 97) e il descrittore di limiti Maxima del segmento di \[ \] Morovic (Morovic \[ 98). \] Ma questi modelli forniscono solo informazioni sugli estremi della gamma del dispositivo; Non sono presenti informazioni su altri punti nel mapping tonale. Senza tali informazioni, gli gma possono solo stimare approssimativamente il mapping dei toni ottimale. In peggiore dei casi, questi modelli non offrono alcuna assistenza per l'intervallo dinamico esteso in scRGB e nelle immagini della fotocamera digitale.

Come viene risolto questo problema nei settori della fotografia e della videografica? La fotocamera acquisisce un'immagine. Gli esperti potrebbero determinare la quantità di rendering eseguita nel dispositivo di acquisizione; ma concordano che non si tratta di una quantità significativa. Entrambe le tecnologie non mappano un bianco diffuso in una scena acquisita al punto bianco del supporto. Analogamente, non mappano il punto nero dalla scena al punto nero del supporto. Il comportamento della filmato illustrativo è descritto nello spazio di densità usando una curva caratteristica, spesso chiamata curva Aferte e Driffield, o curva H&D. La curva mostra la densità della scena originale e la densità risultante nel film. La figura 18 mostra una tipica curva H&D. L'asse x rappresenta un aumento dell'esposizione del log. L'asse y rappresenta la densità sulla diapositiva. Cinque punti di riferimento sono contrassegnati sulla curva: nero senza dettagli, che rappresenta la densità minima sul negativo; nero con dettagli; reference mid-gray card; bianco con dettagli; e bianco senza dettagli. Si noti che c'è spazio tra il nero senza dettagli (che rappresenta il nero del dispositivo) e il nero con dettagli (nero ombreggiato). Analogamente, c'è spazio tra il bianco con dettagli (bianco diffuso) e il bianco senza dettagli (che rappresenta il bianco del dispositivo).

![Diagramma che mostra la curva H e D per la diapositiva.](images/gmmp-image079.png)

**Figura 18:** Curva H&D per la diapositiva

Il settore video fornisce "headroom" e "footroom" nelle immagini. Nella specifica ITU 709 la luminance (denominata Y) viene codificata in 8 bit, con un intervallo compreso tra 0 e 255. Il riferimento nero viene tuttavia codificato a 15 e il bianco di riferimento viene codificato come 235. In questo modo l'intervallo di codifica rimane compreso tra 236 e 255 per rappresentare le evidenziazioni speculari.

Il settore video presenta un sistema a ciclo chiuso essenzialmente chiuso. Anche se esistono molti fornitori di apparecchiature diversi, i sistemi video si basano su dispositivi di riferimento. È disponibile una codifica standard per le immagini video. Non è necessario comunicare un limite di gamut con le immagini video, perché tutte le immagini vengono codificate per la riproduzione nello stesso dispositivo di riferimento. Anche la filmato è a ciclo chiuso perché non è necessario trasmettere dati intermedi tra componenti diversi. Si vuole una soluzione che consenta di riprodurre nell'output le immagini provenienti da dispositivi con varie gamut e che rappresentano scene sia di cui è stato eseguito il pre-rendering che di cui non è stato eseguito il rendering nell'output con gamut variabili.

Un quarto problema che la nuova CTE deve risolvere è che i colori visivamente grigi prodotti da un dispositivo, ad esempio quando red=green=blue su un monitor, spesso non cadono sull'asse neutro della CAM (quando la chroma = 0,0). Ciò causa grandi difficoltà per gli gma. Per fare in modo che gli gma funzionino correttamente, è necessario modificare la descrizione della gamma del dispositivo e dei punti di input in modo che l'asse neutro del dispositivo cada sull'asse neutro dello spazio dell'aspetto. È necessario regolare i punti dall'asse neutro di una quantità simile. In caso contrario, non è possibile eseguire gradazioni uniformi attraverso l'immagine. All'uscita dall'gma, si annulla questo mapping rispetto all'asse neutro del dispositivo di output. Questa operazione viene definita raddrizzamento "chiropratico" dell'asse. Come un chiropratico, non solo si raddrizza lo scheletro (asse neutro), ma si regola il resto del corpo per spostarsi insieme allo scheletro. Come un chiropratico, lo scheletro non viene regolato della stessa quantità nell'intero spazio. È invece possibile modificare diverse sezioni in modo diverso.

![Diagramma che mostra la curvatura dell'asse neutro del dispositivo rispetto all'asse neutro DELLM.](images/gmmp-image081.png)

**Figura 19:** Curvatura dell'asse neutro del dispositivo rispetto all'asse NEUTROM

La nuova CTE richiede un modello di limite gamut che può essere usato per rappresentare immagini di origine di cui è stato eseguito il rendering e non sottoposte a rendering, fornire informazioni sull'aspetto dei neutri del dispositivo e fornire informazioni per le immagini di mapping del tono con un ampio intervallo di luminance.

![Diagramma che mostra le tre shell gamut.](images/gmmp-image083.png)

**Figura 20:** Tre shell gamut

Il limite della gamma è costituito da tre shell che definiscono tre aree.

Nella nuova CTE, la shell esterna della gamma è formata da uno scafo convesso costituito da punti di campionamento nella gamma del dispositivo. Uno scafo viene formato prendendo un set di punti di campionamento e circondandoli da una superficie. Uno scafo convesso ha la proprietà aggiuntiva di essere convesso ovunque. Pertanto, questo non è il più piccolo scafo possibile che può essere adattato ai dati. Tuttavia, la sperimentazione ha dimostrato che l'adattamento troppo stretto dei punti di campionamento causa artefatti poco appetibili nelle immagini, ad esempio la mancanza di ombreggiatura uniforme. Lo scafo convesso sembra risolvere questi problemi.

Nell'algoritmo, i valori di aspetto del colore vengono ottenuti per un set di punti campionati dal dispositivo. Per monitoraggi e stampanti, i valori relativi all'aspetto dei colori vengono ottenuti generando campioni e quindi misurandoli. È anche possibile creare un modello di dispositivo e quindi eseguire dati sintetici tramite il modello di dispositivo per stimare i valori misurati. I valori misurati vengono quindi convertiti dallo spazio colorimetrico (XYZ) allo spazio dell'aspetto (Jab) e lo scafo viene incapsulato intorno ai punti.

Il punto chiave di questo algoritmo è che il punto bianco adottato usato nella conversione dallo spazio colorimetrico allo spazio dell'aspetto non deve essere il punto bianco del supporto. È invece possibile selezionare un punto più lontano all'interno della gamma e sull'asse neutro (o vicino). Tale punto avrà quindi un valore J pari a 100. I campioni con un valore Y misurato superiore al punto bianco adottato finiranno con un valore J maggiore di 100.

Se si posiziona il punto bianco diffuso della scena come punto bianco adottato per la conversione dello spazio colore, le evidenziazioni speculari nella scena verranno facilmente rilevate come con un valore J maggiore di 100.

Poiché il modello a colori DIM02 è basato sul sistema visivo umano, dopo aver selezionato un bianco adottato, il livello di luminanza del punto nero (J = 0) viene determinato automaticamente dal modello. Se l'immagine di input ha un intervallo dinamico ampio, è possibile che siano presenti valori che eseere mappati a valori J minori di zero.

La figura 21 seguente illustra i dispositivi neutri in esecuzione al centro delle gamut plausibili e di riferimento.

![Diagramma che mostra l'asse neutro del dispositivo aggiunto al limite di gamut.](images/gmmp-image085.png)

**Figura 21:** Asse neutro del dispositivo aggiunto al limite gamut

Tutti i mapping di gamut comportano il ritaglio di un intervallo di input in una gamma di output o la compressione della gamma di input per adattarla alla gamma di output. Gli algoritmi più complessi vengono formati tramite la compressione e il ritaglio in direzioni diverse oppure dividendo la gamma in aree diverse e quindi eseguendo il ritaglio o la compressione nelle diverse aree.

La nuova CTE estende questo concetto per supportare le aree di una possibile gamma, una gamut plausibile e una gamma di riferimento e consente agli OGM di mapparle in modi diversi. Inoltre, gli OGM hanno informazioni sull'asse neutro del dispositivo. La discussione seguente illustra come gestire situazioni in cui le gamut plausibili e le gamut di riferimento sono compresse l'una sull'altra.

![Diagramma che mostra la G M A con due descrittori di gamut non compressi.](images/gmmp-image091.png)

**Figura 22:** Gma con due descrittori di gamut non compressi

Questo esempio può essere visualizzato se si esegue il mapping da un dispositivo di input, ad esempio una fotocamera o uno scanner caratterizzato da una destinazione riflettente, allo spazio scRGB. Qui i colori plausibili più chiari del bianco di riferimento sono evidenziazioni speculari. In pratica, la caratterizzazione di una fotocamera con una destinazione potrebbe non generare l'intera gamma di valori possibili nella fotocamera. tuttavia, evidenziazioni speculari e colori molto cromatici trovati in natura. Le destinazioni trasmissive hanno in genere una patch che rappresenta la densità minima possibile sul supporto. Con una destinazione di questo tipo, le evidenziazioni speculari rientrano nell'intervallo della destinazione. Il nero di riferimento per una destinazione riflettente è l'inizio dell'area nera dell'ombreggiatura. Ciò significa che è probabile che nelle ombreggiature siano presenti colori più scuri del nero sulla destinazione. Se l'immagine contiene molti contenuti interessanti in tale area, può essere utile conservare tale variazione tonale.

![Diagramma che mostra la G M A con una gamma di destinazione compressa.](images/gmmp-image095.png)

**Figura 23:** Gma con gamut di destinazione compresso

La figura 23 mostra un possibile algoritmo di mapping di gamut quando la gamma di destinazione fornisce solo l'intervallo dal bianco al nero del dispositivo e non sono presenti colori possibili al di fuori di questa gamma. Ciò è probabile che si verifica per i dispositivi di output tipici, ad esempio le stampanti. I colori possibili vengono mappati al bordo della gamma di destinazione. Ma manca una curva tonale per il dispositivo di output. Il GMA deve selezionare un punto neutro di luminanza inferiore da usare come destinazione di mapping per il bianco di riferimento. Un algoritmo sofisticato può eseguire questa operazione istogrando le leggerezze nell'immagine di origine e vedere quanti rientrano nell'intervallo previsto, ma più leggero del bianco di riferimento. Maggiore è la leggerezza, maggiore è lo spazio necessario nel dispositivo di destinazione tra i punti mappati per le evidenziazioni speculari e il bianco di riferimento. Un algoritmo più semplice potrebbe scegliere una distanza arbitraria rispetto alla scala di leggerezza dal bianco del dispositivo, ad esempio il 5%. Un approccio simile si applica per il mapping del nero massimo e dell'ombreggiatura nera.

Dopo aver generato la curva tono di destinazione, è possibile eseguire il mapping in un metodo simile a quello usato nella figura 23 precedente. Tutti i punti nella curva del tono di destinazione rientrano nella gamma del dispositivo e tutti i punti nel mapping devono rientrare nella gamma del dispositivo.

Se si inverteno le figure a sinistra e a destra e le direzioni delle frecce nella figura 23, è possibile descrivere il caso in cui l'immagine di origine ha solo una gamma di riferimento e le tre gamut del dispositivo di output non sono compresse tra loro. Un esempio di questo potrebbe essere il mapping da un monitoraggio a scRGB. Anche in questo caso, il GMA deve sintetizzare i punti di controllo per i cinque punti sulla curva tonale per l'immagine di origine. Alcuni mapping potrebbero inserire tutti i punti della curva tonale all'interno della gamma di dispositivi scRGB, mentre altri mapping potrebbero usare una maggiore gamma di scRGB mappando il bianco diffuso al bianco di riferimento e consentendo al bianco speculare di eseguire il mapping a un valore più chiaro.

Infine, si ha il caso in cui entrambi i dispositivi hanno solo la gamma di riferimento, ovvero il funzionamento della maggior parte degli algoritmi di mapping della gamma. Per risolvere questo problema, è sufficiente eseguire il rollback agli algoritmi correnti. In alternativa, se si dispone di un modo ragionevole per determinare i cinque punti di riferimento per i dispositivi di origine e di destinazione, è possibile disporre per eseguire il mapping dei punti di riferimento.

Le gamut del dispositivo contengono più dei cinque punti di riferimento sull'asse neutro. Questi rappresentano semplicemente i limiti tra le aree potenziali nell'immagine. Tra ognuno dei punti di riferimento, è possibile usare una delle tecniche di mapping della gamma esistenti. È quindi possibile ritagliare l'intervallo di colori imprevisti e comprimere tutti i colori tra il bianco e il nero previsti oppure ritagliare tutti i colori al di fuori dell'intervallo di riferimento e comprimersi all'interno di tale intervallo. Esistono molte possibilità, che possono essere implementate in diversi OGM. Inoltre, gli OGM possono comprimere e ritagliare in modi diversi. Tutte queste combinazioni sono coperte in questa invenzione.

Finora in questa discussione, la gamma è stata considerata come se fosse solo una funzione del dispositivo in cui l'immagine è stata creata, acquisita o visualizzata. Tuttavia, non esiste alcun motivo per cui tutte le immagini per un dispositivo devono avere la stessa gamma. Gli OGM dipendono dai dati in GBD. Se il descrittore viene modificato tra le immagini, non è possibile che gli OGM lo sappiano. In particolare, se le immagini non hanno evidenziazioni speculari, gli OGM hanno prestazioni migliori se il descrittore di gamut non mostra che sono presenti colori più chiari del bianco diffuso.

Nella nuova architettura CTE è possibile usare più di un gma. L'uso di più OGM non è intrinsecamente definito. Ad esempio, se un dispositivo di acquisizione associa un GMA al suo "aspetto", tende a farlo con una gamma di destinazione "mirata". Lo stesso vale per i dispositivi di output e le gamut di origine "di destinazione". La gamma sRGB è una gamma implicita comunemente mirata. Pertanto, è consigliabile usare un singolo gma, se la prevedibilità è una priorità. Un singolo flusso di lavoro GMA deve essere l'impostazione predefinita per tutti i flussi di lavoro, in particolare i flussi di lavoro consumer e prosumer. Anche se il mapping a gamut per la riproduzione preferita deve essere eseguito una sola volta, in alcuni casi sono inclusi più processi di mapping. Prima di tutto, per la correzione, si esegue un mapping preferito alla gamma del dispositivo di destinazione finale e quindi un rendering colorimetrico alla gamma del dispositivo di correzione. In secondo piano, alcuni tipi di mapping vengono usati per modificare le caratteristiche dell'immagine, ma non sono inclusi per eseguire il mapping a una gamma di dispositivi, ad esempio regolando la curva tonale o la cromaticità. Se vengono usati più gma, l'interfaccia di trasformazione accetta una matrice di mappe gamut associate, cio' mappe gamut inizializzate con una coppia di descrizioni dei limiti di gamut. Quando è presente più di una mappa di gamut, il limite di gamut di input per una mappa di gamut completata deve essere lo stesso del limite di gamut di output del relativo predecessore.

La funzione limite di gamut del dispositivo accetta il motore del modello di dispositivo e i parametri analitici e deriva un limite di gamut del dispositivo a colori descritto come un elenco di vertici ordinato dello scafo convesso della gamma del dispositivo. L'elenco di vertici ordinato viene archiviato in CIEJab. La struttura dell'elenco di vertici ordinato è ottimizzata per l'accelerazione hardware da DirectX. Questo approccio ha molte soluzioni note (cercare "convex hull DirectX" sul Web e ottenere oltre 100 riscontri). C'è anche un riferimento dal 1983 su questo argomento (Teoria della grafica computer e applicazione, "Shiphulls, b-spline surfaces and cadcam" pp. 34-49), con riferimenti relativi dal 1970 al 1982 sull'argomento.

Per calcolare i triangoli nella shell gamut è possibile usare due tecniche diverse. Per altri dispositivi diversi da dispositivi RGB additivi, si calcola uno scafo convesso. È possibile analizzare il supporto dello scafo non convesso per altri dispositivi se si ha accesso diretto a tali dispositivi per convalidare la solidità, le prestazioni e la fedeltà degli algoritmi. Si tratta di un processo noto che non richiede ulteriori descrizioni. La tecnica usata per i dispositivi RGB additivi è descritta di seguito.

GbD diversi presentano vantaggi e svantaggi. La rappresentazione dello scafo convesso garantisce proprietà geometriche di qualità, ad esempio sezioni di tonalità convessa che forniscono un punto di intersezione univoco con un raggio che emana da un punto sull'asse neutro. Anche lo svantaggio della rappresentazione dello scafo convesso è la convessità. È noto che molti dispositivi, in particolare i dispositivi di visualizzazione, hanno gamut che non sono convessi. Se la gamma effettiva devia in modo significativo dal presupposto di convessabilità, la rappresentazione dello scafo convesso sarebbe imprecisa, possibilmente nella misura in cui non rappresenta la realtà.

Dopo aver adottato un GBD che fornisce una rappresentazione ragionevolmente accurata della gamma effettiva, si verificano altri problemi, alcuni a causa del concetto stesso di sezione di tonalità. Esistono almeno due situazioni patologiche. Nella figura 24 seguente, una gamma CRT dà origine a sezioni di tonalità con "isole". Nella figura 25, una gamma di stampanti dà origine a una sezione di tonalità con parte dell'asse neutro mancante. Le sezioni di tonalità patologiche non sono causate da limiti di gamut particolarmente patologici in questi casi. Sono causati dal concetto stesso di sezione di tonalità, perché (a) viene assunto con una tonalità costante e (b) accetta solo una metà del piano che corrisponde all'angolo della tonalità.

![Diagramma che mostra una visualizzazione superiore e una vista laterale del "curving in" nelle sfumature blu.](images/gmmp-image097.jpg)

**Figura 24:** un tipico monitor CRT ha una gamma che mostra particolari "curving in" nelle sfumature blu. Se le sezioni di tonalità vengono prelevate all'interno di questo intervallo di tonalità, è possibile che le isole isolate vengano visualizzate nelle sezioni di tonalità.

![Diagramma di una gamma con un 'gap' nell'asse neutro.](images/gmmp-image099.jpg)

**Figura 25:** una stampante può avere una gamma con "gap" nell'asse neutro. Quando viene presa una sezione di tonalità (che è solo la metà del piano), c'è un "dent" nella parte del limite che è l'asse neutro. Questa operazione può essere difficile da risolvere in modo algoritmico.

Per risolvere queste pathologie, viene proposto un nuovo framework che abbandona il concetto di sezione di tonalità usata come punto di partenza. Il framework usa invece il set di "elementi linea limite" o linee che si trovano sul limite gamut. Non forniscono necessariamente una visualizzazione geometrica coerente come le sezioni di tonalità, ma supportano tutte le operazioni di gamut comuni. Oltre a risolvere i problemi menzionati in precedenza, questo approccio suggerisce anche che la costruzione di sezioni di tonalità, anche quando è possibile, è disdetta dal punto di vista computazionale.

### <a name="triangulation-of-the-gamut-boundary"></a>Triangolazione del limite Gamut

Il punto iniziale è un GBD costituito da una triangolazione del limite di gamut. I metodi noti per la costruzione di GBD forniscono in genere tale triangolazione. Per concretezza, un metodo per costruire GBD per i dispositivi additivi è descritto qui. Questi dispositivi includono monitor (sia basati su CRT che basati su LCD) e proiettori. La geometria semplice del cubo consente di introdurre un normale reticolo sul cubo. Le visi limite del cubo possono essere triangolate in diversi modalità, ad esempio quella illustrata nella figura 26. L'architettura fornisce un modello di dispositivo per il dispositivo in modo che i valori colorimetrici dei punti reticolo possano essere ottenuti in modo algoritmico o che le misurazioni siano state effettuate direttamente per tali punti. L'architettura fornisce anche ILM02, in modo che sia possibile presupporre che i dati di avvio siano già stati mappati nello spazio DELLA SINCRONIZZAZIONEM02. Ogni punto di lattice sulle facce limite del cubo RGB ha quindi un punto corrispondente nello spazio vuoto. Le connessioni dei punti che formano il set di triangoli nello spazio RGB provocano anche un set di triangoli nello spazio Disatteso. Questo set di triangoli forma una triangolazione ragionevole del limite di gamut se (a) il reticolo sul cubo RGB è abbastanza fine e (b) la trasformazione dallo spazio del dispositivo allo spazio colori uniforme è topologicamente ben comportata; ciò significa che esegue il mapping del limite al limite e non trasforma la gamma all'interno in modo che i punti interni diventino punti limite.

![Diagramma che illustra un metodo semplice per triangolare il limite di gamut di un dispositivo con R G B come spazio del dispositivo.](images/gmmp-image100.png)

**Figura 26:** Metodo semplice per triangolare il limite di gamut di un dispositivo con RGB come spazio del dispositivo

### <a name="boundary-line-elements"></a>Elementi linea limite

Il concetto centrale di questo framework è il concetto di elementi linea limite; un set di segmenti di linea che (a) si trovano sul limite di gamut e (b) si trovano su un piano. In questo caso, il piano è un piano di tonalità. Ogni segmento di linea è il risultato dell'intersezione del piano con un triangolo limite gamut. Anche se molti ricercatori hanno usato la costruzione dell'intersezione di un piano con triangoli limite, in genere analizzano la relazione tra questi segmenti di linea e tentano di costruire un oggetto geometrico coerente fuori dai segmenti di linea. Sono stati escociati algoritmi diversi per seguire questi segmenti di linea uno dopo l'altro fino a quando non viene ottenuta un'intera sezione di tonalità e sono stati effettuati molti tentativi per velocizzare il processo di ricerca.

Questo approccio è diverso. Intersecare il piano con i triangoli per ottenere i segmenti di linea. Si considerino quindi questi segmenti di linea come oggetti *concettuali* di base. È necessario analizzare la relazione tra i segmenti di linea. Non è necessario sapere in che modo sono interconnesse tra loro. Questo punto di vista risolve il problema della sezione hue con le isole. Gli approcci noti che tentano di costruire una sezione di tonalità presuppongono che, se uno inizia con un segmento di linea e lo segue al segmento di linea successivo e così via; alla fine riporta al punto iniziale, a quel punto viene costruita un'intera sezione di tonalità. Sfortunatamente, questo approccio potrebbe perdere l'isola (e nello scenario peggiore, il continente). Senza insodettersi nell'ottenere un'immagine geometrica coerente; in altre parole, hue slice, è possibile gestire il problema dell'isola senza problemi. Un'altra differenza importante in questo approccio è che, per velocizzare la costruzione dei segmenti di linea, usa un "filtro triangolo". Il filtro triangolo genera alcuni triangoli che sicuramente non produrranno segmenti di linea che sarebbero utili nell'operazione di gamut corrente. Poiché l'intersezione di un triangolo con il piano è dispendiosa dal punto di vista del calcolo, ciò migliora la velocità. Un effetto collaterale è che non è possibile costruire una sezione di tonalità perché alcuni segmenti di linea non sono presenti a causa del filtro del triangolo.

### <a name="gamut-operation-checkgamut"></a>Operazione Gamut: CheckGamut

L'esempio seguente illustra il funzionamento del framework e come viene eseguito CheckGamut, cio' l'operazione di controllo se un colore è in gamut.

Il framework generale è illustrato nella figura 27 seguente. Sono disponibili vari componenti. I componenti etichettati in corsivo sono componenti che possono essere diversi nell'implementazione a seconda dell'operazione di gamut in questione. Gli altri componenti sono invarianti in tutte le operazioni gamut. Per iniziare, ***Input è*** un set di attributi di colore. Nel caso di CheckGamut, è il colore della query. Nella figura 27 e nella discussione seguente si presuppone che l'angolo della tonalità sia tra gli attributi di colore di input o possa essere ottenuto da essi. Questo è chiaramente il caso se l'input è l'intero punto di colore, in Parentesi o JCh, da cui è quindi possibile calcolare l'angolo della tonalità. Si noti che l'angolo della tonalità è necessario solo perché vengono usati piani di tonalità. A seconda dell'operazione gamut in questione, potrebbe non essere necessario usare il piano di tonalità. Ad esempio, nella costruzione della routine CheckGamut, è possibile usare piani della costante J. Si tratta di una generalità che non verrà usata o discussa ulteriormente; ma potrebbe essere utile ricordare questa flessibilità della metodologia per supportare altre operazioni gamut quando il piano hue potrebbe non essere la scelta migliore.

![Diagramma che mostra il flusso per supportare le operazioni di gamut.](images/gmmp-image112.jpg)

**Figura 27:** Framework per supportare le operazioni gamut

L'angolo della tonalità, ottenuto direttamente dagli input o calcolato dagli input, viene usato per inizializzare il piano di tonalità con etichetta **Full Hue Plane** nella figura. "Full" è evidenziato perché questo è il piano completo, non solo il mezzo piano contenente la tonalità. Il piano completo contiene sia l'angolo di tonalità di input che l'angolo di 180 gradi opposti. La funzionalità chiave del piano tonalità è la funzione Intersect, illustrata nella sottosezione Seguente, Full Hue Plane: Intersect. Si supponga che il GBD sia già stato costruito e che sia disponibile il set di triangoli **limite Gamut.** Intersecare i triangoli che sono sopravvivenzi a **_Triangle Filter_* _ con il piano di tonalità usando Intersect. Il componente Triangle Filter* è etichettato in corsivo, il che significa che il componente varia nell'implementazione _per diverse operazioni di gamut. Il *filtro triangolare* per CheckGamut è illustrato nella sezione Operazione Gamut: CheckGamut (continua). Il risultato dell'intersezione di un triangolo con il piano di tonalità è vuoto o un elemento **linea** limite, ci esempio una coppia di punti distinti. Se il risultato è non vuoto,**_ viene passato a * Line Element Processor , che esegue di nuovo operazioni diverse a seconda dell'operazione gamut. Line Element Processor* aggiorna la struttura dei _dati interni, * Internal Processed **Data**_ , il cui contenuto o layout dipende anche dall'operazione gamut. In genere, i dati interni elaborati* contengono la "risposta" al problema, che viene continuamente aggiornata con ogni nuovo _elemento linea limite trovato. Dopo l'elaborazione di tutti gli elementi linea limite, è stata trovata la risposta. Rimane per accedervi tramite l'adattatore di **output ***_. Poiché il _Internal dati elaborati* è specifico dell'operazione di gamut, anche l'adattatore di *output* è specifico dell'operazione di gamut.

### <a name="full-hue-plane-intersect"></a>Piano Tonalità completa: Interseca

La funzione Intersect calcola l'intersezione del piano di tonalità e di un triangolo. Per quanto semplice, questa funzione è importante per due motivi.

In primo luogo, l'intersezione di ogni bordo del triangolo con il piano potrebbe produrre tre punti di intersezione, una situazione geometricamente impossibile. Il motivo per cui questa situazione può verificarsi nel calcolo è che, quando i calcoli vengono eseguono in virgola mobile, ad esempio in formato IEEE, esistono incertezze, o "disturbo numerico", in ogni passaggio che influiscono sulla conclusione che un bordo interseca il piano. Quando il piano interseca i bordi in una situazione di mancata corrispondenza, i punti di intersezione sono vicini l'uno all'altro e la determinazione se un punto di intersezione si trova all'interno del bordo è casuale. Anche se il rumore nei valori numerici dei punti è ridotto, la conclusione qualitativa che ci sono più di due punti di intersezione è geometricamente impossibile e difficile da gestire correttamente nell'algoritmo.

In secondo momento, questa funzione è nel ciclo critico per ogni bordo di ogni triangolo filtrato, quindi è importante ottimizzarne il più possibile l'efficienza.

Per risolvere il primo problema relativo al disturbo numerico, eseguire i calcoli in numeri interi. Per risolvere il secondo problema di ottimizzazione dell'efficienza, memorizzare nella cache l'attributo più usato di ogni vertice o il "prodotto punto" associato a ogni vertice. Il passaggio di interi è un modo tipico per garantire la coerenza geometrica. L'idea di base è che, se è necessario quantificare, eseguire questa operazione all'inizio. I calcoli successivi possono quindi essere eseguiti in numeri interi e, se i numeri interi sono sufficientemente grandi in modo che non vi sia alcun rischio di overflow, i calcoli possono essere eseguiti con precisione infinita. La funzione di quantizzazione seguente è utile a questo scopo.

ScaleAndTruncate(x) = Parte intera di x \* 10000

Il fattore di scala 10000 indica che il numero a virgola mobile di input ha quattro cifre decimali, abbastanza precise per questa applicazione. A seconda dell'intervallo di valori dello spazio dell'aspetto del colore, si vuole scegliere un tipo integer con bit sufficientemente grandi da contenere i calcoli intermedi. Nella maggior parte degli spazi di aspetto dei colori, l'intervallo di ogni coordinata è compreso nell'intervallo compreso tra -1.000 e 1.000. La coordinata quantizzata ha un valore assoluto massimo possibile pari a 1.000 \* 10.000 = 10.000.000. Come si noterà, la quantità intermedia è un prodotto punto, ovvero una somma di due prodotti di coordinate, quindi ha un valore assoluto massimo possibile pari a \* 2 (10.000.000) CIÒ = 2?10 ₁₄. Il numero di bit necessari è log Â (2?10 ₁₄ ) = 47,51. Una scelta pratica per il tipo Integer è, pertanto, interi a 64 bit.

Per garantire che l'intersecazione di un piano con un triangolo ofchi sempre un set vuoto o un set di due punti, è necessario considerare il triangolo nel suo complesso, non come singoli bordi del triangolo separatamente. Per comprendere la situazione geometrica, considerare le "distanze con segno" dei vertici del triangolo dal piano di tonalità. Non calcolare direttamente queste distanze con segno; calcola invece i prodotti del punto dei vettori di posizione dei vertici con il vettore normale quantizzato al piano. In particolare, durante l'inizializzazione del piano di tonalità, il vettore normale quantizzato viene calcolato come segue.

NormalVector = (ScaleAndTruncate(-sin(hue)), ScaleAndTruncate(cos(hue)))

Si noti che questo vettore è un vettore bidimensionale. È possibile usare un vettore bidimensionale perché il piano di tonalità è verticale, quindi il terzo componente del vettore normale è sempre zero. Inoltre, viene inizializzata una tabella di ricerca di prodotti punto con una voce per ogni vertice dai triangoli limite Gamut e il prodotto punto corrispondente impostato su un valore non valido.

Durante un'operazione di intersecazione del piano di tonalità con un triangolo, viene cercato il prodotto del punto di ogni vertice del triangolo. Se il valore nella tabella di ricerca non è valido, il prodotto punto viene calcolato usando l'espressione seguente.

NormalVector.a \* ScaleAndTruncate(vertex.a) + NormalVector.b \* ScaleAndTruncate(vertex.b)

Anche in questo caso, il componente J del vertice non viene mai usato, perché il vettore normale è orizzontale. Questo prodotto punto viene quindi salvato nella tabella di ricerca in modo che non sia necessario calcolarlo di nuovo se il prodotto del punto del vertice viene sottoposto a query in un secondo momento.

Caching consente di determinare rapidamente se un bordo interseca il piano, dopo la tabulazione dei prodotti punto nella tabella di ricerca, che viene compilata progressivamente durante l'elaborazione dei vertici.

![Diagramma che mostra l'intersezione del piano di tonalità con un triangolo.](images/gmmp-image114.jpg)

**Figura 28:** Intersezione del piano di tonalità con un triangolo

Perché il triangolo nella figura 28 interseci il piano della tonalità in un segmento di linea non degenerato, i prodotti punto dei vertici devono essere in uno dei modelli seguenti, se ordinati in ordine crescente.

0,0,+; -,0,0; -,0,+; -,-,+; -,+,+

Un punto finale del segmento di linea si verifica quando il piano viene intersecato da un bordo con vertici con segni diversi nel prodotto punto. Se il segno è zero, il vertice si trova direttamente sul piano e l'intersezione del bordo con il piano è il vertice stesso. Si noti anche che i case sono 0,0,0; -,-,0; 0,+,+ non vengono segnalati. Il primo caso (0,0,0) indica che l'intero triangolo si trova sul piano. Questo non viene segnalato perché ogni bordo del triangolo deve appartenere a un triangolo adiacente che non si trova interamente sul piano. Il bordo verrà segnalato quando viene considerato tale triangolo. Gli altri due casi (-,-,0 e 0,+,+) corrispondono alla configurazione geometrica in cui il triangolo tocca il piano in un vertice. Questi casi non vengono segnalati perché non danno origine a un segmento di linea non degenerato.

L'algoritmo precedente determina quando calcolare un'intersezione tra un bordo del triangolo e il piano della tonalità. Dopo aver determinato un bordo, l'intersezione viene calcolata usando equazioni parametrici. Se uno dei prodotti punto è zero, l'intersezione è il vertice stesso, quindi non è necessario alcun calcolo. Supponendo che entrambi i prodotti punto dei vertici del bordo siano diversi da  zero, vertex1 è il vertice con il prodotto dotProduct1 negativo; e vertex2 è il vertice con *dot* product dotProduct2 positivo. Questo ordine è importante per garantire che il punto di intersezione calcolato non dipendo dal modo in cui l'ordinamento dei vertici viene visualizzato nella rappresentazione del bordo. Il concetto geometrico del bordo è simmetrico rispetto ai vertici. L'aspetto computazionale dell'uso di equazioni parametriche del bordo introduce l'asimmetria (scelta del vertice iniziale), che può fornire un punto di intersezione leggermente diverso a causa del disturbo numerico e del condizionamento delle equazioni lineari da risolvere. Detto questo, il punto di intersezione, l'intersezione, è dato dal seguente.

t = dotProduct1/(dotProduct1 - dotProduct2)

Intersezione. J = vertice1. J + t \* (vertice2. J - vertice1. J)

intersection.a = vertex1.a + t \* (vertex2.a - vertex1.a)

intersection.b = vertex1.b + t \* (vertex2.b - vertex1.b)

### <a name="gamut-operation-checkgamut-continued"></a>Operazione Gamut: CheckGamut (continua)

L'algoritmo geometrico di base usato per il controllo della gamma è il conteggio del numero di attraversamenti di raggi. Per un determinato punto di query, prendere in considerazione un raggio che inizia con il punto di query e punta verso l'alto (direzione J). Contare il numero di volte in cui questo raggio attraversa il limite della gamma. Se questo numero è pari, il punto di query non è disponibile. Se questo numero è dispari, il punto si trova all'interno. In linea di principio, questo algoritmo può essere implementato in 3D, in genere è afflitto da difficoltà causate da situazioni degenerate, ad esempio il raggio che si trova (in parte) su un triangolo limite o una degenerazione dimensionale inferiore, ad esempio il raggio che si trova (in parte) su un bordo di un triangolo limite. Anche in 2D, è necessario gestire queste situazioni degenerate; ma il problema è più semplice ed è stato risolto in modo soddisfacente. Vedere \[ O'Rourke \] .

Per un determinato punto di input, determinare l'angolo della tonalità h come indicato di seguito.

h = atan(b/a),

Inizializzare il piano di tonalità e quindi determinare gli elementi linea limite corrispondenti a questo piano di tonalità. Poiché gli elementi linea limite sono rilevanti solo se intersecano il raggio verso l'alto, configurare un filtro triangolo per rimuovere i triangoli che forniscono elementi linea che sicuramente non intersecano il raggio verso l'alto. In questo caso, si consideri il rettangolo di selezione del triangolo. Il raggio verso l'alto non interseca il triangolo se il punto di query si trova all'esterno dell'"ombreggiatura" impostata dal rettangolo di selezione se una sorgente di luce si trova direttamente sopra. Gonfiare leggermente questo valore con una tolleranza prefisse per consentire disturbo numerico in modo da non buttare inavvertitamente triangoli che potrebbero fornire elementi di linea utili. Il risultato è il cilindro rettangolare semi-infinito illustrato nella figura 29. Controllare se il punto di query si trova all'interno o all'esterno di questo cilindro può essere implementato in modo efficiente usando diseguaglianze semplici.

![Mostra il filtro triangolo per CheckGamut.](images/gmmp-image116.jpg)

**Figura 29:** Filtro triangolo per CheckGamut

CheckGamut include tre componenti specifici dell'operazione gamut: *Internal Processed Data*, Line Element *Processor* e *Output Adaptor*. I *dati interni elaborati* sono un elenco di elementi riga elaborati da *Processore di elementi riga.* In questo caso, Line *Element Processor* aggiunge semplicemente un elemento line all'elenco. La struttura dei dati interni per *i dati elaborati* interni può essere un elenco collegato o una matrice che può aumentare le dimensioni.

*L'adattatore* di output è un modulo che accede all'elenco di elementi riga, determina se un elemento linea attraversa il raggio verso l'alto (conteggio 1) o meno (conteggio 0). Sommando tutti questi conteggi viene visualizzato un conteggio totale. Output *Adaptor* restituisce infine una risposta "yes" (in-gamut) o "no" (out-of-gamut), a seconda che il conteggio totale sia dispari o pari. Il passaggio in cui si determina se un elemento linea attraversa il raggio verso l'alto merita attenzione perché è qui che si verifica il problema della degenerazione e si verifica anche il problema dell'over counting. Dopo O'Rourke , perché un elemento linea attraversi il raggio, il punto finale \[ destro (l'estremità con una croma più grande) deve essere rigorosamente sul lato destro del \] raggio. Ciò garantisce che, se un punto finale si trova esattamente sul raggio, viene conteggiato una sola volta. La stessa regola risolve anche la situazione degenerata in cui l'elemento linea si trova esattamente sul raggio. Il conteggio per questo elemento riga non viene incrementato.

La figura 30 mostra gli elementi riga risultanti di un gamut di esempio con il punto di query in varie posizioni.

![Diagramma che mostra gli elementi riga risultanti di una gamma di campioni con il punto di query in varie posizioni.](images/gmmp-image118.jpg)

**Figura 30:** Funzionamento di CheckGamut

### <a name="minimum-color-difference-gamut-mapping"></a>Mapping gamut differenza colore minima

Minimum Color Difference Gamut Mapping, MinDEMap, ha una semplice specifica: se un colore è in gamut, non eseguire alcuna operazione. Se un colore è fuori gamma, proiettarlo al punto "più vicino" sul limite della gamma. La parola chiave "nearest" non è ben definita fino a quando non si specifica l'equazione della differenza di colore da usare. In pratica, per semplificare e velocizzare il calcolo, come metrica della differenza di colore viene usata la distanza euclidea dello spazio dell'aspetto colore scelto, o una sua variante. Il vantaggio della metrica euclidea è che è compatibile con il prodotto punto dello spazio, che consente di usare l'algebra lineare. In dettaglio, se nello spazio è definito un "prodotto punto", una distanza può essere definita come radice quadrata del prodotto del punto del vettore di differenza con se stesso. Un prodotto punto può in genere essere definito da una matrice definita positiva 3x3 A.

u?v = u <sub>T</sub> Av

dove il lato destro è la solita moltiplicazione di matrici. Se A è la matrice di identità, viene ripristinato il prodotto punto standard. In pratica, se Jab è lo spazio colore, non si vogliono combinare i componenti, quindi è possibile usare una matrice diagonale diversa dalla matrice di identità. È anche possibile mantenere invariata la scala su a e b in modo che la misura della tonalità venga mantenuta. Una variante utile del prodotto standard euclideo dot è quindi la seguente.

w <sub>J</sub> (componente J dell'utente)(componente J di v) + (componente di v) + (componente di v) + (componente b dell'utente)(componente b di v)

dove w <sub>J</sub> è un numero positivo. Un'altra variazione è consentire a w <sub>J</sub> di variare con il punto di query di input:

w <sub>J\ =</sub> w <sub>J</sub> (queryPoint)

Il risultato finale è una misura di distanza asimmetrica rispetto ai due punti e con pesi relativi diversi sulla leggerezza e la croma o la tonalità quando il punto di query di input varia. Ciò è conforme ad alcune osservazioni sulla percezione del colore umano secondo cui le differenze di colore non vengono ponderate equamente in tutte le dimensioni. È stato rilevato che le persone sono meno sensibili alle differenze di leggerezza rispetto alle differenze di tonalità e croma.

La funzione di peso seguente è utile.

w <sub>J</sub> = k RSI - k ₁ (C - C mₐₓ ) n

dove k rsi = 1, k ₁ = 0,75/(C mₐₓ ) n, C mₐₓ = 100, n = 2 e C è il più piccolo della croma del punto di query e C mₐₓ.

in modo che un peso di 0,25 viene inserito sul termine J quando chroma è zero e un peso pari a 1 quando chroma è 100. La tendenza a mettere meno peso su J quando la croma è piccola e più peso su J quando la croma è grande segue l'utilizzo consigliato per CMC e CIEDE2000.

![Graph che mostra la funzione weight sul componente J della metrica.](images/gmmp-image119.png)

**Figura 31:** Funzione weight sul componente J della metrica

Per l'esempio seguente, usare lo spazio Disassato. È difficile dal punto di vista computazionale cercare tutti i triangoli limite per determinare il punto più vicino nella metrica euclidea. Di seguito è riportato un approccio semplice per rendere questo processo il più efficiente possibile, senza introdurre presupposti aggiuntivi che possono accelerare il processo, ma finiscono anche in una risposta approssimativa. Prima di tutto, è necessario comprendere la procedura geometrica di proiettare un punto sul triangolo specificato. Qui viene fornita una descrizione.

Viene eseguita per la prima volta una proiezione ortogonale sul piano infinito contenente il triangolo. La distanza più breve del punto di query dal piano può essere determinata in due passaggi.

**(a)** Calcolare il vettore normale unità al triangolo.

**(b)** Calcolare il prodotto del punto del vettore normale dell'unità e un vettore formato dal punto di query e da un punto sul triangolo; cio, uno dei relativi vertici. Poiché il vettore normale ha lunghezza unità, il valore assoluto di questo prodotto punto è la distanza del punto di query dal piano.

Il punto proiettato potrebbe non essere la risposta, perché potrebbe trovarsi all'esterno del triangolo. È quindi necessario eseguire prima un controllo. Il calcolo equivale al calcolo delle coordinate barycentriche del punto proiettato rispetto al triangolo. Se il punto proiettato è determinato all'interno del triangolo, è la risposta. In caso contrario, il punto più vicino viene acquisito su uno dei bordi del triangolo. Eseguire una ricerca su ognuno dei tre bordi. Determinare la proiezione del punto di query su un bordo è un processo simile alla proiezione sul triangolo, ma una dimensione in meno. Viene prima calcolata una proiezione ortogonale. Se il punto proiettato si trova sul bordo, è la risposta. In caso contrario, il punto più vicino viene acquisito in uno dei due punti finali. Eseguire una ricerca sui due punti finali; ovvero calcolare la distanza del punto di query da ogni punto di query e confrontare quello più piccolo.

Un esame attento rivela che è presente una ricerca ripetuta quando si attraversano tutti i triangoli perché un bordo è sempre condiviso da due triangoli e un vertice condiviso da almeno tre bordi. Inoltre, non si è molto interessati a trovare il punto più vicino a un particolare triangolo; si è invece interessati a trovare il punto più vicino all'intero limite della gamma. Tuttavia, un particolare triangolo sarebbe quello in cui si ottiene questo risultato. Esistono due strategie che è possibile usare per velocizzare la ricerca.

**Strategia I**. Ogni vertice verrà elaborato al massimo una volta. Ogni edge verrà elaborato al massimo una volta.

**Strategia II**. In qualsiasi punto della ricerca è presente un candidato migliore con la distanza migliore corrispondente. Se è possibile determinare, con un rapido controllo, che un triangolo non è in grado di offrire una distanza migliore, non è necessario continuare ulteriormente il calcolo. Non sono necessari il punto e la distanza più vicini per questo triangolo.

![Diagramma che mostra il flusso del mapping DE minimo.](images/gmmp-image120.png)

**Figura 32:** Schemi minimi di de mapping

La figura 32 mostra il flusso generale della logica per la mappa di gamut MinDEMap. Per un punto di query, viene prima richiamata la funzione CheckGamut. Se il punto è in gamut, la mappa è no-op. Se il punto è fuori gamma, chiamare ProjectPointToBoundary. Passare ora alla figura 33. A questo punto, si presuppone che siano stati calcolati i valori seguenti.

**(a)** Unità del vettore normale a ogni triangolo limite Gamut rispetto al prodotto punto standard.

**(b)** Elenco vertici ed elenco di bordi, oltre all'elenco dei triangoli.

![Diagramma che mostra la routine "ProjectPointToBoundary".](images/gmmp-image122.jpg)

**Figura 33:** Routine ProjectPointToBoundary

Si tratta di un sovraccarico costante e avrebbe un costo minore se vengono eseguite query sufficienti a questo limite di gamma. In genere, questo avviene quando si compila un LUT di trasformazione da un dispositivo a un altro, in cui sono presenti solo due gamut fisse e la trasformazione LUT viene eseguita attraverso punti sulla griglia campionata in modo uniforme. È possibile pre-calcolare i vettori normali rispetto al prodotto punto standard, anche se la nozione di perpendicolare sarà basata sul prodotto punto ponderato, che dipende dal punto di query, come spiegato in precedenza. Il motivo è che un vettore normale rispetto al prodotto punto ponderato può essere ottenuto facilmente dal vettore normale rispetto al prodotto punto standard. Se n ₀ è un vettore normale rispetto al prodotto punto standard,

n = (componente J di n ₀ /w <sub>J</sub>, a-component di n ₀, b-component di n ₀ )

è normale al triangolo rispetto al prodotto punto ponderato. A causa di questa relazione, è comunque utile pre-calcolare n ₀ anche se deve essere regolata in base al punto di query.

La routine ProjectPointToBoundary inizia reimpostando la "cronologia elaborata" dei vertici e dei bordi. Si tratta di tabelle di flag BOOLEAN che rilevano se un vertice o un bordo è stato visitato in precedenza. Reimposta anche la variabile ShortestDistance su "INFINITY", ovvero il valore codificato massimo nel sistema di numeri a virgola mobile usato. Viene quindi eseguito un ciclo, cercando il punto più vicino da ogni triangolo usando la chiamata ProcessTriangle. ProcessTriangle è la routine per aggiornare la variabile ShortestDistance ed è chiaramente nel ciclo critico. Un'ottimizzazione è arrestarsi quando il risultato è sufficientemente positivo. Dopo ogni chiamata a ProcessTriangle, viene esaminata la variabile ShortestDistance. Se soddisfa una soglia predefinita, è possibile arrestarla. La soglia predefinita dipende dalla spazio colore usato e dall'accuratezza richiesta del sistema di creazione delle immagini a colori. Per un'applicazione tipica, non è necessario eseguire operazioni non necessarie se la differenza di colore è inferiore a quella che può essere individuata dalla visione umana. Per ILM02, questa differenza di colore è 1. Usare tuttavia un valore soglia pari a 0,005 nell'implementazione per mantenere la precisione dei calcoli, perché potrebbe trattarsi solo di un passaggio intermedio in una catena di trasformazioni.

ProcessTriangle implementa la strategia II precedente. Ottenendo un vettore normale dal vettore normale dell'unità pre-calcolata al triangolo rispetto al prodotto punto standard, calcola la distanza del punto di query al piano infinito contenente il triangolo formando il prodotto del punto del vettore normale dell'unità e del vettore queryVector, il vettore da uno dei vertici del triangolo,  vertex1, al punto di query, queryPoint.

queryVector = queryPoint - vertex1

distance = \| normalVector \* queryVector \| / \| \| normalVector\|\|

Si tratta di un calcolo relativamente economico e la distanza è necessaria per eseguire ulteriori calcoli. Se questa distanza non è inferiore alla distanza migliore corrente, ShortestDistance, questo triangolo non produrrà una distanza migliore, perché non offrirà una distanza migliore rispetto al piano che lo contiene. In questo caso, si restituisce il controllo al ciclo triangolare. Se la distanza è inferiore a ShortestDistance, potenzialmente si ha un punto più vicino, se questo punto si trova all'interno del triangolo. È necessario eseguire alcuni calcoli "hard" (anche se non oltre l'algebra lineare) per determinarne l'esecuzione. Se gli altri due vertici del triangolo sono vertex2 e vertex3, formare i vettori di base firstBasisVector e secondBasisVector.

firstBasisVector = vertex2 - vertex1

secondBasisVector = vertex3 - vertex1

Usare il sistema lineare di equazioni seguente per risolvere le incognite che si e v.

firstBasisVector \* queryVector = (firstBasisVector \* firstBasisVector)u + (firstBasisVector \* secondBasisVector)v

secondBasisVector \* queryVector = (secondBasisVector \* firstBasisVector)u + (secondBasisVector \* secondBasisVector)v

e le condizioni per il punto proiettato che si trovano all'interno del triangolo sono:

0 ≤ u ≤ 1, 0 ≤ v ≤ 1 e + v ≤ 1

Dopo questo calcolo, se viene determinato che il punto proiettato si trova all'interno del triangolo, è stato trovato un nuovo punto più vicino. la distanza calcolata all'inizio è la nuova distanza più breve. In questo caso, aggiornare le variabili ShortestDistance e ClosestPoint. Se il punto proiettato si trova all'esterno del triangolo, è possibile trovare un punto più vicino su uno dei bordi. È quindi possibile chiamare la routine ProcessEdge su ognuno dei tre bordi.

![Diagramma che mostra il flusso delle routine ProcessEdge e ProcessVertex.](images/gmmp-image124.jpg)

**Figura 34:** Routine ProcessEdge e ProcessVertex

La routine ProcessEdge implementa la strategia I, illustrata nella figura 34. ProcessEdge inizia controllando se il perimetro è stato elaborato in precedenza. In tal caso, non vengono intraprese altre azioni. In caso contrario, procede al calcolo della proiezione ortogonale del punto di query sulla linea infinita contenente il bordo. L'algebra lineare coinvolta nel calcolo è simile alle equazioni triangolo precedenti. Tuttavia, il calcolo è più semplice, non è descritto qui. Se il punto proiettato si trova all'interno del bordo, si trova la distanza del punto proiettato dal punto di query. Se questa distanza è inferiore a ShortestDistance, è stato trovato un nuovo punto più vicino. Aggiornare sia ShortestDistance che ClosestPoint. Se il punto proiettato si trova all'esterno del bordo, chiamare ProcessVertex sui due punti finali. Prima di restituire il controllo, aggiornare la cronologia dei bordi in modo che questo bordo sia contrassegnato come "ELABORATO".

Infine, si assegna una descrizione di ProcessVertex. La routine ProjectVertex implementa anche la strategia I e gestisce una tabella di cronologia dei vertici. Come illustrato nella figura 34, verifica innanzitutto se il vertice è stato elaborato in precedenza. In tal caso, non vengono intraprese altre azioni. In caso contrario, procede al calcolo della distanza del vertice dal punto di query. Se la distanza è inferiore a ShortestDistance, aggiornare sia ShortestDistance che ClosestPoint. Alla fine, aggiorna la cronologia dei vertici in modo che questo vertice sia contrassegnato come "ELABORATO".

Quando il ciclo di controllo esterno ha esaurito tutti i triangoli o è terminato prima che sia stata raggiunta la soglia della differenza di colore, viene eseguito l'accesso alla variabile ClosestPoint. Questo è il risultato di MinDEMap. Il chiamante può anche recuperare ShortestDistance se si è interessati alla distanza del colore mappato dal colore della query.

### <a name="hue-smoothing"></a>Smussamento della tonalità

![Diagramma che mostra due viste principali dell'arrotondamento della tonalità, l'originale nella parte superiore e la tonalità smussata nella parte inferiore.](images/gmmp-image125.png)

**Figura 35:** Smussamento delle tonalità

Si verifica un problema con operazioni vincolate alla tonalità. in altre informazioni, l'operazione considera solo le variabili all'interno di un piano di tonalità. La figura 35 mostra un esempio di gamut che mostra sezioni di tonalità "discontinue" nelle tonalità blu. All'interno di questo intervallo di tonalità, per determinati angoli di tonalità, il limite della gamma è tangente al piano della tonalità. In effetti, ciò causa una modifica nella struttura topologica delle sezioni di tonalità. Nell'esempio illustrato, mentre il piano di tonalità attraversa questo intervallo di tonalità, emerge e si inserirà un'"isola". Questa modifica della topologia causerà la discontinuità delle operazioni specifiche della tonalità. Ad esempio, la cuspide con una tonalità fissa cambierà improvvisamente quando l'angolo della tonalità cambia in questo intervallo.

Esiste un motivo per cui è consigliabile mantenere la tonalità in determinate operazioni. Per risolvere il problema precedente, i triangoli limite gamut originali devono essere "smussati di tonalità". In generale, un arrotondamento della tonalità di un set di triangoli limite Gamut è un set di triangoli in modo che (a) formi il limite di una nuova "gamut", che potrebbe non corrispondere alla gamma effettiva del dispositivo e che contiene la gamma definita dal set originale di triangoli; e (b) i triangoli nel nuovo set sono delimitati dall'essere paralleli ai piani di tonalità.

Un modo pratico per ottenere un set di triangoli smussati di tonalità è prendere lo scafo convesso dei vertici originali. Come illustrato nella figura 35, le sezioni di tonalità dello scafo convesso variano uniformemente nell'intervallo di tonalità problematico senza un cambiamento improvviso della topologia.

### <a name="setting-primaries-and-secondaries-in-the-gamut-boundary-description"></a>Impostazione di primarie e secondarie nella descrizione dei limiti gamut

Alcuni metodi di mapping di gamut, ad esempio HueMap, dipendono dalla posizione dei database primari e secondari del dispositivo. Per i dispositivi additivi, le primarie sono rosse, verdi e blu (R, G e B); e i secondari sono ciano, magenta e giallo (C, M e Y). Per i dispositivi sottrattivi, i valori primari sono C, M e Y. e i database secondari sono R, G e B. GbD tiene traccia di tutti e sei questi valori, più il bianco e il nero (W e K), in una matrice di valori di colore di Jab. Questi valori vengono impostati nella descrizione del limite di gamut al momento della creazione. Per i dispositivi di output, le primarie possono essere determinate eseguendo combinazioni di valori di controllo del dispositivo tramite il modello di dispositivo. Per i dispositivi di acquisizione, questo approccio non è adatto per la creazione del GBD di riferimento, perché è quasi impossibile acquisire un'immagine che restituisce un valore del dispositivo puro completamente saturato, ad esempio (0.0, 0.0, 1.0). I profili di dispositivo WCS contengono gli indici delle primarie nella destinazione di acquisizione. Poiché questi valori non sono contenuti in un profilo ICC, usare i valori misurati da una tipica destinazione dello scanner dopo la conversione in Jab, in relazione alle condizioni di visualizzazione ICC.

### <a name="setting-the-neutral-axis-in-the-gamut-boundary-description"></a>Impostazione dell'asse neutro nella descrizione del limite gamut

I metodi di mapping della gamma HueMap e Relative MinCD usano l'asse neutro del dispositivo per la raddrizzatura. Per i dispositivi di output di base, l'asse neutro può essere determinato eseguendo i valori neutri del dispositivo (R=G=B o C=M=Y) tramite il metodo DeviceToColorimetric e quindi tramite il metodo ColorimetricToAppearance dell'oggetto CIECAM02. Tuttavia, i dispositivi di acquisizione non restituiscono sempre un valore indipendente dal dispositivo quando vengono presentati con un campione neutro. Ciò vale in particolare quando l'illuminazione ambiente non è perfettamente neutra. I profili di dispositivo WCS contengono gli indici degli esempi neutri nella destinazione. Usare questi esempi per impostare l'asse neutro. Poiché queste informazioni non sono disponibili per i profili ICC, è necessario usare lo stesso metodo usato per i dispositivi di output. eseguire esempi indipendenti dal dispositivo tramite il metodo DeviceToColorimetric e quindi accoppiare i valori di input e i risultati colorimetrici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base sulla gestione dei colori](basic-color-management-concepts.md)
</dt> <dt>

[Windows Schemi e algoritmi del sistema di colori](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




