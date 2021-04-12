---
description: Il controllo GroupBox visualizza un rettangolo, possibilmente con testo della didascalia, che serve per raggruppare altri controlli nella finestra di dialogo.
ms.assetid: e1cdcf71-876f-4115-96a4-95d8a0f61a9b
title: Controllo GroupBox (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5182284055d95719299b1fecb7dc3f7825176c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226614"
---
# <a name="groupbox-control"></a>Controllo GroupBox

Il controllo GroupBox visualizza un rettangolo, possibilmente con testo della didascalia, che serve per raggruppare altri controlli nella finestra di dialogo.

## <a name="control-attributes"></a>Attributi del controllo

Con il controllo GroupBox è possibile usare gli attributi seguenti. Per modificare il valore di un attributo utilizzando un evento, sottoscrivere il controllo in un ControlEvent nella [tabella EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna attributo. Immettere l'identificatore del ControlEvent nella colonna evento.



| Identificatore di attributo                               | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)         |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate del controllo dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella di controllo](control-table.md) o della [tabella BBControl](bbcontrol-table.md). Usare le [unità del programma di installazione](installer-units.md) per lunghezza e distanza.<br/>                                                                                                                         |
| [Text](text-control-attribute.md)                 |                                  | Visualizza una didascalia nell'angolo superiore sinistro del controllo. Per impostare il tipo di carattere e lo stile del carattere di una stringa di testo, anteporre alla stringa dei caratteri visualizzati lo stile { \\ Style} o {&Style}. Dove Style è un identificatore elencato nella colonna TextStyle della [tabella TextStyle](textstyle-table.md). Se nessuna di queste è presente, ma la proprietà [**DefaultUIFont**](defaultuifont.md) è definita come uno stile di testo valido, verrà usato tale tipo di carattere.<br/> |
| [Visible](visible-control-attribute.md)           | 0x00000001 0x00000000<br/> | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola bit della colonna attributi nella [tabella dei controlli](control-table.md) o nella [tabella BBControl](bbcontrol-table.md) per rendere il controllo visibile o nascosto alla sua creazione.<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>                                                                             |
| [Sunken](sunken-control-attribute.md)             | 0x00000004 0x00000000<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto incassato, 3D.<br/> Includere questi bit nella parola bit nella colonna attributi della [tabella dei controlli](control-table.md).<br/>                                                                                                                                                                                                                                               |
| [RTLRO](rtlro-control-attribute.md)               | 0x00000020 0x00000000<br/> | Il testo nel controllo viene visualizzato nell'ordine di lettura da sinistra a destra. Il testo nel controllo viene visualizzato in ordine di lettura da destra a sinistra.<br/>                                                                                                                                                                                                                                                                                                                |
| [RightAligned](rightaligned-control-attribute.md) | 0x00000040 0x00000000<br/> | Il testo nel controllo è allineato a sinistra. Il testo nel controllo è allineato a destra.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Commenti

Questo controllo può essere creato dalla classe BUTTON tramite la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Dispone degli stili **BS \_ GroupBox**, **WS \_ child** e **WS \_ Group** .

C'è sempre un divario tra la parte superiore della finestra del controllo e il frame visibile, anche in assenza di didascalie.

 

 
