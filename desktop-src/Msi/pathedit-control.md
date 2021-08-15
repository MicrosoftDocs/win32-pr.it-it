---
description: Il controllo PathEdit visualizza un campo di modifica che consente a un utente di selezionare la sezione finale di un percorso.
ms.assetid: 074ef4d5-3ac1-4bdb-90c5-9798d89a749f
title: Controllo PathEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed7655cc893c30f417c9a7ef374eb6d4ade10dfd618ca328e1be2fc7a0e0a9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377614"
---
# <a name="pathedit-control"></a>Controllo PathEdit

Il controllo PathEdit visualizza un campo di modifica che consente a un utente di selezionare la sezione finale di un percorso. Questo controllo supporta l'immissione del nome della cartella selezionata o dell'intero percorso nel campo di modifica. Un utente può anche immettere un Universal Naming Convention (UNC) a un'unità senza lettera di unità. Se l'utente immette un segmento finale per il percorso non valido per il volume corrente, il controllo PathEdit non può trasferire lo stato attivo al controllo successivo.

I controlli PathEdit, [DirectoryCombo](directorycombo-control.md)e [DirectoryList](directorylist-control.md) sono associati alla stessa proprietà con valori stringa. Questa proprietà è il percorso selezionato dall'utente. Immettere il nome della proprietà nella colonna Proprietà della [tabella Control](control-table.md). Questa proprietà deve avere un valore iniziale contenente almeno un volume e un sottolivello. Specificare il valore iniziale per la proprietà nella colonna Valore della [tabella Proprietà](property-table.md).

Questo controllo deve essere usato in una finestra [di dialogo sfoglia](browse-dialog.md) insieme ai controlli PathEdit e [DirectoryList.](directorylist-control.md)

## <a name="control-attributes"></a>Attributi del controllo

Con questo controllo è possibile usare gli attributi seguenti. Per modificare il valore di un attributo usando un evento , sottoscrivere il controllo a un oggetto ControlEvent nella tabella [EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna Attribute . Immettere l'identificatore di ControlEvent nella colonna Event .



| Identificatore dell'attributo                                               | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Nome di una proprietà indiretta associata al controllo. Se il bit dell'attributo indiretto è impostato, il controllo visualizza o modifica il valore della proprietà con questo nome. Se il bit dell'attributo indiretto è impostato, questo nome è anche il valore della proprietà elencata nella colonna Proprietà della [tabella Control](control-table.md).                                                                                                                                                                              |
| [Position](position-control-attribute.md)                         |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella Control](control-table.md). Usare le [unità del programma](installer-units.md) di installazione per lunghezza e distanza.<br/>                                                                                                                                                                                                                                   |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Nome della proprietà associata a questo controllo. Se il bit dell'attributo indiretto non è impostato, il controllo visualizza o modifica il valore della proprietà con questo nome. Questo attributo viene specificato nella colonna Proprietà della [tabella Control](control-table.md).                                                                                                                                                                                                                                              |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valore corrente della proprietà visualizzata o modificata da questo controllo. Se il bit dell'attributo indiretto non è impostato, questo è il valore di PropertyName. Se il bit dell'attributo indiretto è impostato, questo è il valore di IndirectPropertyName. Se l'attributo viene modificato, il controllo riflette il nuovo valore.                                                                                                                                                                                                                                 |
| [Text](text-control-attribute.md)                                 |                                  | Per impostare il tipo di carattere e lo stile del carattere di una stringa di testo, antessare alla stringa di caratteri visualizzati { style} o \\ {&style}. Dove style è un identificatore elencato nella colonna TextStyle della [tabella TextStyle](textstyle-table.md). Se nessuna di queste proprietà è presente, ma la [**proprietà DefaultUIFont**](defaultuifont.md) è definita come stile di testo valido, verrà usato tale tipo di carattere. Per specificare il numero di caratteri che l'utente può immettere, aggiungere {n} dopo le specifiche del tipo di carattere, dove n è un numero intero positivo.<br/> |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola di bit della colonna Attributes nella tabella [Control](control-table.md) per rendere il controllo visibile o nascosto al momento della creazione.<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                           |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Controllo in uno stato disabilitato. Controllo in uno stato abilitato.<br/> Includere questo bit nella parola di bit nella colonna Attributi del [controllo](control-table.md) per abilitare il controllo al momento della creazione.<br/> È anche possibile abilitare o disabilitare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                         |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto 3D incassato.<br/> Includere questi bit nella parola di bit nella colonna Attributi della [tabella Control](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                  |
| [Indiretto](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | Il controllo visualizza o modifica il valore della proprietà nella colonna Proprietà della [tabella Control](control-table.md). Il controllo visualizza o modifica il valore della proprietà con l'identificatore elencato nella colonna Proprietà della tabella Control.<br/> Determina se alla proprietà associata a questo controllo viene fatto riferimento indirettamente.<br/>                                                                                                                                                       |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | Il testo nel controllo viene visualizzato in ordine di lettura da sinistra a destra. Il testo nel controllo viene visualizzato in ordine di lettura da destra a sinistra.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | Il testo nel controllo è allineato a sinistra. Il testo nel controllo è allineato a destra.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Commenti

Il controllo PathEdit deriva dal [controllo Edit.](edit-control.md)

Per compatibilità con le utilità per la lettura dello schermo, quando si crea una finestra di dialogo con un controllo PathEdit come primo controllo attivo, è necessario impostare il campo di testo appartenente al campo di modifica come primo controllo attivo nella tabella [Dialog](dialog-table.md). Poiché il testo statico non può assumere lo stato attivo, quando viene creata la finestra di dialogo, il campo di modifica avrà inizialmente lo stato attivo come previsto; ciò garantisce che le utilità per la lettura dello schermo mostrino le informazioni corrette.

 

 




