---
title: Identificatori di attributi di testo (UIAutomationClient.h)
description: In questo argomento vengono descritte le costanti denominate utilizzate per identificare gli attributi di testo di un intervallo di Automazione interfaccia utente Microsoft.
ms.assetid: 67d86817-6a3f-4047-88d9-34f33f52a563
topic_type:
- apiref
api_name:
- UIA_AfterParagraphSpacingAttributeId
- UIA_AnimationStyleAttributeId
- UIA_AnnotationObjectsAttributeId
- UIA_AnnotationTypesAttributeId
- UIA_BackgroundColorAttributeId
- UIA_BeforeParagraphSpacingAttributeId
- UIA_BulletStyleAttributeId
- UIA_CapStyleAttributeId
- UIA_CaretBidiModeAttributeId
- UIA_CaretPositionAttributeId
- UIA_CultureAttributeId
- UIA_FontNameAttributeId
- UIA_FontSizeAttributeId
- UIA_FontWeightAttributeId
- UIA_ForegroundColorAttributeId
- UIA_HorizontalTextAlignmentAttributeId
- UIA_IndentationFirstLineAttributeId
- UIA_IndentationLeadingAttributeId
- UIA_IndentationTrailingAttributeId
- UIA_IsActiveAttributeId
- UIA_IsHiddenAttributeId
- UIA_IsItalicAttributeId
- UIA_IsReadOnlyAttributeId
- UIA_IsSubscriptAttributeId
- UIA_IsSuperscriptAttributeId
- UIA_LineSpacingAttributeId
- UIA_LinkAttributeId
- UIA_MarginBottomAttributeId
- UIA_MarginLeadingAttributeId
- UIA_MarginTopAttributeId
- UIA_MarginTrailingAttributeId
- UIA_OutlineStylesAttributeId
- UIA_OverlineColorAttributeId
- UIA_OverlineStyleAttributeId
- UIA_SelectionActiveEndAttributeId
- UIA_StrikethroughColorAttributeId
- UIA_StrikethroughStyleAttributeId
- UIA_StyleIdAttributeId
- UIA_StyleNameAttributeId
- UIA_TabsAttributeId
- UIA_TextFlowDirectionsAttributeId
- UIA_UnderlineColorAttributeId
- UIA_UnderlineStyleAttributeId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e84ba97b387097233b7a838fbe192585b9676b6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468768"
---
# <a name="text-attribute-identifiers"></a>Identificatori di attributi di testo

In questo argomento vengono descritte le costanti denominate utilizzate per identificare gli attributi di testo di un intervallo di Automazione interfaccia utente Microsoft. Queste costanti vengono usate con i metodi seguenti:

-   [**ITextRangeProvider::FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
-   [**ITextRangeProvider::GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
-   [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
-   [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)




| Costante/valore | Descrizione | 
|----------------|-------------|
| <span id="UIA_AfterParagraphSpacingAttributeId"></span><span id="uia_afterparagraphspacingattributeid"></span><span id="UIA_AFTERPARAGRAPHSPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_AfterParagraphSpacingAttributeId</strong></dt><dt>40042</dt></dl> | Identifica <strong>l'attributo di testo AfterParagraphSpacing,</strong> che specifica le dimensioni della spaziatura dopo il paragrafo.<br /> Tipo variant: <strong>VT_R8</strong><br /> Valore predefinito: 0<br /> | 
| <span id="UIA_AnimationStyleAttributeId"></span><span id="uia_animationstyleattributeid"></span><span id="UIA_ANIMATIONSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_AnimationStyleAttributeId</strong></dt><dt>40000</dt></dl> | Identifica <strong>l'attributo di testo AnimationStyle,</strong> che specifica il tipo di animazione applicata al testo. Questo attributo viene specificato come valore dal tipo <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"><strong>enumerato AnimationStyle.</strong></a> <br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"> <strong>AnimationStyle_None</strong></a><br /> | 
| <span id="UIA_AnnotationObjectsAttributeId"></span><span id="uia_annotationobjectsattributeid"></span><span id="UIA_ANNOTATIONOBJECTSATTRIBUTEID"></span><dl><dt><strong>UIA_AnnotationObjectsAttributeId</strong></dt><dt>40032</dt></dl> | Identifica l'attributo di testo <strong>AnnotationObjects,</strong> che gestisce una matrice di interfacce <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2"><strong>IUIAutomationElement2,</strong></a> una per ogni elemento nell'intervallo di testo corrente che implementa il pattern di controllo <a href="uiauto-implementingannotation.md">Annotation.</a> Ogni elemento può anche implementare altri pattern di controllo in base alle esigenze per descrivere l'annotazione. Ad esempio, un'annotazione che è un commento supporterebbe anche il pattern <a href="uiauto-implementingtextandtextrange.md">di controllo</a> Text. Supportato a partire da Windows 8.<br /> Tipo variant: <strong>VT_UNKNOWN</strong><br /> Valore predefinito: matrice vuota <br /> | 
| <span id="UIA_AnnotationTypesAttributeId"></span><span id="uia_annotationtypesattributeid"></span><span id="UIA_ANNOTATIONTYPESATTRIBUTEID"></span><dl><dt><strong>UIA_AnnotationTypesAttributeId</strong></dt><dt>40031</dt></dl> | Identifica <strong>l'attributo di testo AnnotationTypes,</strong> che gestisce un elenco di identificatori del tipo di annotazione per un intervallo di testo. Per un elenco dei valori possibili, vedere <a href="uiauto-annotation-type-identifiers.md"><strong>Identificatori dei tipi di annotazione.</strong></a> Supportato a partire da Windows 8.<br /> Tipo variant: <strong>VT_ARRAY</strong> | <strong>VT_I4</strong><br /> Valore predefinito: matrice vuota <br /> | 
| <span id="UIA_BackgroundColorAttributeId"></span><span id="uia_backgroundcolorattributeid"></span><span id="UIA_BACKGROUNDCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_BackgroundColorAttributeId</strong></dt><dt>40001</dt></dl> | Identifica <strong>l'attributo</strong> di testo BackgroundColor, che specifica il colore di sfondo del testo. Questo attributo viene specificato come <a href="/windows/win32/gdi/colorref">COLORREF</a>; Valore a 32 bit usato per specificare un colore RGB o RGBA. <br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: 0 <br /> | 
| <span id="UIA_BeforeParagraphSpacingAttributeId"></span><span id="uia_beforeparagraphspacingattributeid"></span><span id="UIA_BEFOREPARAGRAPHSPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_BeforeParagraphSpacingAttributeId</strong></dt><dt>40041</dt></dl> | Identifica <strong>l'attributo di testo BeforeParagraphSpacing,</strong> che specifica le dimensioni della spaziatura prima del paragrafo.<br /> Tipo variant: <strong>VT_R8</strong><br /> Valore predefinito: 0<br /> | 
| <span id="UIA_BulletStyleAttributeId"></span><span id="uia_bulletstyleattributeid"></span><span id="UIA_BULLETSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_BulletStyleAttributeId</strong></dt><dt>40002</dt></dl> | Identifica <strong>l'attributo di testo BulletStyle,</strong> che specifica lo stile dei punti elenco utilizzati nell'intervallo di testo. Questo attributo viene specificato come valore dal tipo <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"><strong>enumerato BulletStyle.</strong></a><br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"> <strong>BulletStyle_None</strong></a><br /> | 
| <span id="UIA_CapStyleAttributeId"></span><span id="uia_capstyleattributeid"></span><span id="UIA_CAPSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_CapStyleAttributeId</strong></dt><dt>40003</dt></dl> | Identifica l'attributo di testo <strong>CapStyle,</strong> che specifica lo stile di maiuscole e minuscole per il testo. Questo attributo viene specificato come valore dal <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"><strong>tipo enumerato CapStyle.</strong></a> <br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"> <strong>CapStyle_None</strong></a><br /> | 
| <span id="UIA_CaretBidiModeAttributeId"></span><span id="uia_caretbidimodeattributeid"></span><span id="UIA_CARETBIDIMODEATTRIBUTEID"></span><dl><dt><strong>UIA_CaretBidiModeAttributeId</strong></dt><dt>40039</dt></dl> | Identifica <strong>l'attributo di testo CaretBidiMode,</strong> che indica la direzione del flusso di testo nell'intervallo di testo. Questo attributo viene specificato come valore dal <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"><strong>tipo enumerato CaretBidiMode.</strong></a> Supportato a partire da Windows 8.<br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"> <strong>CaretBidiMode_LTR</strong></a><br /> | 
| <span id="UIA_CaretPositionAttributeId"></span><span id="uia_caretpositionattributeid"></span><span id="UIA_CARETPOSITIONATTRIBUTEID"></span><dl><dt><strong>UIA_CaretPositionAttributeId</strong></dt><dt>40038</dt></dl> | Identifica <strong>l'attributo di testo CaretPosition,</strong> che indica se il punto di interruzione si trova all'inizio o alla fine di una riga di testo nell'intervallo di testo. Questo attributo viene specificato come valore dal <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"><strong>tipo enumerato CaretPosition.</strong></a> Supportato a partire da Windows 8.<br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"> <strong>CaretPosition_Unknown</strong></a><br /> | 
| <span id="UIA_CultureAttributeId"></span><span id="uia_cultureattributeid"></span><span id="UIA_CULTUREATTRIBUTEID"></span><dl><dt><strong>UIA_CultureAttributeId</strong></dt><dt>40004</dt></dl> | Identifica <strong>l'attributo di</strong> testo Culture, che specifica le impostazioni locali del testo in base all'identificatore delle impostazioni locali (LCID). <br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: impostazioni locali dell'interfaccia utente dell'applicazione<br /> | 
| <span id="UIA_FontNameAttributeId"></span><span id="uia_fontnameattributeid"></span><span id="UIA_FONTNAMEATTRIBUTEID"></span><dl><dt><strong>UIA_FontNameAttributeId</strong></dt><dt>40005</dt></dl> | Identifica <strong>l'attributo di testo FontName,</strong> che specifica il nome del tipo di carattere. Esempi: "Arial Black"; "Arial Narrow". La stringa del nome del tipo di carattere non è localizzata. <br /> Tipo variant: <strong>VT_BSTR</strong><br /> Valore predefinito: stringa vuota<br /> | 
| <span id="UIA_FontSizeAttributeId"></span><span id="uia_fontsizeattributeid"></span><span id="UIA_FONTSIZEATTRIBUTEID"></span><dl><dt><strong>UIA_FontSizeAttributeId</strong></dt><dt>40006</dt></dl> | Identifica <strong>l'attributo di testo FontSize,</strong> che specifica le dimensioni in punti del tipo di carattere. <br /> Tipo variant: <strong>VT_R8</strong><br /> Valore predefinito: 0<br /> | 
| <span id="UIA_FontWeightAttributeId"></span><span id="uia_fontweightattributeid"></span><span id="UIA_FONTWEIGHTATTRIBUTEID"></span><dl><dt><strong>UIA_FontWeightAttributeId</strong></dt><dt>40007</dt></dl> | Identifica <strong>l'attributo di testo FontWeight,</strong> che specifica il tratto relativo, lo spessore o il grassetto del tipo di carattere. <strong>L'attributo FontWeight</strong> è modellato in base al membro <strong>lfWeight</strong> della struttura GDI <a href="/windows/win32/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> e agli standard correlati e può essere uno dei valori seguenti:<ul><li>0 = <strong>DontCare</strong></li><li>100 = <strong>Thin</strong></li><li>200 = <strong>ExtraLight</strong> o <strong>UltraLight</strong></li><li>300 = <strong>Chiaro</strong></li><li>400 = <strong>Normale</strong> o <strong>Normale</strong></li><li>500 = <strong>Media</strong></li><li>600 = <strong>SemiBold</strong></li><li>700 = <strong>Grassetto</strong></li><li>800 = <strong>ExtraBold</strong> <strong>o UltraBold</strong></li><li>900 = <strong>Heavy</strong> o <strong>Black</strong></li></ul><br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: 0<br /> | 
| <span id="UIA_ForegroundColorAttributeId"></span><span id="uia_foregroundcolorattributeid"></span><span id="UIA_FOREGROUNDCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_ForegroundColorAttributeId</strong></dt><dt>40008</dt></dl> | Identifica <strong>l'attributo</strong> di testo ForegroundColor, che specifica il colore di primo piano del testo. Questo attributo viene specificato come <a href="/windows/win32/gdi/colorref">COLORREF,</a>un valore a 32 bit usato per specificare un colore RGB o RGBA. <br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: 0<br /> | 
| <span id="UIA_HorizontalTextAlignmentAttributeId"></span><span id="uia_horizontaltextalignmentattributeid"></span><span id="UIA_HORIZONTALTEXTALIGNMENTATTRIBUTEID"></span><dl><dt><strong>UIA_HorizontalTextAlignmentAttributeId</strong></dt><dt>40009</dt></dl> | Identifica <strong>l'attributo di testo HorizontalTextAlignment,</strong> che specifica la modalità di allineamento orizzontale del testo. Questo attributo viene specificato come valore dal <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"><strong>tipo enumerato HorizontalTextAlignmentEnum.</strong></a> <br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"> <strong>HorizontalTextAlignment_Left</strong></a><br /> | 
| <span id="UIA_IndentationFirstLineAttributeId"></span><span id="uia_indentationfirstlineattributeid"></span><span id="UIA_INDENTATIONFIRSTLINEATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationFirstLineAttributeId</strong></dt><dt>40010</dt></dl> | Identifica <strong>l'attributo di testo IndentationFirstLine,</strong> che specifica la distanza, in punti, per il rientro della prima riga di un paragrafo. <br /> Tipo variant: <strong>VT_R8</strong><br /> Valore predefinito: 0<br /> | 
| <span id="UIA_IndentationLeadingAttributeId"></span><span id="uia_indentationleadingattributeid"></span><span id="UIA_INDENTATIONLEADINGATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationLeadingAttributeId</strong></dt><dt>40011</dt></dl> | Identifica <strong>l'attributo di testo IndentationLeading,</strong> che specifica il rientro iniziale, in punti. <br /> Tipo variant: <strong>VT_R8</strong><br /> Valore predefinito: 0<br /> | 
| <span id="UIA_IndentationTrailingAttributeId"></span><span id="uia_indentationtrailingattributeid"></span><span id="UIA_INDENTATIONTRAILINGATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationTrailingAttributeId</strong></dt><dt>40012</dt></dl> | Identifica <strong>l'attributo di testo IndentationTrailing,</strong> che specifica il rientro finale, in punti. <br /> Tipo variant: <strong>VT_R8</strong><br /> Valore predefinito: 0<br /> | 
| <span id="UIA_IsActiveAttributeId"></span><span id="uia_isactiveattributeid"></span><span id="UIA_ISACTIVEATTRIBUTEID"></span><dl><dt><strong>UIA_IsActiveAttributeId</strong></dt><dt>40036</dt></dl> | Identifica <strong>l'attributo di testo IsActive,</strong> che indica se il controllo che contiene l'intervallo di testo ha lo stato attivo della tastiera<strong>(TRUE)</strong>o meno<strong>(FALSE).</strong> Supportato a partire da Windows 8.<br /> Tipo variant: <strong>VT_BOOL</strong><br /> Valore predefinito: <strong>FALSE</strong><br /> | 
| <span id="UIA_IsHiddenAttributeId"></span><span id="uia_ishiddenattributeid"></span><span id="UIA_ISHIDDENATTRIBUTEID"></span><dl><dt><strong>UIA_IsHiddenAttributeId</strong></dt><dt>40013</dt></dl> | Identifica <strong>l'attributo di testo IsHidden,</strong> che indica se il testo è nascosto<strong>(TRUE)</strong>o visibile<strong>(FALSE).</strong> <br /> Tipo variant: <strong>VT_BOOL</strong><br /> Valore predefinito: <strong>FALSE</strong><br /> | 
| <span id="UIA_IsItalicAttributeId"></span><span id="uia_isitalicattributeid"></span><span id="UIA_ISITALICATTRIBUTEID"></span><dl><dt><strong>UIA_IsItalicAttributeId</strong></dt><dt>40014</dt></dl> | Identifica <strong>l'attributo di testo IsItalic,</strong> che indica se il testo è in corsivo (<strong>TRUE</strong>) o meno<strong>(FALSE).</strong> <br /> Tipo variant: <strong>VT_BOOL</strong><br /> Valore predefinito: <strong>FALSE</strong><br /> | 
| <span id="UIA_IsReadOnlyAttributeId"></span><span id="uia_isreadonlyattributeid"></span><span id="UIA_ISREADONLYATTRIBUTEID"></span><dl><dt><strong>UIA_IsReadOnlyAttributeId</strong></dt><dt>40015</dt></dl> | Identifica <strong>l'attributo di testo IsReadOnly,</strong> che indica se il testo è di sola lettura<strong>(TRUE)</strong>o può essere modificato<strong>(FALSE).</strong> <br /> Tipo variant: <strong>VT_BOOL</strong><br /> Valore predefinito: <strong>FALSE</strong><br /> | 
| <span id="UIA_IsSubscriptAttributeId"></span><span id="uia_issubscriptattributeid"></span><span id="UIA_ISSUBSCRIPTATTRIBUTEID"></span><dl><dt><strong>UIA_IsSubscriptAttributeId</strong></dt><dt>40016</dt></dl> | Identifica <strong>l'attributo di testo IsSubscript,</strong> che indica se il testo è indice<strong>(TRUE)</strong>o meno<strong>(FALSE).</strong> <br /> Tipo variant: <strong>VT_BOOL</strong><br /> Valore predefinito: <strong>FALSE</strong><br /> | 
| <span id="UIA_IsSuperscriptAttributeId"></span><span id="uia_issuperscriptattributeid"></span><span id="UIA_ISSUPERSCRIPTATTRIBUTEID"></span><dl><dt><strong>UIA_IsSuperscriptAttributeId</strong></dt><dt>40017</dt></dl> | Identifica l'attributo di testo <strong>IsSuperscript,</strong> che indica se il testo è indice (<strong>TRUE</strong>) o meno<strong>(FALSE).</strong> <br /> Tipo variant: <strong>VT_BOOL</strong><br /> Valore predefinito: <strong>FALSE</strong><br /> | 
| <span id="UIA_LineSpacingAttributeId"></span><span id="uia_linespacingattributeid"></span><span id="UIA_LINESPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_LineSpacingAttributeId</strong></dt><dt>40040</dt></dl> | Identifica <strong>l'attributo di testo LineSpacing,</strong> che specifica la spaziatura tra le righe di testo.<br /> Tipo variant: <strong>VT_BSTR</strong><br /> Valore predefinito: "LineSpacingAttributeDefault"<br /> | 
| <span id="UIA_LinkAttributeId"></span><span id="uia_linkattributeid"></span><span id="UIA_LINKATTRIBUTEID"></span><dl><dt><strong>UIA_LinkAttributeId</strong></dt><dt>40035</dt></dl> | Identifica <strong>l'attributo</strong> di testo Link, che contiene <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange"><strong>l'interfaccia IUIAutomationTextRange</strong></a> dell'intervallo di testo che rappresenta la destinazione di un collegamento interno in un documento. Supportato a partire da Windows 8.<br /> Tipo variant: <strong>VT_UNKNOWN</strong><br /> Valore predefinito: <strong>NULL</strong><br /> | 
| <span id="UIA_MarginBottomAttributeId"></span><span id="uia_marginbottomattributeid"></span><span id="UIA_MARGINBOTTOMATTRIBUTEID"></span><dl><dt><strong>UIA_MarginBottomAttributeId</strong></dt><dt>40018</dt></dl> | Identifica l'attributo di testo <strong>MarginBottom,</strong> che specifica le dimensioni, in punti, del margine inferiore applicato alla pagina associata all'intervallo di testo. <br /> Tipo variant: <strong>VT_R8</strong><br /> Valore predefinito: 0<br /> | 
| <span id="UIA_MarginLeadingAttributeId"></span><span id="uia_marginleadingattributeid"></span><span id="UIA_MARGINLEADINGATTRIBUTEID"></span><dl><dt><strong>UIA_MarginLeadingAttributeId</strong></dt><dt>40019</dt></dl> | Identifica l'attributo di testo <strong>MarginLeading,</strong> che specifica le dimensioni, in punti, del margine iniziale applicato alla pagina associata all'intervallo di testo. <br /> Tipo variant: <strong>VT_R8</strong><br /> Valore predefinito: 0<br /> | 
| <span id="UIA_MarginTopAttributeId"></span><span id="uia_margintopattributeid"></span><span id="UIA_MARGINTOPATTRIBUTEID"></span><dl><dt><strong>UIA_MarginTopAttributeId</strong></dt><dt>40020</dt></dl> | Identifica <strong>l'attributo di testo MarginTop,</strong> che specifica le dimensioni, in punti, del margine superiore applicato alla pagina associata all'intervallo di testo. <br /> Tipo variant: <strong>VT_R8</strong><br /> Valore predefinito: 0<br /> | 
| <span id="UIA_MarginTrailingAttributeId"></span><span id="uia_margintrailingattributeid"></span><span id="UIA_MARGINTRAILINGATTRIBUTEID"></span><dl><dt><strong>UIA_MarginTrailingAttributeId</strong></dt><dt>40021</dt></dl> | Identifica l'attributo di testo <strong>MarginTrailing,</strong> che specifica le dimensioni, in punti, del margine finale applicato alla pagina associata all'intervallo di testo. <br /> Tipo variant: <strong>VT_R8</strong><br /> Valore predefinito: 0<br /> | 
| <span id="UIA_OutlineStylesAttributeId"></span><span id="uia_outlinestylesattributeid"></span><span id="UIA_OUTLINESTYLESATTRIBUTEID"></span><dl><dt><strong>UIA_OutlineStylesAttributeId</strong></dt><dt>40022</dt></dl> | Identifica <strong>l'attributo di testo OutlineStyles,</strong> che specifica lo stile della struttura del testo. Questo attributo viene specificato come valore dal <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"><strong>tipo enumerato OutlineStyles.</strong></a> <br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"> <strong>OutlineStyles_None</strong></a><br /> | 
| <span id="UIA_OverlineColorAttributeId"></span><span id="uia_overlinecolorattributeid"></span><span id="UIA_OVERLINECOLORATTRIBUTEID"></span><dl><dt><strong>UIA_OverlineColorAttributeId</strong></dt><dt>40023</dt></dl> | Identifica <strong>l'attributo di testo OverlineColor,</strong> che specifica il colore della decorazione di testo overline. Questo attributo viene specificato come <a href="/windows/win32/gdi/colorref">COLORREF,</a>un valore a 32 bit usato per specificare un colore RGB o RGBA. <br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: 0<br /> | 
| <span id="UIA_OverlineStyleAttributeId"></span><span id="uia_overlinestyleattributeid"></span><span id="UIA_OVERLINESTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_OverlineStyleAttributeId</strong></dt><dt>40024</dt></dl> | Identifica <strong>l'attributo di testo OverlineStyle,</strong> che specifica lo stile della decorazione di testo in linea. Questo attributo viene specificato come valore dal <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>tipo enumerato TextDecorationLineStyleEnum.</strong></a> <br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 
| <span id="UIA_SelectionActiveEndAttributeId"></span><span id="uia_selectionactiveendattributeid"></span><span id="UIA_SELECTIONACTIVEENDATTRIBUTEID"></span><dl><dt><strong>UIA_SelectionActiveEndAttributeId</strong></dt><dt>40037</dt></dl> | Identifica <strong>l'attributo di testo SelectionActiveEnd,</strong> che indica la posizione del punto di selezione rispetto a un intervallo di testo che rappresenta il testo attualmente selezionato. Questo attributo viene specificato come valore <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"><strong>dell'enumerazione ActiveEnd.</strong></a> Supportato a partire da Windows 8.<br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"> <strong>ActiveEnd_None</strong></a><br /> | 
| <span id="UIA_StrikethroughColorAttributeId"></span><span id="uia_strikethroughcolorattributeid"></span><span id="UIA_STRIKETHROUGHCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_StrikethroughColorAttributeId</strong></dt><dt>40025</dt></dl> | Identifica <strong>l'attributo di testo StrikethroughColor,</strong> che specifica il colore dell'effetto di testo barrato. Questo attributo viene specificato come <a href="/windows/win32/gdi/colorref">COLORREF,</a>un valore a 32 bit usato per specificare un colore RGB o RGBA. <br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: 0<br /> | 
| <span id="UIA_StrikethroughStyleAttributeId"></span><span id="uia_strikethroughstyleattributeid"></span><span id="UIA_STRIKETHROUGHSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_StrikethroughStyleAttributeId</strong></dt><dt>40026</dt></dl> | Identifica <strong>l'attributo di testo StrikethroughStyle,</strong> che specifica lo stile dell'effetto di testo barrato. Questo attributo viene specificato come valore dal <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>tipo enumerato TextDecorationLineStyleEnum.</strong></a> <br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 
| <span id="UIA_StyleIdAttributeId"></span><span id="uia_styleidattributeid"></span><span id="UIA_STYLEIDATTRIBUTEID"></span><dl><dt><strong>UIA_StyleIdAttributeId</strong></dt><dt>40034</dt></dl> | Identifica <strong>l'attributo</strong> di testo StyleId, che indica gli stili di testo in uso per un intervallo di testo. Per un elenco dei valori possibili, vedere <a href="uiauto-style-identifiers.md"><strong>Identificatori di stile.</strong></a> Supportato a partire da Windows 8.<br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: 0 <br /> | 
| <span id="UIA_StyleNameAttributeId"></span><span id="uia_stylenameattributeid"></span><span id="UIA_STYLENAMEATTRIBUTEID"></span><dl><dt><strong>UIA_StyleNameAttributeId</strong></dt><dt>40033</dt></dl> | Identifica <strong>l'attributo di testo StyleName,</strong> che identifica il nome localizzato dello stile di testo in uso per un intervallo di testo. Supportato a partire da Windows 8.<br /> Tipo variant: <strong>VT_BSTR</strong><br /> Valore predefinito: stringa vuota<br /> | 
| <span id="UIA_TabsAttributeId"></span><span id="uia_tabsattributeid"></span><span id="UIA_TABSATTRIBUTEID"></span><dl><dt><strong>UIA_TabsAttributeId</strong></dt><dt>40027</dt></dl> | Identifica <strong>l'attributo di</strong> testo Tabs, ovvero una matrice che specifica i tabulazioni per l'intervallo di testo. Ogni elemento della matrice specifica una distanza, in punti, dal margine iniziale. <br /> Tipo variant: <strong> VT_ARRAY | VT_R8</strong><br /> Valore predefinito: matrice vuota<br /> | 
| <span id="UIA_TextFlowDirectionsAttributeId"></span><span id="uia_textflowdirectionsattributeid"></span><span id="UIA_TEXTFLOWDIRECTIONSATTRIBUTEID"></span><dl><dt><strong>UIA_TextFlowDirectionsAttributeId</strong></dt><dt>40028</dt></dl> | Identifica <strong>l'attributo di testo TextFlowDirections,</strong> che specifica la direzione del flusso di testo. Questo attributo viene specificato come combinazione di valori del <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"><strong>tipo enumerato FlowDirections.</strong></a> <br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"> <strong>FlowDirections_Default</strong></a><br /> | 
| <span id="UIA_UnderlineColorAttributeId"></span><span id="uia_underlinecolorattributeid"></span><span id="UIA_UNDERLINECOLORATTRIBUTEID"></span><dl><dt><strong>UIA_UnderlineColorAttributeId</strong></dt><dt>40029</dt></dl> | Identifica <strong>l'attributo di testo UnderlineColor,</strong> che specifica il colore della decorazione del testo sottolineato. Questo attributo viene specificato come <a href="/windows/win32/gdi/colorref">COLORREF,</a>un valore a 32 bit usato per specificare un colore RGB o RGBA. <br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: 0<br /> | 
| <span id="UIA_UnderlineStyleAttributeId"></span><span id="uia_underlinestyleattributeid"></span><span id="UIA_UNDERLINESTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_UnderlineStyleAttributeId</strong></dt><dt>40030</dt></dl> | Identifica <strong>l'attributo di testo UnderlineStyle,</strong> che specifica lo stile della decorazione del testo sottolineato. Questo attributo viene specificato come valore dal <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>tipo enumerato TextDecorationLineStyleEnum.</strong></a> <br /> Tipo variant: <strong>VT_I4</strong><br /> Valore predefinito: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 




## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App \[ desktop XP per app \| UWP\]<br/>                                              |
| Server minimo supportato<br/> | Windows App desktop di Server 2003 \[ \| per app UWP\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>UIAutomationClient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**ITextRangeProvider::FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
</dt> <dt>

[**ITextRangeProvider::GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
</dt> <dt>

[**IUIAutomation::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
</dt> <dt>

[**IUIAutomation::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Automazione interfaccia utente supporto per contenuto testuale](uiauto-ui-automation-textpattern-overview.md)
</dt> </dl>
