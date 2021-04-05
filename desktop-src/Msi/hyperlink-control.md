---
description: Il controllo HyperLink Visualizza un collegamento HTML a un indirizzo, che viene aperto nel browser predefinito del computer.
ms.assetid: 06678b10-0915-4649-b917-ec90c40d5160
title: Controllo collegamento ipertestuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d074efa00fcf51fec979d9df07f1854631279d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882953"
---
# <a name="hyperlink-control"></a>Controllo collegamento ipertestuale

Il controllo HyperLink Visualizza un collegamento HTML a un indirizzo, che viene aperto nel browser predefinito del computer. I collegamenti non sono supportati per i protocolli diversi da HTML.

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato. Questo controllo è disponibile a partire da Windows Installer 5,0.

Il valore di testo del controllo collegamento ipertestuale usa il <a> tag anchor e il valore dell'attributo href per specificare l'URL e il testo visualizzato del collegamento.

``` syntax
[Blue Yonder Airlines](https://www.blueyonderairlines.com)
```

## <a name="control-attributes"></a>Attributi del controllo

Con il controllo HyperLink è possibile usare gli attributi seguenti. Per modificare il valore di un attributo utilizzando un evento, sottoscrivere il controllo in un ControlEvent nella [tabella EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna attributo. Immettere l'identificatore del ControlEvent nella colonna evento.



| Identificatore di attributo                             | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)       |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate del controllo dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella di controllo](control-table.md) o della [tabella BBControl](bbcontrol-table.md). Usare le [unità del programma di installazione](installer-units.md) per lunghezza e distanza.<br/>                                                                                                                                                                       |
| [Text](text-control-attribute.md)               |                                  | Testo visualizzato dal controllo. Per impostare il tipo di carattere e lo stile del carattere di una stringa di testo, anteporre alla stringa dei caratteri visualizzati lo stile { \\ Style} o {&Style}. Dove Style è un identificatore elencato nella colonna TextStyle della [tabella TextStyle](textstyle-table.md). Se nessuna di queste è presente, ma la proprietà [**DefaultUIFont**](defaultuifont.md) è definita come uno stile di testo valido, verrà usato tale tipo di carattere. Il valore di testo risolverà \[ anche \] la proprietà nella proprietà a cui si fa riferimento. <br/> |
| [Visible](visible-control-attribute.md)         | 0x00000001 0x00000000<br/> | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola bit della colonna attributi nella [tabella dei controlli](control-table.md) o nella [tabella BBControl](bbcontrol-table.md). per rendere il controllo visibile o nascosto alla sua creazione.<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>                                                                                                                           |
| [Enabled](enabled-control-attribute.md)         | 0x00000002 0x00000000<br/> | Controllo in uno stato disabilitato. Controllo in uno stato abilitato.<br/> Includere questo bit nella parola bit nella colonna attributi delle tabelle [Control](control-table.md) o [BBControl](bbcontrol-table.md) per abilitare il controllo alla creazione.<br/> È anche possibile abilitare o disabilitare un controllo tramite la [tabella ControlCondition](controlcondition-table.md).<br/>                                                                                                                        |
| [Sunken](sunken-control-attribute.md)           | 0x00000004 0x00000000<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto incassato, 3D.<br/> Includere questi bit nella parola bit nella colonna attributi della [tabella dei controlli](control-table.md).<br/>                                                                                                                                                                                                                                                                                            |
| [Modalità trasparente](transparent-control-attribute.md) | 0x00010000 0x00000000<br/> | Controllo opaco. Lo sfondo viene visualizzato tramite il controllo. Il controllo ha lo stile WS- \_ \_ Transparent.<br/> Includere questo bit nella colonna attributi delle tabelle [Control](control-table.md) o [BBControl](bbcontrol-table.md).<br/>                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Commenti

Questo controllo può essere creato dalla \_ classe di collegamento WC usando la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Dispone degli stili WS \_ child, WS \_ TABSTOP e WS \_ Group.

Non posizionare [controlli testo](text-control.md) trasparenti su bitmap colorate. Il testo potrebbe non essere visibile se l'utente modifica la combinazione di colori di visualizzazione. Ad esempio, il testo potrebbe diventare invisibile se l'utente imposta il parametro a contrasto elevato per motivi di accessibilità.

Se il testo nel controllo supera la larghezza del controllo, il testo viene incapsulato o troncato, a seconda che l'altezza sia sufficiente per adattarsi al testo di cui è stato eseguito il wrapping.

 

 
