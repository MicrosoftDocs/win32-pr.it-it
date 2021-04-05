---
description: Questo controllo Visualizza una stringa di testo lungo che non può essere interamente adatta alla pagina. Un uso comune di questo controllo è la visualizzazione del contratto di licenza.
ms.assetid: a49209f3-043c-4360-b1e3-9fa9538c2c9b
title: Controllo ScrollableText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ff807f2b0175eb411b3c45eb9d1e3b5eeaea01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881837"
---
# <a name="scrollabletext-control"></a>Controllo ScrollableText

Questo controllo Visualizza una stringa di testo lungo che non può essere interamente adatta alla pagina. Un uso comune di questo controllo è la visualizzazione del contratto di licenza.

Si noti che la stringa di testo utilizzata con questo controllo non può contenere una proprietà incorporata. Per visualizzare il testo con proprietà incorporate, usare invece il [controllo di testo](text-control.md).

## <a name="control-attributes"></a>Attributi del controllo

Con questo controllo è possibile usare gli attributi seguenti. Per modificare il valore di un attributo utilizzando un evento, sottoscrivere il controllo in un ControlEvent nella [tabella EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna attributo. Immettere l'identificatore del ControlEvent nella colonna evento.



| Identificatore di attributo                               | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)         |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate del controllo dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella di controllo](control-table.md) o della [tabella BBControl](bbcontrol-table.md). Usare le [unità del programma di installazione](installer-units.md) per lunghezza e distanza.<br/>                                            |
| [Text](text-control-attribute.md)                 |                                  | Testo visualizzato dal controllo. Immettere la stringa di testo RTF nella colonna di testo della [tabella dei controlli](control-table.md).                                                                                                                                                                                                                                                       |
| [Visible](visible-control-attribute.md)           | 0x00000001 0x00000000<br/> | Controllo nascosto. Controllo visibile.<br/> Per rendere visibile o nascosto il controllo durante la creazione, includere questo bit nella parola bit della colonna attributi nella [tabella di controllo](control-table.md) o nella [tabella BBControl](bbcontrol-table.md).<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/> |
| [Enabled](enabled-control-attribute.md)           | 0x00000002 0x00000000<br/> | Controllo in uno stato disabilitato. Controllo in uno stato abilitato.<br/> Includere questo bit nella colonna attributi delle tabelle [Control](control-table.md) o [BBControl](bbcontrol-table.md) per abilitare il controllo al momento della creazione.<br/> È anche possibile abilitare o disabilitare un controllo tramite la [tabella ControlCondition](controlcondition-table.md).<br/>             |
| [Sunken](sunken-control-attribute.md)             | 0x00000004 0x00000000<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizzare il controllo con un aspetto incassato, 3D.<br/> Includere questi bit nella parola bit nella colonna attributi della [tabella dei controlli](control-table.md).<br/>                                                                                                                                                                    |
| [RTLRO](rtlro-control-attribute.md)               | 0x00000020 0x00000000<br/> | Il testo nel controllo viene visualizzato in un ordine di lettura da sinistra a destra. Il testo nel controllo viene visualizzato in un ordine di lettura da destra a sinistra.<br/>                                                                                                                                                                                                                               |
| [RightAligned](rightaligned-control-attribute.md) | 0x00000040 0x00000000<br/> | Il testo nel controllo è allineato a sinistra. Il testo nel controllo è allineato a destra.<br/>                                                                                                                                                                                                                                                                            |
| [LeftScroll](leftscroll-control-attribute.md)     | 0x00000080 0x00000000<br/> | La barra di scorrimento si trova sul lato destro del controllo. La barra di scorrimento si trova sul lato sinistro del controllo.<br/>                                                                                                                                                                                                                                              |
| [BiDi](bidi-control-attribute.md)                 | 0x000000E0                       | Impostare questo valore per una combinazione degli attributi [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)e [LeftScroll](leftscroll-control-attribute.md) .                                                                                                                                                                               |



 

## <a name="remarks"></a>Commenti

Questo controllo può essere creato dalla classe RichEdit tramite la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Include gli stili **es \_ Multiline**, **WS \_ VSCROLL**, **es \_ ReadOnly**, **WS \_ TABSTOP**, **es \_ AUTOVSCROLL**, **WS \_ child**, **WS \_ Group** ed **es \_ NOOLEDRAGDROP** .

 

 
