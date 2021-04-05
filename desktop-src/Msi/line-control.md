---
description: Il controllo linea è una linea orizzontale.
ms.assetid: 8b180b71-1e80-47c0-bb44-d5fcecabaed2
title: Controllo linea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba3b7374574e2a0087e7dae8d0ffa9f097be9f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755618"
---
# <a name="line-control"></a>Controllo linea

Il controllo linea è una linea orizzontale.

## <a name="control-attributes"></a>Attributi del controllo

Con questo controllo è possibile usare gli attributi seguenti. Per modificare il valore di un attributo utilizzando un evento, sottoscrivere il controllo in un ControlEvent nella [tabella EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna attributo. Immettere l'identificatore del ControlEvent nella colonna evento.



| Identificatore di attributo                       | Bit esadecimale                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md) |                                  | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate del controllo dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella di controllo](control-table.md) o della [tabella BBControl](bbcontrol-table.md). Usare le [unità del programma di installazione](installer-units.md) per lunghezza e distanza.<br/>                                         |
| [Visible](visible-control-attribute.md)   | 0x00000001 0x00000000<br/> | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola bit della colonna attributi nella [tabella dei controlli](control-table.md) o nella [tabella BBControl](bbcontrol-table.md) per rendere il controllo visibile o nascosto alla sua creazione.<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/> |
| [Sunken](sunken-control-attribute.md)     | 0x00000004 0x00000000<br/> | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto incassato, 3D.<br/> Includere questi bit nella parola bit nella colonna attributi della [tabella dei controlli](control-table.md).<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Commenti

Questo controllo può essere creato dalla classe statica tramite la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Dispone degli stili **\_ incassati** **SS \_ ETCHEDHORZ** e SS.

 

 
