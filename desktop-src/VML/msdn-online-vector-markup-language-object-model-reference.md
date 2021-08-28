---
title: Informazioni di riferimento sul modello a oggetti VML
description: Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.
ms.assetid: 68a84c68-3aac-4971-9611-45f52e057708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa8c608a60cbdb5af0fa5699fb1d458a5f18552
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884170"
---
# <a name="vml-object-model-reference"></a>Informazioni di riferimento sul modello a oggetti VML

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

In questo argomento

-   [Introduzione](#introduction)
-   [Esempio](#example)
-   [Configurazione di VML](#setting-up-vml)
-   [Informazioni di riferimento su VML OM](#vml-om-reference)
    -   [Elemento Shape](#shape-element)
-   [Sottoelementi dell'elemento Shape](#subelements-of-the-shape-element)
    -   [Elemento Background](#background-element)
    -   [Elemento Extrusion](#extrusion-element)
    -   [Fill - elemento](#fill-element)
    -   [Group - elemento](#group-element)
    -   [Elemento Imagedata](#imagedata-element)
    -   [Elemento Path](#path-element)
    -   [Elemento Shadow](#shadow-element)
    -   [Elemento Skew](#skew-element)
    -   [Elemento Stroke](#stroke-element)
    -   [Elemento TextPath](#textpath-element)
-   [Tipi di dati usati nel modello a oggetti VML](#data-types-used-in-the-vml-object-model)

## <a name="introduction"></a>Introduzione

[Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-datetime.html) è un linguaggio basato su testo che usa [XML](https://www.w3.org/TR/REC-xml.mdl) per estendere il codice HTML allo scopo di visualizzare informazioni grafiche vettoriali. Il modello DOCUMENT OBJECT MODEL (DOM) definisce un'interfaccia a livello di codice per la manipolazione degli elementi del documento. In questo modo l'utente può creare e modificare dinamicamente la grafica vettoriale tramite un'interfaccia indipendente dalla piattaforma e dalla lingua. Il DOM VML è conforme alla [Document Object Model](https://www.w3.org/TR/REC-DOM-Level-1/) specifica.

VML usa [l'elemento Shape](#shape-element) come blocco predefinito di base per le immagini grafiche vettoriali. Dopo aver creato una forma, è possibile modificarla tramite attributi o sottoelementi collegati. Ad esempio, per modificare il colore di una forma, assegnare un valore di colore **all'attributo FillColor.**


```HTML
myshape.fillcolor = "red"
```



Molti attributi di una forma sono anche [sottoelementi](/windows) e hanno i propri attributi, tra cui:

-   [Background](#background-element)
-   [Estrusione](#extrusion-element)
-   [Fill](#fill-element)
-   [Gruppo](#group-element)
-   [Imagedata](#imagedata-element)
-   [Percorso](#path-element)
-   [Shadow](#shadow-element)
-   [Inclinazione](#skew-element)
-   [Infarto](#stroke-element)
-   [Percorso di testo](#textpath-element)

VmL OM usa diversi tipi [di dati](/windows) per definire i parametri. I tipi di dati preceduti da "Vg" sono enumerazioni e quelli preceduti da "IVg" sono oggetti . Fare clic qui per un elenco. I tipi di dati secondari sono elencati con parametri specifici.

## <a name="example"></a>Esempio

Il codice VBScript seguente illustra come creare una forma semplice:


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



Nell'esempio precedente viene creata una forma usando il Document Object Model **createElement**. La forma è una forma Rect predefinita VML. Anche se l'oggetto esiste, non può far parte del documento fino a quando non viene allegato al documento. Usando il **metodo AppendChild,** Rect viene reso figlio di un **elemento DIV** denominato MyDiv. Alcuni attributi di stile minimi (**Position**, **Width**, **Height**, **Top**, **Left**) sono impostati per assegnare alla forma una dimensione specifica. Infine, un colore viene assegnato con **l'attributo FillColor.** Si noti che è possibile usare qualsiasi linguaggio di scripting o qualsiasi linguaggio che Document Object Model interfacce.

## <a name="setting-up-vml"></a>Configurazione di VML

Un'implementazione di VML è tramite Microsoft Internet Explorer 5.0 o versione successiva. Per configurare correttamente l'oggetto di rendering in una pagina Web, è necessario eseguire le aggiunte seguenti:

1.  Lo schema deve essere configurato nel &lt; tag HTML iniziale nel modo &gt; seguente:
    ```HTML
    <HTML xmlns:v="urn:schemas-microsoft-com:vml">
    ```

    

2.  Il comportamento di rendering deve far parte dello stile del documento:
    ```HTML
    <STYLE>
    v\:* { behavior: url(#default#VML); display:inline-block}
    </STYLE>
    ```

    

Di seguito viene illustrata una pagina Web HTML di esempio configurata correttamente per VML che mostra la creazione dinamica di una forma.


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



Si noti che nelle versioni beta sono necessari ActiveX tag dell'oggetto e uno stile di comportamento diverso.

## <a name="vml-om-reference"></a>Informazioni di riferimento su VML OM

Questo riferimento definisce [l'elemento Shape,](#shape-element) [i sottoelementi](/windows) [e](/windows) i tipi di dati usati dal modello a oggetti di VML.

### <a name="shape-element"></a>Elemento Shape

Le forme sono i blocchi predefiniti delle immagini grafiche definite da Vector Markup Language (VML). La forma è l'elemento di primo livello e diversi sottoelementi consentono di definire la natura di ogni forma.

VML fornisce forme predefinite:

**Attributi di forma**

-   **Arc**
-   **Curva**
-   **Linea**
-   **Polilinea**
-   **Rect**
-   **RoundRect**



|   Sottoelemento           |    Descrizione                                                                                                                                                                                                                                                                                                                                                                              |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Adj          | [IVgAdjustments](msdn-online-vml-ivgadjustments-data-type.md). Elenco delimitato da virgole di numeri che sono i parametri per le formule guida che definiscono il percorso della forma. I valori possono essere omessi per consentire l'uso delle impostazioni predefinite. Possono essere presenti fino a 8 valori di regolazione.                                                                                                   |
| ALT          | Stringa. Testo alternativo associato alla forma. Usato per l'esplorazione non grafica.                                                                                                                                                                                                                                                                                                 |
| Button       | [VgTriState](msdn-online-vml-vgtristate.md). Visualizza il comportamento del pulsante al clic del mouse.                                                                                                                                                                                                                                                                                                 |
| BWMode       | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Determina la modalità di rendering della forma nella visualizzazione in bianco e nero nelle app o quando viene stampata su stampanti in bianco e nero. I valori includono: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**. Impostazione predefinita: **Auto.** |
| BWNormal     | VgBlackWhiteMode. Quando BWMode è Auto, questa proprietà viene consultata per informazioni su come eseguire il rendering della forma in bianco e nero normali. I valori includono: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**. Impostazione predefinita: **Auto.**                                                |
| BWPure       | VgBlackWhiteMode. Quando BWMode è Auto, questa proprietà viene consultata per informazioni su come eseguire il rendering della forma in B/W puro. I valori includono: **Color**, **Auto**, **GrayScale**, **LightGrayScale**, **InverseGray**, **GrayOutline**, **BlackTextAndLines**, **HighContrast**, **Black**, **White**, **Undrawn**. Impostazione predefinita: **Auto.**                                                              |
| Forme figlio  | IVgGroupShapes. Raccolta di altre forme in questo gruppo. Questa raccolta supporta i metodi standard Length e Item.                                                                                                                                                                                                                                                       |
| Chromakey    | [Oggetto IVgColor.](msdn-online-vml-ivgcolor.md) Valore del colore che sarà trasparente e mostrerà tutto ciò che si nasconde dietro la forma.                                                                                                                                                                                                                                                             |
| Control1     | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto di controllo per la curva.                                                                                                                                                                                                                                                                                                  |
| Controllo2     | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto di controllo per la curva.                                                                                                                                                                                                                                                                                                  |
| CoordOrigin  | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md) Coordinate nell'angolo superiore sinistro del rettangolo del contenitore. Intervallo compreso tra 0 e infinito.                                                                                                                                                                                                                               |
| CoordSize    | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Larghezza e altezza dello spazio delle coordinate all'interno del rettangolo di riferimento di questa forma. Se non viene specificato, corrisponde alla larghezza e all'altezza del rettangolo. Intervallo compreso tra 0 e infinito. Impostazione predefinita: "1000,1000".                                                                                               |
| EndAngle     | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Angolo finale della forma.                                                                                                                                                                                                                                                                                          |
| Estrusione    | IVgExtrusion. Specifica il valore dell'oggetto Extrusion per questa forma. Per informazioni dettagliate, vedere l'elemento [Extrusion.](msdn-online-vml-extrusion-element.md)                                                                                                                                                                                                                               |
| Fill         | VgFillFormat. Specifica il valore di riempimento per questa forma. Per altri dettagli, vedere l'elemento [Fill.](msdn-online-vml-fill-element.md)                                                                                                                                                                                                                                                |
| Fillcolor    | [Oggetto IVgColor.](msdn-online-vml-ivgcolor.md) Colore principale del pennello da usare per riempire il tracciato di questa forma.                                                                                                                                                                                                                                                                  |
| Riempito       | [VgTriState](msdn-online-vml-vgtristate.md). Se True, il percorso che definisce la forma verrà riempito. Per impostazione predefinita, verrà riempito con un colore a tinta unita, a meno che non sia presente un sottoelemento Fill che specifica proprietà di riempimento più complesse. Se False, il riempimento è trasparente.                                                                                                           |
| Flip         | VgFlipOrientation. I valori sono: X Y XY YX                                                                                                                                                                                                                                                                                                                                         |
| ForceDash    | [VgTriState](msdn-online-vml-vgtristate.md). Indica che deve essere eseguito il rendering di un contorno tratteggiato quando non è presente alcuna linea e nessun riempimento per una forma. Questo comportamento è in genere utile per rendere visibili le forme invisibili nelle applicazioni di modifica in modo che possano essere selezionate e gestite, ad esempio in una mappa immagine.                                                                 |
| Formule     | IVgFormulas. Matrice di formule che definisce una forma.                                                                                                                                                                                                                                                                                                                          |
| Da         | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto iniziale della linea.                                                                                                                                                                                                                                                                                                   |
| Href         | [Stringa](#data-types-used-in-the-vml-object-model). URL a cui passare se si fa clic su questa forma.                                                                                                                                                                                                                                                                                 |
| ImageData    | IVgImageData. Informazioni sull'immagine se la forma è un'immagine. Per altre informazioni, vedere l'elemento ImageData.                                                                                                                                                                                                                                                                       |
| OnEd         | [VgTriState](msdn-online-vml-vgtristate.md). Nasconde tutti gli handle tranne quelli in alto a sinistra e in basso a destra, come negli handle per un segmento di linea retta.                                                                                                                                                                                                                             |
| Opacità      | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Opacità dell'intera forma. Numero compreso tra 0,0 e 1,0.                                                                                                                                                                                                                                                           |
| Percorso         | IVgPath. Stringa contenente i comandi che definiscono il percorso.                                                                                                                                                                                                                                                                                                                  |
| Punti       | [IVgPoints](msdn-online-vml-ivgpoints-data-type.md). Raccolta di punti che definiscono una forma.                                                                                                                                                                                                                                                                                   |
| Stampa        | [VgTriState](msdn-online-vml-vgtristate.md). Se True, questa forma deve essere stampata.                                                                                                                                                                                                                                                                                        |
| Rotazione     | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Imposta la rotazione della forma. Il valore viene propagato allo stile della forma.                                                                                                                                                                                                                                              |
| Scalabilità        | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Scala della forma.                                                                                                                                                                                                                                                                                                           |
| Ombreggiatura       | IVgShadow. Specifica l'ombreggiatura per questa forma. Per informazioni [dettagliate,](msdn-online-vml-shadow-element.md) vedere l'elemento Shadow.                                                                                                                                                                                                                                                        |
| Spt          | Riservato.                                                                                                                                                                                                                                                                                                                                                                        |
| StartAngle   | [VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md). Angolo iniziale della forma.                                                                                                                                                                                                                                                                                        |
| Stroke       | VgStrokeFormat. Per informazioni dettagliate, vedere Elemento Stroke.                                                                                                                                                                                                                                                                                                                                  |
| StrokeColor  | [IVgColor](msdn-online-vml-ivgcolor.md). Colore principale del pennello da usare per tracciare il percorso di questa forma.                                                                                                                                                                                                                                                                |
| Accarezzò      | [VgTriState](msdn-online-vml-vgtristate.md). Se True, il tracciato che definisce la forma verrà tracciato.                                                                                                                                                                                                                                                                              |
| StrokeWeight | [VGLength](msdn-online-vml-vglength.md). Larghezza del pennello da usare per tracciare il tracciato. Intervalli compresi tra 0 e 1584.                                                                                                                                                                                                                                                           |
| TextPath     | IVgTextPath. Specifica l'oggetto TextPath della forma. Per altre [informazioni, vedere l'elemento TextPath.](msdn-online-vml-textpath-element.md)                                                                                                                                                                                                                                  |
| Per           | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto finale della linea.                                                                                                                                                                                                                                                                                                        |
| Tipo         | Stringa. Tipo di forma.                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="subelements-of-the-shape-element"></a>Sottoelementi dell'elemento Shape

I sottoelementi seguenti fanno parte del modello a oggetti VML.

-   [Background](#background-element)
-   [Estrusione](#extrusion-element)
-   [Fill](#fill-element)
-   [Gruppo](#group-element)
-   [Imagedata](#imagedata-element)
-   [Percorso](#path-element)
-   [Shadow](#shadow-element)
-   [Inclinazione](#skew-element)
-   [Infarto](#stroke-element)
-   [TextPath](#textpath-element)

### <a name="background-element"></a>Elemento Background

Descrive il riempimento dello sfondo di una pagina usando riempimenti VML.


|   Attributo        |   Descrizione                                                                                                                                                                                      |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BWMode    | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Determina la modalità di rendering della forma nella visualizzazione in bianco e nero nelle applicazioni o quando viene stampata.                                     |
| BWNormal  | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Quando BWMode è Auto, questa proprietà viene consultata per informazioni su come eseguire il rendering della forma in bianco e nero normale.                        |
| BWPure    | [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md). Quando BWMode è Auto, questa proprietà viene consultata per informazioni su come eseguire il rendering della forma in bianco e nero puro.                          |
| Fill      | VgFillFormat. Specifica il riempimento per questa forma. Per [altre informazioni,](msdn-online-vml-fill-element.md) vedere Elemento Fill.                                                             |
| Fillcolor | [IVgColor](msdn-online-vml-ivgcolor.md). Colore principale del pennello da usare per riempire il percorso di questa forma. Duplicato del valore Color nell'elemento Fill. Il valore predefinito è bianco. |



 

### <a name="extrusion-element"></a>Elemento Extrusion

Descrive un'estrusione 3D della forma.

**Attributes (Attributi)**



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>AutoRotationCenter</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Se True, il centro di rotazione del gruppo di oggetti 3D (in realtà è presente un solo oggetto nel gruppo) viene determinato automaticamente come il centro del gruppo; in caso contrario, è determinato dai parametri RotationCenter, che sono una frazione della forma con 0,0,0 come centro.</td>
</tr>
<tr class="even">
<td>BackDepth</td>
<td><a href="msdn-online-vml-vglength.md"><strong>VgLength</strong></a>. Quantità di estrusione all'indietro. È compreso tra 0 e 32767.</td>
</tr>
<tr class="odd">
<td>Luminosità</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Luminosità complessiva della scena. Il valore &quot; predefinito è 20.000 &quot; .</td>
</tr>
<tr class="even">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Colore dell'estrusione. Usato solo se ColorMode è Custom. In caso contrario, Auto imposta il colore dell'effetto di estrusione sullo stesso colore di FillColor.</td>
</tr>
<tr class="odd">
<td>ColorMode</td>
<td>Vg3DColorMode. I valori possibili sono:
<ul>
<li>Auto (impostazione predefinita)</li>
<li>Personalizzato</li>
</ul></td>
</tr>
<tr class="even">
<td>Diffusione</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Rapporto tra evento imprevisto e luce riflessa diffusamente. I valori minori di 1,0 sono normali, ma i valori superiori a uno possono generare effetti interessanti.</td>
</tr>
<tr class="odd">
<td>Microsoft Edge</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Imposta le dimensioni di un bordo smussato arrotondato simulato. È compreso tra 0 e 32767 in pts a virgola mobile. Il valore predefinito &quot; è 1pt. &quot;</td>
</tr>
<tr class="even">
<td>Facet</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Imposta il facet della scena. Il valore &quot; predefinito è 30.000 &quot; .</td>
</tr>
<tr class="odd">
<td>ForeDepth</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Quantità di estrusione in avanti. È compreso tra 0 e 32767.</td>
</tr>
<tr class="even">
<td>LightFace</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Determina se la parte anteriore dell'oggetto risponderà alle modifiche dell'illuminazione 3D, ad esempio quando un oggetto ruota.</td>
</tr>
<tr class="odd">
<td>LightHarsh</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Illuminazione dura per la sorgente di luce primaria. Il valore predefinito è False.</td>
</tr>
<tr class="even">
<td>LightHarsh2</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Illuminazione dura per la sorgente di luce secondaria. Il valore predefinito è False.</td>
</tr>
<tr class="odd">
<td>LightLevel</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>. Intensità della sorgente di luce primaria. Il valore predefinito &quot; è 38000 &quot; .</td>
</tr>
<tr class="even">
<td>LightLevel2</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgNumber</a>. Intensità della sorgente di luce secondaria. Il valore predefinito &quot; è 38000 &quot; .</td>
</tr>
<tr class="odd">
<td>LightPosition</td>
<td>Vector3d. Posizione della sorgente di luce primaria. Il valore &quot; predefinito è 50000,0,10000 &quot; .</td>
</tr>
<tr class="even">
<td>LightPosition2</td>
<td>Vector3d. Posizione della sorgente di luce secondaria. Il valore &quot; predefinito è -50000,0,10000 &quot; .</td>
</tr>
<tr class="odd">
<td>LockRotationCenter</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. &quot;Lockrotationcenter indica che la rotazione del gruppo è definita in base ai gradi rotation-angle[1] circa l'asse y nella pagina seguita da &quot; rotation-angle[0] gradi circa l'asse x. Quando LockRotationCenter è False, la rotazione viene definita in base ai gradi dell'angolo di orientamento rispetto al vettore definito dall'orientamento. Ad esempio, lockrotationcenter=false orientationangle=45 orientation=(0,1,0) equivale a lockrotationcenter=true rotationangle=(0,45).</td>
</tr>
<tr class="even">
<td>Metallico</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Fa sì che la luce riflessa specularmente sia il colore del materiale anziché il colore della sorgente di luce, rendendo l'oggetto più metallico.</td>
</tr>
<tr class="odd">
<td>On</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Attiva e disattiva la visualizzazione dell'effetto di estrusione.</td>
</tr>
<tr class="even">
<td>Orientamento</td>
<td>Vector3d. Orientamento della fotocamera.</td>
</tr>
<tr class="odd">
<td>OrientationAngle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. Angolo tra l'orientamento della fotocamera e il piano xy.</td>
</tr>
<tr class="even">
<td>Aereo</td>
<td>Vg3DExtrudePlane. Consente l'estrusione da piani ortogonali al piano dello schermo. Richiede che ForeDepth e BackDepth siano specificati in unità di disegno anziché in emus. I valori possibili sono:
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
<li>Wireframe</li>
<li>BoundingCube</li>
</ul></td>
</tr>
<tr class="even">
<td>RotationAngle</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. AngleX, AngleY o AngleZ è controllato dall'attributo ShapeRotation.</td>
</tr>
<tr class="odd">
<td>RotationCenter</td>
<td>Vector3d. Centro di rotazione.</td>
</tr>
<tr class="even">
<td>Luminosità</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Determina la concentrazione o la diffusione della reflection speculare. Un valore alto è compreso tra 8 e 10 e si avvicina a uno mirror e un valore basso è compreso tra 2 e 3 e indica un abbigliamento con paillettes approssimativo. Sono consigliati valori da 3 a 7. I valori alti rifletteranno le sorgenti di luce di puntina.</td>
</tr>
<tr class="odd">
<td>SkewAmt</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPercentage</a>. Se Type è Parallel, l'attributo determina la quantità di agitazione. È compreso tra 0 e 100.</td>
</tr>
<tr class="even">
<td>SkewAngle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. Se Type è Parallel, l'attributo determina il grado di agitazione. Il valore predefinito &quot; è -45. &quot;</td>
</tr>
<tr class="odd">
<td>Specularità</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgPositiveNumber</a>. Rapporto tra evento imprevisto e luce riflessa in modo speculare. I valori minori di 1,0 sono normali, ma i valori superiori a uno possono generare effetti interessanti.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td>VgExtrusionType. I valori possibili sono:
<ul>
<li>Parallelo (impostazione predefinita)</li>
<li>Prospettiva</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vista</td>
<td>Vector3d. Punto da cui viene visualizzata la scena.</td>
</tr>
<tr class="even">
<td>ViewpointOrigin</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Può avere valori da 0,5 a -0,5 per posizionare l'origine del punto di vista all'interno del rettangolo di selezione della forma.</td>
</tr>
</tbody>
</table>



 

### <a name="fill-element"></a>Elemento Fill

Descrive come riempire un percorso per i riempimenti più complessi rispetto a un colore a tinta unita.

**Attributes (Attributi)**



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>AlignShape</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Allineare l'immagine alla forma. Se False, allineare l'immagine alla finestra.</td>
</tr>
<tr class="even">
<td>Angle</td>
<td><a href="msdn-online-vml-vgangleindegrees-data-type.md">VgAngleInDegrees</a>. Angolo lungo il quale va la sfumatura. 0 gradi è lungo l'asse orizzontale da sinistra a destra.</td>
</tr>
<tr class="odd">
<td>Aspetto</td>
<td><strong>VgAspectType</strong>. L'attributo ImageSize verrà regolato per mantenere l'aspetto dell'immagine. I possibili valori sono:
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
<td>Ignorare i problemi relativi all'aspetto.</td>
</tr>
<tr class="even">
<td>Atleast</td>
<td>L'immagine è grande almeno quanto le dimensioni dell'immagine.</td>
</tr>
<tr class="odd">
<td>AtMost</td>
<td>Le dimensioni dell'immagine non sono maggiori delle dimensioni dell'immagine.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a> Colore di riempimento principale. Uguale all'attributo FillColor nella forma.</td>
</tr>
<tr class="odd">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Colore secondario per un riempimento quando il tipo di immagine è Pattern o un riempimento sfumato.</td>
</tr>
<tr class="even">
<td>Colori</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgGradientColorArray</a>. Colori intermedi nella sfumatura e le relative posizioni lungo la sfumatura, ad esempio, &quot; 30% rosso, 70% blu, 90% &quot; verde. Il colore primario (attributo Color nella forma) è 0% e il colore secondario (attributo Color2) è 100%.</td>
</tr>
<tr class="odd">
<td>Focus</td>
<td><a href="#data-types-used-in-the-vml-object-model">VgSignedPercentage</a>. Punto focale per il riempimento sfumato lineare. I valori vanno da -100 a +100.</td>
</tr>
<tr class="even">
<td>FocusPosition</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Posizione del rettangolo più interno per le sfumature radiali. Il vettore è una frazione (0,0 - 1,0) della larghezza e dell'altezza della forma.</td>
</tr>
<tr class="odd">
<td>FocusSize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Dimensione del rettangolo più interno per le sfumature radiali. Il vettore è una frazione (da 0,0 a 1,0) della larghezza e dell'altezza della forma.</td>
</tr>
<tr class="even">
<td>Metodo</td>
<td>VgSigmaType. I possibili valori sono:
<ul>
<li>Nessuno</li>
<li>Lineari</li>
<li>Sigma</li>
<li>Qualsiasi</li>
</ul>
<p>Il valore predefinito è Sigma.</p></td>
</tr>
<tr class="odd">
<td>On</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Attiva la visualizzazione del riempimento. Uguale all'attributo Fill nella forma.</td>
</tr>
<tr class="even">
<td>Opacità</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacità del riempimento.</td>
</tr>
<tr class="odd">
<td>Opacità2</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacità secondaria per le sfumature.</td>
</tr>
<tr class="even">
<td>Origine</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Punto relativo all'angolo superiore sinistro dell'immagine considerata come origine dell'immagine. Il valore predefinito è il centro dell'immagine. Il vettore è una frazione (da 0,0 a 1,0) della larghezza e dell'altezza dell'immagine.</td>
</tr>
<tr class="odd">
<td>Posizione</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Punto nel rettangolo di riferimento della forma per posizionare l'origine dell'immagine. Il valore predefinito è il centro del rettangolo del contenitore. Il vettore è una frazione (0,0 - 1,0) della larghezza e dell'altezza dell'immagine.</td>
</tr>
<tr class="even">
<td>Dimensione</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Dimensioni dell'immagine. Il valore predefinito è la dimensione in pixel dell'immagine. Può essere specificato in coordinate assolute o in percentuale.</td>
</tr>
<tr class="odd">
<td>Src</td>
<td><a href="#data-types-used-in-the-vml-object-model">Stringa</a>. URL di un'immagine da caricare per i riempimenti di immagine e motivo. Questo attributo deve essere sempre presente e puntare a dati immagine validi per visualizzare un'immagine.</td>
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
Tile, Pattern e Frame richiedono che siano specificati gli attributi dell'immagine. Gradient e GradientRadial richiedono che siano specificati gli attributi della sfumatura.</td>
</tr>
</tbody>
</table>



 

### <a name="group-element"></a>Group - elemento

Un gruppo è una raccolta di singole forme che possono essere posizionate e trasformate come unità.



|   Attributo        |   Descrizione                                                                                                                                                                                      |
|--------|----------------------------------------------------------------------------------------------|
| Elemento   | [IVgShape](#data-types-used-in-the-vml-object-model). Elemento specificato nella matrice di forme. |
| Length | [Integer](#data-types-used-in-the-vml-object-model). Numero di forme in questo gruppo.         |



 

### <a name="imagedata-element"></a>Elemento Imagedata

Descrive un'immagine di cui eseguire il rendering sopra una forma.



|   Attributo        |   Descrizione                                                                                                                                                                                      |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bilevel     | [VgTriState](msdn-online-vml-vgtristate.md). Visualizzare l'immagine solo in due colori (in genere bianco e nero).                                                                                                                                                                                                                                                     |
| BlackLevel  | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Consente di impostare il livello in modo che i nere vengano visualizzati come neri veri e che tutti gli altri colori siano visibili come sfumature sopra il nero.                                                                                                                                                                        |
| Chromakey   | [Oggetto IVgColor.](msdn-online-vml-ivgcolor.md) Colore trasparente dell'immagine.                                                                                                                                                                                                                                                                                         |
| CropBottom  | [VgNumber](#data-types-used-in-the-vml-object-model). Distanza di ritaglio dalla parte inferiore dell'immagine espressa come percentuale delle dimensioni dell'immagine.                                                                                                                                                                                                                           |
| CropLeft    | [VgNumber](#data-types-used-in-the-vml-object-model). Distanza di ritaglio dal bordo sinistro dell'immagine espressa come frazione delle dimensioni dell'immagine (da 0,0 a 1,0). Tuttavia, il "ritaglio in uscita" è supportato e pertanto sono supportati valori minori di 0 e maggiori di 1. Ad esempio, -5, 20 ritagliano i limiti 25X delle dimensioni dell'immagine con 4/5 su un lato dell'immagine. |
| CropRight   | [VgNumber](#data-types-used-in-the-vml-object-model). Distanza di ritaglio da destra dell'immagine espressa come percentuale delle dimensioni dell'immagine.                                                                                                                                                                                                                            |
| CropTop     | [VgNumber](#data-types-used-in-the-vml-object-model). Distanza di ritaglio dalla parte superiore dell'immagine espressa come percentuale delle dimensioni dell'immagine.                                                                                                                                                                                                                              |
| EmbossColor | [Oggetto IVgColor.](msdn-online-vml-ivgcolor.md) Questa proprietà è impostata su una percentuale del colore dell'ombreggiatura per creare un effetto immagine in rilievo.                                                                                                                                                                                                                                 |
| Guadagno        | [VgPositiveNumber](#data-types-used-in-the-vml-object-model). Regola l'intensità di tutti i colori. Imposta essenzialmente il livello di luminosità del bianco. È compreso tra 0 e 32767.                                                                                                                                                                                           |
| Gamma       | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Correzione gamma. Aumentandola si aumenta il contrasto di un'immagine.                                                                                                                                                                                                                                           |
| GrayScale   | [VgTriState](msdn-online-vml-vgtristate.md). Visualizzare l'immagine in gradazioni di grigio.                                                                                                                                                                                                                                                                              |
| Src         | [Stringa](#data-types-used-in-the-vml-object-model). URL di un'immagine da caricare per i riempimenti immagine e motivo. Questo attributo deve essere sempre presente e puntare a dati immagine validi per visualizzare un'immagine.                                                                                                                                                           |



 

### <a name="path-element"></a>Path - elemento

Definisce il tracciato che costituisce la forma, usando una stringa che contiene un set completo di comandi di "movimento della penna".



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Limousine</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">IVgVector2D</a>. Definisce il punto in cui viene estesa la forma. Ad esempio, per una forma di giraffa, il punto di limousine si trova in un punto di ridimensionamento in modo che, quando la forma viene ridimensionata, il collo si allunga e il resto della forma manterrà le dimensioni.</td>
</tr>
<tr class="even">
<td>TextBoxRect</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgFixedRectangleArray</a>. Matrice contenente i rettangoli che definiscono dove deve andare il testo.</td>
</tr>
<tr class="odd">
<td>V</td>
<td><a href="#data-types-used-in-the-vml-object-model">Stringa</a>. Corrisponde all'attributo v nel tag Path. Si noti che path può corrispondere all'attributo o all'elemento Path.</td>
</tr>
<tr class="even">
<td>Valore</td>
<td><a href="#data-types-used-in-the-vml-object-model">Stringa</a>. Rappresentazione testuale dei comandi che definiscono il percorso. I valori delle coordinate X o y possono essere un riferimento a una formula nel formato dove # è il numero ordinale della &quot; @# &quot; formula, ad esempio &quot; @2 &quot; . Questa stringa di attributo è costituito da un set di comandi ricco, inclusi i seguenti: <br/> 
<table>
<thead>
<tr class="header">
<th>Comando</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ae (angleellipseto)</td>
<td><strong>center</strong>(x,y) <strong>size</strong>(w,h) <strong>start-angle</strong>, <strong>end-angle</strong><br/> Disegnare un segmento di un'ellisse. Viene disegnata una linea retta dal punto corrente al punto iniziale del segmento.<br/></td>
</tr>
<tr class="even">
<td>al (angleelipse)</td>
<td>Uguale a ae, ad eccezione del fatto che è presente un m implicito al punto iniziale del segmento.</td>
</tr>
<tr class="odd">
<td>ar (arc)</td>
<td>Uguale a at. Tuttavia, un nuovo sottopercorso viene avviato da un m implicito al punto iniziale dell'arco.</td>
</tr>
<tr class="even">
<td>at (arcto)</td>
<td><strong>left</strong>, <strong>top</strong>, <strong>right</strong>, <strong>bottom</strong>, <strong>start</strong>(x,y) <strong>end</strong>(x,y) <br/> I primi quattro valori definiscono il rettangolo di selezione di un'ellisse. Gli ultimi quattro definiscono due vettori radiali. Viene disegnato un segmento dell'ellisse che inizia in corrispondenza dell'angolo definito dal vettore del raggio iniziale e termina in corrispondenza dell'angolo definito dal vettore finale. Viene disegnata una linea retta dal punto corrente all'inizio dell'arco. L'arco viene sempre disegnato in senso antiorario. <br/></td>
</tr>
<tr class="odd">
<td>c (curveto)</td>
<td><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>to</strong>(x,y) <br/> Disegnare una curva di Bézier cubica dal punto corrente alla coordinata specificata dai due parametri finali, i punti di controllo specificati dai primi quattro parametri. Il punto corrente diventa l'endpoint della Bézier.<br/></td>
</tr>
<tr class="even">
<td>e (end)</td>
<td>Termina il set corrente di sottopercorso. Un set specificato di sottopercorso (come delimitato dalla fine) viene riempito usando il riempimento. I set successivi di sottopercorsi vengono riempiti in modo indipendente e sovrapposti a quelli esistenti.</td>
</tr>
<tr class="odd">
<td>l (lineto)</td>
<td>x,y<br/> Disegna una linea dal punto corrente alla coordinata x,y specificata, che diventa il nuovo punto corrente. È possibile impostare coppie di coordinate aggiuntive per formare una polilinea, ad esempio &quot; l 10,13,45,27,89,-12 &quot; .<br/></td>
</tr>
<tr class="even">
<td>m (moveto)</td>
<td>x,y<br/> Avvia un nuovo sottopercorso in corrispondenza della coordinata x,y specificata.<br/></td>
</tr>
<tr class="odd">
<td>nf (nofill)</td>
<td>Il set corrente di sottopercorso (delimitato dalla fine) non verrà riempito.</td>
</tr>
<tr class="even">
<td>ns (nostroke)</td>
<td>Il set corrente di sottopercorso (delimitato dalla fine) non verrà tratto.</td>
</tr>
<tr class="odd">
<td>qb (quadraticbezier)</td>
<td>(<strong>controlpoint</strong>(x, y))*,<strong>end</strong>(x,y) <br/> Definisce una o più curve di Bézier quadratica tramite punti di controllo e un endpoint. I punti intermedi (su curva) vengono ottenuti tramite interpolazione tra punti di controllo successivi simili ai tipi di carattere TrueType. Il sottopercorso non deve essere un inizio, nel qual caso il sottopercorso è chiuso e l'ultimo punto definisce il punto iniziale.<br/></td>
</tr>
<tr class="even">
<td>qx (ellipticalquadrantx)</td>
<td><strong>end</strong>(x,y) <br/> Un quarto di ellisse viene disegnato dal punto corrente al punto finale specificato. Il segmento ellittico è inizialmente tangente a una linea parallela all'asse x; Ad esempio, il segmento inizia orizzontalmente.<br/></td>
</tr>
<tr class="odd">
<td>qy (ellipticalquadranty)</td>
<td><strong>end</strong>(x,y) <br/> Uguale a qx ad eccezione del fatto che il segmento ellittico è inizialmente tangente a una linea parallela all'asse y; Ad esempio, il segmento inizia in verticale.<br/></td>
</tr>
<tr class="even">
<td>r (rlineto)</td>
<td>x,y <br/> Disegnare una linea dal punto corrente alla coordinata relativa (cpx + x, cpy + y). Se vengono specificate altre coppie di coordinate, ogni nuovo punto viene calcolato rispetto all'ultimo.<br/></td>
</tr>
<tr class="odd">
<td>t (rmoveto)</td>
<td>x,y<br/> Avviare un nuovo sottopercorso in corrispondenza delle coordinate relative ( cpx + x, cpy + y) dove cpx, cpy è la posizione corrente. <br/></td>
</tr>
<tr class="even">
<td>v (curveto)</td>
<td><strong>control1</strong>(x,y) <strong>control2</strong>(x,y) <strong>a</strong> (x,y) <br/> Curva di Bézier cubica usando le coordinate specificate relative al punto corrente. Tutti i punti vengono calcolati rispetto allo stesso punto iniziale.<br/></td>
</tr>
<tr class="odd">
<td>wa (clockwisearcto)</td>
<td>Uguale a , ma l'arco viene disegnato in senso orario.</td>
</tr>
<tr class="even">
<td>wr (clockwisearc)</td>
<td>Uguale a ar, ma viene disegnato in senso orario.</td>
</tr>
<tr class="odd">
<td>x (chiudi)</td>
<td>Chiudere il sottopercorso corrente tracciando una linea retta dal punto corrente al punto di spostamento originale.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="shadow-element"></a>Elemento shadow

Descrive un effetto ombreggiatura su una forma.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Color</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Colore dell'ombreggiatura primaria. Il valore predefinito è RGB(128,128,128)</td>
</tr>
<tr class="even">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Colore della seconda ombreggiatura o evidenziazione in un'ombreggiatura in rilievo o incisa. Il valore predefinito è RGB(203,203,203).</td>
</tr>
<tr class="odd">
<td>Matrice</td>
<td><a href="#data-types-used-in-the-vml-object-model">IvgSkewMatrix</a>. Matrice di trasformazione prospettica nel formato &quot; sxx,sxy,syx,syy,px,py &quot; [s=scale, p=perspective]. Gli elementi s specificano come ridimensionare l'ombreggiatura rispetto alla forma e gli elementi p specificano come l'ombreggiatura deve essere a inclinazione rispetto alla forma. Ad esempio, la matrice seguente ridimensiona la forma di un fattore 2 e la inclina di un fattore 4 in tutte le direzioni: <br/> &quot;2,2,2,2,4,4&quot;<br/> Questa matrice viene usata solo se il tipo di ombreggiatura è impostato su perspective.<br/></td>
</tr>
<tr class="even">
<td>Oscurato</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. L'ombreggiatura può essere vista attraverso se non è presente alcun riempimento sulla forma. Il valore predefinito è False.</td>
</tr>
<tr class="odd">
<td>Offset</td>
<td><a href="#data-types-used-in-the-vml-object-model">IVgSkewOffset</a>. Quantità di offset x,y dalla posizione della forma. Il valore predefinito &quot; è 2pt,2pt. &quot;</td>
</tr>
<tr class="even">
<td>Offset2</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Quantità di offset x,y secondo dalla posizione della forma. I valori sono una misura assoluta o un valore frazionario di forma (da -0,5 a +0,5).</td>
</tr>
<tr class="odd">
<td>On</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Attiva e disattiva la visualizzazione dell'ombreggiatura.</td>
</tr>
<tr class="even">
<td>Opacità</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacità dell'effetto ombreggiatura.</td>
</tr>
<tr class="odd">
<td>Origine</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a> Coppia di valori frazionari della forma da -0,5 a +0,5.</td>
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



 

### <a name="skew-element"></a>Elemento Skew

Descrive un effetto di a inclinazione prospettica su una forma. L'a inclinazione viene applicata ai dati grafici vettoriali, non ai dati immagine.



|   Attributo        |   Descrizione                                                                                                                                                                                      |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Matrice | [IVgSkewMatrix](#data-types-used-in-the-vml-object-model). Matrice di trasformazione prospettica nel formato "sxx,sxy,syx,syy,px,py" \[ s=scale, p=perspective \] . Se offset è in unità assolute, px,py è in emu ^ -1 unità; in caso contrario, sono una frazione inversa delle dimensioni della forma. |
| Offset | [IvgSkewOffset](#data-types-used-in-the-vml-object-model). Quantità di offset x,y dalla posizione della forma. Il valore predefinito è "2pt,2pt".                                                                                                                                                   |
| On     | [VgTriState](msdn-online-vml-vgtristate.md). Attiva o disattiva la visualizzazione dell'a inclinazione.                                                                                                                                                                                             |
| Origine | [Vector2D](msdn-online-vml-ivgvector2d-data-type.md). Coppia di valori frazionari della forma da -0,5 a +0,5.                                                                                                                                                                     |



 

### <a name="stroke-element"></a>Elemento Stroke

Descrive come disegnare il tracciato se si desidera un elemento oltre una linea continua con un colore a tinta unita.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Color</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Colore della linea. Uguale all'attributo StrokeColor in Shape, ma ne esegue l'override.</td>
</tr>
<tr class="even">
<td>Color2</td>
<td><a href="msdn-online-vml-ivgcolor.md">IVgColor</a>. Colore secondario. Usato quando FillType è Pattern.</td>
</tr>
<tr class="odd">
<td>Dashstyle</td>
<td><strong>VgLineDashStyle</strong>. Formato dello stile del trattino. Può essere un valore specifico o una sequenza di numeri con un motivo a trattino definito dall'utente. I valori possibili sono:
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
<td><strong>VgArrowheadStyle</strong>. Freccia per la fine della linea. I valori possibili sono:
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
<td><strong>VgArrowHeadLength</strong>. Lunghezza della freccia per la fine della linea. I valori possibili sono:
<ul>
<li>Short</li>
<li>Media (impostazione predefinita)</li>
<li>long</li>
</ul></td>
</tr>
<tr class="even">
<td>EndArrowWidth</td>
<td><strong>VgArrowheadWidth</strong>. Larghezza della freccia per la fine della linea. I valori possibili sono:
<ul>
<li>Stretta</li>
<li>Media (impostazione predefinita)</li>
<li>Largo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Endcap</td>
<td><strong>VgLineEndCapStyle</strong>. I valori possibili sono:
<ul>
<li>Semplice</li>
<li>Square</li>
<li>Round</li>
</ul></td>
</tr>
<tr class="even">
<td>FillType</td>
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
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Allineare l'immagine alla forma. Se False, allineare l'immagine alla finestra.</td>
</tr>
<tr class="even">
<td>Oggetto ImageAspect</td>
<td><strong>VgAspectType</strong>. L'attributo ImageSize verrà modificato per mantenere l'aspetto dell'immagine. I possibili valori sono:
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
<td>Ignorare i problemi relativi all'aspetto.</td>
</tr>
<tr class="even">
<td>Atleast</td>
<td>Le dimensioni dell'immagine sono almeno le dimensioni dell'immagine.</td>
</tr>
<tr class="odd">
<td>AtMost</td>
<td>Le dimensioni dell'immagine non sono superiori alle dimensioni dell'immagine.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>Imagesize</td>
<td><a href="msdn-online-vml-ivgvector2d-data-type.md">Vector2D</a>. Dimensioni dell'immagine con cui formare il pennello. Il valore predefinito è la dimensione dell'immagine.</td>
</tr>
<tr class="even">
<td>Stile join</td>
<td><strong>VgLineJoinStyle</strong>. I valori possibili sono:
<ul>
<li>Round (giunzione arrotondata)</li>
<li>Smussatura (giunzione smussata)</li>
<li>Miter (miter joint)</li>
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
<td><a href="msdn-online-vml-vglength.md">Lunghezza</a>. Distanza massima tra il punto interno e il punto esterno di un'giunzione. Questo numero è un multiplo dello spessore della linea. È compreso tra 0 e 32.767.</td>
</tr>
<tr class="odd">
<td>On</td>
<td><a href="msdn-online-vml-vgtristate.md">VgTriState</a>. Attiva e disattiva la visualizzazione della riga. Uguale all'attributo Stroke in Shape, ma ne esegue l'override.</td>
</tr>
<tr class="even">
<td>Opacità</td>
<td><a href="msdn-online-vml-vgfraction-data-type.md">VgFraction</a>. Opacità del tratto.</td>
</tr>
<tr class="odd">
<td>Src</td>
<td>Stringa. URL di un'immagine da caricare per i riempimenti di immagine e motivo. Questo attributo deve essere sempre presente e puntare a dati immagine validi per visualizzare un'immagine.</td>
</tr>
<tr class="even">
<td>StartArrow</td>
<td><strong>VgArrowheadStyle</strong>. Freccia per l'inizio della linea. I valori possibili sono:
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
<td>VgArrowHeadLength. Lunghezza della freccia per l'inizio della linea. I valori possibili sono:
<ul>
<li>Short</li>
<li>Media (impostazione predefinita)</li>
<li>long</li>
</ul></td>
</tr>
<tr class="even">
<td>StartArrowWidth</td>
<td>VgArrowheadWidth. Larghezza della freccia per l'inizio della linea. I valori possibili sono:
<ul>
<li>Narrow Medium (impostazione predefinita) Wide</li>
</ul></td>
</tr>
<tr class="odd">
<td>Peso</td>
<td><a href="msdn-online-vml-vglength.md">VgLength</a>. Larghezza della linea. È compreso tra 0 e 1584.
<div class="alert">
<blockquote>
[!Note]<br />
L'attributo DashStyle consente all'utente di specificare un modello di tratteggio personalizzato. Questa operazione viene eseguita usando una serie di numeri. Gli stili dei trattini sono definiti in termini di lunghezza del trattino (la parte disegnata del tratto) e lunghezza dello spazio tra i trattini. Le lunghezze sono relative alla larghezza della linea. una lunghezza &quot; pari a 1 è uguale alla larghezza &quot; della riga. Lo stile EndCap viene applicato a ogni trattino, gli stili freccia no. La stringa definisce prima la lunghezza del trattino e quindi la lunghezza dello spazio. Questa operazione può essere ripetuta per formare stili trattini complessi. La stringa deve contenere sempre una coppia di numeri. se contiene un numero dispari di numeri, l'ultimo può essere ignorato. Nella tabella seguente sono elencati alcuni valori tipici e una descrizione dell'effetto desiderato. &quot;0 implica un punto che deve essere simmetrico quattro volte (con estremità arrotondate &quot; deve essere un cerchio). Se l'estremità linea è Flat, un visualizzatore deve scegliere un trattino del sistema operativo predefinito, laddove possibile , ad esempio qualcosa che sia veloce da disegnare. Di seguito sono illustrati alcuni esempi.
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td>&quot;2 2&quot;</td>
<td>trattini brevi (ogni trattino e lo spazio tra è il doppio della larghezza della linea)</td>
</tr>
<tr class="even">
<td>&quot;1 2&quot;</td>
<td>punto (ogni trattino è la larghezza della linea mentre ogni spazio è il doppio della larghezza della linea)</td>
</tr>
<tr class="odd">
<td>&quot;4 2&quot;</td>
<td>trattino (ogni trattino è quattro volte la larghezza della linea mentre ogni spazio è il doppio della larghezza della linea)</td>
</tr>
<tr class="even">
<td>&quot;8 2&quot;</td>
<td>trattino lungo</td>
</tr>
<tr class="odd">
<td>&quot;4 2 1 2&quot;</td>
<td>punto trattino</td>
</tr>
<tr class="even">
<td>&quot;8 2 1 2&quot;</td>
<td>punto con trattino lungo</td>
</tr>
<tr class="odd">
<td>&quot;8 2 1 2 1 2&quot;</td>
<td>punto con trattino lungo</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="textpath-element"></a>Elemento TextPath

Descrive un percorso vettoriale in base ai dati di testo, al tipo di carattere e agli stili forniti. Il percorso di testo viene wared in modo che sia conforme a un **elemento Path,** se specificato.



|   Attributo        |   Descrizione                                                                                                                                                                                      |
|----------|-------------------------------------------------------------------------------------------------------------------------------|
| FitPath  | [VgTriState](msdn-online-vml-vgtristate.md). Ridimensiona il testo per riempire il percorso su cui si trova.                                 |
| FitShape | [VgTriState](msdn-online-vml-vgtristate.md). Estende il percorso del testo ai bordi della casella della forma.                      |
| On       | [VgTriState](msdn-online-vml-vgtristate.md). Determina se i percorsi dei caratteri vengono visualizzati o meno.                    |
| Stringa   | Stringa. Testo di cui eseguire il rendering come percorso di testo.                                                                                    |
| Taglio     | [VgTriState](msdn-online-vml-vgtristate.md). Rimuove qualsiasi spazio aggiuntivo riservato a ascendenti e discendenti se non viene usato. |
| Xscale   | [VgTriState](msdn-online-vml-vgtristate.md). Usare la misura straight x invece di misurare lungo il percorso.                 |



 

## <a name="data-types-used-in-the-vml-object-model"></a>Tipi di dati usati nel modello a oggetti VML

I tipi di dati seguenti vengono usati dal modello a oggetti VML.

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

Intero a precisione doppia con intervallo compreso tra -infinito e infinito.

**Tipo di dati fisso**

Numero a virgola mobile con intervallo compreso tra -32.766,0 e 32.766,0.

**Tipo di dati Integer**

Intero con un intervallo compreso tra -infinito e infinito.

**Tipo di dati IVgAdjustments**

Raccolta di modifiche a una forma che può essere utilizzata per modificare le dimensioni di una forma. Le rettifiche possono essere usate come segnaposto temporanei o per qualsiasi motivo si usino le variabili. La raccolta contiene solo 8 modifiche.



| Attributo | Descrizione                                                                                                                                                                                                                                                                                                                                                                    |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exists     | [IVgTriState](msdn-online-vml-vgtristate.md). Determina se esiste una regolazione specificata. Si noti che è necessario usare un indice. ovvero exists( item ) deve essere usato per recuperare l'esistenza di un elemento.                                                                                                                                                                   |
| Elemento       | [Long](#data-types-used-in-the-vml-object-model). Matrice di rettifiche indicizzate da 0 a 7. Si noti che le rettifiche possono essere specificate con parsimonio; ciò significa che i valori intermedi della matrice potrebbero non essere sempre riempiti. Ad esempio, gli elementi 1, 3 e 5 possono avere valori per una lunghezza pari a 3, con item(0), item(2) e item(4) specificati. Per verificare se esiste un elemento, usare l'attributo Exists. |
| Length     | [Integer](#data-types-used-in-the-vml-object-model). Numero di rettifiche. Non può essere maggiore di 8.                                                                                                                                                                                                                                                                          |
| Valore      | [Stringa](#data-types-used-in-the-vml-object-model). Rappresentazione testuale di valori numerici, con virgole tra ogni numero.                                                                                                                                                                                                                                                    |



 

**IVgColor**

Specifica un colore.



<table>
<colgroup>
<col  />
<col  />
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
<td><strong>VgRGBType</strong>. Valore RGB (Long) del colore. Valido solo se Type è RGB.</td>
</tr>
<tr class="even">
<td>R</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a>. Componente rosso del colore. Può essere compreso tra 0 e 255.</td>
</tr>
<tr class="odd">
<td>G</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a>. Componente verde del colore. Può essere compreso tra 0 e 255.</td>
</tr>
<tr class="even">
<td>B</td>
<td><a href="#data-types-used-in-the-vml-object-model">Integer</a>. Componente blu del colore. Può essere compreso tra 0 e 255.</td>
</tr>
<tr class="odd">
<td>Stringa</td>
<td><a href="#data-types-used-in-the-vml-object-model">Stringa</a>. Rappresentazione testuale del colore. Sono supportati i tipi di colore denominati seguenti:
<ul>
<li>Nero (#000000)</li>
<li>Silver (#C0C0C0)</li>
<li>Grigio (#808080)</li>
<li>Bianco (#FFFFFF)</li>
<li>Maroon (#800000)</li>
<li>Rosso (#FF0000)</li>
<li>Viola (#800080)</li>
<li>Fuchsia (#FF00FF)</li>
<li>Verde (#008000)</li>
<li>Bianco (#00FF00)</li>
<li>Olivo (#808000)</li>
<li>Giallo (#FFFF00)</li>
<li>Rieti (#000080)</li>
<li>Blu (#0000FF)</li>
<li>Teal (#008080)</li>
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

Equazioni usate per le formule.



<table>
<colgroup>
<col  />
<col  />
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
<td>Valore assoluto. <br/> <strong>abs</strong>(v) <br/></td>
</tr>
<tr class="even">
<td>Atan2</td>
<td>Aritmetica polare: i risultati sono unità fd (gradi moltiplicati per 65536).<br/> <strong>atan2</strong>(p1,v) <br/></td>
</tr>
<tr class="odd">
<td>Cos</td>
<td>Coseno, argomento in unità fd (gradi moltiplicati per 65536).<br/> v * <strong>cos</strong>(p1) <br/></td>
</tr>
<tr class="even">
<td>Cosatan2</td>
<td>Mantiene l'accuratezza completa nel calcolo intermedio.<br/> v * <strong>cos(atan2(</strong> p2,p1 <strong>))</strong><br/></td>
</tr>
<tr class="odd">
<td>Ellisse</td>
<td>Ellisse</td>
</tr>
<tr class="even">
<td>Se</td>
<td>Se il test della condizione. v > 0 <strong>?</strong> p1 : p2</td>
</tr>
<tr class="odd">
<td>Max</td>
<td>Maggiore di due valori. <br/> <strong>max</strong>(v,p1) <br/></td>
</tr>
<tr class="even">
<td>Mid</td>
<td>Media ( v + p1)/2</td>
</tr>
<tr class="odd">
<td>Min</td>
<td>Minore di due valori. <strong>min</strong>(v,p1)</td>
</tr>
<tr class="even">
<td>Mod</td>
<td>Modulo.</td>
</tr>
<tr class="odd">
<td>Prodotto</td>
<td>Usato per la moltiplicazione e la divisione. v * p1 /p2</td>
</tr>
<tr class="even">
<td>Sin</td>
<td>Seno, argomento in unità fd (gradi moltiplicati per 65536). <br/> v * <strong>sin</strong>(p1) <br/></td>
</tr>
<tr class="odd">
<td>Sinatan2</td>
<td>Mantiene l'accuratezza completa nel calcolo intermedio. v * <strong>sin</strong>(<strong>atan2</strong>(p2,p1))</td>
</tr>
<tr class="even">
<td>Sqrt</td>
<td>Il risultato è positivo e viene arrotondato per e per intero. <br/> <strong>sqrt</strong>(v) <br/></td>
</tr>
<tr class="odd">
<td>Sum</td>
<td>Usato per l'addizione e la sottrazione.<br/> v + p1 p2<br/></td>
</tr>
<tr class="even">
<td>Sumangle</td>
<td>Angolo esistente (ridimensionato di 65536), dove p1 e p2 sono in gradi.<br/> v + p1 * 65536 + p2 * 65536<br/></td>
</tr>
<tr class="odd">
<td>Tan</td>
<td>Tangente, l'argomento è in unità fd (gradi moltiplicati per 65536). <br/> v * tan( p1 )<br/></td>
</tr>
<tr class="even">
<td>Val</td>
<td>Definisce un valore guida da un altro valore.</td>
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
<td>Il parametro è un riferimento a una rettifica. Ad esempio, se il primo parametro è 1, verrà usato il valore della prima rettifica.</td>
</tr>
<tr class="odd">
<td>FormulaReference</td>
<td>Il parametro è il risultato di un riferimento al risultato di una formula precedente. Ad esempio, se il primo parametro è 2, verrà usato il risultato della formula 2.</td>
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
<td><strong>VgFormulaParamType</strong> Tipo del parametro 2.</td>
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



| Attributo | Descrizione                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Valore      | [Stringa](#data-types-used-in-the-vml-object-model). Valore di testo che specifica il percorso.         |
| Sinistra       | [Double](#data-types-used-in-the-vml-object-model). Coordinata più a sinistra del rettangolo.   |
| Inizio        | [Double](#data-types-used-in-the-vml-object-model). Coordinata superiore del rettangolo.    |
| Destra      | [Double](#data-types-used-in-the-vml-object-model). Coordinata più a destra del rettangolo.  |
| Ultimo     | [Double](#data-types-used-in-the-vml-object-model). Coordinata più in basso del rettangolo. |



 

**IVgFixedRectangleArray**

Matrice di rettangoli fissi.



| Attributo | Descrizione                                                                                                 |
|------------|-------------------------------------------------------------------------------------------------------------|
| Valore      | [Stringa](#data-types-used-in-the-vml-object-model). Rappresentazione testuale della matrice.                           |
| Length     | [Integer](#data-types-used-in-the-vml-object-model). Numero di rettangoli in questa matrice.                    |
| Elemento       | [IVgFixedRectangle](#data-types-used-in-the-vml-object-model). Oggetto rettangolo in corrispondenza dell'indice specificato. |



 

**Tipo di dati IVgFormula**

Definizioni per formule che possono variare il percorso di una forma o che possono essere usate per altri scopi di calcolo. Le formule possono essere basate **sull'attributo Adj** di una forma, che può cambiare. Le formule possono fare riferimento anche ad altre formule.



| Attributo| Descrizione                                           |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eqn        | [IVgEquation](#data-types-used-in-the-vml-object-model). Ogni formula definisce un singolo valore come risultato della valutazione dell'espressione. L'espressione è definita da questo attributo e ha la forma generale di un'operazione seguita da un massimo di tre argomenti, che possono essere valori di rettifica (ad esempio, 2), i risultati di formule precedenti (ad esempio, ), numeri fissi o valori \# @2 predefiniti. |



 

**Tipo di dati IVgFormulas**

Raccolta di oggetti formula.



| Attributo | Descrizione                                                                                                                                  |
|------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Length     | [Integer](#data-types-used-in-the-vml-object-model). Numero di oggetti formula nella raccolta.                                                |
| Elemento       | [IVgFormula](#data-types-used-in-the-vml-object-model). Formula specifica. Si noti che la matrice di formule può essere ereditata in base al tipo di forma. |



 

**IVgGradientColorArray**

Matrice di colori che definiscono una sfumatura (intervallo di colori misto).



| Attributo | Descrizione                                                                                                                  |
|------------|------------------------------------------------------------------------------------------------------------------------------|
| Valore      | [Stringa](#data-types-used-in-the-vml-object-model). Specifica la matrice di colori. ad esempio "red .2; verde .4; nero .7" |
| Length     | [Integer](#data-types-used-in-the-vml-object-model). Numero di colori nella matrice.                                          |



 



| Metodo     | Descrizione                                                                                                                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AddColor    | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Aggiunge il nuovo colore in corrispondenza dell'endpoint specificato da fraction. Il nuovo colore è bianco per impostazione predefinita e rappresenta il valore restituito. Il colore può quindi essere modificato in base al riferimento. |
| RemoveColor | [VgFraction](msdn-online-vml-vgfraction-data-type.md). Rimuove un colore in corrispondenza dell'endpoint specificato da fraction. Nota: se 0.0 o 1.0 non esiste, è implicito e il colore bianco viene usato a quel punto.          |



 

**Tipo di dati IVgPoints**

Matrice di punti che definiscono una forma.



| Attributo | Descrizione                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| Valore      | [Stringa](#data-types-used-in-the-vml-object-model). Rappresentazione testuale della matrice.           |
| Length     | [Integer](#data-types-used-in-the-vml-object-model). Numero di punti in questa matrice.        |
| Elemento       | [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md). Punto in corrispondenza dell'indice specificato. |



 

**Tipo di dati IVgSkewMatrix**

Matrice usata per le forme a inclinazione, matrice di trasformazione prospettica nel formato "*sxx,sxy,syx,syy,px,py* " \[ *s* =scale, *p* =perspective \] . Se offset è in unità assolute, *px,py* è in emu ^-1 unità; in caso contrario, sono una frazione inversa delle dimensioni della forma.



| Attributo   | Descrizione                                         |
|--------------|-----------------------------------------------------|
| XtoX         | [Double](#data-types-used-in-the-vml-object-model). |
| YtoX         | [Double](#data-types-used-in-the-vml-object-model). |
| XtoY         | [Double](#data-types-used-in-the-vml-object-model). |
| YtoY         | [Double](#data-types-used-in-the-vml-object-model). |
| PerspectiveX | [Double](#data-types-used-in-the-vml-object-model). |
| PerspectiveY | [Double](#data-types-used-in-the-vml-object-model). |



 

**IVgSkewOffset**

Specifica l'offset dell'aassamento.



<table>
<colgroup>
<col  />
<col  />
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
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente X. Percentuale o misura. Se non sono presenti unità, il tipo ShapeRelative è implicito; in caso contrario, il tipo assoluto è implicito.</td>
</tr>
<tr class="odd">
<td>S</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente Y.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><strong>VgSkewTransformType</strong>. Specifica il tipo di trasformazione. I valori validi sono punti interi compresi tra -infinity e infinity. 
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
<td>I valori dell'offset sono percentuali (proporzioni) delle dimensioni della forma originale. Ad esempio, un valore pari a 0,5 indica un offset pari alla metà delle dimensioni della forma.</td>
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

Specifica un vettore bidimensionale costituito da due **numeri Double.**



<table>
<colgroup>
<col  />
<col  />
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
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente X di questo vettore.</td>
</tr>
<tr class="odd">
<td>S</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente Y di questo vettore.</td>
</tr>
<tr class="even">
<td>Tipo</td>
<td><strong>VgVectorType</strong>. Unità previste per questo vettore. I valori possibili sono:
<ul>
<li>Misura</li>
<li>Length</li>
<li>AngleInDegrees</li>
<li>Fraction</li>
<li>Number Percentage Integer</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Tipo di dati IVgVector3D**

Specifica un vettore tridimensionale costituito da tre **numeri Double.**



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Valore</td>
<td><strong>Stringa</strong>. Rappresentazione testuale di tre numeri vettoriali separati da uno spazio.</td>
</tr>
<tr class="even">
<td>X</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente X di questo vettore.</td>
</tr>
<tr class="odd">
<td>S</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente Y di questo vettore.</td>
</tr>
<tr class="even">
<td>Z</td>
<td><a href="#data-types-used-in-the-vml-object-model">Double</a>. Componente Z di questo vettore.</td>
</tr>
<tr class="odd">
<td>Tipo</td>
<td><strong>VgVectorType</strong>. Unità previste per questo vettore. I valori possibili sono:
<ul>
<li>Misura</li>
<li>Length</li>
<li>AngleInDegrees</li>
<li>Fraction</li>
<li>Numero</li>
<li>Percentuale</li>
<li>Intero</li>
</ul></td>
</tr>
</tbody>
</table>



 

**Tipo di dati Length**

Numero a virgola mobile con un intervallo compreso tra 0 e infinito.

**Tipo di dati measure**

Numero a virgola mobile da -infinity a infinity.

**Tipo di dati String**

Dati di tipo carattere di qualsiasi lunghezza.

**VgBlackWhiteMode**

Modalità di rendering per il bianco e nero. I valori possibili sono:

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
-   **Non ridisegnato**

**Tipo di dati VgFraction**

Numero a virgola mobile con intervallo compreso tra 0,0 e 1,0. Le frazioni possono anche essere specificate come percentuale. ad esempio "50%".

**Tipo di dati VgTriState**

Enumerazione utilizzata per i valori che possono essere uno dei tre stati seguenti:

-   **TRUE**
-   **FALSE**
-   **MIXED**
