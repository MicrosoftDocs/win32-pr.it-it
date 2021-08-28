---
title: Tipo di controllo SemanticZoom
description: In questo argomento vengono fornite informazioni Automazione interfaccia utente supporto per il tipo di controllo SemanticZoom.
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- Automazione interfaccia utente,supporto per il tipo di controllo SemanticZoom
- Automazione interfaccia utente, tipo di controllo SemanticZoom
- Automazione interfaccia utente,struttura ad albero per il tipo di controllo SemanticZoom
- Automazione interfaccia utente,proprietà per il tipo di controllo SemanticZoom
- Automazione interfaccia utente,pattern di controllo per il tipo di controllo SemanticZoom
- Automazione interfaccia utente,eventi per il tipo di controllo SemanticZoom
- strutture ad albero, tipo di controllo SemanticZoom
- proprietà, tipo di controllo SemanticZoom
- pattern di controllo, tipo di controllo SemanticZoom
- eventi, tipo di controllo SemanticZoom
- supporto per il tipo di controllo SemanticZoom
- Tipo di controllo SemanticZoom
- tipi di controllo, struttura ad albero per il tipo di controllo SemanticZoom
- tipi di controllo, pattern di controllo per il tipo di controllo SemanticZoom
- tipi di controllo, supporto per SemanticZoom
- tipi di controllo, SemanticZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9673c5e9beb0c78ecc7dfccc10b6716d6d3afa3f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467758"
---
# <a name="semanticzoom-control-type"></a>Tipo di controllo SemanticZoom

Questo argomento fornisce informazioni sul supporto Automazione interfaccia utente per il **tipo di controllo SemanticZoom.**

Lo zoom semantico è una tecnica introdotta in Windows 8 per la presentazione e l'esplorazione di grandi set di dati correlati o contenuto all'interno di una singola visualizzazione, ad esempio un album di foto, un elenco di app o una rubrica. Lo zoom semantico usa due modalità distinte di classificazione, o *livelli di zoom,* per organizzare e presentare il contenuto. La modalità di basso livello *(o ingrandita)* visualizza gli elementi in una struttura semplice e "all-up"; e la modalità di alto livello (o *ingrandita)* visualizza gli elementi in gruppi, consentendo all'utente di spostarsi rapidamente ed esplorare il contenuto. Ad esempio, lo zoom di un elenco di città potrebbe cambiare in un elenco di stati contenenti tali città. Lo zoom di un elenco di programmi può cambiare in un elenco di gruppi di programmi logici.

Per altre informazioni sullo zoom semantico usato in modo specifico per le Windows Store, vedere [Linee guida per lo zoom semantico.](/windows/uwp/controls-and-patterns/semantic-zoom)

Il modello di utilizzo per il **tipo di controllo SemanticZoom** è insolito perché esiste principalmente per l'accesso a livello di codice. Microsoft Automazione interfaccia utente client possono monitorare e modificare il controllo Zoom semantico per controllare lo stato ingrandito dell'elenco. Gli utenti che non usano assistive technology in genere manipolano il controllo Zoom semantico direttamente tramite movimenti tocco o tasti di scelta rapida.

Nelle sezioni seguenti vengono definiti i Automazione interfaccia utente struttura ad albero, le proprietà, i pattern di controllo e gli eventi per il tipo di controllo **SemanticZoom.** I Automazione interfaccia utente si applicano a tutti i controlli zoom semantico in cui il framework o la piattaforma dell'interfaccia utente si integra Automazione interfaccia utente per i tipi di controllo e i pattern di controllo.

In questo argomento sono contenute le sezioni seguenti.

-   [Struttura ad albero tipica](#typical-tree-structure)
-   [Proprietà rilevanti](#relevant-properties)
-   [Proprietà e pattern di controllo obbligatori](#required-control-patterns-and-properties)
-   [Eventi obbligatori](#required-events)
-   [Osservazioni:](#remarks)
-   [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

La tabella seguente illustra un controllo tipico e una visualizzazione contenuto dell'albero Automazione interfaccia utente relativo al tipo di controllo **SemanticZoom** e descrive cosa può essere contenuto in ogni visualizzazione. Per altre informazioni sull'albero Automazione interfaccia utente, vedere Automazione interfaccia utente [Tree Overview](uiauto-treeoverview.md).




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>Elenco<ul><li>[SemanticZoom]<ul><li>ListItem (0 o più)</li></ul></li></ul></li></ul> | <ul><li>Elenco<ul><li>ListItem (0 o più)</li></ul></li></ul> | 




 

Oppure:




| Visualizzazione controlli | Visualizzazione contenuto | 
|--------------|--------------|
| <ul><li>[SemanticZoom]<ul><li>Elenco<ul><li>ListItem (0 o più)</li></ul></li></ul></li></ul> | <ul><li>Elenco<ul><li>ListItem (0 o più)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le Automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli che implementano il tipo di controllo **SemanticZoom.** Per altre informazioni sulle Automazione interfaccia utente, vedere [Recupero di proprietà da Automazione interfaccia utente elementi](uiauto-propertiesforclients.md).




| Proprietà di automazione interfaccia utente | valore | Note | 
|------------------------|-------|-------|
| <a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a> | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata dell'Automazione interfaccia utente albero. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a> | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a> | Vedere le note. | Se il controllo elenco ha un punto selezionabile (un punto su cui è possibile fare clic per fare in modo che l'elenco abbia lo stato attivo), tale punto deve essere esposto tramite questa proprietà. Se il valore della proprietà <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> è <strong>TRUE,</strong>il tentativo di recuperare questa proprietà comporta l'UIA_E_NOCLICKABLEPOINT errore. <a href="uiauto-error-codes.md"><strong></strong></a> | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a> | <strong>SemanticZoom</strong> | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a> | true | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a> | true | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a> | FALSE | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a> | Vedere le note. | Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento a tale controllo. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a> | Vedere le note. | Stringa localizzata corrispondente al tipo <strong>di controllo SemanticZoom.</strong> Il valore predefinito è "zoom semantico" per en-US o inglese (Stati Uniti).<blockquote>[!Note]<br />Alcuni framework lo concatenavano come "semanticzoom".</blockquote><br /> | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a> | Vedere le note. | Una stringa vuota è accettabile o è possibile specificare un nome più utile, a condizione che non contenga il termine zoom semantico , che potrebbe generare confusione nella combinazione di tipo di controllo e nome. | 




 

## <a name="required-control-patterns-and-properties"></a>Proprietà e pattern di controllo obbligatori

Nella tabella seguente sono elencati Automazione interfaccia utente i pattern di controllo che devono essere supportati da tutti i controlli zoom semantico. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).



| Pattern di controllo/proprietà del pattern                  | Supporto/valore | Note                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Dipende da       | I controlli Zoom semantico [supportano il](uiauto-implementingtoggle.md) pattern di controllo Toggle per consentire l'a attivazione o la disattivazione dello zoom. [**ToggleState \_ Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corrisponde allo stato flat, all-up e [**ToggleState \_ On**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corrisponde alla visualizzazione ingrandita di alto livello. |



 

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli Automazione interfaccia utente che i controlli Zoom semantico devono supportare. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).



| Automazione interfaccia utente eventi                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**Interfaccia \_ utente Evento di modifica della proprietà BoundingRectanglePropertyId.**](uiauto-automation-element-propids.md) |                                                                                                                            |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsEnabledPropertyId.**](uiauto-automation-element-propids.md)                 | Se il controllo supporta la [**proprietà IsEnabled,**](uiauto-automation-element-propids.md) deve supportare questo evento.   |
| [**Interfaccia \_ utente Evento di modifica della proprietà IsOffscreenPropertyId.**](uiauto-automation-element-propids.md)             | Se il controllo supporta la [**proprietà IsOffscreen,**](uiauto-automation-element-propids.md) deve supportare questo evento. |
| [**Interfaccia \_ utente Evento di modifica della proprietà ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)    |                                                                                                                            |



 

## <a name="remarks"></a>Commenti

Se un'interfaccia utente ha un pulsante visibile per attivare o disattivare il comportamento del controllo Zoom semantico, questo pulsante non deve avere un tipo di controllo **SemanticZoom.** Si tratta di un'operazione contro intuitiva, ma il tipo di controllo **SemanticZoom** caratterizza il contenitore del contenuto di zoom, non un pulsante che controlla lo zoom. Un pulsante di questo tipo può essere rappresentato semplicemente come tipo [di controllo Button](uiauto-supportbuttoncontroltype.md) con il pattern di controllo [Toggle.](uiauto-implementingtoggle.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
</dt> </dl>

 

