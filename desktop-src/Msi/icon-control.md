---
description: Il controllo icona Visualizza un'immagine statica di un'icona. Lo sfondo dell'immagine è trasparente.
ms.assetid: a2d19093-73d0-4e1f-bf82-21e7334a3f34
title: Controllo icona (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a9bf90697ff3a839c1953918179fb8cf41f2809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525170"
---
# <a name="icon-control"></a>Controllo Icon

Il controllo icona Visualizza un'immagine statica di un'icona. Lo sfondo dell'immagine è trasparente.

## <a name="control-attributes"></a>Attributi del controllo

Con questo controllo è possibile usare gli attributi seguenti. Per modificare il valore di un attributo utilizzando un evento, sottoscrivere il controllo in un ControlEvent nella [tabella EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna attributo. Immettere l'identificatore del ControlEvent nella colonna evento.



| Identificatore di attributo                         | Bit esadecimale                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)   |                                                                              | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate del controllo dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella del controllo](control-table.md). Usare le [unità del programma di installazione](installer-units.md) per lunghezza e distanza.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [Text](text-control-attribute.md)           |                                                                              | Contiene il nome di un'icona archiviata nella [tabella binaria](binary-table.md). Per visualizzare un'icona archiviata nella tabella binaria, immettere il nome del record dell'immagine visualizzato nella tabella binaria nella colonna di testo del record della [tabella dei controlli](control-table.md) per questo controllo.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [Visible](visible-control-attribute.md)     | 0x00000001 0x00000000<br/>                                             | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola bit della colonna attributi nella [tabella dei controlli](control-table.md) per rendere il controllo visibile o nascosto alla sua creazione.<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                                                                                                                                                         |
| [Sunken](sunken-control-attribute.md)       | 0x00000004 0x00000000<br/>                                             | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto incassato, 3D.<br/> Includere questi bit nella parola bit nella colonna attributi della [tabella dei controlli](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [FixedSize](fixedsize-control-attribute.md) | 0x00100000 0x00000000<br/>                                             | Estende l'immagine dell'icona per adattarla al controllo. Coltiva o Centra l'immagine dell'icona nel controllo.<br/> Includere questo bit nella parola bit della colonna Attributes della tabella dei [controlli](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [IconSize](iconsize-control-attribute.md)   | 0x00200000 0x00000000<br/> 0x00400000<br/> 0x00600000<br/> | Carica la prima immagine. Carica la prima immagine di 16x16.<br/> Carica la prima immagine di 32x32.<br/> Carica la prima immagine di 48x48.<br/> Un file di icona può contenere immagini con dimensioni diverse della stessa icona. Includere il valore della parola di bit appropriata nella colonna attributi della tabella dei [controlli](control-table.md)<br/> Se questi bit non sono impostati, il programma di installazione ignora l'attributo FixedSize e l'immagine viene adattata al rettangolo del controllo. Se entrambi i bit IconSize e FixedSize sono impostati, un'immagine più piccola del controllo viene centrata e un'immagine è più grande del controllo che viene compattato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo controllo può essere creato dalla classe statica tramite la funzione [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Dispone degli stili **\_ icona SS**, **SS \_ CENTERIMAGE**, **WS \_ child** e **WS \_ Group** .

 

 
