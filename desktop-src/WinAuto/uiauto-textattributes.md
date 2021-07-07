---
title: Automazione interfaccia utente di testo
description: Questo argomento descrive come Microsoft Automazione interfaccia utente il formato e le proprietà di stile (attributi di testo) del contenuto testuale e fornisce un elenco di attributi di testo supportati.
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- Automazione interfaccia utente,attributi di testo
- attributi di testo, informazioni
- attributi di testo, tipi variant
- attributi di testo, tipi di dati
- Automazione interfaccia utente,elenco di attributi
- Automazione interfaccia utente,elenco di attributi di testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8ae2d51a222e3833d0dd95fa6c048114a370a6
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353624"
---
# <a name="ui-automation-text-attributes"></a>Automazione interfaccia utente di testo

Questo argomento descrive come Microsoft Automazione interfaccia utente il formato e le proprietà di stile *(* attributi di testo ) del contenuto testuale e fornisce un elenco di attributi di testo supportati.

Automazione interfaccia utente provider di testo espongono attributi di testo tramite [**i metodi GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) [**e FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) del [pattern di controllo TextRange.](uiauto-about-text-and-textrange-patterns.md) Le applicazioni client usano [**il metodo IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) per recuperare il valore di un particolare attributo di testo per un intervallo di testo. I client possono usare [**il metodo IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) per cercare testo con un attributo specifico in un intervallo di testo. Se viene trovato un testo corrispondente, il metodo crea un nuovo intervallo di testo contenente il testo corrispondente.

Gli attributi di testo nell'elenco seguente sono supportati dal pattern **di controllo TextRange.** I nomi degli attributi derivano dagli identificatori Automazione interfaccia utente degli attributi di testo. Ad esempio, l'attributo **AnimationStyle** viene identificato dai client come [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (definito in Uiautomationclient.h) e dai provider come GUID dell'attributo **Text \_ \_ \_ AnimationStyle** (definito in Uiautomationcoreapi.h). Per altre informazioni su ogni attributo di testo supportato, vedere [**Identificatori di attributi di testo**](uiauto-textattribute-ids.md).

> [!Note]  
> Alcuni degli attributi elencati sono supportati a partire da Windows 8. Per le note sul supporto [**della versione,**](uiauto-textattribute-ids.md) vedere Identificatori di attributi di testo.

 

In questo argomento sono incluse le sezioni seguenti:

-   [Attributi di annotazione](#annotation-attributes)
-   [Attributi dei tipi di carattere](#font-attributes)
-   [Attributi del linguaggio](#language-attributes)
-   [Attributo di collegamento](#link-attribute)
-   [Attributi del margine di pagina](#page-margin-attributes)
-   [Attributi di allineamento del testo](#text-alignment-attributes)
-   [Attributi di colore del testo](#text-color-attributes)
-   [Attributi di decorazione del testo](#text-decoration-attributes)
-   [Attributi di stile del testo](#text-style-attributes)
-   [Attributi di interazione e selezione](#interaction-and-selection-attributes)
-   [Argomenti correlati](#related-topics)

## <a name="annotation-attributes"></a>Attributi di annotazione

Gli oggetti annotazione e i tipi di annotazione sono disponibili tramite gli attributi seguenti.



| Attributo             | Identificatore                                                            |
|-----------------------|-----------------------------------------------------------------------|
| **AnnotationObjects** | [**UIA \_ AnnotationObjectsAttributeId**](uiauto-annotation-type-identifiers.md) |
| **AnnotationTypes**   | [**UIA \_ AnnotationTypesAttributeId**](uiauto-annotation-type-identifiers.md)   |



 

## <a name="font-attributes"></a>Attributi dei tipi di carattere

Il nome, la dimensione e lo spessore di un tipo di carattere sono disponibili tramite gli attributi seguenti.



| Attributo      | Identificatore                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| **FontName**   | [**UIA \_ FontNameAttributeId**](uiauto-textattribute-ids.md)     |
| **FontSize**   | [**UIA \_ FontSizeAttributeId**](uiauto-textattribute-ids.md)     |
| **SpessoreCarattere** | [**UIA \_ FontWeightAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a>Attributi del linguaggio

Le informazioni sulla lingua del testo sono disponibili tramite gli attributi seguenti.



| Attributo              | Identificatore                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **culture**            | [**UIA \_ CultureAttributeId**](uiauto-textattribute-ids.md)                       |
| **TextFlowDirections** | [**UIA \_ TextFlowDirectionsAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a>Attributo di collegamento

L'attributo seguente fornisce l'intervallo di testo che rappresenta la destinazione di un collegamento in un documento.



| Attributo | Identificatore                                                                   |
|-----------|------------------------------------------------------------------------------|
| **Collegamento**  | [**UIA \_ LinkAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a>Attributi del margine di pagina

I rettangoli di delimitazione di un intervallo di testo non espongono le coordinate del testo nella pagina. Tuttavia, un provider può esporre le informazioni sul margine della pagina usando gli attributi di testo seguenti.



| Attributo          | Identificatore                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| **MarginBottom**   | [**UIA \_ MarginBottomAttributeId**](uiauto-textattribute-ids.md)     |
| **MarginLeading**  | [**UIA \_ MarginLeadingAttributeId**](uiauto-textattribute-ids.md)   |
| **MarginTop**      | [**UIA \_ MarginTopAttributeId**](uiauto-textattribute-ids.md)           |
| **MarginTrailing** | [**UIA \_ MarginTrailingAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a>Attributi di allineamento del testo

Informazioni sull'allineamento del testo, ad esempio rientro, impostazioni di tabulazione e allineamento orizzontale, sono disponibili tramite gli attributi seguenti.



| Attributo                   | Identificatore                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| **HorizontalTextAlignment** | [**UIA \_ HorizontalTextAlignmentAttributeId**](uiauto-textattribute-ids.md) |
| **IndentationFirstLine**    | [**UIA \_ IndentationFirstLineAttributeId**](uiauto-textattribute-ids.md)       |
| **RientroLeading**      | [**UIA \_ IndentationLeadingAttributeId**](uiauto-textattribute-ids.md)           |
| **RientroTrailing**     | [**UIA \_ IndentationTrailingAttributeId**](uiauto-textattribute-ids.md)         |
| **Schede**                    | [**Schede dell'interfaccia \_ utenteAAttributeId**](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a>Attributi di colore del testo

I colori del testo in primo piano e di sfondo sono disponibili tramite gli attributi di testo seguenti. Entrambi i colori vengono specificati come [**tipo di dati COLORREF.**](/windows/desktop/gdi/colorref)



| Attributo           | Identificatore                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| **BackgroundColor** | [**UIA \_ BackgroundColorAttributeId**](uiauto-textattribute-ids.md) |
| **ForegroundColor** | [**UIA \_ ForegroundColorAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a>Attributi di decorazione del testo

Le decorazione di testo includono aree come elenchi puntati, sottolineatura e animazioni. Se il testo include punti elenco o numeri iniziali, il simbolo o il testo usato per il punto elenco o il numero deve essere incluso nel flusso di testo, se applicabile.

Le informazioni sulle decorazione di testo sono disponibili tramite gli attributi seguenti.



| Attributo              | Identificatore                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **AnimationStyle**     | [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md)         |
| **Bulletstyle**        | [**UIA \_ BulletStyleAttributeId**](uiauto-textattribute-ids.md)               |
| **OutlineStyles**      | [**UIA \_ OutlineStylesAttributeId**](uiauto-textattribute-ids.md)           |
| **OverlineColor**      | [**UIA \_ OverlineColorAttributeId**](uiauto-textattribute-ids.md)           |
| **OverlineStyle**      | [**UIA \_ OverlineStyleAttributeId**](uiauto-textattribute-ids.md)           |
| **StrikethroughColor** | [**UIA \_ StrikethroughColorAttributeId**](uiauto-textattribute-ids.md) |
| **StrikethroughStyle** | [**UIA \_ StrikethroughStyleAttributeId**](uiauto-textattribute-ids.md) |
| **UnderlineColor**     | [**UIA \_ UnderlineColorAttributeId**](uiauto-textattribute-ids.md)         |
| **UnderlineStyle**     | [**UIA \_ UnderlineStyleAttributeId**](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a>Attributi di stile del testo

Le informazioni sugli stili di testo sono disponibili anche con gli attributi seguenti.



| Attributo         | Identificatore                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| **CapStyle**      | [**UIA \_ CapStyleAttributeId**](uiauto-textattribute-ids.md)           |
| **IsHidden**      | [**UIA \_ IsHiddenAttributeId**](uiauto-textattribute-ids.md)           |
| **IsItalic**      | [**UIA \_ IsItalicAttributeId**](uiauto-textattribute-ids.md)           |
| **IsReadOnly**    | [**UIA \_ IsReadOnlyAttributeId**](uiauto-textattribute-ids.md)       |
| **IsSuperscript** | [**UIA \_ IsSuperscriptAttributeId**](uiauto-textattribute-ids.md) |
| **IsSubscript**   | [**UIA \_ IsSubscriptAttributeId**](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a>Attributi di interazione e selezione

Le informazioni sulla selezione del testo corrente nell'intervallo e nello stato attivo sono disponibili negli attributi seguenti.



| Attributo              | Identificatore                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| **IsActive**           | [**UIA \_ IsActiveAttributeId**](uiauto-textattribute-ids.md)           |
| **SelectionActiveEnd** | [**UIA \_ SelectionActiveEndAttributeId**](uiauto-textattribute-ids.md) |
| **CaretPosition**      | [**UIA \_ CaretPositionAttributeId**](uiauto-textattribute-ids.md)      |
| **CaretBidiMode**      | [**UIA \_ CaretBidiModeAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Informazioni sui pattern Automazione interfaccia utente di controllo Text e TextRange](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[Pattern di controllo Text e TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Uso di controlli basati su testo](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 