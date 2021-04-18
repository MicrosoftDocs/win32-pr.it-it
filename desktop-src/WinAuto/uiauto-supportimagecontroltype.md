---
title: Tipo di controllo Image
description: In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo Image.
ms.assetid: 439c708c-4fb4-481b-a2ff-3816d649f3ff
keywords:
- Automazione interfaccia utente, supporto per il tipo di controllo Image
- Automazione interfaccia utente, tipo di controllo Image
- Automazione interfaccia utente, struttura ad albero per il tipo di controllo Image
- Automazione interfaccia utente, proprietà per il tipo di controllo Image
- Automazione interfaccia utente, pattern di controllo per il tipo di controllo Image
- Automazione interfaccia utente, eventi per il tipo di controllo Image
- strutture ad albero, tipo di controllo Image
- Proprietà, tipo di controllo Image
- pattern di controllo, tipo di controllo Image
- eventi, tipo di controllo Image
- supporto per il tipo di controllo Image
- Image (tipo di controllo)
- tipi di controllo, struttura ad albero per il tipo di controllo Image
- tipi di controllo, pattern di controllo per il tipo di controllo Image
- tipi di controllo, supporto per l'immagine
- tipi di controllo, immagine
ms.topic: article
ms.date: 10/08/2019
ms.openlocfilehash: b91d55bf8e21813e180476146625172e3eab1a6d
ms.sourcegitcommit: da8cc3fb3c9f14cb768855502a2b6815ddee13b6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/10/2019
ms.locfileid: "106299005"
---
# <a name="image-control-type"></a>Tipo di controllo Image

In questo argomento vengono fornite informazioni sul supporto di automazione interfaccia utente Microsoft per il tipo di controllo **Image** .

I controlli immagine usati come icone, grafica informativa e grafici supportano il tipo di controllo **Image** . I controlli usati come immagini di sfondo o filigrana non supportano il tipo di controllo **Image** .

Nelle sezioni seguenti vengono definiti la struttura ad albero, le proprietà, i pattern di controllo e gli eventi di automazione interfaccia utente necessari per il tipo di controllo **Image** . I requisiti di automazione interfaccia utente si applicano a tutti i controlli immagine in cui la piattaforma/Framework dell'interfaccia utente integra il supporto di automazione interfaccia utente per i tipi di controllo e i pattern

In questo argomento sono contenute le sezioni seguenti.

- [Struttura ad albero tipica](#typical-tree-structure)
- [Proprietà rilevanti](#relevant-properties)
- [Pattern di controllo obbligatori](#required-control-patterns)
- [Eventi obbligatori](#required-events)
- [Argomenti correlati](#related-topics)

## <a name="typical-tree-structure"></a>Struttura ad albero tipica

Nella tabella seguente viene illustrata una tipica visualizzazione del controllo e del contenuto dell'albero di automazione interfaccia utente relativo ai controlli immagine e viene descritto il possibile contenuto di ogni visualizzazione. Per altre informazioni sull'albero di automazione interfaccia utente, vedere [Cenni preliminari sull'albero di automazione interfaccia utente](uiauto-treeoverview.md).

| Visualizzazione controlli | Visualizzazione contenuto |
| ------------ | ------------ |
| Immagine | Image (a seconda che l'immagine contenga informazioni, in base al valore della proprietà [identificatori di proprietà degli elementi di automazione](uiauto-automation-element-propids.md) ) |

## <a name="relevant-properties"></a>Proprietà rilevanti

La tabella seguente elenca le proprietà di automazione interfaccia utente il cui valore o la cui definizione è particolarmente rilevante per i controlli immagine. Per altre informazioni sulle proprietà di automazione interfaccia utente, vedere [recupero di proprietà da elementi di automazione interfaccia utente](uiauto-propertiesforclients.md).

| Proprietà di automazione interfaccia utente                                                                                              | Valore      | Note                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONIDPROPERTYID UIA**](uiauto-automation-element-propids.md)                 | Vedere le note. | Il valore di questa proprietà deve essere univoco tra tutti gli elementi peer nella visualizzazione non elaborata della struttura ad albero di automazione interfaccia utente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)       | Vedere le note. | Il rettangolo più esterno che contiene l'intero controllo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)             | Vedere le note. | Il punto selezionabile del controllo immagine deve essere un punto all'interno del rettangolo di delimitazione del controllo immagine.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**\_CONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md)                   | **Immagine**  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**\_HELPTEXTPROPERTYID UIA**](uiauto-automation-element-propids.md)                         | Vedere le note. | La proprietà **HelpText** espone una stringa localizzata che descrive l'aspetto visivo effettivo del controllo o altre informazioni sulla descrizione comandi associate all'immagine. Questa proprietà deve essere supportata quando è necessaria una descrizione estesa per fornire ulteriori informazioni sul controllo immagine, ad esempio se l'immagine è un grafico o un diagramma complesso. Questa proprietà esegue il mapping al tag HTML **longdesc** e al tag **desc** Scalable Vector Graphics (SVG). Gli strumenti di sviluppo che usano i controlli immagine devono supportare una proprietà che consenta la descrizione visiva da impostare per il controllo. È necessario eseguire il mapping di questa proprietà alla proprietà **VisualDescription** di automazione interfaccia utente. |
| [**\_ISCONTENTELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | Vedere le note. | Il controllo immagine deve essere incluso nella visualizzazione contenuto dell'albero di automazione interfaccia utente quando contiene informazioni significative non ancora esposte all'utente finale.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**\_ISCONTROLELEMENTPROPERTYID UIA**](uiauto-automation-element-propids.md)         | true       | Il controllo immagine viene sempre incluso nella visualizzazione controlli dell'albero di automazione interfaccia utente.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)   | Vedere le note. | Se il controllo può ricevere lo stato attivo, deve supportare questa proprietà.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**\_ITEMSTATUSPROPERTYID UIA**](uiauto-automation-element-propids.md)                     | Vedere le note. | Se il controllo immagine rappresenta le informazioni sullo stato relative a un particolare elemento sullo schermo, il controllo deve essere contenuto all'interno dell'elemento. Quando l'immagine è contenuta all'interno di un elemento, l'elemento deve supportare la proprietà Status e generare le notifiche appropriate quando lo stato cambia. Se un'immagine è un controllo autonomo che visualizza lo stato, questa proprietà deve essere supportata.                                                                                                                                                                                                                                                                                    |
| [**\_LABELEDBYPROPERTYID UIA**](uiauto-automation-element-propids.md)                       | Vedere le note. | Se è presente un'etichetta di testo statico, questa proprietà deve esporre un riferimento a tale controllo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**\_LOCALIZEDCONTROLTYPEPROPERTYID UIA**](uiauto-automation-element-propids.md) | Vedere le note. | Stringa localizzata corrispondente al tipo di controllo **Image** . Il valore predefinito è "image" per en-US o inglese (Stati Uniti).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)                                 | Vedere le note. | La proprietà **Name** deve essere esposta per tutti i controlli immagine che contengono informazioni. L'accesso a livello di codice a queste informazioni richiede che venga specificato un equivalente testuale dell'immagine. Se il controllo immagine è puramente decorativo, deve essere visualizzato solo nella visualizzazione controlli dell'albero di automazione interfaccia utente e non deve necessariamente avere un nome (vedere la [sezione Osservazioni](#remarks)). I framework dell'interfaccia utente devono supportare una proprietà ALT o testo alternativo sulle immagini, in grado di essere impostata dall'interno del relativo framework. Questa proprietà verrà quindi mappata alla proprietà del nome di automazione interfaccia utente.                                                                                                                                                     |

## <a name="required-control-patterns"></a>Pattern di controllo obbligatori

La tabella seguente elenca i pattern di controllo di automazione interfaccia utente che devono essere supportati per i controlli immagine. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

| Pattern di controllo                                                 | Supporto | Note                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)           | Dipende da | Il controllo immagine supporta il pattern di controllo [GridItem](uiauto-implementinggriditem.md) se il controllo si trova all'interno di un contenitore della griglia.                                                                                                                                                                                                                                                                                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | Mai   | Se il controllo immagine è un oggetto selezionabile, il controllo deve supportare un tipo di controllo che supporta il pattern di controllo [Invoke](uiauto-implementinginvoke.md) , ad esempio il tipo di controllo [Button](uiauto-supportbuttoncontroltype.md) . Per un oggetto Image che contiene più oggetti selezionabili, l'elemento (tipo di controllo Image) può ospitare collegamenti figlio (tipo di controllo[Hyperlink](uiauto-supporthyperlinkcontroltype.md) ) nell'albero di automazione interfaccia utente. |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | Mai   | I controlli immagine non devono supportare il pattern di controllo [SelectionItem](uiauto-implementingselectionitem.md) . Se le immagini fanno parte di un contenitore selezionabile, ad esempio un pulsante con un'icona di immagine come contenuto, tale contenitore supporta il pattern, non l'immagine all'interno di.                                                                                                                                                                           |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)         | Dipende da | Il controllo immagine supporta il pattern di controllo [TableItem](uiauto-implementingtableitem.md) se il controllo si trova all'interno di un contenitore che dispone di controlli intestazione.                                                                                                                                                                                                                                                                                                |

## <a name="required-events"></a>Eventi obbligatori

La tabella seguente elenca gli eventi di automazione interfaccia utente necessari per supportare i controlli immagine. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).

| Evento di automazione interfaccia utente                                                                                                                   | Note                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**\_AUTOMATIONFOCUSCHANGEDEVENTID UIA**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsEnabledPropertyId.                 | Se il controllo supporta la proprietà [**IsEnabled**](uiauto-automation-element-propids.md) , deve supportare questo evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà IsOffscreenPropertyId.             | Se il controllo supporta la proprietà [**IsOffscreen**](uiauto-automation-element-propids.md) , deve supportare questo evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà ItemStatusPropertyId.               | Se il controllo supporta la proprietà [**ItemStatus**](uiauto-automation-element-propids.md) , deve supportare questo evento.  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento di modifica della proprietà NamePropertyId.                           |                                                                                                                            |
| [**\_STRUCTURECHANGEDEVENTID UIA**](uiauto-event-ids.md)                                                  |                                                                                                                            |

## <a name="remarks"></a>Commenti

Il World Wide Web Consortium (W3C) definisce un'immagine decorativa come una che non aggiunge informazioni al contenuto di una pagina. Per altri dettagli, vedere l'argomento W3C sulle [Immagini decorative](https://www.w3.org/WAI/tutorials/images/decorative/).

Per quanto riguarda l'automazione dell'interfaccia utente:

- Se un'immagine è puramente decorativa, non è interattiva e non trasmette alcuna informazione, l'immagine:
  - Potrebbe o non trovarsi nell'albero di UIA
  - Potrebbe o non trovarsi nella visualizzazione RAW di UIA
  - Non deve trovarsi nella visualizzazione del controllo UIA
  - Non deve trovarsi nella visualizzazione contenuto
  - Potrebbe o non avere un nome
- Se un'immagine trasmette informazioni, ma è presente un testo chiaramente associato che fornisce le stesse informazioni, ad esempio un pulsante Riproduci che contiene una rappresentazione grafica del triangolo verso sinistra e il testo "Play", l'immagine viene considerata decorativa e l'immagine:
  - Deve trovarsi nella visualizzazione non elaborata
  - Deve trovarsi nella visualizzazione controlli
  - Non deve trovarsi nella visualizzazione contenuto
  - È possibile che non abbia un valore nella proprietà Name
  - Il testo che trasmette anche il significato dell'immagine deve trovarsi nella visualizzazione contenuto
- Se un'immagine è informativa e trasmette dettagli non forniti da alcun testo associato, l'immagine:
  - Deve trovarsi nella visualizzazione non elaborata
  - Deve trovarsi nella visualizzazione controlli
  - Deve trovarsi nella visualizzazione contenuto
  - Deve avere un valore di nome che descrive l'immagine e il relativo significato

## <a name="related-topics"></a>Argomenti correlati

### <a name="conceptual"></a>Informazioni concettuali

- [Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
- [Cenni preliminari su automazione interfaccia utente](uiauto-uiautomationoverview.md)
