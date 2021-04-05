---
title: Riferimento al modello a oggetti la
description: In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889c977260548c26bbfd8196160e4537ccb8895d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047267"
---
# <a name="vml-object-model-reference"></a>Riferimento al modello a oggetti la

In questo argomento viene descritto la, una funzionalità deprecata a partire da Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su la devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> Al 2011 dicembre, questo argomento è stato archiviato. Di conseguenza, non viene più gestita attivamente. Per altre informazioni, vedere [contenuto archiviato](/previous-versions/windows/internet-explorer/ie-developer/). Per informazioni, suggerimenti e indicazioni per la versione corrente di Windows Internet Explorer, vedere il [centro per sviluppatori di Internet Explorer](https://msdn.microsoft.com/ie/).

 

In questo argomento

-   [Introduzione](#introduction)
-   [Esempio](#example)
-   [Configurazione di la](#setting-up-vml)
-   [Riferimento a la OM](#vml-om-reference)
    -   [Shape-elemento](#shape-element)
-   [Sottoelementi dell'elemento Shape](#subelements-of-the-shape-element)
    -   [Elemento background](#background-element)
    -   [Elemento Extrusion](#extrusion-element)
    -   [Fill (elemento)](#fill-element)
    -   [Group - elemento](#group-element)
    -   [Elemento ImageData](#imagedata-element)
    -   [Path-elemento](#path-element)
    -   [Elemento Shadow](#shadow-element)
    -   [Elemento asimmetria](#skew-element)
    -   [Stroke-elemento](#stroke-element)
    -   [Elemento TextPath](#textpath-element)
-   [Tipi di dati utilizzati nel modello a oggetti la](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a>Introduzione

[Vector Markup Language (la)](https://www.w3.org/TR/NOTE-datetime.html) è un linguaggio basato su testo che usa [XML](https://www.w3.org/TR/REC-xml.mdl) per estendere il codice HTML allo scopo di visualizzare le informazioni grafiche vettoriali. Il Document Object Model la (DOM) definisce un'interfaccia a livello di codice per la manipolazione degli elementi del documento. Ciò consente all'utente di creare e modificare dinamicamente la grafica vettoriale tramite un'interfaccia indipendente dalla piattaforma e dal linguaggio. Il DOM la è conforme alla specifica [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) .

LA usa l'elemento [Shape](#shape-element) come blocco predefinito di base per le immagini grafiche vettoriali. Una volta creata una forma, è possibile modificare la forma tramite gli attributi o i sottoelementi collegati. Per modificare, ad esempio, il colore di una forma, assegnare un valore di colore all'attributo **FillColor** .


```HTML
myshape.fillcolor = "red"
```



Molti degli attributi di una forma sono anche [sottoelementi](/windows) e hanno attributi propri, inclusi i seguenti:

-   [Background](#background-element)
-   [Estrusione](#extrusion-element)
-   [Fill](#fill-element)
-   [Gruppo](#group-element)
-   [ImageData](#imagedata-element)
-   [Percorso](#path-element)
-   [Shadow](#shadow-element)
-   [Sfasamento](#skew-element)
-   [Stroke](#stroke-element)
-   [TextPath](#textpath-element)

LA OM usa diversi [tipi di dati](/windows) per definire i parametri. I tipi di DataType con prefisso "VG" sono enumerazioni e quelli con prefisso "IVg" sono oggetti. Per un elenco, fare clic qui. I tipi di Data Type secondari sono elencati con parametri specifici.

## <a name="example"></a>Esempio

Nel codice VBScript seguente viene illustrato come creare una forma semplice:


```HTML
        Set MyRect = Document.CreateElement("v:Rect")
        Set R = MyDiv.AppendChild(MyRect)
        R.Style.Position = "absolute"
        R.Style.Width = 20
        R.Style.Height = 20
        R.Style.Top = 50
        R.Style.Left = 50
        R.FillColor = "red"
```



Nell'esempio precedente viene creata una forma usando il Document Object Model metodo **CreateElement**. La forma è una forma Rect predefinita di la. Anche se l'oggetto esiste, non può far parte del documento finché non viene collegato al documento. Utilizzando il metodo **AppendChild** , il Rect viene trasformato come figlio di un elemento **div** denominato MyDiv. Alcuni attributi di stile minimo (**posizione**, **larghezza**, **altezza**, **superiore**, **sinistra**) sono impostati in modo da assegnare alla forma una dimensione specifica. Infine, viene assegnato un colore con l'attributo **FillColor** . Si noti che è possibile usare qualsiasi linguaggio di scripting o qualsiasi linguaggio in grado di funzionare con Document Object Model interfacce.

## <a name="setting-up-vml"></a>Configurazione di la

Un'implementazione di la è tramite Microsoft Internet Explorer 5,0 o versione successiva. Per configurare correttamente l'oggetto rendering in una pagina Web, è necessario effettuare le aggiunte seguenti:

1.  È necessario configurare lo schema nella finestra iniziale <HTML> Tag come segue:
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  Il comportamento di rendering deve far parte dello stile del documento:
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

Di seguito viene illustrata una pagina Web HTML di esempio configurata correttamente per la che mostra la creazione dinamica di una forma.


```HTML
<HTML xmlns:v="urn:schemas-microsoft-com:vml">
<HEAD>
<STYLE>
v\:* { behavior: url(#default#VML); display:inline-block}
</STYLE>
<TITLE>VML Sample</TITLE>
</HEAD>
<BODY>
<DIV id="MyDiv"></DIV>
<SCRIPT ID="MYSCRIPT" LANGUAGE="VBScript">
<!--
Set MyRect = Document.CreateElement("v:Rect")
Set R = MyDiv.AppendChild(MyRect)
R.Style.Position = "absolute"
R.Style.Width = 20
R.Style.Height = 20
R.Style.Top = 50
R.Style.Left = 50
R.FillColor = "red"
-->
</SCRIPT>
</BODY>
</HTML>
```



Si noti che nelle versioni beta, era necessario un tag Object ActiveX e uno stile di comportamento diverso.

## <a name="vml-om-reference"></a>Riferimento a la OM

Questo riferimento definisce l'elemento della [forma](#shape-element) , i [sottoelementi](/windows)e i [tipi di dati](/windows) utilizzati dal modello a oggetti di la.

### <a name="shape-element"></a>Shape-elemento

Le forme sono i blocchi predefiniti delle immagini grafiche definite da Vector Markup Language (la). La forma è l'elemento di primo livello e diversi sottoelementi consentono di definire la natura di ogni forma.

LA fornisce forme predefinite:

**Attributi di forma**

-   **Arc**
-   **Curva**
-   **Linea**
-   **Polilinea**
-   **Rect**
-   **RoundRect**



|              |                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADJ          | [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md). Elenco delimitato da virgole di numeri che rappresentano i parametri per le formule della guida che definiscono il percorso della forma. È possibile omettere i valori per consentire l'utilizzo delle impostazioni predefinite. Possono essere presenti fino a 8 valori di regolazione.                                                                                                   |
| ALT          | Stringa. Testo alternativo associato alla forma. Usato per l'esplorazione non grafica.                                                                                                                                                                                                                                                                                                 |
| Pulsante       | [VgTriState](msdn-online-vml-vgtristate.md). Visualizza il comportamento del pulsante sul clic.                                                                                                                                                                                                                                                                                                 |
| BWMode       | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Determina la modalità di rendering della forma nella visualizzazione in bianco e nero nelle app o quando viene stampata su stampanti nere e bianche. I valori includono: **color**, **auto**, **gradazioni di grigio**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **undisegnato**. Impostazione predefinita: **auto**. |
| BWNormal     | VgBlackWhiteMode. Quando BWMode è auto, viene consultata questa proprietà per il rendering della forma in bianco e nero normale. I valori includono: **color**, **auto**, **gradazioni di grigio**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **undisegnato**. Impostazione predefinita: **auto**.                                                |
| BWPure       | VgBlackWhiteMode. Quando BWMode è auto, viene consultata questa proprietà per il rendering della forma in B/W pure. I valori includono: **color**, **auto**, **gradazioni di grigio**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **undisegnato**. Impostazione predefinita: **auto**.                                                              |
| ChildShapes  | IVgGroupShapes. Raccolta di altre forme in questo gruppo. Questa raccolta supporta i metodi di lunghezza ed elemento standard.                                                                                                                                                                                                                                                       |
| Chromakey    | [IVgColor](msdn-online-vml-ivgcolor.md). Valore di colore che sarà trasparente e visualizzerà qualsiasi elemento sottostante la forma.                                                                                                                                                                                                                                                             |
| Control1     | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto di controllo per la curva.                                                                                                                                                                                                                                                                                                  |
| Controllo2     | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto di controllo per la curva.                                                                                                                                                                                                                                                                                                  |
| CoordOrigin  | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md) Coordinate nell'angolo superiore sinistro del rettangolo del contenitore. Intervallo compreso tra 0 e infinito.                                                                                                                                                                                                                               |
| CoordSize    | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Larghezza e altezza dello spazio delle coordinate all'interno del rettangolo di riferimento di questa forma. Se non è specificato, è uguale alla larghezza e all'altezza del rettangolo. Intervallo compreso tra 0 e infinito. Impostazione predefinita: "1000, 1000".                                                                                               |
| EndAngle     | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Angolo finale della forma.                                                                                                                                                                                                                                                                                          |
| Estrusione    | IVgExtrusion. Specifica il valore dell'oggetto estrusione per la forma. Per informazioni dettagliate, vedere l'elemento [estrusione](msdn-online-vml-extrusion-element.md) .                                                                                                                                                                                                                               |
| Fill         | VgFillFormat. Specifica il valore di riempimento per questa forma. Per ulteriori informazioni, vedere l'elemento [Fill](msdn-online-vml-fill-element.md) .                                                                                                                                                                                                                                                |
| FillColor    | [IVgColor](msdn-online-vml-ivgcolor.md). Colore principale del pennello da utilizzare per riempire il percorso di questa forma.                                                                                                                                                                                                                                                                  |
| Compilato       | [VgTriState](msdn-online-vml-vgtristate.md). Se true, verrà riempito il percorso che definisce la forma. Per impostazione predefinita, verrà riempito con un colore a tinta unita a meno che non esista un sottoelemento Fill che specifica proprietà di riempimento più complesse. Se false, il riempimento è trasparente.                                                                                                           |
| Capovolgi         | VgFlipOrientation. I valori sono: X Y XY YX                                                                                                                                                                                                                                                                                                                                         |
| ForceDash    | [VgTriState](msdn-online-vml-vgtristate.md). Indica che deve essere eseguito il rendering di un contorno tratteggiato quando non è presente alcuna riga e nessun riempimento per una forma. Questo comportamento è in genere utile per rendere visibili le forme invisibili nella modifica delle applicazioni in modo che possano essere selezionate e utilizzate, ad esempio in una mappa immagine.                                                                 |
| Formule     | IVgFormulas. Matrice di formule che definisce una forma.                                                                                                                                                                                                                                                                                                                          |
| Da         | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto iniziale della linea.                                                                                                                                                                                                                                                                                                   |
| HRef         | [Stringa](#data-types-used-in-the-vml-object-model). URL a cui passare se si fa clic sulla forma.                                                                                                                                                                                                                                                                                 |
| ImageData    | IVgImageData. Informazioni sull'immagine se la forma è un'immagine. Per ulteriori informazioni, vedere l'elemento ImageData.                                                                                                                                                                                                                                                                       |
| OnEd         | [VgTriState](msdn-online-vml-vgtristate.md). Nasconde tutti gli handle ad eccezione della parte superiore sinistra e della parte inferiore destra, come negli handle per un segmento di linea retta.                                                                                                                                                                                                                             |
| Opacità      | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Opacità dell'intera forma. Numero compreso tra 0,0 e 1,0.                                                                                                                                                                                                                                                           |
| Percorso         | IVgPath. Stringa contenente i comandi che definiscono il percorso.                                                                                                                                                                                                                                                                                                                  |
| Punti       | [IVgPoints](msdn-online-vml-ivgpoints-data-type.md). Raccolta di punti che definiscono una forma.                                                                                                                                                                                                                                                                                   |
| Stampa        | [VgTriState](msdn-online-vml-vgtristate.md). Se true, la forma deve essere stampata.                                                                                                                                                                                                                                                                                        |
| Rotazione     | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Imposta la rotazione della forma. Il valore viene propagato allo stile della forma.                                                                                                                                                                                                                                              |
| Scalabilità        | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Scala della forma.                                                                                                                                                                                                                                                                                                           |
| Ombreggiatura       | IVgShadow. Specifica l'ombreggiatura per questa forma. Per informazioni dettagliate, vedere l'elemento [shadow](msdn-online-vml-shadow-element.md) .                                                                                                                                                                                                                                                        |
| SPT          | Riservato.                                                                                                                                                                                                                                                                                                                                                                        |
| StartAngle   | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Angolo iniziale della forma.                                                                                                                                                                                                                                                                                        |
| Stroke       | VgStrokeFormat. Per informazioni dettagliate, vedere elemento Stroke.                                                                                                                                                                                                                                                                                                                                  |
| StrokeColor  | [IVgColor](msdn-online-vml-ivgcolor.md). Colore principale del pennello da utilizzare per tracciare il percorso di questa forma.                                                                                                                                                                                                                                                                |
| Tracciato      | [VgTriState](msdn-online-vml-vgtristate.md). Se true, verrà tracciato il percorso che definisce la forma.                                                                                                                                                                                                                                                                              |
| StrokeWeight | [VGLength](msdn-online-vml-vglength.md). Larghezza del pennello da utilizzare per tracciare il tracciato. Intervallo compreso tra 0 e 1584.                                                                                                                                                                                                                                                           |
| TextPath     | IVgTextPath. Specifica l'oggetto TextPath della forma. Per ulteriori informazioni, vedere l'elemento [TextPath](msdn-online-vml-textpath-element.md) .                                                                                                                                                                                                                                  |
| A           | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto finale della linea.                                                                                                                                                                                                                                                                                                        |
| Tipo         | Stringa. Tipo di forma.                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a>Sottoelementi dell'elemento Shape

I sottoelementi seguenti fanno parte del modello a oggetti la.

-   [Background](#background-element)
-   [Estrusione](#extrusion-element)
-   [Fill](#fill-element)
-   [Gruppo](#group-element)
-   [ImageData](#imagedata-element)
-   [Percorso](#path-element)
-   [Shadow](#shadow-element)
-   [Sfasamento](#skew-element)
-   [Stroke](#stroke-element)
-   [TextPath](#textpath-element)

### <a name="background-element"></a>Elemento background

Descrive il riempimento dello sfondo di una pagina usando Fill la.

**Attributes (Attributi)**



|           |                                                                                                                                                                                         |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BWMode    | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Determina la modalità di rendering della forma nella visualizzazione in bianco e nero nelle applicazioni o quando viene stampata.                                     |
| BWNormal  | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Quando BWMode è auto, viene consultata questa proprietà per il rendering della forma in bianco e nero normale.                        |
| BWPure    | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Quando BWMode è auto, viene consultata questa proprietà per il rendering della forma in bianco e nero puro.                          |
| Fill      | VgFillFormat. Specifica il riempimento per questa forma. Per ulteriori informazioni, vedere elemento [Fill](msdn-online-vml-fill-element.md) .                                                             |
| FillColor | [IVgColor](msdn-online-vml-ivgcolor.md). Colore principale del pennello da utilizzare per riempire il percorso di questa forma. Duplicato del valore del colore nell'elemento Fill. Il valore predefinito è bianco. |



 

### <a name="extrusion-element"></a>Elemento Extrusion

Descrive un'estrusione 3D della forma.

**Attributes (Attributi)**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>AutoRotationCenter</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Se true, il centro di rotazione del gruppo di oggetti 3D (in effetti esiste solo un oggetto nel gruppo) viene determinato automaticamente come il centro del gruppo. in caso contrario, viene determinato dai parametri RotationCenter, che sono una frazione della forma con 0, 0, 0 che corrisponde al centro.</td>
</tr>
<tr class="even">
<td>Backdepth</td>
<td><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>. Quantità di estrusione a ritroso. È compreso tra 0 e 32767.</td>
</tr>
<tr class="odd">
<td>Luminosità</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Luminosità complessiva della scena. Il valore predefinito è &quot; 20.000 &quot; .</td>
</tr>
<tr class="even">
<td>Colore</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Colore dell'estrusione. Usato solo se ColorMode è Custom. In caso contrario, imposta automaticamente il colore dell'effetto Estrusione sullo stesso FillColor.</td>
</tr>
<tr class="odd">
<td>ColorMode</td>
<td>Vg3DColorMode. I valori possibili sono:
<ul>
<li>Automatico (impostazione predefinita)</li>
<li>Personalizzato</li>
</ul></td>
</tr>
<tr class="even">
<td>Diffusione</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Rapporto tra evento imprevisto e riflesso chiaro. I valori minori di 1,0 sono normali, ma i valori superiori a uno possono generare effetti interessanti.</td>
</tr>
<tr class="odd">
<td>Microsoft Edge</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Imposta la dimensione di un bordo smussato arrotondato simulato. Varia da 0 a 32767 in PTS a virgola mobile. Il valore predefinito è &quot; 1Pt &quot; .</td>
</tr>
<tr class="even">
<td>Facet</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Imposta il facet della scena. Il valore predefinito è &quot; 30.000 &quot; .</td>
</tr>
<tr class="odd">
<td>ForeDepth</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Quantità di estrusione di avanzamento. È compreso tra 0 e 32767.</td>
</tr>
<tr class="even">
<td>LightFace</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Determimes se il front-end dell'oggetto risponderà alle modifiche nell'illuminazione 3D, ad esempio quando un oggetto viene ruotato.</td>
</tr>
<tr class="odd">
<td>LightHarsh</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Illuminazione rigida per la fonte di luce primaria. Il valore predefinito è False.</td>
</tr>
<tr class="even">
<td>LightHarsh2</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Illuminazione rigida per la sorgente di luce secondaria. Il valore predefinito è False.</td>
</tr>
<tr class="odd">
<td>LightLevel</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>. Intensità della sorgente di luce primaria. Il valore predefinito è &quot; 38000 &quot; .</td>
</tr>
<tr class="even">
<td>LightLevel2</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>. Intensità della sorgente di luce secondaria. Il valore predefinito è &quot; 38000 &quot; .</td>
</tr>
<tr class="odd">
<td>Posizioneilluminazione</td>
<td>Vector3D. Posizione della sorgente di luce primaria. Il valore predefinito è &quot; 50000, 0, 10000 &quot; .</td>
</tr>
<tr class="even">
<td>LightPosition2</td>
<td>Vector3D. Posizione della sorgente di luce secondaria. Il valore predefinito è &quot; -50000, 0, 10000 &quot; .</td>
</tr>
<tr class="odd">
<td>LockRotationCenter</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. &quot;Lockrotationcenter &quot; significa che la rotazione del gruppo è definita in base all'angolo di rotazione [1] gradi sull'asse y della pagina, seguito da angolo di rotazione [0] gradi sull'asse x. Quando LockRotationCenter è false, la rotazione viene definita in base ai gradi dell'angolo di orientamento del vettore definito dall'orientamento. Quindi, ad esempio, lockrotationcenter = false OrientationAngle = 45 Orientation = (0, 1, 0) equivale a lockrotationcenter = true RotationAngle = (0, 45).</td>
</tr>
<tr class="even">
<td>Metallico</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Fa in modo che la luce riflessa in modo speculare sia il colore del materiale anziché il colore della sorgente di luce, rendendo l'oggetto più metallico.</td>
</tr>
<tr class="odd">
<td>Attivato</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Attiva e disattiva la visualizzazione dell'effetto estrusione.</td>
</tr>
<tr class="even">
<td>Orientamento</td>
<td>Vector3D. Orientamento della fotocamera.</td>
</tr>
<tr class="odd">
<td>OrientationAngle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. Angolo tra l'orientamento della fotocamera e il piano XY.</td>
</tr>
<tr class="even">
<td>Aereo</td>
<td>Vg3DExtrudePlane. Consente l'estrusione da piani ortogonali al piano dello schermo. È necessario specificare ForeDepth e backdepth nelle unità di disegno anziché in emù. I valori possibili sono:
<ul>
<li>XY</li>
<li>ZX</li>
<li>YZ</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rendering</td>
<td>Vg3DRenderMode. I valori possibili sono:
<ul>
<li>Solid (valore predefinito)</li>
<li>WireFrame</li>
<li>BoundingCube</li>
</ul></td>
</tr>
<tr class="even">
<td>RotationAngle</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. AngleX, AngleY o AngleZ è controllato dall'attributo ShapeRotation.</td>
</tr>
<tr class="odd">
<td>RotationCenter</td>
<td>Vector3D. Centro di rotazione.</td>
</tr>
<tr class="even">
<td>Lucentezza</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Determina il modo in cui la reflection speculare è concentrata o distribuita. Un valore elevato è da 8 a 10 e si avvicinerà a un mirror e un valore basso sarebbe da 2 a 3 e avrebbe approssimato gli indumenti paillettes. Sono consigliati i valori da 3 a 7. I valori elevati riflettono le fonti di luce.</td>
</tr>
<tr class="odd">
<td>SkewAmt</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>. Se il tipo è parallelo, l'attributo determina la quantità di asimmetria. È compreso tra 0 e 100.</td>
</tr>
<tr class="even">
<td>SkewAngle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. Se il tipo è parallelo, l'attributo determina il grado di asimmetria. Il valore predefinito è &quot; -45 &quot; .</td>
</tr>
<tr class="odd">
<td>Specularità</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Rapporto tra evento imprevisto e riflesso chiaro. I valori minori di 1,0 sono normali, ma i valori superiori a uno possono generare effetti interessanti.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td>VgExtrusionType. I valori possibili sono:
<ul>
<li>Parallel (impostazione predefinita)</li>
<li>Prospettiva</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vista</td>
<td>Vector3D. Punto da cui viene visualizzata la scena.</td>
</tr>
<tr class="even">
<td>ViewpointOrigin</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Il valore di può essere compreso tra 0,5 e-0,5 per posizionare l'origine del punto di vista nel rettangolo di delimitazione della forma.</td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a>Fill (elemento)

Descrive il modo in cui deve essere compilato un percorso per riempimenti più complessi rispetto a un colore a tinta unita.

**Attributes (Attributi)**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>AlignShape</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Allineare l'immagine alla forma. Se false, allineare l'immagine con la finestra.</td>
</tr>
<tr class="even">
<td>Angle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. Angolo lungo il quale viene rilasciata la sfumatura. 0 gradi si trova lungo l'asse orizzontale da sinistra a destra.</td>
</tr>
<tr class="odd">
<td>Aspetto</td>
<td><strong>VgAspectType</strong>. L'attributo ImageSize verrà regolato in modo da mantenere l'aspetto dell'immagine. I possibili valori sono:
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignora</td>
<td>Ignorare i problemi di aspetto.</td>
</tr>
<tr class="even">
<td>AtLeast</td>
<td>L'immagine è almeno uguale alla dimensione dell'immagine.</td>
</tr>
<tr class="odd">
<td>AtMost</td>
<td>L'immagine non è più grande delle dimensioni dell'immagine.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Colore</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> Colore di riempimento principale. Uguale all'attributo FillColor nella forma.</td>
</tr>
<tr class="odd">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Colore secondario per un riempimento quando il tipo di immagine è motivo o riempimento sfumato.</td>
</tr>
<tr class="even">
<td>Colori</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>. Colori intermedi nella sfumatura e relative posizioni lungo la sfumatura, ad esempio &quot; 30% rosso, 70% blu, 90% verde &quot; . Il colore primario (attributo color nella forma) è 0% e il colore secondario (attributo color2) è 100%.</td>
</tr>
<tr class="odd">
<td>Focus</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>. Punto focale del riempimento lineare sfumato. I valori vanno da-100 a + 100.</td>
</tr>
<tr class="even">
<td>FocusPosition</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Posizione del rettangolo più interno per le sfumature radiali. Il vettore è una frazione (0,0-1,0) della larghezza e dell'altezza della forma.</td>
</tr>
<tr class="odd">
<td>FocusSize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Dimensioni del rettangolo più interno per le sfumature radiali. Il vettore è una frazione (da 0,0 a 1,0) della larghezza e dell'altezza della forma.</td>
</tr>
<tr class="even">
<td>Metodo</td>
<td>VgSigmaType. I possibili valori sono:
<ul>
<li>nessuno</li>
<li>Lineari</li>
<li>Sigma</li>
<li>Qualsiasi</li>
</ul>
<p>Il valore predefinito è Sigma.</p></td>
</tr>
<tr class="odd">
<td>Attivato</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Attiva la visualizzazione del riempimento. Uguale all'attributo Fill nella forma.</td>
</tr>
<tr class="even">
<td>Opacità</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacità del riempimento.</td>
</tr>
<tr class="odd">
<td>Opacity2</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacità secondaria per le sfumature.</td>
</tr>
<tr class="even">
<td>Origine</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Punto relativo all'angolo superiore sinistro dell'immagine trattata come origine dell'immagine. Il valore predefinito è il centro dell'immagine. Il vettore è una frazione (da 0,0 a 1,0) della larghezza e dell'altezza dell'immagine.</td>
</tr>
<tr class="odd">
<td>Posizione</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Puntare il rettangolo di riferimento della forma per posizionare l'origine dell'immagine. Il valore predefinito è il centro del rettangolo del contenitore. Il vettore è una frazione (0,0-1,0) della larghezza e dell'altezza dell'immagine.</td>
</tr>
<tr class="even">
<td>Dimensione</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Dimensione dell'immagine. Il valore predefinito è la dimensione in pixel dell'immagine. Può essere specificato in coordinate assolute o in percentuale.</td>
</tr>
<tr class="odd">
<td>Src</td>
<td><a href="#data-types-used-in-the-vml-object-model">Stringa</a>. URL di un'immagine da caricare per le compilazioni di immagini e modelli. Questo attributo deve essere sempre presente e puntare a dati di immagine validi affinché venga visualizzata un'immagine.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td>VgFillType. indicati di seguito.
<ul>
<li>Sfondo</li>
<li>Frame</li>
<li>Sfumatura</li>
<li>GradientCenter</li>
<li>GradientRadial</li>
<li>GradientTitle</li>
<li>GradientUnscaled</li>
<li>Modello</li>
<li>Tinta unita</li>
<li>Tile</li>
</ul>
Il riquadro, il pattern e il frame richiedono gli attributi di immagine da fornire. Gradient e GradientRadial richiedono che vengano forniti gli attributi di sfumatura.</td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a>Group - elemento

Un gruppo è una raccolta di forme singole che possono essere posizionate e trasformate come unità.



|        |                                                                                              |
|--------|----------------------------------------------------------------------------------------------|
| Elemento   | [IVgShape](#data-types-used-in-the-vml-object-model). Elemento specificato nella matrice di forme. |
| Length | [Integer](#data-types-used-in-the-vml-object-model). Numero di forme in questo gruppo.         |



 

### <a name="imagedata-element"></a>Elemento ImageData

Descrive un'immagine di cui eseguire il rendering su una forma.



|             |                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bilivello     | [VgTriState](msdn-online-vml-vgtristate.md). Visualizza l'immagine solo in due colori, in genere nero e bianco.                                                                                                                                                                                                                                                     |
| BlackLevel  | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Consente la regolazione per impostare il livello in modo che i neri appaiano come veri neri e tutti gli altri colori siano visibili come ombreggiatura sopra il nero.                                                                                                                                                                        |
| Chromakey   | [IVgColor](msdn-online-vml-ivgcolor.md). Colore trasparente dell'immagine.                                                                                                                                                                                                                                                                                         |
| CropBottom  | [VgNumber](#data-types-used-in-the-vml-object-model). Distanza di ritaglio dalla parte inferiore dell'immagine espressa come percentuale delle dimensioni dell'immagine.                                                                                                                                                                                                                           |
| CropLeft    | [VgNumber](#data-types-used-in-the-vml-object-model). Distanza di ritaglio dal bordo sinistro dell'immagine espressa come frazione delle dimensioni dell'immagine (da 0,0 a 1,0). Tuttavia, il "out-ritaglio" è supportato e pertanto sono supportati i valori minori di 0 e maggiori di 1. ad esempio,-5, 20 dovrebbe ritagliare i limiti 25X le dimensioni dell'immagine con 4/5 su un lato dell'immagine. |
| CropRight   | [VgNumber](#data-types-used-in-the-vml-object-model). Distanza di ritaglio rispetto a destra dell'immagine espressa come percentuale delle dimensioni dell'immagine.                                                                                                                                                                                                                            |
| CropTop     | [VgNumber](#data-types-used-in-the-vml-object-model). Distanza di ritaglio dalla parte superiore dell'immagine espressa come percentuale delle dimensioni dell'immagine.                                                                                                                                                                                                                              |
| EmbossColor | [IVgColor](msdn-online-vml-ivgcolor.md). Questa proprietà è impostata su una percentuale del colore di ombreggiatura per creare un effetto immagine in rilievo.                                                                                                                                                                                                                                 |
| Ottenere        | [VgPositiveNumber](#data-types-used-in-the-vml-object-model). Regola l'intensità di tutti i colori. In sostanza, imposta la luminosità del bianco. È compreso tra 0 e 32767.                                                                                                                                                                                           |
| Gamma       | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Correzione gamma. Aumentando il numero di immagini, si ottiene un contrasto maggiore.                                                                                                                                                                                                                                           |
| GrayScale   | [VgTriState](msdn-online-vml-vgtristate.md). Visualizza l'immagine nei colori in scala di grigi.                                                                                                                                                                                                                                                                              |
| Src         | [Stringa](#data-types-used-in-the-vml-object-model). URL di un'immagine da caricare per le compilazioni di immagini e modelli. Questo attributo deve essere sempre presente e puntare a dati di immagine validi affinché venga visualizzata un'immagine.                                                                                                                                                           |



 

### <a name="path-element"></a>Path - elemento

Definisce il percorso che costituisce la forma, usando una stringa che contiene un set completo di comandi "movimento penna".



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Limousine</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>. Definisce il punto in cui la forma è allungata. ad esempio, per una forma giraffa, il punto di limo si trova sul collo in modo che quando la forma viene ridimensionata, il collo si estenderà e il resto della forma manterrà le dimensioni.</td>
</tr>
<tr class="even">
<td>TextBoxRect</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>. Matrice contenente i rettangoli che definiscono la posizione in cui deve essere inserito il testo.</td>
</tr>
<tr class="odd">
<td>V</td>
<td><a href="#data-types-used-in-the-vml-object-model">Stringa</a>. Corrisponde all'attributo v nel tag Path. Si noti che il percorso può corrispondere all'attributo o all'elemento Path.</td>
</tr>
<tr class="even">
<td>Valore</td>
<td><a href="#data-types-used-in-the-vml-object-model">Stringa</a>. Rappresentazione testuale dei comandi che definiscono il percorso. I valori delle coordinate X o y possono essere un riferimento a una formula nel formato &quot; @# &quot; dove # è il numero ordinale della formula, ad esempio &quot; . @2 &quot; Questa stringa di attributo è costituita da un set completo di comandi, inclusi i seguenti: <br/> 
<table>
<thead>
<tr class="header">
<th>Comando</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AE (angleellipseto)</td>
<td><strong>dimensioni</strong> <strong>centrali</strong>(x, y) (w, h) <strong>Inizio-angolo</strong>, <strong>angolo finale</strong><br/> Creare un segmento di un'ellisse. Viene disegnata una linea retta dal punto corrente al punto iniziale del segmento.<br/></td>
</tr>
<tr class="even">
<td>al (angleelipse)</td>
<td>Uguale a AE ad eccezione del fatto che esiste un m implicito al punto iniziale del segmento.</td>
</tr>
<tr class="odd">
<td>AR (Arc)</td>
<td>Uguale a. Tuttavia, un nuovo sottopercorso viene avviato da un m implicito al punto iniziale dell'arco.</td>
</tr>
<tr class="even">
<td>all'indirizzo (ArcTo)</td>
<td><strong>Left</strong>, <strong>Top</strong>, <strong>right</strong>, <strong>Bottom</strong>, <strong>Start</strong>(x, y) <strong>end</strong>(x, y) <br/> I primi quattro valori definiscono il rettangolo di delimitazione di un'ellisse. Le ultime quattro definiscono due vettori radiali. Viene disegnato un segmento dell'ellisse che inizia in corrispondenza dell'angolo definito dal vettore RADIUS iniziale e termina in corrispondenza dell'angolo definito dal vettore finale. Viene disegnata una linea retta dal punto corrente all'inizio dell'arco. L'arco viene sempre disegnato in senso antiorario. <br/></td>
</tr>
<tr class="odd">
<td>c (curveTo)</td>
<td><strong>Control1</strong>(x, y) <strong>controllo2</strong>(x, y) <strong>a</strong>(x, y) <br/> Consente di creare una curva di Bezier cubica dal punto corrente alla coordinata fornita dai due parametri finali, ovvero i punti di controllo forniti dai primi quattro parametri. Il punto corrente diventa l'endpoint di Bezier.<br/></td>
</tr>
<tr class="even">
<td>e (fine)</td>
<td>Termina il set corrente di sottopercorsi. Un set specificato di sottopercorsi (delimitati da end) viene riempito usando eofill. I set successivi di sottopercorsi vengono compilati in modo indipendente e sovrapposti a quelli esistenti.</td>
</tr>
<tr class="odd">
<td>l (LineTo)</td>
<td>x, y<br/> Consente di creare una linea dal punto corrente alla coordinata x, y specificata, che diventa il nuovo punto corrente. È possibile specificare coppie di coordinate aggiuntive per formare una polilinea, ad esempio &quot; l 10, 13, 45, 27, 89,-12 &quot; .<br/></td>
</tr>
<tr class="even">
<td>m (MoveTo)</td>
<td>x, y<br/> Avvia un nuovo sottopercorso in corrispondenza della coordinata x, y specificata.<br/></td>
</tr>
<tr class="odd">
<td>NF (NoFill)</td>
<td>Il set corrente di sottopercorsi (delimitati da end) non verrà compilato.</td>
</tr>
<tr class="even">
<td>NS (noStroke)</td>
<td>Il set corrente di sottopercorsi (delimitati da end) non verrà tracciato.</td>
</tr>
<tr class="odd">
<td>QB (quadraticbezier)</td>
<td>(<strong>ControlPoint</strong>(x, y)) *,<strong>end</strong>(x, y) <br/> Definisce una o più curve di Bézier quadratiche per mezzo di punti di controllo e un endpoint. I punti intermedi (su curva) sono ottenuti dall'interpolazione tra punti di controllo successivi simili a tipi di carattere TrueType. Il sottopercorso non deve essere un inizio, nel qual caso il sottopercorso viene chiuso e l'ultimo punto definisce il punto iniziale.<br/></td>
</tr>
<tr class="even">
<td>QX (ellipticalquadrantx)</td>
<td><strong>fine</strong>(x, y) <br/> Viene disegnato un ellisse del trimestre dal punto corrente all'endpoint specificato. Il segmento ellittico è inizialmente tangente a una linea parallela all'asse x. ovvero, il segmento inizia orizzontalmente.<br/></td>
</tr>
<tr class="odd">
<td>QY (ellipticalquadranty)</td>
<td><strong>fine</strong>(x, y) <br/> Uguale a QX, ad eccezione del fatto che il segmento ellittico è inizialmente tangente a una linea parallela all'asse y. ovvero, il segmento inizia verticalmente.<br/></td>
</tr>
<tr class="even">
<td>r (rlineto)</td>
<td>x, y <br/> Consente di creare una linea dal punto corrente alla coordinata relativa (CPX + x, CPY + y). Se vengono fornite coppie di coordinate aggiuntive, ogni nuovo punto viene calcolato in relazione all'ultima.<br/></td>
</tr>
<tr class="odd">
<td>t (rmoveto)</td>
<td>x, y<br/> Avviare un nuovo sottopercorso in corrispondenza delle coordinate relative (CPX + x, CPY + y) dove CPX, CPY è la posizione corrente. <br/></td>
</tr>
<tr class="even">
<td>v (curveTo)</td>
<td><strong>Control1</strong>(x, y) <strong>controllo2</strong>(x, y) <strong>a</strong> (x, y) <br/> Curva di Bezier cubica usando le coordinate specificate rispetto al punto corrente. Tutti i punti vengono calcolati in relazione allo stesso punto di partenza.<br/></td>
</tr>
<tr class="odd">
<td>WA (clockwisearcto)</td>
<td>Uguale a, ma l'arco viene disegnato in senso orario.</td>
</tr>
<tr class="even">
<td>WR (clockwisearc)</td>
<td>Uguale a AR ma viene disegnato in senso orario.</td>
</tr>
<tr class="odd">
<td>x (Chiudi)</td>
<td>Chiudere il sottopercorso corrente disegnando una linea retta dal punto corrente al punto MoveTo originale.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a>Elemento Shadow

Descrive un effetto ombreggiatura su una forma.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Colore</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Colore dell'ombreggiatura primaria. Il valore predefinito è RGB (128128128)</td>
</tr>
<tr class="even">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Colore della seconda ombreggiatura o evidenziazione in un'ombreggiatura goffrata o incisa. Il valore predefinito è RGB (203203203).</td>
</tr>
<tr class="odd">
<td>Matrice</td>
<td><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>. Una matrice di trasformazione prospettica nel formato &quot; SXX, SXY, SYX, SYY, px, py &quot; [s = scale, p = Perspective]. Gli elementi s specificano il modo in cui deve essere ridimensionata l'ombreggiatura rispetto alla forma e gli elementi p specificano come deve essere inclinata l'ombreggiatura rispetto alla forma. Ad esempio, la matrice seguente ridimensiona la forma in base a un fattore 2 e la inclina per un fattore di 4 in tutte le direzioni: <br/> &quot;2, 2, 2, 2, 4, 4&quot;<br/> Questa matrice viene utilizzata solo se il tipo dell'ombreggiatura è impostato sulla prospettiva.<br/></td>
</tr>
<tr class="even">
<td>Nascosto</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. L'ombreggiatura può essere visualizzata se non è presente alcun riempimento della forma. Il valore predefinito è False.</td>
</tr>
<tr class="odd">
<td>Offset</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>. Quantità di offset x, y dalla posizione della forma. Il valore predefinito è &quot; 2PT, 2PT &quot; .</td>
</tr>
<tr class="even">
<td>Offset2</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Quantità di offset x, y secondo rispetto alla posizione della forma? s. I valori sono una misura assoluta o un valore frazionario della forma (da-0,5 a + 0,5).</td>
</tr>
<tr class="odd">
<td>Attivato</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Attiva e disattiva la visualizzazione dell'ombreggiatura.</td>
</tr>
<tr class="even">
<td>Opacità</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacità dell'effetto di ombreggiatura.</td>
</tr>
<tr class="odd">
<td>Origine</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Coppia di valori frazionari della forma da-0,5 a + 0,5.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgShadowType</a>. I valori possibili sono:
<ul>
<li>Single (impostazione predefinita)</li>
<li>Double</li>
<li>Prospettiva</li>
<li>ShapeRelative</li>
<li>DrawingRelative</li>
<li>Rilievo</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="skew-element"></a>Elemento asimmetria

Descrive un effetto di inclinazione della prospettiva su una forma. L'inclinazione viene applicata ai dati grafici vettoriali, non ai dati di immagine.



|        |                                                                                                                                                                                                                                                                                    |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Matrice | [IVgSkewMatrix](#data-types-used-in-the-vml-object-model). Una matrice di trasformazione della prospettiva nel formato "SXX, SXY, SYX, SYY, px, py" \[ s = scale, p = Perspective \] . Se l'offset è in unità assolute, il px, py si trovano in unità Emu ^-1; in caso contrario, si tratta di una frazione inversa della dimensione della forma. |
| Offset | [IvgSkewOffset](#data-types-used-in-the-vml-object-model). Quantità di offset x, y dalla posizione della forma. Il valore predefinito è "2PT, 2PT".                                                                                                                                                   |
| Attivato     | [VgTriState](msdn-online-vml-vgtristate.md). Attiva o disattiva la visualizzazione della distorsione.                                                                                                                                                                                             |
| Origine | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Coppia di valori frazionari della forma da-0,5 a + 0,5.                                                                                                                                                                     |



 

### <a name="stroke-element"></a>Stroke-elemento

Viene descritto come tracciare il percorso se si desidera un elemento che supera una linea continua con un colore a tinta unita.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Colore</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Colore della linea. Uguale all'attributo StrokeColor nella forma, ma ne esegue l'override.</td>
</tr>
<tr class="even">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Colore secondario. Utilizzato quando elemento FillType è pattern.</td>
</tr>
<tr class="odd">
<td>DashStyle</td>
<td><strong>VgLineDashStyle</strong>. Formato di stile Dash. Può essere un valore specifico o una sequenza di numeri con un modello Dash definito dall'utente. I valori possibili sono:
<ul>
<li>Solid (valore predefinito)</li>
<li>ShortDash</li>
<li>ShortDot</li>
<li>ShortDashDot</li>
<li>ShortDashDotDot</li>
<li>Punto</li>
<li>Trattino</li>
<li>DashDot</li>
<li>LongDash</li>
<li>LongDashDot</li>
<li>LongDashDotDot</li>
</ul></td>
</tr>
<tr class="even">
<td>EndArrow</td>
<td><strong>VgArrowheadStyle</strong>. Freccia per la fine della riga. I valori possibili sono:
<ul>
<li>Nessuno (valore predefinito)</li>
<li>Blocca</li>
<li>Classic</li>
<li>Diamond</li>
<li>Ovale</li>
<li>Apri</li>
<li>Frecce di espansione</li>
<li>DoubleChevron</li>
</ul></td>
</tr>
<tr class="odd">
<td>EndArrowLength</td>
<td><strong>VgArrowHeadLength</strong>. Lunghezza della freccia per la fine della riga. I valori possibili sono:
<ul>
<li>Short</li>
<li>Media (impostazione predefinita)</li>
<li>long</li>
</ul></td>
</tr>
<tr class="even">
<td>EndArrowWidth</td>
<td><strong>VgArrowheadWidth</strong>. Larghezza della freccia per la fine della riga. I valori possibili sono:
<ul>
<li>Limitare</li>
<li>Media (impostazione predefinita)</li>
<li>Largo</li>
</ul></td>
</tr>
<tr class="odd">
<td>EndCap</td>
<td><strong>VgLineEndCapStyle</strong>. I valori possibili sono:
<ul>
<li>Semplice</li>
<li>Square</li>
<li>Round</li>
</ul></td>
</tr>
<tr class="even">
<td>Elemento FillType</td>
<td><strong>VgLineFillType</strong>. I valori possibili sono:
<ul>
<li>Solid (valore predefinito)</li>
<li>Tile</li>
<li>Modello</li>
<li>Frame</li>
</ul></td>
</tr>
<tr class="odd">
<td>ImageAlignShape</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Allineare l'immagine alla forma. Se false, allineare l'immagine con la finestra.</td>
</tr>
<tr class="even">
<td>ImageAspect</td>
<td><strong>VgAspectType</strong>. L'attributo ImageSize verrà regolato in modo da mantenere l'aspetto dell'immagine. I possibili valori sono:
<table>
<thead>
<tr class="header">
<th>Valore</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ignora</td>
<td>Ignorare i problemi di aspetto.</td>
</tr>
<tr class="even">
<td>AtLeast</td>
<td>L'immagine è almeno uguale alla dimensione dell'immagine.</td>
</tr>
<tr class="odd">
<td>AtMost</td>
<td>L'immagine non è più grande delle dimensioni dell'immagine.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>ImageSize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Dimensione dell'immagine con cui formare il pennello. Il valore predefinito corrisponde alla dimensione dell'immagine.</td>
</tr>
<tr class="even">
<td>JoinStyle</td>
<td><strong>VgLineJoinStyle</strong>. I valori possibili sono:
<ul>
<li>Round (misto arrotondato)</li>
<li>Smussato (misto smussato)</li>
<li>Miter (misto smussato)</li>
</ul></td>
</tr>
<tr class="odd">
<td>LineStyle</td>
<td><strong>VgLineStyle</strong>. I valori possibili sono:
<ul>
<li>Single</li>
<li>ThinThin (1:1:1)</li>
<li>ThinThick (1:1:2)</li>
<li>ThickThin (2:1:1)</li>
<li>ThickBetweenThin (1:1:2:1:1)</li>
</ul></td>
</tr>
<tr class="even">
<td>MiterLimit</td>
<td><a href="msdn-online-vml-vglength.md">Lunghezza</a>. Distanza massima tra il punto interno e il punto esterno di una giunzione. Questo numero è un multiplo dello spessore della linea. È compreso tra 0 e 32.767.</td>
</tr>
<tr class="odd">
<td>Attivato</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Attiva e disattiva la visualizzazione della riga. Uguale all'attributo Stroke nella forma, ma ne esegue l'override.</td>
</tr>
<tr class="even">
<td>Opacità</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacità del tratto.</td>
</tr>
<tr class="odd">
<td>Src</td>
<td>Stringa. URL di un'immagine da caricare per le compilazioni di immagini e modelli. Questo attributo deve essere sempre presente e puntare a dati di immagine validi affinché venga visualizzata un'immagine.</td>
</tr>
<tr class="even">
<td>StartArrow</td>
<td><strong>VgArrowheadStyle</strong>. Freccia per l'inizio della riga. I valori possibili sono:
<ul>
<li>Nessuno (valore predefinito)</li>
<li>Blocca</li>
<li>Classic</li>
<li>Diamond</li>
<li>Ovale</li>
<li>Apri</li>
<li>Frecce di espansione</li>
<li>DoubleChevron</li>
</ul></td>
</tr>
<tr class="odd">
<td>StartArrowLength</td>
<td>VgArrowHeadLength. Lunghezza della freccia per l'inizio della riga. I valori possibili sono:
<ul>
<li>Short</li>
<li>Media (impostazione predefinita)</li>
<li>long</li>
</ul></td>
</tr>
<tr class="even">
<td>StartArrowWidth</td>
<td>VgArrowheadWidth. Larghezza della freccia per l'inizio della riga. I valori possibili sono:
<ul>
<li>Larghezza media ristretta (predefinita)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Peso</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Larghezza della linea. È compreso tra 0 e 1584.
<div class="alert">
<blockquote>
[!Note]<br />
L'attributo DashStyle consente all'utente di specificare un modello Dash definito in modo personalizzato. Questa operazione viene eseguita usando una serie di numeri. Gli stili Dash sono definiti in termini di lunghezza del trattino (la parte disegnata del tratto) e della lunghezza dello spazio tra i trattini. Le lunghezze sono relative alla lunghezza riga; la lunghezza di &quot; 1 &quot; è uguale alla lunghezza della linea. Lo stile di estremità viene applicato a ogni trattino, mentre gli stili delle frecce non lo sono. La stringa definisce prima di tutto la lunghezza del trattino, quindi la lunghezza dello spazio. Questa operazione può essere ripetuta per formare stili trattini complessi. La stringa deve sempre contenere una coppia di numeri; Se contiene un numero dispari di numeri, l'ultimo può essere ignorato. Nella tabella seguente sono elencati alcuni valori tipici e una descrizione dell'effetto desiderato. &quot;0 indica &quot; un punto che dovrebbe essere quadruplo simmetrico (con round estremità deve essere un cerchio). Se il limite di riga è Flat, un visualizzatore deve scegliere un trattino del sistema operativo predefinito, laddove possibile (ad esempio, un elemento che è veloce da creare). Di seguito sono riportati alcuni esempi.
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td>&quot;2 2&quot;</td>
<td>brevi trattini (ogni trattino e lo spazio tra due corrisponde al doppio della larghezza della linea)</td>
</tr>
<tr class="even">
<td>&quot;1 2&quot;</td>
<td>punto (ogni trattino è la larghezza della linea mentre ogni spazio è il doppio della larghezza della linea)</td>
</tr>
<tr class="odd">
<td>&quot;4 2&quot;</td>
<td>Dash (ogni trattino è quattro volte la larghezza della linea mentre ogni spazio è il doppio della larghezza della linea)</td>
</tr>
<tr class="even">
<td>&quot;8 2&quot;</td>
<td>trattino lungo</td>
</tr>
<tr class="odd">
<td>&quot;4 2 1 2&quot;</td>
<td>punto tratteggiato</td>
</tr>
<tr class="even">
<td>&quot;8 2 1 2&quot;</td>
<td>punto lungo trattino</td>
</tr>
<tr class="odd">
<td>&quot;8 2 1 2 1 2&quot;</td>
<td>punto a trattino lungo</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a>Elemento TextPath

Descrive un percorso vettoriale basato sui dati di testo, il tipo di carattere e gli stili forniti. Il percorso di testo è decurvato per essere conforme a un elemento **path** , se specificato.



|          |                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| FitPath  | [VgTriState](msdn-online-vml-vgtristate.md). Ridimensiona il testo per riempire il percorso su cui si trova.                                 |
| FitShape | [VgTriState](msdn-online-vml-vgtristate.md). Estende il percorso del testo ai bordi della casella della forma.                      |
| Attivato       | [VgTriState](msdn-online-vml-vgtristate.md). Determina se i percorsi dei caratteri sono visualizzati o meno.                    |
| string   | Stringa. Testo di cui eseguire il rendering come percorso di testo.                                                                                    |
| Taglio     | [VgTriState](msdn-online-vml-vgtristate.md). Rimuove qualsiasi spazio aggiuntivo riservato per gli ascendenti e i discendenti se non viene utilizzato. |
| XScale   | [VgTriState](msdn-online-vml-vgtristate.md). Utilizzare la misurazione x dritto anziché misurare lungo il percorso.                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a>Tipi di dati utilizzati nel modello a oggetti la

I tipi di dati seguenti vengono utilizzati dal modello a oggetti la.

-   [Double](/windows)
-   [Fisso](/windows)
-   [Integer](/windows)
-   [IVgAdjustments](/windows)
-   [IVgColor](/windows)
-   [IVgEquation](/windows)
-   [IVgFixedRectangle](/windows)
-   [IVgFixedRectangleArray](/windows)
-   [IVgFormula](/windows)
-   [IVgFormulas](/windows)
-   [IVgGradientColorArray](/windows)
-   [IVgPoints](/windows)
-   [IVgSkewMatrix](/windows)
-   [IVgSkewOffset](/windows)
-   [IVgVector2D](/windows)
-   [IVgVector3D](/windows)
-   [Length](/windows)
-   [Measure](/windows)
-   [Stringa](/windows)
-   [VgBlackWhiteMode](/windows)
-   [VgFraction](/windows)
-   [VgTriState](/windows)

**Tipo di dati Double**

Intero a precisione doppia con intervallo compreso tra-infinito e infinito.

**Tipo di dati Fixed**

Numero a virgola mobile con intervallo compreso tra-32.766,0 e 32.766,0.

**Tipo di dati Integer**

Intero con un intervallo compreso tra-infinito e infinito.

**Tipo di dati IVgAdjustments**

Raccolta di modifiche apportate a una forma che può essere utilizzata per modificare le dimensioni di una forma. Le regolazioni possono essere utilizzate come segnaposti temporanei o per qualsiasi motivo per cui si utilizzano le variabili. Sono presenti solo 8 modifiche nella raccolta.



| Attributi | Descrizione                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exists     | [IVgTriState](msdn-online-vml-vgtristate.md). Determina se esiste una rettifica specificata. Si noti che è necessario utilizzare un indice. ovvero è necessario utilizzare EXISTS (item) per recuperare l'esistenza di un elemento.                                                                                                                                                                   |
| Elemento       | [Long](#data-types-used-in-the-vml-object-model). Matrice di regolazioni indicizzate da 0 a 7. Si noti che le regolazioni possono essere specificate in SPARC; ovvero i valori della matrice intermedia potrebbero non essere sempre compilati. Ad esempio, Item 1, 3 e 5 possono avere valori per una lunghezza di 3, con Item (0), Item (2) e Item (4) specificati. Per verificare se esiste un elemento, usare l'attributo exists. |
| Length     | [Integer](#data-types-used-in-the-vml-object-model). Numero di rettifiche. Non può essere maggiore di 8.                                                                                                                                                                                                                                                                          |
| Valore      | [Stringa](#data-types-used-in-the-vml-object-model). Rappresentazione testuale dei valori numerici, con virgole tra ogni numero.                                                                                                                                                                                                                                                    |



 

**IVgColor**

Specifica un colore.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributi</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>RGB</td>
<td><strong>VgRGBType</strong>. Valore RGB (Long) del colore. Valido solo se il tipo è RGB.</td>
</tr>
<tr class="even">
<td>R</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a>. Componente rosso del colore. Può variare da 0 a 255.</td>
</tr>
<tr class="odd">
<td>G</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a>. Componente verde del colore. Può variare da 0 a 255.</td>
</tr>
<tr class="even">
<td>B</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a>. Componente blu del colore. Può variare da 0 a 255.</td>
</tr>
<tr class="odd">
<td>string</td>
<td><a href="#data-types-used-in-the-vml-object-model">Stringa</a>. Rappresentazione testuale del colore. Sono supportati i seguenti tipi di colori denominati:
<ul>
<li>Nero (#000000)</li>
<li>Argento (#C0C0C0)</li>
<li>Grigio (#808080)</li>
<li>Bianco (#FFFFFF)</li>
<li>Marrone (#800000)</li>
<li>Rosso (#FF0000)</li>
<li>Viola (#800080)</li>
<li>Fucsia (#FF00FF)</li>
<li>Verde (#008000)</li>
<li>Lime (#00FF00)</li>
<li>Olive (#808000)</li>
<li>Giallo (#FFFF00)</li>
<li>Navy (#000080)</li>
<li>Blu (#0000FF)</li>
<li>Verde acqua (#008080)</li>
<li>Aqua (#00FFFF)</li>
</ul></td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><strong>VgColorType</strong>. Tipo di colore. Uno dei tipi seguenti:
<ul>
<li>Mixed</li>
<li>denominata</li>
<li>RGB</li>
<li>Schema</li>
</ul></td>
</tr>
</tbody>
</table>



 

**IVgEquation**

Equazioni utilizzate per le formule.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Operazione</td>
<td><strong>VgEquationOperationType</strong> Nome dell'operazione da eseguire sui parametri. In un'equazione è possibile usare le operazioni seguenti:
<table>
<thead>
<tr class="header">
<th>Operazione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Abs</td>
<td>Valore assoluto. <br/> <strong>ABS</strong>(v) <br/></td>
</tr>
<tr class="even">
<td>Atan2</td>
<td>Aritmetica polare: restituisce unità FD (gradi moltiplicate per 65536).<br/> <strong>Atan2</strong>(P1, v) <br/></td>
</tr>
<tr class="odd">
<td>Cos</td>
<td>Coseno, argomento in unità FD (gradi moltiplicato per 65536).<br/> v * <strong>cos</strong>(P1) <br/></td>
</tr>
<tr class="even">
<td>Cosatan2</td>
<td>Conserva la precisione completa nel calcolo intermedio.<br/> v * <strong>cos (atan2 (</strong> P2, P1 <strong>))</strong><br/></td>
</tr>
<tr class="odd">
<td>Ellisse</td>
<td>Ellisse</td>
</tr>
<tr class="even">
<td>Se</td>
<td>Se il test della condizione. v > 0 <strong>?</strong> P1: P2</td>
</tr>
<tr class="odd">
<td>Max</td>
<td>Maggiore di due valori. <br/> <strong>Max</strong>(v, P1) <br/></td>
</tr>
<tr class="even">
<td>Mid</td>
<td>Media (v + P1)/2</td>
</tr>
<tr class="odd">
<td>Min</td>
<td>Minore di due valori. <strong>min</strong>(v, P1)</td>
</tr>
<tr class="even">
<td>Mod</td>
<td>Modulo.</td>
</tr>
<tr class="odd">
<td>Prodotto</td>
<td>Usato per la moltiplicazione e la divisione. v * P1/P2</td>
</tr>
<tr class="even">
<td>Sin</td>
<td>Seno, argomento in unità FD (gradi moltiplicato per 65536). <br/> v * <strong>sin</strong>(P1) <br/></td>
</tr>
<tr class="odd">
<td>Sinatan2</td>
<td>Conserva la precisione completa nel calcolo intermedio. v * <strong>sin</strong>(<strong>Atan2</strong>(P2, P1))</td>
</tr>
<tr class="even">
<td>Sqrt</td>
<td>Il risultato è positivo e viene arrotondato per difetto. <br/> <strong>Sqrt</strong>(v) <br/></td>
</tr>
<tr class="odd">
<td>Sum</td>
<td>Utilizzato per l'addizione e la sottrazione.<br/> v + P1 P2<br/></td>
</tr>
<tr class="even">
<td>Sumangle</td>
<td>Angolo esistente (ridimensionato di 65536), dove P1 e P2 sono in gradi.<br/> v + P1 * 65536 + P2 * 65536<br/></td>
</tr>
<tr class="odd">
<td>Tan</td>
<td>Tangente, argomento in unità FD (gradi moltiplicato per 65536). <br/> v * Tan (P1)<br/></td>
</tr>
<tr class="even">
<td>Val</td>
<td>Definisce un valore di guida da un altro valore.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Param1</td>
<td><strong>Integer</strong>. Primo parametro.</td>
</tr>
<tr class="odd">
<td>Paramtype1</td>
<td><strong>VgFormulaParamType</strong>. Tipo del primo parametro. Sono supportati i valori seguenti:
<table>
<thead>
<tr class="header">
<th>Tipo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valore</td>
<td>Il parametro è un valore semplice.</td>
</tr>
<tr class="even">
<td>AdjustmentReference</td>
<td>Il parametro è un riferimento a una rettifica. Se, ad esempio, il primo parametro è 1, verrà utilizzato il valore della prima regolazione.</td>
</tr>
<tr class="odd">
<td>FormulaReference</td>
<td>Il parametro è il risultato di un riferimento al risultato di una formula precedente. Se, ad esempio, il primo parametro è 2, verrà utilizzato il risultato della formula 2.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Param2</td>
<td><strong>Integer</strong>. Secondo parametro.</td>
</tr>
<tr class="odd">
<td>Paramtype2</td>
<td><strong>VgFormulaParamType</strong> Tipo di parametro 2.</td>
</tr>
<tr class="even">
<td>Val</td>
<td><strong>Integer</strong>. Risultato.</td>
</tr>
<tr class="odd">
<td>Valtype2</td>
<td><strong>VgFormulaParamType</strong>. Tipo del risultato.</td>
</tr>
</tbody>
</table>



 

**IVgFixedRectangle**

Specifica un rettangolo fisso.



| Attributi | Descrizione                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Valore      | [Stringa](#data-types-used-in-the-vml-object-model). Valore di testo che specifica il percorso.         |
| Sinistra       | [Valore Double](#data-types-used-in-the-vml-object-model). Coordinata più a sinistra del rettangolo.   |
| Inizio        | [Valore Double](#data-types-used-in-the-vml-object-model). Coordinata superiore del rettangolo.    |
| Destra      | [Valore Double](#data-types-used-in-the-vml-object-model). Coordinata più a destra del rettangolo.  |
| Ultimo     | [Valore Double](#data-types-used-in-the-vml-object-model). Coordinata inferiori del rettangolo. |



 

**IVgFixedRectangleArray**

Matrice di rettangoli fissi.



| Attributi | Descrizione                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| Valore      | [Stringa](#data-types-used-in-the-vml-object-model). Rappresentazione testuale della matrice.                           |
| Length     | [Integer](#data-types-used-in-the-vml-object-model). Numero di rettangoli in questa matrice.                    |
| Elemento       | [IVgFixedRectangle](#data-types-used-in-the-vml-object-model). Oggetto rettangolo in corrispondenza dell'indice specificato. |



 

Tipo di dati **IVgFormula**

Definizioni per le formule che possono variare il percorso di una forma o essere utilizzate per altri scopi di calcolo. Le formule possono essere basate sull'attributo **ADJ** di una forma, che può cambiare. Le formule possono anche fare riferimento ad altre formule.



| Attributi | Descrizione                                                                                                                                                                                                                                                                                                                                                                                          |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| EQN        | [IVgEquation](#data-types-used-in-the-vml-object-model). Ogni formula definisce un singolo valore come risultato della valutazione dell'espressione. L'espressione è definita da questo attributo e ha il formato generale di un'operazione seguita da un massimo di tre argomenti, che possono essere valori di rettifica (ad esempio, \# 2), i risultati delle formule precedenti (ad esempio, @2 ), i numeri fissi o i valori predefiniti. |



 

**Tipo di dati IVgFormulas**

Raccolta di oggetti formula.



| Attributi | Descrizione                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Length     | [Integer](#data-types-used-in-the-vml-object-model). Numero di oggetti formula nella raccolta.                                                |
| Elemento       | [IVgFormula](#data-types-used-in-the-vml-object-model). Formula specifica. Si noti che la matrice di formule può essere ereditata dal tipo di forma. |



 

**IVgGradientColorArray**

Matrice di colori che definiscono una sfumatura (intervallo di colori misto).



| Attributi | Descrizione                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| Valore      | [Stringa](#data-types-used-in-the-vml-object-model). Specifica la matrice di colori; ad esempio, "rosso. 2; verde. 4; nero. 7 " |
| Length     | [Integer](#data-types-used-in-the-vml-object-model). Numero di colori nella matrice.                                          |



 



| Metodi     | Descrizione                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AddColor    | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Aggiunge nuovo colore all'endpoint specificato dalla frazione. Per impostazione predefinita, il nuovo colore è bianco e il valore restituito è. Il colore può quindi essere modificato per riferimento. |
| RemoveColor | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Rimuove un colore in corrispondenza dell'endpoint specificato dalla frazione. Nota: se 0,0 o 1,0 non esiste, è implicito e il colore bianco viene usato in quel punto.          |



 

**Tipo di dati IVgPoints**

Matrice di punti che definiscono una forma.



| Attributi | Descrizione                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Valore      | [Stringa](#data-types-used-in-the-vml-object-model). Rappresentazione testuale della matrice.           |
| Length     | [Integer](#data-types-used-in-the-vml-object-model). Numero di punti in questa matrice.        |
| Elemento       | [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto in corrispondenza dell'indice specificato. |



 

**Tipo di dati IVgSkewMatrix**

Matrice utilizzata per le forme inclinate, una matrice di trasformazione prospettica nel formato "*SXX, SXY, SYX, SYY, px, py* " \[ *s* = scale, *p* = Perspective \] . Se l'offset è espresso in unità assolute, *px, py* si trovano in unità Emu ^-1; in caso contrario, si tratta di una frazione inversa della dimensione della forma.



| Attributi   | Descrizione                                         |
|--------------|-----------------------------------------------------|
| XtoX         | [Valore Double](#data-types-used-in-the-vml-object-model). |
| YtoX         | [Valore Double](#data-types-used-in-the-vml-object-model). |
| XtoY         | [Valore Double](#data-types-used-in-the-vml-object-model). |
| YtoY         | [Valore Double](#data-types-used-in-the-vml-object-model). |
| PerspectiveX | [Valore Double](#data-types-used-in-the-vml-object-model). |
| Prospettiva | [Valore Double](#data-types-used-in-the-vml-object-model). |



 

**IVgSkewOffset**

Specifica l'offset dell'asimmetria.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributi</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valore</td>
<td><a href="#data-types-used-in-the-vml-object-model">Stringa</a>. Rappresentazione testuale dell'offset.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Valore Double</a>. Componente X. Percentuale o misura. Se non sono presenti unità, il tipo ShapeRelative è implicito; in caso contrario, il tipo assoluto è implicito.</td>
</tr>
<tr class="odd">
<td>S</td>
<td><a href="#data-types-used-in-the-vml-object-model">Valore Double</a>. Componente Y.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><strong>VgSkewTransformType</strong>. Specifica il tipo di trasformazione. I valori validi sono punti interi compresi tra-infinito e infinito. 
<table>
<thead>
<tr class="header">
<th>Tipo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ShapeRelative</td>
<td>I valori dell'offset sono percentuali (rapporti) delle dimensioni della forma originale; ad esempio, il valore 0,5 indica un offset metà della dimensione della forma.</td>
</tr>
<tr class="even">
<td>Assoluto</td>
<td>I valori sono unità assolute.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

**Tipo di dati IVgVector2D**

Specifica un vettore bidimensionale costituito da due numeri **doppi** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributi</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valore</td>
<td><strong>Stringa</strong>. Rappresentazione testuale di entrambi i numeri di vettore separati da uno spazio.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Valore Double</a>. Componente X di questo vettore.</td>
</tr>
<tr class="odd">
<td>S</td>
<td><a href="#data-types-used-in-the-vml-object-model">Valore Double</a>. Componente Y di questo vettore.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><strong>VgVectorType</strong>. Unità previste per questo vettore. I valori possibili sono:
<ul>
<li>Measure</li>
<li>Length</li>
<li>AngoloInGradi</li>
<li>Fraction</li>
<li>Numero intero percentuale</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Tipo di dati IVgVector3D**

Specifica un vettore tridimensionale costituito da tre numeri **doppi** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Valore</td>
<td><strong>Stringa</strong>. Rappresentazione testuale di tre numeri di vettore separati da uno spazio.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Valore Double</a>. Componente X di questo vettore.</td>
</tr>
<tr class="odd">
<td>S</td>
<td><a href="#data-types-used-in-the-vml-object-model">Valore Double</a>. Componente Y di questo vettore.</td>
</tr>
<tr class="even">
<td>Z</td>
<td><a href="#data-types-used-in-the-vml-object-model">Valore Double</a>. Componente Z di questo vettore.</td>
</tr>
<tr class="odd">
<td>Tipo</td>
<td><strong>VgVectorType</strong>. Unità previste per questo vettore. I valori possibili sono:
<ul>
<li>Measure</li>
<li>Length</li>
<li>AngoloInGradi</li>
<li>Fraction</li>
<li>Numero</li>
<li>Percentuale</li>
<li>Integer</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Tipo di dati length**

Numero a virgola mobile con un intervallo compreso tra 0 e infinito.

**Tipo di dati Measure**

Numero a virgola mobile da-infinito a infinito.

**Tipo di dati String**

Dati di tipo carattere di qualsiasi lunghezza.

**VgBlackWhiteMode**

Modalità di rendering per il bianco e il nero. I valori possibili sono:

-   **Colore**
-   **Auto**
-   **Grigi**
-   **LightGrayScale**
-   **InverseGray**
-   **GrayOutline**
-   **BlackTextAndLines**
-   **HighContrast**
-   **Nero**
-   **White**
-   **Non disegnato**

**Tipo di dati VgFraction**

Numero a virgola mobile con intervallo compreso tra 0,0 e 1,0. È inoltre possibile specificare frazioni come percentuale; ad esempio, "50%".

**Tipo di dati VgTriState**

Enumerazione utilizzata per i valori che possono essere uno dei tre stati seguenti:

-   **TRUE**
-   **FALSE**
-   **MIXED**