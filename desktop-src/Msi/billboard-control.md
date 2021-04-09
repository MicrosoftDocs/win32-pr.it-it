---
description: Il controllo Billboard Visualizza i controlli di uso comune che vengono aggiunti e rimossi dalla finestra di dialogo ControlEvents.
ms.assetid: c4c0ed5a-2518-499f-805f-dcbe0b0f9393
title: Controllo Billboard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e056a764ec4a71c3ce6785acf331b4bc1ff95ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881093"
---
# <a name="billboard-control"></a>Controllo Billboard

Il controllo Billboard Visualizza i controlli di uso comune che vengono aggiunti e rimossi dalla finestra di dialogo ControlEvents. Solo i controlli che non sono associati a una proprietà, ad esempio [testo](text-control.md), [bitmap](bitmap-control.md)o [icona](icon-control.md)o controlli personalizzati, possono essere inseriti in un tabellone. I controlli Billboard visualizzano generalmente i messaggi di stato.

## <a name="control-attributes"></a>Attributi del controllo

Con il controllo Billboard è possibile usare gli attributi seguenti. Per modificare il valore di un attributo utilizzando un evento, sottoscrivere il controllo in un ControlEvent nella [tabella EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna attributo. Immettere l'identificatore del ControlEvent nella colonna evento.



| Identificatore di attributo                                 | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Billboardname](billboardname-control-attribute.md) |                                  | Nome del tabellone corrente. Immettere l'identificatore del tabellone nella colonna Billboard della [tabella BBControl](bbcontrol-table.md).<br/>                                                                                                                                                                            |
| [Position](position-control-attribute.md)           |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate del controllo dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella BBControl](bbcontrol-table.md). Usare le [unità del programma di installazione](installer-units.md) per lunghezza e distanza.<br/>                                |
| [Visible](visible-control-attribute.md)             | 0x00000001 0x00000000<br/> | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola bit della colonna attributi nella [tabella BBControl](bbcontrol-table.md) per rendere il controllo visibile o nascosto alla sua creazione.<br/> Nascondere o visualizzare un controllo tramite la [tabella ControlCondition](controlcondition-table.md).<br/> |
| [Sunken](sunken-control-attribute.md)               | 0x00000004 0x00000000<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto incassato, 3D.<br/> Includere questi bit nella parola bit nella colonna attributi della [tabella dei controlli](control-table.md).<br/>                                                                                                               |



 

## <a name="remarks"></a>Commenti

Questo controllo non ha una finestra propria.

I controlli Billboard visualizzati nell'interfaccia utente completa sono elencati nella [tabella Billboard](billboard-table.md).

I controlli che si trovano in un tabellone devono essere elencati nella [tabella BBControl](bbcontrol-table.md) anziché nella [tabella dei controlli](control-table.md).

 

 




