---
description: La tabella delle finestre di dialogo contiene tutte le finestre di dialogo visualizzate nell'interfaccia utente in modalità completa e ridotta.
ms.assetid: 981386dd-4fee-4003-8c62-16933cc5bd14
title: Tabella delle finestre di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554bc551b41a7ebeaa8b63b2a0d1b74a0f55cfb1d7a087936a394a060286caba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692841"
---
# <a name="dialog-table"></a>Tabella delle finestre di dialogo

La tabella delle finestre di dialogo contiene tutte le finestre di dialogo visualizzate nell'interfaccia utente in modalità completa e ridotta.

La tabella delle finestre di dialogo include le colonne seguenti.



| Colonna           | Tipo                               | Chiave | Nullable |
|------------------|------------------------------------|-----|----------|
| Finestra di dialogo           | [Identificatore](identifier.md)       | S   | N        |
| HCentering       | [Integer](integer.md)             | N   | N        |
| VCentering       | [Integer](integer.md)             | N   | N        |
| Larghezza            | [Integer](integer.md)             | N   | N        |
| Altezza           | [Integer](integer.md)             | N   | N        |
| Attributi       | [DoubleInteger](doubleinteger.md) | N   | S        |
| Titolo            | [Formattato](formatted.md)         | N   | S        |
| Control \_ First   | [Identificatore](identifier.md)       | N   | N        |
| Impostazione \_ predefinita del controllo | [Identificatore](identifier.md)       | N   | S        |
| Annullamento \_ del controllo  | [Identificatore](identifier.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Dialog"></span><span id="dialog"></span><span id="DIALOG"></span>Dialogo
</dt> <dd>

Chiave primaria e nome della finestra di dialogo.

</dd> <dt>

<span id="HCentering"></span><span id="hcentering"></span><span id="HCENTERING"></span>HCentering
</dt> <dd>

Posizione orizzontale della finestra di dialogo.

L'intervallo è compreso tra 0 e 100, con 0 sul bordo sinistro dello schermo e 100 sul bordo destro.

</dd> <dt>

<span id="VCentering"></span><span id="vcentering"></span><span id="VCENTERING"></span>VCentering
</dt> <dd>

Posizione verticale della finestra di dialogo.

L'intervallo è compreso tra 0 e 100, con 0 nel bordo superiore dello schermo e 100 nel bordo inferiore.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Larghezza
</dt> <dd>

Larghezza del limite rettangolare della finestra di dialogo.

Questo numero deve essere non negativo.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Altezza
</dt> <dd>

Altezza del limite rettangolare della finestra di dialogo.

Questo numero deve essere non negativo.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributi
</dt> <dd>

Parola a 32 bit che specifica i flag di attributo da applicare a questa finestra di dialogo.

Questo numero deve essere non negativo. Per altre informazioni, vedere [Bit di stile della finestra di dialogo.](dialog-style-bits.md)

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Titolo
</dt> <dd>

Stringa di testo localizzabile che specifica il titolo da visualizzare nella barra del titolo della finestra di dialogo.

</dd> <dt>

<span id="Control_First"></span><span id="control_first"></span><span id="CONTROL_FIRST"></span>Control \_ First
</dt> <dd>

Chiave esterna alla seconda colonna della tabella [di controllo](control-table.md).

Combinando questo campo con il campo Dialog [](control-table.md) viene specificato un controllo univoco nella tabella di controllo che assume lo stato attivo all'apertura della finestra di dialogo. In genere, può trattarsi di un [controllo Edit,](edit-control.md) [selectionTree Control](selectiontree-control.md)o qualsiasi altro controllo che può spostare lo stato attivo. Se il [controllo PushButton](pushbutton-control.md) è l'unico controllo presente nella finestra di dialogo che può spostare lo stato attivo, anche il controllo PushButton immesso nel campo ControlDefault deve essere immesso nel campo Control First. Questa colonna viene ignorata in una [finestra di dialogo di](error-dialog.md) errore.

Poiché il testo statico non [](text-control.md) può assumere lo stato attivo, un controllo Di testo che descrive un controllo [Edit,](edit-control.md) [pathEdit Control,](pathedit-control.md) [ListView Control,](listview-control.md) [ComboBox Control](combobox-control.md) o [VolumeSelectCombo Control](volumeselectcombo-control.md) deve essere il primo controllo nella finestra di dialogo per garantire la compatibilità con le utilità per la lettura dello schermo.

</dd> <dt>

<span id="Control_Default"></span><span id="control_default"></span><span id="CONTROL_DEFAULT"></span>Impostazione \_ predefinita del controllo
</dt> <dd>

Chiave esterna alla seconda colonna della tabella [di controllo](control-table.md).

La combinazione di questo campo con il campo Finestra di dialogo specifica il controllo predefinito che assume lo stato attivo all'apertura della finestra di dialogo. In genere, può trattarsi di [un controllo PushButton.](pushbutton-control.md) Se nessun controllo PushButton nella finestra di dialogo ha lo stato attivo, il tasto INVIO equivale a fare clic sul controllo predefinito. Se questa colonna viene lasciata vuota, non è presente alcun controllo predefinito. Questa colonna viene ignorata in una [finestra di dialogo di](error-dialog.md) errore.

</dd> <dt>

<span id="Control_Cancel"></span><span id="control_cancel"></span><span id="CONTROL_CANCEL"></span>Annullamento \_ del controllo
</dt> <dd>

Chiave esterna alla seconda colonna della tabella [di controllo](control-table.md).

Combinando questo campo con il campo Dialog viene specificato un controllo che annulla l'installazione. Questo controllo è associato agli eventi nella tabella [ControlEvent usata](controlevent-table.md) per annullare l'installazione. Premere ESC o fare clic sul pulsante Chiudi equivale a fare clic sul controllo Annulla. Questa colonna viene ignorata in una finestra [di dialogo di errore](error-dialog.md)

.

Il controllo di annullamento viene nascosto durante il rollback o la rimozione dei file di cui è stato eseguito il backup. Il gestore dell'interfaccia utente interno nasconde il controllo alla ricezione di un messaggio INSTALLMESSAGE \_ COMMONDATA.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori interi per larghezza e altezza si trova nelle unità del programma [di installazione,](installer-units.md)non nelle unità di finestra di dialogo.

I due valori di centratura vengono ignorati per le finestre di dialogo successive in una sequenza della procedura guidata. Le posizioni delle finestre di dialogo vengono impostate dall'utente o come per la finestra di dialogo precedente. Queste sequenze di finestre di dialogo vengono create da [un oggetto NewDialog ControlEvent.](newdialog-controlevent.md)

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE13](ice13.md)  
[ICE20](ice20.md)  
[ICE23](ice23.md)  
[ICE27](ice27.md)  
[ICE32](ice32.md)  
[ICE44](ice44.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
</dl>

 

 



