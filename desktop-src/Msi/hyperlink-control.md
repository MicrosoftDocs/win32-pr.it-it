---
description: Il controllo Collegamento ipertestuale visualizza un collegamento HTML a un indirizzo, che viene aperto nel browser predefinito per il computer.
ms.assetid: 06678b10-0915-4649-b917-ec90c40d5160
title: Controllo Collegamento ipertestuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce515b64a518012ea187eb2c3a933e653b1ea5cf99b316028f9cfe3b397c5f96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129461"
---
# <a name="hyperlink-control"></a>Controllo Collegamento ipertestuale

Il controllo Collegamento ipertestuale visualizza un collegamento HTML a un indirizzo, che viene aperto nel browser predefinito per il computer. I collegamenti non sono supportati per protocolli diversi da HTML.

**[Windows Installer 4.5 o versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato. Questo controllo è disponibile a partire da Windows Installer 5.0.

Il valore Text del controllo HyperLink usa il tag di ancoraggio e il valore dell'attributo HREF per specificare l'URL e il <a> testo visualizzato del collegamento.

``` syntax
[Blue Yonder Airlines](https://www.blueyonderairlines.com)
```

## <a name="control-attributes"></a>Attributi del controllo

È possibile usare gli attributi seguenti con il controllo Collegamento ipertestuale. Per modificare il valore di un attributo usando un evento , sottoscrivere il controllo a un oggetto ControlEvent nella tabella [EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna Attribute . Immettere l'identificatore di ControlEvent nella colonna Event .



| Identificatore dell'attributo                             | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)       |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella Control](control-table.md) o [BBControl](bbcontrol-table.md). Usare le [unità del programma](installer-units.md) di installazione per lunghezza e distanza.<br/>                                                                                                                                                                       |
| [Text](text-control-attribute.md)               |                                  | Testo visualizzato dal controllo . Per impostare il tipo di carattere e lo stile del carattere di una stringa di testo, antessare alla stringa di caratteri visualizzati { style} o \\ {&style}. Dove style è un identificatore elencato nella colonna TextStyle della [tabella TextStyle](textstyle-table.md). Se nessuna di queste proprietà è presente, ma la [**proprietà DefaultUIFont**](defaultuifont.md) è definita come stile di testo valido, verrà usato tale tipo di carattere. Il valore di testo risolverà anche \[ Property nella proprietà a cui si fa \] riferimento. <br/> |
| [Visible](visible-control-attribute.md)         | 0x00000000 0x00000001<br/> | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola di bit della colonna Attributes nella tabella [Control](control-table.md) o [BBControl per](bbcontrol-table.md)rendere il controllo visibile o nascosto al momento della creazione.<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>                                                                                                                           |
| [Enabled](enabled-control-attribute.md)         | 0x00000000 0x00000002<br/> | Controllo in uno stato disabilitato. Controllo in uno stato abilitato.<br/> Includere questo bit nella parola di bit nella colonna Attributi delle tabelle [Control](control-table.md) o [BBControl](bbcontrol-table.md) per abilitare il controllo durante la creazione.<br/> È anche possibile abilitare o disabilitare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>                                                                                                                        |
| [Sunken](sunken-control-attribute.md)           | 0x00000000 0x00000004<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto 3D incassato.<br/> Includere questi bit nella parola di bit nella colonna Attributi della [tabella Control](control-table.md).<br/>                                                                                                                                                                                                                                                                                            |
| [Modalità trasparente](transparent-control-attribute.md) | 0x00000000 0x00010000<br/> | Controllo opaco. Lo sfondo viene visualizzato tramite il controllo . Il controllo ha lo stile WS \_ EX \_ TRANSPARENT.<br/> Includere questo bit nella colonna Attributi delle tabelle [Control](control-table.md) [o BBControl](bbcontrol-table.md).<br/>                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Commenti

Questo controllo può essere creato dalla classe WC \_ LINK usando la funzione [**CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Include gli stili WS \_ CHILD, WS \_ TABSTOP e WS \_ GROUP.

Non posizionare i controlli [Text trasparenti](text-control.md) sopra le bitmap colorate. Il testo potrebbe non essere visibile se l'utente modifica la combinazione di colori di visualizzazione. Ad esempio, il testo può diventare invisibile se l'utente imposta il parametro di contrasto elevato per motivi di accessibilità.

Se il testo nel controllo è più lungo della larghezza del controllo, il testo viene a capo o troncato, a seconda che l'altezza sia sufficiente per adattarlo al testo a capo.

 

 
