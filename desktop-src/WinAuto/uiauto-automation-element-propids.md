---
title: Identificatori delle proprietà degli elementi di automazione (UIAutomationClient.h)
description: In questo argomento vengono descritte le costanti denominate che identificano le proprietà di Microsoft Automazione interfaccia utente elementi.
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
ms.openlocfilehash: b373091ec34e71afbac32fca962ec380513acfcd
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627697"
---
# <a name="automation-element-property-identifiers"></a>Identificatori delle proprietà degli elementi di automazione

In questo argomento vengono descritte le costanti denominate che identificano le proprietà di Microsoft Automazione interfaccia utente elementi.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Costante/valore</th>
<th >Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="UIA_AcceleratorKeyPropertyId"></span><span id="uia_acceleratorkeypropertyid"></span><span id="UIA_ACCELERATORKEYPROPERTYID"></span><dl> <dt><strong>UIA_AcceleratorKeyPropertyId</strong></dt> <dt>30006</dt> </dl></td>
<td >Identifica la <strong>proprietà AcceleratorKey,</strong> ovvero una stringa contenente le combinazioni di tasti di scelta rapida (denominate anche tasti di scelta rapida) per l'elemento di automazione. <br/> Le combinazioni di tasti di scelta rapida richiamano un'azione. Ad esempio, CTRL+O viene spesso usato per richiamare la finestra di dialogo Comune Apri file. Un elemento di automazione con la <strong>proprietà AcceleratorKey</strong> può implementare il pattern di controllo <a href="uiauto-implementinginvoke.md">Invoke</a> per l'azione equivalente al comando di scelta rapida.<br/> Tipo variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_AccessKeyPropertyId"></span><span id="uia_accesskeypropertyid"></span><span id="UIA_ACCESSKEYPROPERTYID"></span><dl> <dt><strong>UIA_AccessKeyPropertyId</strong></dt> <dt>30007</dt> </dl></td>
<td >Identifica la <strong>proprietà AccessKey,</strong> ovvero una stringa contenente il carattere del tasto di scelta per l'elemento di automazione.<br/> Un tasto di scelta (talvolta denominato tasto di scelta) è un carattere nel testo di un menu, una voce di menu o un'etichetta di un controllo, ad esempio un pulsante, che attiva la funzione di menu associata. Ad esempio, per aprire il menu File, per il quale il tasto di scelta è in genere F, l'utente preme ALT+F.<br/> Tipo variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_AnnotationObjectsPropertyId"></span><span id="uia_annotationobjectspropertyid"></span><span id="UIA_ANNOTATIONOBJECTSPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationObjectsPropertyId</strong></dt> <dt>30156</dt> </dl></td>
<td >Identifica la <strong>proprietà AnnotationObjects,</strong> ovvero un elenco di oggetti annotazione in un documento, ad esempio commento, intestazione, piè di pagina e così via.<br/> Tipo variant: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: matrice vuota<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_AnnotationTypesPropertyId"></span><span id="uia_annotationtypespropertyid"></span><span id="UIA_ANNOTATIONTYPESPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationTypesPropertyId</strong></dt> <dt>30155</dt> </dl></td>
<td >Identifica la <strong>proprietà AnnotationTypes,</strong> ovvero un elenco dei tipi di annotazioni in un documento, ad esempio commento, intestazione, piè di pagina e così via.<br/> Tipo variant: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: matrice vuota<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_AriaPropertiesPropertyId"></span><span id="uia_ariapropertiespropertyid"></span><span id="UIA_ARIAPROPERTIESPROPERTYID"></span><dl> <dt><strong>UIA_AriaPropertiesPropertyId</strong></dt> <dt>30102</dt> </dl></td>
<td >Identifica la <strong>proprietà AriaProperties,</strong> ovvero una stringa formattata contenente le informazioni sulla proprietà ARIA (Accessible Rich Internet Application) per l'elemento di automazione. Per altre informazioni sul mapping di stati e proprietà ARIA Automazione interfaccia utente proprietà e funzioni, vedere Automazione interfaccia utente <a href="uiauto-ariaspecification.md">for W3C Accessible Rich Internet Applications Specification</a>.<br/> <strong>AriaProperties</strong> è una raccolta di coppie nome/valore con delimitatori (uguale a) e ; (punto e virgola), ad esempio <strong>=</strong> <strong></strong> &quot; checked=true;disabled=false &quot; . La barra rovesciata viene usata come carattere di escape quando questi caratteri <strong>\</strong> di delimitazione o vengono visualizzati nei <strong>\</strong> valori. Per motivi di sicurezza e per altri motivi, l'implementazione del provider di questa proprietà può eseguire passaggi per convalidare le proprietà ARIA originali. tuttavia non è obbligatorio.<br/> Tipo variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_AriaRolePropertyId"></span><span id="uia_ariarolepropertyid"></span><span id="UIA_ARIAROLEPROPERTYID"></span><dl> <dt><strong>UIA_AriaRolePropertyId</strong></dt> <dt>30101</dt> </dl></td>
<td >Identifica la <strong>proprietà AriaRole,</strong> ovvero una stringa contenente le informazioni sul ruolo Aria (Accessible Rich Internet Application) per l'elemento di automazione. Per altre informazioni sul mapping dei ruoli ARIA Automazione interfaccia utente tipi di controllo, vedere <a href="uiauto-ariaspecification.md">Automazione interfaccia utente for W3C Accessible Rich Internet Applications Specification</a>.<br/>
<blockquote>
[!Note]<br />
Come opzione, l'agente utente può anche offrire una descrizione localizzata del ruolo ARIA W3C nella <strong>proprietà LocalizedControlType.</strong> Quando la stringa localizzata non viene specificata, il sistema fornirà la stringa <strong>LocalizedControlType predefinita</strong> per l'elemento.
</blockquote>
<br/> <br/> Tipo variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_AutomationIdPropertyId"></span><span id="uia_automationidpropertyid"></span><span id="UIA_AUTOMATIONIDPROPERTYID"></span><dl> <dt><strong>UIA_AutomationIdPropertyId</strong></dt> <dt>30011</dt> </dl></td>
<td >Identifica la <strong>proprietà AutomationId,</strong> che è una stringa contenente l Automazione interfaccia utente id (ID) per l'elemento di automazione.<br/> Quando è disponibile, <strong>automationId</strong> di un elemento deve essere lo stesso in qualsiasi istanza dell'applicazione, indipendentemente dalla lingua locale. Il valore deve essere univoco tra gli elementi di pari livello, ma non necessariamente univoco nell'intero desktop. Ad esempio, più istanze di un'applicazione o più visualizzazioni cartelle in Microsoft Windows Explorer possono contenere elementi con la stessa proprietà <strong>AutomationId,</strong> ad esempio &quot; SystemMenuBar &quot; .<br/> Anche se il supporto <strong>per AutomationId</strong> è sempre consigliato per migliorare il supporto dei test automatizzati, questa proprietà non è obbligatoria. Dove è supportato, <strong>AutomationId è</strong> utile per la creazione di uno script di automazione di test che viene eseguito indipendentemente dal linguaggio dell'interfaccia utente. I client non devono fare ipotesi sui valori <strong>AutomationId</strong> esposti da altre applicazioni. Non è garantito che <strong>AutomationId</strong> sia stabile tra versioni o build diverse di un'applicazione.<br/> Tipo variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_BoundingRectanglePropertyId"></span><span id="uia_boundingrectanglepropertyid"></span><span id="UIA_BOUNDINGRECTANGLEPROPERTYID"></span><dl> <dt><strong>UIA_BoundingRectanglePropertyId</strong></dt> <dt>30001</dt> </dl></td>
<td >Identifica la <strong>proprietà BoundingRectangle,</strong> che specifica le coordinate del rettangolo che racchiude completamente l'elemento di automazione. Il rettangolo è espresso in coordinate fisiche dello schermo. Può contenere punti che non sono selezionabili se la forma o l'area selezionabile dell'elemento dell'interfaccia utente è irregolare o se l'elemento è nascosto da altri elementi dell'interfaccia utente.<br/> Tipo variant: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: [0,0,0,0]<br/>
<blockquote>
[!Note]<br />
Questa proprietà è <strong>NULL se</strong> l'elemento non visualizza attualmente un'interfaccia utente.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_CenterPointPropertyId"></span><span id="uia_centerpointpropertyid"></span><span id="UIA_CENTERPOINTPROPERTYID"></span><dl> <dt><strong>UIA_CenterPointPropertyId</strong></dt> <dt>30165</dt> </dl></td>
<td >Identifica la <strong>proprietà CenterPoint,</strong> che specifica le coordinate dei punti X e Y al centro dell'elemento di automazione. Lo spazio delle coordinate è ciò che il provider considera logicamente una pagina.<br/> Tipo variant: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ClassNamePropertyId"></span><span id="uia_classnamepropertyid"></span><span id="UIA_CLASSNAMEPROPERTYID"></span><dl> <dt><strong>UIA_ClassNamePropertyId</strong></dt> <dt>30012</dt> </dl></td>
<td >Identifica la <strong>proprietà ClassName,</strong> ovvero una stringa contenente il nome della classe per l'elemento di automazione assegnato dallo sviluppatore del controllo.<br/> Il nome della classe dipende dall'implementazione del provider Automazione interfaccia utente e pertanto non è sempre in un formato standard. Tuttavia, se il nome della classe è noto, può essere usato per verificare che un'applicazione funzioni con l'elemento di automazione previsto.<br/> Tipo variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ClickablePointPropertyId"></span><span id="uia_clickablepointpropertyid"></span><span id="UIA_CLICKABLEPOINTPROPERTYID"></span><dl> <dt><strong>UIA_ClickablePointPropertyId</strong></dt> <dt>30014</dt> </dl></td>
<td >Identifica la <strong>proprietà ClickablePoint,</strong> ovvero un punto sull'elemento di automazione su cui è possibile fare clic. Non è possibile fare clic su un elemento se è completamente o parzialmente nascosto da un'altra finestra.<br/> Tipo variant: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ControllerForPropertyId"></span><span id="uia_controllerforpropertyid"></span><span id="UIA_CONTROLLERFORPROPERTYID"></span><dl> <dt><strong>UIA_ControllerForPropertyId</strong></dt> <dt>30104</dt> </dl></td>
<td >Identifica la <strong>proprietà ControllerFor,</strong> ovvero una matrice di elementi di automazione che vengono manipolati dall'elemento di automazione che supporta questa proprietà.<br/> <strong>ControllerFor viene</strong> usato quando un elemento di automazione influisce su uno o più segmenti dell'interfaccia utente dell'applicazione o sul desktop; In caso contrario, è difficile associare l'impatto dell'operazione di controllo agli elementi dell'interfaccia utente.<br/> Questo identificatore viene comunemente usato per <a href="/windows/uwp/design/accessibility/accessible-text-requirements">l'accessibilità Suggerimento automatico.</a><br/> Tipo variant per i provider: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo variant per i client: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a> )<br/> Valore predefinito: matrice vuota<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ControlTypePropertyId"></span><span id="uia_controltypepropertyid"></span><span id="UIA_CONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ControlTypePropertyId</strong></dt> <dt>30003</dt> </dl></td>
<td >Identifica la <strong>proprietà ControlType,</strong> ovvero una classe che identifica il tipo dell'elemento di automazione. <strong>ControlType definisce</strong> le caratteristiche degli elementi dell'interfaccia utente da primitive di controlli dell'interfaccia utente note, ad esempio pulsante o casella di controllo. <br/> Tipo variant: <strong>VT_I4</strong><br/> Valore predefinito: <a href="uiauto-controltype-ids.md"> <strong>UIA_CustomControlTypeId</strong></a><br/>
<blockquote>
[!Note]<br />
Usare il valore predefinito solo se l'elemento di automazione rappresenta un tipo di controllo completamente nuovo.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_CulturePropertyId"></span><span id="uia_culturepropertyid"></span><span id="UIA_CULTUREPROPERTYID"></span><dl> <dt><strong>UIA_CulturePropertyId</strong></dt> <dt>30015</dt> </dl></td>
<td >Identifica la <strong>proprietà Culture,</strong> che contiene un identificatore delle impostazioni locali per l'elemento di automazione, ad esempio <code>0x0409</code> per en-US o english &quot; &quot; (Stati Uniti)).<br/> Ogni impostazione locale ha un identificatore univoco, un valore a 32 bit costituito da un identificatore di lingua e un identificatore di ordinamento. L'identificatore delle impostazioni locali è un'abbreviazione numerica internazionale standard e include i componenti necessari per identificare in modo univoco una delle impostazioni locali definite dal sistema operativo installato. Per altre informazioni, vedere Costanti e stringhe <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">degli identificatori di lingua.</a><br/> Questa proprietà può esistere in base al controllo, ma in genere è disponibile solo a livello di applicazione.<br/> Tipo variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_DescribedByPropertyId"></span><span id="uia_describedbypropertyid"></span><span id="UIA_DESCRIBEDBYPROPERTYID"></span><dl> <dt><strong>UIA_DescribedByPropertyId</strong></dt> <dt>30105</dt> </dl></td>
<td >Identifica la <strong>proprietà DescribedBy,</strong> ovvero una matrice di elementi che forniscono altre informazioni sull'elemento di automazione.<br/> <strong>DescribedBy viene</strong> usato quando un elemento di automazione è spiegato da un altro segmento dell'interfaccia utente dell'applicazione. Ad esempio, la proprietà può puntare a un elemento di testo di &quot; 2.529 elementi in 85 gruppi, 10 elementi selezionati da un oggetto elenco personalizzato &quot; complesso. Invece di usare il modello a oggetti per i client per il digest di informazioni simili, la proprietà <strong>DescribedBy</strong> può offrire accesso rapido all'elemento dell'interfaccia utente che potrebbe già offrire informazioni utili per l'utente finale che descrivono l'elemento dell'interfaccia utente.<br/> Tipo variant per i provider: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo variant per i client: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valore predefinito: matrice vuota<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_FillColorPropertyId"></span><span id="uia_fillcolorpropertyid"></span><span id="UIA_FILLCOLORPROPERTYID"></span><dl> <dt><strong>UIA_FillColorPropertyId</strong></dt> <dt>30160</dt> </dl></td>
<td >Identifica la <strong>proprietà FillColor,</strong> che specifica il colore usato per riempire l'elemento di automazione. Questo attributo viene specificato come COLORREF, un valore a 32 bit usato per specificare un colore RGB o RGBA.<br/> Tipo variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_FillTypePropertyId"></span><span id="uia_filltypepropertyid"></span><span id="UIA_FILLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_FillTypePropertyId</strong></dt> <dt>30162</dt> </dl></td>
<td >Identifica la <strong>proprietà FillType,</strong> che specifica il modello usato per riempire l'elemento di automazione, ad esempio nessuno, colore, sfumatura, immagine, motivo e così via.<br/> Tipo variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_FlowsFromPropertyId"></span><span id="uia_flowsfrompropertyid"></span><span id="UIA_FLOWSFROMPROPERTYID"></span><dl> <dt><strong>UIA_FlowsFromPropertyId</strong></dt> <dt>30148</dt> </dl></td>
<td >Identifica la <strong>proprietà FlowsFrom,</strong> ovvero una matrice di elementi di automazione che suggerisce l'ordine di lettura prima dell'elemento di automazione corrente. Supportato a partire da Windows 8.<br/> La <strong>proprietà FlowsFrom</strong> specifica l'ordine di lettura quando gli elementi di automazione non sono esposti o strutturati nello stesso ordine di lettura percepito dall'utente. Anche se <strong>la proprietà FlowsFrom</strong> può specificare più elementi precedenti, in genere contiene solo l'elemento precedente nell'ordine di lettura.<br/> Tipo variant per i provider: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo variant per i client: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valore predefinito: matrice vuota<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_FlowsToPropertyId"></span><span id="uia_flowstopropertyid"></span><span id="UIA_FLOWSTOPROPERTYID"></span><dl> <dt><strong>UIA_FlowsToPropertyId</strong></dt> <dt>30106</dt> </dl></td>
<td >Identifica la <strong>proprietà FlowsTo,</strong> ovvero una matrice di elementi di automazione che suggerisce l'ordine di lettura dopo l'elemento di automazione corrente.<br/> La <strong>proprietà FlowsTo</strong> specifica l'ordine di lettura quando gli elementi di automazione non sono esposti o strutturati nello stesso ordine di lettura percepito dall'utente. Anche se <strong>la proprietà FlowsTo</strong> può specificare più elementi successivi, in genere contiene solo l'elemento successivo nell'ordine di lettura.<br/> Tipo variant per i provider: <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Tipo variant per i client: <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valore predefinito: matrice vuota<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_FrameworkIdPropertyId"></span><span id="uia_frameworkidpropertyid"></span><span id="UIA_FRAMEWORKIDPROPERTYID"></span><dl> <dt><strong>UIA_FrameworkIdPropertyId</strong></dt> <dt>30024</dt> </dl></td>
<td >Identifica la <strong>proprietà FrameworkId,</strong> ovvero una stringa contenente il nome del framework dell'interfaccia utente sottostante a cui appartiene l'elemento di automazione.<br/> FrameworkId <strong>consente alle applicazioni</strong> client di elaborare gli elementi di automazione in modo diverso a seconda del framework dell'interfaccia utente specifico. Esempi di valori di proprietà &quot; includono Win32, &quot; &quot; WinForm &quot; e &quot; &quot; DirectUI.<br/> Tipo variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_FullDescriptionPropertyId"></span><span id="uia_fulldescriptionpropertyid"></span><span id="UIA_FULLDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_FullDescriptionPropertyId</strong></dt> <dt>30159</dt> </dl></td>
<td >La <strong>proprietà FullDescription</strong> espone una stringa localizzata che può contenere testo di descrizione esteso per un elemento. <strong>FullDescription può</strong> contenere una descrizione più completa di un elemento di quanto possa essere appropriato per l'elemento <strong>Name</strong>.<br/> Tipo variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_HasKeyboardFocusPropertyId"></span><span id="uia_haskeyboardfocuspropertyid"></span><span id="UIA_HASKEYBOARDFOCUSPROPERTYID"></span><dl> <dt><strong>UIA_HasKeyboardFocusPropertyId</strong></dt> <dt>30008</dt> </dl></td>
<td >Identifica la <strong>proprietà HasKeyboardFocus,</strong> che è un valore booleano che indica se l'elemento di automazione ha lo stato attivo della tastiera.<br/> Tipo variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_HeadingLevelPropertyId"></span><span id="uia_headinglevelpropertyid"></span><span id="UIA_HEADINGLEVELPROPERTYID"></span><dl> <dt><strong>UIA_HeadingLevelPropertyId</strong></dt> <dt>30173</dt> </dl></td>
<td >Identifica la <strong>proprietà HeadingLevel,</strong> che indica il livello di intestazione di un Automazione interfaccia utente elemento.<br/> Tipo variant: <strong>VT_I4</strong><br/> Valore predefinito: <strong>HeadingLevel_None</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_HelpTextPropertyId"></span><span id="uia_helptextpropertyid"></span><span id="UIA_HELPTEXTPROPERTYID"></span><dl> <dt><strong>UIA_HelpTextPropertyId</strong></dt> <dt>30013</dt> </dl></td>
<td >Identifica la <strong>proprietà HelpText,</strong> che è una stringa di testo della Guida associata all'elemento di automazione.<br/> La <strong>proprietà HelpText</strong> può essere supportata con il testo segnaposto visualizzato nei controlli di modifica o elenco. Ad esempio, Digitare qui il testo per la ricerca è un buon candidato alla proprietà HelpText per un controllo di modifica che posiziona il testo prima &quot; &quot; dell'input effettivo dell'utente. <strong></strong> Tuttavia, non è adeguato per la proprietà name del controllo di modifica.<br/> Quando <strong>HelpText è supportato,</strong> la stringa deve corrispondere alla lingua dell'interfaccia utente dell'applicazione o alla lingua predefinita dell'interfaccia utente del sistema operativo.<br/> Tipo variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsContentElementPropertyId"></span><span id="uia_iscontentelementpropertyid"></span><span id="UIA_ISCONTENTELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsContentElementPropertyId</strong></dt> <dt>30017</dt> </dl></td>
<td >Identifica la <strong>proprietà IsContentElement,</strong> ovvero un valore booleano che specifica se l'elemento viene visualizzato nella visualizzazione contenuto dell'albero degli elementi di automazione. Per altre informazioni, vedere Panoramica <a href="uiauto-treeoverview.md">Automazione interfaccia utente albero di .</a><br/>
<blockquote>
[!Note]<br />
Per visualizzare un elemento nella visualizzazione contenuto, sia la proprietà <strong>IsContentElement</strong> che la <strong>proprietà IsControlElement</strong> devono essere <strong>TRUE.</strong>
</blockquote>
<br/> <br/> Tipo variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>TRUE</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_IsControlElementPropertyId"></span><span id="uia_iscontrolelementpropertyid"></span><span id="UIA_ISCONTROLELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsControlElementPropertyId</strong></dt> <dt>30016</dt> </dl></td>
<td >Identifica la <strong>proprietà IsControlElement,</strong> ovvero un valore booleano che specifica se l'elemento viene visualizzato nella visualizzazione controlli dell'albero degli elementi di automazione. Per altre informazioni, vedere Panoramica <a href="uiauto-treeoverview.md">Automazione interfaccia utente albero di .</a><br/> Tipo variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>TRUE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsDataValidForFormPropertyId"></span><span id="uia_isdatavalidforformpropertyid"></span><span id="UIA_ISDATAVALIDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsDataValidForFormPropertyId</strong></dt> <dt>30103</dt> </dl></td>
<td >Identifica la <strong>proprietà IsDataValidForForm,</strong> ovvero un valore booleano che indica se il valore immesso o selezionato è valido per la regola del modulo associata all'elemento di automazione. Ad esempio, se l'utente ha immesso &quot; 425-555-5555 per un campo di codice postale che richiede 5 o 9 cifre, la proprietà &quot; <strong>IsDataValidForForm</strong> può essere impostata su <strong>FALSE</strong> per indicare che i dati non sono validi.<br/> Tipo variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>FALSE</strong><br/></td>
</tr>

<tr class="odd">
<td ><span id="UIA_IsDialogPropertyId"></span><span id="uia_isdialogpropertyid"></span><span id="UIA_ISDIALOGPROPERTYID"></span><dl> <dt><strong>UIA_IsDialogPropertyId</strong></dt> <dt>30174</dt> </dl></td>
<td >Identifica la <strong>proprietà IsDialog,</strong> ovvero un valore booleano che indica se l'elemento di automazione è una finestra di dialogo. Ad esempio, assistive technology ad esempio le utilità per la lettura dello schermo pronunciano in genere il titolo della finestra di dialogo, il controllo con lo stato attivo nella finestra di dialogo e quindi il contenuto della finestra di dialogo fino al controllo con lo stato attivo ( Salvare le modifiche prima di &quot; chiudere &quot; ). Per le finestre standard, un'utilità per la lettura dello schermo in genere pronuncia il titolo della finestra seguito dal controllo con lo stato attivo. La <strong>proprietà IsDialog</strong> può essere impostata su <strong>TRUE</strong> per indicare che l'applicazione client deve considerare l'elemento come finestra di dialogo.<br/> Tipo variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>FALSE</strong><br/></td>
</tr>

<tr class="even">
<td ><span id="UIA_IsEnabledPropertyId"></span><span id="uia_isenabledpropertyid"></span><span id="UIA_ISENABLEDPROPERTYID"></span><dl> <dt><strong>UIA_IsEnabledPropertyId</strong></dt> <dt>30010</dt> </dl></td>
<td >Identifica la <strong>proprietà IsEnabled,</strong> che è un valore booleano che indica se l'elemento dell'interfaccia utente a cui fa riferimento l'elemento di automazione è abilitato e con cui è possibile interagire.<br/> Quando lo stato abilitato di un controllo è <strong>FALSE,</strong>si presuppone che anche i controlli figlio non siano abilitati. I client non devono prevedere eventi di modifica delle proprietà dagli elementi figlio quando lo stato del controllo padre cambia.<br/> Tipo variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsKeyboardFocusablePropertyId"></span><span id="uia_iskeyboardfocusablepropertyid"></span><span id="UIA_ISKEYBOARDFOCUSABLEPROPERTYID"></span><dl> <dt><strong>UIA_IsKeyboardFocusablePropertyId</strong></dt> <dt>30009</dt> </dl></td>
<td >Identifica la <strong>proprietà IsKeyboardFocusable,</strong> che è un valore booleano che indica se l'elemento di automazione può accettare lo stato attivo della tastiera.<br/> Tipo variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>FALSE</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_IsOffscreenPropertyId"></span><span id="uia_isoffscreenpropertyid"></span><span id="UIA_ISOFFSCREENPROPERTYID"></span><dl> <dt><strong>UIA_IsOffscreenPropertyId</strong></dt> <dt>30022</dt> </dl></td>
<td >Identifica la proprietà <strong>IsOffscreen,</strong> che è un valore booleano che indica se l'elemento di automazione viene interamente scorrendo all'esterno della visualizzazione (ad esempio, un elemento in una casella di riepilogo esterna al riquadro di visualizzazione dell'oggetto contenitore) o compresso fuori visualizzazione (ad esempio, un elemento in una visualizzazione struttura ad albero o in un menu o in una finestra ridotta a icona). Se l'elemento ha un punto selezionabile che può fare in modo che riceva lo stato attivo, l'elemento viene considerato sullo schermo mentre una parte dell'elemento è fuori schermo.<br/> Il valore della proprietà non è influenzato dall'occlusione da altre finestre o dal fatto che l'elemento sia visibile su un monitor specifico.<br/> Se la <strong>proprietà IsOffscreen</strong> è <strong>TRUE,</strong>l'elemento dell'interfaccia utente viene scorrendo fuori dalla schermata o compresso. L'elemento è temporaneamente nascosto, ma rimane nella percezione dell'utente finale e continua a essere incluso nel modello di interfaccia utente. È possibile visualizzare nuovamente l'oggetto scorrendo, facendo clic su un elenco a discesa e così via.<br/> Gli oggetti che l'utente finale non considera affatto o che sono nascosti a livello di codice (ad esempio, una finestra di dialogo che è stata chiusa, ma che l'oggetto sottostante è ancora memorizzato nella cache dall'applicazione) non devono essere prima nell'albero degli elementi di automazione (invece di impostare lo stato di &quot; &quot; <strong>IsOffscreen</strong> su <strong>TRUE).</strong><br/> Tipo variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsPasswordPropertyId"></span><span id="uia_ispasswordpropertyid"></span><span id="UIA_ISPASSWORDPROPERTYID"></span><dl> <dt><strong>UIA_IsPasswordPropertyId</strong></dt> <dt>30019</dt> </dl></td>
<td >Identifica la <strong>proprietà IsPassword,</strong> ovvero un valore booleano che indica se l'elemento di automazione contiene contenuto protetto o una password.<br/> Quando la <strong>proprietà IsPassword</strong> è <strong>TRUE</strong> e l'elemento ha lo stato attivo della tastiera, un'applicazione client deve disabilitare l'eco della tastiera o il feedback di input della tastiera che potrebbe esporre le informazioni protette dell'utente. Il tentativo di accedere alla <strong>proprietà Value</strong> dell'elemento protetto (controllo di modifica) può causare un errore.<br/> Tipo variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>FALSE</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_IsPeripheralPropertyId"></span><span id="uia_isperipheralpropertyid"></span><span id="UIA_ISPERIPHERALPROPERTYID"></span><dl> <dt><strong>UIA_IsPeripheralPropertyId</strong></dt> <dt>30150</dt> </dl></td>
<td >Identifica la <strong>proprietà IsPeripheral,</strong> ovvero un valore booleano che indica se l'elemento di automazione rappresenta l'interfaccia utente periferica. L'interfaccia utente periferica viene visualizzata e supporta l'interazione dell'utente, ma non accetta lo stato attivo della tastiera quando viene visualizzata. Esempi di interfaccia utente periferica includono popup, riquadri a comparsa, menu di scelta rapida o notifiche mobili. Supportato a partire da Windows 8.1.<br/> Quando la <strong>proprietà IsPeripheral</strong> è <strong>TRUE,</strong>un'applicazione client non può presupporre che lo stato attivo sia stato assunto dall'elemento anche se è attualmente interattivo con la tastiera.<br/> Questa proprietà è pertinente per i tipi di controllo seguenti:<br/>
<ul>
<li><strong>UIA_GroupControlTypeId</strong></li>
<li><strong>UIA_MenuControlTypeId</strong></li>
<li><strong>UIA_PaneControlTypeId</strong></li>
<li><strong>UIA_ToolBarControlTypeId</strong></li>
<li><strong>UIA_ToolTipControlTypeId</strong></li>
<li><strong>UIA_WindowControlTypeId</strong></li>
<li><strong>UIA_CustomControlTypeId</strong></li>
</ul>
Tipo variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsRequiredForFormPropertyId"></span><span id="uia_isrequiredforformpropertyid"></span><span id="UIA_ISREQUIREDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsRequiredForFormPropertyId</strong></dt> <dt>30025</dt> </dl></td>
<td >Identifica la <strong>proprietà IsRequiredForForm,</strong> ovvero un valore booleano che indica se l'elemento di automazione deve essere compilato in un modulo.<br/> Tipo variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>FALSE</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ItemStatusPropertyId"></span><span id="uia_itemstatuspropertyid"></span><span id="UIA_ITEMSTATUSPROPERTYID"></span><dl> <dt><strong>UIA_ItemStatusPropertyId</strong></dt> <dt>30026</dt> </dl></td>
<td >Identifica la <strong>proprietà ItemStatus,</strong> ovvero una stringa di testo che descrive lo stato di un elemento dell'elemento di automazione.<br/> <strong>ItemStatus</strong> consente a un client di determinare se un elemento comunica lo stato di un elemento e lo stato. Ad esempio, un elemento associato a un contatto in un'applicazione di messaggistica potrebbe essere &quot; Occupato &quot; o &quot; &quot; Connesso.<br/> Quando <strong>ItemStatus è supportato,</strong> la stringa deve corrispondere alla lingua dell'interfaccia utente dell'applicazione o alla lingua predefinita dell'interfaccia utente del sistema operativo.<br/> Tipo variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ItemTypePropertyId"></span><span id="uia_itemtypepropertyid"></span><span id="UIA_ITEMTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ItemTypePropertyId</strong></dt> <dt>300021</dt> </dl></td>
<td >Identifica la <strong>proprietà ItemType,</strong> ovvero una stringa di testo che descrive il tipo dell'elemento di automazione.<br/> <strong>ItemType</strong> viene usato per ottenere informazioni sugli elementi in un elenco, in una visualizzazione albero o in una griglia dei dati. Ad esempio, un elemento in una visualizzazione di directory file può essere un &quot; file di documento o una cartella &quot; &quot; &quot; .<br/> Quando <strong>ItemType è supportato,</strong> la stringa deve corrispondere alla lingua dell'interfaccia utente dell'applicazione o alla lingua predefinita dell'interfaccia utente del sistema operativo.<br/> Tipo variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_LabeledByPropertyId"></span><span id="uia_labeledbypropertyid"></span><span id="UIA_LABELEDBYPROPERTYID"></span><dl> <dt><strong>UIA_LabeledByPropertyId</strong></dt> <dt>30018</dt> </dl></td>
<td >Identifica la <strong>proprietà LabeledBy,</strong> ovvero un elemento di automazione che contiene l'etichetta di testo per questo elemento.<br/> Questa proprietà può essere usata per recuperare, ad esempio, l'etichetta di testo statico per una casella combinata.<br/> Tipo variant: <strong>VT_UNKNOWN</strong><br/> Valore predefinito: <strong>NULL</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_LandmarkTypePropertyId"></span><span id="uia_landmarktypepropertyid"></span><span id="UIA_LANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LandmarkTypePropertyId</strong></dt> <dt>30157</dt> </dl></td>
<td >Identifica la <strong>proprietà LandmarkType,</strong> ovvero un <a href="landmark-type-identifiers.md"><strong>identificatore del tipo di punto</strong></a> di riferimento associato a un elemento.<br/> La <strong>proprietà LandmarkType</strong> descrive un elemento che rappresenta un gruppo di elementi. Ad esempio, un punto di riferimento di ricerca può rappresentare un set di controlli correlati per la ricerca.<br/> Se <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> viene <strong>usato,</strong> UIA_LocalizedLandmarkTypePropertyId necessario per descrivere il punto di riferimento personalizzato.<br/> Tipo variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_LevelPropertyId"></span><span id="uia_levelpropertyid"></span><span id="UIA_LEVELPROPERTYID"></span><dl> <dt><strong>UIA_LevelPropertyId</strong></dt> <dt>30154</dt> </dl></td>
<td >Identifica la <strong>proprietà Level,</strong> ovvero un intero in base 1 associato a un elemento di automazione.<br/> La <strong>proprietà Level</strong> descrive la posizione di un elemento all'interno di strutture gerarchiche gerarchiche o interrotte. Ad esempio, un elenco puntato/numerato, intestazioni o altri elementi di dati strutturati possono avere varie relazioni padre/figlio. <strong>Level</strong> descrive dove si trova l'elemento nella struttura.<br/> È consigliabile usare il <a href="/windows/desktop/WinAuto/uiauto-implementingcustomnavigation">pattern di controllo CustomNavigation</a> in tandem con <strong>Level</strong>.<br/> Tipo variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_LiveSettingPropertyId"></span><span id="uia_livesettingpropertyid"></span><span id="UIA_LIVESETTINGPROPERTYID"></span><dl> <dt><strong>UIA_LiveSettingPropertyId</strong></dt> <dt>30135</dt> </dl></td>
<td >Identifica la <strong>proprietà LiveSetting,</strong> supportata da un elemento di automazione che rappresenta un'area in tempo reale. La <strong>proprietà LiveSetting</strong> indica il livello di cortesia che un client deve usare per notificare all'utente le &quot; modifiche apportate &quot; all'area in tempo reale. Questa proprietà può essere uno dei valori <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-livesetting"><strong>dell'enumerazione LiveSetting.</strong></a> Supportato a partire da Windows 8.<br/> Tipo variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_LocalizedControlTypePropertyId"></span><span id="uia_localizedcontroltypepropertyid"></span><span id="UIA_LOCALIZEDCONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedControlTypePropertyId</strong></dt> <dt>30004</dt> </dl></td>
<td >Identifica la <strong>proprietà LocalizedControlType,</strong> ovvero una stringa di testo che descrive il tipo di controllo rappresentato dall'elemento di automazione. La stringa deve contenere solo caratteri minuscoli:
<ul>
<li>Pulsante &quot; Correggi:&quot;</li>
<li>Non corretto: &quot; pulsante&quot;</li>
</ul>
<br/> Quando <strong>LocalizedControlType</strong> non viene specificato dal provider di elementi, la stringa localizzata predefinita viene fornita dal framework, in base al tipo di controllo dell'elemento , ad esempio button per il &quot; tipo di controllo &quot; <a href="uiauto-supportbuttoncontroltype.md">Button.</a> Un elemento di <strong></strong> automazione con il tipo di controllo Custom deve supportare una stringa di tipo controllo localizzata che rappresenta il ruolo dell'elemento , ad esempio la selezione colori per un controllo personalizzato che consente agli utenti di scegliere e specificare i &quot; &quot; colori.<br/> Quando viene fornito un valore personalizzato, la stringa deve corrispondere alla lingua dell'interfaccia utente dell'applicazione o alla lingua predefinita dell'interfaccia utente del sistema operativo.<br/> Tipo variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_LocalizedLandmarkTypePropertyId"></span><span id="uia_localizedlandmarktypepropertyid"></span><span id="UIA_LOCALIZEDLANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedLandmarkTypePropertyId</strong></dt> <dt>30158</dt> </dl></td>
<td >Identifica <strong>LocalizedLandmarkType,</strong>ovvero una stringa di testo che descrive il tipo di punto di riferimento rappresentato dall'elemento di automazione.<br/> Deve essere usato in tandem con <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId,</strong></a> tuttavia <strong>LocalizedLandmarkType</strong> deve sempre avere la precedenza su <strong>LandmarkType</strong> e deve essere usato per descrivere il punto di riferimento prima <strong>di LandmarkType.</strong><br/> La stringa deve corrispondere alla lingua dell'interfaccia utente dell'applicazione o alla lingua predefinita dell'interfaccia utente del sistema operativo.<br/> Tipo variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_NamePropertyId"></span><span id="uia_namepropertyid"></span><span id="UIA_NAMEPROPERTYID"></span><dl> <dt><strong>UIA_NamePropertyId</strong></dt> <dt>30005</dt> </dl></td>
<td >Identifica la <strong>proprietà Name,</strong> ovvero una stringa che contiene il nome dell'elemento di automazione.<br/> La <strong>proprietà Name</strong> deve essere uguale al testo dell'etichetta sullo schermo. Ad esempio, <strong>Il nome</strong> deve essere &quot; Sfoglia per un elemento pulsante con &quot; l'etichetta &quot; Sfoglia &quot; . La <strong>proprietà Name</strong> non deve includere il carattere mnemotico per i tasti di scelta , ovvero , sottolineati nella presentazione del testo &quot; & &quot; dell'interfaccia utente. Inoltre, la proprietà <strong>Name</strong> non deve essere una versione estesa o modificata dell'etichetta sullo schermo perché l'incoerenza tra il nome e l'etichetta può causare confusione tra le applicazioni client e gli utenti.<br/> Quando il testo dell'etichetta corrispondente non è visibile sullo schermo o quando viene sostituito da grafica, è necessario scegliere testo alternativo. Il testo alternativo deve essere conciso, intuitivo e localizzato nella lingua dell'interfaccia utente dell'applicazione o nella lingua predefinita dell'interfaccia utente del sistema operativo. Il testo alternativo non deve essere una descrizione dettagliata dei dettagli visivi, ma una descrizione concisa della funzione o della funzionalità dell'interfaccia utente come se fosse etichettata con testo semplice. Ad esempio, il Windows menu Start pulsante è denominato Start (pulsante) anziché Windows logo sulla grafica a sfera tonda &quot; &quot; blu &quot; &quot; (pulsante). Per altre informazioni, vedere <a href="/previous-versions/windows/desktop/dnacc/creating-text-equivalents-for-images">Creazione di equivalenti di testo per immagini</a>.<br/> Quando un'etichetta dell'interfaccia utente usa elementi grafici di testo (ad esempio, l'uso di per un pulsante che aggiunge un elemento da sinistra a destra), la proprietà Name deve essere sostituita da un'alternativa di testo appropriata &quot; >> &quot; (ad esempio, Aggiungi <strong></strong> &quot; &quot; ). Tuttavia, la pratica di usare la grafica di testo come etichetta dell'interfaccia utente è sconsigliata a causa di problemi di localizzazione e accessibilità.<br/> La proprietà <strong>Name</strong> non deve includere il ruolo del controllo o le informazioni sul tipo, ad esempio pulsante o elenco. In caso contrario, sarà in conflitto con il testo della proprietà &quot; &quot; &quot; &quot; <strong>LocalizedControlType</strong> quando queste due proprietà vengono aggiunte (molte tecnologie di assistive esistenti a tale scopo).<br/> La <strong>proprietà Name</strong> non può essere usata come identificatore univoco tra gli elementi di pari livello. Tuttavia, purché sia coerente con la presentazione dell'interfaccia utente, lo stesso valore <strong>Name</strong> può essere supportato tra peer. Per l'automazione di test, i client devono prendere in considerazione l'uso <strong>della proprietà AutomationId</strong> <strong>o RuntimeId.</strong><br/> I controlli di testo non devono sempre avere la proprietà <strong>Name</strong> identica al testo <strong></strong> visualizzato all'interno del controllo, purché sia supportato anche il modello Text.<br/> Tipo variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_NativeWindowHandlePropertyId"></span><span id="uia_nativewindowhandlepropertyid"></span><span id="UIA_NATIVEWINDOWHANDLEPROPERTYID"></span><dl> <dt><strong>UIA_NativeWindowHandlePropertyId</strong></dt> <dt>30020</dt> </dl></td>
<td >Identifica la <strong>proprietà NativeWindowHandle,</strong> che è un intero che rappresenta l'handle (<strong>HWND</strong>) della finestra dell'elemento di automazione, se presente; In caso contrario, questa proprietà è 0.<br/> Tipo variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_OptimizeForVisualContentPropertyId"></span><span id="uia_optimizeforvisualcontentpropertyid"></span><span id="UIA_OPTIMIZEFORVISUALCONTENTPROPERTYID"></span><dl> <dt><strong>UIA_OptimizeForVisualContentPropertyId</strong></dt> <dt>30111</dt> </dl></td>
<td >Identifica la <strong>proprietà OptimizeForVisualContent,</strong> che è un valore booleano che indica se il provider espone solo gli elementi visibili. Un provider può usare questa proprietà per ottimizzare le prestazioni quando si lavora con parti di contenuto molto grandi. Ad esempio, quando l'utente passa attraverso una parte di contenuto di grandi dimensioni, il provider può eliminare gli elementi di contenuto che non sono più visibili. Quando un elemento di contenuto viene eliminato, il provider deve restituire il UIA_E_ELEMENTNOTAVAILABLE <strong>di</strong> errore. Supportato a partire da Windows 8.<br/> Tipo variant: <strong>VT_BOOL</strong><br/> Valore predefinito: <strong>FALSE</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_OrientationPropertyId"></span><span id="uia_orientationpropertyid"></span><span id="UIA_ORIENTATIONPROPERTYID"></span><dl> <dt><strong>UIA_OrientationPropertyId</strong></dt> <dt>300023</dt> </dl></td>
<td >Identifica la <strong>proprietà Orientation,</strong> che indica l'orientamento del controllo rappresentato dall'elemento di automazione. La proprietà viene espressa come valore del <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>tipo enumerato OrientationType.</strong></a><br/> La <strong>proprietà Orientation</strong> è supportata dai controlli, ad esempio barre di scorrimento e dispositivi di scorrimento, che possono avere un orientamento verticale o orizzontale. In caso contrario, può sempre <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>essere OrientationType_None</strong></a>, il che significa che il controllo non ha orientamento.<br/> Tipo variant: <strong>VT_I4</strong><br/> Valore predefinito: 0 (<a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>)<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_OutlineColorPropertyId"></span><span id="uia_outlinecolorpropertyid"></span><span id="UIA_OUTLINECOLORPROPERTYID"></span><dl> <dt><strong>UIA_OutlineColorPropertyId</strong></dt> <dt>30161</dt> </dl></td>
<td >Identifica la <strong>proprietà OutlineColor,</strong> che specifica il colore utilizzato per la struttura dell'elemento di automazione. Questo attributo viene specificato come <strong>COLORREF,</strong>un valore a 32 bit usato per specificare un colore RGB o RGBA.<br/> Tipo variant: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_OutlineThicknessPropertyId"></span><span id="uia_outlinethicknesspropertyid"></span><span id="UIA_OUTLINETHICKNESSPROPERTYID"></span><dl> <dt><strong>UIA_OutlineThicknessPropertyId</strong></dt> <dt>30164</dt> </dl></td>
<td >Identifica la <strong>proprietà OutlineThickness,</strong> che specifica la larghezza per la struttura dell'elemento di automazione.<br/> Tipo variant: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_PositionInSetPropertyId"></span><span id="uia_positioninsetpropertyid"></span><span id="UIA_POSITIONINSETPROPERTYID"></span><dl> <dt><strong>UIA_PositionInSetPropertyId</strong></dt> <dt>30152</dt> </dl></td>
<td >Identifica la <strong>proprietà PositionInSet,</strong> ovvero un intero in base 1 associato a un elemento di automazione. <strong>PositionInSet</strong> descrive la posizione ordinale dell'elemento all'interno di un set di elementi considerati elementi di pari livello.<br/> <strong>PositionInSet</strong> funziona in coordinamento con la <strong>proprietà SizeOfSet</strong> per descrivere la posizione ordinale nel set.<br/> Tipo variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ProcessIdPropertyId"></span><span id="uia_processidpropertyid"></span><span id="UIA_PROCESSIDPROPERTYID"></span><dl> <dt><strong>UIA_ProcessIdPropertyId</strong></dt> <dt>30002</dt> </dl></td>
<td >Identifica la <strong>proprietà ProcessId,</strong> ovvero un intero che rappresenta l'identificatore (ID) del processo dell'elemento di automazione.<br/> L'identificatore di processo (ID) viene assegnato dal sistema operativo. Può essere visualizzato nella colonna <strong>PID</strong> della <strong>scheda</strong> Processi in Gestione attività.<br/> Tipo variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ProviderDescriptionPropertyId"></span><span id="uia_providerdescriptionpropertyid"></span><span id="UIA_PROVIDERDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_ProviderDescriptionPropertyId</strong></dt> <dt>30107</dt> </dl></td>
<td >Identifica la <strong>proprietà ProviderDescription,</strong> ovvero una stringa formattata contenente le informazioni di origine del provider Automazione interfaccia utente per l'elemento di automazione, incluse le informazioni sul proxy.<br/> Tipo variant: <strong>VT_BSTR</strong><br/> Valore predefinito: stringa vuota<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_RotationPropertyId"></span><span id="uia_rotationpropertyid"></span><span id="UIA_ROTATIONPROPERTYID"></span><dl> <dt><strong>UIA_RotationPropertyId</strong></dt> <dt>30166</dt> </dl></td>
<td >Identifica la <strong>proprietà Rotation,</strong> che specifica l'angolo di rotazione in unità non specificate.<br/> Tipo variant: <strong>VT_R8</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_RuntimeIdPropertyId"></span><span id="uia_runtimeidpropertyid"></span><span id="UIA_RUNTIMEIDPROPERTYID"></span><dl> <dt><strong>UIA_RuntimeIdPropertyId</strong></dt> <dt>30000</dt> </dl></td>
<td >Identifica la <strong>proprietà RuntimeId,</strong> ovvero una matrice di interi che rappresenta l'identificatore per un elemento di automazione.<br/> L'identificatore è univoco sul desktop, ma è garantito che sia univoco solo all'interno dell'interfaccia utente del desktop in cui è stato generato. Gli identificatori possono essere riutilizzati nel tempo.<br/> Il formato di <strong>RuntimeId</strong> può cambiare. L'identificatore restituito deve essere considerato come un valore opaco e usato solo per il confronto. ad esempio per determinare se un elemento di automazione si trova nella cache.<br/> Tipo variant: <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_SizePropertyId"></span><span id="uia_sizepropertyid"></span><span id="UIA_SIZEPROPERTYID"></span><dl> <dt><strong>UIA_SizePropertyId</strong></dt> <dt>30167</dt> </dl></td>
<td >Identifica la <strong>proprietà Size,</strong> che specifica la larghezza e l'altezza dell'elemento di automazione.<br/> Tipo variant: <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valore predefinito: <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_SizeOfSetPropertyId"></span><span id="uia_sizeofsetpropertyid"></span><span id="UIA_SIZEOFSETPROPERTYID"></span><dl> <dt><strong>UIA_SizeOfSetPropertyId</strong></dt> <dt>30153</dt> </dl></td>
<td >Identifica la <strong>proprietà SizeOfSet,</strong> ovvero un intero in base 1 associato a un elemento di automazione. <strong>SizeOfSet</strong> descrive il numero di elementi di automazione in un gruppo o in un set considerati elementi di pari livello.<br/> <strong>SizeOfSet</strong> funziona in coordinamento con la <strong>proprietà PositionInSet</strong> per descrivere il conteggio degli elementi nel set.<br/> Tipo variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_VisualEffectsPropertyId"></span><span id="uia_visualeffectspropertyid"></span><span id="UIA_VISUALEFFECTSPROPERTYID"></span><dl> <dt><strong>UIA_VisualEffectsPropertyId</strong></dt> <dt>30163</dt> </dl></td>
<td >Identifica la <strong>proprietà VisualEffects,</strong> ovvero un campo di bit che specifica gli effetti sull'elemento di automazione, ad esempio ombreggiatura, reflection, alone, bordi sfumati o smussatura.<br/> Oggetti Visivi:<br/>
<ul>
<li>VisualEffects_Shadow: 0x1</li>
<li>VisualEffects_Reflection: 0x2</li>
<li>VisualEffects_Glow: 0x4</li>
<li>VisualEffects_SoftEdges: 0x8</li>
<li>VisualEffects_Bevel: 0x10</li>
</ul>
Tipo variant: <strong>VT_I4</strong><br/> Valore predefinito: 0<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App \[ UWP per app desktop \| XP\]<br/>                                              |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2003 \[ \|\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>UIAutomationClient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sulle proprietà di automazione interfaccia utente](uiauto-propertiesoverview.md)
</dt> <dt>

[Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md)
</dt> </dl>
