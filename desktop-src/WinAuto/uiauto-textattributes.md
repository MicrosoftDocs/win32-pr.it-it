---
title: Attributi di testo di automazione interfaccia utente
description: Questo argomento descrive il modo in cui automazione interfaccia utente Microsoft espone le proprietà di formato e stile (attributi di testo) del contenuto testuale e fornisce un elenco di attributi di testo supportati.
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- Automazione interfaccia utente, attributi di testo
- attributi di testo, informazioni
- attributi di testo, tipi Variant
- attributi di testo, tipi di dati
- Automazione interfaccia utente, elenco di attributi
- Automazione interfaccia utente, elenco di attributi di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b011203111a6484156921d63cc27bb11b017e596
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300120"
---
# <a name="ui-automation-text-attributes"></a>Attributi di testo di automazione interfaccia utente

Questo argomento descrive il modo in cui automazione interfaccia utente Microsoft espone le proprietà di formato e stile (*attributi di testo*) del contenuto testuale e fornisce un elenco di attributi di testo supportati.

I provider di automazione interfaccia utente espongono gli attributi di testo tramite i metodi [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) e [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) del pattern di controllo [TextRange](uiauto-about-text-and-textrange-patterns.md) . Le applicazioni client usano il metodo [**IUIAutomationTextRange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) per recuperare il valore di un attributo di testo specifico per un intervallo di testo. I client possono usare il metodo [**IUIAutomationTextRange:: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) per eseguire la ricerca in un intervallo di testo per il testo con un attributo specifico. Se viene trovato un testo corrispondente, il metodo crea un nuovo intervallo di testo che contiene il testo corrispondente.

Gli attributi di testo nell'elenco seguente sono supportati dal pattern di controllo **TextRange** . I nomi di attributo sono derivati dagli identificatori degli attributi di testo di automazione interfaccia utente. Ad esempio, l'attributo **AnimationStyle** viene identificato dai client come [**\_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (definito in UIAutomationClient. h) e dai provider come **testo \_ \_ \_ GUID dell'attributo AnimationStyle** (definito in Uiautomationcoreapi. h). Per altre informazioni su ogni attributo di testo supportato, vedere [**identificatori di attributi di testo**](uiauto-textattribute-ids.md).

> [!Note]  
> Alcuni degli attributi elencati sono supportati a partire da Windows 8. Vedere [**identificatori di attributi di testo**](uiauto-textattribute-ids.md) per note sul supporto della versione.

 

In questo argomento sono incluse le sezioni seguenti:

-   [Attributi di annotazione](#annotation-attributes)
-   [Attributi dei tipi di carattere](#font-attributes)
-   [Attributi del linguaggio](#language-attributes)
-   [Attributo link](#link-attribute)
-   [Attributi del margine della pagina](#page-margin-attributes)
-   [Attributi di allineamento del testo](#text-alignment-attributes)
-   [Attributi colore testo](#text-color-attributes)
-   [Attributi di decorazione testo](#text-decoration-attributes)
-   [Attributi di stile testo](#text-style-attributes)
-   [Attributi di interazione e selezione](#interaction-and-selection-attributes)
-   [Argomenti correlati](#related-topics)

## <a name="annotation-attributes"></a>Attributi di annotazione

Gli oggetti Annotation e i tipi di annotazione sono disponibili tramite gli attributi seguenti.



| Attributo             | Identificatore                                                            |
|-----------------------|-----------------------------------------------------------------------|
| **AnnotationObjects** | [**\_ANNOTATIONOBJECTSATTRIBUTEID UIA**](uiauto-textattribute-ids.md) |
| **AnnotationTypes**   | [**\_ANNOTATIONTYPESATTRIBUTEID UIA**](uiauto-textattribute-ids.md)   |



 

## <a name="font-attributes"></a>Attributi dei tipi di carattere

Il nome, le dimensioni e il peso di un tipo di carattere sono disponibili tramite gli attributi seguenti.



| Attributo      | Identificatore                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| **FontName**   | [**\_FONTNAMEATTRIBUTEID UIA**](uiauto-textattribute-ids.md)     |
| **FontSize**   | [**\_FONTSIZEATTRIBUTEID UIA**](uiauto-textattribute-ids.md)     |
| **SpessoreCarattere** | [**\_FONTWEIGHTATTRIBUTEID UIA**](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a>Attributi del linguaggio

Le informazioni sulla lingua del testo sono disponibili tramite gli attributi seguenti.



| Attributo              | Identificatore                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **culture**            | [**\_CULTUREATTRIBUTEID UIA**](uiauto-textattribute-ids.md)                       |
| **TextFlowDirections** | [**\_TEXTFLOWDIRECTIONSATTRIBUTEID UIA**](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a>Attributo link

L'attributo seguente fornisce l'intervallo di testo che rappresenta la destinazione di un collegamento in un documento.



| Attributo | Identificatore                                                                   |
|-----------|------------------------------------------------------------------------------|
| **Collegamento**  | [**\_LINKATTRIBUTEID UIA**](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a>Attributi del margine della pagina

I rettangoli di delimitazione di un intervallo di testo non espongono le coordinate del testo nella pagina. Tuttavia, un provider può esporre le informazioni sul margine della pagina usando gli attributi di testo seguenti.



| Attributo          | Identificatore                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| **MarginBottom**   | [**\_MARGINBOTTOMATTRIBUTEID UIA**](uiauto-textattribute-ids.md)     |
| **MarginLeading**  | [**\_MARGINLEADINGATTRIBUTEID UIA**](uiauto-textattribute-ids.md)   |
| **MarginTop**      | [**\_MARGINTOPATTRIBUTEID UIA**](uiauto-textattribute-ids.md)           |
| **MarginTrailing** | [**\_MARGINTRAILINGATTRIBUTEID UIA**](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a>Attributi di allineamento del testo

Le informazioni sull'allineamento del testo, ad esempio il rientro, le impostazioni di tabulazione e l'allineamento orizzontale, sono disponibili tramite gli attributi seguenti.



| Attributo                   | Identificatore                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| **HorizontalTextAlignment** | [**\_HORIZONTALTEXTALIGNMENTATTRIBUTEID UIA**](uiauto-textattribute-ids.md) |
| **IndentationFirstLine**    | [**\_INDENTATIONFIRSTLINEATTRIBUTEID UIA**](uiauto-textattribute-ids.md)       |
| **IndentationLeading**      | [**\_INDENTATIONLEADINGATTRIBUTEID UIA**](uiauto-textattribute-ids.md)           |
| **IndentationTrailing**     | [**\_INDENTATIONTRAILINGATTRIBUTEID UIA**](uiauto-textattribute-ids.md)         |
| **Schede**                    | [**\_TABSATTRIBUTEID UIA**](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a>Attributi colore testo

I colori del testo in primo piano e in background sono disponibili tramite gli attributi di testo seguenti. Entrambi i colori sono specificati come tipo di dati [**COLORREF**](/windows/desktop/gdi/colorref) .



| Attributo           | Identificatore                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| **BackgroundColor** | [**\_BACKGROUNDCOLORATTRIBUTEID UIA**](uiauto-textattribute-ids.md) |
| **ForegroundColor** | [**\_FOREGROUNDCOLORATTRIBUTEID UIA**](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a>Attributi di decorazione testo

Gli effetti di testo includono aree quali elenchi puntati, sottolinee e animazioni. Se il testo include punti elenco o numeri iniziali, il simbolo o il testo utilizzato per il punto elenco o il numero deve essere incluso nel flusso di testo, se applicabile.

Le informazioni sugli effetti di testo sono disponibili tramite gli attributi seguenti.



| Attributo              | Identificatore                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **AnimationStyle**     | [**\_ANIMATIONSTYLEATTRIBUTEID UIA**](uiauto-textattribute-ids.md)         |
| **BulletStyle**        | [**\_BULLETSTYLEATTRIBUTEID UIA**](uiauto-textattribute-ids.md)               |
| **OutlineStyles**      | [**\_OUTLINESTYLESATTRIBUTEID UIA**](uiauto-textattribute-ids.md)           |
| **OverlineColor**      | [**\_OVERLINECOLORATTRIBUTEID UIA**](uiauto-textattribute-ids.md)           |
| **OverlineStyle**      | [**\_OVERLINESTYLEATTRIBUTEID UIA**](uiauto-textattribute-ids.md)           |
| **StrikethroughColor** | [**\_STRIKETHROUGHCOLORATTRIBUTEID UIA**](uiauto-textattribute-ids.md) |
| **StrikethroughStyle** | [**\_STRIKETHROUGHSTYLEATTRIBUTEID UIA**](uiauto-textattribute-ids.md) |
| **UnderlineColor**     | [**\_UNDERLINECOLORATTRIBUTEID UIA**](uiauto-textattribute-ids.md)         |
| **UnderlineStyle**     | [**\_UNDERLINESTYLEATTRIBUTEID UIA**](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a>Attributi di stile testo

Le informazioni sugli stili di testo sono disponibili anche con gli attributi seguenti.



| Attributo         | Identificatore                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| **CapStyle**      | [**\_CAPSTYLEATTRIBUTEID UIA**](uiauto-textattribute-ids.md)           |
| **IsHidden**      | [**\_ISHIDDENATTRIBUTEID UIA**](uiauto-textattribute-ids.md)           |
| **IsItalic**      | [**\_ISITALICATTRIBUTEID UIA**](uiauto-textattribute-ids.md)           |
| **IsReadOnly**    | [**\_ISREADONLYATTRIBUTEID UIA**](uiauto-textattribute-ids.md)       |
| **IsSuperscript** | [**\_ISSUPERSCRIPTATTRIBUTEID UIA**](uiauto-textattribute-ids.md) |
| **IsSubscript**   | [**\_ISSUBSCRIPTATTRIBUTEID UIA**](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a>Attributi di interazione e selezione

Le informazioni sulla selezione di testo corrente nello stato intervallo e stato attivo sono disponibili anche se gli attributi seguenti.



| Attributo              | Identificatore                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| **IsActive**           | [**\_ISACTIVEATTRIBUTEID UIA**](uiauto-textattribute-ids.md)           |
| **SelectionActiveEnd** | [**\_SELECTIONACTIVEENDATTRIBUTEID UIA**](uiauto-textattribute-ids.md) |
| **CaretPosition**      | [**\_CARETPOSITIONATTRIBUTEID UIA**](uiauto-textattribute-ids.md)      |
| **CaretBidiMode**      | [**\_CARETBIDIMODEATTRIBUTEID UIA**](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sul testo di automazione interfaccia utente e sui pattern di controllo TextRange](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[Pattern di controllo Text e TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Utilizzo di controlli basati su testo](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 