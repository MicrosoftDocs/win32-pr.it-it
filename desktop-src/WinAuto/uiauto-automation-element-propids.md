---
title: Identificatori di proprietà degli elementi di automazione (UIAutomationClient. h)
description: Questo argomento descrive le costanti denominate che identificano le proprietà degli elementi di automazione interfaccia utente Microsoft.
ms.assetid: f7613ad1-0b75-46fb-b9ac-b1ae9eea4193
topic_type:
- apiref
api_name:
- UIA_AcceleratorKeyPropertyId
- UIA_AccessKeyPropertyId
- UIA_AnnotationObjectsPropertyId
- UIA_AnnotationTypesPropertyId
- UIA_AriaPropertiesPropertyId
- UIA_AriaRolePropertyId
- UIA_AutomationIdPropertyId
- UIA_BoundingRectanglePropertyId
- UIA_CenterPointPropertyId
- UIA_ClassNamePropertyId
- UIA_ClickablePointPropertyId
- UIA_ControllerForPropertyId
- UIA_ControlTypePropertyId
- UIA_CulturePropertyId
- UIA_DescribedByPropertyId
- UIA_FillColorPropertyId
- UIA_FillTypePropertyId
- UIA_FlowsFromPropertyId
- UIA_FlowsToPropertyId
- UIA_FrameworkIdPropertyId
- UIA_FullDescriptionPropertyId
- UIA_HasKeyboardFocusPropertyId
- UIA_HeadingLevelPropertyId
- UIA_HelpTextPropertyId
- UIA_IsContentElementPropertyId
- UIA_IsControlElementPropertyId
- UIA_IsDataValidForFormPropertyId
- UIA_IsEnabledPropertyId
- UIA_IsKeyboardFocusablePropertyId
- UIA_IsOffscreenPropertyId
- UIA_IsPasswordPropertyId
- UIA_IsPeripheralPropertyId
- UIA_IsRequiredForFormPropertyId
- UIA_ItemStatusPropertyId
- UIA_ItemTypePropertyId
- UIA_LabeledByPropertyId
- UIA_LandmarkTypePropertyId
- UIA_LevelPropertyId
- UIA_LiveSettingPropertyId
- UIA_LocalizedControlTypePropertyId
- UIA_LocalizedLandmarkTypePropertyId
- UIA_NamePropertyId
- UIA_NativeWindowHandlePropertyId
- UIA_OptimizeForVisualContentPropertyId
- UIA_OrientationPropertyId
- UIA_OutlineColorPropertyId
- UIA_OutlineThicknessPropertyId
- UIA_PositionInSetPropertyId
- UIA_ProcessIdPropertyId
- UIA_ProviderDescriptionPropertyId
- UIA_RotationPropertyId
- UIA_RuntimeIdPropertyId
- UIA_SizePropertyId
- UIA_SizeOfSetPropertyId
- UIA_VisualEffectsPropertyId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60c90b1a6d56fa62b6ddb241ce38c8cb2ae40afa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121178"
---
# <a name="automation-element-property-identifiers"></a>Identificatori delle proprietà degli elementi di automazione

Questo argomento descrive le costanti denominate che identificano le proprietà degli elementi di automazione interfaccia utente Microsoft.



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
<td style="text-align: left;"><span id="UIA_AcceleratorKeyPropertyId"></span><span id="uia_acceleratorkeypropertyid"></span><span id="UIA_ACCELERATORKEYPROPERTYID"></span><dl> <dt><strong>UIA_AcceleratorKeyPropertyId</strong></dt> <dt>30006</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>AcceleratorKey</strong> , che è una stringa contenente le combinazioni di tasti di scelta rapida (denominate anche tasti di scelta rapida) per l'elemento di automazione. <br/> Combinazioni di tasti di scelta rapida richiamare un'azione. Ad esempio, CTRL + O viene spesso usato per richiamare la finestra di dialogo Apri file comune. Un elemento di automazione con la proprietà <strong>AcceleratorKey</strong> può implementare il pattern di controllo <a href="uiauto-implementinginvoke.md">Invoke</a> per l'azione equivalente al comando di collegamento.<br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AccessKeyPropertyId"></span><span id="uia_accesskeypropertyid"></span><span id="UIA_ACCESSKEYPROPERTYID"></span><dl> <dt><strong>UIA_AccessKeyPropertyId</strong></dt> <dt>30007</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>AccessKey</strong> , che è una stringa contenente il carattere di chiave di accesso per l'elemento di automazione.<br/> Un tasto di scelta (talvolta denominato mnemonico) è un carattere nel testo di un menu, di una voce di menu o di un'etichetta di un controllo, ad esempio un pulsante, che attiva la funzione di menu associata. Ad esempio, per aprire il menu file, per cui la chiave di accesso è in genere F, l'utente preme ALT + F.<br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AnnotationObjectsPropertyId"></span><span id="uia_annotationobjectspropertyid"></span><span id="UIA_ANNOTATIONOBJECTSPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationObjectsPropertyId</strong></dt> <dt>30156</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>AnnotationObjects</strong> , che è un elenco di oggetti Annotation in un documento, ad esempio comment, header, piè di pagina e così via.<br/> Tipo Variant: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: matrice vuota<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AnnotationTypesPropertyId"></span><span id="uia_annotationtypespropertyid"></span><span id="UIA_ANNOTATIONTYPESPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationTypesPropertyId</strong></dt> <dt>30155</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>AnnotationTypes</strong> , che è un elenco dei tipi di annotazioni in un documento, ad esempio commento, intestazione, piè di pagina e così via.<br/> Tipo Variant: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: matrice vuota<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AriaPropertiesPropertyId"></span><span id="uia_ariapropertiespropertyid"></span><span id="UIA_ARIAPROPERTIESPROPERTYID"></span><dl> <dt><strong>UIA_AriaPropertiesPropertyId</strong></dt> <dt>30102</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>AriaProperties</strong> , ovvero una stringa formattata contenente le informazioni sulle proprietà dell'applicazione Internet (aria) accessibili per l'elemento di automazione. Per altre informazioni sul mapping degli Stati e delle proprietà di ARIA alle proprietà e alle funzioni di automazione interfaccia utente, vedere <a href="uiauto-ariaspecification.md">UI Automation per W3C Accessible Rich Internet Applications Specification</a>.<br/> <strong>AriaProperties</strong> è una raccolta di coppie nome/valore con delimitatori di <strong>=</strong> (uguale a) e <strong>;</strong> (punto e virgola), ad esempio, &quot; Checked = true; disabled = false &quot; . La <strong>\</strong> barra rovesciata viene usata come carattere di escape quando questi caratteri delimitatori o <strong>\</strong> vengono visualizzati nei valori. Per motivi di sicurezza e per altri motivi, l'implementazione del provider di questa proprietà può eseguire le operazioni necessarie per convalidare le proprietà ARIA originali. Tuttavia, non è obbligatorio.<br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_AriaRolePropertyId"></span><span id="uia_ariarolepropertyid"></span><span id="UIA_ARIAROLEPROPERTYID"></span><dl> <dt><strong>UIA_AriaRolePropertyId</strong></dt> <dt>30101</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>AriaRole</strong> , che è una stringa che contiene le informazioni sui ruoli aria (Rich Internet Application) accessibili per l'elemento di automazione. Per altre informazioni sul mapping dei ruoli ARIA ai tipi di controllo di automazione interfaccia utente, vedere <a href="uiauto-ariaspecification.md">UI Automation per W3C Accessible Rich Internet Applications Specification</a>.<br/>
<blockquote>
[!Note]<br />
In alternativa, l'agente utente può anche offrire una descrizione localizzata del ruolo del W3C ARIA nella proprietà <strong>LocalizedControlType</strong> . Quando la stringa localizzata non viene specificata, il sistema fornirà la stringa <strong>LocalizedControlType</strong> predefinita per l'elemento.
</blockquote>
<br/> <br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_AutomationIdPropertyId"></span><span id="uia_automationidpropertyid"></span><span id="UIA_AUTOMATIONIDPROPERTYID"></span><dl> <dt><strong>UIA_AutomationIdPropertyId</strong></dt> <dt>30011</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>AutomationId</strong> , che è una stringa che contiene l'identificatore (ID) di automazione interfaccia utente per l'elemento di automazione.<br/> Quando è disponibile, il <strong>AutomationId</strong> di un elemento deve essere lo stesso in qualsiasi istanza dell'applicazione, indipendentemente dalla lingua locale. Il valore deve essere univoco tra gli elementi di pari livello, ma non necessariamente univoco nell'intero desktop. Ad esempio, più istanze di un'applicazione o più visualizzazioni di cartelle in Microsoft Windows Explorer possono contenere elementi con la stessa proprietà <strong>AutomationId</strong> , ad esempio &quot; SystemMenuBar &quot; .<br/> Sebbene il supporto per <strong>AutomationId</strong> sia sempre consigliato per un migliore supporto dei test automatizzati, questa proprietà non è obbligatoria. Se è supportata, <strong>AutomationId</strong> è utile per la creazione di uno script di automazione di test che viene eseguito indipendentemente dalla lingua dell'interfaccia utente. I client non devono fare supposizioni sui valori <strong>AutomationId</strong> esposti da altre applicazioni. <strong>AutomationId</strong> non è garantito che sia stabile in versioni o Build diverse di un'applicazione.<br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_BoundingRectanglePropertyId"></span><span id="uia_boundingrectanglepropertyid"></span><span id="UIA_BOUNDINGRECTANGLEPROPERTYID"></span><dl> <dt><strong>UIA_BoundingRectanglePropertyId</strong></dt> <dt>30001</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>BoundingRectangle</strong> , che specifica le coordinate del rettangolo che racchiude completamente l'elemento di automazione. Il rettangolo è espresso in coordinate dello schermo fisico. Può contenere punti non selezionabili se la forma o l'area selezionabile dell'elemento dell'interfaccia utente è irregolare oppure se l'elemento è nascosto da altri elementi dell'interfaccia utente.<br/> Tipo Variant: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: [0, 0, 0, 0]<br/>
<blockquote>
[!Note]<br />
Questa proprietà è <strong>null</strong> se l'elemento non visualizza attualmente un'interfaccia utente.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_CenterPointPropertyId"></span><span id="uia_centerpointpropertyid"></span><span id="UIA_CENTERPOINTPROPERTYID"></span><dl> <dt><strong>UIA_CenterPointPropertyId</strong></dt> <dt>30165</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>Centerpoint</strong> , che specifica le coordinate del punto X e Y del centro dell'elemento di automazione. Lo spazio delle coordinate è quello che il provider considera logicamente una pagina.<br/> Tipo Variant: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ClassNamePropertyId"></span><span id="uia_classnamepropertyid"></span><span id="UIA_CLASSNAMEPROPERTYID"></span><dl> <dt><strong>UIA_ClassNamePropertyId</strong></dt> <dt>30012</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>ClassName</strong> , che è una stringa contenente il nome della classe per l'elemento di automazione come assegnato dallo sviluppatore del controllo.<br/> Il nome della classe dipende dall'implementazione del provider di automazione interfaccia utente e pertanto non è sempre in un formato standard. Tuttavia, se il nome della classe è noto, può essere utilizzato per verificare che un'applicazione stia utilizzando l'elemento di automazione previsto.<br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ClickablePointPropertyId"></span><span id="uia_clickablepointpropertyid"></span><span id="UIA_CLICKABLEPOINTPROPERTYID"></span><dl> <dt><strong>UIA_ClickablePointPropertyId</strong></dt> <dt>30014</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>ClickablePoint</strong> , che è un punto sull'elemento di automazione su cui è possibile fare clic. Non è possibile fare clic su un elemento se è completamente o parzialmente nascosto da un'altra finestra.<br/> Tipo Variant: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ControllerForPropertyId"></span><span id="uia_controllerforpropertyid"></span><span id="UIA_CONTROLLERFORPROPERTYID"></span><dl> <dt><strong>UIA_ControllerForPropertyId</strong></dt> <dt>30104</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>ControllerFor</strong> , che è una matrice di elementi di automazione che vengono modificati dall'elemento di automazione che supporta questa proprietà.<br/> <strong>ControllerFor</strong> viene usato quando un elemento di automazione interessa uno o più segmenti dell'interfaccia utente dell'applicazione o del desktop; in caso contrario, è difficile associare l'effetto dell'operazione di controllo agli elementi dell'interfaccia utente.<br/> Questo identificatore viene comunemente usato per l' <a href="/windows/uwp/design/accessibility/accessible-text-requirements">accessibilità automatica dei suggerimenti</a>.<br/> Tipo Variant per i provider: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo Variant per i client: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a> )<br/> Valore predefinito: matrice vuota<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ControlTypePropertyId"></span><span id="uia_controltypepropertyid"></span><span id="UIA_CONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ControlTypePropertyId</strong></dt> <dt>30003</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>ControlType</strong> , che è una classe che identifica il tipo dell'elemento di automazione. <strong>ControlType</strong> definisce le caratteristiche degli elementi dell'interfaccia utente dalle primitive di controllo dell'interfaccia utente note, ad esempio il pulsante o la casella di controllo. <br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: <a href="uiauto-controltype-ids.md"> <strong>UIA_CustomControlTypeId</strong></a><br/>
<blockquote>
[!Note]<br />
Usare il valore predefinito solo se l'elemento di automazione rappresenta un tipo completamente nuovo di controllo.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_CulturePropertyId"></span><span id="uia_culturepropertyid"></span><span id="UIA_CULTUREPROPERTYID"></span><dl> <dt><strong>UIA_CulturePropertyId</strong></dt> <dt>30015</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà delle <strong>impostazioni cultura</strong> , che contiene un identificatore delle impostazioni locali per l'elemento di automazione (ad esempio, <code>0x0409</code> per &quot; en-US &quot; o inglese (Stati Uniti)).<br/> Ogni impostazioni locali dispone di un identificatore univoco, un valore a 32 bit costituito da un identificatore di lingua e un identificatore di ordinamento. L'identificatore delle impostazioni locali è un'abbreviazione numerica internazionale standard e include i componenti necessari per identificare in modo univoco una delle impostazioni locali definite dal sistema operativo installate. Per altre informazioni, vedere <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">costanti e stringhe degli identificatori di lingua</a>.<br/> Questa proprietà può esistere in base al controllo, ma in genere è disponibile solo a livello di applicazione.<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_DescribedByPropertyId"></span><span id="uia_describedbypropertyid"></span><span id="UIA_DESCRIBEDBYPROPERTYID"></span><dl> <dt><strong>UIA_DescribedByPropertyId</strong></dt> <dt>30105</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>DescribedBy</strong> , che è una matrice di elementi che forniscono ulteriori informazioni sull'elemento di automazione.<br/> <strong>DescribedBy</strong> viene usato quando un elemento di automazione viene spiegato da un altro segmento dell'interfaccia utente dell'applicazione. Ad esempio, la proprietà può puntare a un elemento di testo di &quot; 2.529 elementi in 85 gruppi, 10 elementi selezionati &quot; da un oggetto elenco personalizzato complesso. Invece di usare il modello a oggetti per i client per il digest di informazioni simili, la proprietà <strong>DescribedBy</strong> può offrire accesso rapido all'elemento dell'interfaccia utente che può già offrire informazioni utili sull'utente finale che descrivono l'elemento dell'interfaccia utente.<br/> Tipo Variant per i provider: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo Variant per i client: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valore predefinito: matrice vuota<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FillColorPropertyId"></span><span id="uia_fillcolorpropertyid"></span><span id="UIA_FILLCOLORPROPERTYID"></span><dl> <dt><strong>UIA_FillColorPropertyId</strong></dt> <dt>30160</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>FillColor</strong> , che specifica il colore utilizzato per riempire l'elemento di automazione. Questo attributo viene specificato come COLORREF, un valore a 32 bit utilizzato per specificare un colore RGB o RGBA.<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FillTypePropertyId"></span><span id="uia_filltypepropertyid"></span><span id="UIA_FILLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_FillTypePropertyId</strong></dt> <dt>30162</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>elemento FillType</strong> , che specifica il modello utilizzato per riempire l'elemento di automazione, ad esempio None, color, Gradient, Picture, pattern e così via.<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FlowsFromPropertyId"></span><span id="uia_flowsfrompropertyid"></span><span id="UIA_FLOWSFROMPROPERTYID"></span><dl> <dt><strong>UIA_FlowsFromPropertyId</strong></dt> <dt>30148</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>FlowsFrom</strong> , che è una matrice di elementi di automazione che suggerisce l'ordine di lettura prima dell'elemento di automazione corrente. Supportato a partire da Windows 8.<br/> La proprietà <strong>FlowsFrom</strong> specifica l'ordine di lettura quando gli elementi di automazione non sono esposti o strutturati nello stesso ordine di lettura percepito dall'utente. Sebbene la proprietà <strong>FlowsFrom</strong> possa specificare più elementi precedenti, in genere contiene solo l'elemento precedente nell'ordine di lettura.<br/> Tipo Variant per i provider: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo Variant per i client: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valore predefinito: matrice vuota<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FlowsToPropertyId"></span><span id="uia_flowstopropertyid"></span><span id="UIA_FLOWSTOPROPERTYID"></span><dl> <dt><strong>UIA_FlowsToPropertyId</strong></dt> <dt>30106</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>FlowsTo</strong> , che è una matrice di elementi di automazione che suggerisce l'ordine di lettura dopo l'elemento di automazione corrente.<br/> La proprietà <strong>FlowsTo</strong> specifica l'ordine di lettura quando gli elementi di automazione non sono esposti o strutturati nello stesso ordine di lettura percepito dall'utente. Sebbene la proprietà <strong>FlowsTo</strong> possa specificare più elementi successivi, in genere contiene solo l'elemento successivo nell'ordine di lettura.<br/> Tipo Variant per i provider: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo Variant per i client: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valore predefinito: matrice vuota<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_FrameworkIdPropertyId"></span><span id="uia_frameworkidpropertyid"></span><span id="UIA_FRAMEWORKIDPROPERTYID"></span><dl> <dt><strong>UIA_FrameworkIdPropertyId</strong></dt> <dt>30024</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>FrameworkId</strong> , che è una stringa che contiene il nome del Framework dell'interfaccia utente sottostante a cui appartiene l'elemento di automazione.<br/> <strong>FrameworkId</strong> consente alle applicazioni client di elaborare gli elementi di automazione in modo diverso a seconda del Framework dell'interfaccia utente specifico. Esempi di valori di proprietà includono &quot; Win32 &quot; , &quot; WinForm &quot; e &quot; directui &quot; .<br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_FullDescriptionPropertyId"></span><span id="uia_fulldescriptionpropertyid"></span><span id="UIA_FULLDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_FullDescriptionPropertyId</strong></dt> <dt>30159</dt> </dl></td>
<td style="text-align: left;">La proprietà <strong>FullDescription</strong> espone una stringa localizzata che può contenere testo descrittivo esteso per un elemento. <strong>FullDescription</strong> può contenere una descrizione più completa di un elemento che può essere appropriato per il <strong>nome</strong>dell'elemento.<br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_HasKeyboardFocusPropertyId"></span><span id="uia_haskeyboardfocuspropertyid"></span><span id="UIA_HASKEYBOARDFOCUSPROPERTYID"></span><dl> <dt><strong>UIA_HasKeyboardFocusPropertyId</strong></dt> <dt>30008</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>HasKeyboardFocus</strong> , che è un valore booleano che indica se l'elemento di automazione dispone dello stato attivo della tastiera.<br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_HeadingLevelPropertyId"></span><span id="uia_headinglevelpropertyid"></span><span id="UIA_HEADINGLEVELPROPERTYID"></span><dl> <dt><strong>UIA_HeadingLevelPropertyId</strong></dt> <dt>30173</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>HeadingLevel</strong> , che indica il livello di intestazione di un elemento di automazione interfaccia utente.<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: <strong>HeadingLevel_None</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_HelpTextPropertyId"></span><span id="uia_helptextpropertyid"></span><span id="UIA_HELPTEXTPROPERTYID"></span><dl> <dt><strong>UIA_HelpTextPropertyId</strong></dt> <dt>30013</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>HelpText</strong> , che è una stringa di testo della Guida associata all'elemento di automazione.<br/> La proprietà <strong>HelpText</strong> può essere supportata con testo segnaposto visualizzato nei controlli di modifica o di elenco. Ad esempio, &quot; digitare qui il testo per la ricerca &quot; è un buon candidato la proprietà <strong>HelpText</strong> per un controllo di modifica che inserisce il testo prima dell'input effettivo dell'utente. Tuttavia, non è adeguato per la proprietà Name del controllo di modifica.<br/> Quando <strong>HelpText</strong> è supportato, la stringa deve corrispondere alla lingua dell'interfaccia utente dell'applicazione o alla lingua dell'interfaccia utente predefinita del sistema operativo.<br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsContentElementPropertyId"></span><span id="uia_iscontentelementpropertyid"></span><span id="UIA_ISCONTENTELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsContentElementPropertyId</strong></dt> <dt>30017</dt> </dl></td>
<td style="text-align: left;">Identifica la <strong>Proprietà IsSynchronized</strong> , che è un valore booleano che specifica se l'elemento viene visualizzato nella visualizzazione contenuto della struttura ad albero dell'elemento di automazione. Per altre informazioni, vedere <a href="uiauto-treeoverview.md">Panoramica dell'albero di automazione interfaccia utente</a>.<br/>
<blockquote>
[!Note]<br />
Per visualizzare un elemento nella visualizzazione contenuto, sia la proprietà <strong>IsSynchronized che la</strong> <strong>Proprietà IsSynchronized devono</strong> essere <strong>true</strong>.
</blockquote>
<br/> <br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>true</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsControlElementPropertyId"></span><span id="uia_iscontrolelementpropertyid"></span><span id="UIA_ISCONTROLELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsControlElementPropertyId</strong></dt> <dt>30016</dt> </dl></td>
<td style="text-align: left;">Identifica la <strong>Proprietà IsSynchronized</strong> , che è un valore booleano che specifica se l'elemento viene visualizzato nella visualizzazione controlli dell'albero degli elementi di automazione. Per altre informazioni, vedere <a href="uiauto-treeoverview.md">Panoramica dell'albero di automazione interfaccia utente</a>.<br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>true</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsDataValidForFormPropertyId"></span><span id="uia_isdatavalidforformpropertyid"></span><span id="UIA_ISDATAVALIDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsDataValidForFormPropertyId</strong></dt> <dt>30103</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>IsDataValidForForm</strong> , che è un valore booleano che indica se il valore immesso o selezionato è valido per la regola del modulo associata all'elemento di automazione. Se, ad esempio, l'utente ha immesso &quot; 425-555-5555 &quot; per un campo di codice postale che richiede 5 o 9 cifre, la proprietà <strong>IsDataValidForForm</strong> può essere impostata su <strong>false</strong> per indicare che i dati non sono validi.<br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>false</strong><br/></td>
</tr>

<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsDialogPropertyId"></span><span id="uia_isdialogpropertyid"></span><span id="UIA_ISDIALOGPROPERTYID"></span><dl> <dt><strong>UIA_IsDialogPropertyId</strong></dt> <dt>30174</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà della finestra di <strong>dialogo</strong> , che è un valore booleano che indica se l'elemento di automazione è una finestra di dialogo. Ad esempio, la tecnologia per l'accessibilità, ad esempio le utilità per la lettura dello schermo, indica in genere il titolo della finestra di dialogo, il controllo attivo nella finestra di dialogo e quindi il contenuto della finestra di dialogo fino al controllo attivo ( &quot; salvare le modifiche prima di chiudere &quot; ). Per le finestre standard, un'area di lettura dello schermo parla in genere del titolo della finestra seguito dal controllo attivo. La <strong>Proprietà IsSynchronized</strong> può essere impostata su <strong>true</strong> per indicare che l'applicazione client deve trattare l'elemento come una finestra di dialogo.<br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>false</strong><br/></td>
</tr>

<tr class="even">
<td style="text-align: left;"><span id="UIA_IsEnabledPropertyId"></span><span id="uia_isenabledpropertyid"></span><span id="UIA_ISENABLEDPROPERTYID"></span><dl> <dt><strong>UIA_IsEnabledPropertyId</strong></dt> <dt>30010</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>IsEnabled</strong> , che è un valore booleano che indica se l'elemento dell'interfaccia utente a cui fa riferimento l'elemento di automazione è abilitato e può essere interagito con.<br/> Quando lo stato di abilitazione di un controllo è <strong>false</strong>, si presuppone che anche i controlli figlio non siano abilitati. I client non devono prevedere eventi di modifica della proprietà dagli elementi figlio quando lo stato del controllo padre viene modificato.<br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsKeyboardFocusablePropertyId"></span><span id="uia_iskeyboardfocusablepropertyid"></span><span id="UIA_ISKEYBOARDFOCUSABLEPROPERTYID"></span><dl> <dt><strong>UIA_IsKeyboardFocusablePropertyId</strong></dt> <dt>30009</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>IsKeyboardFocusable</strong> , che è un valore booleano che indica se l'elemento di automazione può accettare lo stato attivo della tastiera.<br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsOffscreenPropertyId"></span><span id="uia_isoffscreenpropertyid"></span><span id="UIA_ISOFFSCREENPROPERTYID"></span><dl> <dt><strong>UIA_IsOffscreenPropertyId</strong></dt> <dt>30022</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>IsOffscreen</strong> , che è un valore booleano che indica se l'elemento di automazione è completamente scorrevole fuori dalla visualizzazione (ad esempio, un elemento in una casella di riepilogo all'esterno del viewport dell'oggetto contenitore) o compresso fuori dalla visualizzazione (ad esempio, un elemento in una visualizzazione albero o un menu o in una finestra ridotta a icona). Se l'elemento ha un punto selezionabile che può causare la ricezione dello stato attivo, l'elemento viene considerato sullo schermo mentre una parte dell'elemento è fuori schermo.<br/> Il valore della proprietà non è influenzato dall'occlusione da altre finestre o dal fatto che l'elemento sia visibile su un monitor specifico.<br/> Se la proprietà <strong>IsOffscreen</strong> è <strong>true</strong>, l'elemento dell'interfaccia utente viene spostato fuori schermo o compresso. L'elemento è temporaneamente nascosto, ma rimane nella percezione dell'utente finale e continua a essere incluso nel modello dell'interfaccia utente. È possibile riportare l'oggetto nella visualizzazione scorrendo, facendo clic su un elenco a discesa e così via.<br/> Oggetti che l'utente finale non percepisce affatto o che sono nascosti a livello di &quot; codice &quot; (ad esempio, una finestra di dialogo che è stata ignorata, ma l'oggetto sottostante è ancora memorizzato nella cache dall'applicazione) non deve trovarsi nell'albero degli elementi di automazione nella prima posizione, anziché impostare lo stato di <strong>IsOffscreen</strong> su <strong>true</strong>.<br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsPasswordPropertyId"></span><span id="uia_ispasswordpropertyid"></span><span id="UIA_ISPASSWORDPROPERTYID"></span><dl> <dt><strong>UIA_IsPasswordPropertyId</strong></dt> <dt>30019</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà di <strong>password</strong> , ovvero un valore booleano che indica se l'elemento di automazione contiene contenuto protetto o una password.<br/> Quando la <strong>Proprietà IsSynchronized</strong> è <strong>true</strong> e l'elemento dispone dello stato attivo della tastiera, un'applicazione client deve disabilitare l'eco della tastiera o il feedback dell'input da tastiera che può esporre le informazioni protette dell'utente. Il tentativo di accedere alla proprietà <strong>value</strong> dell'elemento Protected (controllo di modifica) può causare un errore.<br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_IsPeripheralPropertyId"></span><span id="uia_isperipheralpropertyid"></span><span id="UIA_ISPERIPHERALPROPERTYID"></span><dl> <dt><strong>UIA_IsPeripheralPropertyId</strong></dt> <dt>30150</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà di <strong>periferia</strong> , che è un valore booleano che indica se l'elemento di automazione rappresenta l'interfaccia utente periferica. Viene visualizzata l'interfaccia utente periferica che supporta l'interazione dell'utente, ma non lo stato attivo quando viene visualizzato. Esempi di interfaccia utente periferica includono popup, riquadri a comparsa, menu di scelta rapida o notifiche a virgola mobile. Supportato a partire da Windows 8.1.<br/> Quando la <strong>Proprietà IsSynchronized</strong> è <strong>true</strong>, un'applicazione client non può presupporre che lo stato attivo è stato rilevato dall'elemento anche se è attualmente interattivo da tastiera.<br/> Questa proprietà è pertinente per i tipi di controllo seguenti:<br/>
<ul>
<li><strong>UIA_GroupControlTypeId</strong></li>
<li><strong>UIA_MenuControlTypeId</strong></li>
<li><strong>UIA_PaneControlTypeId</strong></li>
<li><strong>UIA_ToolBarControlTypeId</strong></li>
<li><strong>UIA_ToolTipControlTypeId</strong></li>
<li><strong>UIA_WindowControlTypeId</strong></li>
<li><strong>UIA_CustomControlTypeId</strong></li>
</ul>
Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_IsRequiredForFormPropertyId"></span><span id="uia_isrequiredforformpropertyid"></span><span id="UIA_ISREQUIREDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsRequiredForFormPropertyId</strong></dt> <dt>30025</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>IsRequiredForForm</strong> , che è un valore booleano che indica se è necessario compilare l'elemento di automazione in un form.<br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ItemStatusPropertyId"></span><span id="uia_itemstatuspropertyid"></span><span id="UIA_ITEMSTATUSPROPERTYID"></span><dl> <dt><strong>UIA_ItemStatusPropertyId</strong></dt> <dt>30026</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>ItemStatus</strong> , ovvero una stringa di testo che descrive lo stato di un elemento dell'elemento di automazione.<br/> <strong>ItemStatus</strong> consente a un client di verificare se un elemento comunica lo stato di un elemento e lo stato. Ad esempio, un elemento associato a un contatto in un'applicazione di messaggistica potrebbe essere &quot; occupato &quot; o &quot; connesso &quot; .<br/> Quando <strong>ItemStatus</strong> è supportato, la stringa deve corrispondere alla lingua dell'interfaccia utente dell'applicazione o alla lingua dell'interfaccia utente predefinita del sistema operativo.<br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ItemTypePropertyId"></span><span id="uia_itemtypepropertyid"></span><span id="UIA_ITEMTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ItemTypePropertyId</strong></dt> <dt>300021</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>ItemType</strong> , ovvero una stringa di testo che descrive il tipo dell'elemento di automazione.<br/> <strong>ItemType</strong> viene usato per ottenere informazioni sugli elementi in un elenco, in una visualizzazione albero o in una griglia di dati. Ad esempio, un elemento in una visualizzazione directory di file può essere un &quot; file di documento &quot; o una &quot; cartella &quot; .<br/> Quando <strong>ItemType</strong> è supportato, la stringa deve corrispondere alla lingua dell'interfaccia utente dell'applicazione o alla lingua dell'interfaccia utente predefinita del sistema operativo.<br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LabeledByPropertyId"></span><span id="uia_labeledbypropertyid"></span><span id="UIA_LABELEDBYPROPERTYID"></span><dl> <dt><strong>UIA_LabeledByPropertyId</strong></dt> <dt>30018</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>LabeledBy</strong> , che è un elemento di automazione che contiene l'etichetta di testo per questo elemento.<br/> Questa proprietà può essere utilizzata per recuperare, ad esempio, l'etichetta di testo statico per una casella combinata.<br/> Tipo Variant: <strong>VT_UNKNOWN</strong><br/> Valore predefinito: <strong>null</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LandmarkTypePropertyId"></span><span id="uia_landmarktypepropertyid"></span><span id="UIA_LANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LandmarkTypePropertyId</strong></dt> <dt>30157</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>LandmarkType</strong> , che è un <a href="landmark-type-identifiers.md"><strong>identificatore del tipo di riferimento</strong></a> associato a un elemento.<br/> La proprietà <strong>LandmarkType</strong> descrive un elemento che rappresenta un gruppo di elementi. Un punto di riferimento di ricerca, ad esempio, potrebbe rappresentare un set di controlli correlati per la ricerca.<br/> Se <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> viene usato, <strong>UIA_LocalizedLandmarkTypePropertyId</strong> è necessario per descrivere il punto di riferimento personalizzato.<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LevelPropertyId"></span><span id="uia_levelpropertyid"></span><span id="UIA_LEVELPROPERTYID"></span><dl> <dt><strong>UIA_LevelPropertyId</strong></dt> <dt>30154</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>Level</strong> , che è un Integer in base 1 associato a un elemento di automazione.<br/> La proprietà <strong>Level</strong> descrive la posizione di un elemento all'interno di strutture gerarchiche gerarchiche o interrotte. Ad esempio, un elenco puntato/numerato, intestazioni o altri elementi di dati strutturati possono avere diverse relazioni padre/figlio. Il <strong>livello</strong> descrive il punto della struttura in cui si trova l'elemento.<br/> È consigliabile usare il pattern di <a href="/windows/desktop/WinAuto/uiauto-implementingcustomnavigation">controllo CustomNavigation</a> in tandem con <strong>Level</strong>.<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LiveSettingPropertyId"></span><span id="uia_livesettingpropertyid"></span><span id="UIA_LIVESETTINGPROPERTYID"></span><dl> <dt><strong>UIA_LiveSettingPropertyId</strong></dt> <dt>30135</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>LiveSetting</strong> , supportata da un elemento di automazione che rappresenta un'area dinamica. La proprietà <strong>LiveSetting</strong> indica il &quot; livello di cortesia &quot; che un client deve usare per notificare all'utente le modifiche apportate all'area dinamica. Questa proprietà può essere uno dei valori dell'enumerazione <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-livesetting"><strong>LiveSetting</strong></a> . Supportato a partire da Windows 8.<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_LocalizedControlTypePropertyId"></span><span id="uia_localizedcontroltypepropertyid"></span><span id="UIA_LOCALIZEDCONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedControlTypePropertyId</strong></dt> <dt>30004</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>LocalizedControlType</strong> , ovvero una stringa di testo che descrive il tipo di controllo rappresentato dall'elemento di automazione. La stringa deve contenere solo caratteri minuscoli:
<ul>
<li>Corretto: &quot; pulsante&quot;</li>
<li>Errato: &quot; pulsante&quot;</li>
</ul>
<br/> Quando <strong>LocalizedControlType</strong> non viene specificato dal provider di elementi, la stringa localizzata predefinita viene fornita dal Framework, in base al tipo di controllo dell'elemento, ad esempio il &quot; pulsante &quot; per il tipo di controllo <a href="uiauto-supportbuttoncontroltype.md">Button</a> . Un elemento di automazione con il tipo di controllo <strong>personalizzato</strong> deve supportare una stringa del tipo di controllo localizzato che rappresenta il ruolo dell'elemento, ad esempio la &quot; selezione colori &quot; per un controllo personalizzato che consente agli utenti di scegliere e specificare i colori.<br/> Quando viene specificato un valore personalizzato, la stringa deve corrispondere alla lingua dell'interfaccia utente dell'applicazione o alla lingua dell'interfaccia utente predefinita del sistema operativo.<br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_LocalizedLandmarkTypePropertyId"></span><span id="uia_localizedlandmarktypepropertyid"></span><span id="UIA_LOCALIZEDLANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedLandmarkTypePropertyId</strong></dt> <dt>30158</dt> </dl></td>
<td style="text-align: left;">Identifica <strong>LocalizedLandmarkType</strong>, ovvero una stringa di testo che descrive il tipo di riferimento rappresentato dall'elemento di automazione.<br/> Questa operazione deve essere utilizzata in combinazione con <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> tuttavia, <strong>LocalizedLandmarkType</strong> deve avere sempre la precedenza su <strong>LandmarkType</strong> e essere usato per descrivere il Landmark prima di <strong>LandmarkType</strong>.<br/> La stringa deve corrispondere alla lingua dell'interfaccia utente dell'applicazione o alla lingua dell'interfaccia utente predefinita del sistema operativo.<br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_NamePropertyId"></span><span id="uia_namepropertyid"></span><span id="UIA_NAMEPROPERTYID"></span><dl> <dt><strong>UIA_NamePropertyId</strong></dt> <dt>30005</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>Name</strong> , che è una stringa che include il nome dell'elemento di automazione.<br/> La proprietà <strong>Name</strong> deve essere identica a quella del testo dell'etichetta sullo schermo. Ad esempio, il <strong>nome</strong> deve essere &quot; ricerca &quot; di un elemento Button con l'etichetta &quot; Browse &quot; . La proprietà <strong>Name</strong> non deve includere il carattere mnemonico per le chiavi di accesso (ovvero &quot; & &quot; ), sottolineato nella presentazione del testo dell'interfaccia utente. Inoltre, la proprietà <strong>Name</strong> non deve essere una versione estesa o modificata dell'etichetta sullo schermo perché l'incoerenza tra il nome e l'etichetta può causare confusione tra applicazioni client e utenti.<br/> Quando il testo dell'etichetta corrispondente non è visibile sullo schermo o quando viene sostituito da grafica, è necessario scegliere il testo alternativo. Il testo alternativo deve essere conciso, intuitivo e localizzato per la lingua dell'interfaccia utente dell'applicazione o per la lingua dell'interfaccia utente predefinita del sistema operativo. Il testo alternativo non deve essere una descrizione dettagliata dei dettagli visivi, ma una descrizione concisa della funzione o della funzionalità dell'interfaccia utente come se fosse contrassegnata da testo semplice. Il pulsante del menu Start di Windows, ad esempio, è denominato &quot; inizio &quot; (pulsante) invece del &quot; logo Windows sulla grafica della sfera rotonda blu &quot; (pulsante). Per ulteriori informazioni, vedere <a href="/previous-versions/windows/desktop/dnacc/creating-text-equivalents-for-images">creazione di equivalenti di testo per le immagini</a>.<br/> Quando un'etichetta dell'interfaccia utente usa grafica di testo (ad esempio, usando &quot; >> &quot; per un pulsante che aggiunge un elemento da sinistra a destra), la proprietà <strong>Name</strong> deve essere sottoposta a override da un testo alternativo appropriato, ad esempio &quot; Add &quot; . Tuttavia, la pratica di usare grafica di testo come etichetta dell'interfaccia utente è sconsigliata a causa di problemi di localizzazione e accessibilità.<br/> Il <strong>nome</strong> della proprietà non deve includere le informazioni sul tipo o sul ruolo del controllo, ad esempio un &quot; pulsante &quot; o un &quot; elenco &quot; ; in caso contrario, sarà in conflitto con il testo della proprietà <strong>LocalizedControlType</strong> quando queste due proprietà vengono accodate (molte tecnologie per l'accessibilità esistenti lo eseguono).<br/> Impossibile utilizzare la proprietà <strong>Name</strong> come identificatore univoco tra gli elementi di pari livello. Tuttavia, purché sia coerente con la presentazione dell'interfaccia utente, lo stesso valore del <strong>nome</strong> può essere supportato tra i peer. Per l'automazione di test, i client devono considerare l'uso della proprietà <strong>AutomationId</strong> o <strong>IDruntime</strong> .<br/> Per i controlli di testo non è sempre necessario che la proprietà <strong>Name</strong> sia identica al testo visualizzato all'interno del controllo, purché sia supportato anche il modello di <strong>testo</strong> .<br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_NativeWindowHandlePropertyId"></span><span id="uia_nativewindowhandlepropertyid"></span><span id="UIA_NATIVEWINDOWHANDLEPROPERTYID"></span><dl> <dt><strong>UIA_NativeWindowHandlePropertyId</strong></dt> <dt>30020</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>NativeWindowHandle</strong> , che è un intero che rappresenta l'handle (<strong>HWND</strong>) della finestra dell'elemento di automazione, se esistente; in caso contrario, questa proprietà è 0.<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_OptimizeForVisualContentPropertyId"></span><span id="uia_optimizeforvisualcontentpropertyid"></span><span id="UIA_OPTIMIZEFORVISUALCONTENTPROPERTYID"></span><dl> <dt><strong>UIA_OptimizeForVisualContentPropertyId</strong></dt> <dt>30111</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>OptimizeForVisualContent</strong> , che è un valore booleano che indica se il provider espone solo elementi visibili. Un provider può utilizzare questa proprietà per ottimizzare le prestazioni quando si utilizzano parti di contenuto molto grandi. Ad esempio, quando le pagine utente passano da un contenuto elevato, il provider può eliminare definitivamente gli elementi di contenuto che non sono più visibili. Quando un elemento di contenuto viene eliminato definitivamente, il provider deve restituire il codice di errore <strong>UIA_E_ELEMENTNOTAVAILABLE</strong> . Supportato a partire da Windows 8.<br/> Tipo Variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_OrientationPropertyId"></span><span id="uia_orientationpropertyid"></span><span id="UIA_ORIENTATIONPROPERTYID"></span><dl> <dt><strong>UIA_OrientationPropertyId</strong></dt> <dt>300023</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>Orientation</strong> , che indica l'orientamento del controllo rappresentato dall'elemento di automazione. La proprietà viene espressa come valore dal tipo enumerato <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType</strong></a> .<br/> La proprietà <strong>Orientation</strong> è supportata dai controlli, ad esempio barre di scorrimento e cursori, che possono avere un orientamento verticale o orizzontale. In caso contrario, può sempre essere <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>, il che significa che il controllo non ha un orientamento.<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0 (<a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>)<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_OutlineColorPropertyId"></span><span id="uia_outlinecolorpropertyid"></span><span id="UIA_OUTLINECOLORPROPERTYID"></span><dl> <dt><strong>UIA_OutlineColorPropertyId</strong></dt> <dt>30161</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>OutlineColor</strong> , che specifica il colore utilizzato per la struttura dell'elemento di automazione. Questo attributo viene specificato come <strong>COLORREF</strong>, un valore a 32 bit utilizzato per specificare un colore RGB o RGBA.<br/> Tipo Variant: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_OutlineThicknessPropertyId"></span><span id="uia_outlinethicknesspropertyid"></span><span id="UIA_OUTLINETHICKNESSPROPERTYID"></span><dl> <dt><strong>UIA_OutlineThicknessPropertyId</strong></dt> <dt>30164</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>OutlineThickness</strong> , che specifica la larghezza per la struttura dell'elemento di automazione.<br/> Tipo Variant: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_PositionInSetPropertyId"></span><span id="uia_positioninsetpropertyid"></span><span id="UIA_POSITIONINSETPROPERTYID"></span><dl> <dt><strong>UIA_PositionInSetPropertyId</strong></dt> <dt>30152</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>PositionInSet</strong> , che è un Integer in base 1 associato a un elemento di automazione. <strong>PositionInSet</strong> descrive la posizione ordinale dell'elemento in un set di elementi considerati di pari livello.<br/> <strong>PositionInSet</strong> funziona in modo coordinato con la proprietà <strong>SizeOfSet</strong> per descrivere la posizione ordinale nel set.<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_ProcessIdPropertyId"></span><span id="uia_processidpropertyid"></span><span id="UIA_PROCESSIDPROPERTYID"></span><dl> <dt><strong>UIA_ProcessIdPropertyId</strong></dt> <dt>30002</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>ProcessID</strong> , che è un Integer che rappresenta l'identificatore di processo (ID) dell'elemento di automazione.<br/> L'identificatore (ID) del processo viene assegnato dal sistema operativo. Può essere visualizzato nella colonna <strong>PID</strong> della scheda <strong>processi</strong> di gestione attività.<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_ProviderDescriptionPropertyId"></span><span id="uia_providerdescriptionpropertyid"></span><span id="UIA_PROVIDERDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_ProviderDescriptionPropertyId</strong></dt> <dt>30107</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>ProviderDescription</strong> , che è una stringa formattata contenente le informazioni sull'origine del provider di automazione interfaccia utente per l'elemento di automazione, incluse le informazioni sul proxy.<br/> Tipo Variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_RotationPropertyId"></span><span id="uia_rotationpropertyid"></span><span id="UIA_ROTATIONPROPERTYID"></span><dl> <dt><strong>UIA_RotationPropertyId</strong></dt> <dt>30166</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>Rotation</strong> , che specifica l'angolo di rotazione in unità non specificate.<br/> Tipo Variant: <strong>VT_R8</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_RuntimeIdPropertyId"></span><span id="uia_runtimeidpropertyid"></span><span id="UIA_RUNTIMEIDPROPERTYID"></span><dl> <dt><strong>UIA_RuntimeIdPropertyId</strong></dt> <dt>30000</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>IDruntime</strong> , che è una matrice di Integer che rappresenta l'identificatore per un elemento di automazione.<br/> L'identificatore è univoco sul desktop, ma è sicuramente univoco solo all'interno dell'interfaccia utente del desktop in cui è stato generato. Gli identificatori possono essere riutilizzati nel tempo.<br/> Il formato di <strong>IDruntime</strong> può cambiare. L'identificatore restituito deve essere trattato come un valore opaco e utilizzato solo per il confronto. ad esempio, per determinare se un elemento di automazione si trova nella cache.<br/> Tipo Variant: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_SizePropertyId"></span><span id="uia_sizepropertyid"></span><span id="UIA_SIZEPROPERTYID"></span><dl> <dt><strong>UIA_SizePropertyId</strong></dt> <dt>30167</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>size</strong> , che specifica la larghezza e l'altezza dell'elemento di automazione.<br/> Tipo Variant: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="UIA_SizeOfSetPropertyId"></span><span id="uia_sizeofsetpropertyid"></span><span id="UIA_SIZEOFSETPROPERTYID"></span><dl> <dt><strong>UIA_SizeOfSetPropertyId</strong></dt> <dt>30153</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>SizeOfSet</strong> , che è un Integer in base 1 associato a un elemento di automazione. <strong>SizeOfSet</strong> descrive il numero di elementi di automazione in un gruppo o in un set considerati di pari livello.<br/> <strong>SizeOfSet</strong> funziona in coordinamento con la proprietà <strong>PositionInSet</strong> per descrivere il numero di elementi nel set.<br/> Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="UIA_VisualEffectsPropertyId"></span><span id="uia_visualeffectspropertyid"></span><span id="UIA_VISUALEFFECTSPROPERTYID"></span><dl> <dt><strong>UIA_VisualEffectsPropertyId</strong></dt> <dt>30163</dt> </dl></td>
<td style="text-align: left;">Identifica la proprietà <strong>VisualEffects</strong> , che è un campo di bit che specifica gli effetti sull'elemento di automazione, ad esempio ombreggiatura, Reflection, bagliore, bordi morbidi o smussatura.<br/> VisualEffects:<br/>
<ul>
<li>VisualEffects_Shadow: 0x1</li>
<li>VisualEffects_Reflection: 0x2</li>
<li>VisualEffects_Glow: 0x4</li>
<li>VisualEffects_SoftEdges: 0x8</li>
<li>VisualEffects_Bevel: 0x10</li>
</ul>
Tipo Variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
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

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sulle proprietà di automazione interfaccia utente](uiauto-propertiesoverview.md)
</dt> <dt>

[Recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md)
</dt> </dl>
