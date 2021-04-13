---
title: Controllo carattere
description: Per semplificare l'integrazione e la configurazione del supporto per i tipi di carattere nelle applicazioni che richiedono l'elaborazione di testi e le funzionalità di modifica del testo, il Framework della barra multifunzione di Windows fornisce un controllo del tipo di carattere specializzato che espone un'ampia gamma di proprietà dei tipi di carattere, ad esempio il nome tipografico, lo stile
ms.assetid: 6052f2e3-2c9e-432e-9ed6-c1e3a50843d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e179296ae03163bf03e08d2fbf7287264792e6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399283"
---
# <a name="font-control"></a>Controllo carattere

Per semplificare l'integrazione e la configurazione del supporto per i tipi di carattere nelle applicazioni che richiedono l'elaborazione di testi e le funzionalità di modifica del testo, il Framework della barra multifunzione di Windows fornisce un controllo del tipo di carattere specializzato che espone un'ampia gamma di proprietà dei tipi di carattere, ad esempio il nome tipografico, lo stile

-   [Introduzione](#introduction)
-   [Esperienza coerente](#a-consistent-experience)
-   [Facile integrazione e configurazione](#easy-integration-and-configuration)
-   [Allineamento con strutture di testo GDI comuni](#alignment-with-common-gdi-text-structures)
-   [Aggiungere un FontControl](#add-a-fontcontrol)
    -   [Dichiarazione di un FontControl nel markup](#declaring-a-fontcontrol-in-markup)
    -   [Proprietà del controllo del tipo di carattere](#font-control-properties)
-   [Definire un gestore di comandi FontControl](#define-a-fontcontrol-command-handler)
-   [Argomenti correlati](#related-topics)

## <a name="introduction"></a>Introduzione

Il controllo del tipo di carattere è un controllo composto costituito da pulsanti, pulsanti di attivazione, caselle di riepilogo a discesa e caselle combinate, tutti usati per specificare una particolare proprietà del tipo di carattere o un'opzione di formattazione.

Lo screenshot seguente mostra il controllo del tipo di carattere della barra multifunzione in WordPad per Windows 7.

![screenshot dell'elemento fontcontrol con l'attributo richfont impostato su true.](images/controls/fontcontrol.png)

## <a name="a-consistent-experience"></a>Esperienza coerente

Come controllo della barra multifunzione incorporato, il controllo del tipo di carattere migliora le funzionalità generali di gestione dei caratteri, selezione e formattazione e offre un'esperienza utente avanzata e coerente in tutte le applicazioni della barra multifunzione.

Questa esperienza coerente include

-   Formattazione standardizzata e selezione di tipi di carattere nelle applicazioni della barra multifunzione.
-   Rappresentazione dei tipi di carattere standardizzata nelle applicazioni della barra multifunzione.
-   Automatica, in Windows 7, attivazione dei tipi di carattere basata sull'impostazione **Mostra** o **Nascondi** per ogni tipo di carattere nel pannello di controllo dei **tipi** di carattere. Il controllo font Visualizza solo i tipi di carattere impostati per la **visualizzazione**.
    > [!Note]  
    > In Windows Vista, il pannello di controllo dei **tipi di carattere** non offre la funzionalità **Mostra** o **Nascondi** , quindi tutti i tipi di carattere sono attivati.

     

-   Gestione dei tipi di carattere disponibile direttamente dal controllo.

    Lo screenshot seguente mostra che è possibile accedere al pannello di controllo dei **tipi di carattere** direttamente dal controllo del tipo di carattere.

    ![screenshot dell'elenco di famiglie di caratteri in WordPad per Windows 7.](images/controls/fontcontrol-fontcpl.png)

-   Supporto per l'anteprima automatica.
-   Esposizione dei tipi di carattere più rilevanti per un utente, ad esempio
    -   Elenchi di tipi di carattere localizzati per gli utenti internazionali.
    -   Elenchi di tipi di carattere basati sul dispositivo di input.

    > [!Note]  
    > Il supporto per questa funzionalità non è disponibile in nessuna piattaforma precedente a Windows 7.

     

## <a name="easy-integration-and-configuration"></a>Facile integrazione e configurazione

Grazie alla funzionalità standard, riutilizzabile e facilmente utilizzata, il controllo del tipo di carattere della barra multifunzione semplifica l'integrazione del supporto dei tipi di carattere in un'applicazione.

I dettagli della selezione e della formattazione dei tipi di carattere sono racchiusi in un elemento logico autonomo che

-   Elimina la gestione complessa delle interdipendenze del controllo tipiche delle implementazioni del controllo del tipo di carattere.
-   Richiede un singolo gestore di comando per tutte le funzionalità esposte dai controlli secondari del controllo del tipo di carattere.

Questo unico gestore comando consente al controllo del tipo di carattere di gestire internamente la funzionalità di vari controlli secondari; un sottocontrollo non interagisce mai direttamente con l'applicazione, indipendentemente dalla funzione.

Altre funzionalità del controllo del tipo di carattere includono

-   Generazione automatica in grado di riconoscere DPI di un oggetto WYSIWYG (elementi visualizzati) rappresentazione bitmap per ogni tipo di carattere nel menu della **famiglia di caratteri** .
-   Integrazione di [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) .
-   Bitmap e descrizioni comandi della famiglia di caratteri localizzati.
-   Enumerazione del tipo di carattere, raggruppamento e metadati per la gestione e la presentazione di tipi di carattere.
    > [!Note]  
    > Il supporto per questa funzionalità non è disponibile in nessuna piattaforma precedente a Windows 7.

     

-   Il colore del **testo** e i [selettori](windowsribbon-controls-dropdowncolorpicker.md) di colore dell' **evidenziazione del testo** che riflettono il comportamento della selezione colori a discesa della barra multifunzione.
-   Supporto dell'anteprima automatica da parte di tutti i controlli secondari basati sulla raccolta di controlli del tipo di carattere: **famiglia di caratteri**, **dimensioni del carattere**, colore del **testo** e **colore di evidenziazione del testo**.

## <a name="alignment-with-common-gdi-text-structures"></a>Allineamento con strutture di testo GDI comuni

I componenti dello stack di testo di [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) vengono utilizzati per esporre la funzionalità di selezione e formattazione del tipo di carattere tramite il controllo del tipo di carattere Le varie funzionalità del tipo di carattere supportate dalla struttura [LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), dalla struttura [ChooseFont](/windows/win32/api/commdlg/ns-commdlg-choosefonta)e dalla [struttura CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a) sono esposte tramite i controlli secondari inclusi nel controllo del tipo di carattere.

I controlli secondari visualizzati nel controllo del tipo di carattere dipendono dal modello *FontType* dichiarato nel markup della barra multifunzione. I modelli *FontType* , descritti in dettaglio nella sezione seguente, sono progettati per essere allineati alle strutture di testo comuni di [Windows Graphics Device Interface (GDI)](../gdi/windows-gdi.md) .

## <a name="add-a-fontcontrol"></a>Aggiungere un FontControl

In questa sezione vengono descritti i passaggi di base per l'aggiunta di un controllo del tipo di carattere a un'applicazione Ribbon.

### <a name="declaring-a-fontcontrol-in-markup"></a>Dichiarazione di un FontControl nel markup

Analogamente ad altri controlli della barra multifunzione, il controllo del tipo di carattere viene dichiarato nel markup con un elemento [**FontControl**](windowsribbon-element-fontcontrol.md) e associato a una dichiarazione di comando tramite un ID di comando. Quando l'applicazione viene compilata, l'ID comando viene usato per associare il comando a un gestore di comando nell'applicazione host.

> [!Note]  
> Se non viene dichiarato alcun ID di comando con [**FontControl**](windowsribbon-element-fontcontrol.md) nel markup, ne viene generato uno dal Framework.

 

Poiché i controlli secondari del controllo del tipo di carattere non sono esposti direttamente, la personalizzazione del controllo del tipo di carattere è limitata a tre modelli di layout *FontType* definiti dal Framework.

Una maggiore personalizzazione del controllo del tipo di carattere può essere eseguita combinando il modello di layout con attributi [**FontControl**](windowsribbon-element-fontcontrol.md) , ad esempio *IsHighlightButtonVisible*, *IsStrikethroughButtonVisible* e *IsUnderlineButtonVisible*.

> [!Note]  
> Le funzionalità dei tipi di carattere oltre a quelle esposte dagli attributi e dai modelli di controllo dei tipi di carattere standard richiedono un'implementazione del controllo del tipo di carattere personalizzata che esula dall'ambito di

 

Nella tabella seguente sono elencati i modelli di controllo dei tipi di carattere e il tipo di controllo di modifica a cui è allineato ogni modello.



| Modello      | Supporti                                                                 |
|---------------|--------------------------------------------------------------------------|
| FontOnly      | [LOGFONT (struttura)](/windows/win32/api/wingdi/ns-wingdi-logfonta)     |
| FontWithColor | [Struttura CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)  |
| RichFont      | [Struttura CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a) |



 

Nella tabella seguente sono elencati i controlli associati a ogni modello e vengono identificati i controlli facoltativi per un modello associato.



Controlli

Modelli

**RichFont**

**FontWithColor**

**FontOnly**

Predefinito

Facoltativo

Predefinito

Facoltativo

Predefinito

Facoltativo

Casella combinata **dimensione carattere**

Sì

No

Sì

No

Sì

No

Casella combinata della **famiglia di caratteri**

Sì

No

Sì

No

Sì

No

Pulsante **Grow font**

Sì

Sì

Sì

Sì

\-

\-

Pulsante **compatta carattere**

Sì

Sì

Sì

Sì

\-

\-

Pulsante **grassetto**

Sì

No

Sì

No

Sì

No

Pulsante **corsivo**

Sì

No

Sì

No

Sì

No

Pulsante **sottolineato**

Sì

No

Sì

Sì

Sì

Sì

Pulsante **barrato**

Sì

No

Sì

Sì

Sì

Sì

Pulsante **Indice**

Sì

No

\-

\-

\-

\-

Pulsante **apice**

Sì

No

\-

\-

\-

\-

Pulsante **colore evidenziazione testo**

Sì

No

Sì

Sì

\-

\-

Pulsante **colore testo**

Sì

No

Sì

No

\-

\-



 

Quando viene dichiarato il comportamento del layout di un controllo del tipo di carattere, il Framework della barra multifunzione fornisce un modello di layout *SizeDefinition* facoltativo, `OneFontControl` , che definisce due configurazioni di sottocontrollo in base alla dimensione della barra multifunzione e allo spazio disponibile per il controllo del tipo di carattere. Per ulteriori informazioni, vedere [personalizzazione di una barra multifunzione tramite le definizioni delle dimensioni e i criteri di scalabilità](windowsribbon-templates.md).

### <a name="adding-a-fontcontrol-to-a-ribbon"></a>Aggiunta di un FontControl a una barra multifunzione

Gli esempi di codice seguenti illustrano i requisiti di markup di base per l'aggiunta di un controllo tipo di carattere a una barra multifunzione

Questa sezione di codice mostra il markup della dichiarazione del comando [**FontControl**](windowsribbon-element-fontcontrol.md) , inclusi i comandi di [**tabulazione**](windowsribbon-element-tab.md) e [**gruppo**](windowsribbon-element-group.md) necessari per visualizzare un controllo nella [**barra multifunzione**](windowsribbon-element-ribbon.md).


```C++
<Command Name="cmdTab1"
  Comment="These comments are optional and are inserted into the header file."
  Symbol="cmdTab1" Id="10000" >
  <Command.LabelTitle>Tab 1</Command.LabelTitle>
</Command>
<Command Name="cmdGroup1" Comment="Group #1" Symbol="cmdGroup1" Id="20000">
  <!-- This image is used when the group scales to a pop-up. -->
  <Command.SmallImages>
    <Image>res/Button_Image.bmp</Image>
  </Command.SmallImages>
</Command>
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



Questa sezione di codice mostra il markup necessario per dichiarare e associare un [**FontControl**](windowsribbon-element-fontcontrol.md) a un [**comando**](windowsribbon-element-command.md) tramite un ID di comando. Questo particolare esempio include le dichiarazioni di [**tabulazione**](windowsribbon-element-tab.md) e di [**gruppo**](windowsribbon-element-group.md) , con preferenze di ridimensionamento.


```C++
<Ribbon.Tabs>
  <Tab CommandName="cmdTab1">
    <Tab.ScalingPolicy>
      <ScalingPolicy>
        <ScalingPolicy.IdealSizes>
          <Scale Group="cmdGroup1" Size="Large" />
        </ScalingPolicy.IdealSizes>
        <!-- Describe how the FontControl group scales. -->
        <Scale Group="cmdGroup1" Size="Medium" />
        <Scale Group="cmdGroup1" Size="Popup" />
      </ScalingPolicy>
    <Group CommandName="cmdGroup1" SizeDefinition="OneFontControl">
      <FontControl CommandName="cmdFontControl" FontType="RichFont" />
    </Group>
  </Tab>
</Ribbon.Tabs>
```



### <a name="adding-a-fontcontrol-to-a-contextpopup"></a>Aggiunta di un FontControl a un ContextPopup

L'aggiunta di un controllo del tipo di carattere a un [popup del contesto](windowsribbon-controls-contextpopup.md) richiede una procedura simile a quella di aggiunta di un controllo tipo di carattere alla barra multifunzione. Tuttavia, un controllo del tipo di carattere in un [**MiniToolbar**](windowsribbon-element-minitoolbar.md) è limitato al set di controlli secondari predefiniti comuni a tutti i modelli di controllo dei tipi di carattere: **famiglia di caratteri**, **dimensioni del carattere**, **grassetto** e **corsivo**.

Gli esempi di codice seguenti illustrano i requisiti di markup di base per aggiungere un controllo del tipo di carattere a un [popup del contesto](windowsribbon-controls-contextpopup.md):

Questa sezione di codice mostra il markup della dichiarazione di comando [**FontControl**](windowsribbon-element-fontcontrol.md) necessario per visualizzare un **FontControl** in [**ContextPopup**](windowsribbon-element-contextpopup.md).


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" />
```



Questa sezione di codice mostra il markup necessario per dichiarare e associare un [**FontControl**](windowsribbon-element-fontcontrol.md) a un comando tramite un ID di comando.


```C++
<ContextPopup.MiniToolbars>
  <MiniToolBar Name="MiniToolbar1">
    <MenuCategory Class="StandardItems">
      <FontControl CommandName="cmdFontControl" />
    </MenuCategory>
  </MiniToolBar>
</ContextPopup.MiniToolbars>
```



### <a name="keytips"></a>Suggerimenti per i tasti di scelta

Ogni sottocontrollo nel controllo del tipo di carattere della barra multifunzione è accessibile tramite un tasto di scelta rapida o un suggerimento tasto di scelta. Questo suggerimento è predefinito e assegnato a ogni sottocontrollo dal Framework.

Se un valore dell'attributo del tasto di *Suggerimento* viene assegnato all'elemento [**FontControl**](windowsribbon-element-fontcontrol.md) nel markup, questo valore viene aggiunto come prefisso al suggerimento tasto di definizione definito dal Framework.

> [!Note]  
> L'applicazione deve applicare una regola a carattere singolo per questo prefisso.

 

Nella tabella seguente sono elencati i suggerimenti tasti definiti dal Framework. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Controllo secondario</th>
<th>Suggerimento tasto</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Famiglia di caratteri</td>
<td>F</td>
</tr>
<tr class="even">
<td>Stile carattere</td>
<td>T</td>
</tr>
<tr class="odd">
<td>Dimensioni del carattere</td>
<td>S</td>
</tr>
<tr class="even">
<td>Espandi carattere</td>
<td>G</td>
</tr>
<tr class="odd">
<td>Compatta carattere</td>
<td>K</td>
</tr>
<tr class="even">
<td>Grassetto</td>
<td>B</td>
</tr>
<tr class="odd">
<td>Corsivo</td>
<td>I</td>
</tr>
<tr class="even">
<td>Sottolineato</td>
<td>U</td>
</tr>
<tr class="odd">
<td>barrato</td>
<td>X</td>
</tr>
<tr class="even">
<td>Apice</td>
<td>Y o Z
<blockquote>
[!Note]<br />
Se l'attributo del <em>Suggerimento</em> tasto di opzione non è dichiarato nel markup, il suggerimento predefinito è Y; in caso contrario, il suggerimento tasto di opzione predefinito è il <em>Suggerimento</em> + Z.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Pedice</td>
<td>A</td>
</tr>
<tr class="even">
<td>Colore carattere</td>
<td>C</td>
</tr>
<tr class="odd">
<td>Evidenziazione carattere</td>
<td>H</td>
</tr>
</tbody>
</table>



 

Il prefisso consigliato per una barra multifunzione di Multilingual User Interface (MUI) EN-US è' F ', come illustrato nell'esempio seguente.


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



Lo screenshot seguente illustra i suggerimenti dei tasti di controllo del tipo di carattere così come sono definiti nell'esempio precedente.

![screenshot dei suggerimenti per i tasti di fontcontrol in WordPad per Windows 7.](images/controls/fontcontrol-keytips.png)

### <a name="the-ribbon-resource-file"></a>File di risorse della barra multifunzione

Quando il file di markup viene compilato, viene generato un file di risorse che contiene tutti i riferimenti alle risorse per l'applicazione Ribbon.

Esempio di un file di risorse semplice:


```C++
// ******************************************************************************
// * This is an automatically generated file containing the ribbon resource for *
// * your application.                                                          *
// ******************************************************************************

#include ".\ids.h"

STRINGTABLE 
BEGIN
  cmdTab1_LabelTitle_RESID L"Tab 1" 
    /* LabelTitle cmdTab1_LabelTitle_RESID: These comments are optional and are 
       inserted into the header file. */
END

cmdGroup1_SmallImages_RESID    BITMAP    "res\\Button_Image.bmp" 
  /* SmallImages cmdGroup1_SmallImages_RESID: Group #1 */
STRINGTABLE 
BEGIN
  cmdFontControl_Keytip_RESID L"F" /* Keytip cmdFontControl_Keytip_RESID: FontControl */
END

FCSAMPLE_RIBBON    UIFILE    "Debug\\FCSample.bml"

```



### <a name="font-control-properties"></a>Proprietà del controllo del tipo di carattere

Il Framework della barra multifunzione definisce una raccolta di [chiavi di proprietà](windowsribbon-reference-properties.md) per il controllo del tipo di carattere e i relativi controlli secondari.

In genere, una proprietà del controllo del tipo di carattere viene aggiornata nell'interfaccia utente della barra multifunzione invalidando il comando associato al controllo tramite una chiamata al metodo [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . L'evento di invalidamento viene gestito e gli aggiornamenti delle proprietà definiti dal metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Il metodo di callback [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) non viene eseguito e l'applicazione ha sottoposto a query un valore aggiornato della proprietà, fino a quando la proprietà non è richiesta dal Framework. Ad esempio, quando viene attivata una scheda e viene visualizzato un controllo nell'interfaccia utente della barra multifunzione o quando viene visualizzata una descrizione comando.

> [!Note]  
> In alcuni casi, una proprietà può essere recuperata tramite il metodo [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e impostata con il metodo [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

Nella tabella seguente sono elencate le chiavi di proprietà associate al controllo del tipo di carattere.



| Chiave della proprietà                                                                                                                  | Note                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interfaccia utente \_ pkey \_ FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md)                                      | Espone, in aggregato come oggetto [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) , tutte le proprietà del sottocontrollo del controllo del tipo di carattere.<br/> Il Framework esegue una query su questa proprietà quando `UI_INVALIDATIONS_VALUE` viene passato come valore di *flag* nella chiamata a [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).<br/> |
| [Interfaccia utente \_ pkey \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md) | Espone, in aggregato come oggetto [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) , solo le proprietà del controllo del sottocontrollo del tipo di carattere che sono state modificate.<br/>                                                                                                                                                                                                        |
| [Suggerimento tasto di interfaccia utente \_ pkey \_](windowsribbon-reference-properties-uipkey-keytip.md)                                                      | Può essere aggiornato solo tramite l'invalidamento.                                                                                                                                                                                                                                                                                                                                                      |
| [Interfaccia utente \_ pkey \_ abilitata](windowsribbon-reference-properties-uipkey-enabled.md)                                                    | Supporta [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).                                                                                                                                                                  |



 

Oltre alle proprietà supportate dal controllo del tipo di carattere stesso, il Framework della barra multifunzione definisce anche una [chiave di proprietà](windowsribbon-reference-properties.md) per ogni controllo secondario del controllo del tipo di carattere. Queste chiavi di proprietà e i relativi valori vengono esposte dal Framework tramite un'implementazione dell'interfaccia [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) che definisce i metodi per la gestione di una raccolta, denominata anche contenitore delle proprietà, di coppie nome-valore.

L'applicazione converte le strutture dei tipi di carattere in proprietà accessibili tramite i metodi di interfaccia [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) . Questo modello enfatizza la distinzione tra il controllo del tipo di carattere e i componenti dello stack di testo di Windows Graphics Device Interface (GDI) ([struttura LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), [struttura ChooseFont](/windows/win32/api/commdlg/ns-commdlg-choosefonta)e [struttura CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a)) supportati dal Framework.

Nella tabella seguente sono elencati i singoli controlli e le relative chiavi di proprietà associate.



| Controlli                 | Chiave della proprietà                                                                                                                                                                                                                                                           | Note                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Dimensioni carattere**            | [\_ \_ Dimensioni FontProperties dell'interfaccia utente pkey \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Quando viene evidenziata un'esecuzione di testo di dimensioni eterogenee, il Framework della barra multifunzione imposta il controllo della **dimensione del carattere** su Blank e il valore di [UI \_ pkey \_ FontProperties \_ size](windowsribbon-reference-properties-uipkey-fontproperties-size.md) su 0. Quando si fa clic sul pulsante **Grow font** o **Shrink font** , tutto il testo evidenziato viene ridimensionato, ma viene mantenuta la differenza relativa nelle dimensioni del testo.                                                                                                                                                    |
| **Famiglia di caratteri**          | [Interfaccia \_ utente \_ pkey \_ famiglia FontProperties](windowsribbon-reference-properties-uipkey-fontproperties-family.md)                                                                                                                                                                | I nomi delle famiglie di caratteri GDI variano a seconda delle impostazioni locali del sistema. Di conseguenza, se il valore di [UI \_ pkey \_ FontProperties \_ Family](windowsribbon-reference-properties-uipkey-fontproperties-family.md) viene mantenuto nelle sessioni dell'applicazione, tale valore deve essere recuperato in ogni nuova sessione.                                                                                                                                                                                                                                                                            |
| **Espandi carattere**            | [\_ \_ Dimensioni FontProperties dell'interfaccia utente pkey \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Vedere **dimensioni carattere**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Compatta carattere**          | [\_ \_ Dimensioni FontProperties dell'interfaccia utente pkey \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Vedere **dimensioni carattere**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Grassetto**                 | [Interfaccia utente \_ pkey \_ FontProperties \_ Bold](windowsribbon-reference-properties-uipkey-fontproperties-bold.md)                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Corsivo**               | [Interfaccia utente \_ pkey \_ FontProperties \_ corsivo](windowsribbon-reference-properties-uipkey-fontproperties-italic.md)                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Sottolineato**            | [\_ \_ Sottolineato FontProperties pkey dell'interfaccia utente \_](windowsribbon-reference-properties-uipkey-fontproperties-underline.md)                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **barrato**        | [Barra dell'interfaccia utente \_ pkey \_ FontProperties \_](windowsribbon-reference-properties-uipkey-fontproperties-strikethrough.md)                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Pedice**            | [Interfaccia utente \_ pkey \_ FontProperties \_ VerticalPositioning](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | Se viene impostato il pulsante **pedice** , non è possibile impostare anche l' **apice** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Apice**          | [Interfaccia utente \_ pkey \_ FontProperties \_ VerticalPositioning](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | Se il pulsante **apice** è impostato, non è possibile impostare anche il **pedice** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Colore di evidenziazione testo** | [Interfaccia utente \_ PKEY \_ FontProperties \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI \_ pkey \_ FontProperties \_ BackgroundColorType](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md) | Fornisce la stessa funzionalità del `HighlightColors` modello dell'elemento [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .<br/> Si consiglia vivamente di impostare l'applicazione solo un valore di **colore di evidenziazione del testo** iniziale. L'ultimo valore selezionato deve essere mantenuto e non impostato quando il cursore viene riposizionato all'interno di un documento. In questo modo è possibile accedere rapidamente all'ultima selezione dell'utente e non è necessario riaprire la selezione colori.<br/> I campioni di colore non possono essere personalizzati.<br/> |
| **Colore del testo**           | [Interfaccia utente \_ PKEY \_ FontProperties \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [UI \_ pkey \_ FontProperties \_ ](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md) ForegroundColorType           | Fornisce la stessa funzionalità del `StandardColors` modello dell'elemento [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) .<br/> Si consiglia vivamente di impostare l'applicazione solo un valore di **colore del testo** iniziale. L'ultimo valore selezionato deve essere mantenuto e non impostato quando il cursore viene riposizionato all'interno di un documento. In questo modo è possibile accedere rapidamente all'ultima selezione dell'utente e non è necessario riaprire la selezione colori.<br/> I campioni di colore non possono essere personalizzati.<br/>            |



 

## <a name="define-a-fontcontrol-command-handler"></a>Definire un gestore di comandi FontControl

In questa sezione vengono descritti i passaggi necessari per associare un controllo del tipo di carattere a un gestore comando.

> [!WARNING]
> Qualsiasi tentativo di selezionare un campione di colore dalla selezione colori di un controllo del tipo di carattere può causare una violazione di accesso se al controllo non è associato alcun gestore di comando.

 

Nell'esempio di codice riportato di seguito viene illustrato come associare i comandi dichiarati nel markup a un gestore di comandi.


```C++
//
//  FUNCTION: OnCreateUICommand(UINT, UI_COMMANDTYPE, IUICommandHandler)
//
//  PURPOSE: Called by the Ribbon framework for each command specified in markup, to allow
//           the host application to bind a command handler to that command.
//
STDMETHODIMP CApplication::OnCreateUICommand(
  UINT nCmdID,
  __in UI_COMMANDTYPE typeID,
  __deref_out IUICommandHandler** ppCommandHandler)
{
  UNREFERENCED_PARAMETER(typeID);
  UNREFERENCED_PARAMETER(nCmdID);

  if (NULL == m_pCommandHandler)
  {
    HRESULT hr = CCommandHandler::CreateInstance(&m_pCommandHandler);
    if (FAILED(hr))
    {
      return hr;
    }
  }

  return m_pCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
}
```



Nell'esempio di codice seguente viene illustrato come implementare il metodo [**IUICommandHandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) per un controllo del tipo di carattere.


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a command is executed 
//           by the user. For example, when a button is pressed.
//
STDMETHODIMP CCommandHandler::Execute(
  UINT nCmdID,
  UI_EXECUTIONVERB verb,
  __in_opt const PROPERTYKEY* key,
  __in_opt const PROPVARIANT* ppropvarValue,
  __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if ((key) && (*key == UI_PKEY_FontProperties))
  {
    // Font properties have changed.
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Using the changed properties, set the new font on the selection on RichEdit control.
              g_pFCSampleAppManager->SetValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_PREVIEW:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties for the preview event.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Set the previewed values on the RichEdit control.
              g_pFCSampleAppManager->SetPreviewValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_CANCELPREVIEW:
      {
        hr = E_POINTER;
        if (ppropvarValue != NULL)
        {
          // Cancel the preview.
          IPropertyStore *pValues;
          hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarValue, &pValues);
          if (SUCCEEDED(hr))
          {   
            g_pFCSampleAppManager->CancelPreview(pValues);
            pValues->Release();
          }
        }
        break;
      }
    }
  }

  return hr;
}
```



Nell'esempio di codice seguente viene illustrato come implementare il metodo [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) per un controllo del tipo di carattere.


```C++
//
//  FUNCTION: UpdateProperty()
//
//  PURPOSE: Called by the Ribbon framework when a command property (PKEY) needs to be updated.
//
//  COMMENTS:
//
//    This function is used to provide new command property values, such as labels, icons, or
//    tooltip information, when requested by the Ribbon framework.  
//    
//
STDMETHODIMP CCommandHandler::UpdateProperty(
  UINT nCmdID,
  __in REFPROPERTYKEY key,
  __in_opt const PROPVARIANT* ppropvarCurrentValue,
  __out PROPVARIANT* ppropvarNewValue)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_FontProperties)
  {
    hr = E_POINTER;
    if (ppropvarCurrentValue != NULL)
    {
      // Get the font values for the selected text in the font control.
      IPropertyStore *pValues;
      hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarCurrentValue, &pValues);
      if (SUCCEEDED(hr))
      {
        g_pFCSampleAppManager->GetValues(pValues);

        // Provide the new values to the font control.
        hr = UIInitPropertyFromInterface(UI_PKEY_FontProperties, pValues, ppropvarNewValue);
        pValues->Release();
      }
    }
  }

  return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Libreria di controlli Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento FontControl**](windowsribbon-element-fontcontrol.md)
</dt> <dt>

[Proprietà del controllo del tipo di carattere](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Esempio FontControl](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

