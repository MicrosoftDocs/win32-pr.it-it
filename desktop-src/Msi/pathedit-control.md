---
description: Il controllo PathEdit Visualizza un campo di modifica che consente a un utente di selezionare la sezione finale di un percorso.
ms.assetid: 074ef4d5-3ac1-4bdb-90c5-9798d89a749f
title: Controllo PathEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65d1237199f202e6c674ab4526ccd4747b02c09b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231539"
---
# <a name="pathedit-control"></a>Controllo PathEdit

Il controllo PathEdit Visualizza un campo di modifica che consente a un utente di selezionare la sezione finale di un percorso. Questo controllo supporta l'immissione del nome della cartella selezionata o l'intero percorso nel campo di modifica. Un utente può anche immettere un percorso di Universal Naming Convention (UNC) per un'unità senza lettera di unità. Se l'utente immette un segmento finale per il percorso non valido per il volume presente, il controllo PathEdit non può trasferire lo stato attivo al controllo successivo.

I controlli PathEdit, [DirectoryCombo](directorycombo-control.md)e [directory](directorylist-control.md) sono associati alla stessa proprietà con valori di stringa. Tale proprietà è il percorso selezionato dall'utente. Immettere il nome della proprietà nella colonna proprietà della tabella dei [controlli](control-table.md). Questa proprietà deve avere un valore iniziale contenente almeno un volume e un sottolivello. Specificare il valore iniziale per la proprietà nella colonna valore della tabella delle [Proprietà](property-table.md).

Questo controllo è destinato a essere utilizzato in una [finestra di dialogo di esplorazione](browse-dialog.md) insieme ai controlli PathEdit e [directory](directorylist-control.md) .

## <a name="control-attributes"></a>Attributi del controllo

Con questo controllo è possibile usare gli attributi seguenti. Per modificare il valore di un attributo utilizzando un evento, sottoscrivere il controllo in un ControlEvent nella [tabella EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna attributo. Immettere l'identificatore del ControlEvent nella colonna evento.



| Identificatore di attributo                                               | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | Si tratta del nome di una proprietà indiretta associata al controllo. Se viene impostato il bit di attributo indiretto, il controllo Visualizza o modifica il valore della proprietà con questo nome. Se viene impostato il bit di attributo indiretto, questo nome è anche il valore della proprietà elencata nella colonna proprietà della [tabella dei controlli](control-table.md).                                                                                                                                                                              |
| [Position](position-control-attribute.md)                         |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate del controllo dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella del controllo](control-table.md). Usare le [unità del programma di installazione](installer-units.md) per lunghezza e distanza.<br/>                                                                                                                                                                                                                                   |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | Si tratta del nome della proprietà associata a questo controllo. Se il bit di attributo indiretto non è impostato, il controllo Visualizza o modifica il valore della proprietà con questo nome. Questo attributo viene specificato nella colonna proprietà della tabella dei [controlli](control-table.md).                                                                                                                                                                                                                                              |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Valore corrente della proprietà visualizzata o modificata da questo controllo. Se il bit di attributo indiretto non è impostato, questo è il valore di PropertyName. Se viene impostato il bit di attributo indiretto, questo è il valore di IndirectPropertyName. Se l'attributo viene modificato, il controllo riflette il nuovo valore.                                                                                                                                                                                                                                 |
| [Text](text-control-attribute.md)                                 |                                  | Per impostare il tipo di carattere e lo stile del carattere di una stringa di testo, anteporre alla stringa dei caratteri visualizzati lo stile { \\ Style} o {&Style}. Dove Style è un identificatore elencato nella colonna TextStyle della [tabella TextStyle](textstyle-table.md). Se nessuna di queste è presente, ma la proprietà [**DefaultUIFont**](defaultuifont.md) è definita come uno stile di testo valido, verrà usato tale tipo di carattere. Per specificare il numero di caratteri che l'utente può immettere, accodare {n} dopo le specifiche del tipo di carattere, dove n è un numero intero positivo.<br/> |
| [Visible](visible-control-attribute.md)                           | 0x00000001 0x00000000<br/> | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola bit della colonna attributi nella [tabella dei controlli](control-table.md) per rendere il controllo visibile o nascosto alla sua creazione.<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                           |
| [Enabled](enabled-control-attribute.md)                           | 0x00000002 0x00000000<br/> | Controllo in uno stato disabilitato. Controllo in uno stato abilitato.<br/> Includere questo bit nella parola bit nella colonna attributi del [controllo](control-table.md) per abilitare il controllo alla creazione.<br/> È anche possibile abilitare o disabilitare un controllo tramite la [tabella ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                         |
| [Sunken](sunken-control-attribute.md)                             | 0x00000004 0x00000000<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto incassato, 3D.<br/> Includere questi bit nella parola bit nella colonna attributi della [tabella dei controlli](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                  |
| [Indiretto](indirect-control-attribute.md)                         | 0x00000008 0x00000000<br/> | Il controllo Visualizza o modifica il valore della proprietà nella colonna proprietà della [tabella dei controlli](control-table.md). Il controllo Visualizza o modifica il valore della proprietà con l'identificatore elencato nella colonna proprietà della tabella dei controlli.<br/> Determina se viene fatto riferimento indirettamente alla proprietà associata a questo controllo.<br/>                                                                                                                                                       |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000020 0x00000000<br/> | Il testo nel controllo viene visualizzato nell'ordine di lettura da sinistra a destra. Il testo nel controllo viene visualizzato in ordine di lettura da destra a sinistra.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000040 0x00000000<br/> | Il testo nel controllo è allineato a sinistra. Il testo nel controllo è allineato a destra.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Commenti

Il controllo PathEdit è derivato dal controllo di [modifica](edit-control.md) .

Per la compatibilità con utilità per la lettura dello schermo, quando si crea una finestra di dialogo con un controllo PathEdit come primo controllo attivo, è necessario fare in modo che il campo di testo appartenga al campo Edit il primo controllo attivo nella [tabella della finestra di dialogo](dialog-table.md). Poiché il testo statico non può avere lo stato attivo, quando viene creata la finestra di dialogo, il campo di modifica avrà lo stato attivo inizialmente come previsto. in questo modo si garantisce che le informazioni vengano visualizzate dalle utilità di lettura dello schermo.

 

 




