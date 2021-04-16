---
title: Schema e algoritmi del profilo del modello di mappa del programma WCS
description: Schema e algoritmi del profilo del modello di mappa del programma WCS
ms.assetid: 64b9871a-1b4f-4e9a-be4d-4c25b3198b91
keywords:
- Windows Color System (WCS), profilo del modello di mappa gamut (GMMP)
- WCS (sistema di colori Windows), profilo del modello di mappa gamut (GMMP)
- Gestione colori immagine, profilo del modello di mappa gamut (GMMP)
- gestione dei colori, profilo del modello di mappa gamut (GMMP)
- colori, profilo del modello di mappa gamut (GMMP)
- Windows Color System (WCS), profili
- WCS (Windows Color System), profili
- Gestione colori immagine, profili
- gestione dei colori, profili
- colori, profili
- profilo del modello di mappa gamut (GMMP)
- GMMP (Profilo modello di mappa gamut)
- Profilo del modello di mappa della gamma WCS
- schemi, profilo del modello di mappa gamut (GMMP)
- algoritmi, profilo del modello di mappa gamut (GMMP)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714e5d7592cb1fbbbfa98e238642a2fcb38bafd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104554173"
---
# <a name="wcs-gamut-map-model-profile-schema-and-algorithms"></a>Schema e algoritmi del profilo del modello di mappa del programma WCS

-   [Overview](#overview)
-   [Architettura del profilo del modello di mappa gamut](#gamut-map-model-profile-architecture)
-   [Generazione del limite della gamma](#generation-of-the-gamut-boundary)
-   [Schema GMMP](#the-gmmp-schema)
-   [Elementi dello schema GMMP](#the-gmmp-schema-elements)
-   [GamutMapModel](#defaultbaselinegamutmapmodel-type)
    -   [Namespace](#namespace)
    -   [Versione](#version)
    -   [Documentazione](#documentation)
    -   [Tipo DefaultBaselineGamutMapModel](#defaultbaselinegamutmapmodel-type)
    -   [PlugInGamutMapType](#plugingamutmaptype)
    -   [ExtensionType](#extensiontype)
-   [Algoritmi di base di GMMP](#the-gmmp-baseline-algorithms)
-   [Allineamento degli assi neutri](#aligning-the-neutral-axes)
    -   [Differenza colore minima (macinata)](#minimum-color-difference-mincd)
    -   [BasicPhoto](#basicphoto)
    -   [Overview](#overview)
    -   [Il caso della shell della gamma singola](#the-case-of-single-gamut-shell)
    -   [Miglioramento nero](#black-enhancement)
    -   [Il caso di Shell Dual gamut](#the-case-of-dual-gamut-shells)
    -   [Motivi per le modifiche apportate ai consigli CIE TC8-03](#reasons-for-changes-from-the-cie-tc8-03-recommendations)
    -   [Mapping tonalità](#hue-mapping)
-   [Descrizione limite gamut e algoritmi della shell gamut](#gamut-boundary-description-and-gamut-shell-algorithms)
    -   [Triangolazione del limite della gamma](#triangulation-of-the-gamut-boundary)
    -   [Elementi linea limite](#boundary-line-elements)
    -   [Operazione gamut: CheckGamut](#gamut-operation-checkgamut)
    -   [Piano di Hue completo: Intersect](#full-hue-plane-intersect)
    -   [Operazione gamut: CheckGamut (continua)](#gamut-operation-checkgamut-continued)
    -   [Mapping del gamut di differenza colore minimo](#minimum-color-difference-gamut-mapping)
    -   [Smussatura tonalità](#hue-smoothing)
    -   [Impostazione di primari e secondari nella descrizione del limite della gamma](#setting-primaries-and-secondaries-in-the-gamut-boundary-description)
    -   [Impostazione dell'asse neutro nella descrizione del limite della gamut](#setting-the-neutral-axis-in-the-gamut-boundary-description)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

Questo schema viene utilizzato per specificare il contenuto di un profilo del modello di mappa gamut (GMMP). Gli algoritmi di base associati sono descritti nell'argomento seguente.

Lo schema GMMP di base è costituito da informazioni di intestazione comuni, un riferimento facoltativo a un plug-in del modello di mappa gamut preferito e tag di estensione.

Inoltre, GMMP fornisce informazioni esplicite sul modello di mappa del gamut di destinazione e fornisce un criterio sul modello di mappa del gamut di fallback di base da usare se il modello di destinazione non è disponibile. Lo schema può includere informazioni sull'estensione privata, ma non includerà altre informazioni estranee.

## <a name="gamut-map-model-profile-architecture"></a>Architettura del profilo del modello di mappa gamut

![Diagramma che mostra il profilo del modello di mappa gamut.](images/gmmp-image002.png)

Il campionamento dello spazio colorante del dispositivo di output viene eseguito scorrendo i coloranti da 0,0 a 1,0 con un passaggio frazionario, accumulando tutte le combinazioni di ogni colore a ogni passaggio e quindi convertendo tali combinazioni dallo spazio colorante del dispositivo allo spazio di aspetto dei colori utilizzando il metodo DM::D eviceToColorimetricColors seguito dal metodo CAM:: ColorimetricToAppearanceColors. Di seguito è riportato un esempio di come eseguire questa operazione per RGB.


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



## <a name="generation-of-the-gamut-boundary"></a>Generazione del limite della gamma

Sono disponibili tre componenti al limite della gamma: le primarie, gli esempi neutri e le shell. Le primarie vengono generate prendendo le primarie del dispositivo e applicando la trasformazione DeviceToColorimetric/ColorimetricToAppearance. Gli esempi neutri vengono generati eseguendo il campionamento dello spazio colorante del dispositivo nell'area neutra e applicando la stessa trasformazione. Per tre dispositivi colorati (RGB o CMY), gli esempi neutri vengono definiti come aventi tutti i coloranti uguali, ad esempio R = = G = = B. Per CMYK, gli esempi neutri sono definiti con C = = M = = Y = = 0.

I fattori che influenzano i dati usati per creare il limite di gamut sono gli esempi di dati (solo per i dispositivi baseline) e le condizioni di visualizzazione. La dimensione del passaggio utilizzata per eseguire il campionamento completo dello spazio colorato (per i monitoraggi e per la shell plausibile) è una costante interna e non è disponibile per la manipolazione esterna. Se si modificano le condizioni di visualizzazione, il comportamento del modello di aspetto colore (camma) viene modificato e viene modificata la forma del limite della gamma, pertanto è necessario generare un limite di gamut associato al profilo delle condizioni di visualizzazione. Se si usano dati di esempio, come nel caso delle stampanti di base e dei dispositivi di acquisizione, gli esempi avranno un notevole impatto sulla forma della gamma di riferimento e influiscono sul comportamento del modello stesso.

Per i dispositivi di input, ad esempio fotocamere e scanner, vengono usati campionamenti diversi per generare la shell di riferimento e la shell plausibile. La shell di riferimento viene generata dalle misurazioni usate per inizializzare il modello di dispositivo. La shell plausibile viene generata in modo analogo all'illustrazione precedente per i dispositivi di output. La differenza è che quando si importano una destinazione tipica, non si ottengono valori completamente saturi (dove R, G o B = 255). È necessario estrapolare usando il modello di dispositivo per stimare tali valori.

## <a name="the-gmmp-schema"></a>Schema GMMP


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

Questo elemento è una sequenza dei sottoelementi seguenti:

1.  Stringa ProfileName,
2.  DefaultBaselineGamutMapModel,
3.  Stringa di descrizione facoltativa,
4.  Stringa autore facoltativa,
5.  PlugInGamutMap facoltativo e
6.  ExtensionType facoltativo.

**Condizioni di convalida** : ogni sottoelemento viene convalidato in base al relativo tipo.

### <a name="namespace"></a>Spazio dei nomi

xmlns: MGM = " http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel "

### <a name="version"></a>Versione

Versione "1,0" con la prima versione di Windows Vista.

**Condizioni di convalida** : 1,0 in Windows Vista. &lt;Sono inoltre valide le versioni 2,0 per supportare le modifiche non di rilievo nel formato.

### <a name="documentation"></a>Documentazione

Schema del profilo del modello di mappa gamut.

Copyright (C) Microsoft. Tutti i diritti sono riservati.

**Condizioni di convalida** : ogni sottoelemento viene convalidato in base al relativo tipo.

### <a name="defaultbaselinegamutmapmodel-type"></a>Tipo DefaultBaselineGamutMapModel

Tipo UINT

Valori di enumerazione:

<dl> "Totale tritati \_ "  
"MinCd \_ relativa"  
"SIG \_ ginocchio"  
"HueMap"  
</dl>

**Condizioni di convalida** : i valori devono corrispondere a una delle enumerazioni precedenti.

### <a name="plugingamutmaptype"></a>PlugInGamutMapType

Questo elemento è una sequenza di un GUID GUIDType e di tutti gli elementi secondari.

**Condizioni di convalida** : il GUID viene usato per trovare la corrispondenza con il GUID della dll del plug-in MGM. Sono presenti un massimo di 100.000 sottoelementi personalizzati.

### <a name="extensiontype"></a>ExtensionType

Questo elemento è una sequenza facoltativa di qualsiasi sottoelemento.

**Condizioni di convalida** : possono essere presenti al massimo 100.000 sottoelementi.

## <a name="the-gmmp-baseline-algorithms"></a>Algoritmi di base di GMMP

## <a name="aligning-the-neutral-axes"></a>Allineamento degli assi neutri

La maggior parte degli algoritmi di mapping di gamut è in grado di eseguire il mapping dell'asse neutro del dispositivo di origine all'asse neutro del dispositivo di destinazione, ovvero il bianco passa a bianco, da nero a nero e da grigio a grigio. Questo problema viene risolto in parte scalando la luminosità dei colori di origine in modo che corrisponda all'intervallo di luminosità del dispositivo di destinazione. Ma questo non risolve completamente il problema.

Si tratta di una proprietà fisica della maggior parte dei dispositivi di imaging che la cromatità del dispositivo bianco non corrisponde esattamente alla cromaticità del nero del dispositivo. Ad esempio, il monitoraggio del bianco dipende dalla somma delle cromaticità e dalle luminanze relative dei tre primari, mentre il monitor nero dipende dalla riflettenza della superficie di visualizzazione. Il bianco della stampante dipende dalla cromaticità della carta, mentre la stampante nera dipende dall'input penna o dal toner usato. Un modello di aspetto che esegue il mapping del dispositivo bianco esattamente all'asse neutro dello spazio di aspetto (Chroma esattamente uguale a zero) non eseguirà il mapping del dispositivo nero all'asse neutro. Poiché l'occhio è più sensibile alle differenze di croma Man mano che aumenta la luminosità, i grigi sono rappresentati come ancora più cromatici del nero del dispositivo. Nella figura 1 viene illustrata la curvatura degli assi neutri in due dimensioni. Infatti, gli assi neutri formano una curva più complessa in tre dimensioni.

Mentre la camma prevede che questi colori neutri del dispositivo appariranno cromatici, gli osservatori effettivi sembrano compensare. La maggior parte degli utenti non considera questi valori neutri del dispositivo come cromatici. Per la maggior parte dei modelli di mapping di gamut, è pertanto necessario continuare a eseguire il mapping di origini neutre al dispositivo neutro.

Per eseguire il mapping dei dati di origine neutri ai dispositivi neutri, regolare i limiti della gamma di origine e di destinazione e ogni pixel quando si applica l'algoritmo di mapping gamut. Modificare prima di tutto il valore del colore di origine in modo che l'asse neutro del dispositivo di origine alla luce del colore di origine cada direttamente sull'asse neutro dello spazio di aspetto. (Vedere il lato sinistro della figura 1). Modificare quindi la descrizione del limite gamut del dispositivo di destinazione in modo che ogni colore sull'asse neutro del dispositivo di destinazione alla luce del colore del limite della gamma di dispositivi di destinazione cada direttamente sull'asse neutro dello spazio di aspetto. (Vedere il lato destro della figura 1).

![Diagramma che mostra il grafico dei limiti della gamma di origine a sinistra e il limite della gamma di destinazione a destra.](images/gmmp-image004.png)

**Figura 1** : allineamento degli assi neutri illustrati. Left: regolazione dei punti di origine relativi all'asse neutro del dispositivo di origine. Right: regolazione della descrizione del limite della gamma di destinazione rispetto alla descrizione del limite della gamma di destinazione.

Si noti che si regola ogni valore del pixel di origine in relazione all'asse neutro in corrispondenza del valore di luminosità. Ciò assicura che i dispositivi di origine neutri siano ricadenti sull'asse neutro del modello di aspetto. Si spostano anche tutti gli altri colori alla luce della stessa quantità, in modo che non vi siano discontinuità nella rappresentazione del gamut di origine. È necessario passare da importi diversi a livelli di luminosità diversi, perché i valori neutri del dispositivo di origine non sono rappresentati come cromatici allo stesso modo a livelli di luminosità diversi. Ovviamente, non si tratta di una trasformazione semplice.

La gestione dei valori del dispositivo di destinazione è leggermente più complessa. Inizialmente si regola l'intero limite della gamma di destinazione in modo analogo, ma in relazione all'asse neutro del dispositivo di destinazione. Questa operazione è illustrata nella figura 1 sul lato destro. Questa regolazione garantisce che i valori grigio di origine eseguiranno il mapping ai valori grigi di destinazione. Si tratta dello spazio in cui operano gli algoritmi di mapping della gamma.

Tuttavia, questo spazio non descrive in modo accurato il vero comportamento del dispositivo di destinazione. È necessario invertire il mapping prima che i colori con mapping del gamut vengano passati al modello di aspetto e al modello di dispositivo di destinazione. Si sfalsano tutti i valori mappati in base al contrario dell'offset applicato in precedenza all'asse neutro del dispositivo di destinazione. In questo modo viene eseguito il mapping dell'asse neutro di destinazione al valore rappresentato originariamente dalla camma. Esegue la stessa operazione per il limite della gamma e per tutti i valori intermedi.

![Diagramma che mostra un grafico per l'angolazione dell'allineamento dell'asse neutro del dispositivo di destinazione.](images/gmmp-image008.png)

**Figura 2** : angolazione dell'allineamento dell'asse neutro del dispositivo di destinazione

### <a name="minimum-color-difference-mincd"></a>Differenza colore minima (macinata)

Differenze di colore minime (tritate) e relative versioni assolute, equivalenti allo scopo colorimetrico di ICC.

> [!Note]  
> Il MGM tritato è adatto per il mapping di elementi grafici e linee che contengono colori "logo" (colori spot), sfumature di colore del logo con alcuni colori fuori gamma e per la fase finale delle trasformazioni di correzione. Sebbene il MGM tritato possa essere usato per immagini fotografiche completamente incluse nel gamut di destinazione, non è consigliabile per il rendering generale delle immagini fotografiche. Il mapping dei colori out-of-gamut ai colori sulla superficie della gamma di destinazione può comportare artefatti indesiderati, ad esempio irregolarità di tono o Croma in sfumature smussate che superano il limite della gamma. BasicPhoto è consigliato per le immagini fotografiche. Se un'immagine fotografica o contonica richiede un mapping di gamut diverso da BasicPhoto, l'alternativa dovrebbe essere la creazione di un plug-in MGM di implementazione del mapping, anziché l'uso di MinCd.

 

I colori in-gamut rimangono invariati. Per i colori fuori gamma, la luminosità e la cromaticità vengono regolate individuando il punto nella gamma di destinazione che ha la distanza di colore minima dai punti di input fuori dalla gamma. La distanza del colore viene calcolata nello spazio JCh. Tuttavia, si pondera la distanza in chiaro (J) e la distanza in Chroma (C) o Hue (h) in modo diverso. Una funzione di peso dipendente da Chroma viene utilizzata per la distanza in chiaro, in modo che il peso sia minore per la Croma piccola e più grande per la crominanza grande fino a quando non viene raggiunta la croma della soglia, dopo la quale il peso rimane a 1, ovvero lo stesso peso della distanza in Chroma o Hue. Segue l'utilizzo consigliato per CMC e CIEDE2000. Esistono due varianti: colorimetrico relativo e colorimetrico assoluto.

**Colorimetrico relativo:** Allineare innanzitutto gli assi neutri di origine e di destinazione come descritto in precedenza. Quindi ritagliare il colore di origine regolato al limite della gamma di destinazione adattata. (Vedere la figura 4. Chroma mapping lungo la luminosità costante). Modificare i valori del dispositivo di destinazione come descritto in precedenza. Nel caso di un limite di gamut di destinazione monocromatico, il ritaglio Chroma significa che il valore Chroma (C) è impostato su zero (0,0).

**Colorimetrico assoluto:** Questa operazione è simile a colorimetrico relativo, ma senza l'allineamento dell'asse neutro di origine e di destinazione. Il valore di origine viene ritagliato direttamente sull'asse neutro di destinazione. Si noti che se i limiti del gamut di origine e di destinazione sono monocromi, il comportamento è identico alla variante colorimetrico relativa; ovvero viene eseguito l'allineamento degli assi neutri e quindi il Chroma viene troncato a zero. In questo modo si garantisce che un output ragionevole venga raggiunto anche se i supporti e i coloranti sono molto diversi.

![Diagramma che mostra un grafico per il ritaglio tritato alla gamma adattata.](images/gmmp-image010.png)

**Figura 3** : ritaglio tritato alla gamma adattata

### <a name="basicphoto"></a>BasicPhoto

### <a name="overview"></a>Panoramica

BasicPhoto: equivalente all'intento di Preferred, pittorico o percettivo ICC.

Questo algoritmo è una variante del mapping di luminosità sigmoidal che dipende dal Chroma e del ridimensionamento del ginocchio cuspide (SGCK) descritto da CIE TC8-03 in CIE156:2004. Questo algoritmo Variant supporta i descrittori di limite gamut (GBDs) con le shell a doppio gamut; ovvero GBDs con una shell di riferimento e una shell plausibile. L'algoritmo SGCK, che in origine presuppone solo una shell gamut in GBD, si basa sull'algoritmo del \_ ginocchio sig (Braun 1999), che incorpora il mapping della luminosità sigmoidal e il ridimensionamento delle funzioni ginocchio proposto da Braun e Fairchild (1999), combinati con la dipendenza Chroma da GCUSP (Morovic, 1998). Mantiene la costante Hue percepita, ad esempio, l'angolo di tonalità nel jab con correzione per Hue e usa un ridimensionamento della luminosità sigmoidal generico (indipendente dall'immagine) che viene applicato in modo dipendente da Chroma e una funzione del ginocchio del 90%. La variante si ridimensiona lungo le linee della luminosità costante.

### <a name="the-case-of-single-gamut-shell"></a>Il caso della shell della gamma singola

È utile esaminare l'algoritmo nel caso in cui GBDs di origine e di destinazione abbiano solo una shell gamut. In questo caso, l'algoritmo è costituito dai calcoli seguenti.

Eseguire innanzitutto il mapping della luminosità iniziale usando la formula seguente:

![Mostra la formula per il mapping della luminosità iniziale.](images/gmmp-image012.png) (1)

dove *j ₒ* è la luce originale e *j <sub>R</sub>* è la luminosità della riproduzione.

![Mostra la seconda formula di mapping di luminosità.](images/gmmp-image014.png) (2)

Quando il limite della gamma di origine è monocromatico, il valore Chroma sarà zero per il limite monocromatico a causa dell'allineamento dell'asse neutro. Questa operazione comporterà il caso di degenerazione dove C è uguale a zero. In questo caso, *p <sub>C</sub>* viene impostato su 1.

*p <sub>C</sub>* è un fattore di ponderazione dipendente da Chroma (Morovic, 1998) che dipende dal Chroma del colore originale, C e J sono *il <sub></sub>* risultato della luminosità originale di cui viene eseguito il mapping mediante una funzione sigmoidal.

 

Per calcolare *J <sub>S</sub>* (Braun e Fairchild, 1999), una tabella di ricerca unidimensionale (LUT) tra i valori originali e la luminosità della riproduzione viene prima configurata in base a una o più funzioni normali cumulative discrete.

![Mostra una formula per il calcolo di J s.](images/gmmp-image016.png) (3)

dove x ₀ e S sono rispettivamente la media e la deviazione standard della distribuzione normale e *i* = 0, 1, 2... *m*,*m* è il numero di punti usato in LUT. *I <sub></sub> è il* valore della funzione normale cumulativa *per la*  / percentuale *m* . I parametri dipendono dalla luminosità del punto nero del gamut di riproduzione e possono essere interpolati dalla tabella 1. Per informazioni dettagliate sul calcolo di questi parametri, vedere Braun e Fairchild (1999, p. 391).

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
        ₀ x
    :::column-end:::
    :::column:::
       53,7
    :::column-end:::
    :::column:::
        56,8
    :::column-end:::
    :::column:::
        58,2
    :::column-end:::
    :::column:::
        60,6
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


**Tabella 1** : calcolo del parametro di compressione della luminosità BasicPhoto

Per usare S come un mapping di luminosità LUT (S <sub>LUT</sub> ), è necessario prima normalizzarlo nell'intervallo di luminosità di \[ 0100 \] . I dati normalizzati vengono quindi ridimensionati nell'intervallo dinamico del dispositivo di destinazione, come illustrato nell'equazione 4, dove *j*<sub>min \ *out*</sub> e *j*<sub>Max \ *out*</sub> sono i valori della leggerezza del punto nero e il punto bianco del supporto di riproduzione, rispettivamente.

![Mostra la formula per S come LUT di mapping di luminosità.](images/gmmp-image018.png) (4)

A questo punto, è possibile ottenere i valori di *j* dalla <sub>LUT</sub> eseguendo l'interpolazione tra i punti *m* dei corrispondenti *j o '* e *j s* valori in esso contenuti e usando l'equazione seguente come input.

![Mostra la formula per ottenere i valori di J.](images/gmmp-image020.png) (5)

J <sub>Minin</sub> è il valore di luminosità del punto nero del supporto originale, j <sub>Maxin</sub> è il valore di luminosità del punto bianco del supporto originale e j <sub>O</sub> è la luce originale. Per riferimento futuro, è possibile indicare a *S* la funzione sigmoidal definita nel modo appena descritto, come illustrato nella figura 4 riportata di seguito.

![Diagramma che mostra il grafico per il mapping croma lungo la luce costante.](images/gmmp-image024.png)

**Figura 4** : mapping di Chroma lungo la luminosità costante

In secondo luogo, se il limite della gamma di destinazione è cromatico, comprimere Chroma lungo le linee della luminosità costante (l) ed eseguire la compressione come indicato di seguito.

![Mostra la formula per eseguire la compressione Chroma.](images/gmmp-image026.png)  (6)

dove *d* rappresenta la distanza da *E* in *l*; *g* rappresenta il limite della gamma media; *r* rappresenta la riproduzione. e *o* la figura 5 originale.

![Diagramma che mostra il grafico per la compressione Chroma e Light in BasicPhoto.](images/gmmp-image028.png)

**Figura 5** : compressione Chroma e lightity in BasicPhoto

Se il limite della gamma di destinazione è monocromatico, il valore Chroma viene ritagliato a zero.

In terzo luogo, usare un clip tritato (descritto in precedenza) per eliminare eventuali errori residui.

### <a name="black-enhancement"></a>Miglioramento nero

L'algoritmo precedente può essere modificato per migliorare il nero quando la destinazione è un dispositivo di stampa. Il problema ha a che fare con la scelta di *J <sub>minOut</sub>*, che in genere non corrisponde al colore più scuro che una stampante può produrre.

In particolare, il colore con densità più elevata, ottenuto inserendo inchiostri 100% (o massima copertura possibile, se è attiva la limitazione di GCR/Ink), in genere non è "neutral" nello spazio di aspetto dei colori. Vedere la figura 6. In altre parole, se per il dispositivo di destinazione viene usata la luminosità minima neutra, la luce scaler costruita verrà mappata a una leggerezza minima che non è la densità più elevata che può essere conseguita dalla stampante. Considerare il caso di utilizzo ulteriore di monitor per la stampante. Il monitoraggio nero, R = G = B = 0, verrà quindi stampato come non la densità più elevata. L'effetto sulla qualità dell'immagine è la mancanza di profondità e contrasto.

![Diagramma che Mostra come il punto nero del dispositivo potrebbe essere più scuro della luminosità minima neutra.](images/gmmp-seqfigure01.png)

**Figura 6** : il punto nero del dispositivo può essere più scuro della luminosità minima neutra.

Si supponga che il "punto nero del dispositivo" di destinazione sia Jkakbk/JkCkh k. Se C k è diverso da zero, il punto nero del dispositivo non è neutro rispetto a CAM02. Se si usa J k per la "luminosità minima neutra" della destinazione nella costruzione del scaler di luminosità; ovvero impostando

*J <sub>minOut</sub> = JK*

e applicarlo alla shell della gamma di origine, è possibile ottenere la configurazione illustrata nella figura 7. Nella figura il piano Hue corrisponde a h k.

![Diagramma che mostra il ridimensionamento della luminosità modificato con il punto nero del dispositivo di destinazione.](images/gmmp-seqfigure02.png)

**Figura 7** : geometria usando il ridimensionamento della luminosità modificato con il punto nero del dispositivo di destinazione

Per consentire il proseguimento dell'algoritmo di compressione Chroma successivo, è necessario allineare le lightnesses massime e minime nelle shell di origine e di destinazione. Questa operazione può essere eseguita modificando la shell di destinazione tra J <sub>neutralMin</sub> e j k spostando i punti verso sinistra. Inoltre, questa trasformazione deve essere applicata all'intero spazio jab, non solo al piano di tonalità corrispondente a h k.

La trasformazione è

![Mostra la formula per la trasformazione.](images/gmmp-seqfigure03.png)

Nella figura 8 viene illustrato l'effetto della trasformazione.

![Diagramma che illustra l'effetto del ridimensionamento della luminosità modificato con il punto nero del dispositivo di destinazione.](images/gmmp-seqfigure04.png)

**Figura 8** : geometria usando il ridimensionamento della luminosità modificato con il punto nero del dispositivo di destinazione

Dopo aver applicato il consueto algoritmo di compressione Chroma, il punto deve essere "spostato indietro", ovvero è necessario applicare la trasformazione inversa per ottenere il colore finale mappato.

![Mostra la formula per la trasformazione inversa per ottenere il colore finale mappato.](images/gmmp-seqfigure05.png)

### <a name="the-case-of-dual-gamut-shells"></a>Il caso di Shell Dual gamut

L'obiettivo consiste nel generalizzare il \_ ginocchio sig per la shell a gamma singola, nel caso in cui il dispositivo di origine GBD o il dispositivo di destinazione GBD disponga di una struttura a due Shell. La shell interna verrà denominata Shell di riferimento, mentre la shell esterna verrà chiamata Shell plausibile. Si desidera considerare i casi seguenti.

(a) sia la GBD di origine che la GBD di destinazione hanno una struttura a due Shell.

(b) il GBD di origine dispone di una struttura a due Shell. il GBD di destinazione ha una sola Shell.

(c) il GBD di origine ha una sola Shell; la GBD di destinazione ha una struttura a due Shell.

(d) la GBD di origine e la GBD di destinazione hanno solo una shell.

Il caso (d) è il caso di una shell a gamma singola descritta in precedenza. Per i casi (a), (b) e (c), è possibile generalizzare il ridimensionamento della luminosità per usare le informazioni aggiuntive della struttura Dual Shell. Nei casi (b) e (c) in cui l'origine o la destinazione dispone solo di una shell, viene introdotta una "shell di riferimento indotta" che verrà descritta in una sezione successiva, "indotta shell di riferimento". L'algoritmo generale per due Shell verrà descritto per i casi (a). Dopo la spiegazione della costruzione della shell di riferimento indotta, l'algoritmo può essere applicato anche a case (b) e (c). Come per la compressione Chroma, il rapporto di compressione sarà determinato dalle shell più grandi disponibili. In altre parole, se sono disponibili sia la shell plausibile che la shell di riferimento, verrà usata la shell plausibile. in caso contrario, verrà utilizzata la shell di riferimento.

*Ridimensionamento della luminosità generalizzato*

L'esistenza di due Shell per GBD di origine e di destinazione significa che è necessario eseguire il mapping di un set di quattro punti dall'origine GBD a un set corrispondente nel GBD di destinazione.

![Viene illustrato come eseguire il mapping di un set di quattro punti a un set corrispondente.](images/gmmp-image030.png)

Gli indici hanno i significati seguenti.

o o r: "originale" (origine) o "riproduzione" (destinazione)

min o max: luminosità minima neutra o luminosità massima neutra

PLA o Ref: Shell plausibile o Shell di riferimento

L'ordinamento in ogni quadrupla è anche la grandezza relativa prevista di questi punti.

La mappa di ridimensionamento della luminosità usa le stesse prime due equazioni della singola shell, ma *J S* è definito in modo a tratti, come indicato di seguito.

![Mostra la formula per J S in modo a tratti.](images/gmmp-image032.png) (7)

In altre parole, è sigmoidal all'interno della shell di riferimento e lineare all'esterno. Vedere Figura 9.

![Diagramma che mostra un grafico per la funzione di ridimensionamento della luminosità per GBDs a due Shell.](images/gmmp-image033.png)

**Figura 9** : funzione di ridimensionamento della luminosità per GBDs a due Shell

**SHELL DI RIFERIMENTO INDOTTA**

Dove un GBD ha una shell e l'altra GBD ha due Shell, è necessario creare una "shell di riferimento" per il GBD con una sola Shell. La shell esistente, che verrebbe denominata Shell di riferimento, verrà modificata nella "Shell plausibile". In realtà, non è necessario creare una shell nello spazio jab completo. Poiché il ridimensionamento della luminosità usa solo *j max* e *j min*, è necessario costituire solo questi valori per la shell di riferimento indotta. Esistono due casi, a seconda del GBD che dispone di due Shell.

Caso 1: il GBD di origine ha due Shell; GBD di destinazione ha una shell.

Determinare la shell di riferimento indotta dalla destinazione sull'asse neutro; ovvero J <sub>r, \ min, \ Ref</sub> e j <sub>r, \ Max, \ Ref</sub> della shell. Questa operazione viene eseguita utilizzando l'algoritmo seguente.

![Mostra l'algoritmo per determinare la shell di riferimento indotta dalla destinazione.](images/gmmp-induced01.png)

I fattori? <sub>bassa</sub> e? controllo <sub>elevato</sub> della separazione tra la shell plausibile e la shell di riferimento. Il valore 1 indica che i valori J <sub>min</sub> o j m ₐ ₓ coincidono. I valori sono "indotto" dalla shell di riferimento di origine e dalla shell plausibile di origine.

![Mostra la formula per i valori della shell del riferimento di origine e della shell plausibile di origine.](images/gmmp-induced02.png)

I "fattori di fudge" F <sub>low</sub> e f <sub>High</sub> sono *parametri ottimizzabili* che devono essere compresi tra 0 e 1. Se il valore è 0, il valore di J <sub>min</sub> o j m ₐ ₓ viene direttamente indotto dalle shell di origine. Per questo caso, scegliere F <sub>low</sub> = 0,95 e f <sub>High</sub> = 0,1.

Caso 2: l'origine GBD dispone di una shell; GBD di destinazione ha due Shell.

Determinare la shell di riferimento indotta dall'origine sull'asse neutro; ovvero J <sub>o, \ min, \ Ref</sub> e j <sub>o, \ Max, \ Ref</sub> della shell. Questa operazione viene eseguita utilizzando l'algoritmo seguente.

![Mostra l'algoritmo per determinare la shell di riferimento indotta dalla destinazione sull'asse neutro.](images/gmmp-induced03.png)

Anche in questo caso, i fattori? <sub>bassa</sub> e? controllo <sub>elevato</sub> della separazione tra la shell plausibile e la shell di riferimento. Il valore 1 indica che i valori J <sub>min</sub> o j m ₐ ₓ coincidono. I valori sono "indotto" dalla shell di riferimento di origine e dalla shell plausibile di origine:

![Mostra l'algoritmo per controllare la separazione tra la shell di riferimento e la shell plausibile di origine.](images/gmmp-induced04.png)

### <a name="reasons-for-changes-from-the-cie-tc8-03-recommendations"></a>Motivi per le modifiche apportate ai consigli CIE TC8-03

BasicPhoto differisce dalle raccomandazioni CIE TC8-03 nei modi seguenti.

1.  Chroma non viene compresso verso la cuspide ma lungo le linee di luminosità costante.
2.  L'intervallo di luminosità usa la luminosità del colore più scuro nella gamma anziché il punto in corrispondenza del quale il limite della gamut supera l'asse neutro.
3.  BasicPhoto supporta sia una shell gamut di riferimento sia una shell della gamma plausibile, se uno dei limiti della gamma nella trasformazione è costituito da due Shell.
4.  BasicPhoto USA CIECAM02; anziché usare CIECAM97s per eseguire la conversione in D65 a 400 CD/m2, quindi usare lo spazio dei colori RIT IPT.

La prima modifica è stata apportata per evitare problemi di inversione dei toni che possono verificarsi quando si usa la compressione verso un cuspide. Come illustrato nella figura 10, la compressione cuspide può causare inversioni di tono. Questo problema può verificarsi quando i colori della croma alta sono più chiari dei colori della croma inferiore. Poiché SGCK comprime ogni pixel in modo indipendente sia nella luminosità che nel Chroma, non è garantita la conservazione della relazione di luminosità tra i valori dei pixel dopo la compressione. Lo svantaggio noto a questa decisione di comprimere le linee di leggerezza costante è che è possibile soffrire di perdite di Chroma, in particolare nelle aree in cui il limite della gamma di destinazione è molto semplice, come avviene con gialli luminosi.

![Diagramma che mostra l'inversione del tono causata da SGCK.](images/gmmp-toneinversion.png)

**Figura 10** : inversione del tono causata da SGCK

![Mostra un'immagine originale di una teiera.](images/originalteapot.jpg)![Mostra il risultato SGCK dell'immagine della teiera.](images/badteapot.jpg)![Mostra il risultato BasicPhoto dell'immagine della teiera.](images/betterteapot.jpg)

**Figura 11** : immagine originale, risultato SGCK e risultato BasicPhoto

Nella figura 11 è illustrata questa inversione del tono. A sinistra è presente un'immagine originale acquisita da una fotocamera digitale; al centro, immagine riprodotta da SGCK; e a destra, l'immagine riprodotta da BasicPhoto. L'immagine a sinistra si trova nello spazio colore della fotocamera digitale, le immagini al centro e a destra si trovano nello spazio dei colori di uno schermo LCD. Nell'immagine originale la parte superiore della teiera è più scura della parte inferiore, perché la parte inferiore riflette la tovaglia su cui si trova. Nell'immagine SGCK la parte superiore è effettivamente più chiara della parte inferiore, a causa dell'inversione del tono. Inoltre, è difficile vedere gli elementi riflessi nella parte inferiore della teiera. A destra, BasicPhoto ha corretto l'inversione del tono e gli articoli riflessi sono più chiaramente distinguibili.

La seconda modifica è stata apportata per migliorare la riproduzione dei colori quasi neri sulle stampanti in cui il nero nero non rientra direttamente sull'asse CIECAM02 neutro. Nella figura 12 riportata di seguito viene illustrata un'immagine convertita in sRGB; riprodotto per una stampante inkjet RGB con SGCK; e riprodotto per la stessa stampante usando BasicPhoto. L'immagine al centro non usa il nero completo del dispositivo e pertanto manca il contrasto riscontrato nell'originale. Il contrasto viene ripristinato con BasicPhoto.

![Mostra l'immagine originale di un complay.](images/playstructure.jpg)![Mostra l'immagine del gioco riprodotto per una stampante inkjet R G B con SGCK.](images/playstructurebad.jpg)![Mostra l'immagine del gioco riprodotto per una stampante inkjet R G B con BasicPhoto.](images/betterplaystructure.jpg)

**Figura 12** : nero avanzato

La terza modifica è stata apportata per migliorare la riproduzione dei colori per le fotocamere digitali. In particolare nei casi in cui la fotocamera digitale è stata profilata usando una destinazione di riferimento, una descrizione del limite di gamut basata su colori misurati potrebbe non includere tutti i colori che possono essere acquisiti in una scena reale. Anziché ritagliare tutti i colori alla gamma della destinazione dei colori misurata, si consente all'estrapolazione di produrre un limite di gamut plausibile. L'algoritmo BasicPhoto è progettato per supportare un limite di gamut estrapolato.

La quarta modifica è stata apportata perché CIECAM02 funziona bene per il mapping di gamut. Il processo consigliato da TC8-03 per la conversione dei colori del dispositivo in D65 a 400 CD/m2, quindi l'uso dello spazio dei colori del RIT IPT è sia a elevato utilizzo di calcolo che richiede molto tempo.

### <a name="hue-mapping"></a>Mapping tonalità

HueMap è l'equivalente della finalità di saturazione ICC.

Se il limite della gamma di origine o il limite della gamma di destinazione non contiene primari, questo modello viene ripristinato nel modello tritato (relativo) descritto in una sezione precedente. ad esempio, i dispositivi per cui non è possibile determinare gli primari (profili ICC con più di quattro canali) o profili ICC monocromi.

Questo algoritmo regola innanzitutto la tonalità del valore del colore di input. Quindi regola simultaneamente la luminosità e il Chroma, usando un mapping di taglio. Infine, viene ritagliato il valore del colore per assicurarsi che si trovi all'interno di gamut.

Il primo passaggio consiste nel determinare le "ruote Hue". Trovare i valori di JCh per i colori primario e secondario per il dispositivo di origine e di destinazione. Si stanno prendendo in considerazione solo i componenti Hue. In questo modo viene generata una rotellina di tonalità primaria o secondaria con sei punti di colore per ogni dispositivo. (Vedere la figura 13).

![Diagramma che mostra le ruote Hue con sei punti di colore.](images/gmmp-figure12.png)

**Figura 13** : rotelle Hue

È possibile ottenere risultati migliori se l'origine blu primaria non viene ruotata nel database primario blu di destinazione. L'angolo di tonalità primario blu di origine viene invece usato come angolo di tonalità principale blu di destinazione.

Successivamente, eseguire le rotazioni tonalità per ogni colore di input dall'immagine di origine,

a) utilizzando l'angolo di sfumatura del colore di input, determinare la posizione del colore sulla rotellina di tonalità di origine rispetto al colore primario o secondario di due adiacenti. La posizione può essere considerata come una percentuale della distanza tra le primarie. Ad esempio, la tonalità di colore di input è il 40% della strada dal valore di tonalità di Magenta al valore di tonalità di rosso.

b) nella rotellina Hue di destinazione trovare l'angolo di tonalità associato, ad esempio, 40% da Magenta a rosso. Questo valore sarà l'angolo di tonalità di destinazione.

In generale, le primarie e i database secondari di origine non si troveranno sugli stessi angoli di tonalità delle primarie di destinazione e dei database secondari; ovvero, l'angolo di tonalità di destinazione in genere sarà diverso dall'angolo di tonalità di origine.

Si supponga, ad esempio, che le ruote Hue producano i valori seguenti:

Source M = 295 Degrees, source R = 355 Degrees.

Destinazione M = 290 gradi, destinazione R = 346 gradi.

Se l'angolo di tinta del colore di input è 319 gradi, è il 40% dell'angolo (24 gradi) dall'origine M al codice sorgente R. L'angolo da M a R è 60 gradi e l'angolo da M a tonalità di input è di 24 gradi. Calcolare l'angolo sulla destinazione che corrisponde al 40% dalla destinazione M alla destinazione R (22 gradi), quindi l'angolo di tonalità del colore di destinazione è 312 gradi.

Calcolare quindi i punti di riferimento Hue per la tonalità di origine e la tonalità di destinazione. Per calcolare il punto di riferimento Hue per un particolare valore h (Hue), è necessario trovare il valore J (luminosità) e il valore C (Chroma).

-   Trovare il valore J del punto di riferimento tonalità eseguendo l'interpolazione tra i valori J per i punti primari o secondari adiacenti, usando la posizione relativa della tonalità. ad esempio, 40% in questo esempio.
-   Trovare il valore massimo di C a questo valore J e il valore h. È ora disponibile il JCh del punto di riferimento Hue per tale tonalità.

![Diagramma che mostra una foglia tonalità.](images/gmmp-figure13.png)

**Figura 14** : foglia tonalità (visualizzazione di una sezione limite gamut in corrispondenza di una determinata tonalità)

Il passaggio successivo consiste nel calcolare il mapping di taglio per ogni pixel. Prima di tutto, visualizzare una foglia tonalità dalla gamma di origine per l'angolo di tinta del colore di origine e una foglia tonalità dalla gamma di destinazione per l'angolo di tonalità di destinazione calcolato durante la rotazione tonalità. Le foglie di tonalità vengono create eseguendo una "sezione" dalla superficie limite della gamma JCh in corrispondenza di un angolo di tonalità specifico (vedere la figura 14).

Nota: per motivi di ottimizzazione delle prestazioni, le foglie Hue non vengono effettivamente create. vengono descritte e illustrate qui solo a scopo di visualizzazione. Le operazioni vengono eseguite direttamente sulla superficie limite del gamut alla tonalità specificata. Quindi si calcolano i punti di riferimento Hue per determinare il mapping di taglio.

-   Eseguire un ridimensionamento della luminosità per eseguire il mapping dei punti neri e bianchi della foglia di origine alla foglia di destinazione (vedere la figura 15). I punti neri e vuoti della foglia tonalità di origine vengono mappati in modo lineare ai punti neri e bianchi della foglia tonalità di destinazione, ridimensionando tutte le coordinate J del limite di origine. Il valore del colore di input mappato a tonalità viene ridimensionato nello stesso modo.

![Diagramma che mostra il mapping di luminosità.](images/gmmp-figure14.png)

**Figura 15** : mapping della luminosità

-   Determinare i punti di riferimento Hue per ogni foglia tonalità. Applicare un mapping di taglio alla foglia di origine in modo che i punti di riferimento di origine e di destinazione coincidano (vedere la figura 16). Il punto di riferimento per una gamma a una determinata tonalità è il punto di riferimento della tonalità interpolata tra le primarie adiacenti. Il punto di riferimento della foglia tonalità di origine viene mappato in modo lineare al punto di riferimento della foglia tonalità di destinazione, usando un'operazione di "distorsione" che blocca l'asse J, mantenendo i punti neri e i puntini bianchi fissi. I punti neri, i punti bianchi e i punti di riferimento delle foglie di tonalità di origine e di destinazione devono coincidere.
-   Applicare il mapping di taglio al valore del colore di input con regolazione della luminosità. Le coordinate J e C del valore del colore di origine vengono ridimensionate in modo proporzionale rispetto alla distanza dall'asse J.
-   Successivamente, una lieve compressione della luminosità dipendente da Chroma verso il valore J del punto di riferimento Hue viene eseguita sul punto di colore con mapping di taglio. La compressione verso il riferimento Hue J viene eseguita in un modo simile a gamma, dove bianco, nero, grigio e punti sul riferimento tonalità J non sono interessati. Tutti gli altri punti tendono a raggiungere il riferimento di tonalità J in modo uniforme, leggermente raggruppando in prossimità del riferimento Hue J, con la costante Chroma rimanente. La dipendenza Chroma garantisce che i colori neutri non siano interessati e che l'effetto venga aumentato sui colori con Chroma superiore.

Di seguito è riportata una descrizione matematica della compressione della luminosità verso il riferimento di tonalità J o la modifica del valore J del punto di destinazione. Viene chiamato punto di destinazione perché è stato mappato al gamut di destinazione.

Per prima cosa, calcolare "factorC" (fattore di dipendenza Chroma) per il punto di destinazione, che determina la quantità di effetti della compressione della luminosità. I punti vicini o sull'asse J avranno una compressione minima o nulla. i punti più lontani dall'asse J (High-Chroma) avranno una maggiore compressione applicata. Moltiplicare per 0,5 per assicurarsi che factorC sia minore di 1, perché è possibile che sourceC sia leggermente maggiore di referenceC, ma non due volte più grande.

factorC = (destinationC/referenceC)? 0.5

dove:

destinationC è il valore C del punto di destinazione.

referenceC è il valore C del punto di riferimento tonalità.

Determinare quindi se il punto di destinazione J è al di sopra o al di sotto del riferimento di tonalità J. In caso contrario, eseguire le operazioni seguenti:

1.  Calcolare "factorJ" per il punto di destinazione rispetto a referenceJ. Il valore di factorJ sarà compreso tra 0 e 1 (0 se in referenceJ; 1 se in maxJ).
2.  factorJ = (destinationJ-referenceJ)/(maxJ-referenceJ)

    dove:

    destinationJ è il valore J del punto di destinazione.

    referenceJ è il valore J del punto di riferimento tonalità.

    maxJ è il valore J massimo della gamma.

3.  Applicare una funzione di risparmio energia di tipo gamma a factorJ, che ridurrà factorJ di una determinata quantità. Questo esempio usa la potenza di 2 (il quadrato). Sottrarre il factorJ ridotto dalla factorJ originale e moltiplicare il risultato per l'intervallo J totale sopra il referenceJ primario per trovare il "deltaJ", che rappresenta la modifica in J dopo la compressione della luminosità, ma senza includere la dipendenza Chroma.
4.  deltaJ = (factorJ-(factorJ? factorJ)) ? (maxJ - referenceJ)

5.  Applicare factorC al deltaJ (maggiore è la Croma, maggiore sarà l'effetto) e calcolare il nuovo valore J per il punto di destinazione.
6.  destinationJ = destinationJ-(deltaJ? factorC)

Se J-value per il punto di destinazione è inferiore a referenceJ, viene eseguito un calcolo simile ai passaggi precedenti a-C, usando minJ anziché maxJ per trovare l'intervallo in J per calcolare il factorJ e tenendo conto della polarità delle operazioni "sotto" referenceJ.

factorJ = (referenceJ-destinationJ)/(referenceJ-minJ)

deltaJ = (factorJ-(factorJ? factorJ)) ? (referenceJ-minJ)

destinationJ = destinationJ + (deltaJ? factorC)

dove:

minJ è il valore J minimo del gamut.

La crominanza per i punti colore di input viene espansa in modo lineare (se possibile) insieme alla luminosità costante proporzionale al valore di Chroma massimo dei gamut di origine e di destinazione a tale tonalità e luminosità. In combinazione con la precedente compressione della luminosità dipendente dalla Croma, questo consente di mantenere la saturazione perché il mapping di distorsione usando i punti di riferimento a volte causa la sovracompressione del punto di origine in Chroma (vedere la figura 16).

![Diagramma che mostra il mapping di taglio per trovare la corrispondenza con i punti di riferimento tonalità, prima del taglio a sinistra, dopo la distorsione a destra.](images/gmmp-shearmapping.png)

**Figura 16** : mapping di taglio, compressione della luminosità verso il riferimento di Hue J e espansione Chroma

Di seguito è riportata una descrizione matematica del processo di espansione croma o la modifica del valore C del punto di destinazione. Viene chiamato punto di destinazione perché è stato mappato a forbice e la leggerezza è stata compressa nel gamut di destinazione.

1.  Prima del mapping di taglio, determinare sourceExtentC (l'extent Chroma alla luminosità e alla tonalità del punto di origine).
2.  Dopo il mapping di taglio e la compressione della luminosità che trasformano il punto di origine nel punto di destinazione, determinare il destExtentC (l'extent Chroma alla luminosità e la tonalità del punto di destinazione).
3.  Se sourceExtentC è maggiore di destExtentC, non è necessaria alcuna regolazione croma per il punto di destinazione ed è possibile ignorare il passaggio successivo.
4.  Modificare destinationC (croma del punto di destinazione) per adattarlo all'ambito della croma di destinazione in base a questa luminosità e tonalità.
5.  destinationC = destinationC? (destExtentC / sourceExtentC)

    dove:

    destinationC è il punto di destinazione C-value.

    sourceExtentC è il valore C massimo della gamma di origine alla luminosità e alla tonalità del punto di origine.

    destExtentC è il valore C massimo della gamma di destinazione alla luminosità e alla tonalità del punto di destinazione.

Infine, eseguire il ritaglio della distanza di minimo. Se il colore di input con rotazione tonalità, luminosità e con mapping di inclinazione è ancora leggermente esterno al gamut di destinazione, ritagliarlo (spostarlo) al punto più vicino sul limite della gamma di destinazione (vedere la figura 17).

![Diagramma che mostra il ritaglio della distanza minima.](images/gmmp-figure15.png)

**Figura 17** : ritaglio a distanza minima

## <a name="gamut-boundary-description-and-gamut-shell-algorithms"></a>Descrizione limite gamut e algoritmi della shell gamut

La funzione limite gamma dispositivi usa il motore del modello di dispositivo e i parametri analitici per derivare un limite di gamut del dispositivo di colore, descritto come un elenco di vertici indicizzati dello scafo del gamut del dispositivo. Lo scafo viene calcolato in modo diverso a seconda che si stiano utilizzando dispositivi additivi, ad esempio monitoraggi e proiettori, o dispositivi sottrattivi. L'elenco di vertici indicizzati viene archiviato in CIEJab. La struttura dell'elenco di vertici indicizzati è ottimizzata per l'accelerazione hardware da DirectX.

Questo approccio presenta molte soluzioni ben note. Se si cerca "convessa Hull DirectX" sul Web, si ottengono più di 100 riscontri. È ad esempio disponibile un riferimento da 1983 in questo argomento specifico (teoria grafica del computer e applicazione, "Shiphulls, superfici b-spline e CADCAM", pp. 34-49) con riferimenti che risalgono da 1970 a 1982 nell'argomento.

La raccolta di punti può essere determinata da informazioni disponibili esternamente, come indicato di seguito:

-   I punti per la shell di riferimento per i monitoraggi vengono generati utilizzando un campionamento del cubo colori nello spazio di colore del dispositivo.
-   I punti per la shell di riferimento per le stampanti e i dispositivi di acquisizione vengono ottenuti dai dati di esempio utilizzati per inizializzare il modello.
-   I punti per la shell di riferimento per scRGB e sRGB vengono generati utilizzando un campionamento del cubo di colore per sRGB.
-   I punti per la shell plausibile per i dispositivi di acquisizione vengono generati usando un campionamento del cubo di colori nello spazio di colore del dispositivo.
-   I punti per la shell di riferimento per i proiettori vengono generati usando un campionamento di un poliedro nel cubo dei colori nello spazio colorante del dispositivo.
-   I punti per la shell possibile per gli spazi dei colori a intervalli dinamici estesi vengono generati utilizzando un campionamento del cubo di colori nello spazio stesso.

È possibile creare un elenco di vertici che descrive in modo efficiente la gamma di colori dei dispositivi, dato un profilo di dispositivo e servizi di supporto del sistema.

Per i dispositivi di output, il limite della gamma descrive l'intervallo di colori che possono essere visualizzati dal dispositivo. Un limite di gamut viene generato dagli stessi dati usati per modellare il comportamento del dispositivo. Dal punto di vista concettuale, viene restituito un campionamento dell'intervallo di colori che il dispositivo può produrre, misurare i colori, convertire le misurazioni in spazio di aspetto e quindi usare i risultati per creare il limite della gamma.

I dispositivi di input sono più complicati. Ogni pixel in un'immagine di input deve avere un valore. Ogni pixel deve essere in grado di rappresentare in qualche modo qualsiasi colore trovato nel mondo reale. In questo senso, nessun colore è "fuori gamma" per un dispositivo di input, perché è sempre possibile rappresentarli.

Tutti i formati di immagine digitale hanno un intervallo dinamico fisso. A causa di questa limitazione, sono sempre presenti alcuni stimoli distinti che si mappano allo stesso valore digitale. Non è quindi possibile stabilire un mapping uno-a-uno tra i colori reali e i valori delle fotocamere digitali. Al contrario, il limite della gamma è formato dalla stima di un intervallo di colori reali che può produrre le risposte digitali della fotocamera. Si usa tale intervallo stimato come gamut per il dispositivo di input.

Sono incluse le primarie per fornire il mapping del gamut dei tipi di business graphics.

In uno stile orientato a oggetti reale si estrae la rappresentazione sottostante del limite della gamma. In questo modo è possibile modificare la rappresentazione in futuro. Per comprendere il descrittore di limite gamut (GBD) usato nella nuova CTE, è necessario innanzitutto comprendere il funzionamento degli algoritmi di mapping di gamut (GMAs). Tradizionalmente, GMAs è stato progettato per soddisfare le esigenze della community grafica. ovvero per riprodurre le immagini che sono già state visualizzate correttamente per il dispositivo in cui è stata creata l'immagine di input. L'obiettivo di Graphic Arts GMAs è quello di eseguire la migliore riproduzione possibile dell'immagine di input nel dispositivo di output. La nuova CTE GBD è progettata per risolvere quattro problemi principali.

Poiché viene eseguito il rendering dell'immagine di input per il dispositivo di input, tutti i colori rientrano nell'intervallo tra il punto bianco e il punto nero del supporto. Si supponga che l'immagine sia una fotografia di una scena in cui è presente un bianco diffuso, ad esempio una persona in una maglietta bianca, e un'evidenziazione speculare, ad esempio la luce che riflette una finestra o un paraurti di Chrome. Verrà eseguito il rendering della scena sul supporto di input in modo che l'evidenziazione speculare venga mappata al punto bianco del supporto e che il bianco diffuso sia mappato a un colore neutro scuro rispetto al punto bianco del supporto. La scelta di eseguire il mapping dei colori dalla scena al supporto di input è una decisione dipendente dalla scena e una decisione estetica. Se l'evidenziazione speculare non era presente nella scena originale, il bianco diffuso verrebbe probabilmente mappato al punto bianco del supporto. In una scena con una grande quantità di dettagli, viene lasciato un intervallo superiore tra il bianco speculare e il bianco diffuso. In una scena in cui l'evidenziazione non è significativa, potrebbe essere lasciato un intervallo molto ridotto.

Per le immagini pre-renderizzate, il mapping di gamut è relativamente semplice. Fondamentalmente, il punto bianco originale del supporto viene mappato al punto bianco del supporto di riproduzione, il punto nero di origine viene mappato al punto nero di destinazione e la maggior parte del mapping è completa. I diversi GMAs in esistenza forniscono varianti per eseguire il mapping di altri punti sulla scala dei toni del supporto di origine e modi diversi per gestire i valori cromatici fuori gamma. Tuttavia, il mapping tra il bianco e il bianco e il nero a nero è coerente in tutte le varianti. Questa implementazione richiede che il bianco sia superiore a J \* di 50 e nero sotto un j \* di 50.

Non tutte le codifiche dei colori limitano gli intervalli di colori per le immagini di input. La codifica dei colori standard IEC (IEC 61966-2-2) fornisce 16 bit per ognuno dei tre canali di colore rosso, verde e blu (RGB). In tale codifica, il riferimento nero non è codificato come triple RGB (0, 0, 0), ma come (4096, 4096, 4096). Il riferimento bianco è codificato come (12288, 12288, 12288). La codifica scRGB può essere utilizzata per rappresentare le evidenziazioni speculari e i dettagli dell'ombreggiatura. Include triple RGB che non sono fisicamente possibili perché richiedono quantità di luce negative e codifiche esterne al locus spettrale CIE. Ovviamente, nessun dispositivo può produrre tutti i colori nella gamma di scRGB. In realtà, nessun dispositivo può produrre tutti i colori che possono essere visualizzati da un uomo. Quindi, i dispositivi non possono riempire la gamma di scRGB e sarebbe utile poter rappresentare la parte della gamma che riempiono. Ogni dispositivo ha un intervallo di valori nello spazio scRGB che può produrre. Questi sono i colori "previsti" per il dispositivo; sarebbe sorprendente per il dispositivo produrre colori al di fuori di questa gamma. Esiste una trasformazione definita dallo spazio scRGB allo spazio di aspetto, quindi ogni dispositivo dispone anche di un intervallo di valori di aspetto che dovrebbe essere riprodotto.

In scRGB e input da dispositivi di acquisizione caratterizzati da una destinazione fissa, è possibile ottenere un valore non compreso nell'intervallo dei valori previsti. Se un utente calibra una fotocamera a una destinazione di test; quindi acquisisce una scena con evidenziazioni speculari. potrebbero essere presenti pixel più luminosi rispetto al punto bianco della destinazione. La stessa cosa può verificarsi se un rosso naturale è più cromatico rispetto a quello rosso di destinazione. Se un utente accetta un'immagine di scRGB da un dispositivo e quindi modifica manualmente i colori nell'immagine, è possibile creare pixel che non rientrano nell'intervallo previsto del gamut del dispositivo, anche se si trovano all'interno del gamut completo di scRGB.

In primo luogo, un secondo problema potrebbe non essere correlato a questo. Si verifica quando si usa una destinazione dei colori per caratterizzare un dispositivo di input, ad esempio una fotocamera o uno scanner. Gli obiettivi riflessivi vengono in genere prodotti su carta e contengono numerose patch colorate. Manufaturers fornisce i file di dati con misurazioni colore eseguite in una condizione di visualizzazione fissa per ogni patch di colore. Gli strumenti di profilatura dei colori creano un mapping tra questi valori misurati e i valori restituiti dai sensori di colore nei dispositivi. Il problema è che spesso queste destinazioni dei colori non coprono l'intera gamma di valori del dispositivo. Ad esempio, lo scanner o la fotocamera potrebbe restituire un valore (253, 253, 253) per il punto bianco di riferimento e una patch rossa di riferimento potrebbe avere un valore RGB pari a (254, 12, 4). Rappresentano l'intervallo di valori previsti per il dispositivo di input, in base ai valori di destinazione. Se si caratterizza il dispositivo di input in base alle risposte alla destinazione, si prevede che i colori si trovino solo all'interno di questo intervallo limitato. Questo intervallo non solo è inferiore all'intervallo di colori che può essere visualizzato dagli utenti, è più piccolo dell'intervallo di colori che il dispositivo può produrre.

In entrambi i casi, è difficile stimare la gamma del dispositivo o dell'immagine di input, nonostante l'esistenza di un gamut o misurazioni di riferimento. Nel primo problema, la gamma plausibile del dispositivo di input è inferiore alla gamma completa di scRGB. Nel secondo problema la gamma di riferimento della destinazione è inferiore alla gamma completa possibile del dispositivo di input.

Il terzo problema riguarda il mapping dei toni. Molti modelli di limiti di gamut che possono rappresentare in modo adeguato le immagini di cui è stato eseguito il rendering usati negli arti grafici sono stati proposti, ad esempio, Braun e Fairchild Mountain Range GBD (Braun \[ 97 \] ) e il descrittore di limite di Morovic segmento Maxima (Morovic \[ 98 \] ). Tuttavia, questi modelli forniscono solo informazioni sugli estremi del gamut del dispositivo. non sono disponibili informazioni su altri punti nel mapping tonale. Senza tali informazioni, GMAs è in grado di eseguire stime approssimative del mapping dei toni ottimali. Peggiori, questi modelli non forniscono alcuna guida per l'intervallo dinamico esteso in scRGB e nelle immagini della fotocamera digitale.

In che modo questo problema è risolto nei settori fotografici e videografica? La fotocamera acquisisce un'immagine. Gli esperti potrebbero discutere della quantità di rendering eseguita nel dispositivo di acquisizione. ma accettano che non si tratta di un importo significativo. Entrambe le tecnologie non eseguono il mapping di un bianco diffuso in una scena acquisita al punto bianco del supporto. Analogamente, non eseguono il mapping del punto nero dalla scena al punto nero del supporto. Il comportamento di un film fotografico viene descritto in spazio di densità usando una curva caratteristica, spesso denominata "Hurt" e "Driffield" o la curva H&D. La curva mostra la densità della scena originale e la densità risultante sul film. Nella figura 18 viene illustrata una tipica curva H&D. L'asse x rappresenta un aumento dell'esposizione dei log. L'asse y rappresenta la densità della diapositiva. Cinque punti di riferimento sono contrassegnati sulla curva: nero senza dettagli, che rappresenta la densità minima sul valore negativo. nero con dettaglio; riferimento alla scheda a metà grigio; bianco con dettaglio; e bianco senza dettagli. Si noti che c'è uno spazio tra il nero senza dettagli (che rappresenta il nero del dispositivo) e il nero con dettagli (nero scuro). Analogamente, c'è uno spazio tra il bianco e il dettaglio (il bianco diffuso) e il bianco senza dettagli, che rappresenta il bianco del dispositivo.

![Diagramma che mostra la curva H e D per la pellicola della diapositiva.](images/gmmp-image079.png)

**Figura 18** : curva H&D per la pellicola della diapositiva

Il settore video fornisce "capacità" e "footroom" nelle immagini. Nella specifica ITU 709, la luminanza (denominata Y) viene codificata in 8 bit, con un intervallo compreso tra 0 e 255. Tuttavia, il nero di riferimento è codificato a 15 e il riferimento bianco è codificato come 235. Questa operazione lascia l'intervallo di codifica compreso tra 236 e 255 per rappresentare le evidenziazioni speculari.

Il settore video presenta un sistema di ciclo essenzialmente chiuso. Sebbene ci siano molti fornitori di apparecchiature diversi, i sistemi video si basano sui dispositivi di riferimento. Per le immagini video è disponibile una codifica standard. Non è necessario comunicare un limite di gamut con le immagini video, perché tutte le immagini sono codificate per la riproduzione nello stesso dispositivo di riferimento. Il film è anche un ciclo chiuso perché non è necessario trasferire i dati intermedi tra i diversi componenti. Si vuole una soluzione che consenta di creare immagini da dispositivi con gamme diverse e di rappresentare sia le scene pre-renderizzate che quelle non sottoposte a rendering da riprodurre nell'output con gamme diverse.

Un quarto problema che deve essere risolto dalla nuova CTE è che i colori visivi in grigio prodotti da un dispositivo, ad esempio, quando rosso = verde = blu su un monitor, spesso non rientrano nell'asse neutro della camma (quando Chroma = 0,0). Ciò causa grandi difficoltà per GMAs. Per fare in modo che GMAs funzioni correttamente, è necessario modificare la descrizione del gamut del dispositivo e dei punti di input in modo che l'asse neutro del dispositivo cada sull'asse neutro dello spazio aspetto. È necessario modificare i punti dall'asse neutro di un importo simile. In caso contrario, non è possibile eseguire gradazioni uniformi tramite l'immagine. All'esterno della GMA, questo mapping viene annullato rispetto all'asse neutro del dispositivo di output. Questa operazione viene definita "Chiropratica" di raddrizzamento dell'asse. Come un chiropratico, non solo si raddrizza la Skeleton (asse neutro), ma si regola il resto del corpo per spostarsi insieme alla Skeleton. Analogamente a un chiropratico, la struttura non viene modificata in base alla stessa quantità nell'intero spazio. Al contrario, si modificano le diverse sezioni in modo diverso.

![Diagramma che mostra la curvatura dell'asse neutro del dispositivo rispetto all'asse neutro CIECAM.](images/gmmp-image081.png)

**Figura 19:** Curvatura dell'asse neutro del dispositivo rispetto all'asse neutro CIECAM

La nuova CTE richiede un modello di limite di gamut che può essere usato per rappresentare le immagini di origine sottoposte a rendering e non sottoposte a rendering, fornire informazioni sull'aspetto dei dispositivi neutri e fornire informazioni per le immagini di mapping del tono con un intervallo di luminanza ampio.

![Diagramma che mostra le tre Shell della gamma.](images/gmmp-image083.png)

**Figura 20** : tre shell di gamut

Il limite della gamma è costituito da tre Shell che definiscono tre aree.

Nella nuova CTE la shell esterna della gamma viene formata con una struttura convessa eseguita da punti di esempio nel gamut del dispositivo. Uno scafo è costituito da un set di punti di esempio che li circonda da una superficie. Una struttura convessa ha la proprietà aggiuntiva di essere convessa ovunque. Non si tratta quindi dello scafo più piccolo possibile che può essere adattato ai dati. Tuttavia, la sperimentazione ha dimostrato che l'adattamento dei punti di esempio causa troppe complicazioni negli artefatti delle immagini, ad esempio la mancanza di ombreggiatura uniforme. Il guscio convesso sembra risolvere questi problemi.

Nell'algoritmo vengono ottenuti i valori di aspetto dei colori per un set di punti campionati dal dispositivo. Per i monitoraggi e le stampanti, i valori relativi all'aspetto dei colori vengono ottenuti tramite l'output degli esempi e quindi la relativa misurazione. È anche possibile creare un modello di dispositivo, quindi eseguire dati sintetici tramite il modello di dispositivo per stimare i valori misurati. I valori misurati vengono quindi convertiti da spazio colorimetrico (XYZ) a spazio aspetto (jab) e la struttura viene avvolta intorno ai punti.

Il punto chiave di questo algoritmo è che il punto bianco adottato usato nella conversione da colorimetrico a spazio aspetto non deve essere il punto bianco del supporto. In alternativa, è possibile selezionare un punto più a lungo all'interno della gamut e, in alternativa, l'asse neutro. Tale punto avrà quindi un valore J pari a 100. Gli esempi con un valore Y misurato superiore al punto bianco adottato finiranno con un valore J maggiore di 100.

Se si posiziona il punto bianco diffuso della scena come punto bianco adottato per la conversione dello spazio colore, le evidenziazioni speculari nella scena saranno facilmente rilevate come se avessero un valore J maggiore di 100.

Poiché il modello di colore CIECAM02 è basato sul sistema visivo umano, dopo che è stato selezionato un bianco adottato, il livello di luminanza del punto nero (J = 0) viene determinato automaticamente dal modello. Se l'immagine di input ha un intervallo dinamico ampio, è possibile che siano presenti valori che vengono mappati a J-valori minori di zero.

Nella figura 21 riportata di seguito vengono illustrati i dispositivi neutri in esecuzione al centro delle gamme plausibili e di riferimento.

![Diagramma che mostra l'asse del dispositivo neutro aggiunto al limite della gamma.](images/gmmp-image085.png)

**Figura 21** : asse neutro del dispositivo aggiunto al limite della gamma

Tutti i mapping di gamut coinvolgono il ritaglio di un intervallo di input in un gamut di output o la compressione del gamut di input per adattarlo all'interno del gamut di output. Algoritmi più complessi sono formati da comprimere e ritagliare in direzioni diverse oppure dividendo la gamma in aree diverse e quindi eseguendo il ritaglio o la compressione nelle diverse aree.

La nuova CTE estende questo concetto per supportare le aree di una possibile gamma, una gamma plausibile e una gamma di riferimento e consente a GMAs di eseguire il mapping in modi diversi. Inoltre, i GMAs includono informazioni sull'asse neutro del dispositivo. Nella discussione seguente viene illustrato come gestire le situazioni in cui le gamme plausibili e le gamme di riferimento sono state compresse l'una sull'altra.

![Diagramma che mostra la G M A con due descrittori di gamut non compressi.](images/gmmp-image091.png)

**Figura 22** : GMA con due descrittori di gamut non compressi

Questo esempio può essere visualizzato se si esegue il mapping da un dispositivo di input, ad esempio una fotocamera o uno scanner caratterizzato da una destinazione riflettente, allo spazio scRGB. Di seguito sono riportati i colori plausibili più chiari rispetto a quelli di riferimento bianco. In pratica, la caratterizzazione di una fotocamera con una destinazione potrebbe non generare l'intera gamma di valori possibili nella fotocamera; Tuttavia, le evidenziazioni speculari e i colori molto cromatici rilevati in natura. (Le destinazioni di trasmissione in genere hanno una patch che è la densità minima possibile sul supporto. Con tale destinazione, le evidenziazioni speculari rientrano nell'intervallo della destinazione. Il nero di riferimento per una destinazione riflessiva è l'inizio dell'area nera Shadow. Ovvero, è probabile che siano presenti colori nelle ombre più scure del nero sulla destinazione. Se l'immagine contiene una grande quantità di contenuto interessante in tale area, potrebbe essere utile mantenere la variazione tonale.

![Diagramma che mostra il G M A con un gamut di destinazione compresso.](images/gmmp-image095.png)

**Figura 23** : GMA con gamut di destinazione compresso

La figura 23 Mostra un algoritmo di mapping di gamut possibile quando il gamut di destinazione fornisce solo l'intervallo dal dispositivo bianco al nero e non vi sono colori possibili al di fuori di questa gamma. Questo problema si verifica probabilmente per i dispositivi di output tipici, ad esempio le stampanti. I colori possibili sono mappati al bordo del gamut di destinazione. Ma non dispone di una curva di tono per il dispositivo di output. Il GMA deve selezionare un punto neutro della luminanza inferiore da usare come destinazione del mapping per il bianco di riferimento. Un algoritmo sofisticato può eseguire questa operazione histogramming lightnesses nell'immagine di origine e visualizzare il numero di rientri nell'intervallo di previsto ma più chiaro del bianco di riferimento. Maggiore è il numero di lightnesses, maggiore è il numero di spazio necessario nel dispositivo di destinazione tra i punti di mapping per le evidenziazioni speculari e il bianco di riferimento. Un algoritmo più semplice può scegliere una distanza arbitraria dalla scala di luminosità del dispositivo bianco, ad esempio il 5%. Un approccio simile è valido per il mapping del nero massimo e nero ombreggiato.

Dopo aver generato la curva di tono di destinazione, è possibile eseguire il mapping in un metodo simile a quello usato nella figura 23 precedente. Tutti i punti nella curva di tono di destinazione rientrano nel gamut del dispositivo e tutti i punti nel mapping devono rientrare nel gamut del dispositivo.

Se si invertono le figure a sinistra e a destra e le direzioni delle frecce nella figura 23, è possibile descrivere il caso in cui l'immagine di origine dispone solo di una gamma di riferimento e le tre gamme del dispositivo di output non sono state compresse l'una sull'altra. Un esempio potrebbe essere il mapping da un monitoraggio a scRGB. Anche in questo caso, la GMA deve sintetizzare i punti di controllo per i cinque punti sulla curva di tono per l'immagine di origine. Alcuni mapping potrebbero inserire tutti i punti della curva di tono all'interno del gamut del dispositivo scRGB, mentre altri mapping potrebbero utilizzare più della gamut di scRGB eseguendo il mapping tra il bianco e il bianco di riferimento e consentendo al bianco speculare di eseguire il mapping a un valore più chiaro.

Infine, si ha il caso in cui entrambi i dispositivi hanno solo la gamma di riferimento, ovvero la maggior parte degli algoritmi di mapping di gamut. Per risolvere questo problema, è possibile eseguire il fallback solo sugli algoritmi correnti. In alternativa, se si dispone di un modo ragionevole per determinare i cinque punti di riferimento per i dispositivi di origine e di destinazione, è possibile disporre di per eseguire il mapping dei punti di riferimento.

Le gamme di dispositivi contengono più di cinque punti di riferimento sull'asse neutro. Rappresentano solo i limiti tra le aree potenziali nell'immagine. Tra i punti di riferimento è possibile usare qualsiasi tecnica di mapping di gamut esistente. Quindi, è possibile ritagliare l'intervallo di colori imprevisti e comprimere tutti i colori tra il bianco e il nero previsti oppure è possibile ritagliare tutti i colori all'esterno dell'intervallo di riferimento e comprimere all'interno di tale intervallo. Sono disponibili molte possibilità, che possono essere implementate in GMAs diversi. Inoltre, GMAs può comprimere e ritagliare in modi diversi. Tutte queste combinazioni sono incluse in questa invenzione.

Finora in questa discussione, la gamma è stata trattata come se fosse solo una funzione del dispositivo in cui l'immagine è stata creata, acquisita o visualizzata. Tuttavia, non esiste alcun motivo per cui tutte le immagini per un dispositivo devono avere lo stesso gamut. I GMAs dipendono dai dati in GBD. Se il descrittore viene modificato tra le immagini, non esiste alcun modo per la conoscenza del GMAs. In particolare, se le immagini non hanno evidenziazioni speculari, GMAs prestazioni migliori se il descrittore della gamma non mostra che sono presenti colori più chiari rispetto al bianco diffuso.

Nella nuova architettura CTE è possibile usare più di un GMA. L'uso di più GMAs è intrinsecamente definito in modo non corretto. Se, ad esempio, un dispositivo di acquisizione associa un GMA al suo "aspetto", tende a eseguire questa operazione con una gamma di destinazione "mirata". Lo stesso vale per i dispositivi di output e le gamme di origine "mirate". La gamut sRGB è una gamma implicita di destinazione comune. Si consiglia pertanto di usare un singolo GMA, se la prevedibilità è una priorità. Un singolo flusso di lavoro GMA dovrebbe essere l'impostazione predefinita per tutti i flussi di lavoro, in particolare i flussi di lavoro consumer e prosumer. Sebbene il mapping di gamut per la riproduzione preferita venga eseguito una sola volta, sono presenti istanze in cui sono inclusi più processi di mapping. Per prima cosa, per la correzione si esegue un mapping preferenziale alla gamma del dispositivo di destinazione finale, quindi un rendering colorimetrico nella gamma del dispositivo di correzione. In secondo luogo, alcuni tipi di mapping vengono usati per modificare le caratteristiche dell'immagine, ma non sono inclusi per eseguire il mapping a una gamma di dispositivi, ad esempio per regolare la curva di tono o la cromaticità. Se vengono usati più GMAs, l'interfaccia di trasformazione accetta una matrice di mappe di gamut associate, ovvero mappe di gamut che sono state inizializzate con una coppia di descrizioni dei limiti della gamma. Quando è presente più di una mappa gamut, il limite della gamma di input per una mappa di gamut successiva deve corrispondere al limite della gamma di output del predecessore.

La funzione limite della gamma di dispositivi accetta il motore del modello di dispositivo e i parametri analitici e deriva un limite di gamut dei dispositivi di colore descritto come un elenco di vertici ordinati della struttura convessa del gamut del dispositivo. L'elenco dei vertici ordinati viene archiviato in CIEJab. La struttura dell'elenco dei vertici ordinati è ottimizzata per l'accelerazione hardware da DirectX. Questo approccio presenta molte soluzioni ben note (cercare "convesso Hull DirectX" sul Web e si ottengono oltre 100 riscontri). In questo argomento è disponibile anche un riferimento a 1983 (teoria grafica del computer e applicazione, "Shiphulls, b-spline Surfaces e CADCAM" pp. 34-49), con riferimenti che risalgono da 1970 a 1982 nell'argomento.

Per calcolare i triangoli nella shell gamut, è possibile usare due tecniche diverse. Per altri dispositivi diversi dai dispositivi RGB aggiuntivi, viene calcolata una struttura convessa. Se si dispone dell'accesso diretto a tali dispositivi per convalidare l'affidabilità, le prestazioni e la fedeltà degli algoritmi, è possibile valutare il supporto della struttura non convessa per altri dispositivi. Si tratta di un processo noto che non richiede una descrizione aggiuntiva. La tecnica usata per i dispositivi RGB aggiuntivi è descritta di seguito.

GBDs diversi presentano vantaggi e svantaggi. La rappresentazione convessa della struttura garantisce proprietà geometriche interessanti, ad esempio sezioni di tonalità convesse che forniscono un punto di intersezione univoco con un raggio che emana da un punto sull'asse neutro. Anche il lato negativo della rappresentazione convessa è la convessità. È noto che molti dispositivi, in particolare i dispositivi di visualizzazione, hanno gamme che non sono più convesse. Se il gamut effettivo devia significativamente dal presupposto della convessità, la rappresentazione della struttura convessa risulterebbe non accurata, probabilmente nella misura in cui non rappresenta la realtà.

Dopo aver adottato un GBD che fornisce una rappresentazione ragionevolmente accurata del gamut reale, si verificano altri problemi, alcuni a causa del concetto di sezione tonalità. Esistono almeno due situazioni patologiche. Nella figura seguente, una gamma CRT fornisce le sezioni Hue con "Islands". Nella figura 25 una gamma di stampanti viene sollevata in una sezione di tonalità con parte dell'asse neutro mancante. In questi casi, le sezioni di tonalità patologiche non sono causate da limiti di gamut patologici. Sono causati dal concetto di sezione Hue, perché (a) viene preso in tinta costante e (b) richiede solo una metà del piano che corrisponde all'angolo di tonalità.

![Diagramma che mostra una visualizzazione superiore e una visualizzazione laterale dell'"curvatura in" nelle tonalità blu.](images/gmmp-image097.jpg)

**Figura 24** : un tipico monitor CRT presenta una gamma che mostra la "curvatura" nelle tonalità blu. Se vengono rilevate sezioni di tonalità in questo intervallo di tonalità, le isole isolate possono essere visualizzate nelle sezioni tonalità.

![Diagramma di una gamma con ' Gap ' nell'asse neutro.](images/gmmp-image099.jpg)

**Figura 25** : una stampante può avere una gamma con "gap" nell'asse neutro. Quando viene eseguita una sezione di tonalità (che corrisponde solo a una metà del piano), è presente un "dente" sulla parte del limite che rappresenta l'asse neutro. Questo può essere difficile da risolvere algoritmicamente.

Per risolvere queste patologie, viene proposto un nuovo Framework che abbandona il concetto di sezione Hue utilizzata come punto di partenza. Il Framework usa invece il set di "elementi linea limite" o le linee che si trovano sul limite della gamma. Non forniscono necessariamente una visualizzazione geometrica coerente come le sezioni Hue, ma supportano tutte le operazioni di gamut comuni. Oltre a risolvere i problemi citati in precedenza, questo approccio suggerisce anche che la costruzione di sezioni di tonalità, anche quando è possibile, è molto dispendiosa dal punto di vista del calcolo.

### <a name="triangulation-of-the-gamut-boundary"></a>Triangolazione del limite della gamma

Il punto di partenza è un GBD costituito da una triangolazione del limite della gamma. I metodi noti per costruire GBDs in genere forniscono la triangolazione. Per concreta, un metodo di costruzione di GBDs per i dispositivi additivi lo spazio del dispositivo è descritto qui. Questi dispositivi includono i monitoraggi (basati su CRT e su LCD) e i proiettori. La geometria semplice del cubo consente di introdurre un normale reticolo sul cubo. I visi limite del cubo possono essere triangolati in diversi modi, ad esempio quello illustrato nella figura 26. L'architettura fornisce un modello di dispositivo per il dispositivo, in modo che sia possibile ottenere i valori colorimetrico dei punti di reticolo algoritmicamente oppure che le misurazioni siano state effettuate direttamente per tali punti. L'architettura fornisce anche CIECAM02, in modo che sia possibile presupporre che i dati iniziali siano già stati mappati nello spazio CIECAM02 jab. Ogni punto di reticolo sui bordi del cubo RGB dispone quindi di un punto corrispondente nello spazio jab. Le connessioni di punti che formano il set di triangoli nello spazio RGB provocano anche un set di triangoli nello spazio jab. Questo set di triangoli costituisce una triangolazione ragionevole del limite della gamma se (a) il reticolo sul cubo RGB è sufficiente e (b) la trasformazione dallo spazio del dispositivo allo spazio uniforme del colore è topologicamente ben funzionante. ovvero, esegue il mapping del limite al limite e non trasforma la gamma interna, in modo che i punti interni diventino punti limite.

![Diagramma che illustra un metodo semplice per triangluate il limite della gamma di un dispositivo con R G B come spazio del dispositivo.](images/gmmp-image100.png)

**Figura 26** : un metodo semplice per triangolare il limite della gamma di un dispositivo con RGB come spazio del dispositivo

### <a name="boundary-line-elements"></a>Elementi linea limite

La centralità di questo Framework è il concetto di elementi linea limite; un set di segmenti di linea che (a) si trovano sul limite della gamma e (b) si trovano su un piano. In questo caso, il piano è un piano di tonalità. Ogni segmento di linea è il risultato dell'intersezione del piano con un triangolo di limite della gamma. Anche se molti ricercatori hanno usato la costruzione dell'intersezione di un piano con triangoli limite, in genere analizzano la relazione tra questi segmenti di linea e tentano di costruire un oggetto geometrico coerente tra i segmenti di linea. Sono stati concepiti algoritmi diversi per seguire questi segmenti di riga uno dopo l'altro fino a quando non viene ottenuta un'intera sezione di tonalità e sono stati effettuati molti tentativi per velocizzare il processo di ricerca.

Questo approccio è diverso. Il piano viene intersecato con i triangoli per ottenere i segmenti di linea. Questi segmenti di linea vengono quindi considerati come oggetti concettuali di *base* . È necessario analizzare la relazione tra i segmenti di linea; non è necessario capire come sono interconnesse tra loro. Questo punto di vista consente di risolvere il problema della sezione Hue con le isole. Gli approcci noti che tentano di costruire la sezione Hue presuppongono che, se uno inizia con un segmento di linea e lo segue al segmento di riga successivo e così via; Infine, viene restituito il punto iniziale, a quel punto viene costruita un'intera sezione di tonalità. Sfortunatamente, questo approccio potrebbe perdere l'isola (e nello scenario peggiore, il continente). Senza insistere sull'ottenimento di un'immagine geometrica coerente; ovvero, la sezione Hue consente di gestire facilmente il problema dell'isola. Un'altra differenza importante in questo approccio è che, per velocizzare la costruzione di segmenti di linea, viene usato un "filtro triangolo". Il filtro del triangolo genera determinati triangoli che non produrranno i segmenti di linea che risultano utili nell'operazione di gamut corrente. Poiché l'intersezione di un triangolo con il piano è costosa dal punto di vista del calcolo, questo migliora la velocità. Un effetto collaterale è che non è possibile costruire la sezione Hue perché alcuni segmenti di linea risultano mancanti a causa del filtro del triangolo.

### <a name="gamut-operation-checkgamut"></a>Operazione gamut: CheckGamut

Nell'esempio seguente viene illustrato il funzionamento del Framework e il modo in cui viene eseguito CheckGamut, vale a dire l'operazione di verifica se un colore è in gamma.

Il framework generale è illustrato nella figura 27 seguente. Sono disponibili diversi componenti. I componenti etichettati in corsivo sono componenti che possono essere diversi nell'implementazione a seconda dell'operazione di gamut in questione. Gli altri componenti sono invariabili in tutte le operazioni di gamut. Per iniziare, l' ***input*** è un set di attributi di colore. Nel caso di CheckGamut, è il colore della query. Nella figura 27 e nella discussione seguente si presuppone che l'angolo di tonalità sia tra gli attributi di colore di input o che possa essere ottenuto da essi. Questa situazione è evidente se l'input è l'intero punto di colore, in jab o JCh, da cui è possibile calcolare l'angolo di tonalità. Si noti che l'angolo di tonalità è necessario solo perché vengono usati i piani Hue. A seconda dell'operazione di gamut in questione, potrebbe non essere necessario usare il piano di tonalità. Ad esempio, nella costruzione della routine CheckGamut, può essere necessario usare i piani di costante J. Si tratta di una generalità che non verrà utilizzata o discussa ulteriormente; può tuttavia essere utile ricordare questa flessibilità della metodologia per supportare altre operazioni di gamut quando il piano Hue potrebbe non essere la scelta migliore.

![Diagramma che mostra il flusso per supportare le operazioni di gamut.](images/gmmp-image112.jpg)

**Figura 27** : Framework per supportare le operazioni di gamut

L'angolo di tonalità, ottenuto direttamente dagli input o calcolato dagli input, viene usato per inizializzare il piano di Hue con etichetta **full Hue** nella figura. Viene enfatizzato "full" poiché si tratta del piano completo, non solo del piano di metà che contiene la tonalità. Il piano completo contiene sia l'angolo di tonalità di input che l'angolo di 180 gradi opposto. La funzionalità chiave del piano Hue è la funzione Intersect, descritta nella sottosezione seguente, Full Hue Plane: Intersect. Si supponga che GBD sia già stato costruito e che sia disponibile il set di **triangoli limite gamma** . Intersecare i triangoli che sono sopravvissuti al *_filtro triangolo_** con il piano di tonalità usando Intersect. Il _componente filtro triangolo * è contrassegnato in corsivo, il che significa che il componente varia nell'implementazione per diverse operazioni di gamut. Il *filtro del triangolo* per CheckGamut è illustrato nella sezione operazione gamut: CheckGamut (continua). Il risultato dell'intersezione di un triangolo con il piano di tonalità è vuoto o un **elemento della linea di limite** , ovvero una coppia di punti distinti. Se il risultato non è vuoto, viene passato al processore di elementi a *_linee_*_ , che esegue nuovamente diverse operazioni a seconda dell'operazione di gamut. Il _processore di elementi linea * Aggiorna la struttura dei dati interna, ***dati elaborati interni**_ il cui contenuto o layout dipende anche dall'operazione di gamut. In genere, i _dati elaborati interni * contengono la risposta al problema, che viene continuamente aggiornata con ogni nuovo elemento linea limite trovato. Quando tutti gli elementi linea limite sono stati elaborati, la risposta è stata trovata. Rimane ad accedervi tramite l'adattatore di **output**_. Poiché i dati elaborati _Internal * sono specifici dell'operazione di gamma, anche l' *adattatore di output* è specifico dell'operazione di gamut.

### <a name="full-hue-plane-intersect"></a>Piano di Hue completo: Intersect

La funzione Intersect calcola l'intersezione tra il piano di tonalità e un triangolo. Questa funzione è importante per due motivi.

Prima di tutto, l'intersezione di ogni bordo del triangolo con il piano potrebbe produrre tre punti di intersezione, una situazione geometricamente impossibile. Il motivo per cui questa situazione potrebbe verificarsi nel calcolo è che, quando i calcoli vengono eseguiti in virgola mobile, ad esempio in formato IEEE, esistono incertezze o "rumore numerico" in ogni passaggio che influiscono sulla conclusione del fatto che un bordo interseca il piano. Quando il piano interseca i bordi in una situazione di mancata presenza, i punti di intersezione sono vicini tra loro e la determinazione che un punto di intersezione si trovi all'interno del bordo è casuale. Sebbene il rumore nei valori numerici dei punti sia piccolo, la conclusione qualitativa che ci sono più di due punti di intersezione è geometricamente impossibile e difficile da gestire correttamente nell'algoritmo.

In secondo luogo, questa funzione è nel ciclo critico per ogni bordo di ogni triangolo filtrato, quindi è importante ottimizzarne l'efficienza quanto più possibile.

Per risolvere il primo problema del rumore numerico, eseguire i calcoli in numeri interi. Per risolvere il secondo problema di ottimizzazione dell'efficienza, memorizzare nella cache l'attributo più usato di ogni vertice o il "prodotto a punti" associato a ogni vertice. Il passaggio in numeri interi è un modo tipico per garantire la coerenza geometrica. L'idea di base è che se è necessario quantizzare, eseguire l'operazione all'inizio. I calcoli successivi possono essere eseguiti in numeri interi e se i numeri interi sono sufficientemente ampi, in modo che non vi sia alcun rischio di overflow, è possibile eseguire calcoli con una precisione infinita. La funzione di quantizzazione seguente è utile a questo scopo.

ScaleAndTruncate (x) = parte intera di x \* 10000

Il fattore di scala 10000 indica che il numero a virgola mobile di input ha quattro posizioni decimali, che è sufficientemente preciso per questa applicazione. A seconda dell'intervallo di valori dello spazio aspetto colore, si desidera scegliere un tipo integer con bit sufficientemente ampio da includere i calcoli intermedi. Nella maggior parte degli spazi di aspetto dei colori, l'intervallo di ogni coordinata rientra nell'intervallo compreso tra-1.000 e 1.000. La coordinata quantizzata ha un valore assoluto massimo possibile di 1.000 \* 10.000 = 10 milioni. Come si vedrà, la quantità intermedia è un prodotto a virgola, ovvero una somma di due prodotti di coordinate, quindi il valore massimo possibile assoluto è 2 \* (10 milioni) ₂ = 2? 10 ₁ ₄. Il numero di bit richiesti è log ₂ (2? 10 ₁ ₄) = 47,51. Una scelta ottimale per il tipo Integer è, pertanto, gli Integer a 64 bit.

Per garantire che l'intersezione di un piano con un triangolo fornisca sempre un set vuoto o un set di due punti, è necessario prendere in considerazione il triangolo nel suo complesso, non come singoli bordi del triangolo separatamente. Per comprendere la situazione geometrica, prendere in considerazione le "distanze con segno" dei vertici del triangolo dal piano di tonalità. Non calcolare direttamente queste distanze firmate; calcolare invece i prodotti punto dei vettori di posizione dei vertici con il vettore normale quantizzato al piano. In particolare, durante l'inizializzazione del piano di tonalità, il vettore normale quantizzato viene calcolato come segue.

NormalVector = (ScaleAndTruncate (-sin (Hue)), ScaleAndTruncate (cos (Hue)))

Si noti che questo vettore è un vettore bidimensionale. È possibile usare un vettore bidimensionale perché il piano Hue è verticale, quindi il terzo componente del vettore normale è sempre zero. Inoltre, una tabella di ricerca di prodotti punto viene inizializzata in modo da includere una voce per ogni vertice tra i triangoli dei limiti della gamma e il prodotto punto corrispondente impostato su un valore non valido.

Durante un'operazione di intersezione del piano Hue con un triangolo, viene ricercato il prodotto punto di ogni vertice del triangolo. Se il valore nella tabella di ricerca è un valore non valido, il prodotto punto viene calcolato usando l'espressione seguente.

NormalVector. a \* ScaleAndTruncate (Vertex. a) + NormalVector. b \* ScaleAndTruncate (Vertex. b)

Anche in questo caso, il componente J del vertice non viene mai usato, perché il vettore normale è orizzontale. Questo prodotto a virgola viene quindi salvato nella tabella di ricerca in modo che non debba essere ricalcolato se viene eseguita una query in un secondo momento sul prodotto del vertice.

La memorizzazione nella cache consente di determinare rapidamente se un bordo interseca il piano, dopo che i prodotti punto sono stati catalogati nella tabella di ricerca, compilata progressivamente man mano che vengono elaborati i vertici.

![Diagramma che mostra l'intersezione del piano di tonalità con un triangolo.](images/gmmp-image114.jpg)

**Figura 28** : intersezione del piano Hue con un triangolo

Per il triangolo nella figura 28 per intersecare il piano Hue in un segmento di linea non degenerate, i prodotti punto dei vertici devono trovarsi in uno dei modelli seguenti, se ordinati in ordine crescente.

0, 0, +; -,0, 0; -, 0, +; -,-,+; -,+,+

Un punto finale del segmento di linea si verifica quando il piano viene intersecato da un bordo con vertici con segni diversi nel prodotto del punto. Se il segno è zero, il vertice si trova direttamente sul piano e l'intersezione del bordo con il piano è il vertice stesso. Si noti anche che i case 0, 0, 0; -,-, 0; 0, +, + non vengono segnalati. Il primo caso (0, 0, 0) indica che l'intero triangolo si trova sul piano. Questo non viene segnalato perché ogni bordo del triangolo deve appartenere a un triangolo adiacente che non si trova interamente sul piano. Il bordo verrà segnalato quando il triangolo viene considerato. Gli altri due casi (-,-, 0 e 0, +, +) corrispondono alla configurazione geometrica che il triangolo tocca il piano in un vertice. Questi casi non vengono segnalati perché non danno luogo a un segmento di linea non degenerate.

L'algoritmo precedente determina quando calcolare un'intersezione tra un bordo del triangolo e il piano di tonalità. Dopo aver determinato un bordo, l'intersezione viene calcolata usando equazioni parametriche. Se uno dei prodotti punto è zero, l'intersezione è il vertice stesso, quindi non è necessario alcun calcolo. Supponendo che entrambi i prodotti punto dei vertici del perimetro siano diversi da zero, vertex1 è il vertice con il punto *negativo* prodotto dotProduct1; e VERTEX2 è il vertice con dotProduct2 punto *positivo* prodotto. Questo ordine è importante per garantire che il punto di intersezione calcolato non dipenda dal modo in cui viene visualizzato l'ordine dei vertici nella rappresentazione del bordo. Il concetto geometrico del perimetro è simmetrico rispetto ai vertici. L'aspetto computazionale dell'uso di equazioni parametriche del perimetro introduce l'asimmetria (scelta del vertice iniziale), che può fornire un punto di intersezione leggermente diverso a causa del rumore numerico e del condizionamento delle equazioni lineari da risolvere. In questo modo, il punto di intersezione, intersezione, viene fornito dal codice seguente.

t = dotProduct1/(dotProduct1-dotProduct2)

intersezione. J = vertex1. J + t \* (VERTEX2. J-vertex1. J

intersezione. a = vertex1. a + t \* (VERTEX2. a-vertex1. a)

intersezione. b = vertex1. b + t \* (VERTEX2. b-vertex1. b)

### <a name="gamut-operation-checkgamut-continued"></a>Operazione gamut: CheckGamut (continua)

L'algoritmo geometrico di base usato per la verifica del gamut consiste nel contare il numero di incroci del raggio. Per un determinato punto di query, prendere in considerazione un raggio che inizia con il punto di query e punta verso l'alto (direzione J). Contare il numero di volte in cui questo raggio supera il limite della gamma. Se questo numero è pari, il punto di query è fuori gamma. Se questo numero è dispari, il punto si trova all'interno. In linea di principio, questo algoritmo può essere implementato in 3D, in genere è afflitto da problemi causati da situazioni degenerate, ad esempio il raggio (in parte) in un triangolo limite o degenerazione di dimensioni inferiori, ad esempio il raggio (in parte) in un bordo di un triangolo di limite. Anche in 2-D, è necessario gestire queste situazioni degenerate. Tuttavia, il problema è più semplice ed è stato risolto in modo soddisfacente. Vedere \[ Rourke \] .

Per un determinato punto di input diretto, determinare il relativo angolo di tonalità h, come indicato di seguito.

h = Atan (b/a),

Inizializzare il piano di tonalità, quindi determinare gli elementi della linea limite corrispondenti a questo piano di tonalità. Poiché gli elementi della linea limite sono rilevanti solo se intersecano il raggio ascendente, impostare un filtro triangolo per rimuovere i triangoli che forniscono elementi linea che non intersecano definitivamente il raggio ascendente. In questo caso, si consideri il rettangolo di delimitazione del triangolo. Il raggio ascendente non interseca il triangolo se il punto di query si trova al di fuori del cast "Shadow" dal rettangolo di delimitazione se una sorgente di luce è stata immediatamente sopra. Ingrandire leggermente questo valore con una tolleranza prefissa per consentire un rumore numerico, in modo da non eliminare inavvertitamente triangoli che potrebbero fornire elementi linea utili. Il risultato è il cilindro rettangolare semi-infinito illustrato nella Figura 29. Controllare se il punto di query si trova all'interno o all'esterno di questo cilindro può essere implementato in modo efficiente usando semplici disuguaglianze.

![Mostra il filtro del triangolo per CheckGamut.](images/gmmp-image116.jpg)

**Figura 29** : filtro triangolo per CheckGamut

CheckGamut dispone di tre componenti specifici per le operazioni di gamma: *dati elaborati interni*,*elaboratore di elementi linea* e *adattatore di output*. I *dati elaborati interni* sono un elenco di elementi linea elaborati dal *processore di elementi linea*. In questo caso, il *processore di elementi linea* aggiunge semplicemente un elemento linea all'elenco. La struttura dei dati interni per i *dati elaborati interni* può essere un elenco collegato o una matrice che può aumentare di dimensioni.

L' *adattatore di output* è un modulo che accede all'elenco di elementi linea, determina se un elemento linea incrocia il raggio ascendente (conteggio 1) o meno (conteggio 0). Sommando tutti questi conteggi si ottiene un conteggio totale. In definitiva, l' *adattatore di output* restituisce una risposta di "Sì" (in-gamut) o "No" (out-of-gamut), a seconda che il conteggio totale sia dispari o uniforme. Il passaggio in cui si determina se un elemento linea incrocia il raggio ascendente merita un'attenzione perché questo è il punto in cui si verifica il problema di degenerazione e anche il problema del conteggio eccessivo. Dopo \[ l' \] elemento Rourke, affinché un elemento Line attraversi il raggio, l'endpoint destro (il punto finale con Chroma maggiore) deve essere rigorosamente sul lato destro del raggio. Ciò garantisce che, se un punto finale si trova esattamente sul raggio, viene conteggiato una sola volta. La stessa regola consente inoltre di risolvere la situazione di degenerazione in cui l'elemento riga si trova esattamente sul raggio. Non si incrementa il conteggio per questo elemento linea.

La figura 30 Mostra gli elementi riga risultanti di una gamut di esempio con il punto di query in varie posizioni.

![Diagramma che Mostra gli elementi riga risultanti di una gamut di esempio con il punto di query in varie posizioni.](images/gmmp-image118.jpg)

**Figura 30** : funzionamento di CheckGamut

### <a name="minimum-color-difference-gamut-mapping"></a>Mapping del gamut di differenza colore minimo

Il mapping del gamut dei colori minimo, MinDEMap, presenta una specifica semplice: se un colore è in gamut, non eseguire alcuna operazione. Se un colore è esterno al gamut, proiettarlo sul punto "più vicino" sul limite della gamma. La parola chiave "più vicina" non è ben definita fino a quando non si specifica l'equazione di differenza dei colori da usare. In pratica, per semplificare e velocizzare il calcolo, la distanza euclidea dello spazio di aspetto dei colori scelto o una variante di esso viene utilizzata come metrica di differenza dei colori. Il vantaggio della metrica euclidea è che è compatibile con il prodotto a punti dello spazio, che rende possibile l'uso di algebra lineare. In dettaglio, se nello spazio viene definito un "prodotto punto", è possibile definire una distanza come radice quadrata del prodotto a punti del vettore di differenza. Un prodotto a virgola può in genere essere definito da una matrice 3x3 positiva definita A.

u? v = u <sub>T</sub> AV

dove il lato destro corrisponde alla moltiplicazione di matrice consueta. Se è la matrice di identità, viene recuperato il prodotto A virgola standard. In pratica, se jab è lo spazio colore, non si desidera combinare i componenti, pertanto è possibile utilizzare una matrice diagonale diversa dalla matrice di identità. Inoltre, potrebbe essere necessario mantenere la scala su a e b invariata in modo che la misura di tonalità venga mantenuta. Quindi, una variante utile del prodotto standard euclideo dot è la seguente.

w <sub>j</sub> (j componente di te) (j component of v) + (un componente di te) (componente di v) + (componente b di te) (componente b di v)

dove w <sub>J</sub> è un numero positivo. Un'ulteriore variazione consiste nel consentire a w <sub>J</sub> di variare con il punto di query di input:

w <sub>j \ =</sub> w <sub>j</sub> (queryPoint)

Il risultato finale è una misura della distanza asimmetrica rispetto ai due punti e con pesi relativi diversi sulla luminosità e Chroma o Hue quando il punto di query di input varia. In conformità con alcune osservazioni sulla percezione dei colori umani, le differenze di colore non vengono ponderate in modo uniforme in tutte le dimensioni. È stato rilevato che le persone sono meno sensibili alle differenze di luminosità rispetto a quelle di Hue e Chroma.

La funzione Weight seguente è utile.

w <sub>J</sub> = k ₂-k ₁ (C-c m ₐ ₓ) n

dove k ₂ = 1, k ₁ = 0,75/(C m ₐ ₓ) n, C m ₐ ₓ = 100, n = 2 e C è il più piccolo di Chroma del punto di query e C m ₐ ₓ.

in modo che un peso di 0,25 venga inserito nel termine J quando Chroma è zero e un peso di 1 quando Chroma è 100. La tendenza a mettere un peso minore su J quando Chroma è piccola e un peso maggiore su J quando Chroma è grande segue l'utilizzo consigliato per CMC e CIEDE2000.

![Grafico che mostra la funzione Weight sul componente J della metrica.](images/gmmp-image119.png)

**Figura 31** : funzione Weight sul componente J della metrica

Usare lo spazio jab per l'esempio seguente. Il calcolo richiede la ricerca di tutti i triangoli limite per determinare il punto più vicino nella metrica euclidea. Di seguito è riportato un semplice approccio per rendere questo processo il più efficiente possibile, senza introdurre presupposti aggiuntivi che potrebbero velocizzare il processo, ma anche finire solo in una risposta approssimativa. Per prima cosa, è necessario comprendere la procedura geometrica per proiettare un punto sul triangolo specificato. Qui viene fornita una descrizione.

Viene eseguita prima una proiezione ortogonale sul piano infinito che contiene il triangolo. La distanza più breve del punto di query dal piano può essere determinata in due passaggi.

**(a)** calcolare il vettore del normale dell'unità al triangolo.

**(b)** calcolare il prodotto punto del vettore di unità normale e un vettore formato dal punto di query e un punto sul triangolo; ovvero uno dei vertici. Poiché il vettore normale presenta una lunghezza di unità, il valore assoluto di questo prodotto punto corrisponde alla distanza del punto di query dal piano.

Il punto proiettato potrebbe non essere la risposta, perché potrebbe trovarsi all'esterno del triangolo. Pertanto, è necessario eseguire prima una verifica. Il calcolo equivale a calcolare le coordinate baricentrica del punto proiettato rispetto al triangolo. Se il punto proiettato è determinato all'interno del triangolo, è la risposta. In caso contrario, viene acquisito il punto più vicino su uno dei bordi del triangolo. Eseguire una ricerca su ognuno dei tre bordi. Determinare la proiezione del punto di query su un bordo è un processo simile alla proiezione sul triangolo, ma una dimensione minore. Viene innanzitutto calcolata una proiezione ortogonale. Se il punto proiettato si trova sul bordo, è la risposta. In caso contrario, viene acquisito il punto più vicino in uno dei due punti finali. Eseguire una ricerca sui due punti finali; ovvero calcolare la distanza del punto di query da ciascuno di essi e confrontare quello più piccolo.

L'analisi attenta rivela che è presente una grande quantità di ricerche ripetute quando si esaminano tutti i triangoli perché un bordo è sempre condiviso da due triangoli e un vertice condiviso da almeno tre bordi. Inoltre, non si è molto interessati a trovare il punto più vicino a un particolare triangolo; si è invece interessati a trovare il punto più vicino all'intero limite della gamma. Tuttavia, un particolare triangolo è quello in cui si raggiunge questa situazione. Esistono due strategie che è possibile utilizzare per velocizzare la ricerca.

**Strategia I**. Ogni vertice verrà elaborato al massimo una volta. Ogni bordo verrà elaborato al massimo una volta.

**Strategia II**. In qualsiasi punto della ricerca si ha un candidato migliore con la distanza migliore corrispondente. Se è possibile determinare, mediante un controllo rapido, che un triangolo non è in grado di fornire una distanza migliore, non è necessario continuare ulteriormente il calcolo. Non sono necessari il punto e la distanza più vicini per questo triangolo.

![Diagramma che mostra il flusso del mapping minimo di.](images/gmmp-image120.png)

**Figura 32** : schemi di mapping minimi

La figura 32 illustra il flusso generale della logica per la mappa gamut MinDEMap. Per un punto di query, viene prima richiamata la funzione CheckGamut. Se il punto è in-gamut, la mappa è un no-op. Se il punto è out-of-gamut, chiamare ProjectPointToBoundary. Passare ora alla figura 33. A questo punto si presuppone che siano stati calcolati i valori seguenti.

**(a)** unità vettore normale per ogni triangolo limite gamma rispetto al prodotto a virgola standard.

**(b)** elenco di vertici e bordi, oltre all'elenco dei triangoli.

![Diagramma che mostra la routine ' ProjectPointToBoundary '.](images/gmmp-image122.jpg)

**Figura 33** : routine ProjectPointToBoundary

Tutti questi sono un sovraccarico costante e potrebbero ridurre i costi se vengono eseguite query sufficienti per questo limite di gamut. In genere, questa situazione si verifica quando si compila un LUT di trasformazione da un dispositivo a un altro, in cui sono presenti solo due gamme fisse e il LUT di trasformazione viene eseguito attraverso punti della griglia campionata in modo uniforme. Si precalcolano i vettori normali rispetto al prodotto punto standard, anche se la nozione di perpendicolarità sarà basata sul prodotto del punto ponderato, che dipende dal punto di query, come illustrato in precedenza. Il motivo è dovuto al fatto che un vettore normale rispetto al prodotto dot ponderato può essere ottenuto facilmente dal vettore normale rispetto al prodotto punto standard. Se n ₀ è un vettore normale rispetto al prodotto punto standard,

n = (J-component of n ₀/w <sub>J</sub>, a-component of n ₀, b-component of n ₀)

è normale per il triangolo rispetto al prodotto del punto ponderato. A causa di questa relazione, è comunque vantaggioso pre-calcolare n ₀ anche se deve essere regolato in base al punto di query.

La routine ProjectPointToBoundary viene avviata reimpostando la "cronologia elaborata" dei vertici e dei bordi. Si tratta di tabelle di flag BOOLEANI che rilevano se un vertice o un bordo è stato visitato prima. Reimposta inoltre la variabile ShortestDistance su "INFINITY", che rappresenta il valore codificato massimo nel sistema con numero a virgola mobile utilizzato. Viene quindi eseguito un ciclo, cercando il punto più vicino da ogni triangolo usando la chiamata ProcessTriangle. ProcessTriangle è la routine per aggiornare la variabile ShortestDistance ed è chiaramente nel ciclo critico. Un'ottimizzazione consiste nell'arrestare quando il risultato è sufficientemente adatto. Dopo ogni chiamata a ProcessTriangle, viene esaminata la variabile ShortestDistance. Se soddisfa una soglia predefinita, è possibile arrestare. La soglia predefinita dipende dallo spazio di colore utilizzato e dall'accuratezza necessaria del sistema di imaging dei colori. Per un'applicazione tipica, non si desidera eseguire operazioni superflue se la differenza di colore è inferiore a quella che può essere individuata dalla visione umana. Per CIECAM02, la differenza di colore è 1. Usare tuttavia un valore soglia di 0,005 nell'implementazione, per mantenere la precisione dei calcoli, perché potrebbe trattarsi solo di un passaggio intermedio in una catena di trasformazioni.

ProcessTriangle implementa la strategia precedente II. Ottenendo un vettore normale dal vettore normale dell'unità pre-calcolata al triangolo rispetto al prodotto punto standard, viene calcolata la distanza tra il punto di query e il piano infinito che contiene il triangolo formando il prodotto a virgola del vettore di unità normale e il queryVector, il vettore da uno dei vertici del triangolo, vertex1, al punto di query , queryPoint.

queryVector = queryPoint-vertex1

distance = \| normalVector \* queryVector \| / \| \| normalVector\|\|

Si tratta di un calcolo relativamente economico e la distanza è necessaria per eseguire ulteriori calcoli. Se questa distanza non è inferiore alla distanza ottimale corrente, ShortestDistance, questo triangolo non produrrà una distanza migliore, poiché non fornirà una distanza migliore rispetto al piano che la contiene. In questo caso, si restituisce il controllo al ciclo triangolare. Se la distanza è inferiore a ShortestDistance, potenzialmente si ha un punto più vicino, se questo punto si trova all'interno del triangolo. È necessario eseguire alcuni calcoli "rigidi" (anche se non oltre l'algebra lineare) per determinarlo. Se gli altri due vertici del triangolo sono VERTEX2 e vertex3, formare i vettori di base firstBasisVector e secondBasisVector.

firstBasisVector = VERTEX2-vertex1

secondBasisVector = vertex3-vertex1

Usare il sistema lineare di equazioni seguente per risolvere i problemi relativi a e v.

firstBasisVector \* queryVector = (firstBasisVector \* firstBasisVector) u + (firstBasisVector \* secondBasisVector) v

secondBasisVector \* queryVector = (secondBasisVector \* firstBasisVector) u + (secondBasisVector \* secondBasisVector) v

e le condizioni per il punto proiettato che si trovano all'interno del triangolo sono:

0 ≤ u ≤ 1, 0 ≤ v ≤ 1 e u + v ≤ 1

Dopo questo calcolo, se è stato determinato che il punto proiettato si trova all'interno del triangolo, è stato trovato un nuovo punto più vicino; la distanza calcolata all'inizio è la nuova distanza più breve. In questo caso, aggiornare le variabili ShortestDistance e ClosestPoint. Se il punto proiettato si trova all'esterno del triangolo, è possibile trovare un punto più vicino su uno dei bordi. Quindi, è possibile chiamare la routine ProcessEdge su ognuno dei tre bordi.

![Diagramma che mostra il flusso delle routine ProcessEdge e ProcessVertex.](images/gmmp-image124.jpg)

**Figura 34** : routine ProcessEdge e ProcessVertex

La routine ProcessEdge implementa la strategia I, illustrata nella Figura 34. ProcessEdge inizia controllando se il bordo è stato elaborato prima. In tal caso, non viene eseguita alcuna azione ulteriore. In caso contrario, viene calcolata la proiezione ortogonale del punto di query sulla riga infinita che contiene il bordo. L'algebra lineare che interessano il calcolo è simile alle equazioni del triangolo precedenti. Tuttavia, il calcolo è più semplice e non è descritto qui. Se il punto proiettato si trova all'interno del bordo, è possibile trovare la distanza del punto proiettato dal punto di query. Se questa distanza è inferiore a ShortestDistance, è stato trovato un nuovo punto più vicino. Aggiornare sia ShortestDistance che ClosestPoint. Se il punto proiettato è esterno al bordo, chiamare ProcessVertex sui due endpoint. Prima di restituire il controllo, aggiornare la cronologia perimetrale in modo che il bordo sia contrassegnato come "elaborato".

Infine, si dà una descrizione di ProcessVertex. La routine ProjectVertex implementa anche la strategia I e mantiene una tabella di cronologia dei vertici. Come illustrato nella Figura 34, prima controlla se il vertice è stato elaborato prima. In tal caso, non viene eseguita alcuna azione ulteriore. In caso contrario, viene calcolata la distanza del vertice dal punto di query. Se la distanza è inferiore a ShortestDistance, aggiornare sia ShortestDistance che ClosestPoint. Alla fine, aggiorna la cronologia dei vertici in modo che questo vertice venga contrassegnato come "elaborato".

Quando il ciclo di controllo esterno ha esaurito tutti i triangoli o è stato terminato prima che venisse soddisfatta la soglia di differenza colore, viene eseguito l'accesso alla variabile ClosestPoint. Questo è il risultato di MinDEMap. Il chiamante può anche recuperare ShortestDistance se è interessato alla distanza del colore mappato dal colore della query.

### <a name="hue-smoothing"></a>Smussatura tonalità

![Diagramma che mostra due viste principali della smussatura tonalità, l'originale sulla parte superiore e la tonalità smussate in basso.](images/gmmp-image125.png)

**Figura 35** : smussatura Hue

Si verifica un problema con le operazioni con tonalità vincolata; ovvero, l'operazione considera solo le variabili all'interno di un piano di tonalità. La figura 35 illustra un esempio di gamut che mostra le sezioni di tonalità "discontinue" nelle tonalità blu. All'interno di questo intervallo di tonalità, per determinati angoli di tonalità, il limite della gamma è tangente al piano di tonalità. In effetti, ciò causa una modifica nella struttura topologica delle sezioni tonalità. Nell'esempio illustrato, quando il piano di tonalità si estende in questo intervallo di tonalità, emerge una "isola" e le sottofusioni. Questa modifica nella topologia causerà la discontinuità delle operazioni specifiche di Hue. Ad esempio, la cuspide a tonalità fissa verrà modificata bruscamente quando l'angolo di tonalità cambierà in questo intervallo.

Esiste una ragione per la scienza dei colori perché è consigliabile mantenere Hue in determinate operazioni. Per risolvere il problema precedente, i triangoli di limite della gamma originale devono essere "tonalità smussata". In generale, una sfumatura di tonalità di un set di triangoli di limite di gamut è un set di triangoli in modo che (a) formi il limite di un nuovo "gamut", che potrebbe non corrispondere al gamut effettivo del dispositivo e che contiene la gamma definita dal set originale di triangoli; e (b) i triangoli del nuovo set sono delimitati dall'esecuzione parallela ai piani Hue.

Un modo pratico per ottenere un set smussato di tonalità di triangoli consiste nel prendere la struttura convessa dei vertici originali. Come illustrato nella Figura 35, le sezioni di tonalità della struttura convessa variano in modo uniforme nell'intervallo di tonalità problematico senza modifiche improvvise nella topologia.

### <a name="setting-primaries-and-secondaries-in-the-gamut-boundary-description"></a>Impostazione di primari e secondari nella descrizione del limite della gamma

Determinati metodi di mapping di gamut, ad esempio HueMap, dipendono dalla posizione delle primarie del dispositivo e dei database secondari. Per i dispositivi additivi, i primari sono rosso, verde e blu (R, G e B); e i database secondari sono cyan, magenta e Yellow (C, M e Y). Per i dispositivi sottrattivi, le primarie sono C, M e Y; e i database secondari sono R, G e B. Il GBD tiene traccia di tutti i sei valori, più bianco e nero (W e K), in una matrice di valori di colore jab. Questi valori vengono impostati nella descrizione del limite della gamma al momento della creazione. Per i dispositivi di output, è possibile determinare gli primari eseguendo combinazioni di valori di controllo del dispositivo tramite il modello di dispositivo. Per i dispositivi di acquisizione, questo approccio non è particolarmente adatto per la creazione del GBD di riferimento, perché è quasi impossibile acquisire un'immagine che restituisce un valore di dispositivo puro completamente saturo, ad esempio (0,0, 0,0, 1,0). I profili dei dispositivi WCS contengono gli indici delle primarie nella destinazione di acquisizione. Poiché questi valori non sono contenuti in un profilo ICC, utilizzare i valori misurati da una tipica destinazione dello scanner dopo la conversione in jab rispetto alle condizioni di visualizzazione ICC.

### <a name="setting-the-neutral-axis-in-the-gamut-boundary-description"></a>Impostazione dell'asse neutro nella descrizione del limite della gamut

Il HueMap e i metodi di mapping di gamut tritati relativi usano l'asse neutro del dispositivo per la raddrizzatura. Per i dispositivi di output di base, l'asse neutro può essere determinato eseguendo valori neutri del dispositivo (R = G = B o C = M = Y) tramite il metodo DeviceToColorimetric e quindi tramite il metodo ColorimetricToAppearance dell'oggetto CIECAM02. Tuttavia, i dispositivi di acquisizione non restituiscono sempre un valore neutro del dispositivo quando viene presentato un campione neutro. Ciò è particolarmente vero quando l'illuminazione ambientale non è perfettamente neutra. I profili dei dispositivi WCS contengono gli indici degli esempi neutri nella destinazione. Usare questi esempi per impostare l'asse neutro. Poiché queste informazioni non sono disponibili per i profili ICC, è necessario usare lo stesso metodo usato per i dispositivi di output. eseguire esempi di dispositivo neutro tramite il metodo DeviceToColorimetric, quindi abbinare i valori di input e i risultati di colorimetrico.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti di base sulla gestione dei colori](basic-color-management-concepts.md)
</dt> <dt>

[Schemi e algoritmi del sistema di colori Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




