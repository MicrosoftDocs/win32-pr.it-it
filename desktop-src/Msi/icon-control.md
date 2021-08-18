---
description: Il controllo Icona visualizza un'immagine statica di un'icona. Lo sfondo dell'immagine è trasparente.
ms.assetid: a2d19093-73d0-4e1f-bf82-21e7334a3f34
title: Controllo Icon (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce6d1dca9e6664018a0c7a36c9b44f3b5a0b6310bc8c6d18309b73649fa9240
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996711"
---
# <a name="icon-control"></a>Controllo Icona

Il controllo Icona visualizza un'immagine statica di un'icona. Lo sfondo dell'immagine è trasparente.

## <a name="control-attributes"></a>Attributi del controllo

Con questo controllo è possibile usare gli attributi seguenti. Per modificare il valore di un attributo usando un evento, sottoscrivere il controllo a un ControlEvent nella tabella [EventMapping](eventmapping-table.md) ed elencare l'identificatore dell'attributo nella colonna Attribute. Immettere l'identificatore di ControlEvent nella colonna Evento.



| Identificatore dell'attributo                         | Bit esadecimale                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)   |                                                                              | Posizione del controllo nella finestra di dialogo. Immettere la larghezza, l'altezza e le coordinate dell'angolo sinistro del controllo nelle colonne Width, Height, X e Y della [tabella Control](control-table.md). Usare le [unità di installazione](installer-units.md) per lunghezza e distanza.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [Text](text-control-attribute.md)           |                                                                              | Contiene il nome di un'icona archiviata nella [tabella binaria](binary-table.md). Per visualizzare un'icona archiviata nella tabella Binary, immettere il nome del record dell'immagine visualizzato nella tabella Binary nella colonna Text del record della tabella [Control](control-table.md) per questo controllo.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [Visible](visible-control-attribute.md)     | 0x00000000 0x00000001<br/>                                             | Controllo nascosto. Controllo visibile.<br/> Includere questo bit nella parola di bit della colonna Attributes nella tabella [Control](control-table.md) per rendere il controllo visibile o nascosto al momento della creazione.<br/> È anche possibile nascondere o visualizzare un controllo usando la [tabella ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                                                                                                                                                         |
| [Sunken](sunken-control-attribute.md)       | 0x00000000 0x00000004<br/>                                             | Visualizza lo stile di visualizzazione predefinito. Visualizza il controllo con un aspetto 3D incassato.<br/> Includere questi bit nella parola di bit nella colonna Attributi della [tabella Control](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [Dimensione fissa](fixedsize-control-attribute.md) | 0x00000000 0x00100000<br/>                                             | Estende l'immagine dell'icona per adattarla al controllo. Ritaglia o centra l'immagine dell'icona nel controllo.<br/> Includere questo bit nella parola di bit della colonna Attributes della [tabella Control](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [IconSize](iconsize-control-attribute.md)   | 0x00000000 0x00200000<br/> 0x00400000<br/> 0x00600000<br/> | Carica la prima immagine. Carica la prima immagine 16x16.<br/> Carica la prima immagine 32x32.<br/> Carica la prima immagine 48x48.<br/> Un file di icona può contenere immagini di dimensioni diverse della stessa icona. Includere il valore della parola di bit appropriata nella colonna Attributi della [tabella Control](control-table.md)<br/> Se questi bit non sono impostati, il programma di installazione ignora l'attributo FixedSize e l'immagine viene adattata al rettangolo di controllo. Se entrambi i bit IconSize e FixedSize sono impostati, un'immagine più piccola del controllo viene centrata e un'immagine è più grande del controllo per adattarla.<br/> |



 

## <a name="remarks"></a>Commenti

Questo controllo può essere creato dalla classe STATIC usando la [**funzione CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Include gli stili **SS \_ ICON,** **SS \_ CENTERIMAGE,** **WS \_ CHILD** e **WS \_ GROUP.**

 

 
