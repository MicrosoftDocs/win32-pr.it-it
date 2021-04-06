---
description: La tabella della finestra di dialogo contiene tutte le finestre di dialogo visualizzate nell'interfaccia utente in modalità completa e ridotta.
ms.assetid: 981386dd-4fee-4003-8c62-16933cc5bd14
title: Tabella finestra di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a210ad051eec950dcff8f8f940a1df11bf74c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882985"
---
# <a name="dialog-table"></a>Tabella finestra di dialogo

La tabella della finestra di dialogo contiene tutte le finestre di dialogo visualizzate nell'interfaccia utente in modalità completa e ridotta.

Nella tabella della finestra di dialogo sono presenti le colonne seguenti.



| Colonna           | Tipo                               | Chiave | Nullable |
|------------------|------------------------------------|-----|----------|
| Finestra di dialogo           | [Identificatore](identifier.md)       | S   | N        |
| HCentering       | [Integer](integer.md)             | N   | N        |
| VCenter       | [Integer](integer.md)             | N   | N        |
| Larghezza            | [Integer](integer.md)             | N   | N        |
| Altezza           | [Integer](integer.md)             | N   | N        |
| Attributi       | [DoubleInteger](doubleinteger.md) | N   | S        |
| Titolo            | [Formattato](formatted.md)         | N   | S        |
| \_Primo controllo   | [Identificatore](identifier.md)       | N   | N        |
| Controllo \_ predefinito | [Identificatore](identifier.md)       | N   | S        |
| \_Annulla controllo  | [Identificatore](identifier.md)       | N   | S        |



 

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

<span id="VCentering"></span><span id="vcentering"></span><span id="VCENTERING"></span>VCenter
</dt> <dd>

Posizione verticale della finestra di dialogo.

L'intervallo è compreso tra 0 e 100, con 0 sul bordo superiore dello schermo e 100 sul bordo inferiore.

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

Questo numero deve essere non negativo. Per altre informazioni, vedere [bit di stile della finestra di dialogo](dialog-style-bits.md).

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Titolo
</dt> <dd>

Stringa di testo localizzabile che specifica il titolo da visualizzare nella barra del titolo della finestra di dialogo.

</dd> <dt>

<span id="Control_First"></span><span id="control_first"></span><span id="CONTROL_FIRST"></span>\_Primo controllo
</dt> <dd>

Chiave esterna per la seconda colonna della tabella dei [controlli](control-table.md).

Combinando questo campo con il campo della finestra di dialogo viene specificato un controllo univoco nella [tabella dei controlli](control-table.md) che attiva quando viene aperta la finestra di dialogo. In genere, può trattarsi di un controllo di [modifica](edit-control.md), di un [controllo SelectionTree](selectiontree-control.md)o di qualsiasi altro controllo che può assumere lo stato attivo. Se il controllo [pulsante](pushbutton-control.md) è l'unico presente nella finestra di dialogo che può assumere lo stato attivo, è necessario immettere anche il pulsante immesso nel campo ControlDefault nel primo campo del controllo. Questa colonna viene ignorata in una finestra di [dialogo di errore](error-dialog.md) .

Poiché il testo statico non può avere lo stato attivo, un [controllo di testo](text-control.md) che descrive un controllo di [modifica](edit-control.md), un controllo [PathEdit](pathedit-control.md), un [controllo ListView](listview-control.md), un [controllo ComboBox](combobox-control.md) o un [controllo VolumeSelectCombo](volumeselectcombo-control.md) deve essere reso il primo controllo nella finestra di dialogo per garantire la compatibilità con le utilità per la lettura dello schermo.

</dd> <dt>

<span id="Control_Default"></span><span id="control_default"></span><span id="CONTROL_DEFAULT"></span>Controllo \_ predefinito
</dt> <dd>

Chiave esterna per la seconda colonna della tabella dei [controlli](control-table.md).

Combinando questo campo con il campo finestra di dialogo viene specificato il controllo predefinito che assume lo stato attivo quando viene aperta la finestra di dialogo. In genere, può trattarsi di un [controllo pulsante](pushbutton-control.md). Se nella finestra di dialogo non sono presenti controlli pulsante con lo stato attivo, la chiave restituita è equivalente a fare clic sul controllo predefinito. Se questa colonna viene lasciata vuota, non esiste alcun controllo predefinito. Questa colonna viene ignorata in una finestra di [dialogo di errore](error-dialog.md) .

</dd> <dt>

<span id="Control_Cancel"></span><span id="control_cancel"></span><span id="CONTROL_CANCEL"></span>\_Annulla controllo
</dt> <dd>

Chiave esterna per la seconda colonna della tabella dei [controlli](control-table.md).

Combinando questo campo con il campo finestra di dialogo viene specificato un controllo che annulla l'installazione. Questo controllo è associato agli eventi nella [tabella ControlEvent](controlevent-table.md) utilizzata per annullare l'installazione. Quando si preme il tasto ESC o si fa clic sul pulsante Chiudi è equivalente a fare clic sul controllo Cancel (Annulla). Questa colonna viene ignorata in una [finestra di dialogo di errore](error-dialog.md)

.

Il controllo Annulla è nascosto durante il rollback o la rimozione dei file di cui è stato eseguito il backup. Il gestore interno dell'interfaccia utente nasconde il controllo alla ricezione di un \_ messaggio INSTALLMESSAGE COMMONDATA.

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori integer per larghezza e altezza si trovano nelle [unità del programma di installazione](installer-units.md), non nelle unità di dialogo.

I due valori di centramento vengono ignorati per le finestre di dialogo successive in una sequenza della procedura guidata. Le posizioni della finestra di dialogo vengono impostate dall'utente o come per la finestra di dialogo precedente. Queste sequenze della finestra di dialogo vengono create da un [ControlEvent NewDialog](newdialog-controlevent.md).

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

 

 



