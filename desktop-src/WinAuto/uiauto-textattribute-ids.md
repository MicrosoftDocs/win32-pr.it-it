---
title: Identificatori di attributi di testo (UIAutomationClient. h)
description: Questo argomento descrive le costanti denominate usate per identificare gli attributi di testo di un intervallo di testo di automazione interfaccia utente Microsoft.
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
ms.openlocfilehash: 9b81c1829c36501b7c0ba4f3862dd9617acfea9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400558"
---
# <a name="text-attribute-identifiers"></a>Identificatori di attributi di testo

Questo argomento descrive le costanti denominate usate per identificare gli attributi di testo di un intervallo di testo di automazione interfaccia utente Microsoft. Queste costanti vengono usate con i metodi seguenti:

-   [**ITextRangeProvider:: FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
-   [**ITextRangeProvider:: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
-   [**IUIAutomationTextRange:: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
-   [**IUIAutomationTextRange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante/valore</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AfterParagraphSpacingAttributeId"></span><span id="uia_afterparagraphspacingattributeid"></span><span id="UIA_AFTERPARAGRAPHSPACINGATTRIBUTEID"></span><dl> <dt><strong>UIA_AfterParagraphSpacingAttributeId</strong></dt> <dt>40042</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>AfterParagraphSpacing</strong> , che specifica la dimensione della spaziatura dopo il paragrafo.<br/> Tipo Variant: <strong>VT_R8</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AnimationStyleAttributeId"></span><span id="uia_animationstyleattributeid"></span><span id="UIA_ANIMATIONSTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_AnimationStyleAttributeId</strong></dt> <dt>40000</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>AnimationStyle</strong> , che specifica il tipo di animazione applicato al testo. Questo attributo viene specificato come valore dal tipo enumerato <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"><strong>AnimationStyle</strong></a> . <br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"> <strong>AnimationStyle_None</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AnnotationObjectsAttributeId"></span><span id="uia_annotationobjectsattributeid"></span><span id="UIA_ANNOTATIONOBJECTSATTRIBUTEID"></span><dl> <dt><strong>UIA_AnnotationObjectsAttributeId</strong></dt> <dt>40032</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>AnnotationObjects</strong> , che gestisce una matrice di interfacce <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2"><strong>IUIAutomationElement2</strong></a> , una per ogni elemento nell'intervallo di testo corrente che implementa il pattern di controllo dell' <a href="uiauto-implementingannotation.md">annotazione</a> . Ogni elemento può inoltre implementare altri pattern di controllo in base alle esigenze per descrivere l'annotazione. Ad esempio, un'annotazione che è un commento supporta anche il pattern di controllo <a href="uiauto-implementingtextandtextrange.md">Text</a> . Supportato a partire da Windows 8.<br/> Tipo Variant: <strong>VT_UNKNOWN</strong><br/> Valore predefinito: matrice vuota <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AnnotationTypesAttributeId"></span><span id="uia_annotationtypesattributeid"></span><span id="UIA_ANNOTATIONTYPESATTRIBUTEID"></span><dl> <dt><strong>UIA_AnnotationTypesAttributeId</strong></dt> <dt>40031</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>AnnotationTypes</strong> , che mantiene un elenco di identificatori del tipo di annotazione per un intervallo di testo. Per un elenco di valori possibili, vedere <a href="uiauto-annotation-type-identifiers.md"><strong>identificatori del tipo di annotazione</strong></a>. Supportato a partire da Windows 8.<br/> Tipo Variant: <strong>VT_ARRAY</strong>  |  <strong>VT_I4</strong><br/> Valore predefinito: matrice vuota <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_BackgroundColorAttributeId"></span><span id="uia_backgroundcolorattributeid"></span><span id="UIA_BACKGROUNDCOLORATTRIBUTEID"></span><dl> <dt><strong>UIA_BackgroundColorAttributeId</strong></dt> <dt>40001</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>BackgroundColor</strong> , che specifica il colore di sfondo del testo. Questo attributo viene specificato come <a href="/windows/win32/gdi/colorref">COLORREF</a>; valore a 32 bit utilizzato per specificare un colore RGB o RGBA. <br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0 <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_BeforeParagraphSpacingAttributeId"></span><span id="uia_beforeparagraphspacingattributeid"></span><span id="UIA_BEFOREPARAGRAPHSPACINGATTRIBUTEID"></span><dl> <dt><strong>UIA_BeforeParagraphSpacingAttributeId</strong></dt> <dt>40041</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>BeforeParagraphSpacing</strong> , che specifica la dimensione della spaziatura prima del paragrafo.<br/> Tipo Variant: <strong>VT_R8</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_BulletStyleAttributeId"></span><span id="uia_bulletstyleattributeid"></span><span id="UIA_BULLETSTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_BulletStyleAttributeId</strong></dt> <dt>40002</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>BulletStyle</strong> , che specifica lo stile dei punti elenco utilizzati nell'intervallo di testo. Questo attributo viene specificato come valore dal tipo enumerato <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"><strong>BulletStyle</strong></a> .<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"> <strong>BulletStyle_None</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_CapStyleAttributeId"></span><span id="uia_capstyleattributeid"></span><span id="UIA_CAPSTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_CapStyleAttributeId</strong></dt> <dt>40003</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>CapStyle</strong> , che specifica lo stile delle maiuscole per il testo. Questo attributo viene specificato come valore dal tipo enumerato <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"><strong>CapStyle</strong></a> . <br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"> <strong>CapStyle_None</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_CaretBidiModeAttributeId"></span><span id="uia_caretbidimodeattributeid"></span><span id="UIA_CARETBIDIMODEATTRIBUTEID"></span><dl> <dt><strong>UIA_CaretBidiModeAttributeId</strong></dt> <dt>40039</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>CaretBidiMode</strong> , che indica la direzione del flusso di testo nell'intervallo di testo. Questo attributo viene specificato come valore dal tipo enumerato <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"><strong>CaretBidiMode</strong></a> . Supportato a partire da Windows 8.<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"> <strong>CaretBidiMode_LTR</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_CaretPositionAttributeId"></span><span id="uia_caretpositionattributeid"></span><span id="UIA_CARETPOSITIONATTRIBUTEID"></span><dl> <dt><strong>UIA_CaretPositionAttributeId</strong></dt> <dt>40038</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>CaretPosition</strong> , che indica se il punto di inserimento si trova all'inizio o alla fine di una riga di testo nell'intervallo di testo. Questo attributo viene specificato come valore dal tipo enumerato <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"><strong>CaretPosition</strong></a> . Supportato a partire da Windows 8.<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"> <strong>CaretPosition_Unknown</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_CultureAttributeId"></span><span id="uia_cultureattributeid"></span><span id="UIA_CULTUREATTRIBUTEID"></span><dl> <dt><strong>UIA_CultureAttributeId</strong></dt> <dt>40004</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo delle <strong>impostazioni cultura</strong> , che specifica le impostazioni locali del testo in base all'identificatore delle impostazioni locali (LCID). <br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: impostazioni locali dell'interfaccia utente dell'applicazione<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FontNameAttributeId"></span><span id="uia_fontnameattributeid"></span><span id="UIA_FONTNAMEATTRIBUTEID"></span><dl> <dt><strong>UIA_FontNameAttributeId</strong></dt> <dt>40005</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>fontname</strong> , che specifica il nome del tipo di carattere. Esempi: &quot; Arial Black &quot; ; &quot; Arial Narrow &quot; . La stringa del nome del tipo di carattere non è localizzata. <br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FontSizeAttributeId"></span><span id="uia_fontsizeattributeid"></span><span id="UIA_FONTSIZEATTRIBUTEID"></span><dl> <dt><strong>UIA_FontSizeAttributeId</strong></dt> <dt>40006</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>FontSize</strong> , che specifica la dimensione in punti del tipo di carattere. <br/> Tipo Variant: <strong>VT_R8</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FontWeightAttributeId"></span><span id="uia_fontweightattributeid"></span><span id="UIA_FONTWEIGHTATTRIBUTEID"></span><dl> <dt><strong>UIA_FontWeightAttributeId</strong></dt> <dt>40007</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>FontWeight</strong> , che specifica il tratto relativo, lo spessore o il grassetto del tipo di carattere. L'attributo <strong>FontWeight</strong> viene modellato dopo il membro <strong>LFWEIGHT</strong> della struttura GDI <a href="/windows/win32/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> e gli standard correlati. i possibili valori sono i seguenti:
<ul>
<li>0 = <strong>DontCare</strong></li>
<li>100 = <strong>Thin</strong></li>
<li>200 = <strong>luce</strong> o <strong>Ultralight</strong></li>
<li>300 = <strong>chiaro</strong></li>
<li>400 = <strong>normale</strong> o <strong>normale</strong></li>
<li>500 = <strong>medio</strong></li>
<li>600 = <strong>SemiBold</strong></li>
<li>700 = <strong>grassetto</strong></li>
<li>800 = <strong>grassetto</strong> o <strong>Ultra-grassetto</strong></li>
<li>900 = <strong>elevato</strong> o <strong>nero</strong></li>
</ul>
<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ForegroundColorAttributeId"></span><span id="uia_foregroundcolorattributeid"></span><span id="UIA_FOREGROUNDCOLORATTRIBUTEID"></span><dl> <dt><strong>UIA_ForegroundColorAttributeId</strong></dt> <dt>40008</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>ForegroundColor</strong> , che specifica il colore di primo piano del testo. Questo attributo viene specificato come <a href="/windows/win32/gdi/colorref">COLORREF</a>, un valore a 32 bit utilizzato per specificare un colore RGB o RGBA. <br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_HorizontalTextAlignmentAttributeId"></span><span id="uia_horizontaltextalignmentattributeid"></span><span id="UIA_HORIZONTALTEXTALIGNMENTATTRIBUTEID"></span><dl> <dt><strong>UIA_HorizontalTextAlignmentAttributeId</strong></dt> <dt>40009</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>HorizontalTextAlignment</strong> , che specifica la modalità di allineamento orizzontale del testo. Questo attributo viene specificato come valore dal tipo enumerato <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"><strong>HorizontalTextAlignmentEnum</strong></a> . <br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"> <strong>HorizontalTextAlignment_Left</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IndentationFirstLineAttributeId"></span><span id="uia_indentationfirstlineattributeid"></span><span id="UIA_INDENTATIONFIRSTLINEATTRIBUTEID"></span><dl> <dt><strong>UIA_IndentationFirstLineAttributeId</strong></dt> <dt>40010</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>IndentationFirstLine</strong> , che specifica la distanza, in punti, per il rientro della prima riga di un paragrafo. <br/> Tipo Variant: <strong>VT_R8</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IndentationLeadingAttributeId"></span><span id="uia_indentationleadingattributeid"></span><span id="UIA_INDENTATIONLEADINGATTRIBUTEID"></span><dl> <dt><strong>UIA_IndentationLeadingAttributeId</strong></dt> <dt>40011</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>IndentationLeading</strong> , che specifica i rientri iniziali, in punti. <br/> Tipo Variant: <strong>VT_R8</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IndentationTrailingAttributeId"></span><span id="uia_indentationtrailingattributeid"></span><span id="UIA_INDENTATIONTRAILINGATTRIBUTEID"></span><dl> <dt><strong>UIA_IndentationTrailingAttributeId</strong></dt> <dt>40012</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>IndentationTrailing</strong> , che specifica il rientro finale, in punti. <br/> Tipo Variant: <strong>VT_R8</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsActiveAttributeId"></span><span id="uia_isactiveattributeid"></span><span id="UIA_ISACTIVEATTRIBUTEID"></span><dl> <dt><strong>UIA_IsActiveAttributeId</strong></dt> <dt>40036</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>inattivo</strong> , che indica se il controllo che contiene l'intervallo di testo ha lo stato attivo (<strong>true</strong>) o meno (<strong>false</strong>). Supportato a partire da Windows 8.<br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsHiddenAttributeId"></span><span id="uia_ishiddenattributeid"></span><span id="UIA_ISHIDDENATTRIBUTEID"></span><dl> <dt><strong>UIA_IsHiddenAttributeId</strong></dt> <dt>40013</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>nascosto</strong> , che indica se il testo è nascosto (<strong>true</strong>) o visibile (<strong>false</strong>). <br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsItalicAttributeId"></span><span id="uia_isitalicattributeid"></span><span id="UIA_ISITALICATTRIBUTEID"></span><dl> <dt><strong>UIA_IsItalicAttributeId</strong></dt> <dt>40014</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>Italic</strong> , che indica se il testo è in corsivo (<strong>true</strong>) o meno (<strong>false</strong>). <br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsReadOnlyAttributeId"></span><span id="uia_isreadonlyattributeid"></span><span id="UIA_ISREADONLYATTRIBUTEID"></span><dl> <dt><strong>UIA_IsReadOnlyAttributeId</strong></dt> <dt>40015</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>IsReadOnly</strong> , che indica se il testo è di sola lettura (<strong>true</strong>) o se può essere modificato (<strong>false</strong>). <br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsSubscriptAttributeId"></span><span id="uia_issubscriptattributeid"></span><span id="UIA_ISSUBSCRIPTATTRIBUTEID"></span><dl> <dt><strong>UIA_IsSubscriptAttributeId</strong></dt> <dt>40016</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>IsSubscript</strong> , che indica se il testo è pedice (<strong>true</strong>) o meno (<strong>false</strong>). <br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsSuperscriptAttributeId"></span><span id="uia_issuperscriptattributeid"></span><span id="UIA_ISSUPERSCRIPTATTRIBUTEID"></span><dl> <dt><strong>UIA_IsSuperscriptAttributeId</strong></dt> <dt>40017</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>IsSuperscript</strong> , che indica se il testo è pedice (<strong>true</strong>) o meno (<strong>false</strong>). <br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LineSpacingAttributeId"></span><span id="uia_linespacingattributeid"></span><span id="UIA_LINESPACINGATTRIBUTEID"></span><dl> <dt><strong>UIA_LineSpacingAttributeId</strong></dt> <dt>40040</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>LineSpacing</strong> , che specifica la spaziatura tra le righe di testo.<br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: &quot; LineSpacingAttributeDefault&quot;<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LinkAttributeId"></span><span id="uia_linkattributeid"></span><span id="UIA_LINKATTRIBUTEID"></span><dl> <dt><strong>UIA_LinkAttributeId</strong></dt> <dt>40035</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo del testo del <strong>collegamento</strong> , che contiene l'interfaccia <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange"><strong>IUIAutomationTextRange</strong></a> dell'intervallo di testo che è la destinazione di un collegamento interno in un documento. Supportato a partire da Windows 8.<br/> Tipo Variant: <strong>VT_UNKNOWN</strong><br/> Valore predefinito: <strong>null</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_MarginBottomAttributeId"></span><span id="uia_marginbottomattributeid"></span><span id="UIA_MARGINBOTTOMATTRIBUTEID"></span><dl> <dt><strong>UIA_MarginBottomAttributeId</strong></dt> <dt>40018</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>MarginBottom</strong> , che specifica la dimensione, in punti, del margine inferiore applicato alla pagina associata all'intervallo di testo. <br/> Tipo Variant: <strong>VT_R8</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_MarginLeadingAttributeId"></span><span id="uia_marginleadingattributeid"></span><span id="UIA_MARGINLEADINGATTRIBUTEID"></span><dl> <dt><strong>UIA_MarginLeadingAttributeId</strong></dt> <dt>40019</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>MarginLeading</strong> , che specifica la dimensione, in punti, del margine iniziali applicato alla pagina associata all'intervallo di testo. <br/> Tipo Variant: <strong>VT_R8</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_MarginTopAttributeId"></span><span id="uia_margintopattributeid"></span><span id="UIA_MARGINTOPATTRIBUTEID"></span><dl> <dt><strong>UIA_MarginTopAttributeId</strong></dt> <dt>40020</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>MarginTop</strong> , che specifica la dimensione, in punti, del margine superiore applicato alla pagina associata all'intervallo di testo. <br/> Tipo Variant: <strong>VT_R8</strong><br/> Valore Ddefault: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_MarginTrailingAttributeId"></span><span id="uia_margintrailingattributeid"></span><span id="UIA_MARGINTRAILINGATTRIBUTEID"></span><dl> <dt><strong>UIA_MarginTrailingAttributeId</strong></dt> <dt>40021</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>MarginTrailing</strong> , che specifica la dimensione, in punti, del margine finale applicato alla pagina associata all'intervallo di testo. <br/> Tipo Variant: <strong>VT_R8</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_OutlineStylesAttributeId"></span><span id="uia_outlinestylesattributeid"></span><span id="UIA_OUTLINESTYLESATTRIBUTEID"></span><dl> <dt><strong>UIA_OutlineStylesAttributeId</strong></dt> <dt>40022</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>OutlineStyles</strong> , che specifica lo stile del contorno del testo. Questo attributo viene specificato come valore dal tipo enumerato <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"><strong>OutlineStyles</strong></a> . <br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"> <strong>OutlineStyles_None</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_OverlineColorAttributeId"></span><span id="uia_overlinecolorattributeid"></span><span id="UIA_OVERLINECOLORATTRIBUTEID"></span><dl> <dt><strong>UIA_OverlineColorAttributeId</strong></dt> <dt>40023</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>OverlineColor</strong> , che specifica il colore dell'effetto del testo di overline. Questo attributo viene specificato come <a href="/windows/win32/gdi/colorref">COLORREF</a>, un valore a 32 bit utilizzato per specificare un colore RGB o RGBA. <br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_OverlineStyleAttributeId"></span><span id="uia_overlinestyleattributeid"></span><span id="UIA_OVERLINESTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_OverlineStyleAttributeId</strong></dt> <dt>40024</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>OverlineStyle</strong> , che specifica lo stile dell'effetto di testo di sovralineatura. Questo attributo viene specificato come valore dal tipo enumerato <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> . <br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_SelectionActiveEndAttributeId"></span><span id="uia_selectionactiveendattributeid"></span><span id="UIA_SELECTIONACTIVEENDATTRIBUTEID"></span><dl> <dt><strong>UIA_SelectionActiveEndAttributeId</strong></dt> <dt>40037</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>SelectionActiveEnd</strong> , che indica la posizione del punto di inserimento rispetto a un intervallo di testo che rappresenta il testo attualmente selezionato. Questo attributo viene specificato come valore dall'enumerazione <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"><strong>ActiveEnd</strong></a> . Supportato a partire da Windows 8.<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"> <strong>ActiveEnd_None</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_StrikethroughColorAttributeId"></span><span id="uia_strikethroughcolorattributeid"></span><span id="UIA_STRIKETHROUGHCOLORATTRIBUTEID"></span><dl> <dt><strong>UIA_StrikethroughColorAttributeId</strong></dt> <dt>40025</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>StrikethroughColor</strong> , che specifica il colore della decorazione del testo barrato. Questo attributo viene specificato come <a href="/windows/win32/gdi/colorref">COLORREF</a>, un valore a 32 bit utilizzato per specificare un colore RGB o RGBA. <br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_StrikethroughStyleAttributeId"></span><span id="uia_strikethroughstyleattributeid"></span><span id="UIA_STRIKETHROUGHSTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_StrikethroughStyleAttributeId</strong></dt> <dt>40026</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>StrikethroughStyle</strong> , che specifica lo stile della decorazione del testo barrato. Questo attributo viene specificato come valore dal tipo enumerato <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> . <br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_StyleIdAttributeId"></span><span id="uia_styleidattributeid"></span><span id="UIA_STYLEIDATTRIBUTEID"></span><dl> <dt><strong>UIA_StyleIdAttributeId</strong></dt> <dt>40034</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>StyleId</strong> , che indica gli stili di testo utilizzati per un intervallo di testo. Per un elenco di valori possibili, vedere <a href="uiauto-style-identifiers.md"><strong>identificatori di stile</strong></a>. Supportato a partire da Windows 8.<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0 <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_StyleNameAttributeId"></span><span id="uia_stylenameattributeid"></span><span id="UIA_STYLENAMEATTRIBUTEID"></span><dl> <dt><strong>UIA_StyleNameAttributeId</strong></dt> <dt>40033</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>styleName</strong> , che identifica il nome localizzato dello stile di testo in uso per un intervallo di testo. Supportato a partire da Windows 8.<br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_TabsAttributeId"></span><span id="uia_tabsattributeid"></span><span id="UIA_TABSATTRIBUTEID"></span><dl> <dt><strong>UIA_TabsAttributeId</strong></dt> <dt>40027</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo delle <strong>schede</strong> , ovvero una matrice che specifica le tabulazioni per l'intervallo di testo. Ogni elemento della matrice specifica una distanza, in punti, dal margine iniziali. <br/> Tipo Variant: <strong>VT_ARRAY | VT_R8</strong><br/> Valore predefinito: matrice vuota<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_TextFlowDirectionsAttributeId"></span><span id="uia_textflowdirectionsattributeid"></span><span id="UIA_TEXTFLOWDIRECTIONSATTRIBUTEID"></span><dl> <dt><strong>UIA_TextFlowDirectionsAttributeId</strong></dt> <dt>40028</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>TextFlowDirections</strong> , che specifica la direzione del flusso di testo. Questo attributo viene specificato come una combinazione di valori del tipo enumerato <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"><strong>FlowDirections</strong></a> . <br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"> <strong>FlowDirections_Default</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_UnderlineColorAttributeId"></span><span id="uia_underlinecolorattributeid"></span><span id="UIA_UNDERLINECOLORATTRIBUTEID"></span><dl> <dt><strong>UIA_UnderlineColorAttributeId</strong></dt> <dt>40029</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>UnderlineColor</strong> , che specifica il colore dell'effetto di testo sottolineato. Questo attributo viene specificato come <a href="/windows/win32/gdi/colorref">COLORREF</a>, un valore a 32 bit utilizzato per specificare un colore RGB o RGBA. <br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_UnderlineStyleAttributeId"></span><span id="uia_underlinestyleattributeid"></span><span id="UIA_UNDERLINESTYLEATTRIBUTEID"></span><dl> <dt><strong>UIA_UnderlineStyleAttributeId</strong></dt> <dt>40030</dt> </dl></td>
<td style="text-align: left;">Identifica l'attributo di testo <strong>UnderlineStyle</strong> , che specifica lo stile della decorazione del testo sottolineato. Questo attributo viene specificato come valore dal tipo enumerato <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> . <br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows XP \[ \| UWP\]<br/>                                              |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2003 \|\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>UIAutomationClient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**ITextRangeProvider:: FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
</dt> <dt>

[**ITextRangeProvider:: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
</dt> <dt>

[**IUIAutomation:: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
</dt> <dt>

[**IUIAutomation:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Supporto di automazione interfaccia utente per contenuto testuale](uiauto-ui-automation-textpattern-overview.md)
</dt> </dl>
